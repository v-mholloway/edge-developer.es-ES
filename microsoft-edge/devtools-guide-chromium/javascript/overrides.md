---
description: La característica de invalidaciones es una característica de la herramienta de orígenes de Microsoft Edge DevTools que le permite copiar recursos de páginas web en su disco duro.  Cuando actualice la página web, DevTools no cargue el recurso, pero reemplácelo con su copia local en su lugar.
title: Invalidar los recursos de páginas web con copias locales con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 579ebe92dc50571837e7e3caf8fb7c1a9989bc59
ms.sourcegitcommit: 9dcaf598f3930bcfab9f93ff63463beb98274de0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "11145211"
---
# Invalidar los recursos de páginas web con copias locales con Microsoft Edge DevTools  

En ocasiones, es necesario solucionar un problema en una página web a la que no tiene acceso o las correcciones implican un proceso de compilación lento y complejo.  Puede depurar y corregir todo tipo de problemas en DevTools. Pero el problema es que los cambios no se conservan.  Después de actualizar el archivo, desaparecerá todo el trabajo.  

La característica de invalidaciones de la herramienta [orígenes][DevToolsSourcesTool] le ayuda a resolver este problema.  

Ahora puede tomar un recurso de la página web actual y almacenarlo de forma local.  Al actualizar la página web, el explorador no carga el recurso desde el servidor.  En su lugar, el explorador lo reemplaza por la copia local del recurso.  

## Configurar la carpeta local para almacenar invalidaciones  

1.  En la herramienta **orígenes** , busque varias secciones en la parte izquierda.  Si no se muestra la opción **sobrescrituras** , elija la <code>&#x0226B;</code><!--`≫`--> icono para ir allí.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Herramienta de orígenes con un espacio insuficiente para mostrar la opción sobrescrituras" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             Herramienta de **orígenes** con un espacio insuficiente para mostrar la opción sobrescrituras  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Herramienta de orígenes con un espacio insuficiente para mostrar la opción sobrescrituras" lightbox="../media/javascript-overrides-menu.msft.png":::
             Elegir la opción de sobrescrituras  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Después de elegir la opción **invalidaciones** , debe elegir una carpeta en el equipo local para almacenar los archivos de recursos que desea reemplazar.  Elija la opción **+ Seleccionar carpeta para reemplazos** para buscar una carpeta.  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Herramienta de orígenes con un espacio insuficiente para mostrar la opción sobrescrituras" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       Elegir una carpeta para reemplazarla  
    :::image-end:::  
    
1.  DevTools le advierte que debe tener acceso total a la carpeta y que no debe revelar información confidencial.  En la barra de advertencia, elija **permitir** para conceder acceso.  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="Herramienta de orígenes con un espacio insuficiente para mostrar la opción sobrescrituras" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       Conceder acceso DevTools a la carpeta  
    :::image-end:::  
    
1.  En el panel **sobrescrituras** , debe aparecer una casilla junto a `Enable Local Overrides` la carpeta invalidaciones.  Aparece un icono junto a ella que le permite eliminar la configuración local de reemplazos.  Ya ha terminado de configurar la carpeta y está listo para reemplazar los recursos en vivo por otros locales.
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Herramienta de orígenes con un espacio insuficiente para mostrar la opción sobrescrituras" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       Configuración correcta de una carpeta de invalidaciones  
    :::image-end:::  
    
## Agregar archivos a la carpeta Overrides  
  
Para agregar archivos a la carpeta Overrides, abra la herramienta **elementos** e inspeccione la Página Web.  Para editar, elija el nombre del archivo CSS en el inspector de **estilos** .  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Herramienta de orígenes con un espacio insuficiente para mostrar la opción sobrescrituras" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   Elegir un archivo en el inspector de **estilos**  
:::image-end:::  

En el editor de **orígenes** , desplace el puntero sobre el nombre de archivo del archivo que ha elegido, abra el menú contextual \ (haga clic con el botón derecho \) y elija **Guardar para reemplazos**.  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="Herramienta de orígenes con un espacio insuficiente para mostrar la opción sobrescrituras" lightbox="../media/javascript-overrides-file-name.msft.png":::
   En el editor de **orígenes** , agregue el nombre del archivo a Overrides  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="Herramienta de orígenes con un espacio insuficiente para mostrar la opción sobrescrituras" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   En el menú contextual, elija **Guardar para reemplazos**  
:::image-end:::  

El archivo se almacena en la carpeta Overrides.  Compruebe que DevTools crear una carpeta cuyo nombre contenga la dirección URL del archivo con la estructura de directorios correcta.  El archivo se almacena en el interior.  El nombre de archivo en el editor ahora también muestra un punto púrpura que indica que el archivo es local y no es dinámico.  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Herramienta de orígenes con un espacio insuficiente para mostrar la opción sobrescrituras" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   El archivo se ha guardado correctamente en la carpeta Overrides  
:::image-end:::  

:::row:::
   :::column span="":::
      En el ejemplo siguiente, puede cambiar ahora los estilos de la Página Web.  Para agregar un borde rojo sobre el archivo, en el editor de **estilos** , copie el estilo siguiente y agréguelo al elemento de cuerpo.  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      El archivo se guardará automáticamente en el equipo.  Si actualiza el archivo, se mostrará el borde y no se perderá nada de su trabajo.  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Herramienta de orígenes con un espacio insuficiente para mostrar la opción sobrescrituras" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         Cambiar los estilos de una página web de forma permanente mediante la edición de un archivo en la carpeta sobrescrituras  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      En la herramienta **orígenes** , en la sección **Página** , mantenga el puntero sobre cualquier archivo, abra el menú contextual \ (haga clic con el botón derecho \) y agréguelo a reemplazos.  De nuevo, los archivos que ya están en la carpeta sobrescrituras tienen un punto púrpura en el icono.  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Herramienta de orígenes con un espacio insuficiente para mostrar la opción sobrescrituras" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         Elegir un archivo de la herramienta **orígenes** para invalidaciones  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Como alternativa, en la herramienta **red** , desplace el puntero sobre cualquier archivo, abra el menú contextual \ (haga clic con el botón derecho \) y agréguelo a reemplazos.  Cuando las invalidaciones son efectivas, los archivos que se encuentran en el equipo y no desde la página web en vivo.  Cuando las invalidaciones estén en vigor, en la herramienta **red** , busque un icono de advertencia junto al nombre del archivo.  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Herramienta de orígenes con un espacio insuficiente para mostrar la opción sobrescrituras" lightbox="../media/javascript-overrides-network.msft.png":::
         Elegir un archivo de la herramienta **red** para invalidaciones  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Interacción bidireccional de invalidaciones  

Use el editor que se proporciona con la herramienta **orígenes** de DevTools o cualquier editor al que desee cambiar los archivos.  Los cambios se sincronizan en todos los productos que tienen acceso a los archivos de la carpeta Overrides.  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources.md "Información general de la herramienta orígenes | Microsoft docs"  
