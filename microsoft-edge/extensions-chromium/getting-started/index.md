---
description: Obtenga información sobre las extensiones de cromo y los conceptos básicos para crear extensiones.
title: Conceptos y arquitectura de las extensiones de Microsoft Edge (cromo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/01/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge-cromo, desarrollo web, HTML, CSS, JavaScript, desarrollador, extensiones
ms.openlocfilehash: 8ffdd19e1a1e36a4d10fdd80bd7dd5654d543527
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104731"
---
# Conceptos y arquitectura de extensión

Este artículo proporciona una breve introducción a los conceptos que ayudan al crear extensiones. Para comprender las extensiones de Microsoft Edge \ (cromo \), veremos cómo funcionan los exploradores de varias pestañas.


## Comprender cómo funcionan los exploradores

En la siguiente lista se describe información útil para comprender antes de crear la extensión.

1.  Cada pestaña del explorador está aislada de cada una de las pestañas.  Cada pestaña se ejecuta en su propio subproceso que está aislado de otras pestañas y subprocesos del explorador.

    ![Un hilo por ficha de explorador](media/index-image1-browsertabs.png)  

2.  Cada pestaña administra una solicitud GET.  Cada pestaña usa una dirección URL para obtener una única secuencia de datos, que normalmente es un documento HTML.  Esa secuencia o página en un solo paso incluye instrucciones como, por ejemplo, las etiquetas, referencias de imagen, referencias CSS y mucho más.  Todos los recursos se descargan en una página de pestaña y, a continuación, se representa la página en la pestaña.  

3.  La comunicación se produce entre cada pestaña y los servidores remotos.  Cada pestaña se ejecuta en un entorno aislado. Aún están conectados a Internet, pero están aislados de otras pestañas.  Las tabulaciones pueden ejecutar JavaScript para comunicarse con los servidores. Estos servidores son el servidor de origen de la primera solicitud GET que se especificó en la barra de direcciones URL de la pestaña.  

4.  El modelo de extensión usa un modelo de comunicación diferente.  De forma similar a las páginas de pestañas, las extensiones se ejecutan en subprocesos individuales que están aislados de todos los subprocesos de la página  Las pestañas emiten una sola solicitud GET a los servidores remotos y, a continuación, procesa la página. Sin embargo, Extensions funciona de forma similar a un servidor remoto. La instalación de extensiones en el explorador crea un servidor web independiente en el explorador. La extensión está aislada de todas las páginas de pestañas.  

    ![Las extensiones usan un modelo de comunicación diferente](media/index-image3-upsidedown.png)  

## Arquitectura de extensión

En la siguiente lista se describe información útil en relación con la arquitectura de una extensión.  

1.  El paquete de servidor Web de extensión.  Una extensión es un paquete de recursos Web. Estos recursos web son similares a otros recursos que los desarrolladores web publican en servidores Web. Los desarrolladores empaquetan estos recursos Web en un archivo zip al crear una extensión.
    
    El archivo zip incluye archivos HTML, CSS, JavaScript e imágenes.  Hay un archivo adicional necesario en la raíz del archivo zip. Este archivo es el archivo de manifiesto y se denomina `manifest.json` .  Es el Blueprint de tu extensión e incluye la versión de tu extensión, el título, los permisos necesarios para que se ejecute la extensión y así sucesivamente.

2.  Iniciar el servidor de extensiones.  Los servidores web contienen tu paquete Web. Los exploradores navegan a las direcciones URL en el servidor y descargan el archivo para representarlo en el explorador. Los exploradores navegan mediante certificados, archivos de configuración, etc.  Si hay un `index.html` archivo, se almacena en una ubicación especial en el servidor Web.  

    Cuando usamos extensiones, la página de pestañas de tu explorador llega al conjunto Web de tu extensión con el tiempo de ejecución de la extensión.  La extensión Runtime da servicio a los archivos de la dirección URL `extension://{some-long-unique-identifier}/index.html` , donde `{some-long-unique-identifier}` es un identificador único asignado a la extensión cuando se instala.  Cada extensión usa un identificador único diferente. Cada identificador apunta al paquete web que está instalado en el explorador.   

3.  Las extensiones pueden comunicarse con pestañas y la barra de herramientas del explorador.   Las extensiones pueden interactuar con la barra de herramientas de tu explorador. Cada extensión administra páginas de pestañas en ejecución en subprocesos independientes y aísla la manipulación de DOM en cada página de pestaña.  Las extensiones usan la API de extensiones para comunicarse entre la extensión y las páginas de pestañas.  Esta API de extensión proporciona capacidades adicionales que incluyen administración de notificaciones, administración de almacenamiento, etc.  

    Al igual que los servidores Web, las extensiones esperan en las notificaciones cuando el explorador está abierto.  Las páginas de extensiones y fichas se ejecutan en subprocesos que están aislados entre sí. Sin embargo, los desarrolladores pueden usar la API de extensiones y permisos en el archivo de manifiesto para permitir que una extensión funcione con cualquier página de pestaña.  

4. Las extensiones proporcionan permisos de participación en el momento de la instalación.  El desarrollador especifica los permisos de extensión en el `manifest.json` archivo. Al instalar extensiones, se muestra a los usuarios información sobre los permisos que la extensión necesita para ejecutarse. Según el tipo de permiso requerido, la extensión puede extraer y usar información del explorador.


## Pasos siguientes

 Para obtener información sobre cómo empezar a usar extensiones, vea [crear un tutorial de extensión][CreateAnExtensionPart1]. 



<!-- image links -->  

<!-- links -->  

[CreateAnExtensionPart1]: ./part1-simple-extension.md "Crear un tutorial de extensión: parte 1 | Microsoft docs"  