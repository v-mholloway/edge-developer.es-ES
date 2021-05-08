---
description: Obtenga información sobre cómo vincular estáticamente la biblioteca de cargadores de WebView2.
title: Cómo vincular estáticamente la biblioteca de cargadores de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, html perimetral
ms.openlocfilehash: 8f48a4fde9e2960de6156fc14db8c84f87a49868
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536175"
---
# <a name="statically-link-the-webview2-loader-library"></a><span data-ttu-id="7072f-104">Vincular estáticamente la biblioteca de cargadores de WebView2</span><span class="sxs-lookup"><span data-stu-id="7072f-104">Statically link the WebView2 loader library</span></span>  

<span data-ttu-id="7072f-105">Es posible que desee distribuir la aplicación con un único archivo ejecutable, en lugar de un paquete de muchos archivos.</span><span class="sxs-lookup"><span data-stu-id="7072f-105">You may want to distribute your application with a single executable file, instead of a package of many files.</span></span> <span data-ttu-id="7072f-106">Para crear un único archivo ejecutable o reducir el tamaño del paquete, debe vincular estáticamente los archivos WebView2Loader.</span><span class="sxs-lookup"><span data-stu-id="7072f-106">To create a single executable file, or to reduce the size of your package, you should statically link the WebView2Loader files.</span></span> <span data-ttu-id="7072f-107">El SDK de WebView2 contiene un archivo de encabezado `WebView2Loader.dll` y el `IDL` archivo.</span><span class="sxs-lookup"><span data-stu-id="7072f-107">The WebView2 SDK contains a header file, `WebView2Loader.dll`, and the `IDL` file.</span></span> `WebView2Loader.dll` <span data-ttu-id="7072f-108">es un componente pequeño que ayuda a las aplicaciones a localizar WebView2 Runtime, o canales no estables de Microsoft Edge, en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7072f-108">is a small component that helps apps locate the WebView2 Runtime, or non-stable channels of Microsoft Edge, on the device.</span></span>  

<span data-ttu-id="7072f-109">Para las aplicaciones que no desean enviar un `WebView2Loader.dll` , siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="7072f-109">For apps that don't want to ship a `WebView2Loader.dll`, complete the following steps.</span></span>  

1.  <span data-ttu-id="7072f-110">Abra el `.vcxproj` archivo de proyecto de la aplicación en un editor de texto, como Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="7072f-110">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="7072f-111">El `.vcproj` archivo de proyecto puede ser un archivo oculto, lo que significa que no se muestra en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7072f-111">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span></span>  <span data-ttu-id="7072f-112">Use la línea de comandos para buscar archivos ocultos.</span><span class="sxs-lookup"><span data-stu-id="7072f-112">Use the command-line to find hidden files.</span></span>  
    
1.  <span data-ttu-id="7072f-113">Busque la sección en el código donde se incluyen los archivos de destino de NuGet webView2.</span><span class="sxs-lookup"><span data-stu-id="7072f-113">Locate the section in the code where you include the WebView2 NuGet package target files.</span></span>  <span data-ttu-id="7072f-114">La ubicación del código se resalta en la siguiente figura.</span><span class="sxs-lookup"><span data-stu-id="7072f-114">The location in the code is highlighted in the following figure.</span></span>  
    
    :::image type="complex" source="./media/insert-here.png" alt-text="Project Fragmento de código de archivos" lightbox="./media/insert-here.png":::
       <span data-ttu-id="7072f-116">Project Fragmento de código de archivos</span><span class="sxs-lookup"><span data-stu-id="7072f-116">Project Files code snippet</span></span>   
    :::image-end:::  
    
1.  <span data-ttu-id="7072f-117">Copie el siguiente fragmento de código y péguelo donde `Microsoft.Web.WebView2.targets` esté incluido.</span><span class="sxs-lookup"><span data-stu-id="7072f-117">Copy the following code snippet and paste it where the `Microsoft.Web.WebView2.targets` is included.</span></span>  
    
    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```  
    
    :::image type="complex" source="./media/static-lib.png" alt-text="Fragmento de código insertado" lightbox="./media/static-lib.png":::
       <span data-ttu-id="7072f-119">Fragmento de código insertado</span><span class="sxs-lookup"><span data-stu-id="7072f-119">Inserted code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7072f-120">Edite las dependencias adicionales de la configuración de compilación para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7072f-120">Edit the additional dependencies of the build configuration for your app.</span></span>  <span data-ttu-id="7072f-121">Para empezar, busque todas las `<AdditionalDependencies>` etiquetas.</span><span class="sxs-lookup"><span data-stu-id="7072f-121">To begin, find all of the `<AdditionalDependencies>` tags.</span></span> <span data-ttu-id="7072f-122">Para cada uno, agregue `version.lib` como dependencia adicional a cada configuración de compilación diferente en el `.vcxproj` archivo.</span><span class="sxs-lookup"><span data-stu-id="7072f-122">For each, add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file.</span></span>  
    
    :::image type="complex" source="./media/version-lib.png" alt-text="Adición de version.lib a ItemDefinitionGroups" lightbox="./media/version-lib.png":::
       <span data-ttu-id="7072f-124">Agregar `version.lib` a</span><span class="sxs-lookup"><span data-stu-id="7072f-124">Adding `version.lib` to</span></span> `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="7072f-125">El equipo de WebView2 tiene como objetivo automatizar la adición de la dependencia adicional en futuras versiones.</span><span class="sxs-lookup"><span data-stu-id="7072f-125">The WebView2 team aims to automate adding the additional dependency in future releases.</span></span>  
    
1.  <span data-ttu-id="7072f-126">Compila y ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7072f-126">Compile and run your app.</span></span>  
    
## <a name="getting-in-touch-with-the-webview2-team"></a><span data-ttu-id="7072f-127">Getting in touch with the WebView2 team</span><span class="sxs-lookup"><span data-stu-id="7072f-127">Getting in touch with the WebView2 team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

## <a name="see-also"></a><span data-ttu-id="7072f-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7072f-128">See also</span></span>  

*   <span data-ttu-id="7072f-129">Para empezar a usar WebView2, vaya a [WebView2 Introducción Guías][Webview2MainGetStarted].</span><span class="sxs-lookup"><span data-stu-id="7072f-129">To get started using WebView2, navigate to [WebView2 Get Started Guides][Webview2MainGetStarted].</span></span>  
*   <span data-ttu-id="7072f-130">Para obtener un ejemplo completo de las funcionalidades de WebView2, vaya a [WebView2Samples][GithubMicrosoftedgeWebview2samples] en GitHub.</span><span class="sxs-lookup"><span data-stu-id="7072f-130">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>
*   <span data-ttu-id="7072f-131">Para obtener información más detallada acerca de las API de WebView2, vaya a [Referencia de API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="7072f-131">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="7072f-132">Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="7072f-132">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>
    
<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2 API Reference | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Pasos siguientes: introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  
[Webview2MainGetStarted]: ../index.md#get-started "Introducción: introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "¿Cuáles son las novedades? - Depurador de JavaScript para Visual Studio Code: microsoft/vscode-js-debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge webview (Chromium) - Visual Studio Code - Depurador para Microsoft Edge - microsoft/vscode-edge-debug2 | GitHub"  
