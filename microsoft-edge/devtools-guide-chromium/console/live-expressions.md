---
description: Si en la consola se encuentra escribiendo las mismas expresiones de JavaScript varias veces, pruebe las expresiones en vivo.
title: Ver valores de expresiones de JavaScript en tiempo real con expresiones en vivo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6b66c44b77cd50bc0c1575e5eceb7c8d1a01b709
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993117"
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





# Ver valores de expresiones de JavaScript en tiempo real con expresiones en vivo   

  

Si se encuentra escribiendo la misma expresión de JavaScript en la consola varias veces, es posible que le resulte más fácil crear una **expresión en vivo**.  Con **expresiones en vivo** , escriba una expresión una vez y, a continuación, ancle en la parte superior de la consola.  El valor de la expresión se actualiza casi en tiempo real.  

## Crear una expresión en directo   

1.  [Abra la consola][DevToolsConsoleReferenceOpenConsole].  
1.  Haga clic en **crear expresión en directo** \ ( ![ crear expresión en directo ][ImageCreateLiveExpressionIcon] \).  Aparece el cuadro de texto de la **expresión en vivo** .  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Escritura de Document. activeElement en el cuadro de texto de la expresión en directo" lightbox="../media/console-create-live-expression.msft.png":::
       Escribir `document.activeElement` en el cuadro de texto de la **expresión en directo**  
    :::image-end:::  
    
1.  Escriba `Control` + `Enter` \ (Windows \) o `Command` + `Enter` \ (MacOS \) para guardar la expresión o haga clic fuera del cuadro de texto de la **expresión en directo** .  

<!--todo: add reference open console (open the console) section when available  -->  

 



<!-- image links -->  

[ImageCreateLiveExpressionIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Abra Consola-referencia de consola | Microsoft docs"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
