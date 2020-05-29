---
description: El protocolo Microsoft Edge DevTools versión 0,1 admite los siguientes clientes de herramientas.
title: DevTools de la versión 0,1 de los protocolos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a537102bab7b5d914fd721aeca8bed57817e9216
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573772"
---
# Clientes del protocolo DevTools

> [!NOTE]
> El protocolo Microsoft Edge DevTools solo funciona en la [actualización de Windows 10 de abril de 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) y versiones posteriores de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

El **Protocolo DevTools 0,1** admite los siguientes clientes de herramientas.

[ ![ Microsoft Edge DevTools](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) Preview [ ![ Microsoft Visual Studio 15,7 Preview 2](../media/visual-studio-2017.png)](#microsoft-visual-studio-preview)

## Vista previa de Microsoft Edge DevTools

Puede usar la aplicación independiente [**Microsoft Edge DevTools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) Windows 10 de Microsoft Store para depurar de forma remota un dispositivo host que ejecute Microsoft Edge ([EdgeHTML 17](../../dev-guide.md) o posterior).

Esta versión preliminar 0,1 del protocolo DevTools proporciona la funcionalidad de depuración básica, como la definición de puntos de interrupción, el recorrido paso a paso por el código y la exploración de las pilas. En la interfaz de usuario de Edge DevTools, se traduce a la funcionalidad disponible en el panel de [**depuración**](../../devtools-guide/debugger.md) , menos inspección de caché (para almacenamiento Web, trabajo de servicio, API de caché y IndexedDB). Por el momento, la depuración remota de Microsoft Edge está limitada a los hosts de escritorio y es compatible con otros dispositivos Windows 10 que se publiquen en versiones futuras.

A continuación se explica cómo configurar la depuración remota con la aplicación Microsoft Edge DevTools Preview. El protocolo DevTools está en versión preliminar y requiere la [actualización de Windows 10 de abril de 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) o una compilación posterior de Windows Insider Preview en el equipo de host (de depuración). La aplicación Edge DevTools Preview (usada en el equipo de depuración) se ejecutará en las compilaciones de otoño Creators (versión 1709) y Windows Insider Preview.

**En el equipo host (depurado)...**

1. Si estás en una red WiFi, asegúrate de que la red esté marcada como **dominio** o **privada**. Para comprobarlo, abra la aplicación del [**centro de seguridad de Windows Defender**](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) , haga clic en **firewall & protección de red** y compruebe si su red aparece como red de *dominio* o como *red privada*. 

    Si se muestra como *público*, vaya a **configuración**  >  **red & Internet**  >  **Wi-Fi**, haga clic en su red y cambie el botón *Perfil de red* a **privado**.

2. Abra el panel **de control para desarrolladores** en *configuración* de Windows (busque *desarrollador* y haga clic en *usar características de desarrollador*) y: 

    a. Activar o desactivar el **modo para programadores**. Esto instalará el paquete de *modo de desarrollador* , habilitando herramientas remotas para el escritorio.

    b. Habilite el [**portal de dispositivos**](/windows/uwp/debug-test-perf/device-portal) (Active los*diagnósticos remotos en conexiones de red de área local*) y la **detección de dispositivos** (*haga que su dispositivo sea visible para las conexiones USB y su red local*).

    c. Active la **autenticación** y proporcione un nombre de usuario y contraseña.

    d. Observe que aparece la dirección IP de la máquina y el puerto de conexión (50443).

3. Abra las pestañas de Microsoft Edge que desea depurar desde el equipo cliente.

**En el equipo del cliente (depurador)...**

1.  Instale e inicie la aplicación independiente [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) desde Microsoft Store.

2. Abra el panel **remoto** y escriba la ubicación de red (URL y puerto) del equipo host y haga clic en **conectar**.

3. **Instale** el certificado del equipo host desde el cuadro de diálogo certificado que no es de *confianza* que aparece.

4. Proporciona el nombre de usuario y la contraseña que designaste para la autenticación de Device portal.

5. El panel *remoto* cargará una lista de destinos de página depurables en el equipo host. Seleccione una para iniciar la depuración.

6. Use el botón **Actualizar** para actualizar y volver a cargar la lista de destinos de páginas remotas en el equipo host. Haga clic en el botón **desconectar** para volver a la pantalla *conectarse a un dispositivo remoto* y adjuntar a otro host.

## Microsoft Visual Studio Preview

Con la última versión de [**Visual Studio Preview**](https://www.visualstudio.com/vs/preview/) (visual Studio 15,7 Preview 1 o posterior), puede iniciar y depurar Microsoft Edge desde el IDE en cualquier proyecto de ASP.net o .net Core. El protocolo DevTools está actualmente en versión preliminar y requiere que estés ejecutando una compilación de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

A continuación se explica cómo configurar la depuración de Microsoft Edge con Visual Studio:

1.  Instale e inicie la compilación más reciente de [**Visual Studio Preview**](https://www.visualstudio.com/vs/preview/) (visual Studio 15,7 Preview 1 o posterior).

2. Abra un proyecto existente de ASP.NET o .NET Core o **cree un nuevo proyecto...** usando una de las plantillas de **Visual C#** .net.

3. En el **Explorador de soluciones**de proyecto, abra los archivos de JavaScript que desea depurar y establezca puntos de interrupción dentro del IDE como lo haría con el código del lado del servidor.

4. Pulse `F5` para iniciar Microsoft Edge con el servidor DevTools. Cuando se alcanza un punto de interrupción, se romperá en Visual Studio y podrás inspeccionar y recorrer el código desde allí.
