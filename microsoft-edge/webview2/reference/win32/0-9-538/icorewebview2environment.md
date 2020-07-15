---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2Environment
ms.openlocfilehash: a694411e8dbfd46c09895ce642a41b8a488d12dc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880090"
---
# interfaz ICoreWebView2Environment 

```
interface ICoreWebView2Environment
  : public IUnknown
```

Esto representa el entorno de WebView2.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[add_NewBrowserVersionAvailable](#add_newbrowserversionavailable) | El evento NewBrowserVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.
[CreateCoreWebView2Controller](#createcorewebview2controller) | Cree de forma asincrónica una nueva vista de vista previa.
[CreateWebResourceResponse](#createwebresourceresponse) | Crear un nuevo objeto de respuesta de recursos Web.
[get_BrowserVersionString](#get_browserversionstring) | Información de versión del explorador del [ICoreWebView2Environment]()actual, incluido el nombre del canal si no es el canal estable.
[remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable) | Quitar un controlador de eventos agregado previamente con add_NewBrowserVersionAvailable.

Las vistas web creadas a partir de un entorno se ejecutan en el proceso del explorador especificado con los parámetros de entorno y los objetos creados a partir de un entorno se deben usar en el mismo entorno. No se garantiza que su uso en diferentes entornos sea compatible y podría fallar.

## Miembros

#### add_NewBrowserVersionAvailable 

El evento NewBrowserVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.

> [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)de HRESULT público ([ICoreWebView2NewBrowserVersionAvailableEventHandler](icorewebview2newbrowserversionavailableeventhandler.md) * EventHandler, EventRegistrationToken * token)

Para usar la versión más reciente del explorador, debe crear un entorno y una vista Web nuevos. Este evento solo se activará para la nueva versión desde el mismo canal de borde desde el que se está ejecutando el código. Cuando no se esté ejecutando con Edge instalado, no se desencadenará ningún evento.

Puesto que una carpeta datos de usuario solo puede ser usada por un único proceso del explorador a la vez, si desea usar la misma carpeta datos de usuario en las vistas web con la nueva versión del explorador, debe cerrar primero el entorno y las vistas de web que usan la versión anterior del explorador. O simplemente pide al usuario que reinicie la aplicación.

```cpp
    // After the environment is successfully created,
    // register a handler for the NewBrowserVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewBrowserVersionAvailable(
        Callback<ICoreWebView2NewBrowserVersionAvailableEventHandler>(
            [this](ICoreWebView2Environment* sender, IUnknown* args) -> HRESULT {
                std::wstring message = L"We detected there is a new version for the browser.";
                if (m_webView)
                {
                    message += L"Do you want to restart the app \n\n";
                    message += L"Click No if you only want to re-create the webviews. \n";
                    message += L"Click Cancel for no action. \n";
                }
                int response = MessageBox(
                    m_mainWindow, message.c_str(), L"New available version",
                    m_webView  MB_YESNOCANCEL : MB_OK);

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

#### CreateCoreWebView2Controller 

Cree de forma asincrónica una nueva vista de vista previa.

> [CREATECOREWEBVIEW2CONTROLLER](#createcorewebview2controller)HRESULT público (HWND ParentWindow, [ICoreWebView2CreateCoreWebView2ControllerCompletedHandler](icorewebview2createcorewebview2controllercompletedhandler.md) * handler)

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
    m_dcompDevice = nullptr;
    m_wincompHelper = nullptr;
    LPCWSTR subFolder = nullptr;

    if (m_creationModeId == IDM_CREATION_MODE_VISUAL_DCOMP)
    {
        HRESULT hr = DCompositionCreateDevice2(nullptr, IID_PPV_ARGS(&m_dcompDevice));
        if (!SUCCEEDED(hr))
        {
            MessageBox(
                m_mainWindow,
                L"Attempting to create WebView using DComp Visual is not supported.\r\n"
                "DComp device creation failed.\r\n"
                "Current OS may not support DComp.",
                L"Create with Windowless DComp Visual Failed", MB_OK);
            return;
        }
    }
    else if (m_creationModeId == IDM_CREATION_MODE_VISUAL_WINCOMP)
    {
        HRESULT hr = CreateWinCompCompositor();
        if (!SUCCEEDED(hr))
        {
            MessageBox(
                m_mainWindow,
                L"Attempting to create WebView using WinComp Visual is not supported.\r\n"
                "WinComp compositor creation failed.\r\n"
                "Current OS may not support WinComp.",
                L"Create with Windowless WinComp Visual Failed", MB_OK);
            return;
        }
    }
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    if(!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
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
// This is the callback passed to CreateWebViewEnvironmentWithOptions.
// Here we simply create the WebView.
HRESULT AppWindow::OnCreateEnvironmentCompleted(
    HRESULT result, ICoreWebView2Environment* environment)
{
    CHECK_FAILURE(result);
    m_webViewEnvironment = environment;

    auto webViewExperimentalEnvironment =
        m_webViewEnvironment.try_query<ICoreWebView2ExperimentalEnvironment>();
    if (webViewExperimentalEnvironment && (m_dcompDevice || m_wincompHelper))
    {
        CHECK_FAILURE(webViewExperimentalEnvironment->CreateCoreWebView2CompositionController(
            m_mainWindow,
            Callback<
                ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler>(
                [this](
                    HRESULT result,
                    ICoreWebView2ExperimentalCompositionController* compositionController) -> HRESULT {
                    auto controller =
                        wil::com_ptr<ICoreWebView2ExperimentalCompositionController>(compositionController)
                            .query<ICoreWebView2Controller>();
                    return OnCreateCoreWebView2ControllerCompleted(result, controller.get());
                })
                .Get()));
    }
    else
    {
        CHECK_FAILURE(m_webViewEnvironment->CreateCoreWebView2Controller(
            m_mainWindow, Callback<ICoreWebView2CreateCoreWebView2ControllerCompletedHandler>(
                              this, &AppWindow::OnCreateCoreWebView2ControllerCompleted)
                              .Get()));
    }

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
 Cuando la aplicación vuelve a intentar CreateCoreWebView2Controller cuando se produce un error, se recomienda que la aplicación se reinicie a partir de la creación de un nuevo entorno de WebView2. Si se produce una actualización perimetral, la versión asociada a un entorno de WebView2 se podría haber quitado y provocar que el objeto deje de funcionar. La creación de un nuevo entorno de WebView2 funcionará porque usa la versión más reciente.

La creación de WebView generará un error si ya hay una instancia en ejecución con la misma carpeta datos de usuario y los objetos de entorno tienen diferentes EnvironmentOptions. Por ejemplo, si ya hay una vista previa creada con un idioma, se producirá un error al intentar crear una vista previa con un idioma diferente con la misma carpeta de datos de usuario.

#### CreateWebResourceResponse 

Crear un nuevo objeto de respuesta de recursos Web.

> [CREATEWEBRESOURCERESPONSE](#createwebresourceresponse)HRESULT público (IStream * Content, int STATUSCODE, LPCWSTR REASONPHRASE, LPCWSTR encabezados, [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) * * Response)

La cabecera es la cadena de encabezado de respuesta sin formato delimitada por newline. También es posible crear este objeto con una cadena de encabezados vacía y, a continuación, usar el [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) para construir los encabezados línea a línea. Para obtener información sobre otros parámetros, consulte [ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md).

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        COREWEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
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

#### get_BrowserVersionString 

Información de versión del explorador del [ICoreWebView2Environment]()actual, incluido el nombre del canal si no es el canal estable.

> [get_BrowserVersionString](#get_browserversionstring)de HRESULT público (LPWStr * versionInfo)

Coincide con el formato de la API de GetAvailableCoreWebView2BrowserVersionString. Los nombres de los canales son ' beta ', ' dev ' y ' Canarias '.

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionString(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

#### remove_NewBrowserVersionAvailable 

Quitar un controlador de eventos agregado previamente con add_NewBrowserVersionAvailable.

> [remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)de HRESULT público (token EventRegistrationToken)

