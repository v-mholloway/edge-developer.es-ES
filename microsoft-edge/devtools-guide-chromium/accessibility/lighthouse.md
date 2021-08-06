---
description: Probar la accesibilidad con Lighthouse desde DevTools.
title: Probar la accesibilidad con Lighthouse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: b141ad8c2baab1225df0da46a7922c0ebc86d9875153dd9ac671304148d6788c
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11803002"
---
<!-- this article was created on 05/11/2021 by moving a section out from the "Accessibility reference" article (reference.md) -->
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

# <a name="test-accessibility-using-lighthouse"></a>Probar la accesibilidad con Lighthouse

Puede usar Lighthouse desde DevTools para auditar la accesibilidad de una página y generar un informe. Puede usar la herramienta Faro para determinar:

*   Si una página está correctamente marcada para lectores de pantalla.  
*   Si los elementos de texto de una página tienen suficientes relaciones de contraste con el Selector de colores. Para obtener más información, vaya a Probar contraste [de color de texto con el Selector de colores](color-picker.md).   

> [!NOTE]
> La **herramienta Lighthouse** proporciona vínculos al contenido hospedado en sitios web de terceros.  Microsoft no es responsable y no tiene control sobre el contenido de estos sitios ni sobre los datos que se puedan recopilar.  

Para auditar una página con la herramienta Faro, siga estos pasos.

1.  Vaya a la dirección URL que desea auditar.
1.  En DevTools, seleccione la **herramienta Faro.**  Se muestran las opciones de configuración.
    
    :::image type="complex" source="../media/accessibility-lighthouse.msft.png" alt-text="Opciones de configuración de Faro" lightbox="../media/accessibility-lighthouse.msft.png":::
       Opciones de configuración de Faro
    :::image-end:::  
    
1.  Para **Dispositivo**, selecciona **Móvil** si quieres simular un dispositivo móvil.  Esta opción cambia la cadena del agente de usuario y cambia el tamaño de la ventanilla.  Esta opción puede afectar a los resultados de auditoría.
1.  En la **sección Categorías,** seleccione **Accesibilidad**.
1.  Seleccione **Generar informe**. Después de 10 a 30 segundos, DevTools muestra un informe.  El informe ofrece sugerencias sobre cómo mejorar la accesibilidad de la página.  
    
    :::image type="complex" source="../media/accessibility-lighthouse-result.msft.png" alt-text="Un informe de Faro para la categoría Accesibilidad" lightbox="../media/accessibility-lighthouse-result.msft.png":::
       Un informe de Faro para la **categoría Accesibilidad**
    :::image-end:::  
    
1.  Seleccione un elemento en el informe para obtener más información sobre él.  
    
    :::image type="complex" source="../media/accessibility-lighthouse-result-issue-expanded.msft.png" alt-text="Un problema expandido en un informe de Faro" lightbox="../media/accessibility-lighthouse-result-issue-expanded.msft.png":::
       Un problema expandido en un informe de Faro
    :::image-end:::  
    
1.  Seleccione el **vínculo Más información** para ver la documentación del problema.
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Ver la documentación de un problema" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       Ver la documentación de un problema
    :::image-end:::  

1.  Para volver a las opciones de configuración, en DevTools, seleccione **Realizar una auditoría** ( `+` ).    


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  


<!-- links -->  
[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd "axe - Pruebas de accesibilidad web - Chrome Web Store"  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
