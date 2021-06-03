---
description: Proporciona instrucciones sobre cómo personalizar la presentación del botón de revelación de contraseñas
title: Personalizar el botón de revelación de contraseñas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidad, plataforma web, revelación de contraseñas, icono de ojo
ms.openlocfilehash: 93f618d28e5fa2f16dda87b4122a097ef40618c9
ms.sourcegitcommit: 1f0b2534b51417bb19d05945fea54ddad977e88f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2021
ms.locfileid: "11526161"
---
# <a name="customize-the-password-reveal-button"></a>Personalizar el botón de revelación de contraseñas  

El `password` tipo de entrada de Microsoft Edge incluye un control de **revelación de** contraseña.  Un usuario puede elegir el botón **de entrada de** contraseña para revelar el campo **de** contraseña.  El campo contraseña **revelada** ayuda al usuario a comprobar si la contraseña es correcta.  Después de que un **** usuario haya escrito texto **** en el campo de contraseña, un usuario puede elegir el botón de revelación de contraseña o seleccionar para alternar la visibilidad `Alt` + `F8` de la entrada.  

:::row:::
   :::column span="":::
      Campo **de contraseña** con puntos que ocultan los caracteres escritos por un usuario.  El **botón de revelación** de contraseñas aparece a la derecha del campo **de** contraseña.
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-off.msft.png" alt-text="El icono con forma de ojo aparece junto a los puntos que ocultan el texto de la contraseña" lightbox="./media/mdn-demo-password-reveal-off.msft.png":::
         El icono con forma de ojo aparece junto a los puntos que ocultan el texto de la contraseña  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Alterna el **botón de revelación** de contraseña para cambiar el icono de ojo a un icono de ojo con una barra diagonal a través de él y para mostrar el texto de la contraseña original.  
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-on.msft.png" alt-text="El icono con forma de ojo tiene una barra diagonal y se muestra el texto de la contraseña original" lightbox="./media/mdn-demo-password-reveal-on.msft.png":::
         El icono con forma de ojo tiene una barra diagonal y se muestra el texto de la contraseña original :::image-end:::  
   :::column-end:::
:::row-end:::  

De forma predeterminada, **el botón de revelación** de contraseñas se inserta en el DOM de instantánea de todos los elementos HTML `input` con el conjunto en `type` `"password"` .  A partir Microsoft Edge versión 87, los usuarios o [empresas][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] pueden deshabilitar esta característica globalmente.  Usted, diseñadores web y desarrolladores, debe esperar que la mayoría Microsoft Edge usuarios tengan la experiencia predeterminada.  

## <a name="remove-the-password-reveal-control"></a>Quitar el control de revelación de contraseñas  

Puede quitar por completo el botón **de revelación de** contraseñas apuntando al `::-ms-reveal` pseudo elemento.  

```css
::-ms-reveal {
    display: none;
}
```  

Sin embargo, debes considerar aprovechar el botón de revelación **de** contraseñas.  El botón **de revelación de** contraseña nativa tiene importantes [medidas de seguridad](#visibility-of-the-control) integradas en el comportamiento.  

## <a name="customize-the-control-style"></a>Personalizar el estilo de control  

En lugar de quitar completamente el control, puede **** modificar el estilo del botón de revelación de contraseñas para que coincida mejor con el lenguaje visual del sitio web.  El siguiente fragmento de código proporciona un ejemplo de este estilo.  

```css
::-ms-reveal {
    border: 1px solid transparent;
    border-radius: 50%;
    box-shadow: 0 0 3px currentColor;
}
```  

Tenga en cuenta lo siguiente al aplicar estilo al botón **de revelación de** contraseñas.  

*   El icono de ojo se implementa como una imagen de fondo.  Para agregar un color de fondo al **botón** de revelación de contraseña, use la propiedad CSS en lugar de la `background-color` propiedad `background` shorthand.  
*   Puede ajustar el tamaño y la escala del botón de **revelación de** contraseñas.  
    
    > [!NOTE]
    >El explorador oculta cualquier desbordamiento fuera de los límites del control de entrada de contraseña.  
    
*   Actualmente, no hay selectores de estado disponibles para aplicar estilo al estado alternado del botón **de revelación de** contraseña.  
    
## <a name="visibility-of-the-control"></a>Visibilidad del control  

El **botón de revelación** de contraseña no está disponible hasta que el usuario escribe texto en el campo **de** contraseña.  Para ayudar a proteger la entrada de contraseña del usuario, el explorador suprime el botón en los siguientes escenarios.

*   Si el foco se aleja del campo **de contraseña,** el explorador quita el botón **de revelación de** contraseñas.  
*   Si los scripts modifican **el campo de** contraseña, el explorador quita el botón de **revelación de** contraseñas.  

Si se **quita el botón** de revelación de **** contraseña, el usuario debe eliminar el contenido del campo de contraseña antes de que se muestre de nuevo **el** botón de revelación de contraseñas. Este comportamiento impide que alguien haga un ajuste menor para mostrar la contraseña, si el usuario se aleja de un dispositivo desbloqueado.
    
El **botón de revelación** de contraseñas no está disponible si **el** campo de contraseña se rellena automáticamente con el administrador de contraseñas.  

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled]: /deployedge/microsoft-edge-policies#passwordrevealenabled "PasswordRevealEnabled - Microsoft Edge- Directivas | Microsoft Docs"  
