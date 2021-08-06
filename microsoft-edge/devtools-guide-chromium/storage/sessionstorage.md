---
description: Cómo ver y editar sessionStorage con el panel De Storage sesión y la consola.
title: Ver y editar session Storage con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: a671811e069c11604646ab2ee0d4338013d1dd0b144f01100d8834a5c2255f34
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11809176"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->
# <a name="view-and-edit-session-storage-with-microsoft-edge-devtools"></a>Ver y editar session Storage con Microsoft Edge DevTools  

En esta guía se muestra cómo usar [Microsoft Edge DevTools para][MicrosoftEdgeDevTools] ver, editar y eliminar pares [clave-valor sessionStorage.][MDNSessionStorage]  

## <a name="view-sessionstorage-keys-and-values"></a>Ver claves y valores sessionStorage  

1.  Elija la **pestaña** Aplicación para abrir la **herramienta** Aplicación.  El **** panel Manifiesto se muestra de forma predeterminada.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Panel Manifiesto" lightbox="../media/storage-application-manifest.msft.png":::
       Panel **Manifiesto**  
    :::image-end:::  
    
1.  Expanda el **menú Storage** sesión.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Menú de Storage sesión" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       Menú **de Storage** sesión  
    :::image-end:::  
    
1.  Elija un dominio para ver los pares clave-valor.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Pares clave-valor sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       Pares `sessionStorage` clave-valor  
    :::image-end:::  
    
1.  Elija una fila de la tabla para ver el valor en el visor debajo de la tabla.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Ver el valor de la clave x-sid" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       Ver el valor de la `x-sid` clave  
    :::image-end:::  
    
## <a name="create-a-new-sessionstorage-key-value-pair"></a>Crear un nuevo par clave-valor sessionStorage  

1.  [Ver los pares clave-valor sessionStorage de un dominio](#view-sessionstorage-keys-and-values).  
1.  Haga doble clic en la parte vacía de la tabla.  DevTools crea una nueva fila y centra el cursor en la **columna** Clave.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="La parte vacía de la tabla que se va a hacer doble clic para crear un nuevo par clave-valor" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       La parte vacía de la tabla que se va a hacer doble clic para crear un nuevo par clave-valor  
    :::image-end:::  
    
## <a name="edit-sessionstorage-keys-or-values"></a>Editar claves o valores sessionStorage  

1.  [Ver los pares clave-valor sessionStorage de un dominio](#view-sessionstorage-keys-and-values).  
1.  Haga doble clic en una celda de la **columna Clave** **o** Valor para editar esa clave o valor.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Editar una clave sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       Editar una `sessionStorage` clave  
    :::image-end:::  
    
## <a name="delete-sessionstorage-key-value-pairs"></a>Eliminar pares clave-valor sessionStorage  

1.  [Ver los `sessionStorage` pares clave-valor de un dominio](#view-sessionstorage-keys-and-values).  
1.  Elija el par clave-valor que desea eliminar.  DevTools lo resalta en azul para indicar que está seleccionado.  
1.  Seleccione la `Delete` clave o elija Eliminar **seleccionado** \( Eliminar ![ seleccionado ](../media/delete-icon.msft.png) \).  
    
## <a name="delete-all-sessionstorage-key-value-pairs-for-a-domain"></a>Eliminar todos los pares clave-valor sessionStorage de un dominio  

1.  [Ver los `sessionStorage` pares clave-valor de un dominio](#view-sessionstorage-keys-and-values).  
1.  Elija **Borrar todo** \( Borrar todo ![ ](../media/clear-icon.msft.png) \).  
    
## <a name="interact-with-sessionstorage-from-the-console"></a>Interactuar con sessionStorage desde la consola  

Dado que puede ejecutar JavaScript en **** la consola **y**dado que la consola tiene acceso a los contextos de JavaScript de la página, es posible interactuar con desde `sessionStorage` la **consola**.  

1.  Use el **menú contextos de JavaScript** para **** cambiar el contexto de JavaScript de la consola si desea tener acceso a los pares clave-valor de un dominio distinto de la página en la que `sessionStorage` se encuentra.  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Cambiar el contexto de JavaScript de la consola" lightbox="../media/storage-console-domain-selection.msft.png":::
       Cambiar el contexto de JavaScript de la **consola**  
    :::image-end:::  
    
1.  Ejecute las `sessionStorage` expresiones en la **consola,** lo mismo que su JavaScript.  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Interactuar con sessionStorage desde la consola" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       Interactuar con `sessionStorage` desde la **consola**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Herramientas para desarrolladores | Microsoft Docs"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window.sessionStorage | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
