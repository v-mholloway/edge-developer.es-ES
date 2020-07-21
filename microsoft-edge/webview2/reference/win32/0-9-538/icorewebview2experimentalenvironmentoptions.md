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
# interfaz ICoreWebView2ExperimentalEnvironmentOptions 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalEnvironmentOptions
  : public IUnknown
```

Opciones experimentales utilizadas para crear un entorno WebView2.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled) | La propiedad IsSingleSignOnUsingOSPrimaryAccountEnabled se usa para habilitar el inicio de sesión único con recursos de Azure Active Directory (AAD) dentro de la vista Web, usando la cuenta de inicio de sesión de Windows y el inicio de sesión único con los sitios web asociados a la cuenta de inicio de sesión de Windows.
[put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled) | Establezca la propiedad IsSingleSignOnUsingOSPrimaryAccountEnabled.

Se proporciona una implementación predeterminada en WebView2ExperimentalEnvironmentOptions. h.

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

## Miembros

#### get_IsSingleSignOnUsingOSPrimaryAccountEnabled 

La propiedad IsSingleSignOnUsingOSPrimaryAccountEnabled se usa para habilitar el inicio de sesión único con recursos de Azure Active Directory (AAD) dentro de la vista Web, usando la cuenta de inicio de sesión de Windows y el inicio de sesión único con los sitios web asociados a la cuenta de inicio de sesión de Windows.

> [get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)de HRESULT público (bool * Enabled)

El valor predeterminado es deshabilitado. Las aplicaciones de la plataforma universal de Windows también deben declarar la [funcionalidad restringida](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) de enterpriseCloudSSO para que funcione el inicio de sesión único.

#### put_IsSingleSignOnUsingOSPrimaryAccountEnabled 

Establezca la propiedad IsSingleSignOnUsingOSPrimaryAccountEnabled.

> [put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)de HRESULT público (bool Enabled)

