---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalEnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalEnvironmentOptions
ms.openlocfilehash: 3e18c15e23338404720dae917cb6d009c41c3c04
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886577"
---
# <span data-ttu-id="dad95-104">interfaz ICoreWebView2ExperimentalEnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="dad95-104">interface ICoreWebView2ExperimentalEnvironmentOptions</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalEnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="dad95-105">Opciones experimentales utilizadas para crear un entorno WebView2.</span><span class="sxs-lookup"><span data-stu-id="dad95-105">Experimental options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="dad95-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="dad95-106">Summary</span></span>

 <span data-ttu-id="dad95-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="dad95-107">Members</span></span>                        | <span data-ttu-id="dad95-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="dad95-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dad95-109">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="dad95-109">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span>](#get_issinglesignonusingosprimaryaccountenabled) | <span data-ttu-id="dad95-110">La propiedad IsSingleSignOnUsingOSPrimaryAccountEnabled se usa para habilitar el inicio de sesión único con recursos de Azure Active Directory (AAD) dentro de la vista Web, usando la cuenta de inicio de sesión de Windows y el inicio de sesión único con los sitios web asociados a la cuenta de inicio de sesión de Windows.</span><span class="sxs-lookup"><span data-stu-id="dad95-110">The IsSingleSignOnUsingOSPrimaryAccountEnabled property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>
[<span data-ttu-id="dad95-111">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="dad95-111">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span>](#put_issinglesignonusingosprimaryaccountenabled) | <span data-ttu-id="dad95-112">Establezca la propiedad IsSingleSignOnUsingOSPrimaryAccountEnabled.</span><span class="sxs-lookup"><span data-stu-id="dad95-112">Set the IsSingleSignOnUsingOSPrimaryAccountEnabled property.</span></span>

<span data-ttu-id="dad95-113">Se proporciona una implementación predeterminada en WebView2ExperimentalEnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="dad95-113">A default implementation is provided in WebView2ExperimentalEnvironmentOptions.h.</span></span>

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

## <span data-ttu-id="dad95-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="dad95-114">Members</span></span>

#### <span data-ttu-id="dad95-115">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="dad95-115">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span> 

<span data-ttu-id="dad95-116">La propiedad IsSingleSignOnUsingOSPrimaryAccountEnabled se usa para habilitar el inicio de sesión único con recursos de Azure Active Directory (AAD) dentro de la vista Web, usando la cuenta de inicio de sesión de Windows y el inicio de sesión único con los sitios web asociados a la cuenta de inicio de sesión de Windows.</span><span class="sxs-lookup"><span data-stu-id="dad95-116">The IsSingleSignOnUsingOSPrimaryAccountEnabled property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>

> <span data-ttu-id="dad95-117">[get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="dad95-117">public HRESULT [get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="dad95-118">El valor predeterminado es deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="dad95-118">Default is disabled.</span></span> <span data-ttu-id="dad95-119">Las aplicaciones de la plataforma universal de Windows también deben declarar la [funcionalidad restringida](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) de enterpriseCloudSSO para que funcione el inicio de sesión único.</span><span class="sxs-lookup"><span data-stu-id="dad95-119">Universal Windows Platform apps must also declare enterpriseCloudSSO [restricted capability](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) for the single sign on to work.</span></span>

#### <span data-ttu-id="dad95-120">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="dad95-120">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span> 

<span data-ttu-id="dad95-121">Establezca la propiedad IsSingleSignOnUsingOSPrimaryAccountEnabled.</span><span class="sxs-lookup"><span data-stu-id="dad95-121">Set the IsSingleSignOnUsingOSPrimaryAccountEnabled property.</span></span>

> <span data-ttu-id="dad95-122">[put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="dad95-122">public HRESULT [put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)(BOOL enabled)</span></span>
