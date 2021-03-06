---
description: Referencia del protocolo DevTools versión 0.2 (EdgeHTML) para el dominio de esquema. Proporciona información sobre el esquema de protocolo.
title: 'Dominio de esquema: protocolo DevTools versión 0.2 (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6844939f452bc96980d6d67d4652adcc7c078c7a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398150"
---
# <a name="schema-domain---devtools-protocol-version-02-edgehtml"></a>Dominio de esquema: protocolo DevTools versión 0.2 (EdgeHTML)  

Proporciona información sobre el esquema de protocolo.  

| Clasificación | Miembros |  
|:--- |:--- |  
| [Métodos](#methods) | [getDomains](#getdomains) |  
| [Tipos](#types) | [Domain (objeto)](#domain) |  

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
