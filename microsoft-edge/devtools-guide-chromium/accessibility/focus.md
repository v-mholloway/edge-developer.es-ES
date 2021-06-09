---
description: Abra la consola, cree una expresión en directo y establezca la expresión en document.activeElement.
title: Rastrear qué elemento tiene el foco
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 2fd53caccefefb0b0bce4b5c82f30632e11a3cb6
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597105"
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
# <a name="track-which-element-has-focus"></a>Rastrear qué elemento tiene el foco  

Supongamos que está probando la accesibilidad de navegación del teclado de una página.  Al navegar por la página con la clave, el anillo de enfoque a veces desaparece porque `Tab` el elemento que tiene el foco está oculto.  

Para realizar un seguimiento del elemento centrado en DevTools:

1.  Abra la **consola**.  
1.  Elija **Crear expresión en directo** \( Crear expresión en directo ![ ](../media/create-live-expression-icon.msft.png) \).  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Crear una expresión en directo" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       Crear una expresión en directo  
    :::image-end:::  
    
1.  Escriba `document.activeElement`.  
1.  Para guardar la expresión, seleccione fuera de la expresión en directo.
    
El valor que se muestra `document.activeElement` a continuación es el resultado de la expresión.  

Dado que esa expresión siempre representa el elemento centrado, ahora tiene una forma de realizar siempre un seguimiento de qué elemento tiene el foco.  

*   Mantenga el mouse sobre el resultado para resaltar el elemento centrado en la ventanilla.  
*   Mantenga el mouse sobre el resultado, abra el menú contextual \(clic con el botón derecho\) y elija Mostrar en el **panel** Elementos para mostrar el elemento en el árbol DOM de la **herramienta** Elementos.  
*   Mantenga el mouse sobre el resultado, abra el menú contextual \(haga clic con el botón secundario\) y elija Almacenar como **variable global** para crear una referencia variable al nodo que puede usar en la **consola**.  


## <a name="see-also"></a>Consulta también

*  [Analizar la falta de indicación del foco del teclado en un menú lateral](test-analyze-no-focus-indicator.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->  
> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
