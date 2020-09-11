---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalEnvironment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalEnvironment
ms.openlocfilehash: e7ccb108c137e54635c6e5b69f9bc615ff8ff018
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011140"
---
# <span data-ttu-id="45efe-104">0.9.579: ICoreWebView2ExperimentalEnvironment</span><span class="sxs-lookup"><span data-stu-id="45efe-104">0.9.579 - interface ICoreWebView2ExperimentalEnvironment</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalEnvironment
  : public IUnknown
```

<span data-ttu-id="45efe-105">Esta interfaz es una extensión de la [ICoreWebView2Environment](icorewebview2environment.md).</span><span class="sxs-lookup"><span data-stu-id="45efe-105">This interface is an extension of the [ICoreWebView2Environment](icorewebview2environment.md).</span></span>

## <span data-ttu-id="45efe-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="45efe-106">Summary</span></span>

 <span data-ttu-id="45efe-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="45efe-107">Members</span></span>                        | <span data-ttu-id="45efe-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="45efe-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="45efe-109">CreateCoreWebView2CompositionController</span><span class="sxs-lookup"><span data-stu-id="45efe-109">CreateCoreWebView2CompositionController</span></span>](#createcorewebview2compositioncontroller) | <span data-ttu-id="45efe-110">Cree de forma asincrónica una nueva vista de vista para usarla con el hospedaje visual.</span><span class="sxs-lookup"><span data-stu-id="45efe-110">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="45efe-111">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="45efe-111">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="45efe-112">Cree un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md)vacío.</span><span class="sxs-lookup"><span data-stu-id="45efe-112">Create an empty [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>
[<span data-ttu-id="45efe-113">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="45efe-113">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="45efe-114">Devuelve el proveedor de automatización de la interfaz de usuario de la ICoreWebView2CompositionController que se corresponde con el HWND dado.</span><span class="sxs-lookup"><span data-stu-id="45efe-114">Returns the UI Automation Provider for the ICoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="45efe-115">Un objeto que implementa la interfaz [ICoreWebView2ExperimentalEnvironment]() también implementará [ICoreWebView2Environment](icorewebview2environment.md).</span><span class="sxs-lookup"><span data-stu-id="45efe-115">An object implementing the [ICoreWebView2ExperimentalEnvironment]() interface will also implement [ICoreWebView2Environment](icorewebview2environment.md).</span></span>

## <span data-ttu-id="45efe-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="45efe-116">Members</span></span>

#### <span data-ttu-id="45efe-117">CreateCoreWebView2CompositionController</span><span class="sxs-lookup"><span data-stu-id="45efe-117">CreateCoreWebView2CompositionController</span></span> 

<span data-ttu-id="45efe-118">Cree de forma asincrónica una nueva vista de vista para usarla con el hospedaje visual.</span><span class="sxs-lookup"><span data-stu-id="45efe-118">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="45efe-119">[CREATECOREWEBVIEW2COMPOSITIONCONTROLLER](#createcorewebview2compositioncontroller)HRESULT público (HWND ParentWindow, [ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler](icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="45efe-119">public HRESULT [CreateCoreWebView2CompositionController](#createcorewebview2compositioncontroller)(HWND parentWindow, [ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler](icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="45efe-120">parentWindow es el HWND en el que la aplicación se conectará al árbol visual de la vista de ventana.</span><span class="sxs-lookup"><span data-stu-id="45efe-120">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="45efe-121">Este es el HWND que la aplicación recibirá una entrada de puntero o de mouse para la vista de ventana (y deberá usar SendMouseInput/SendPointerInput para reenviar).</span><span class="sxs-lookup"><span data-stu-id="45efe-121">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="45efe-122">Si la aplicación mueve el árbol visual WebView a una ventana distinta de otra, debe llamar a put_ParentWindow para actualizar el nuevo HWND primario del árbol visual.</span><span class="sxs-lookup"><span data-stu-id="45efe-122">If the app moves the WebView visual tree to underneath a different window, then it needs to call put_ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="45efe-123">Usa put_RootVisualTarget en el CoreWebView2CompositionController creado para proporcionar un objeto visual que hospede el árbol visual del explorador.</span><span class="sxs-lookup"><span data-stu-id="45efe-123">Use put_RootVisualTarget on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="45efe-124">Se recomienda que el identificador de modelo de usuario de la aplicación conjunto de aplicaciones para el proceso o la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="45efe-124">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="45efe-125">Si no se establece ninguna, durante la creación de WebView un identificador de modelo de usuario de aplicación generado se establece en la ventana raíz de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="45efe-125">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 
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
    auto options = Microsoft::WRL::Make<CoreWebView2ExperimentalEnvironmentOptions>();
    CHECK_FAILURE(options->put_IsSingleSignOnUsingOSPrimaryAccountEnabled(
        m_AADSSOEnabled ? TRUE : FALSE));
    if (!m_language.empty())
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
 <span data-ttu-id="45efe-126">Se recomienda que la aplicación se ocupe de los mensajes del administrador de reinicio para que se pueda reiniciar correctamente en el caso de que la aplicación esté usando Edge para WebView desde una instalación determinada y que la instalación se está desinstalando.</span><span class="sxs-lookup"><span data-stu-id="45efe-126">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="45efe-127">Por ejemplo, si un usuario instala Edge desde el canal de desarrollo y opta por usar Edge de ese canal para probar la aplicación y, después, desinstala Edge de ese canal sin cerrar la aplicación, se reiniciará la aplicación para permitir que la desinstalación del canal de desarrollo se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="45efe-127">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 
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

#### <span data-ttu-id="45efe-128">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="45efe-128">CreateCoreWebView2PointerInfo</span></span> 

<span data-ttu-id="45efe-129">Cree un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md)vacío.</span><span class="sxs-lookup"><span data-stu-id="45efe-129">Create an empty [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>

> <span data-ttu-id="45efe-130">HRESULT [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)([ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="45efe-130">public HRESULT [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)([ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \*\* pointerInfo)</span></span>

<span data-ttu-id="45efe-131">La [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) devuelta debe rellenarse con toda la información relevante antes de llamar a SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="45efe-131">The returned [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="45efe-132">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="45efe-132">GetProviderForHwnd</span></span> 

<span data-ttu-id="45efe-133">Devuelve el proveedor de automatización de la interfaz de usuario de la ICoreWebView2CompositionController que se corresponde con el HWND dado.</span><span class="sxs-lookup"><span data-stu-id="45efe-133">Returns the UI Automation Provider for the ICoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="45efe-134">[GETPROVIDERFORHWND](#getproviderforhwnd)HRESULT público (HWND HWND, IUnknown \* \* Provider)</span><span class="sxs-lookup"><span data-stu-id="45efe-134">public HRESULT [GetProviderForHwnd](#getproviderforhwnd)(HWND hwnd, IUnknown \*\* provider)</span></span>

