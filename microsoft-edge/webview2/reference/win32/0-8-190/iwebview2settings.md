---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 649506b28e0ecdbff33b44bbd8010ddb3d2a66b0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885803"
---
# 0.8.355: IWebView2Settings 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Settings
  : public IUnknown
```

Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_IsScriptEnabled](#get_isscriptenabled) | Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.
[put_IsScriptEnabled](#put_isscriptenabled) | Establezca la propiedad IsScriptEnabled.
[get_IsWebMessageEnabled](#get_iswebmessageenabled) | La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.
[put_IsWebMessageEnabled](#put_iswebmessageenabled) | Establezca la propiedad IsWebMessageEnabled.
[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled) | AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.
[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled) | Establezca la propiedad AreDefaultScriptDialogsEnabled.
[get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated) | Esta configuración ha quedado obsoleta y siempre devolverá FALSE.
[put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated) | Esta configuración ha quedado obsoleta y no tendrá ningún efecto.
[get_IsStatusBarEnabled](#get_isstatusbarenabled) | IsStatusBarEnabled controla si se mostrará la barra de estado.
[put_IsStatusBarEnabled](#put_isstatusbarenabled) | Establezca la propiedad IsStatusBarEnabled.
[get_AreDevToolsEnabled](#get_aredevtoolsenabled) | AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.
[put_AreDevToolsEnabled](#put_aredevtoolsenabled) | Establezca la propiedad AreDevToolsEnabled.

Los cambios de configuración realizados después del evento NavigationStarting no se aplicarán hasta la siguiente navegación de nivel superior.

## Miembros

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

#### put_IsScriptEnabled 

Establezca la propiedad IsScriptEnabled.

> [put_IsScriptEnabled](#put_isscriptenabled)de HRESULT público (bool IsScriptEnabled)

#### get_IsWebMessageEnabled 

La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.

> [get_IsWebMessageEnabled](#get_iswebmessageenabled)de HRESULT público (bool * IsWebMessageEnabled)

Si se establece en true, se permite la comunicación desde el host al documento HTML de nivel superior de la WebView a través de PostWebMessageAsJson, PostWebMessageAsString y Window. Chrome. evento de mensaje de WebView (consulte la documentación de PostWebMessageAsJson para obtener más información). Se permite la comunicación desde el documento HTML de nivel superior de WebView al host mediante Window. Chrome. función PostMessage de WebView y el método SetWebMessageReceivedEventHandler (consulte la documentación de SetWebMessageReceivedEventHandler para obtener más información). Si se establece en false, no se permite la comunicación. PostWebMessageAsJson y PostWebMessageAsString producirán errores con E_ACCESSDENIED y Window. Chrome. Webview. PostMessage producirá un error generando una instancia de un objeto de error. Es verdadero de forma predeterminada.

```cpp
    ComPtr<IWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### put_IsWebMessageEnabled 

Establezca la propiedad IsWebMessageEnabled.

> [put_IsWebMessageEnabled](#put_iswebmessageenabled)de HRESULT público (bool IsWebMessageEnabled)

#### get_AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.

> [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)de HRESULT público (bool * AreDefaultScriptDialogsEnabled)

Si se establece en false, WebView no procesará el cuadro de diálogo predeterminado de JavaScript (específicamente los que se muestran en las funciones de alerta, confirmación e petición de JavaScript). En su lugar, si un controlador de eventos se establece mediante SetScriptDialogOpeningEventHandler, WebView enviará un evento que contendrá toda la información del cuadro de diálogo y permitirá que la aplicación host muestre su propia interfaz de usuario personalizada.

#### put_AreDefaultScriptDialogsEnabled 

Establezca la propiedad AreDefaultScriptDialogsEnabled.

> [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de HRESULT público (bool AreDefaultScriptDialogsEnabled)

#### get_IsFullscreenAllowed_deprecated 

Esta configuración ha quedado obsoleta y siempre devolverá FALSE.

> [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)de HRESULT público (bool * IsFullscreenAllowed)

Eso significa que los elementos de la vista en WebView solo rellenarán los límites de la vista de vista. Esta propiedad se eliminará por completo. En su lugar, escucha el evento ContainsFullScreenElementChanged.

Controla si se permite la pantalla completa para los elementos de la vista. Cuando está permitido, el contenido Web, como un elemento de vídeo en la vista Web, se puede mostrar a pantalla completa. Si no está permitido, ese elemento rellenará los límites de la vista previa cuando el elemento solicite la pantalla completa. Es verdadero de forma predeterminada.

#### put_IsFullscreenAllowed_deprecated 

Esta configuración ha quedado obsoleta y no tendrá ningún efecto.

> [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)de HRESULT público (bool IsFullscreenAllowed)

En su lugar, escucha el evento ContainsFullScreenElementChanged.

Establezca la propiedad IsFullscreenAllowed.

#### get_IsStatusBarEnabled 

IsStatusBarEnabled controla si se mostrará la barra de estado.

> [get_IsStatusBarEnabled](#get_isstatusbarenabled)de HRESULT público (bool * IsStatusBarEnabled)

Normalmente, la barra de estado se muestra en la parte inferior izquierda de la vista WebView y muestra aspectos como el URI de un vínculo cuando el usuario mantiene el puntero sobre él y otra información. Es verdadero de forma predeterminada.

#### put_IsStatusBarEnabled 

Establezca la propiedad IsStatusBarEnabled.

> [put_IsStatusBarEnabled](#put_isstatusbarenabled)de HRESULT público (bool IsStatusBarEnabled)

#### get_AreDevToolsEnabled 

AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.

> [get_AreDevToolsEnabled](#get_aredevtoolsenabled)de HRESULT público (bool * AreDevToolsEnabled)

Es verdadero de forma predeterminada.

#### put_AreDevToolsEnabled 

Establezca la propiedad AreDevToolsEnabled.

> [put_AreDevToolsEnabled](#put_aredevtoolsenabled)de HRESULT público (bool AreDevToolsEnabled)

