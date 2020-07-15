---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: d16a12aae823c48b7dd4b0b5e8225cdd40c1dafc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878529"
---
# <span data-ttu-id="cca18-104">0.8.355: IWebView2Environment3</span><span class="sxs-lookup"><span data-stu-id="cca18-104">0.8.355 - interface IWebView2Environment3</span></span> 

> [!NOTE]
> <span data-ttu-id="cca18-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="cca18-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="cca18-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="cca18-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment3
  : public IWebView2Environment2
```

<span data-ttu-id="cca18-107">Funcionalidad adicional implementada por el objeto de entorno.</span><span class="sxs-lookup"><span data-stu-id="cca18-107">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="cca18-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="cca18-108">Summary</span></span>

 <span data-ttu-id="cca18-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="cca18-109">Members</span></span>                        | <span data-ttu-id="cca18-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="cca18-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cca18-111">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="cca18-111">add_NewVersionAvailable</span></span>](#add_newversionavailable) | <span data-ttu-id="cca18-112">El evento NewVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.</span><span class="sxs-lookup"><span data-stu-id="cca18-112">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="cca18-113">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="cca18-113">remove_NewVersionAvailable</span></span>](#remove_newversionavailable) | <span data-ttu-id="cca18-114">Quitar un controlador de eventos agregado previamente con add_NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="cca18-114">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

<span data-ttu-id="cca18-115">Para obtener más información, consulta la interfaz de [IWebView2Environment](IWebView2Environment.md) .</span><span class="sxs-lookup"><span data-stu-id="cca18-115">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="cca18-116">Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="cca18-116">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="cca18-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="cca18-117">Members</span></span>

#### <span data-ttu-id="cca18-118">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="cca18-118">add_NewVersionAvailable</span></span> 

<span data-ttu-id="cca18-119">El evento NewVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.</span><span class="sxs-lookup"><span data-stu-id="cca18-119">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="cca18-120">[add_NewVersionAvailable](#add_newversionavailable)de HRESULT público ([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="cca18-120">public HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="cca18-121">Para usar la versión más reciente del explorador, debes crear un nuevo [IWebView2Environment](IWebView2Environment.md) y [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="cca18-121">To use the newer version of the browser you must create a new [IWebView2Environment](IWebView2Environment.md) and [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="cca18-122">El evento solo se desencadenará para la nueva versión desde el mismo canal de borde desde el que se está ejecutando el código.</span><span class="sxs-lookup"><span data-stu-id="cca18-122">Event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="cca18-123">Cuando no se esté ejecutando con Edge instalado, no se desencadenará ningún evento.</span><span class="sxs-lookup"><span data-stu-id="cca18-123">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="cca18-124">Dado que una carpeta de datos de usuario solo se puede usar en un proceso del explorador a la vez, si desea usar la misma carpeta datos de usuario en las vistas web con la nueva versión del explorador, debe cerrar primero los [IWebView2Environment](IWebView2Environment.md) y IWebView2WebViews que usan la versión anterior del explorador.</span><span class="sxs-lookup"><span data-stu-id="cca18-124">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the [IWebView2Environment](IWebView2Environment.md) and IWebView2WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="cca18-125">O simplemente pide al usuario que reinicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cca18-125">Or simply prompt the user to restart the app.</span></span>

```cpp
    // After the environment is successfully created,
    // register a handler for the NewVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewVersionAvailable(
        Callback<IWebView2NewVersionAvailableEventHandler>(
            [this](IWebView2Environment* sender, IWebView2NewVersionAvailableEventArgs* args)
                -> HRESULT {
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

#### <span data-ttu-id="cca18-126">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="cca18-126">remove_NewVersionAvailable</span></span> 

<span data-ttu-id="cca18-127">Quitar un controlador de eventos agregado previamente con add_NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="cca18-127">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

> <span data-ttu-id="cca18-128">[remove_NewVersionAvailable](#remove_newversionavailable)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="cca18-128">public HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(EventRegistrationToken token)</span></span>

