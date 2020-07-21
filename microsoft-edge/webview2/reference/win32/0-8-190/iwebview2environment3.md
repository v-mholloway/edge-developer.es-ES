---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 327a182c5298ed6de6b9e55b407d138857dbe659
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886097"
---
# <span data-ttu-id="cf764-104">0.8.355: IWebView2Environment3</span><span class="sxs-lookup"><span data-stu-id="cf764-104">0.8.355 - interface IWebView2Environment3</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Environment3
  : public IWebView2Environment2
```

<span data-ttu-id="cf764-105">Funcionalidad adicional implementada por el objeto de entorno.</span><span class="sxs-lookup"><span data-stu-id="cf764-105">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="cf764-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="cf764-106">Summary</span></span>

 <span data-ttu-id="cf764-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="cf764-107">Members</span></span>                        | <span data-ttu-id="cf764-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="cf764-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cf764-109">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="cf764-109">add_NewVersionAvailable</span></span>](#add_newversionavailable) | <span data-ttu-id="cf764-110">El evento NewVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.</span><span class="sxs-lookup"><span data-stu-id="cf764-110">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="cf764-111">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="cf764-111">remove_NewVersionAvailable</span></span>](#remove_newversionavailable) | <span data-ttu-id="cf764-112">Quitar un controlador de eventos agregado previamente con add_NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="cf764-112">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

<span data-ttu-id="cf764-113">Para obtener más información, consulta la interfaz de [IWebView2Environment](IWebView2Environment.md) .</span><span class="sxs-lookup"><span data-stu-id="cf764-113">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="cf764-114">Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="cf764-114">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="cf764-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="cf764-115">Members</span></span>

#### <span data-ttu-id="cf764-116">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="cf764-116">add_NewVersionAvailable</span></span> 

<span data-ttu-id="cf764-117">El evento NewVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.</span><span class="sxs-lookup"><span data-stu-id="cf764-117">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="cf764-118">[add_NewVersionAvailable](#add_newversionavailable)de HRESULT público ([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="cf764-118">public HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="cf764-119">Para usar la versión más reciente del explorador, debes crear un nuevo [IWebView2Environment](IWebView2Environment.md) y [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="cf764-119">To use the newer version of the browser you must create a new [IWebView2Environment](IWebView2Environment.md) and [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="cf764-120">El evento solo se desencadenará para la nueva versión desde el mismo canal de borde desde el que se está ejecutando el código.</span><span class="sxs-lookup"><span data-stu-id="cf764-120">Event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="cf764-121">Cuando no se esté ejecutando con Edge instalado, no se desencadenará ningún evento.</span><span class="sxs-lookup"><span data-stu-id="cf764-121">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="cf764-122">Dado que una carpeta de datos de usuario solo se puede usar en un proceso del explorador a la vez, si desea usar la misma carpeta datos de usuario en las vistas web con la nueva versión del explorador, debe cerrar primero los [IWebView2Environment](IWebView2Environment.md) y IWebView2WebViews que usan la versión anterior del explorador.</span><span class="sxs-lookup"><span data-stu-id="cf764-122">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the [IWebView2Environment](IWebView2Environment.md) and IWebView2WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="cf764-123">O simplemente pide al usuario que reinicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf764-123">Or simply prompt the user to restart the app.</span></span>

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

#### <span data-ttu-id="cf764-124">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="cf764-124">remove_NewVersionAvailable</span></span> 

<span data-ttu-id="cf764-125">Quitar un controlador de eventos agregado previamente con add_NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="cf764-125">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

> <span data-ttu-id="cf764-126">[remove_NewVersionAvailable](#remove_newversionavailable)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="cf764-126">public HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(EventRegistrationToken token)</span></span>

