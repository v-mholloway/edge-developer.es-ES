---
description: Modo IE y el Microsoft Edge (Chromium) DevTools
title: Modo internet Explorer y DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, ie11, internet explorer 11, es el modo ie
ms.openlocfilehash: 070bf970c784b4f2173ebc52e4494fc6807b4a8e
ms.sourcegitcommit: 7cba715ef71cbac4ee0ebe8f07c0c0e4a2c64221
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643238"
---
# <a name="internet-explorer-mode-and-the-devtools"></a><span data-ttu-id="09d7a-104">Modo internet Explorer y DevTools</span><span class="sxs-lookup"><span data-stu-id="09d7a-104">Internet Explorer mode and the DevTools</span></span>  

<span data-ttu-id="09d7a-105">En este artículo se describe cómo se integra el modo de Internet Explorer \(modo IE\) con el Microsoft Edge \(Chromium\) DevTools.</span><span class="sxs-lookup"><span data-stu-id="09d7a-105">This article describes how Internet Explorer mode \(IE mode\) integrates with the Microsoft Edge \(Chromium\) DevTools.</span></span>  

## <a name="understanding-ie-mode"></a><span data-ttu-id="09d7a-106">Descripción del modo IE</span><span class="sxs-lookup"><span data-stu-id="09d7a-106">Understanding IE mode</span></span>  

<span data-ttu-id="09d7a-107">El modo IE permite a las empresas especificar una lista de sitios web que solo funcionan en Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="09d7a-107">IE mode allows enterprises to specify a list of web sites that only work in Internet Explorer 11.</span></span>  <span data-ttu-id="09d7a-108">Al navegar a estos sitios web en Microsoft Edge \(Chromium\), una instancia de Internet Explorer 11 se ejecuta y representa el sitio en una pestaña.  La funcionalidad permite a las empresas administrar la compatibilidad con tecnologías que actualmente no son compatibles con ningún explorador web moderno.</span><span class="sxs-lookup"><span data-stu-id="09d7a-108">When you navigate to these web sites in Microsoft Edge \(Chromium\), an instance of Internet Explorer 11 runs and renders the site in a tab.  The functionality allows enterprises to manage compatibility with technologies that are currently not compatible with any modern web browsers.</span></span>  <span data-ttu-id="09d7a-109">La compatibilidad con las siguientes tecnologías se incluye en el modo IE.</span><span class="sxs-lookup"><span data-stu-id="09d7a-109">Support for the following technologies is included in IE mode.</span></span>  

*   <span data-ttu-id="09d7a-110">Modos de documento de IE</span><span class="sxs-lookup"><span data-stu-id="09d7a-110">IE document modes</span></span>  
*   <span data-ttu-id="09d7a-111">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="09d7a-111">ActiveX controls</span></span>  
*   <span data-ttu-id="09d7a-112">otros componentes heredados</span><span class="sxs-lookup"><span data-stu-id="09d7a-112">other legacy components</span></span>  

<span data-ttu-id="09d7a-113">En el modo IE, el proceso de representación se basa en Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="09d7a-113">In IE mode, the rendering process is based on Internet Explorer 11.</span></span>  <span data-ttu-id="09d7a-114">El Microsoft Edge de procesos \(Chromium\) controla la duración del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="09d7a-114">The Microsoft Edge \(Chromium\) process manager handles the lifetime of the rendering process.</span></span>  <span data-ttu-id="09d7a-115">Está restringido a la duración de la pestaña de un sitio específico \(o app\).</span><span class="sxs-lookup"><span data-stu-id="09d7a-115">It is constrained to the lifetime of the tab for a specific site \(or app\).</span></span>  <span data-ttu-id="09d7a-116">Cuando una pestaña se representa en modo IE, aparece un distintivo en la barra de direcciones de la pestaña específica.</span><span class="sxs-lookup"><span data-stu-id="09d7a-116">When a tab renders in IE mode, a badge appears in the address bar for the specific tab.</span></span>  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="Distintivo de modo IE en la barra de direcciones" lightbox="../media/ie-mode-badge.msft.png":::
   <span data-ttu-id="09d7a-118">Distintivo de modo IE en la barra de direcciones</span><span class="sxs-lookup"><span data-stu-id="09d7a-118">IE mode badge in the address bar</span></span>  
:::image-end:::  

<span data-ttu-id="09d7a-119">Actualmente, el modo IE está disponible en Windows 10 Versión 1903 \(Actualización de mayo de 2019\), pero pronto llegará a todas las plataformas Windows compatibles.</span><span class="sxs-lookup"><span data-stu-id="09d7a-119">IE mode is currently available on Windows 10 Version 1903 \(May 2019 Update\), but is coming soon to all supported Windows platforms.</span></span>  

## <a name="launching-the-devtools-on-a-tab-in-ie-mode"></a><span data-ttu-id="09d7a-120">Iniciar DevTools en una pestaña en modo IE</span><span class="sxs-lookup"><span data-stu-id="09d7a-120">Launching the DevTools on a tab in IE mode</span></span>  

<span data-ttu-id="09d7a-121">Si intenta ver el modo de documento de un sitio web en modo IE, elija el distintivo en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="09d7a-121">If you are trying to view the document mode of a web site in IE mode, choose the badge in the address bar.</span></span>  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Ver el modo de documento con el distintivo de modo IE" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   <span data-ttu-id="09d7a-123">Ver el modo de documento con el distintivo de modo IE</span><span class="sxs-lookup"><span data-stu-id="09d7a-123">View document mode using IE mode badge</span></span>  
:::image-end:::  

<span data-ttu-id="09d7a-124">Si una pestaña usa el modo IE, las DevTools no funcionan y se producen las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="09d7a-124">If a tab is using IE mode, the DevTools do not work and the following conditions occur.</span></span>

*   <span data-ttu-id="09d7a-125">Si selecciona o selecciona , se inicia una instancia en blanco de la Microsoft Edge `F12` `Ctrl` + `Shift` + `I` \(Chromium\) DevTools muestra el siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="09d7a-125">If you select `F12` or select `Ctrl`+`Shift`+`I`, a blank instance of the Microsoft Edge \(Chromium\) DevTools is launched displays the following message.</span></span>  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   <span data-ttu-id="09d7a-126">Si abre un menú contextual \(clic con el botón derecho\) y elige **Ver**origen , Bloc de notas se inicia.</span><span class="sxs-lookup"><span data-stu-id="09d7a-126">If you open a contextual menu \(right-click\) and choose **View Source**, Notepad is launched.</span></span>  
*   <span data-ttu-id="09d7a-127">Si abre un menú contextual \(clic con el botón secundario\), **el elemento Inspect** no está visible.</span><span class="sxs-lookup"><span data-stu-id="09d7a-127">If you open a contextual menu \(right-click\), the **Inspect Element** is not visible.</span></span>  

<span data-ttu-id="09d7a-128">El motivo por el que varias de las herramientas de DevTools \(like the **Network** and **Performance** tools\) no funcionan es que el motor de representación cambia de Chromium a Internet Explorer 11 en modo IE.</span><span class="sxs-lookup"><span data-stu-id="09d7a-128">The reason that a number of the tools within the DevTools \(like the **Network** and **Performance** tools\) do not work is the rendering engine switches from Chromium to Internet Explorer 11 in IE mode.</span></span>  <span data-ttu-id="09d7a-129">Para proporcionar comentarios, vaya a [Getting in touch with the Microsoft Edge DevTools team](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="09d7a-129">To provide feedback, navigate to [Getting in touch with the Microsoft Edge DevTools team](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools se inicia en modo IE" lightbox="../media/ie-mode-devtools.msft.png":::
   <span data-ttu-id="09d7a-131">DevTools se inicia en modo IE</span><span class="sxs-lookup"><span data-stu-id="09d7a-131">DevTools launched in IE mode</span></span>  
:::image-end:::  

<span data-ttu-id="09d7a-132">Para probar el sitio web basado en Internet Explorer 11 \(o app\) en modo Internet Explorer 11 e IE, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="09d7a-132">To test your Internet Explorer 11-based website \(or app\) in Internet Explorer 11 and IE mode, perform the following steps.</span></span>  

1.  <span data-ttu-id="09d7a-133">Abra Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="09d7a-133">Open Internet Explorer 11.</span></span>  
    *   <span data-ttu-id="09d7a-134">En Windows 10, busque el acceso directo para Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="09d7a-134">On Windows 10, locate the shortcut for Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="09d7a-135">**Menú Inicio**  >  **Windows accesorios**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="09d7a-135">**Start Menu** > **Windows Accessories** > **Internet Explorer 11**.</span></span>  
    *   <span data-ttu-id="09d7a-136">En Windows 7, busque Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="09d7a-136">On Windows 7, locate Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="09d7a-137">**Menú Inicio**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="09d7a-137">**Start Menu** > **Internet Explorer 11**.</span></span>  
1.  <span data-ttu-id="09d7a-138">En Internet Explorer 11, abra la misma página web.</span><span class="sxs-lookup"><span data-stu-id="09d7a-138">In Internet Explorer 11, open the same webpage.</span></span>  
1.  <span data-ttu-id="09d7a-139">Inicie Internet Explorer DevTools.</span><span class="sxs-lookup"><span data-stu-id="09d7a-139">Launch the Internet Explorer DevTools.</span></span>  
    *   <span data-ttu-id="09d7a-140">Seleccione `F12` .</span><span class="sxs-lookup"><span data-stu-id="09d7a-140">Select `F12`.</span></span>  
    *   <span data-ttu-id="09d7a-141">Mantenga el mouse en cualquier lugar, abra un menú contextual \(clic con el botón derecho\) y elija **Inspeccionar elemento**.</span><span class="sxs-lookup"><span data-stu-id="09d7a-141">Hover anywhere, open a contextual menu \(right-click\), and choose **Inspect element**.</span></span>  <span data-ttu-id="09d7a-142">Para obtener más información acerca de cómo usar esas herramientas, vaya a Uso de las herramientas para [desarrolladores F12][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span><span class="sxs-lookup"><span data-stu-id="09d7a-142">For more information about how to use those tools, navigate to [Using the F12 developer tools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span></span>  

<span data-ttu-id="09d7a-143">Si Internet Explorer 11 no está disponible, como en Windows 11, puede usar IEChooser para iniciar las DevTools de Internet Explorer para depurar el contenido de las pestañas del modo IE.</span><span class="sxs-lookup"><span data-stu-id="09d7a-143">If Internet Explorer 11 is not available, such as on Windows 11, you can use IEChooser to launch the Internet Explorer DevTools to debug the content of your IE mode tabs.</span></span> <span data-ttu-id="09d7a-144">Para usar IEChooser, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="09d7a-144">To use IEChooser, perform the following steps.</span></span>

1.  <span data-ttu-id="09d7a-145">Abra IEChooser.</span><span class="sxs-lookup"><span data-stu-id="09d7a-145">Open IEChooser.</span></span>
    1. <span data-ttu-id="09d7a-146">Abrir el cuadro de diálogo Ejecutar</span><span class="sxs-lookup"><span data-stu-id="09d7a-146">Open the Run dialog box.</span></span> <span data-ttu-id="09d7a-147">Por ejemplo, presione `Windows logo key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="09d7a-147">For example, press the `Windows logo key` + `R`.</span></span>
    2. <span data-ttu-id="09d7a-148">Escriba `%systemroot%\system32\f12\IEChooser.exe` y, a continuación, **seleccione Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="09d7a-148">Enter `%systemroot%\system32\f12\IEChooser.exe`, and then select **Ok**.</span></span>
2.  <span data-ttu-id="09d7a-149">En IEChooser, seleccione la entrada para la pestaña Modo IE.</span><span class="sxs-lookup"><span data-stu-id="09d7a-149">In IEChooser, select the entry for the IE mode tab.</span></span>


## <a name="remote-debugging-and-ie-mode"></a><span data-ttu-id="09d7a-150">Depuración remota y modo IE</span><span class="sxs-lookup"><span data-stu-id="09d7a-150">Remote debugging and IE mode</span></span>  

<span data-ttu-id="09d7a-151">Inicie Microsoft Edge \(Chromium\) con la depuración remota activada desde la interfaz de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="09d7a-151">Launch Microsoft Edge \(Chromium\) with remote debugging turned on from the command-line interface.</span></span>  <span data-ttu-id="09d7a-152">Microsoft Visual Studio, Microsoft Visual Studio code y otras herramientas de desarrollo normalmente ejecutan un comando para iniciar Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="09d7a-152">Microsoft Visual Studio, Microsoft Visual Studio Code, and other development tools typically run a command to launch Microsoft Edge.</span></span>  <span data-ttu-id="09d7a-153">El siguiente comando inicia Microsoft Edge con el puerto de depuración remota establecido en `9222` .</span><span class="sxs-lookup"><span data-stu-id="09d7a-153">The following command launches Microsoft Edge with the remote debugging port set to `9222`.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="09d7a-154">Después de iniciar Microsoft Edge \(Chromium\) mediante un argumento de línea de comandos, el modo IE no está disponible.</span><span class="sxs-lookup"><span data-stu-id="09d7a-154">After you launch Microsoft Edge \(Chromium\) using a command-line argument, IE mode is unavailable.</span></span>  <span data-ttu-id="09d7a-155">Todavía puede navegar a sitios web \(o aplicaciones\) que de lo contrario se muestran en modo IE.</span><span class="sxs-lookup"><span data-stu-id="09d7a-155">You may still navigate to websites \(or apps\) that are otherwise displayed in IE mode.</span></span>  <span data-ttu-id="09d7a-156">El contenido del sitio web \(or app\) se representa Chromium, no Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="09d7a-156">The website \(or app\) content renders using Chromium, not Internet Explorer 11.</span></span>  <span data-ttu-id="09d7a-157">Espere que las partes de las páginas web que dependen de IE11, como los ActiveX, no se representen correctamente.</span><span class="sxs-lookup"><span data-stu-id="09d7a-157">Expect the parts of the webpages that rely on IE11, such as ActiveX controls, to not render correctly.</span></span>  <span data-ttu-id="09d7a-158">El distintivo de modo IE no aparece en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="09d7a-158">The IE mode badge does not appear in the address bar.</span></span>  

<span data-ttu-id="09d7a-159">El modo IE permanece no disponible hasta que se cierra completamente y se reinicia Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="09d7a-159">IE mode remains unavailable until you completely close and restart Microsoft Edge \(Chromium\).</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="09d7a-160">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="09d7a-160">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Uso de las herramientas de desarrollo de F12 | Microsoft Docs"  
