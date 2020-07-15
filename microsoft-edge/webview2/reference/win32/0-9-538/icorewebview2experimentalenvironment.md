---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalEnvironment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalEnvironment
ms.openlocfilehash: f40dae22e8993c51ed32c0031e8aff1f217c974f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879985"
---
# interfaz ICoreWebView2ExperimentalEnvironment 

> [!NOTE]
> Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.538.

```
interface ICoreWebView2ExperimentalEnvironment
  : public IUnknown
```

Esta interfaz es una extensión de la [ICoreWebView2Environment](icorewebview2environment.md).

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[CreateCoreWebView2CompositionController](#createcorewebview2compositioncontroller) | Cree de forma asincrónica una nueva vista de vista para usarla con el hospedaje visual.
[CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo) | Cree un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md)vacío.
[GetProviderForHwnd](#getproviderforhwnd) | Devuelve el proveedor de automatización de la interfaz de usuario de la ICoreWebView2CompositionController que se corresponde con el HWND dado.

Un objeto que implementa la interfaz [ICoreWebView2ExperimentalEnvironment]() también implementará [ICoreWebView2Environment](icorewebview2environment.md).

## Miembros

#### CreateCoreWebView2CompositionController 

Cree de forma asincrónica una nueva vista de vista para usarla con el hospedaje visual.

> [CREATECOREWEBVIEW2COMPOSITIONCONTROLLER](#createcorewebview2compositioncontroller)HRESULT público (HWND ParentWindow, [ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler](icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md) * handler)

parentWindow es el HWND en el que la aplicación se conectará al árbol visual de la vista de ventana. Este es el HWND que la aplicación recibirá una entrada de puntero o de mouse para la vista de ventana (y deberá usar SendMouseInput/SendPointerInput para reenviar). Si la aplicación mueve el árbol visual WebView a una ventana distinta de otra, debe llamar a put_ParentWindow para actualizar el nuevo HWND primario del árbol visual.

Usa put_RootVisualTarget en el CoreWebView2CompositionController creado para proporcionar un objeto visual que hospede el árbol visual del explorador.

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

#### CreateCoreWebView2PointerInfo 

Cree un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md)vacío.

> HRESULT [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)([ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) * * pointerInfo)

La [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) devuelta debe rellenarse con toda la información relevante antes de llamar a SendPointerInput.

#### GetProviderForHwnd 

Devuelve el proveedor de automatización de la interfaz de usuario de la ICoreWebView2CompositionController que se corresponde con el HWND dado.

> [GETPROVIDERFORHWND](#getproviderforhwnd)HRESULT público (HWND HWND, IUnknown * * Provider)

