---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2Settings
ms.openlocfilehash: 1ad6754d2ff59a92e107c66644e389582ff6053b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012707"
---
# interfaz ICoreWebView2Settings 

```
interface ICoreWebView2Settings
  : public IUnknown
```

Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled) | La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.
[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled) | AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.
[get_AreDevToolsEnabled](#get_aredevtoolsenabled) | AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.
[get_AreHostObjectsAllowed](#get_arehostobjectsallowed) | La propiedad AreHostObjectsAllowed se usa para controlar si se puede acceder a los objetos host desde la página de WebView.
[get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled) | La propiedad IsBuiltInErrorPageEnabled se usa para deshabilitar la página de error integrada para el error de navegación y el error del proceso de representación.
[get_IsScriptEnabled](#get_isscriptenabled) | Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.
[get_IsStatusBarEnabled](#get_isstatusbarenabled) | IsStatusBarEnabled controla si se mostrará la barra de estado.
[get_IsWebMessageEnabled](#get_iswebmessageenabled) | La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.
[get_IsZoomControlEnabled](#get_iszoomcontrolenabled) | La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.
[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled) | Establezca la propiedad AreDefaultContextMenusEnabled.
[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled) | Establezca la propiedad AreDefaultScriptDialogsEnabled.
[put_AreDevToolsEnabled](#put_aredevtoolsenabled) | Establezca la propiedad AreDevToolsEnabled.
[put_AreHostObjectsAllowed](#put_arehostobjectsallowed) | Establezca la propiedad AreHostObjectsAllowed.
[put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled) | Establezca la propiedad IsBuiltInErrorPageEnabled.
[put_IsScriptEnabled](#put_isscriptenabled) | Establezca la propiedad IsScriptEnabled.
[put_IsStatusBarEnabled](#put_isstatusbarenabled) | Establezca la propiedad IsStatusBarEnabled.
[put_IsWebMessageEnabled](#put_iswebmessageenabled) | Establezca la propiedad IsWebMessageEnabled.
[put_IsZoomControlEnabled](#put_iszoomcontrolenabled) | Establezca la propiedad IsZoomControlEnabled.

Los cambios de configuración realizados después del evento NavigationStarting no se aplicarán hasta la siguiente navegación de nivel superior.

## Miembros

#### get_AreDefaultContextMenusEnabled 

La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.

> [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)de HRESULT público (bool * Enabled)

Es verdadero de forma predeterminada.

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

#### get_AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.

> [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)de HRESULT público (bool * AreDefaultScriptDialogsEnabled)

Si se establece en false, WebView no procesará el cuadro de diálogo predeterminado de JavaScript (específicamente los que se muestran en las alertas de JavaScript, CONFIRM, prompt functions y beforeunload Event). En su lugar, si un controlador de eventos se establece a través de add_ScriptDialogOpening, WebView enviará un evento que contendrá toda la información del cuadro de diálogo y permitirá que la aplicación host muestre su propia interfaz de usuario personalizada. Es verdadero de forma predeterminada.

#### get_AreDevToolsEnabled 

AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.

> [get_AreDevToolsEnabled](#get_aredevtoolsenabled)de HRESULT público (bool * AreDevToolsEnabled)

Es verdadero de forma predeterminada.

#### get_AreHostObjectsAllowed 

La propiedad AreHostObjectsAllowed se usa para controlar si se puede acceder a los objetos host desde la página de WebView.

> [get_AreHostObjectsAllowed](#get_arehostobjectsallowed)de HRESULT público (bool * allowed)

Es verdadero de forma predeterminada.

```cpp
            BOOL allowHostObjects;
            CHECK_FAILURE(m_settings->get_AreHostObjectsAllowed(&allowHostObjects));
            if (allowHostObjects)
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(FALSE));
                MessageBox(
                    nullptr, L"Access to host objects will be denied after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(TRUE));
                MessageBox(
                    nullptr, L"Access to host objects will be allowed after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### get_IsBuiltInErrorPageEnabled 

La propiedad IsBuiltInErrorPageEnabled se usa para deshabilitar la página de error integrada para el error de navegación y el error del proceso de representación.

> [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)de HRESULT público (bool * Enabled)

Es verdadero de forma predeterminada. Cuando se deshabilita, se muestra una página en blanco cuando se produce un error relacionado.

```cpp
            BOOL enabled;
            CHECK_FAILURE(m_settings->get_IsBuiltInErrorPageEnabled(&enabled));
            if (enabled)
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(FALSE));
                MessageBox(
                    nullptr, L"Built-in error page will be disabled for future navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(TRUE));
                MessageBox(
                    nullptr, L"Built-in error page will be enabled for future navigation.",
                    L"Settings change", MB_OK);
            }
```

#### get_IsScriptEnabled 

Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.

> [get_IsScriptEnabled](#get_isscriptenabled)de HRESULT público (bool * IsScriptEnabled)

Esto solo afecta a los scripts del documento. los scripts inyectados con ExecuteScript se ejecutarán incluso si el script está deshabilitado. Es verdadero de forma predeterminada.

```cpp
        // Changes to settings will apply at the next navigation, which includes the
        // navigation after a NavigationStarting event.  We can use this to change
        // settings according to what site we're visiting.
        if (ShouldBlockScriptForUri(uri.get()))
        {
            m_settings->put_IsScriptEnabled(FALSE);
        }
        else
        {
            m_settings->put_IsScriptEnabled(m_isScriptEnabled);
        }
```

#### get_IsStatusBarEnabled 

IsStatusBarEnabled controla si se mostrará la barra de estado.

> [get_IsStatusBarEnabled](#get_isstatusbarenabled)de HRESULT público (bool * IsStatusBarEnabled)

Normalmente, la barra de estado se muestra en la parte inferior izquierda de la vista WebView y muestra aspectos como el URI de un vínculo cuando el usuario mantiene el puntero sobre él y otra información. Es verdadero de forma predeterminada.

#### get_IsWebMessageEnabled 

La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.

> [get_IsWebMessageEnabled](#get_iswebmessageenabled)de HRESULT público (bool * IsWebMessageEnabled)

Si se establece en true, se permite la comunicación desde el host al documento HTML de nivel superior de la WebView a través de PostWebMessageAsJson, PostWebMessageAsString y Window. Chrome. evento de mensaje de WebView (consulte la documentación de PostWebMessageAsJson para obtener más información). Se permite la comunicación desde el documento HTML de nivel superior de WebView al host a través de la función PostMessage de window. Chrome. WebMessage y el método add_WebMessageReceived (consulte la documentación de add_WebMessageReceived para obtener más información). Si se establece en false, no se permite la comunicación. PostWebMessageAsJson y PostWebMessageAsString producirán errores con E_ACCESSDENIED y Window. Chrome. Webview. PostMessage producirá un error generando una instancia de un objeto de error. Es verdadero de forma predeterminada.

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### get_IsZoomControlEnabled 

La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.

> [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)de HRESULT público (bool * Enabled)

Es verdadero de forma predeterminada. Cuando está deshabilitado, el usuario no podrá hacer zoom con Ctrl +/o Ctrl + rueda del mouse, pero el zoom puede establecerse a través de la API de ZoomFactor.

```cpp
            BOOL zoomControlEnabled;
            CHECK_FAILURE(m_settings->get_IsZoomControlEnabled(&zoomControlEnabled));
            if (zoomControlEnabled)
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(FALSE));
                MessageBox(
                    nullptr, L"Zoom control will be disabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(TRUE));
                MessageBox(
                    nullptr, L"Zoom control will be enabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
```

#### put_AreDefaultContextMenusEnabled 

Establezca la propiedad AreDefaultContextMenusEnabled.

> [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)de HRESULT público (bool Enabled)

#### put_AreDefaultScriptDialogsEnabled 

Establezca la propiedad AreDefaultScriptDialogsEnabled.

> [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de HRESULT público (bool AreDefaultScriptDialogsEnabled)

#### put_AreDevToolsEnabled 

Establezca la propiedad AreDevToolsEnabled.

> [put_AreDevToolsEnabled](#put_aredevtoolsenabled)de HRESULT público (bool AreDevToolsEnabled)

#### put_AreHostObjectsAllowed 

Establezca la propiedad AreHostObjectsAllowed.

> [put_AreHostObjectsAllowed](#put_arehostobjectsallowed)de HRESULT público (se permite bool)

#### put_IsBuiltInErrorPageEnabled 

Establezca la propiedad IsBuiltInErrorPageEnabled.

> [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)de HRESULT público (bool Enabled)

#### put_IsScriptEnabled 

Establezca la propiedad IsScriptEnabled.

> [put_IsScriptEnabled](#put_isscriptenabled)de HRESULT público (bool IsScriptEnabled)

#### put_IsStatusBarEnabled 

Establezca la propiedad IsStatusBarEnabled.

> [put_IsStatusBarEnabled](#put_isstatusbarenabled)de HRESULT público (bool IsStatusBarEnabled)

#### put_IsWebMessageEnabled 

Establezca la propiedad IsWebMessageEnabled.

> [put_IsWebMessageEnabled](#put_iswebmessageenabled)de HRESULT público (bool IsWebMessageEnabled)

#### put_IsZoomControlEnabled 

Establezca la propiedad IsZoomControlEnabled.

> [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)de HRESULT público (bool Enabled)

