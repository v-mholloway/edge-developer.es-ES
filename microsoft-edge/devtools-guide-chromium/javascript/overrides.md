---
description: La característica Invalidaciones es una característica dentro de la herramienta Orígenes de Microsoft Edge DevTools que permite copiar recursos de página web en el disco duro.  Al actualizar la página web, DevTools no carga el recurso, sino que lo reemplaza por la copia local.
title: Invalidar recursos de página web con copias locales con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 7f273f89708e0948e68cd2c7ba79cefb6d7e167c
ms.sourcegitcommit: 2ddfd98d1e871be9c61380a8ca57da398d38bd54
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "11230967"
---
# <a name="override-webpage-resources-with-local-copies-using-microsoft-edge-devtools"></a>Invalidar recursos de página web con copias locales con Microsoft Edge DevTools  

A veces es necesario solucionar un problema en una página web a la que no tiene acceso o las correcciones implican un proceso de compilación lento y complejo.  Puede depurar y corregir todo tipo de problemas en DevTools. Pero el problema es que los cambios no persisten.  Después de actualizar el archivo, todo el trabajo se ha ido.  

La característica Invalidaciones de la [herramienta Orígenes][DevToolsSourcesTool] le ayuda a resolver este problema.  

Ahora puede tomar un recurso de la página web actual y almacenarlo localmente.  Al actualizar la página web, el explorador no carga el recurso desde el servidor.  En su lugar, el explorador lo reemplaza por la copia local del recurso.  

## <a name="setting-up-your-local-folder-to-store-overrides"></a>Configurar la carpeta local para almacenar invalidaciones  

1.  En la **herramienta Orígenes,** busque varias secciones en el lado izquierdo.  Si no **se muestra** la opción Invalidaciones, elija la opción <code>&#x0226B;</code><!--`≫`--> icono para llegar allí.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Herramienta Orígenes sin espacio suficiente para mostrar la opción invalidaciones" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             **Herramienta Orígenes** sin espacio suficiente para mostrar la opción invalidaciones  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Elegir la opción invalidaciones" lightbox="../media/javascript-overrides-menu.msft.png":::
             Elegir la opción invalidaciones  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Después de elegir la **opción Invalidaciones,** debe elegir una carpeta en el equipo local para almacenar los archivos de recursos que desea reemplazar.  Elija la **carpeta + Seleccionar para reemplazos** para buscar una carpeta.  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Elegir una carpeta que se usará para invalidaciones" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       Elegir una carpeta que se usará para invalidaciones  
    :::image-end:::  
    
1.  DevTools le advierte que debe tener acceso total a la carpeta y que no debe revelar información confidencial.  En la barra de advertencias, elija **Permitir** conceder acceso.  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="conceder acceso de DevTools a la carpeta" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       Conceder acceso de DevTools a la carpeta  
    :::image-end:::  
    
1.  En el **panel Invalidaciones,** debe mostrarse una casilla junto a `Enable Local Overrides` y la carpeta invalidaciones.  Se muestra un icono junto a él que permite eliminar la configuración de invalidaciones locales.  Ya ha terminado de configurar la carpeta y está listo para reemplazar los recursos en directo por los locales.
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Configuración correcta de una carpeta de invalidaciones" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       Configuración correcta de una carpeta de invalidaciones  
    :::image-end:::  
    
## <a name="adding-files-to-your-overrides-folder"></a>Agregar archivos a la carpeta Invalidaciones  
  
Para agregar archivos a la carpeta invalidaciones, abra la **herramienta Elementos** e inspeccione la página web.  Para editar, elija el nombre del archivo CSS en el inspector **de estilos.**  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Elegir un archivo en el inspector de estilos" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   Elegir un archivo en el inspector **de estilos**  
:::image-end:::  

En el editor **de** orígenes, mantenga el mouse sobre el nombre del archivo elegido, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Guardar para reemplazos**.  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="En el editor de orígenes, agregue el nombre del archivo a invalidaciones" lightbox="../media/javascript-overrides-file-name.msft.png":::
   En el editor **de** orígenes, agregue el nombre del archivo a invalidaciones  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="En el menú contextual, elija Guardar para invalidaciones" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   En el menú contextual, elija **Guardar para invalidaciones**  
:::image-end:::  

El archivo se almacena en la carpeta invalidaciones.  Compruebe que DevTools cree una carpeta que se denomina mediante la dirección URL del archivo con la estructura de directorio correcta.  El archivo se almacena dentro.  El nombre de archivo del editor ahora también muestra un punto púrpura que indica que el archivo es local y no uno vivo.  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Almacenado correctamente el archivo en la carpeta invalidaciones" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   Almacenado correctamente el archivo en la carpeta invalidaciones  
:::image-end:::  

:::row:::
   :::column span="":::
      En el siguiente ejemplo, ahora puede cambiar los estilos de la página web.  Para agregar un borde rojo alrededor del archivo, en el editor **de estilos,** copie el siguiente estilo y agrégálo al elemento body.  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      El archivo se guarda automáticamente en el equipo.  Si actualiza el archivo, se muestra el borde y no se pierde nada de su trabajo.  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Cambiar los estilos de página web de forma persistente mediante la edición de un archivo en la carpeta invalidaciones" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         Cambiar los estilos de página web de forma persistente mediante la edición de un archivo en la carpeta invalidaciones  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      En la **herramienta Orígenes,** en la sección Página, mantenga el mouse en cualquier archivo, abra el menú contextual \(haga clic con el botón secundario\) y agrégálo a invalidaciones. ****  De nuevo, los archivos que ya están en la carpeta invalidaciones tienen un punto púrpura en el icono.  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Elegir un archivo de la herramienta Orígenes para invalidaciones" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         Elegir un archivo de la **herramienta Orígenes** para invalidaciones  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Como alternativa, en la **herramienta Red,** mantenga el mouse en cualquier archivo, abra el menú contextual \(haga clic con el botón secundario\) y agrégálo a invalidaciones.  Cuando las invalidaciones están en vigor, los archivos que se encuentran en el equipo y no desde la página web en directo.  Cuando las invalidaciones estén en vigor, en la **herramienta Red,** busque un icono de advertencia junto al nombre del archivo.  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Elegir un archivo de la herramienta Red para invalidaciones" lightbox="../media/javascript-overrides-network.msft.png":::
         Elegir un archivo de la **herramienta Red** para invalidaciones  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="two-way-interaction-of-overrides"></a>Interacción en dos sentidos de invalidaciones  

Use el editor proporcionado con la **herramienta Orígenes** de DevTools o cualquier editor que desee cambiar los archivos.  Los cambios se sincronizan en todos los productos que tienen acceso a los archivos de la carpeta invalidaciones.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources/index.md "Información general sobre la herramienta sources | Microsoft Docs"  
