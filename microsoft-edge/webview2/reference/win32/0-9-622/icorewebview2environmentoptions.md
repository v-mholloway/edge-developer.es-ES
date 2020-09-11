---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2EnvironmentOptions
ms.openlocfilehash: a4e51dc08e2c31664cb77e4e6ee0136bab2f261d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012759"
---
# <span data-ttu-id="18ed7-104">interfaz ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="18ed7-104">interface ICoreWebView2EnvironmentOptions</span></span> 

```
interface ICoreWebView2EnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="18ed7-105">Opciones usadas para crear un entorno WebView2.</span><span class="sxs-lookup"><span data-stu-id="18ed7-105">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="18ed7-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="18ed7-106">Summary</span></span>

 <span data-ttu-id="18ed7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="18ed7-107">Members</span></span>                        | <span data-ttu-id="18ed7-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="18ed7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="18ed7-109">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="18ed7-109">get_AdditionalBrowserArguments</span></span>](#get_additionalbrowserarguments) | <span data-ttu-id="18ed7-110">AdditionalBrowserArguments se puede especificar para cambiar el comportamiento de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="18ed7-110">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="18ed7-111">get_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="18ed7-111">get_AllowSingleSignOnUsingOSPrimaryAccount</span></span>](#get_allowsinglesignonusingosprimaryaccount) | <span data-ttu-id="18ed7-112">La propiedad AllowSingleSignOnUsingOSPrimaryAccount se usa para habilitar el inicio de sesión único con recursos de Azure Active Directory (AAD) dentro de la vista Web, usando la cuenta de inicio de sesión de Windows y el inicio de sesión único con los sitios web asociados a la cuenta de inicio de sesión de Windows.</span><span class="sxs-lookup"><span data-stu-id="18ed7-112">The AllowSingleSignOnUsingOSPrimaryAccount property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>
[<span data-ttu-id="18ed7-113">get_Language</span><span class="sxs-lookup"><span data-stu-id="18ed7-113">get_Language</span></span>](#get_language) | <span data-ttu-id="18ed7-114">El idioma predeterminado con el que se ejecutará la vista previa.</span><span class="sxs-lookup"><span data-stu-id="18ed7-114">The default language that WebView will run with.</span></span>
[<span data-ttu-id="18ed7-115">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="18ed7-115">get_TargetCompatibleBrowserVersion</span></span>](#get_targetcompatiblebrowserversion) | <span data-ttu-id="18ed7-116">La versión de los binarios de la WebView2 en tiempo de ejecución para que sea compatible con la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="18ed7-116">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="18ed7-117">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="18ed7-117">put_AdditionalBrowserArguments</span></span>](#put_additionalbrowserarguments) | <span data-ttu-id="18ed7-118">Establezca la propiedad AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="18ed7-118">Set the AdditionalBrowserArguments property.</span></span>
[<span data-ttu-id="18ed7-119">put_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="18ed7-119">put_AllowSingleSignOnUsingOSPrimaryAccount</span></span>](#put_allowsinglesignonusingosprimaryaccount) | <span data-ttu-id="18ed7-120">Establezca la propiedad AllowSingleSignOnUsingOSPrimaryAccount.</span><span class="sxs-lookup"><span data-stu-id="18ed7-120">Set the AllowSingleSignOnUsingOSPrimaryAccount property.</span></span>
[<span data-ttu-id="18ed7-121">put_Language</span><span class="sxs-lookup"><span data-stu-id="18ed7-121">put_Language</span></span>](#put_language) | <span data-ttu-id="18ed7-122">Establezca la propiedad de idioma.</span><span class="sxs-lookup"><span data-stu-id="18ed7-122">Set the Language property.</span></span>
[<span data-ttu-id="18ed7-123">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="18ed7-123">put_TargetCompatibleBrowserVersion</span></span>](#put_targetcompatiblebrowserversion) | <span data-ttu-id="18ed7-124">Establezca la propiedad TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="18ed7-124">Set the TargetCompatibleBrowserVersion property.</span></span>

<span data-ttu-id="18ed7-125">Se proporciona una implementación predeterminada en WebView2EnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="18ed7-125">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    CHECK_FAILURE(options->put_AllowSingleSignOnUsingOSPrimaryAccount(
        m_AADSSOEnabled ? TRUE : FALSE));
    if (!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## <span data-ttu-id="18ed7-126">Miembros</span><span class="sxs-lookup"><span data-stu-id="18ed7-126">Members</span></span>

#### <span data-ttu-id="18ed7-127">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="18ed7-127">get_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="18ed7-128">AdditionalBrowserArguments se puede especificar para cambiar el comportamiento de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="18ed7-128">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="18ed7-129">[get_AdditionalBrowserArguments](#get_additionalbrowserarguments)de HRESULT público (valor LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="18ed7-129">public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span></span>

<span data-ttu-id="18ed7-130">Se pasarán al proceso de explorador como parte de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="18ed7-130">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="18ed7-131">Consulte [Ejecutar cromo con marcas](https://aka.ms/RunChromiumWithFlags) para obtener más información acerca de los modificadores de la línea de comandos para el proceso del explorador.</span><span class="sxs-lookup"><span data-stu-id="18ed7-131">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="18ed7-132">Si la aplicación se inicia con un modificador de línea de comandos, `--edge-webview-switches=xxx` el valor de ese modificador (XXX en el ejemplo anterior) también se anexará a la línea de comandos del proceso del explorador.</span><span class="sxs-lookup"><span data-stu-id="18ed7-132">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="18ed7-133">Algunos conmutadores como los `--user-data-dir` de WebView son internos y importantes.</span><span class="sxs-lookup"><span data-stu-id="18ed7-133">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="18ed7-134">Estos conmutadores se ignorarán incluso si se especifican.</span><span class="sxs-lookup"><span data-stu-id="18ed7-134">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="18ed7-135">Si se especifican los mismos modificadores varias veces, se gana la última.</span><span class="sxs-lookup"><span data-stu-id="18ed7-135">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="18ed7-136">No hay ningún intento de combinar los distintos valores del mismo modificador, excepto para las características deshabilitado y habilitado.</span><span class="sxs-lookup"><span data-stu-id="18ed7-136">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="18ed7-137">Las características especificadas por `--enable-features` y se `--disable-features` combinarán con lógica simple: las características serán la Unión de las características especificadas y las características integradas, y si una característica está deshabilitada, se quitará de la lista de características habilitadas.</span><span class="sxs-lookup"><span data-stu-id="18ed7-137">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="18ed7-138">El valor de la línea de comandos del proceso de la aplicación `--edge-webview-switches` se procesa después de que se procese el parámetro additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="18ed7-138">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="18ed7-139">Ciertas características están deshabilitadas internamente y no se pueden habilitar.</span><span class="sxs-lookup"><span data-stu-id="18ed7-139">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="18ed7-140">Si se produjo un error de análisis en los modificadores especificados, se ignorarán.</span><span class="sxs-lookup"><span data-stu-id="18ed7-140">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="18ed7-141">El valor predeterminado es ejecutar el proceso del explorador sin ningún marcador adicional.</span><span class="sxs-lookup"><span data-stu-id="18ed7-141">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="18ed7-142">get_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="18ed7-142">get_AllowSingleSignOnUsingOSPrimaryAccount</span></span> 

<span data-ttu-id="18ed7-143">La propiedad AllowSingleSignOnUsingOSPrimaryAccount se usa para habilitar el inicio de sesión único con recursos de Azure Active Directory (AAD) dentro de la vista Web, usando la cuenta de inicio de sesión de Windows y el inicio de sesión único con los sitios web asociados a la cuenta de inicio de sesión de Windows.</span><span class="sxs-lookup"><span data-stu-id="18ed7-143">The AllowSingleSignOnUsingOSPrimaryAccount property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>

> <span data-ttu-id="18ed7-144">[get_AllowSingleSignOnUsingOSPrimaryAccount](#get_allowsinglesignonusingosprimaryaccount)de HRESULT público (bool \* allow)</span><span class="sxs-lookup"><span data-stu-id="18ed7-144">public HRESULT [get_AllowSingleSignOnUsingOSPrimaryAccount](#get_allowsinglesignonusingosprimaryaccount)(BOOL \* allow)</span></span>

<span data-ttu-id="18ed7-145">El valor predeterminado es deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="18ed7-145">Default is disabled.</span></span> <span data-ttu-id="18ed7-146">Las aplicaciones de la plataforma universal de Windows también deben declarar la [funcionalidad restringida](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) de enterpriseCloudSSO para que funcione el inicio de sesión único.</span><span class="sxs-lookup"><span data-stu-id="18ed7-146">Universal Windows Platform apps must also declare enterpriseCloudSSO [restricted capability](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) for the single sign on to work.</span></span>

#### <span data-ttu-id="18ed7-147">get_Language</span><span class="sxs-lookup"><span data-stu-id="18ed7-147">get_Language</span></span> 

<span data-ttu-id="18ed7-148">El idioma predeterminado con el que se ejecutará la vista previa.</span><span class="sxs-lookup"><span data-stu-id="18ed7-148">The default language that WebView will run with.</span></span>

> <span data-ttu-id="18ed7-149">[get_Language](#get_language)de HRESULT público (valor LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="18ed7-149">public HRESULT [get_Language](#get_language)(LPWSTR \* value)</span></span>

<span data-ttu-id="18ed7-150">Se aplica a ius del explorador, como menús contextuales y cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="18ed7-150">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="18ed7-151">También se aplica al encabezado HTTP Accept-Languages que la vista Web envía a los sitios Web.</span><span class="sxs-lookup"><span data-stu-id="18ed7-151">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="18ed7-152">Está en el formato de `language[-country]` donde `language` es el código de 2 Letras de ISO 639 y `country` es el código de 2 letras de ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="18ed7-152">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="18ed7-153">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="18ed7-153">get_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="18ed7-154">La versión de los binarios de la WebView2 en tiempo de ejecución para que sea compatible con la aplicación de llamada.</span><span class="sxs-lookup"><span data-stu-id="18ed7-154">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="18ed7-155">[get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)de HRESULT público (valor LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="18ed7-155">public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span></span>

<span data-ttu-id="18ed7-156">De forma predeterminada, la versión de tiempo de ejecución de Edge WebView2 que corresponde a la versión del SDK que usa la aplicación.</span><span class="sxs-lookup"><span data-stu-id="18ed7-156">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="18ed7-157">El formato de este valor es el mismo que el formato de la propiedad BrowserVersionString y otros valores de BrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="18ed7-157">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="18ed7-158">Solo se respeta la parte de versión del valor BrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="18ed7-158">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="18ed7-159">El sufijo de canal, si existe, se pasa por alto.</span><span class="sxs-lookup"><span data-stu-id="18ed7-159">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="18ed7-160">La versión de los binarios de tiempo de ejecución de WebView2 que se usó en realidad puede ser diferente de la TargetCompatibleBrowserVersion especificada.</span><span class="sxs-lookup"><span data-stu-id="18ed7-160">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="18ed7-161">Solo se garantiza que son compatibles.</span><span class="sxs-lookup"><span data-stu-id="18ed7-161">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="18ed7-162">Puedes comprobar la versión real en la propiedad BrowserVersionString de la ICoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="18ed7-162">You can check the actual version on the BrowserVersionString property on the ICoreWebView2Environment.</span></span>

#### <span data-ttu-id="18ed7-163">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="18ed7-163">put_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="18ed7-164">Establezca la propiedad AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="18ed7-164">Set the AdditionalBrowserArguments property.</span></span>

> <span data-ttu-id="18ed7-165">[put_AdditionalBrowserArguments](#put_additionalbrowserarguments)de HRESULT público (valor de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="18ed7-165">public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR value)</span></span>

#### <span data-ttu-id="18ed7-166">put_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="18ed7-166">put_AllowSingleSignOnUsingOSPrimaryAccount</span></span> 

<span data-ttu-id="18ed7-167">Establezca la propiedad AllowSingleSignOnUsingOSPrimaryAccount.</span><span class="sxs-lookup"><span data-stu-id="18ed7-167">Set the AllowSingleSignOnUsingOSPrimaryAccount property.</span></span>

> <span data-ttu-id="18ed7-168">[put_AllowSingleSignOnUsingOSPrimaryAccount](#put_allowsinglesignonusingosprimaryaccount)de HRESULT público (bool allow)</span><span class="sxs-lookup"><span data-stu-id="18ed7-168">public HRESULT [put_AllowSingleSignOnUsingOSPrimaryAccount](#put_allowsinglesignonusingosprimaryaccount)(BOOL allow)</span></span>

#### <span data-ttu-id="18ed7-169">put_Language</span><span class="sxs-lookup"><span data-stu-id="18ed7-169">put_Language</span></span> 

<span data-ttu-id="18ed7-170">Establezca la propiedad de idioma.</span><span class="sxs-lookup"><span data-stu-id="18ed7-170">Set the Language property.</span></span>

> <span data-ttu-id="18ed7-171">[put_Language](#put_language)de HRESULT público (valor de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="18ed7-171">public HRESULT [put_Language](#put_language)(LPCWSTR value)</span></span>

#### <span data-ttu-id="18ed7-172">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="18ed7-172">put_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="18ed7-173">Establezca la propiedad TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="18ed7-173">Set the TargetCompatibleBrowserVersion property.</span></span>

> <span data-ttu-id="18ed7-174">[put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)de HRESULT público (valor de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="18ed7-174">public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR value)</span></span>

