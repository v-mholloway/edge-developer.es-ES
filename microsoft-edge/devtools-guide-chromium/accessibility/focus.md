---
title: Rastrear qué elemento tiene el foco
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 5261824b725384240453f216071255494e88e98d
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991172"
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

# Rastrear qué elemento tiene el foco  

Suponga que está probando la accesibilidad de navegación por el teclado de una página.  Al navegar por la página con la `Tab` tecla, el anillo de foco desaparece a veces, porque el elemento que tiene el foco está oculto.  

Complete las acciones siguientes para realizar un seguimiento del elemento que tiene el foco en DevTools.  

1.  Abra la **consola**.  
1.  Haga clic en **crear expresión en directo** \ ( ![ crear expresión en directo ][ImageCreateIcon] \).  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Crear una expresión en directo" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       Crear una expresión en directo  
    :::image-end:::  
    
1.  Escribe `document.activeElement`.  
1.  Haga clic fuera de la interfaz de usuario de **Live Expression** para guardar.  
    
El valor que se ve a continuación `document.activeElement` es el resultado de la expresión.  

Dado que esa expresión siempre representa el elemento que tiene el foco, ahora tienes una manera de realizar un seguimiento de qué elemento tiene el foco.  

*   Desplace el puntero sobre el resultado para resaltar el elemento que tiene el foco en la ventanilla.  
*   Haga clic con el botón derecho en el resultado y seleccione Mostrar **en el panel de elementos** para mostrar el elemento en el árbol DOM en el panel **elementos** .  
*   Haga clic con el botón secundario en el resultado y seleccione **almacenar como variable global** para crear una referencia de variable al nodo que se puede usar en la **consola**.  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCreateIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
