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
# 0.8.355: IWebView2Settings2 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Settings2
  : public IWebView2Settings
```

Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled) | La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.
[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled) | Establezca la propiedad AreDefaultContextMenusEnabled.

Los cambios de configuración realizados después del evento NavigationStarting no se aplicarán hasta la siguiente navegación de nivel superior.

## Miembros

#### get_AreDefaultContextMenusEnabled 

La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.

> [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)de HRESULT público (bool * Enabled)

El valor predeterminado es TRUE.

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

#### put_AreDefaultContextMenusEnabled 

Establezca la propiedad AreDefaultContextMenusEnabled.

> [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)de HRESULT público (bool Enabled)

