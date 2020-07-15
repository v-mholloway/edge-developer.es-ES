---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 4e9f1d7baadcb20774bd4816f043f71a1a8b50b8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878207"
---
# <span data-ttu-id="b54cf-104">0.8.355: IWebView2Settings2</span><span class="sxs-lookup"><span data-stu-id="b54cf-104">0.8.355 - interface IWebView2Settings2</span></span> 

> [!NOTE]
> <span data-ttu-id="b54cf-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="b54cf-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="b54cf-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="b54cf-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Settings2
  : public IWebView2Settings
```

<span data-ttu-id="b54cf-107">Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.</span><span class="sxs-lookup"><span data-stu-id="b54cf-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="b54cf-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="b54cf-108">Summary</span></span>

 <span data-ttu-id="b54cf-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b54cf-109">Members</span></span>                        | <span data-ttu-id="b54cf-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b54cf-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b54cf-111">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="b54cf-111">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="b54cf-112">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="b54cf-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="b54cf-113">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="b54cf-113">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="b54cf-114">Establezca la propiedad AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="b54cf-114">Set the AreDefaultContextMenusEnabled property.</span></span>

<span data-ttu-id="b54cf-115">Los cambios de configuración realizados después del evento NavigationStarting no se aplicarán hasta la siguiente navegación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="b54cf-115">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="b54cf-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="b54cf-116">Members</span></span>

#### <span data-ttu-id="b54cf-117">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="b54cf-117">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="b54cf-118">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="b54cf-118">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="b54cf-119">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="b54cf-119">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="b54cf-120">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="b54cf-120">Defaults to TRUE.</span></span>

```cpp
            BOOL allowContextMenus;
            CHECK_FAILURE(m_settings->get_AreDefaultContextMenusEnabled(
                &allowContextMenus));
            if (allowContextMenus) {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(FALSE));
                MessageBox(nullptr,
                L"Context menus will be disabled after the next navigation.",
                L"Settings change", MB_OK);
            }
            else {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(TRUE));
                MessageBox(nullptr,
                    L"Context menus will be enabled after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="b54cf-121">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="b54cf-121">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="b54cf-122">Establezca la propiedad AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="b54cf-122">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="b54cf-123">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="b54cf-123">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

