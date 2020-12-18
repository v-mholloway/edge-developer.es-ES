---
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
description: Más información sobre cómo empaquetar tu extensión.
title: 'Extensiones: empaquetado'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0ea4d6a4450d47d116164fd8481fdfb0f79bd30b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236496"
---
# Empaquetar las extensiones de Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Por eso, finalizaste la ampliación y estás listo para empaquetarla. Es posible que se pregunte cuál es el procedimiento siguiente para obtener esta información en manos de posibles usuarios. La finalidad de esta guía es enseñarle a hacerlo.

La guía de empaquetado de la extensión es completa, ya que cubre todo lo que necesita saber sobre el embalaje, incluso los detalles más precisos. Si no deseas conocer todo lo que hay que saber sobre cómo empaquetar tu extensión, ya estás de suerte. Hemos agregado compatibilidad con extensiones a ManifoldJS, una herramienta de código abierto Node.js que toma la mayoría de tus woess de embalaje.

> [!NOTE]
> El envío de una extensión de Microsoft Edge a Microsoft Store es actualmente una función restringida. Póngase en [contacto con nosotros](https://aka.ms/extension-request) con sus solicitudes para formar parte de Microsoft Store y le daremos una actualización futura.


Usa el siguiente Resumen de proceso para diseñar la aventura de empaquetar.


## [Extensiones en el centro de desarrollo de Windows](./packaging/extensions-in-the-windows-dev-center.md)

Independientemente del camino de creación de paquetes que elija, manual o ManifoldJS, el primer paso es registrarse para una cuenta de Windows Developer y reservar el nombre o los nombres de la extensión.

Una vez que lo haya hecho, puede continuar con la [creación y la prueba de paquetes de extensión](./packaging/creating-and-testing-extension-packages.md) para obtener información sobre cómo se crean AppXs y empaquetar manualmente la extensión, o ir a la ruta de acceso más sencilla y saltarse a [usar ManifoldJS para empaquetar extensiones](./packaging/using-ManifoldJS-to-package-extensions.md).

> [!NOTE]
> Una vez que haya llegado a nosotros y haya sido aprobado para tener su extensión en Microsoft Store, consulte la lista de [comprobación de envío](https://docs.microsoft.com/windows/uwp/publish/app-submissions)de la aplicación.


## [Crear y probar paquetes de extensión](./packaging/creating-and-testing-extension-packages.md)

En esta sección de la guía se recorre la creación de paquetes de extensión manual una vez [que haya configurado su cuenta de desarrollador de Windows y reservado los nombres de extensión](./packaging/extensions-in-the-windows-Dev-Center.md). Si tienes curiosidad sobre los detalles más precisos de empaquetar una extensión, dales una lectura.

También se incluye información sobre cómo [probar y desempaquetar una extensión empaquetada](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package). Esta información es relevante incluso si has salido de la ruta de empaquetado de ManifoldJS.

## [Localizar paquetes de extensión](./packaging/localizing-extension-packages.md)
El paso de localización del paquete se encuentra entre la creación de tu appxmanifest.xml archivo y el comando final para empaquetar tu extensión.
Esto le permite indicar qué idiomas son compatibles con las extensiones en la descripción de Microsoft Store y en qué idioma aparece el nombre de la extensión en Windows.

Puede saltar a [localizar el nombre y la descripción de Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) en esta sección de la guía si la extensión no es compatible con varios idiomas.

## [Usar ManifoldJS para empaquetar extensiones](./packaging/using-ManifoldJS-to-package-extensions.md)

La ruta de la herramienta para embalar tu extensión, ManifoldJS empaquetará tu extensión en un instante con un esfuerzo mínimo para tu fin. Proporciona algunos activos de Windows/Microsoft Store después de rellenar algunas propiedades de AppXManifest y tu extensión se empaquetará en un momento.

Una vez empaquetada la extensión, consulte la sección de [pruebas](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) de creación y prueba de la extensión de Microsoft Edge para obtener información sobre cómo realizar la transferencia o desempaquetar.


## [Ejecutar el kit para la certificación de aplicaciones en Windows](./packaging/running-the-windows-app-certification-kit.md)

Una vez que tenga una extensión empaquetada, puede ejecutarla a través del kit para la certificación de aplicaciones en Windows. Al hacerlo, se ejecutará una serie de pruebas en el paquete de extensión para asegurarse de que esté listo para Microsoft Store.
