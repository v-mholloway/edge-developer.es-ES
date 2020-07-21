---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 6e32c6c050e37f35190a2bf01cd564cd58257b06
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884893"
---
# <span data-ttu-id="e17af-104">0.9.515: ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="e17af-104">0.9.515 - interface ICoreWebView2EnvironmentOptions</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2EnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="e17af-105">Opciones usadas para crear un entorno WebView2.</span><span class="sxs-lookup"><span data-stu-id="e17af-105">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="e17af-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e17af-106">Summary</span></span>

 <span data-ttu-id="e17af-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e17af-107">Members</span></span>                        | <span data-ttu-id="e17af-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e17af-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e17af-109">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="e17af-109">get_AdditionalBrowserArguments</span></span>](#get_additionalbrowserarguments) | <span data-ttu-id="e17af-110">AdditionalBrowserArguments se puede especificar para cambiar el comportamiento de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="e17af-110">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="e17af-111">get_Language</span><span class="sxs-lookup"><span data-stu-id="e17af-111">get_Language</span></span>](#get_language) | <span data-ttu-id="e17af-112">El idioma predeterminado con el que se ejecutará la vista previa.</span><span class="sxs-lookup"><span data-stu-id="e17af-112">The default language that WebView will run with.</span></span>
[<span data-ttu-id="e17af-113">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="e17af-113">get_TargetCompatibleBrowserVersion</span></span>](#get_targetcompatiblebrowserversion) | <span data-ttu-id="e17af-114">La versión de los binarios de la WebView2 en tiempo de ejecución para que sea compatible con la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="e17af-114">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="e17af-115">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="e17af-115">put_AdditionalBrowserArguments</span></span>](#put_additionalbrowserarguments) | <span data-ttu-id="e17af-116">Establezca la propiedad AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="e17af-116">Set the AdditionalBrowserArguments property.</span></span>
[<span data-ttu-id="e17af-117">put_Language</span><span class="sxs-lookup"><span data-stu-id="e17af-117">put_Language</span></span>](#put_language) | <span data-ttu-id="e17af-118">Establezca la propiedad de idioma.</span><span class="sxs-lookup"><span data-stu-id="e17af-118">Set the Language property.</span></span>
[<span data-ttu-id="e17af-119">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="e17af-119">put_TargetCompatibleBrowserVersion</span></span>](#put_targetcompatiblebrowserversion) | <span data-ttu-id="e17af-120">Establezca el TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="e17af-120">Set the TargetCompatibleBrowserVersion.</span></span>

<span data-ttu-id="e17af-121">Se proporciona una implementación predeterminada en WebView2EnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="e17af-121">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    if(!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## <span data-ttu-id="e17af-122">Miembros</span><span class="sxs-lookup"><span data-stu-id="e17af-122">Members</span></span>

#### <span data-ttu-id="e17af-123">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="e17af-123">get_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="e17af-124">AdditionalBrowserArguments se puede especificar para cambiar el comportamiento de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="e17af-124">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="e17af-125">[get_AdditionalBrowserArguments](#get_additionalbrowserarguments)de HRESULT público (valor LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="e17af-125">public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span></span>

<span data-ttu-id="e17af-126">Se pasarán al proceso de explorador como parte de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="e17af-126">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="e17af-127">Consulte [Ejecutar cromo con marcas](https://aka.ms/RunChromiumWithFlags) para obtener más información acerca de los modificadores de la línea de comandos para el proceso del explorador.</span><span class="sxs-lookup"><span data-stu-id="e17af-127">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="e17af-128">Si la aplicación se inicia con un modificador de línea de comandos, `--edge-webview-switches=xxx` el valor de ese modificador (XXX en el ejemplo anterior) también se anexará a la línea de comandos del proceso del explorador.</span><span class="sxs-lookup"><span data-stu-id="e17af-128">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="e17af-129">Algunos conmutadores como los `--user-data-dir` de WebView son internos y importantes.</span><span class="sxs-lookup"><span data-stu-id="e17af-129">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="e17af-130">Estos conmutadores se ignorarán incluso si se especifican.</span><span class="sxs-lookup"><span data-stu-id="e17af-130">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="e17af-131">Si se especifican los mismos modificadores varias veces, se gana la última.</span><span class="sxs-lookup"><span data-stu-id="e17af-131">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="e17af-132">No hay ningún intento de combinar los distintos valores del mismo modificador, excepto para las características deshabilitado y habilitado.</span><span class="sxs-lookup"><span data-stu-id="e17af-132">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="e17af-133">Las características especificadas por `--enable-features` y se `--disable-features` combinarán con lógica simple: las características serán la Unión de las características especificadas y las características integradas, y si una característica está deshabilitada, se quitará de la lista de características habilitadas.</span><span class="sxs-lookup"><span data-stu-id="e17af-133">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="e17af-134">El valor de la línea de comandos del proceso de la aplicación `--edge-webview-switches` se procesa después de que se procese el parámetro additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="e17af-134">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="e17af-135">Ciertas características están deshabilitadas internamente y no se pueden habilitar.</span><span class="sxs-lookup"><span data-stu-id="e17af-135">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="e17af-136">Si se produjo un error de análisis en los modificadores especificados, se ignorarán.</span><span class="sxs-lookup"><span data-stu-id="e17af-136">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="e17af-137">El valor predeterminado es ejecutar el proceso del explorador sin ningún marcador adicional.</span><span class="sxs-lookup"><span data-stu-id="e17af-137">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="e17af-138">get_Language</span><span class="sxs-lookup"><span data-stu-id="e17af-138">get_Language</span></span> 

<span data-ttu-id="e17af-139">El idioma predeterminado con el que se ejecutará la vista previa.</span><span class="sxs-lookup"><span data-stu-id="e17af-139">The default language that WebView will run with.</span></span>

> <span data-ttu-id="e17af-140">[get_Language](#get_language)de HRESULT público (valor LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="e17af-140">public HRESULT [get_Language](#get_language)(LPWSTR \* value)</span></span>

<span data-ttu-id="e17af-141">Se aplica a ius del explorador, como menús contextuales y cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e17af-141">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="e17af-142">También se aplica al encabezado HTTP Accept-Languages que la vista Web envía a los sitios Web.</span><span class="sxs-lookup"><span data-stu-id="e17af-142">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="e17af-143">Está en el formato de `language[-country]` donde `language` es el código de 2 Letras de ISO 639 y `country` es el código de 2 letras de ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="e17af-143">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="e17af-144">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="e17af-144">get_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="e17af-145">La versión de los binarios de la WebView2 en tiempo de ejecución para que sea compatible con la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="e17af-145">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="e17af-146">[get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)de HRESULT público (valor LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="e17af-146">public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span></span>

<span data-ttu-id="e17af-147">De forma predeterminada, la versión de tiempo de ejecución de Edge WebView2 que corresponde a la versión del SDK que usa la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e17af-147">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="e17af-148">El formato de este valor es el mismo que el formato de la propiedad BrowserVersionString y otros valores de BrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="e17af-148">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="e17af-149">Solo se respeta la parte de versión del valor BrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="e17af-149">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="e17af-150">El sufijo de canal, si existe, se pasa por alto.</span><span class="sxs-lookup"><span data-stu-id="e17af-150">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="e17af-151">La versión de los binarios de tiempo de ejecución de WebView2 que se usó en realidad puede ser diferente de la TargetCompatibleBrowserVersion especificada.</span><span class="sxs-lookup"><span data-stu-id="e17af-151">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="e17af-152">Solo se garantiza que son compatibles.</span><span class="sxs-lookup"><span data-stu-id="e17af-152">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="e17af-153">Puedes comprobar la versión real en la propiedad BrowserVersionString de la ICoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="e17af-153">You can check the actual version on the BrowserVersionString property on the ICoreWebView2Environment.</span></span>

#### <span data-ttu-id="e17af-154">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="e17af-154">put_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="e17af-155">Establezca la propiedad AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="e17af-155">Set the AdditionalBrowserArguments property.</span></span>

> <span data-ttu-id="e17af-156">[put_AdditionalBrowserArguments](#put_additionalbrowserarguments)de HRESULT público (valor de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="e17af-156">public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR value)</span></span>

#### <span data-ttu-id="e17af-157">put_Language</span><span class="sxs-lookup"><span data-stu-id="e17af-157">put_Language</span></span> 

<span data-ttu-id="e17af-158">Establezca la propiedad de idioma.</span><span class="sxs-lookup"><span data-stu-id="e17af-158">Set the Language property.</span></span>

> <span data-ttu-id="e17af-159">[put_Language](#put_language)de HRESULT público (valor de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="e17af-159">public HRESULT [put_Language](#put_language)(LPCWSTR value)</span></span>

#### <span data-ttu-id="e17af-160">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="e17af-160">put_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="e17af-161">Establezca el TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="e17af-161">Set the TargetCompatibleBrowserVersion.</span></span>

> <span data-ttu-id="e17af-162">[put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)de HRESULT público (valor de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="e17af-162">public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR value)</span></span>

