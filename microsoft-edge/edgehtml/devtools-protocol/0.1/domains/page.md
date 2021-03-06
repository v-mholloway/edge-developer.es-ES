---
description: Referencia del protocolo DevTools versión 0.1 (EdgeHTML) para el dominio de página. Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de página.
title: 'Dominio de página: protocolo DevTools versión 0.1 (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b04b0685a6b465d40e999a2a48d370573a3058d8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399151"
---
# <a name="page-domain---devtools-protocol-version-01-edgehtml"></a>Dominio de página: protocolo DevTools versión 0.1 (EdgeHTML)  

Las acciones y eventos relacionados con la página inspeccionada pertenecen al dominio de página.  

| Clasificación | Miembros |  
|:--- |:--- |  
| [**Métodos**](#methods) | [enable](#enable), [disable](#disable), [navigate](#navigate) |  
| [**Tipos**](#types) | [FrameId](#frameid) |  

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

| Devuelve | Tipo | Detalles |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | **Experimental**.  Identificador de fotograma que se navegará. |  

---  

## <a name="types"></a>Tipos  

### <a name="frameid-string"></a>Cadena FrameId  

<a name="frameid"></a>  

Identificador de fotograma único.  

&nbsp;  

---  
