---
description: Referencia del protocolo DevTools versión 0.1 (EdgeHTML) para el dominio de esquema. Proporciona información sobre el esquema de protocolo.
title: 'Dominio de esquema: protocolo DevTools versión 0.1 (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e89f4269b4984ee49e83a23fcab9679485c49040
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398864"
---
# <a name="schema-domain---devtools-protocol-version-01-edgehtml"></a>Dominio de esquema: protocolo DevTools versión 0.1 (EdgeHTML)  

Proporciona información sobre el esquema de protocolo.  

| Clasificación | Miembros |  
|:--- |:--- |  
| [Métodos](#methods) | [getDomains](#getdomains) |  
| [Tipos](#types) | [Dominio](#domain) |  

## <a name="methods"></a>Métodos  

### <a name="getdomains"></a>getDomains  

Devuelve dominios admitidos.  

| Devuelve | Tipo | Detalles |  
|:--- |:--- |:--- |  
| dominios | [Dominio[]](#domain) | Lista de dominios admitidos. |  

---  

## <a name="types"></a>Tipos  

### <a name="domain-object"></a>Domain (objeto)  

<a name="domain"></a>  

Descripción del dominio de protocolo.  

| Propiedades | Tipo | Detalles |  
|:--- |:--- |:--- |  
| name | `string` | Nombre de dominio. |  
| version | `string` | Versión de dominio. |  

---  
