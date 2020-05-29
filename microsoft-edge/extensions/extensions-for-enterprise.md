---
ms.assetid: 8e2f75c4-fb7f-4892-a6c2-23bac081581a
description: Descubra los aspectos específicos de la empresa de las extensiones de Microsoft Edge y vea cómo son similares a las aplicaciones para UWP.
title: Extensiones para Enterprise
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.custom: seodec18
ms.openlocfilehash: 8f50c282fce11d2654f990bf135941e0616af3f3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573655"
---
# Extensiones para Enterprise  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Las extensiones de Microsoft Edge tienen un flujo de trabajo similar cuando se comparan con otras aplicaciones de la empresa para UWP. La información siguiente detalla los aspectos específicos de la empresa de las extensiones de Microsoft Edge.

## Requisitos previos
Se recomiendan los siguientes elementos para desarrollar, empaquetar e implementar una extensión de Microsoft Edge para empresas:

+ Cuenta del portal para desarrolladores de Windows, para firmar y liberar la extensión del almacén privado de la empresa. Para obtener más información, consulta [abrir una cuenta de desarrollador](/windows/uwp/publish/opening-a-developer-account) .
+ Microsoft Store para empresas o para el ámbito educativo, para distribuir la aplicación a la empresa. Para obtener más información, consulte la [documentación de Microsoft Store para empresas y educación](/microsoft-store/) .
+ Identifique las versiones de Windows 10 que ejecutarán la extensión de Microsoft Edge. Consulte la [información de lanzamiento de Windows 10](https://www.microsoft.com/itpro/windows-10/release-information) para obtener una lista de las versiones de Windows 10 existentes.

> [!NOTE]
> La transferencia local puede considerarse como una alternativa al uso del portal para desarrolladores de Windows para firmar la versión. Para obtener más información, consulta el comportamiento de las extensiones de transferencia local a continuación.

## Windows Information Protection
Las extensiones de Microsoft Edge actualmente no respetan la configuración de Windows Information Protection (WIP). Si a una empresa le preocupa la protección de datos, la compatibilidad con las extensiones no debe habilitarse para Microsoft Edge.

Para deshabilitar las extensiones para empleados, configure la Directiva de grupo y la configuración de Microsoft Intune. Para obtener más información sobre las directivas que se deben configurar, consulte [directivas disponibles para Microsoft Edge](https://technet.microsoft.com/itpro/microsoft-edge/available-policies).

## Extensiones de empaquetado
Antes de que una empresa pueda distribuir una extensión a sus empleados, primero debe estar empaquetada. Encontrará instrucciones sobre las extensiones de empaquetado en la guía de [empaquetado](./guides/packaging.md) .

> [!TIP]
> Asegúrese de probar y ejecutar la extensión en todas las versiones de Windows 10 para asegurarse de que funcionará de la forma esperada antes de la distribución.

## Distribuir extensiones
Una vez que se ha empaquetado una extensión, se puede distribuir a los empleados a través de Microsoft Store, Microsoft Store para empresas o mediante la transferencia local.

Las extensiones distribuidas a través de Microsoft Store para empresas se pueden asignar a los empleados o se pueden agregar a una tienda privada en la que todos los empleados puedan tener acceso a ellas. Esto puede hacerse siguiendo la guía [distribuir aplicaciones de línea de negocio (LOB) a la guía de empresas](https://msdn.microsoft.com/windows/uwp/publish/distribute-lob-apps-to-enterprises) .

Para transferir las extensiones, los dispositivos (no administrados o administrados) deben estar desbloqueados para la transferencia local. Consulte [transferir localmente aplicaciones LOB en Windows 10](https://technet.microsoft.com/itpro/windows/deploy/sideload-apps-in-windows-10) para obtener más información sobre cómo transferir las extensiones empaquetadas.

> [!IMPORTANT]
> Si la empresa está desarrollando y distribuyendo la extensión de forma interna, la empresa requerirá la cuenta de Microsoft Store para empresas (o educación) y el portal para desarrolladores de Windows.

### Comportamiento de las extensiones de la transferida localmente
A diferencia de las extensiones distribuidas a través de Microsoft Store (o de Microsoft Store para empresas), las extensiones de la transferida localmente se tratan de forma diferente en Microsoft Edge.

La primera diferencia afecta a cómo se comportan las extensiones de la misma después de la instalación. A diferencia de las extensiones de Microsoft Store, las extensiones de transferidas no muestran inmediatamente la notificación "tiene una nueva extensión" y deben activarse de forma manual por el usuario.

Para activar la extensión, abra el menú **más (...)** , seleccione **"extensiones"** y verá la extensión de transferida localmente en la lista de extensiones instaladas. Haga clic en la extensión y enciéndala.

La segunda diferencia afecta a la forma en que las extensiones de transferidas se muestran en el explorador. Por ejemplo, la notificación "usted tiene una nueva extensión" y la lista de extensiones instaladas incluyen una advertencia adicional que indica que la extensión es de un origen desconocido.

![ADVERTENCIA de transferencia de prueba 1](./media/sideload-permissionflyout.PNG)

![ADVERTENCIA de transferencia de prueba 2](./media/sideload-l1warning.PNG)

La tercera y última diferencia afectan a cómo se comportan las extensiones de desinstalación en el explorador. Las extensiones de transferidas localmente en dispositivos que están habilitados para el dominio o MDM se comportan como extensiones de Microsoft Store. Sin embargo, las extensiones transferidas localmente en dispositivos que no se han unido a un dominio o MDM se desactivan durante el inicio del explorador y requieren que el usuario realice una acción explícita.

Poco después del inicio del explorador (después de ~ 10 segundos de inactividad), aparecerá la siguiente notificación cerca de la parte inferior de la ventana.

![notificación de transferencia de prueba](./media/sideload-scareUI.PNG)

Cada vez que se inicie Microsoft Edge, los usuarios deberán seleccionar "activar de todos modos" para poder usar la extensión.
