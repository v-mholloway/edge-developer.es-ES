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
# <span data-ttu-id="73c28-103">Clientes de la versión 0,2 del protocolo Microsoft Edge DevTools (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="73c28-103">Microsoft Edge DevTools Protocol Version 0.2 Clients (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="73c28-104">La versión 0,2 del protocolo Microsoft Edge DevTools solo funciona en la [actualización de Windows 10 de octubre de 2018](/windows/uwp/whats-new/windows-10-build-17763) y versiones posteriores de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="73c28-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>  

<span data-ttu-id="73c28-105">El **Protocolo DevTools 0,2** admite los siguientes clientes de herramientas.</span><span class="sxs-lookup"><span data-stu-id="73c28-105">**DevTools Protocol 0.2** supports the following tooling clients.</span></span>

<span data-ttu-id="73c28-106">[ ![ Microsoft Edge DevTools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [ ![ Visual Studio Code](../media/visual-studio-code.png)](#visual-studio-code) [ ![ Microsoft Visual Studio 15,8](../media/visual-studio-2017.png)](#microsoft-visual-studio)</span><span class="sxs-lookup"><span data-stu-id="73c28-106">[![Microsoft Edge DevTools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [![Visual Studio Code](../media/visual-studio-code.png)](#visual-studio-code) [![Microsoft Visual Studio 15.8](../media/visual-studio-2017.png)](#microsoft-visual-studio)</span></span>

## <span data-ttu-id="73c28-107">Vista previa de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="73c28-107">Microsoft Edge DevTools Preview</span></span>

<span data-ttu-id="73c28-108">Puede usar la aplicación independiente [**Microsoft Edge DevTools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) Windows 10 de Microsoft Store para depurar de forma remota un dispositivo host que ejecute Microsoft Edge ([EdgeHTML 17](../../dev-guide.md) o posterior).</span><span class="sxs-lookup"><span data-stu-id="73c28-108">You can use the standalone [**Microsoft Edge DevTools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) Windows 10 app from the Microsoft Store to remotely debug a host device running Microsoft Edge ([EdgeHTML 17](../../dev-guide.md) or later).</span></span>

<span data-ttu-id="73c28-109">La versión 0,2 del protocolo DevTools proporciona nuevos dominios para la depuración y las API de consola de diseño y estilo, además de la funcionalidad de depuración básica de scripts introducida en la versión 0,1.</span><span class="sxs-lookup"><span data-stu-id="73c28-109">Version 0.2 of the DevTools Protocol provides new domains for style and layout debugging and console APIs, in addition to the core script debugging functionality introduced in Version 0.1.</span></span> <span data-ttu-id="73c28-110">En la interfaz de usuario de Edge DevTools, esto se traduce en la funcionalidad disponible en los paneles [**elementos**](../../devtools-guide/elements.md), [**consola**](../../devtools-guide/console.md) y [**depuración**](../../devtools-guide/debugger.md) .</span><span class="sxs-lookup"><span data-stu-id="73c28-110">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../../devtools-guide/elements.md), [**Console**](../../devtools-guide/console.md) and [**Debugger**](../../devtools-guide/debugger.md) panels.</span></span> <span data-ttu-id="73c28-111">Por el momento, la depuración remota de Microsoft Edge está limitada a los hosts de escritorio y es compatible con otros dispositivos Windows 10 que se publiquen en versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="73c28-111">Currently Microsoft Edge remote debugging is limited to desktop hosts, with support for other Windows 10 devices coming in future releases.</span></span>

<span data-ttu-id="73c28-112">A continuación se explica cómo configurar la depuración remota con la aplicación Microsoft Edge DevTools Preview.</span><span class="sxs-lookup"><span data-stu-id="73c28-112">Here's how to set up remote debugging with the Microsoft Edge DevTools Preview app.</span></span> <span data-ttu-id="73c28-113">La versión 0,2 del protocolo DevTools requiere la [actualización de Windows 10 de octubre de 2018](/windows/uwp/whats-new/windows-10-build-17763) o una compilación posterior de Windows Insider Preview en el equipo de host (de depuración).</span><span class="sxs-lookup"><span data-stu-id="73c28-113">The DevTools Protocol version 0.2 requires [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) or a later Windows Insider Preview build on the host (debugee) machine.</span></span> <span data-ttu-id="73c28-114">La aplicación Edge DevTools Preview (usada en el equipo de depuración) se ejecutará en Windows 10 versión 16299 (Windows 10 Fall Creators Update, 10/2017) o versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="73c28-114">The Edge DevTools Preview app (used on the debugger machine) will run on Windows 10 version 16299 (Windows 10 Fall Creators Update, 10/2017) or higher.</span></span>

**<span data-ttu-id="73c28-115">En el equipo host (depurado)...</span><span class="sxs-lookup"><span data-stu-id="73c28-115">On the host (debugee) machine...</span></span>**

1. <span data-ttu-id="73c28-116">Si estás en una red WiFi, asegúrate de que la red esté marcada como **dominio** o **privada**.</span><span class="sxs-lookup"><span data-stu-id="73c28-116">If you're on a WiFi network, ensure the network is marked as either **Domain** or **Private**.</span></span> <span data-ttu-id="73c28-117">Para comprobarlo, abra la aplicación del [**centro de seguridad de Windows Defender**](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) , haga clic en **firewall & protección de red** y compruebe si su red aparece como red de *dominio* o como *red privada*.</span><span class="sxs-lookup"><span data-stu-id="73c28-117">You can verify this by opening the [**Windows Defender Security Center**](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) app, clicking on **Firewall & network protection** and checking if your network is listed as a *Domain network* or *Private network*.</span></span> 

    <span data-ttu-id="73c28-118">Si se muestra como *público*, vaya a **configuración**  >  **red & Internet**  >  **Wi-Fi**, haga clic en su red y cambie el botón *Perfil de red* a **privado**.</span><span class="sxs-lookup"><span data-stu-id="73c28-118">If its listed as *Public*, go to **Settings** > **Network & Internet** > **Wi-Fi**, click on your network and toggle the *Network profile* button to **Private**.</span></span>

2. <span data-ttu-id="73c28-119">Abra el panel **de control para desarrolladores** en *configuración* de Windows (busque *desarrollador* y haga clic en *usar características de desarrollador*) y:</span><span class="sxs-lookup"><span data-stu-id="73c28-119">Open the **For developers** control panel in Windows *Settings* (search for *developer* and click on *Use developer features*), and:</span></span> 

    <span data-ttu-id="73c28-120">a.</span><span class="sxs-lookup"><span data-stu-id="73c28-120">a.</span></span> <span data-ttu-id="73c28-121">Activar o desactivar el **modo para programadores**.</span><span class="sxs-lookup"><span data-stu-id="73c28-121">Toggle on **Developer Mode**.</span></span> <span data-ttu-id="73c28-122">Esto instalará el paquete de *modo de desarrollador* , habilitando herramientas remotas para el escritorio.</span><span class="sxs-lookup"><span data-stu-id="73c28-122">This will install the *Developer Mode* package, enabling remote tooling for desktop.</span></span>

    <span data-ttu-id="73c28-123">b.</span><span class="sxs-lookup"><span data-stu-id="73c28-123">b.</span></span> <span data-ttu-id="73c28-124">Habilite el [**portal de dispositivos**](/windows/uwp/debug-test-perf/device-portal) (Active los*diagnósticos remotos en conexiones de red de área local*) y la **detección de dispositivos** (*haga que su dispositivo sea visible para las conexiones USB y su red local*).</span><span class="sxs-lookup"><span data-stu-id="73c28-124">Enable [**Device Portal**](/windows/uwp/debug-test-perf/device-portal) (*Turn on remote diagnostics over local area network connections*) and **Device discovery** (*Make your device visible to USB connections and your local network*).</span></span>

    <span data-ttu-id="73c28-125">c.</span><span class="sxs-lookup"><span data-stu-id="73c28-125">c.</span></span> <span data-ttu-id="73c28-126">Active la **autenticación** y proporcione un nombre de usuario y contraseña.</span><span class="sxs-lookup"><span data-stu-id="73c28-126">Turn on **Authentication** and supply a username / password.</span></span>

    <span data-ttu-id="73c28-127">d.</span><span class="sxs-lookup"><span data-stu-id="73c28-127">d.</span></span> <span data-ttu-id="73c28-128">Observe que aparece la dirección IP de la máquina y el puerto de conexión (50443).</span><span class="sxs-lookup"><span data-stu-id="73c28-128">Note the machine IP address and connection port (50443) displayed.</span></span>

3. <span data-ttu-id="73c28-129">Abra las pestañas de Microsoft Edge que desea depurar desde el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="73c28-129">Open tabs in Microsoft Edge that you wish to debug from the client machine.</span></span>

**<span data-ttu-id="73c28-130">En el equipo del cliente (depurador)...</span><span class="sxs-lookup"><span data-stu-id="73c28-130">On the client (debugger) machine...</span></span>**

1.  <span data-ttu-id="73c28-131">Instale e inicie la aplicación independiente [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) desde Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="73c28-131">Install and launch the standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app from the Microsoft Store.</span></span>

2. <span data-ttu-id="73c28-132">Abra el panel **remoto** y escriba la ubicación de red (URL y puerto) del equipo host y haga clic en **conectar**.</span><span class="sxs-lookup"><span data-stu-id="73c28-132">Open the **Remote** panel and enter the network location (URL and port) of the host machine and click **Connect**.</span></span>

3. <span data-ttu-id="73c28-133">**Instale** el certificado del equipo host desde el cuadro de diálogo certificado que no es de *confianza* que aparece.</span><span class="sxs-lookup"><span data-stu-id="73c28-133">**Install** the host machine's certificate from the *Untrusted Certificate* dialog that appears.</span></span>

4. <span data-ttu-id="73c28-134">Proporciona el nombre de usuario y la contraseña que designaste para la autenticación de Device portal.</span><span class="sxs-lookup"><span data-stu-id="73c28-134">Supply the username/password you designated for Device Portal authentication.</span></span>

5. <span data-ttu-id="73c28-135">El panel *remoto* cargará una lista de destinos de página depurables en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="73c28-135">The *Remote* panel will load a list of debuggable page targets on the host machine.</span></span> <span data-ttu-id="73c28-136">Seleccione una para iniciar la depuración.</span><span class="sxs-lookup"><span data-stu-id="73c28-136">Select one to start debugging.</span></span>

6. <span data-ttu-id="73c28-137">Use el botón **Actualizar** para actualizar y volver a cargar la lista de destinos de páginas remotas en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="73c28-137">Use the **Refresh** button to update and reload the list of remote page targets on the host machine.</span></span> <span data-ttu-id="73c28-138">Haga clic en el botón **desconectar** para volver a la pantalla *conectarse a un dispositivo remoto* y adjuntar a otro host.</span><span class="sxs-lookup"><span data-stu-id="73c28-138">Click the **Disconnect** button to return to the *Connect to a remote device* screen and attach to a different host.</span></span>

## <span data-ttu-id="73c28-139">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="73c28-139">Visual Studio Code</span></span>

<span data-ttu-id="73c28-140">Con el [depurador de la extensión de código Edge para Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) , puedes depurar la secuencia de comandos que se ejecuta en Microsoft Edge directamente en Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="73c28-140">With the [Debugger for Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension, you can debug script running in Microsoft Edge directly in Visual Studio Code.</span></span> <span data-ttu-id="73c28-141">La extensión requiere que se preste servicio a la aplicación web desde localhost, que se puede iniciar desde cualquier línea de comandos o desde una [tarea](https://code.visualstudio.com/docs/editor/tasks).</span><span class="sxs-lookup"><span data-stu-id="73c28-141">The extension requires you to be serving your web application from localhost, which you can start from either command-line or a [Task](https://code.visualstudio.com/docs/editor/tasks).</span></span>

<span data-ttu-id="73c28-142">Para empezar:</span><span class="sxs-lookup"><span data-stu-id="73c28-142">To get started:</span></span>

1. <span data-ttu-id="73c28-143">Instale el [depurador para la extensión de código perimetral de](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs.</span><span class="sxs-lookup"><span data-stu-id="73c28-143">Install the [Debugger for Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension.</span></span>

2. <span data-ttu-id="73c28-144">Reinicie VS Code, abra la carpeta que contiene el proyecto que desea depurar y establezca puntos de interrupción en el código.</span><span class="sxs-lookup"><span data-stu-id="73c28-144">Restart VS Code, open the folder containing the project you wish to debug and set breakpoints in your code.</span></span>

3. <span data-ttu-id="73c28-145">Configure una [tarea de inicio](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) localhost para abrir la página deseada del proyecto: **depurar**  >  **Agregar configuración...**. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="73c28-145">Configure a localhost [launch task](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) to open the desired page of your project: **Debug** > **Add Configuration...**. For example:</span></span>

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

    <span data-ttu-id="73c28-146">[*El depurador*](https://github.com/Microsoft/vscode-edge-debug2#using-the-debugger) tiene más información sobre las opciones de configuración de inicio.</span><span class="sxs-lookup"><span data-stu-id="73c28-146">[*Using the debugger*](https://github.com/Microsoft/vscode-edge-debug2#using-the-debugger) has more on launch configuration settings.</span></span> 

4. <span data-ttu-id="73c28-147">Inicia el servidor en localhost y pulsa el botón **iniciar depuración** (reproducir) o `F5` para iniciar Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="73c28-147">Start your server on localhost and press the **Start Debugging** (play) button or `F5` to launch Microsoft Edge.</span></span> <span data-ttu-id="73c28-148">Cuando se alcanza un punto de interrupción, se romperá en VS Code y podrá inspeccionar y recorrer el código desde allí.</span><span class="sxs-lookup"><span data-stu-id="73c28-148">When a breakpoint is hit, you'll break into VS Code and can further inspect and step through code from there.</span></span>

<span data-ttu-id="73c28-149">Para obtener más información, consulta el [depurador de código vs para la documentación de Microsoft Edge](https://github.com/Microsoft/vscode-edge-debug2#----vs-code---debugger-for-microsoft-edge--) .</span><span class="sxs-lookup"><span data-stu-id="73c28-149">For more, check out the [VS Code - Debugger for Microsoft Edge](https://github.com/Microsoft/vscode-edge-debug2#----vs-code---debugger-for-microsoft-edge--) documentation.</span></span>

## <span data-ttu-id="73c28-150">Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="73c28-150">Microsoft Visual Studio</span></span>

<span data-ttu-id="73c28-151">Si usas la última versión de [**Visual Studio**](https://www.visualstudio.com) (visual Studio 15,8 o posterior) que se ejecuta en la [actualización de Windows 10 de octubre de 2018](/windows/uwp/whats-new/windows-10-build-17763), puedes iniciar y depurar Microsoft Edge desde el IDE en cualquier proyecto de ASP.net o .net Core.</span><span class="sxs-lookup"><span data-stu-id="73c28-151">Using the latest [**Visual Studio**](https://www.visualstudio.com) version (Visual Studio 15.8 or later) running on [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763), you can launch and debug Microsoft Edge from the IDE on any ASP.NET or .NET Core project.</span></span>

<span data-ttu-id="73c28-152">A continuación se explica cómo configurar la depuración de Microsoft Edge con Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="73c28-152">Here's how to set up Microsoft Edge debugging with Visual Studio:</span></span>

1.  <span data-ttu-id="73c28-153">Instale e inicie la última versión de [**Visual Studio**](https://www.visualstudio.com/) (visual Studio 15,8 o posterior).</span><span class="sxs-lookup"><span data-stu-id="73c28-153">Install and launch the latest [**Visual Studio**](https://www.visualstudio.com/) (Visual Studio 15.8 or later).</span></span>

2. <span data-ttu-id="73c28-154">Abra un proyecto existente de ASP.NET o .NET Core o **cree un nuevo proyecto...** usando una de las plantillas de **Visual C#** .net.</span><span class="sxs-lookup"><span data-stu-id="73c28-154">Open an existing ASP.NET or .NET Core project or **Create new project...** using one of the **Visual C#** .NET templates.</span></span>

3. <span data-ttu-id="73c28-155">En el **Explorador de soluciones**de proyecto, abra los archivos de JavaScript que desea depurar y establezca puntos de interrupción dentro del IDE como lo haría con el código del lado del servidor.</span><span class="sxs-lookup"><span data-stu-id="73c28-155">In the project **Solution Explorer**, open the JavaScript files you wish to debug and set breakpoints within the IDE just as you would with server-side code.</span></span>

4. <span data-ttu-id="73c28-156">Pulse `F5` para iniciar Microsoft Edge con el servidor DevTools.</span><span class="sxs-lookup"><span data-stu-id="73c28-156">Press `F5` to launch Microsoft Edge running the DevTools Server.</span></span> <span data-ttu-id="73c28-157">Cuando se alcanza un punto de interrupción, se romperá en Visual Studio y podrás inspeccionar y recorrer el código desde allí.</span><span class="sxs-lookup"><span data-stu-id="73c28-157">When a breakpoint is hit, you'll break into Visual Studio and can further inspect and step through the code from there.</span></span>
