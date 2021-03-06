---
description: Obtenga información sobre cómo empaquetar la extensión .
title: 'Extensiones: empaquetado'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/28/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
keywords: edge, web development, html, css, javascript, developer
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 62c7858c38cf0c06e24c25938a885b10b391fd8f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398500"
---
# <a name="packaging-microsoft-edge-extensions"></a>Empaquetar extensiones de Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Por lo tanto, por fin ha completado la extensión y está listo para empaquetar. Es posible que se pregunte cuáles son los pasos siguientes para obtener esto en manos de los usuarios potenciales. Esta guía está diseñada para enseñarte a hacerlo.  

La guía de empaquetado de extensiones es completa, ya que cubre todo lo que quieres saber sobre el empaquetado, incluso los detalles más finos y ingeniosos. Si no quieres aprender todo lo que hay que saber sobre empaquetar la extensión, tienes suerte. Hemos agregado compatibilidad con extensiones a ManifoldJS, una herramienta de código Node.js de código abierto que quita la mayoría de los problemas de empaquetado.  

> [!NOTE]
> Enviar una extensión de Microsoft Edge a la Microsoft Store es actualmente una funcionalidad restringida. [Llámenos con](https://developer.microsoft.com/en-us/microsoft-edge/extensions/requests) sus solicitudes para formar parte de Microsoft Store y le consideraremos para una actualización futura.  

Usa el esquema de proceso siguiente para asignar la aventura de empaquetado.  

## [<a name="extensions-in-the-windows-dev-center"></a>Extensiones en el centro de desarrollo de Windows](./packaging/extensions-in-the-windows-dev-center.md)  

Independientemente de la ruta de creación de paquetes que elijas, manual o ManifoldJS, el primer paso es registrarte para una cuenta de Desarrollador de Windows y reservar los nombres de la extensión.  

Una vez hecho esto, puede pasar [](./packaging/creating-and-testing-extension-packages.md) a Crear y probar paquetes de extensión para obtener información sobre cómo se crean los AppX y empaquetan manualmente la extensión, o bien ir a la ruta más fácil y saltar a [Usar ManifoldJS](./packaging/using-ManifoldJS-to-package-extensions.md)para empaquetar extensiones .  

> [!NOTE]
> Una vez que te hayas puesto en contacto con nosotros y hayas recibido la aprobación para tener la extensión en microsoft Store, consulta la lista de comprobación [de envío de aplicaciones](https://docs.microsoft.com/windows/uwp/publish/app-submissions).  


## [<a name="creating-and-testing-extension-packages"></a>Crear y probar paquetes de extensión](./packaging/creating-and-testing-extension-packages.md)  

En esta sección de la guía se muestra la creación manual de paquetes de extensión una vez que hayas configurado tu cuenta de Desarrollador de Windows y reservados los nombres de [extensión.](./packaging/extensions-in-the-windows-Dev-Center.md) Si tienes curiosidad por los detalles más finos de empaquetar una extensión, dale una lectura.  

También se incluye información sobre cómo [probar y desempaquetar una extensión empaquetada.](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) Esta información es relevante incluso si has pasado la ruta de empaquetado manifoldJS.  

## [<a name="localizing-extension-packages"></a>Localizar paquetes de extensión](./packaging/localizing-extension-packages.md)  

El paso de localización del paquete se encuentra entre crear el archivo appxmanifest.xml y ejecutar el comando final para empaquetar la extensión.  
Esto te permite indicar qué idiomas admiten tus extensiones en la descripción de Microsoft Store y qué idioma aparece el nombre de la extensión en Windows.  

Puedes ir a [Localizing name and description for the Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) en esta sección de la guía si la extensión no admite varios idiomas.  

## [<a name="using-manifoldjs-to-package-extensions"></a>Usar ManifoldJS para empaquetar extensiones](./packaging/using-ManifoldJS-to-package-extensions.md)  

La ruta de herramientas para empaquetar la extensión, ManifoldJS empaquetará la extensión en un instante con el mínimo esfuerzo en el extremo. Proporciona algunos activos de Windows/Microsoft Store después de rellenar algunas propiedades de AppXManifest y la extensión se empaquetará en poco tiempo.  

Una vez empaquetada la [](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) extensión, consulta la sección de pruebas de Crear y probar la extensión de Microsoft Edge para obtener información sobre cómo descargarla o desempaquetarla.  

## [<a name="running-the-windows-app-certification-kit"></a>Ejecutar el kit para la certificación de aplicaciones en Windows](./packaging/running-the-windows-app-certification-kit.md)  

Una vez que tenga una extensión empaquetada, puede ejecutarla a través del Kit de certificación de aplicaciones de Windows. Al hacerlo, se ejecutarán varias pruebas en el paquete de extensión para asegurarse de que está listo para la Microsoft Store.  
