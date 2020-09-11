---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalEnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalEnvironmentOptions
ms.openlocfilehash: ba91056fa6d2e6cf9e7da18202fb3c74d7deb827
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010246"
---
# <span data-ttu-id="0d6cc-104">0.9.579: ICoreWebView2ExperimentalEnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="0d6cc-104">0.9.579 - interface ICoreWebView2ExperimentalEnvironmentOptions</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalEnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="0d6cc-105">Opciones experimentales utilizadas para crear un entorno WebView2.</span><span class="sxs-lookup"><span data-stu-id="0d6cc-105">Experimental options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="0d6cc-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="0d6cc-106">Summary</span></span>

 <span data-ttu-id="0d6cc-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0d6cc-107">Members</span></span>                        | <span data-ttu-id="0d6cc-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="0d6cc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0d6cc-109">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="0d6cc-109">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span>](#get_issinglesignonusingosprimaryaccountenabled) | <span data-ttu-id="0d6cc-110">La propiedad IsSingleSignOnUsingOSPrimaryAccountEnabled se usa para habilitar el inicio de sesión único con recursos de Azure Active Directory (AAD) dentro de la vista Web, usando la cuenta de inicio de sesión de Windows y el inicio de sesión único con los sitios web asociados a la cuenta de inicio de sesión de Windows.</span><span class="sxs-lookup"><span data-stu-id="0d6cc-110">The IsSingleSignOnUsingOSPrimaryAccountEnabled property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>
[<span data-ttu-id="0d6cc-111">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="0d6cc-111">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span>](#put_issinglesignonusingosprimaryaccountenabled) | <span data-ttu-id="0d6cc-112">Establezca la propiedad IsSingleSignOnUsingOSPrimaryAccountEnabled.</span><span class="sxs-lookup"><span data-stu-id="0d6cc-112">Set the IsSingleSignOnUsingOSPrimaryAccountEnabled property.</span></span>

<span data-ttu-id="0d6cc-113">Se proporciona una implementación predeterminada en WebView2ExperimentalEnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="0d6cc-113">A default implementation is provided in WebView2ExperimentalEnvironmentOptions.h.</span></span>

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2ExperimentalEnvironmentOptions>();
    CHECK_FAILURE(options->put_IsSingleSignOnUsingOSPrimaryAccountEnabled(
        m_AADSSOEnabled ? TRUE : FALSE));
    if (!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## <span data-ttu-id="0d6cc-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="0d6cc-114">Members</span></span>

#### <span data-ttu-id="0d6cc-115">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="0d6cc-115">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span> 

<span data-ttu-id="0d6cc-116">La propiedad IsSingleSignOnUsingOSPrimaryAccountEnabled se usa para habilitar el inicio de sesión único con recursos de Azure Active Directory (AAD) dentro de la vista Web, usando la cuenta de inicio de sesión de Windows y el inicio de sesión único con los sitios web asociados a la cuenta de inicio de sesión de Windows.</span><span class="sxs-lookup"><span data-stu-id="0d6cc-116">The IsSingleSignOnUsingOSPrimaryAccountEnabled property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>

> <span data-ttu-id="0d6cc-117">[get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="0d6cc-117">public HRESULT [get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="0d6cc-118">El valor predeterminado es deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="0d6cc-118">Default is disabled.</span></span> <span data-ttu-id="0d6cc-119">Las aplicaciones de la plataforma universal de Windows también deben declarar la [funcionalidad restringida](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) de enterpriseCloudSSO para que funcione el inicio de sesión único.</span><span class="sxs-lookup"><span data-stu-id="0d6cc-119">Universal Windows Platform apps must also declare enterpriseCloudSSO [restricted capability](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) for the single sign on to work.</span></span>

#### <span data-ttu-id="0d6cc-120">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="0d6cc-120">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span> 

<span data-ttu-id="0d6cc-121">Establezca la propiedad IsSingleSignOnUsingOSPrimaryAccountEnabled.</span><span class="sxs-lookup"><span data-stu-id="0d6cc-121">Set the IsSingleSignOnUsingOSPrimaryAccountEnabled property.</span></span>

> <span data-ttu-id="0d6cc-122">[put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="0d6cc-122">public HRESULT [put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)(BOOL enabled)</span></span>

