---
description: Obtenga información sobre cómo vincular estáticamente la biblioteca del cargador de WebView2.
title: Cómo vincular estáticamente la biblioteca del cargador de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/01/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: b7e0ec70cb00f318d4eb67254f37fcec79a5fcf6
ms.sourcegitcommit: 903524ab85321ade278facd741d6487e8cabe33f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/06/2020
ms.locfileid: "11100322"
---
# <span data-ttu-id="13feb-104">Cómo vincular estáticamente la biblioteca del cargador de WebView2</span><span class="sxs-lookup"><span data-stu-id="13feb-104">How to Statically link the WebView2 loader library</span></span>  

## <span data-ttu-id="13feb-105">Contexto</span><span class="sxs-lookup"><span data-stu-id="13feb-105">Context</span></span>  

<span data-ttu-id="13feb-106">¿Qué es el WebView2Loader.dll?</span><span class="sxs-lookup"><span data-stu-id="13feb-106">What is the WebView2Loader.dll?</span></span>  

*   <span data-ttu-id="13feb-107">El SDK de WebView2 contiene un archivo de encabezado, `WebView2Loader.dll.` y el `IDL` archivo.</span><span class="sxs-lookup"><span data-stu-id="13feb-107">The WebView2 SDK contains a header file, `WebView2Loader.dll.`, and the `IDL` file.</span></span> `WebView2Loader.dll` <span data-ttu-id="13feb-108">es un pequeño componente que ayuda a que las aplicaciones encuentren el tiempo de ejecución de WebView2 (o canales de Microsoft Edge no estables) en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13feb-108">is a small component that helps apps locate the WebView2 Runtime (or non-stable Microsoft Edge channels) on the device.</span></span>  

<span data-ttu-id="13feb-109">Para las aplicaciones que tienen un único tiempo de ejecución y no desean enviar un `WebView2Loader.dll` , complete los siguientes pasos de **procedimiento** .</span><span class="sxs-lookup"><span data-stu-id="13feb-109">For apps that have a single runtime, and do not want to ship a `WebView2Loader.dll`, complete the following **Procedure** steps.</span></span>  

## <span data-ttu-id="13feb-110">Procedimiento</span><span class="sxs-lookup"><span data-stu-id="13feb-110">Procedure</span></span>  

1.  <span data-ttu-id="13feb-111">Abra el `.vcxproj` archivo de proyecto de la aplicación en un editor de texto, como código de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="13feb-111">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="13feb-112">El `.vcproj` archivo de proyecto puede ser un archivo oculto, lo que significa que no se muestra en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="13feb-112">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span></span>  <span data-ttu-id="13feb-113">Use la línea de comandos para buscar un archivo oculto.</span><span class="sxs-lookup"><span data-stu-id="13feb-113">Use the command-line to find a hidden file.</span></span>  
    
1.  <span data-ttu-id="13feb-114">Busca la sección en el código en la que incluyes los archivos de destino del paquete NuGet de WebView2.</span><span class="sxs-lookup"><span data-stu-id="13feb-114">Locate the section in the code where you include the WebView2 NuGet package target files.</span></span>  <span data-ttu-id="13feb-115">La ubicación en el código se resalta en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="13feb-115">The location in the code is highlighted in the following figure.</span></span>  
    
    :::image type="complex" source="./media/inserthere.png" alt-text="Fragmentos de código de archivos de proyecto" lightbox="./media/inserthere.png"::: 
       <span data-ttu-id="13feb-117">Fragmentos de código de archivos de proyecto</span><span class="sxs-lookup"><span data-stu-id="13feb-117">Project Files code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="13feb-118">Copie el siguiente fragmento de código y péguelo donde `Microsoft.Web.WebView2.targets` esté incluido.</span><span class="sxs-lookup"><span data-stu-id="13feb-118">Copy the following code snippet and paste it everywhere the `Microsoft.Web.WebView2.targets` is included.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="13feb-119">Por ejemplo, lo incluye después del bloque de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="13feb-119">For example, include it after the following code block.</span></span>  
    > 
    > ```csharp
    > <Import Project="..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets" Condition="Exists('..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets')" />
    > ```  
    
    ```csharp
    <PropertyGroup> <WebView2LoaderPreference>Static</WebView2LoaderPreference> </PropertyGroup>
    ```
    
    :::image type="complex" source="./media/staticlib.png" alt-text="Fragmentos de código de archivos de proyecto" lightbox="./media/staticlib.png"::: 
       <span data-ttu-id="13feb-121">Fragmento de código insertado</span><span class="sxs-lookup"><span data-stu-id="13feb-121">Inserted code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="13feb-122">Edite las dependencias adicionales de la configuración de compilación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="13feb-122">Edit the additional dependencies of the build configuration for your app.</span></span>  <span data-ttu-id="13feb-123">Para empezar, busque todas las `<AdditionalDependencies>` etiquetas.</span><span class="sxs-lookup"><span data-stu-id="13feb-123">To begin, find all of the `<AdditionalDependencies>` tags.</span></span>  
1.  <span data-ttu-id="13feb-124">Agregue `version.lib` como una dependencia adicional a cada configuración de compilación distinta en el `.vcxproj` archivo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="13feb-124">Add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file for your app.</span></span>  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Fragmentos de código de archivos de proyecto" lightbox="./media/versionlib.png"::: 
       <span data-ttu-id="13feb-126">Agregar `version.lib` a</span><span class="sxs-lookup"><span data-stu-id="13feb-126">Adding `version.lib` to</span></span> `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="13feb-127">El equipo de WebView2 se propone automatizar el paso de dependencia adicional en futuras versiones.</span><span class="sxs-lookup"><span data-stu-id="13feb-127">The WebView2 team aims to automate the additional dependency step in future releases.</span></span>  
    
<span data-ttu-id="13feb-128">Compile e implemente la aplicación.</span><span class="sxs-lookup"><span data-stu-id="13feb-128">Compile and deploy your app.</span></span>  <span data-ttu-id="13feb-129">Intentos.</span><span class="sxs-lookup"><span data-stu-id="13feb-129">Success.</span></span>  

## <span data-ttu-id="13feb-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="13feb-130">See also</span></span>  

*   <span data-ttu-id="13feb-131">Para comenzar a usar WebView2, vaya a [WebView2 guías de introducción][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="13feb-131">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="13feb-132">Para obtener un ejemplo completo de las capacidades de WebView2, vaya a [WebView2Samples][GithubMicrosoftedgeWebview2samples] en github.</span><span class="sxs-lookup"><span data-stu-id="13feb-132">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>
*   <span data-ttu-id="13feb-133">Para obtener información más detallada sobre las API de WebView2, vaya a referencia de la [API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="13feb-133">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="13feb-134">Para obtener más información sobre WebView2, vaya a [recursos WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="13feb-134">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>

## <span data-ttu-id="13feb-135">Ponerse en contacto con el equipo de WebView2</span><span class="sxs-lookup"><span data-stu-id="13feb-135">Getting in touch with the WebView2 team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[Webview2ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "AdditionalBrowserArguments-0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions clase | Microsoft docs"  
[Webview2ReferenceWin3209622Webview2IdlParameters]: ../reference/win32/0-9-622/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-Globals | Microsoft docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Referencia de la API de Microsoft Edge WebView2 | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Introducción: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "¿Qué novedades hay? -Depurador de JavaScript para Visual Studio Code-Microsoft/vscode-JS-Debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicaciones de WebView de Microsoft Edge (cromo): depurador de código de Visual Studio para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
