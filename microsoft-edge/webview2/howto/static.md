---
description: Obtenga información sobre cómo vincular estáticamente la biblioteca del cargador de WebView2.
title: Cómo vincular estáticamente la biblioteca del cargador de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 397c226eb958d1e656fb0ecb6dd8f1e2fe300746
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230932"
---
# <span data-ttu-id="84be4-104">Vincular estáticamente la biblioteca del cargador de WebView2</span><span class="sxs-lookup"><span data-stu-id="84be4-104">Statically link the WebView2 loader library</span></span>  

<span data-ttu-id="84be4-105">Es posible que desee distribuir su aplicación con un único archivo ejecutable, en lugar de un paquete de muchos archivos.</span><span class="sxs-lookup"><span data-stu-id="84be4-105">You may want to distribute your application with a single executable file, instead of a package of many files.</span></span> <span data-ttu-id="84be4-106">Para crear un único archivo ejecutable o reducir el tamaño del paquete, debe vincular estáticamente los archivos de WebView2Loader.</span><span class="sxs-lookup"><span data-stu-id="84be4-106">To create a single executable file, or to reduce the size of your package, you should statically link the WebView2Loader files.</span></span> <span data-ttu-id="84be4-107">El SDK de WebView2 contiene un archivo de encabezado, `WebView2Loader.dll` y el `IDL` archivo.</span><span class="sxs-lookup"><span data-stu-id="84be4-107">The WebView2 SDK contains a header file, `WebView2Loader.dll`, and the `IDL` file.</span></span> `WebView2Loader.dll` <span data-ttu-id="84be4-108">es un pequeño componente que ayuda a que las aplicaciones encuentren el tiempo de ejecución de WebView2 o los canales no estables de Microsoft Edge en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84be4-108">is a small component that helps apps locate the WebView2 Runtime, or non-stable channels of Microsoft Edge, on the device.</span></span>  

<span data-ttu-id="84be4-109">Para las aplicaciones que no deseen enviar un `WebView2Loader.dll` , complete los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="84be4-109">For apps that don't want to ship a `WebView2Loader.dll`, complete the following steps.</span></span>  

1.  <span data-ttu-id="84be4-110">Abra el `.vcxproj` archivo de proyecto de la aplicación en un editor de texto, como código de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="84be4-110">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="84be4-111">El `.vcproj` archivo de proyecto puede ser un archivo oculto, lo que significa que no se muestra en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="84be4-111">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span></span>  <span data-ttu-id="84be4-112">Use la línea de comandos para buscar archivos ocultos.</span><span class="sxs-lookup"><span data-stu-id="84be4-112">Use the command-line to find hidden files.</span></span>  
    
1.  <span data-ttu-id="84be4-113">Busca la sección en el código en la que incluyes los archivos de destino del paquete NuGet de WebView2.</span><span class="sxs-lookup"><span data-stu-id="84be4-113">Locate the section in the code where you include the WebView2 NuGet package target files.</span></span>  <span data-ttu-id="84be4-114">La ubicación en el código se resalta en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="84be4-114">The location in the code is highlighted in the following figure.</span></span>  

    :::image type="complex" source="./media/inserthere.png" alt-text="Fragmentos de código de archivos de proyecto" lightbox="./media/inserthere.png":::
       <span data-ttu-id="84be4-116">Fragmentos de código de archivos de proyecto</span><span class="sxs-lookup"><span data-stu-id="84be4-116">Project Files code snippet</span></span>   
    :::image-end:::  
  
1.  <span data-ttu-id="84be4-117">Copie el siguiente fragmento de código y péguelo donde `Microsoft.Web.WebView2.targets` esté incluido.</span><span class="sxs-lookup"><span data-stu-id="84be4-117">Copy the following code snippet and paste it where the `Microsoft.Web.WebView2.targets` is included.</span></span>  

    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```
      
    :::image type="complex" source="./media/staticlib.png" alt-text="Fragmento de código insertado" lightbox="./media/staticlib.png":::
       <span data-ttu-id="84be4-119">Fragmento de código insertado</span><span class="sxs-lookup"><span data-stu-id="84be4-119">Inserted code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="84be4-120">Edite las dependencias adicionales de la configuración de compilación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="84be4-120">Edit the additional dependencies of the build configuration for your app.</span></span>  <span data-ttu-id="84be4-121">Para empezar, busque todas las `<AdditionalDependencies>` etiquetas.</span><span class="sxs-lookup"><span data-stu-id="84be4-121">To begin, find all of the `<AdditionalDependencies>` tags.</span></span> <span data-ttu-id="84be4-122">Para cada uno, agregue `version.lib` como una dependencia adicional a cada configuración de compilación distinta del `.vcxproj` archivo.</span><span class="sxs-lookup"><span data-stu-id="84be4-122">For each, add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file.</span></span>  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Agregar version. lib a ItemDefinitionGroups" lightbox="./media/versionlib.png":::
       <span data-ttu-id="84be4-124">Agregar `version.lib` a</span><span class="sxs-lookup"><span data-stu-id="84be4-124">Adding `version.lib` to</span></span> `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="84be4-125">El equipo WebView2 tiene como objetivo automatizar la adición de la dependencia adicional en versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="84be4-125">The WebView2 team aims to automate adding the additional dependency in future releases.</span></span>  
    
1. <span data-ttu-id="84be4-126">Compila y ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="84be4-126">Compile and run your app.</span></span>

### <span data-ttu-id="84be4-127">Ponerse en contacto con el equipo de WebView2</span><span class="sxs-lookup"><span data-stu-id="84be4-127">Getting in touch with the WebView2 team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

### <span data-ttu-id="84be4-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="84be4-128">See also</span></span>  

*   <span data-ttu-id="84be4-129">Para comenzar a usar WebView2, vaya a [WebView2 guías de introducción][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="84be4-129">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="84be4-130">Para obtener un ejemplo completo de las capacidades de WebView2, vaya a [WebView2Samples][GithubMicrosoftedgeWebview2samples] en github.</span><span class="sxs-lookup"><span data-stu-id="84be4-130">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>
*   <span data-ttu-id="84be4-131">Para obtener información más detallada sobre las API de WebView2, vaya a referencia de la [API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="84be4-131">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="84be4-132">Para obtener más información sobre WebView2, vaya a [recursos WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="84be4-132">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[Webview2ApiReference]: ../webview2-api-reference.md "Referencia de la API de Microsoft Edge WebView2 | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Introducción: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "¿Qué novedades hay? -Depurador de JavaScript para Visual Studio Code-Microsoft/vscode-JS-Debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicaciones de WebView de Microsoft Edge (cromo): depurador de código de Visual Studio para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
