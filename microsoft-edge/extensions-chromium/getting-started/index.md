---
description: Obtenga información sobre Chromium y conceptos básicos para crear extensiones.
title: Microsoft Edge (Chromium) Conceptos y arquitectura de extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo web, html, css, javascript, desarrollador, extensiones
ms.openlocfilehash: 05732287bc1a782ed5830d5e7028cf5580f3b605
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397928"
---
# <a name="extension-concepts-and-architecture"></a>Conceptos de extensión y arquitectura  

En este artículo se proporciona una breve introducción a los conceptos que le ayudarán a crear una extensión.  Para comprender Microsoft Edge extensiones \(Chromium\), siga este procedimiento para comprender cómo funcionan los exploradores de varias pestañas.  

## <a name="understand-how-browsers-work"></a>Comprender cómo funcionan los exploradores  

En la siguiente lista se describe información útil para comprender antes de crear la extensión.  

1.  Cada pestaña del explorador está aislada de todas las demás pestañas.  Cada pestaña se ejecuta en un subproceso independiente que está aislado de otras pestañas y subprocesos del explorador.  
    
    :::image type="complex" source="./media/index-image1-browsertabs.png" alt-text="Una pestaña de un subproceso por explorador" lightbox="./media/index-image1-browsertabs.png":::
       Una pestaña de un subproceso por explorador  
    :::image-end:::  
    
1.  Cada pestaña controla una solicitud GET.  Cada pestaña usa una dirección URL para obtener una sola secuencia de datos, que normalmente es un documento HTML.  Esa única secuencia o página incluye instrucciones como JavaScript, etiquetas, referencias de imagen, referencias CSS y mucho más.  Todos los recursos se descargan en esa página de una pestaña y, a continuación, la página se representa en la pestaña.  
1.  La comunicación se produce entre cada pestaña y un servidor remoto.  Cada pestaña se ejecuta en un entorno aislado.  Cada pestaña todavía está conectada a Internet, pero cada una está aislada de otras pestañas.  Una pestaña puede ejecutar JavaScript para comunicarse con un servidor.  El servidor es el servidor de origen de la primera solicitud GET que se introdujo en la barra de direcciones URL de la pestaña.  
1.  El modelo de extensión usa un modelo de comunicación diferente.  De forma similar a una página de pestaña, una extensión se ejecuta en un subproceso individual que está aislado de otros subprocesos de página de pestañas.  Una pestaña envía solicitudes GET únicas a servidores remotos y, a continuación, representa la página.  Sin embargo, una extensión funciona de forma similar a un servidor remoto.  Al instalar una extensión en un explorador, se crea un servidor web independiente en el explorador.  La extensión está aislada de todas las páginas de pestañas.  
    
    :::image type="complex" source="./media/index-image3-upsidedown.png" alt-text="Las extensiones usan un modelo de comunicación diferente" lightbox="./media/index-image3-upsidedown.png":::
       Las extensiones usan un modelo de comunicación diferente  
    :::image-end:::  
    
## <a name="extension-architecture"></a>Arquitectura de extensión de RIS  

En la siguiente lista se describe información útil en relación con la arquitectura de una extensión.  

1.  El paquete del servidor web de extensión.  Una extensión es un conjunto de recursos web.  Los recursos web son similares a otros recursos que \(el desarrollador web\) publica en servidores web.  Los recursos web se agrupan en un archivo zip al compilar una extensión.  
    
    El archivo zip incluye html, CSS, JavaScript y archivos de imagen.  Se requiere un archivo más en la raíz del archivo zip.  El otro archivo es el archivo de manifiesto denominado `manifest.json` .  El archivo de manifiesto es el plano de la extensión e incluye la versión de la extensión, el título, los permisos necesarios para que se ejecute la extensión, y así sucesivamente.  
    
1.  Iniciar el servidor de extensión.  Los servidores web contienen el paquete web.  Un explorador navega a las direcciones URL del servidor y descarga el archivo para representarlo en el explorador.  Un explorador navega con certificados, archivos de configuración, y así sucesivamente.  Si se `index.html` especifica un archivo, el archivo se almacena en una ubicación especial en el servidor web.  
    
    Cuando se usa una extensión, la página de pestañas del explorador llega al paquete web de la extensión mediante el tiempo de ejecución de extensión.  El tiempo de ejecución de extensión sirve los archivos desde la dirección URL, donde es un identificador `extension://{some-long-unique-identifier}/index.html` único asignado a la extensión durante la `{some-long-unique-identifier}` instalación.  Cada extensión usa un identificador único diferente.  Cada identificador apunta a la agrupación web que está instalada en el explorador.  
    
1.  Una extensión puede comunicarse con pestañas y la barra de herramientas del explorador.  Una extensión puede interactuar con la barra de herramientas del explorador.  Cada extensión administra las páginas de tabulación en ejecución en subprocesos independientes y la manipulación de DOM en cada página de pestaña está aislada.  Una extensión usa la API de extensiones para comunicarse entre las páginas de la extensión y la pestaña.  La API de extensiones proporciona capacidades adicionales que incluyen administración de notificaciones, administración de almacenamiento, entre otras.  
    
    Al igual que los servidores web, una extensión espera las notificaciones cuando el explorador está abierto.  Las páginas de extensión y tabulación se ejecutan en subprocesos aislados entre sí.  Para permitir que una extensión funcione con cualquier página de pestaña, use la API de extensiones y establezca los permisos en el archivo de manifiesto.  
    
1.  Una extensión proporciona permisos de suscripción en el momento de la instalación.  Especifique los permisos de extensión en el `manifest.json` archivo.  Cuando un usuario instala una extensión, se muestra información sobre los permisos que requiere la extensión.  En función del tipo de permiso requerido, la extensión puede extraer y usar información del explorador.  
    
## <a name="next-steps"></a>Pasos siguientes  

Para obtener información sobre cómo empezar a usar la extensión, vaya [a Crear un tutorial de extensión][CreateAnExtensionPart1].  

<!-- links -->  

[CreateAnExtensionPart1]: ./part1-simple-extension.md "Crear un tutorial de extensión: parte 1 | Microsoft Docs"  
