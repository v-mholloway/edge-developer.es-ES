---
description: El protocolo Microsoft Edge DevTools versión 0,2 admite los siguientes clientes de herramientas.
title: Clientes de la versión 0,2 del protocolo Microsoft Edge DevTools (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 92976de257a73fd7206205622a4c79d1277b3950
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882894"
---
# Clientes de la versión 0,2 del protocolo Microsoft Edge DevTools (EdgeHTML)  

> [!NOTE]
> La versión 0,2 del protocolo Microsoft Edge DevTools solo funciona en la [actualización de Windows 10 de octubre de 2018](/windows/uwp/whats-new/windows-10-build-17763) y versiones posteriores de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .  

El **Protocolo DevTools 0,2** admite los siguientes clientes de herramientas.

[ ![ Microsoft Edge DevTools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [ ![ Visual Studio Code](../media/visual-studio-code.png)](#visual-studio-code) [ ![ Microsoft Visual Studio 15,8](../media/visual-studio-2017.png)](#microsoft-visual-studio)

## Vista previa de Microsoft Edge DevTools

Puede usar la aplicación independiente [**Microsoft Edge DevTools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) Windows 10 de Microsoft Store para depurar de forma remota un dispositivo host que ejecute Microsoft Edge ([EdgeHTML 17](../../dev-guide.md) o posterior).

La versión 0,2 del protocolo DevTools proporciona nuevos dominios para la depuración y las API de consola de diseño y estilo, además de la funcionalidad de depuración básica de scripts introducida en la versión 0,1. En la interfaz de usuario de Edge DevTools, esto se traduce en la funcionalidad disponible en los paneles [**elementos**](../../devtools-guide/elements.md), [**consola**](../../devtools-guide/console.md) y [**depuración**](../../devtools-guide/debugger.md) . Por el momento, la depuración remota de Microsoft Edge está limitada a los hosts de escritorio y es compatible con otros dispositivos Windows 10 que se publiquen en versiones futuras.

A continuación se explica cómo configurar la depuración remota con la aplicación Microsoft Edge DevTools Preview. La versión 0,2 del protocolo DevTools requiere la [actualización de Windows 10 de octubre de 2018](/windows/uwp/whats-new/windows-10-build-17763) o una compilación posterior de Windows Insider Preview en el equipo de host (de depuración). La aplicación Edge DevTools Preview (usada en el equipo de depuración) se ejecutará en Windows 10 versión 16299 (Windows 10 Fall Creators Update, 10/2017) o versiones posteriores.

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

## Visual Studio Code

Con el [depurador de la extensión de código Edge para Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) , puedes depurar la secuencia de comandos que se ejecuta en Microsoft Edge directamente en Visual Studio Code. La extensión requiere que se preste servicio a la aplicación web desde localhost, que se puede iniciar desde cualquier línea de comandos o desde una [tarea](https://code.visualstudio.com/docs/editor/tasks).

Para empezar:

1. Instale el [depurador para la extensión de código perimetral de](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs.

2. Reinicie VS Code, abra la carpeta que contiene el proyecto que desea depurar y establezca puntos de interrupción en el código.

3. Configure una [tarea de inicio](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) localhost para abrir la página deseada del proyecto: **depurar**  >  **Agregar configuración...**. Por ejemplo:

    ```json
    {
        "version": "0.2.0",
        "configurations": [

            {
                "name": "Launch localhost",
                "type": "edge",
                "request": "launch",
                "url": "http://localhost/mypage.html",
                "webRoot": "${workspaceFolder}/wwwroot"
            }
        ]
    }
    ```

    [*El depurador*](https://github.com/Microsoft/vscode-edge-debug2#using-the-debugger) tiene más información sobre las opciones de configuración de inicio. 

4. Inicia el servidor en localhost y pulsa el botón **iniciar depuración** (reproducir) o `F5` para iniciar Microsoft Edge. Cuando se alcanza un punto de interrupción, se romperá en VS Code y podrá inspeccionar y recorrer el código desde allí.

Para obtener más información, consulta el [depurador de código vs para la documentación de Microsoft Edge](https://github.com/Microsoft/vscode-edge-debug2#----vs-code---debugger-for-microsoft-edge--) .

## Microsoft Visual Studio

Si usas la última versión de [**Visual Studio**](https://www.visualstudio.com) (visual Studio 15,8 o posterior) que se ejecuta en la [actualización de Windows 10 de octubre de 2018](/windows/uwp/whats-new/windows-10-build-17763), puedes iniciar y depurar Microsoft Edge desde el IDE en cualquier proyecto de ASP.net o .net Core.

A continuación se explica cómo configurar la depuración de Microsoft Edge con Visual Studio:

1.  Instale e inicie la última versión de [**Visual Studio**](https://www.visualstudio.com/) (visual Studio 15,8 o posterior).

2. Abra un proyecto existente de ASP.NET o .NET Core o **cree un nuevo proyecto...** usando una de las plantillas de **Visual C#** .net.

3. En el **Explorador de soluciones**de proyecto, abra los archivos de JavaScript que desea depurar y establezca puntos de interrupción dentro del IDE como lo haría con el código del lado del servidor.

4. Pulse `F5` para iniciar Microsoft Edge con el servidor DevTools. Cuando se alcanza un punto de interrupción, se romperá en Visual Studio y podrás inspeccionar y recorrer el código desde allí.
