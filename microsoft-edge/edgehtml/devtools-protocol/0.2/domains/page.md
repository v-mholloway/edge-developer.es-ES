---
description: Referencia del protocolo DevTools versión 0.2 (EdgeHTML) para el dominio de página. Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de página.
title: 'Dominio de página: protocolo DevTools versión 0.2 (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d969dd100164ace61445a4618174cfa943dcfd2b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398850"
---
# <a name="page-domain---devtools-protocol-version-02-edgehtml"></a>Dominio de página: protocolo DevTools versión 0.2 (EdgeHTML)  

Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de página.  

| Clasificación | Miembros |  
|:--- |:--- |  
| [Métodos](#methods) | [enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree) |  
| [Eventos](#events) | [frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired) |  
| [Tipos](#types) | [FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree) |  

## <a name="methods"></a>Métodos  

### <a name="enable"></a>habilitar  

Habilita las notificaciones de dominio de página.  

&nbsp;  

---  

### <a name="disable"></a>deshabilitar   

Deshabilita las notificaciones de dominio de página.  

&nbsp;  

---  

### <a name="navigate"></a>navegar  

Navega a la página actual a la dirección URL determinada.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| url | `string` | DIRECCIÓN URL para navegar por la página. |  
| frameId \(optional\) | [FrameId](#frameid) | Id. de marco para navegar.  Si no se especifica, navegará por la página superior. |  

| Devuelve | Tipo | Detalles |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | Identificador de marco que se navegará. |  

---  

### <a name="getframetree"></a>getFrameTree  

Devuelve la estructura del árbol de marco actual.  

| Devuelve | Tipo | Detalles |  
|:--- |:--- |:--- |  
| frameTree | [FrameTree](#frametree) | Presentar estructura de árbol de marco. |  

---  

## <a name="events"></a>Eventos  

### <a name="frameattached"></a>frameAttached  

Se desencadena cuando el marco se ha unido a su elemento primario.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | Id. del marco que se ha adjuntado. |  
| parentFrameId | [FrameId](#frameid) | Identificador de fotograma primario. |  
| stack \(optional\) | [Runtime.StackTrace](./runtime.md#stacktrace) | Seguimiento de pila de JavaScript de cuándo se adjunta el marco, solo se establece si el marco se inicia desde el script. |  

---  

### <a name="framedetached"></a>frameDetached  

Se desencadena cuando se ha desasociado el marco de su elemento primario.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | Identificador del marco que se ha desasociado. |  

---  

### <a name="framenavigated"></a>frameNavigated  

Se desencadena una vez completada la navegación del marco.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| marco | [Marco](#frame) | Frame (objeto). |  

---  

### <a name="loadeventfired"></a>loadEventFired  

Corresponde al `window.onload` evento.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| marca de tiempo | `number` | Número de milisegundos desde la época. |  

---  

### <a name="domcontenteventfired"></a>domContentEventFired  

Corresponde al `document.onDOMContentLoaded` evento.  

| Parameters | Tipo | Detalles |  
|:--- |:--- |:--- |  
| marca de tiempo | `number` | Número de milisegundos desde la época. |  

---  

## <a name="types"></a>Tipos  

### <a name="frameid-string"></a>Cadena FrameId  

<a name="frameid"></a>  

Identificador de fotograma único.  

&nbsp;  

---  

### <a name="frame-object"></a>Frame (objeto)  

<a name="frame"></a>  

Información sobre el marco de la página.  

| Propiedades | Tipo | Detalles |  
|:--- |:--- |:--- |  
| id | [FrameId](#frameid) | Identificador único de marco. |  
| parentId \(optional\) | [FrameId](#frameid) | Identificador único del marco primario. |  
| nombre \(optional\) | `string` | Nombre del marco tal como se especifica en la etiqueta. |  
| url | `string` | Dirección URL del documento de marco. |  
| securityOrigin | `string` | Origen de seguridad del documento de marco. |  
| mimeType | `string` | Frame mimeType del documento según lo determinado por el explorador. |  

---  

### <a name="frametree-object"></a>FrameTree (objeto)  

<a name="frametree"></a>  

Información sobre la jerarquía frame.  

| Propiedades | Tipo | Detalles |  
|:--- |:--- |:--- |  
| marco | [Marco](#frame) | Información de marco para este elemento de árbol. |  
| childFrames \(optional\) | [FrameTree[]](#frametree) | Fotogramas secundarios. |  

---  
