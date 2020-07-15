---
description: Hospedar contenido web en la aplicación Win32 con el control de WebView 2 de Microsoft Edge
title: '0.9.430: referencia de Win32 C++'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: a0095660af031cafa09e5223650d174f525ba3df
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880244"
---
# 0.9.430 - Referencia (WebView2)  

> [!NOTE]
> Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430. Consulta la [referencia](../../webview2-api-reference.md) de la API más reciente.

El control Microsoft Edge WebView2 permite hospedar contenido web en tu aplicación con [Microsoft Edge \ (cromo \)](https://www.microsoftedgeinsider.com) como motor de representación.  Para obtener más información, vea [información general sobre Microsoft Edge WebView2](../../index.md)) y [Cómo comenzar a usar WebView2](../../gettingstarted/win32.md).  [ICoreWebView2](0-9-430/ICoreWebView2.md) es un buen lugar para comenzar a conocer los detalles de la API.  

## Global  

*   [Global](0-9-430/webview2-idl.md)  

## Interactúa  
*   [ICoreWebView2](0-9-430/ICoreWebView2.md)
*   [ICoreWebView2Deferral](0-9-430/ICoreWebView2Deferral.md)
*   [ICoreWebView2DevToolsProtocolEventReceiver](0-9-430/ICoreWebView2DevToolsProtocolEventReceiver.md)
*   [ICoreWebView2Environment](0-9-430/ICoreWebView2Environment.md)
*   [ICoreWebView2Host](0-9-430/ICoreWebView2Host.md)
*   [ICoreWebView2HttpHeadersCollectionIterator](0-9-430/ICoreWebView2HttpHeadersCollectionIterator.md)
*   [ICoreWebView2HttpRequestHeaders](0-9-430/ICoreWebView2HttpRequestHeaders.md)
*   [ICoreWebView2HttpResponseHeaders](0-9-430/ICoreWebView2HttpResponseHeaders.md)
*   [ICoreWebView2Settings](0-9-430/ICoreWebView2Settings.md)
*   [ICoreWebView2WebResourceRequest](0-9-430/ICoreWebView2WebResourceRequest.md)
*   [ICoreWebView2WebResourceResponse](0-9-430/ICoreWebView2WebResourceResponse.md)

### Interfaces de argumento de evento

*   [ICoreWebView2AcceleratorKeyPressedEventArgs](0-9-430/ICoreWebView2AcceleratorKeyPressedEventArgs.md)
*   [ICoreWebView2ContentLoadingEventArgs](0-9-430/ICoreWebView2ContentLoadingEventArgs.md)
*   [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](0-9-430/ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md)
*   [ICoreWebView2MoveFocusRequestedEventArgs](0-9-430/ICoreWebView2MoveFocusRequestedEventArgs.md)
*   [ICoreWebView2NavigationCompletedEventArgs](0-9-430/ICoreWebView2NavigationCompletedEventArgs.md)
*   [ICoreWebView2NavigationStartingEventArgs](0-9-430/ICoreWebView2NavigationStartingEventArgs.md)
*   [ICoreWebView2NewBrowserVersionAvailableEventArgs](0-9-430/ICoreWebView2NewBrowserVersionAvailableEventArgs.md)
*   [ICoreWebView2NewWindowRequestedEventArgs](0-9-430/ICoreWebView2NewWindowRequestedEventArgs.md)
*   [ICoreWebView2PermissionRequestedEventArgs](0-9-430/ICoreWebView2PermissionRequestedEventArgs.md)
*   [ICoreWebView2ProcessFailedEventArgs](0-9-430/ICoreWebView2ProcessFailedEventArgs.md)
*   [ICoreWebView2ScriptDialogOpeningEventArgs](0-9-430/ICoreWebView2ScriptDialogOpeningEventArgs.md)
*   [ICoreWebView2SourceChangedEventArgs](0-9-430/ICoreWebView2SourceChangedEventArgs.md)
*   [ICoreWebView2WebMessageReceivedEventArgs](0-9-430/ICoreWebView2WebMessageReceivedEventArgs.md)
*   [ICoreWebView2WebResourceRequestedEventArgs](0-9-430/ICoreWebView2WebResourceRequestedEventArgs.md)

### Interfaces delegadas

*   [ICoreWebView2AcceleratorKeyPressedEventHandler](0-9-430/ICoreWebView2AcceleratorKeyPressedEventHandler.md)
*   [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](0-9-430/ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md)
*   [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](0-9-430/ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md)
*   [ICoreWebView2CapturePreviewCompletedHandler](0-9-430/ICoreWebView2CapturePreviewCompletedHandler.md)
*   [ICoreWebView2ContainsFullScreenElementChangedEventHandler](0-9-430/ICoreWebView2ContainsFullScreenElementChangedEventHandler.md)
*   [ICoreWebView2ContentLoadingEventHandler](0-9-430/ICoreWebView2ContentLoadingEventHandler.md)
*   [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](0-9-430/ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler.md)
*   [ICoreWebView2CreateCoreWebView2HostCompletedHandler](0-9-430/ICoreWebView2CreateCoreWebView2HostCompletedHandler.md)
*   [ICoreWebView2DevToolsProtocolEventReceivedEventHandler](0-9-430/ICoreWebView2DevToolsProtocolEventReceivedEventHandler.md)
*   [ICoreWebView2DocumentTitleChangedEventHandler](0-9-430/ICoreWebView2DocumentTitleChangedEventHandler.md)
*   [ICoreWebView2ExecuteScriptCompletedHandler](0-9-430/ICoreWebView2ExecuteScriptCompletedHandler.md)
*   [ICoreWebView2FocusChangedEventHandler](0-9-430/ICoreWebView2FocusChangedEventHandler.md)
*   [ICoreWebView2HistoryChangedEventHandler](0-9-430/ICoreWebView2HistoryChangedEventHandler.md)
*   [ICoreWebView2MoveFocusRequestedEventHandler](0-9-430/ICoreWebView2MoveFocusRequestedEventHandler.md)
*   [ICoreWebView2NavigationCompletedEventHandler](0-9-430/ICoreWebView2NavigationCompletedEventHandler.md)
*   [ICoreWebView2NavigationStartingEventHandler](0-9-430/ICoreWebView2NavigationStartingEventHandler.md)
*   [ICoreWebView2NewBrowserVersionAvailableEventHandler](0-9-430/ICoreWebView2NewBrowserVersionAvailableEventHandler.md)
*   [ICoreWebView2NewWindowRequestedEventHandler](0-9-430/ICoreWebView2NewWindowRequestedEventHandler.md)
*   [ICoreWebView2PermissionRequestedEventHandler](0-9-430/ICoreWebView2PermissionRequestedEventHandler.md)
*   [ICoreWebView2ProcessFailedEventHandler](0-9-430/ICoreWebView2ProcessFailedEventHandler.md)
*   [ICoreWebView2ScriptDialogOpeningEventHandler](0-9-430/ICoreWebView2ScriptDialogOpeningEventHandler.md)
*   [ICoreWebView2SourceChangedEventHandler](0-9-430/ICoreWebView2SourceChangedEventHandler.md)
*   [ICoreWebView2WebMessageReceivedEventHandler](0-9-430/ICoreWebView2WebMessageReceivedEventHandler.md)
*   [ICoreWebView2WebResourceRequestedEventHandler](0-9-430/ICoreWebView2WebResourceRequestedEventHandler.md)
*   [ICoreWebView2WindowCloseRequestedEventHandler](0-9-430/ICoreWebView2WindowCloseRequestedEventHandler.md)
*   [ICoreWebView2ZoomFactorChangedEventHandler](0-9-430/ICoreWebView2ZoomFactorChangedEventHandler.md)
