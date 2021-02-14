---
description: Proporciona instrucciones para personalizar la visualización del botón mostrar contraseñas
title: Personalizar el botón mostrar contraseña
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidad, plataforma web, mostrar contraseña, icono de ojo
ms.openlocfilehash: af8120aad7316ffc051113591e770fa913814eb3
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327729"
---
# Personalizar el botón mostrar contraseña  

El `password` tipo de entrada en Microsoft Edge incluye un control de **revelación de** contraseñas.  Un usuario puede elegir el botón **de entrada de** contraseña para mostrar el campo **de** contraseña.  El campo de **contraseña revelada** ayuda al usuario a comprobar si la contraseña es correcta.  Una vez que un **** usuario ha escrito texto **** en el campo de contraseña, un usuario puede elegir el botón mostrar contraseña o seleccionar para alternar la `Alt` + `F8` visibilidad de la entrada.  

:::row:::
   :::column span="":::
      Un **campo de** contraseña con puntos que ocultan los caracteres escritos por un usuario.  El **botón Mostrar** contraseña aparece a la derecha del campo **de** contraseña.
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-off.msft.png" alt-text="El icono con forma de ojo aparece junto a los puntos que ocultan el texto de la contraseña" lightbox="./media/mdn-demo-password-reveal-off.msft.png":::
         El icono con forma de ojo aparece junto a los puntos que ocultan el texto de la contraseña  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Alterna el **botón mostrar** contraseña para cambiar el icono de ojo a un icono de ojo con una barra diagonal y para mostrar el texto de la contraseña original.  
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-on.msft.png" alt-text="El icono con forma de ojo tiene una barra diagonal y se muestra el texto de la contraseña original" lightbox="./media/mdn-demo-password-reveal-on.msft.png":::
         El icono con forma de ojo tiene una barra diagonal y se muestra el texto de la contraseña original :::image-end:::  
   :::column-end:::
:::row-end:::  

De forma predeterminada, **el botón mostrar** contraseña se inserta en el DOM de sombra de todos los elementos HTML con el conjunto en `input` `type` `"password"` .  A partir de la versión 87 de Microsoft Edge, los usuarios o [empresas][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] pueden deshabilitar esta característica globalmente.  Usted, los diseñadores web y los desarrolladores, deben esperar que la mayoría de los usuarios de Microsoft Edge tengan la experiencia predeterminada.  

## Quitar el control de revelación de contraseñas  

Puedes quitar por completo el botón **para mostrar** contraseñas apuntando al `::-ms-reveal` pseudo elemento.  

```css
::-ms-reveal {
    display: none;
}
```  

Sin embargo, debes considerar la posibilidad de aprovechar el botón **para mostrar la** contraseña.  El botón **mostrar contraseña** nativa tiene importantes [medidas de seguridad integradas](#visibility-of-the-control) en el comportamiento.  

## Personalizar el estilo de control  

En lugar de quitar completamente el control, puede **** modificar el estilo del botón mostrar contraseña para que coincida mejor con el lenguaje visual del sitio web.  El siguiente fragmento de código proporciona un ejemplo de este estilo.  

```css
::-ms-reveal {
    border: 1px solid transparent;
    border-radius: 50%;
    box-shadow: 0 0 3px currentColor;
}
```  

Ten en cuenta lo siguiente al aplicar estilo al botón **Mostrar** contraseña.  

*   El icono de ojo se implementa como una imagen de fondo.  Para agregar un color de fondo al **botón** Mostrar contraseña, usa la propiedad CSS en lugar de `background-color` la propiedad `background` abreviada.  
*   Puedes ajustar el tamaño y la escala del botón mostrar **contraseña.**  
    
    > [!NOTE]
    >El explorador oculta cualquier desbordamiento fuera de los límites del control de entrada de contraseña.  
    
*   Actualmente, no hay selectores de estado disponibles para aplicar estilo al estado de alternancia del botón **mostrar contraseña.**  
    
## Visibilidad del control  

El **botón mostrar** contraseña no está disponible hasta que el usuario escribe texto en el campo **de** contraseña.  Para ayudar a proteger la entrada de contraseña del usuario, el explorador suprime el botón en los siguientes escenarios.

*   Si el foco se aleja del campo **de contraseña,** el explorador quita el botón **mostrar contraseña.**  
*   Si los scripts modifican **el campo de** contraseña, el explorador quita el botón mostrar **contraseña.**  
*   Si un usuario quita el **botón** mostrar contraseña, el **** usuario debe **** eliminar el contenido del campo de contraseña antes de que el botón mostrar contraseña se muestre de nuevo.  
    
    > [!NOTE]
    > Esta característica impide que alguien haga un pequeño ajuste para ver la contraseña, en caso de que el usuario salga de un dispositivo desbloqueado.
    
El **botón mostrar** contraseña no está disponible si el campo de contraseña se rellena automáticamente con el administrador de contraseñas. ****  

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled]: /deployedge/microsoft-edge-policies#passwordrevealenabled "PasswordRevealEnabled - Microsoft Edge - Directivas | Microsoft Docs"  
