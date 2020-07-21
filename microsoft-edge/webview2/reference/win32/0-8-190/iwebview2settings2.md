---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 4ba0299f3afbc6fc2846481f52c1000cd338ecd8
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885789"
---
# <span data-ttu-id="c0b36-104">0.8.355: IWebView2Settings2</span><span class="sxs-lookup"><span data-stu-id="c0b36-104">0.8.355 - interface IWebView2Settings2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Settings2
  : public IWebView2Settings
```

<span data-ttu-id="c0b36-105">Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.</span><span class="sxs-lookup"><span data-stu-id="c0b36-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="c0b36-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="c0b36-106">Summary</span></span>

 <span data-ttu-id="c0b36-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c0b36-107">Members</span></span>                        | <span data-ttu-id="c0b36-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="c0b36-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c0b36-109">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="c0b36-109">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="c0b36-110">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="c0b36-110">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="c0b36-111">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="c0b36-111">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="c0b36-112">Establezca la propiedad AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="c0b36-112">Set the AreDefaultContextMenusEnabled property.</span></span>

<span data-ttu-id="c0b36-113">Los cambios de configuración realizados después del evento NavigationStarting no se aplicarán hasta la siguiente navegación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="c0b36-113">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="c0b36-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="c0b36-114">Members</span></span>

#### <span data-ttu-id="c0b36-115">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="c0b36-115">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="c0b36-116">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="c0b36-116">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="c0b36-117">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="c0b36-117">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="c0b36-118">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="c0b36-118">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="c0b36-119">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="c0b36-119">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="c0b36-120">Establezca la propiedad AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="c0b36-120">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="c0b36-121">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="c0b36-121">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

