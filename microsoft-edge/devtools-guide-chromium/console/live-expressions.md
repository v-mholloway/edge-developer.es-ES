---
description: Si te encuentras escribiendo las mismas expresiones de JavaScript en la consola repetidamente, prueba Live Expressions en su lugar.
title: Ver valores de expresión de JavaScript en tiempo real con live expressions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 5bc49b60cc1c1dfb41c793c3fec7681fb6415e4c
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398801"
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

# <a name="watch-javascript-expression-values-in-real-time-with-live-expressions"></a>Ver valores de expresión de JavaScript en tiempo real con live expressions  

Si se encuentra escribiendo la misma expresión de JavaScript en la consola repetidamente, es posible que le resulte más fácil crear **una expresión live**.  Con **Live Expressions,** escribe una expresión una vez y, a continuación, anclarla a la parte superior de la consola.  El valor de la expresión se actualiza casi en tiempo real.  

## <a name="create-a-live-expression"></a>Crear una expresión en directo  

1.  [Abra la consola][DevToolsConsoleReferenceOpenConsole].  
1.  Elija **Crear expresión en directo** \( Crear expresión en directo ![ ][ImageCreateLiveExpressionIcon] \).  Aparece **el cuadro de** texto Expresión en directo.  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Escribir document.activeElement en el cuadro de texto Expresión activa" lightbox="../media/console-create-live-expression.msft.png":::
       Escribir `document.activeElement` en el cuadro de texto **Expresión** en directo  
    :::image-end:::  
    
1.  Seleccione `Control` + `Enter` \(Windows, Linux\) o `Command` + `Enter` \(macOS\) **** para guardar la expresión o elija fuera del cuadro de texto Expresión en directo.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCreateLiveExpressionIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Abra la consola: referencia de consola | Microsoft Docs"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
