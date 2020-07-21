---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: ea9234bf666840e6b87dd9827747d11ef74eb4c7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884207"
---
# 0.9.430: ICoreWebView2Environment 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Environment
  : public IUnknown
```

Esto representa el entorno de WebView2.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[CreateCoreWebView2Host](#createcorewebview2host) | Cree de forma asincrónica una nueva vista de vista previa.
[CreateWebResourceResponse](#createwebresourceresponse) | Crear un nuevo objeto de respuesta de recursos Web.
[get_BrowserVersionInfo](#get_browserversioninfo) | Información de versión del explorador del [ICoreWebView2Environment]()actual, incluido el nombre del canal si no es el canal estable.
[add_NewBrowserVersionAvailable](#add_newbrowserversionavailable) | El evento NewBrowserVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.
[remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable) | Quitar un controlador de eventos agregado previamente con add_NewBrowserVersionAvailable.

Las vistas web creadas a partir de un entorno se ejecutan en el proceso del explorador especificado con los parámetros de entorno y los objetos creados a partir de un entorno se deben usar en el mismo entorno. No se garantiza que su uso en diferentes entornos sea compatible y podría fallar.

## Miembros

#### CreateCoreWebView2Host 

Cree de forma asincrónica una nueva vista de vista previa.

> [CREATECOREWEBVIEW2HOST](#createcorewebview2host)HRESULT público (HWND ParentWindow,[ICoreWebView2CreateCoreWebView2HostCompletedHandler](ICoreWebView2CreateCoreWebView2HostCompletedHandler.md) * handler)

parentWindow es el HWND en el que se debe mostrar la vista en la vista previa y desde la que se recibe la entrada. La vista en WebView agregará una ventana secundaria a la ventana proporcionada durante la creación de WebView. El orden Z y otros elementos afectados por el orden de ventanas relacionados se verán afectados según corresponda.

Se recomienda que el identificador de modelo de usuario de la aplicación conjunto de aplicaciones para el proceso o la ventana de la aplicación. Si no se establece ninguna, durante la creación de WebView un identificador de modelo de usuario de aplicación generado se establece en la ventana raíz de parentWindow. 

```cpp
// Create or recreate the WebView and its environment.
void AppWindow::InitializeWebView()
{
    // To ensure browser switches get applied correctly, we need to close
    // the existing WebView. This will result in a new browser process
    // getting created which will apply the browser switches.
    CloseWebView();

    LPCWSTR subFolder = nullptr;
    LPCWSTR additionalBrowserSwitches = nullptr;
    HRESULT hr = CreateCoreWebView2EnvironmentWithDetails(
        subFolder, nullptr, additionalBrowserSwitches,
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
    if (!SUCCEEDED(hr))
    {
        if (hr == HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND))
        {
            MessageBox(
                m_mainWindow,
                L"Couldn't find Edge installation. "
                "Do you have a version installed that's compatible with this "
                "WebView2 SDK version?",
                nullptr, MB_OK);
        }
        else
        {
            ShowFailure(hr, L"Failed to create webview environment");
        }
    }
}

// This is the callback passed to CreateWebViewEnvironmnetWithDetails.
// Here we simply create the WebView.
HRESULT AppWindow::OnCreateEnvironmentCompleted(
    HRESULT result, ICoreWebView2Environment* environment)
{
    CHECK_FAILURE(result);

    CHECK_FAILURE(environment->QueryInterface(IID_PPV_ARGS(&m_webViewEnvironment)));
        CHECK_FAILURE(m_webViewEnvironment->CreateCoreWebView2Host(
            m_mainWindow, Callback<ICoreWebView2CreateCoreWebView2HostCompletedHandler>(
                              this, &AppWindow::OnCreateCoreWebView2HostCompleted)
                              .Get()));
    return S_OK;
}
```

 Se recomienda que la aplicación se ocupe de los mensajes del administrador de reinicio para que se pueda reiniciar correctamente en el caso de que la aplicación esté usando Edge para WebView desde una instalación determinada y que la instalación se está desinstalando. Por ejemplo, si un usuario instala Edge desde el canal de desarrollo y opta por usar Edge de ese canal para probar la aplicación y, después, desinstala Edge de ese canal sin cerrar la aplicación, se reiniciará la aplicación para permitir que la desinstalación del canal de desarrollo se realice correctamente. 

```cpp
    case WM_QUERYENDSESSION:
    {
        // yes, we can shut down
        // Register how we might be restarted
        RegisterApplicationRestart(L"--restore", RESTART_NO_CRASH | RESTART_NO_HANG);
        *result = TRUE;
        return true;
    }
    break;
    case WM_ENDSESSION:
    {
        if (wParam == TRUE)
        {
            // save app state and exit.
            PostQuitMessage(0);
            return true;
        }
    }
    break;
```

#### CreateWebResourceResponse 

Crear un nuevo objeto de respuesta de recursos Web.

> [CREATEWEBRESOURCERESPONSE](#createwebresourceresponse)HRESULT público (IStream * Content, int STATUSCODE, LPCWSTR REASONPHRASE, LPCWSTR encabezados,[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) * * Response)

La cabecera es la cadena de encabezado de respuesta sin formato delimitada por newline. También es posible crear este objeto con una cadena de encabezados vacía y, a continuación, usar el [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) para construir los encabezados línea a línea. Para obtener información sobre otros parámetros, consulte [ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md).

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<ICoreWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### get_BrowserVersionInfo 

Información de versión del explorador del [ICoreWebView2Environment]()actual, incluido el nombre del canal si no es el canal estable.

> [get_BrowserVersionInfo](#get_browserversioninfo)de HRESULT público (LPWStr * versionInfo)

Coincide con el formato de la API de GetCoreWebView2BrowserVersionInfo. Los nombres de los canales son ' beta ', ' dev ' y ' Canarias '.

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

#### add_NewBrowserVersionAvailable 

El evento NewBrowserVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.

> [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)de HRESULT público ([ICoreWebView2NewBrowserVersionAvailableEventHandler](ICoreWebView2NewBrowserVersionAvailableEventHandler.md) * EventHandler, EventRegistrationToken * token)

Para usar la versión más reciente del explorador, debe crear un entorno y una vista Web nuevos. Este evento solo se activará para la nueva versión desde el mismo canal de borde desde el que se está ejecutando el código. Cuando no se esté ejecutando con Edge instalado, no se desencadenará ningún evento.

Puesto que una carpeta datos de usuario solo puede ser usada por un único proceso del explorador a la vez, si desea usar la misma carpeta datos de usuario en las vistas web con la nueva versión del explorador, debe cerrar primero el entorno y las vistas de web que usan la versión anterior del explorador. O simplemente pide al usuario que reinicie la aplicación.

```cpp
    // After the environment is successfully created,
    // register a handler for the NewBrowserVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewBrowserVersionAvailable(
        Callback<ICoreWebView2NewBrowserVersionAvailableEventHandler>(
            [this](
                ICoreWebView2Environment* sender,
                ICoreWebView2NewBrowserVersionAvailableEventArgs* args) -> HRESULT {
                // Get the version value from args
                wil::unique_cotaskmem_string newVersion;
                CHECK_FAILURE(args->get_NewVersion(&newVersion));
                std::wstring message = L"We detected there is a new version for the browser.";
                message += L"\n\nVersion number: ";
                message += newVersion.get();
                message += L"\n\n";
                if (m_webView)
                {
                    message += L"Do you want to restart the app? \n\n";
                    message += L"Click No if you only want to re-create the webviews. \n";
                    message += L"Click Cancel for no action. \n";
                }
                int response = MessageBox(
                    m_mainWindow, message.c_str(), L"New available version",
                    m_webView ? MB_YESNOCANCEL : MB_OK);

                if (response == IDYES)
                {
                    RestartApp();
                }
                else if (response == IDNO)
                {
                    ReinitializeWebViewWithNewBrowser();
                }
                else
                {
                    // do nothing
                }

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_NewBrowserVersionAvailable 

Quitar un controlador de eventos agregado previamente con add_NewBrowserVersionAvailable.

> [remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)de HRESULT público (token EventRegistrationToken)

