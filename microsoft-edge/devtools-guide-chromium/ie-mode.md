---
description: IE mode and the Microsoft Edge (cromo) DevTools
title: Modo Internet Explorer y DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, ie11, Internet Explorer 11, modo IE
ms.openlocfilehash: b059cae3ff48a45fe92cbf69e37ad692e329b200
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "11003979"
---
# <span data-ttu-id="1bea2-104">Modo Internet Explorer y DevTools</span><span class="sxs-lookup"><span data-stu-id="1bea2-104">Internet Explorer mode and the DevTools</span></span>  

<span data-ttu-id="1bea2-105">En este artículo se describe cómo el modo de Internet Explorer \ (modo IE \) se integra con el DevTools de Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="1bea2-105">This article describes how Internet Explorer mode \(IE mode\) integrates with the Microsoft Edge \(Chromium\) DevTools.</span></span>  

## <span data-ttu-id="1bea2-106">Descripción del modo IE</span><span class="sxs-lookup"><span data-stu-id="1bea2-106">Understanding IE mode</span></span>  

<span data-ttu-id="1bea2-107">El modo IE permite a las empresas especificar una lista de sitios web que solo funcionan en Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="1bea2-107">IE mode allows enterprises to specify a list of web sites that only work in Internet Explorer 11.</span></span>  <span data-ttu-id="1bea2-108">Al navegar a estos sitios web en Microsoft Edge \ (cromo \), se ejecuta una instancia de Internet Explorer 11 y se representa el sitio en una pestaña.  La funcionalidad permite a las empresas administrar la compatibilidad con tecnologías que actualmente no son compatibles con ningún explorador web moderno.</span><span class="sxs-lookup"><span data-stu-id="1bea2-108">When you navigate to these web sites in Microsoft Edge \(Chromium\), an instance of Internet Explorer 11 runs and renders the site in a tab.  The functionality allows enterprises to manage compatibility with technologies that are currently not compatible with any modern web browsers.</span></span>  <span data-ttu-id="1bea2-109">La compatibilidad con las siguientes tecnologías está incluida en el modo IE.</span><span class="sxs-lookup"><span data-stu-id="1bea2-109">Support for the following technologies is included in IE mode.</span></span>  

*   <span data-ttu-id="1bea2-110">Modos de documento de IE</span><span class="sxs-lookup"><span data-stu-id="1bea2-110">IE document modes</span></span>  
*   <span data-ttu-id="1bea2-111">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="1bea2-111">ActiveX controls</span></span>  
*   <span data-ttu-id="1bea2-112">otros componentes heredados</span><span class="sxs-lookup"><span data-stu-id="1bea2-112">other legacy components</span></span>  

<span data-ttu-id="1bea2-113">En el modo IE, el proceso de representación se basa en Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="1bea2-113">In IE mode, the rendering process is based on Internet Explorer 11.</span></span>  <span data-ttu-id="1bea2-114">El administrador de procesos de Microsoft Edge \ (cromo \) controla la duración del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="1bea2-114">The Microsoft Edge \(Chromium\) process manager handles the lifetime of the rendering process.</span></span>  <span data-ttu-id="1bea2-115">Está limitado a la duración de la pestaña de un sitio \ (o aplicación \).</span><span class="sxs-lookup"><span data-stu-id="1bea2-115">It is constrained to the lifetime of the tab for a specific site \(or app\).</span></span>  <span data-ttu-id="1bea2-116">Cuando se representa una tabulación en modo IE, aparece un distintivo en la barra de direcciones de la pestaña específica.</span><span class="sxs-lookup"><span data-stu-id="1bea2-116">When a tab renders in IE mode, a badge appears in the address bar for the specific tab.</span></span>  

:::image type="complex" source="./media/ie-mode-badge.msft.png" alt-text="Distintivo de modo IE en la barra de direcciones" lightbox="./media/ie-mode-badge.msft.png":::
   <span data-ttu-id="1bea2-118">Distintivo de modo IE en la barra de direcciones</span><span class="sxs-lookup"><span data-stu-id="1bea2-118">IE mode badge in the address bar</span></span>  
:::image-end:::  

<span data-ttu-id="1bea2-119">El modo IE está disponible actualmente en Windows 10 versión 1903 \ (May 2019 Update \), pero pronto estará disponible para todas las plataformas de Windows compatibles.</span><span class="sxs-lookup"><span data-stu-id="1bea2-119">IE mode is currently available on Windows 10 Version 1903 \(May 2019 Update\), but is coming soon to all supported Windows platforms.</span></span>  

## <span data-ttu-id="1bea2-120">Iniciar DevTools en una pestaña en modo IE</span><span class="sxs-lookup"><span data-stu-id="1bea2-120">Launching the DevTools on a tab in IE mode</span></span>  

<span data-ttu-id="1bea2-121">Si está intentando ver el modo de documento de un sitio web en modo IE, elija el distintivo en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="1bea2-121">If you are trying to view the document mode of a web site in IE mode, choose the badge in the address bar.</span></span>  

:::image type="complex" source="./media/ie-mode-badge-doc-mode.msft.png" alt-text="Ver el modo de documento con distintivo de modo IE" lightbox="./media/ie-mode-badge-doc-mode.msft.png":::
   <span data-ttu-id="1bea2-123">Ver el modo de documento con distintivo de modo IE</span><span class="sxs-lookup"><span data-stu-id="1bea2-123">View document mode using IE mode badge</span></span>  
:::image-end:::  

<span data-ttu-id="1bea2-124">Si una pestaña está usando el modo IE, la DevTools no funciona y se producen las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="1bea2-124">If a tab is using IE mode, the DevTools do not work and the following conditions occur.</span></span>

*   <span data-ttu-id="1bea2-125">Si seleccionas `F12` o seleccionas `Ctrl` + `Shift` + `I` , se inicia una instancia en blanco de la DevTools de Microsoft Edge \ (cromo \) y se muestra el siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="1bea2-125">If you select `F12` or select `Ctrl`+`Shift`+`I`, a blank instance of the Microsoft Edge \(Chromium\) DevTools is launched displays the following message.</span></span>  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   <span data-ttu-id="1bea2-126">Si abre un menú contextual \ (haga clic con el botón derecho \) y elige **Ver origen**, se inicia el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="1bea2-126">If you open a contextual menu \(right-click\) and choose **View Source**, Notepad is launched.</span></span>  
*   <span data-ttu-id="1bea2-127">Si abre un menú contextual \ (haga clic con el botón derecho \), el **elemento inspeccionar** no está visible.</span><span class="sxs-lookup"><span data-stu-id="1bea2-127">If you open a contextual menu \(right-click\), the **Inspect Element** is not visible.</span></span>  

<span data-ttu-id="1bea2-128">El motivo por el que una serie de herramientas de DevTools \ (como las herramientas de **rendimiento** y **red** \) no funciona es el motor de representación cambia de cromo a Internet Explorer 11 en modo IE.</span><span class="sxs-lookup"><span data-stu-id="1bea2-128">The reason that a number of the tools within the DevTools \(like the **Network** and **Performance** tools\) do not work is the rendering engine switches from Chromium to Internet Explorer 11 in IE mode.</span></span>  <span data-ttu-id="1bea2-129">Para proporcionar comentarios, navegue para [ponerse en contacto con el equipo de Microsoft Edge DevTools](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="1bea2-129">To provide feedback, navigate to [Getting in touch with the Microsoft Edge DevTools team](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

:::image type="complex" source="./media/ie-mode-devtools.msft.png" alt-text="DevTools iniciado en modo IE" lightbox="./media/ie-mode-devtools.msft.png":::
   <span data-ttu-id="1bea2-131">DevTools iniciado en modo IE</span><span class="sxs-lookup"><span data-stu-id="1bea2-131">DevTools launched in IE mode</span></span>  
:::image-end:::  

<span data-ttu-id="1bea2-132">Para probar su sitio web basado en Internet Explorer 11 \ (o aplicación \) en el modo Internet Explorer 11 e IE, realice los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="1bea2-132">To test your Internet Explorer 11-based website \(or app\) in Internet Explorer 11 and IE mode, perform the following steps.</span></span>  

1.  <span data-ttu-id="1bea2-133">Abra Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="1bea2-133">Open Internet Explorer 11.</span></span>  
    *   <span data-ttu-id="1bea2-134">En Windows 10, busque el acceso directo para Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="1bea2-134">On Windows 10, locate the shortcut for Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="1bea2-135">**Menú Inicio**  >  **Accesorios**  >  de Windows **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="1bea2-135">**Start Menu** > **Windows Accessories** > **Internet Explorer 11**.</span></span>  
    *   <span data-ttu-id="1bea2-136">En Windows 7, busque Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="1bea2-136">On Windows 7, locate Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="1bea2-137">**Menú Inicio**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="1bea2-137">**Start Menu** > **Internet Explorer 11**.</span></span>  
1.  <span data-ttu-id="1bea2-138">En Internet Explorer 11, abra la misma página web.</span><span class="sxs-lookup"><span data-stu-id="1bea2-138">In Internet Explorer 11, open the same webpage.</span></span>  
1.  <span data-ttu-id="1bea2-139">Inicie Internet Explorer DevTools.</span><span class="sxs-lookup"><span data-stu-id="1bea2-139">Launch the Internet Explorer DevTools.</span></span>  
    *   <span data-ttu-id="1bea2-140">Seleccione `F12` .</span><span class="sxs-lookup"><span data-stu-id="1bea2-140">Select `F12`.</span></span>  
    *   <span data-ttu-id="1bea2-141">Mantenga el puntero sobre cualquier lugar, abra un menú contextual \ (haga clic con el botón derecho \) y elija **Inspeccionar elemento**.</span><span class="sxs-lookup"><span data-stu-id="1bea2-141">Hover anywhere, open a contextual menu \(right-click\), and choose **Inspect element**.</span></span>  <span data-ttu-id="1bea2-142">Para obtener más información sobre cómo usar estas herramientas, vaya a [usar las herramientas de desarrollo F12][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span><span class="sxs-lookup"><span data-stu-id="1bea2-142">For more information about how to use those tools, navigate to [Using the F12 developer tools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span></span>  

## <span data-ttu-id="1bea2-143">Depuración remota y modo IE</span><span class="sxs-lookup"><span data-stu-id="1bea2-143">Remote debugging and IE mode</span></span>  

<span data-ttu-id="1bea2-144">Inicia Microsoft Edge \ (cromo \) con la depuración remota activada desde la interfaz de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="1bea2-144">Launch Microsoft Edge \(Chromium\) with remote debugging turned on from the command-line interface.</span></span>  <span data-ttu-id="1bea2-145">Visual Studio, el código Visual Studio y otras herramientas de desarrollo suelen ejecutar un comando para iniciar Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1bea2-145">Visual Studio, Visual Studio Code, and other development tools typically run a command to launch Microsoft Edge.</span></span>  <span data-ttu-id="1bea2-146">El siguiente comando inicia Microsoft Edge con el puerto de depuración remota establecido en `9222` .</span><span class="sxs-lookup"><span data-stu-id="1bea2-146">The following command launches Microsoft Edge with the remote debugging port set to `9222`.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="1bea2-147">Después de iniciar Microsoft Edge \ (cromo \) con un argumento de línea de comandos, el modo IE no está disponible.</span><span class="sxs-lookup"><span data-stu-id="1bea2-147">After you launch Microsoft Edge \(Chromium\) using a command-line argument, IE mode is unavailable.</span></span>  <span data-ttu-id="1bea2-148">Aún puede navegar a sitios web \ (o aplicaciones \) que, de lo contrario, se mostrarán en modo IE.</span><span class="sxs-lookup"><span data-stu-id="1bea2-148">You may still navigate to websites \(or apps\) that would otherwise display in IE mode.</span></span> <span data-ttu-id="1bea2-149">El contenido del sitio web \ (o aplicación \) se representa con cromo, no con Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="1bea2-149">The website \(or app\) content renders using Chromium, not Internet Explorer 11.</span></span>  <span data-ttu-id="1bea2-150">Espere que las partes de las páginas que dependen de IE11, como los controles ActiveX, no se representen correctamente.</span><span class="sxs-lookup"><span data-stu-id="1bea2-150">Expect the parts of the pages that rely on IE11, such as ActiveX controls, to not render correctly.</span></span>  <span data-ttu-id="1bea2-151">La tarjeta de identificación de modo de IE no aparece en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="1bea2-151">The IE mode badge does not appear in the address bar.</span></span>  

<span data-ttu-id="1bea2-152">El modo IE no está disponible hasta que se cierra completamente y se reinicie Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="1bea2-152">IE mode remains unavailable until you completely close and restart Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="1bea2-153">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1bea2-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Usar las herramientas de desarrollo F12 | Microsoft docs"  