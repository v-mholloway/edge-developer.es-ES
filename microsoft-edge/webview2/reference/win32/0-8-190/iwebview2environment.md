---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 81b6d9814af84995909112ea79f11fbfcf93b488
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886083"
---
# <span data-ttu-id="4d422-104">0.8.355: IWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="4d422-104">0.8.355 - interface IWebView2Environment</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Environment
  : public IUnknown
```

<span data-ttu-id="4d422-105">Esto representa el entorno de WebView2.</span><span class="sxs-lookup"><span data-stu-id="4d422-105">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="4d422-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="4d422-106">Summary</span></span>

 <span data-ttu-id="4d422-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4d422-107">Members</span></span>                        | <span data-ttu-id="4d422-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="4d422-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4d422-109">CreateWebView</span><span class="sxs-lookup"><span data-stu-id="4d422-109">CreateWebView</span></span>](#createwebview) | <span data-ttu-id="4d422-110">Crear de forma asincrónica una nueva [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="4d422-110">Asynchronously create a new [IWebView2WebView](IWebView2WebView.md).</span></span>
[<span data-ttu-id="4d422-111">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="4d422-111">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="4d422-112">Crear un nuevo objeto de respuesta de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="4d422-112">Create a new web resource response object.</span></span>

<span data-ttu-id="4d422-113">Las vistas web creadas a partir de un entorno se ejecutan en el proceso del explorador especificado con los parámetros de entorno y los objetos creados a partir de un entorno se deben usar en el mismo entorno.</span><span class="sxs-lookup"><span data-stu-id="4d422-113">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="4d422-114">No se garantiza que su uso en diferentes entornos sea compatible y podría fallar.</span><span class="sxs-lookup"><span data-stu-id="4d422-114">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="4d422-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="4d422-115">Members</span></span>

#### <span data-ttu-id="4d422-116">CreateWebView</span><span class="sxs-lookup"><span data-stu-id="4d422-116">CreateWebView</span></span> 

<span data-ttu-id="4d422-117">Crear de forma asincrónica una nueva [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="4d422-117">Asynchronously create a new [IWebView2WebView](IWebView2WebView.md).</span></span>

> <span data-ttu-id="4d422-118">[CREATEWEBVIEW](#createwebview)HRESULT público (HWND ParentWindow,[IWebView2CreateWebViewCompletedHandler](IWebView2CreateWebViewCompletedHandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="4d422-118">public HRESULT [CreateWebView](#createwebview)(HWND parentWindow,[IWebView2CreateWebViewCompletedHandler](IWebView2CreateWebViewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="4d422-119">parentWindow es el HWND en el que se debe mostrar la vista en la vista previa y desde la que se recibe la entrada.</span><span class="sxs-lookup"><span data-stu-id="4d422-119">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="4d422-120">La vista en WebView agregará una ventana secundaria a la ventana proporcionada durante la creación de WebView.</span><span class="sxs-lookup"><span data-stu-id="4d422-120">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="4d422-121">El orden Z y otros elementos afectados por el orden de ventanas relacionados se verán afectados según corresponda.</span><span class="sxs-lookup"><span data-stu-id="4d422-121">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="4d422-122">Se recomienda que el identificador de modelo de usuario de la aplicación conjunto de aplicaciones para el proceso o la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4d422-122">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="4d422-123">Si no se establece ninguna, durante la creación de WebView un identificador de modelo de usuario de aplicación generado se establece en la ventana raíz de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="4d422-123">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 

```cpp
// Create or recreate the WebView and its environment.
void AppWindow::InitializeWebView(InitializeWebViewFlags webviewInitFlags)
{
    m_lastUsedInitFlags = webviewInitFlags;
    // To ensure browser switches get applied correctly, we need to close
    // the existing WebView. This will result in a new browser process
    // getting created which will apply the browser switches.
    CloseWebView();

    LPCWSTR subFolder = nullptr;
    LPCWSTR additionalBrowserSwitches = nullptr;
    HRESULT hr = CreateWebView2EnvironmentWithDetails(
        subFolder, nullptr, additionalBrowserSwitches,
        Callback<IWebView2CreateWebView2EnvironmentCompletedHandler>(
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
    HRESULT result, IWebView2Environment* environment)
{
    CHECK_FAILURE(result);

    CHECK_FAILURE(environment->QueryInterface(IID_PPV_ARGS(&m_webViewEnvironment)));
        CHECK_FAILURE(m_webViewEnvironment->CreateWebView(
            m_mainWindow, Callback<IWebView2CreateWebViewCompletedHandler>(
                              this, &AppWindow::OnCreateWebViewCompleted)
                              .Get()));
    return S_OK;
}
```

 <span data-ttu-id="4d422-124">Se recomienda que la aplicación se ocupe de los mensajes del administrador de reinicio para que se pueda reiniciar correctamente en el caso de que la aplicación esté usando Edge para WebView desde una instalación determinada y que la instalación se está desinstalando.</span><span class="sxs-lookup"><span data-stu-id="4d422-124">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="4d422-125">Por ejemplo, si un usuario instala Edge desde el canal de desarrollo y opta por usar Edge de ese canal para probar la aplicación y, después, desinstala Edge de ese canal sin cerrar la aplicación, se reiniciará la aplicación para permitir que la desinstalación del canal de desarrollo se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="4d422-125">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 

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

#### <span data-ttu-id="4d422-126">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="4d422-126">CreateWebResourceResponse</span></span> 

<span data-ttu-id="4d422-127">Crear un nuevo objeto de respuesta de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="4d422-127">Create a new web resource response object.</span></span>

> <span data-ttu-id="4d422-128">[CREATEWEBRESOURCERESPONSE](#createwebresourceresponse)HRESULT público (IStream \* Content, int STATUSCODE, LPCWSTR REASONPHRASE, LPCWSTR encabezados,[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="4d422-128">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content,int statusCode,LPCWSTR reasonPhrase,LPCWSTR headers,[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

<span data-ttu-id="4d422-129">La cabecera es la cadena de encabezado de respuesta sin formato delimitada por newline.</span><span class="sxs-lookup"><span data-stu-id="4d422-129">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="4d422-130">También es posible crear este objeto con una cadena de encabezados vacía y, a continuación, usar el [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) para construir los encabezados línea a línea.</span><span class="sxs-lookup"><span data-stu-id="4d422-130">It's also possible to create this object with empty headers string and then use the [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) to construct the headers line by line.</span></span> <span data-ttu-id="4d422-131">Para obtener información sobre otros parámetros, consulte [IWebView2WebResourceResponse](IWebView2WebResourceResponse.md).</span><span class="sxs-lookup"><span data-stu-id="4d422-131">For information on other parameters see [IWebView2WebResourceResponse](IWebView2WebResourceResponse.md).</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
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

