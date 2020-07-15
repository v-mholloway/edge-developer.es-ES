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
# <span data-ttu-id="366de-104">interfaz ICoreWebView2ExperimentalEnvironment</span><span class="sxs-lookup"><span data-stu-id="366de-104">interface ICoreWebView2ExperimentalEnvironment</span></span> 

> [!NOTE]
> <span data-ttu-id="366de-105">Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="366de-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalEnvironment
  : public IUnknown
```

<span data-ttu-id="366de-106">Esta interfaz es una extensión de la [ICoreWebView2Environment](icorewebview2environment.md).</span><span class="sxs-lookup"><span data-stu-id="366de-106">This interface is an extension of the [ICoreWebView2Environment](icorewebview2environment.md).</span></span>

## <span data-ttu-id="366de-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="366de-107">Summary</span></span>

 <span data-ttu-id="366de-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="366de-108">Members</span></span>                        | <span data-ttu-id="366de-109">Descripciones</span><span class="sxs-lookup"><span data-stu-id="366de-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="366de-110">CreateCoreWebView2CompositionController</span><span class="sxs-lookup"><span data-stu-id="366de-110">CreateCoreWebView2CompositionController</span></span>](#createcorewebview2compositioncontroller) | <span data-ttu-id="366de-111">Cree de forma asincrónica una nueva vista de vista para usarla con el hospedaje visual.</span><span class="sxs-lookup"><span data-stu-id="366de-111">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="366de-112">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="366de-112">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="366de-113">Cree un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md)vacío.</span><span class="sxs-lookup"><span data-stu-id="366de-113">Create an empty [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>
[<span data-ttu-id="366de-114">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="366de-114">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="366de-115">Devuelve el proveedor de automatización de la interfaz de usuario de la ICoreWebView2CompositionController que se corresponde con el HWND dado.</span><span class="sxs-lookup"><span data-stu-id="366de-115">Returns the UI Automation Provider for the ICoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="366de-116">Un objeto que implementa la interfaz [ICoreWebView2ExperimentalEnvironment]() también implementará [ICoreWebView2Environment](icorewebview2environment.md).</span><span class="sxs-lookup"><span data-stu-id="366de-116">An object implementing the [ICoreWebView2ExperimentalEnvironment]() interface will also implement [ICoreWebView2Environment](icorewebview2environment.md).</span></span>

## <span data-ttu-id="366de-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="366de-117">Members</span></span>

#### <span data-ttu-id="366de-118">CreateCoreWebView2CompositionController</span><span class="sxs-lookup"><span data-stu-id="366de-118">CreateCoreWebView2CompositionController</span></span> 

<span data-ttu-id="366de-119">Cree de forma asincrónica una nueva vista de vista para usarla con el hospedaje visual.</span><span class="sxs-lookup"><span data-stu-id="366de-119">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="366de-120">[CREATECOREWEBVIEW2COMPOSITIONCONTROLLER](#createcorewebview2compositioncontroller)HRESULT público (HWND ParentWindow, [ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler](icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="366de-120">public HRESULT [CreateCoreWebView2CompositionController](#createcorewebview2compositioncontroller)(HWND parentWindow, [ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler](icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="366de-121">parentWindow es el HWND en el que la aplicación se conectará al árbol visual de la vista de ventana.</span><span class="sxs-lookup"><span data-stu-id="366de-121">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="366de-122">Este es el HWND que la aplicación recibirá una entrada de puntero o de mouse para la vista de ventana (y deberá usar SendMouseInput/SendPointerInput para reenviar).</span><span class="sxs-lookup"><span data-stu-id="366de-122">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="366de-123">Si la aplicación mueve el árbol visual WebView a una ventana distinta de otra, debe llamar a put_ParentWindow para actualizar el nuevo HWND primario del árbol visual.</span><span class="sxs-lookup"><span data-stu-id="366de-123">If the app moves the WebView visual tree to underneath a different window, then it needs to call put_ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="366de-124">Usa put_RootVisualTarget en el CoreWebView2CompositionController creado para proporcionar un objeto visual que hospede el árbol visual del explorador.</span><span class="sxs-lookup"><span data-stu-id="366de-124">Use put_RootVisualTarget on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="366de-125">Se recomienda que el identificador de modelo de usuario de la aplicación conjunto de aplicaciones para el proceso o la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="366de-125">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="366de-126">Si no se establece ninguna, durante la creación de WebView un identificador de modelo de usuario de aplicación generado se establece en la ventana raíz de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="366de-126">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 
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
 <span data-ttu-id="366de-127">Se recomienda que la aplicación se ocupe de los mensajes del administrador de reinicio para que se pueda reiniciar correctamente en el caso de que la aplicación esté usando Edge para WebView desde una instalación determinada y que la instalación se está desinstalando.</span><span class="sxs-lookup"><span data-stu-id="366de-127">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="366de-128">Por ejemplo, si un usuario instala Edge desde el canal de desarrollo y opta por usar Edge de ese canal para probar la aplicación y, después, desinstala Edge de ese canal sin cerrar la aplicación, se reiniciará la aplicación para permitir que la desinstalación del canal de desarrollo se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="366de-128">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 
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

#### <span data-ttu-id="366de-129">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="366de-129">CreateCoreWebView2PointerInfo</span></span> 

<span data-ttu-id="366de-130">Cree un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md)vacío.</span><span class="sxs-lookup"><span data-stu-id="366de-130">Create an empty [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>

> <span data-ttu-id="366de-131">HRESULT [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)([ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="366de-131">public HRESULT [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)([ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \*\* pointerInfo)</span></span>

<span data-ttu-id="366de-132">La [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) devuelta debe rellenarse con toda la información relevante antes de llamar a SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="366de-132">The returned [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="366de-133">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="366de-133">GetProviderForHwnd</span></span> 

<span data-ttu-id="366de-134">Devuelve el proveedor de automatización de la interfaz de usuario de la ICoreWebView2CompositionController que se corresponde con el HWND dado.</span><span class="sxs-lookup"><span data-stu-id="366de-134">Returns the UI Automation Provider for the ICoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="366de-135">[GETPROVIDERFORHWND](#getproviderforhwnd)HRESULT público (HWND HWND, IUnknown \* \* Provider)</span><span class="sxs-lookup"><span data-stu-id="366de-135">public HRESULT [GetProviderForHwnd](#getproviderforhwnd)(HWND hwnd, IUnknown \*\* provider)</span></span>

