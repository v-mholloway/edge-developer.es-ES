---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions
ms.openlocfilehash: 705e030caba03227749002bad8c9777197839a28
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885565"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

Opciones usadas para crear un entorno WebView2.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[AdditionalBrowserArguments](#additionalbrowserarguments) | AdditionalBrowserArguments se puede especificar para cambiar el comportamiento de la vista en WebView.
[IsSingleSignOnUsingOSPrimaryAccountEnabled](#issinglesignonusingosprimaryaccountenabled) | La propiedad IsSingleSignOnUsingOSPrimaryAccountEnabled se usa para habilitar el inicio de sesión único con recursos de Azure Active Directory (AAD) dentro de la vista Web, usando la cuenta de inicio de sesión de Windows y el inicio de sesión único con los sitios web asociados a la cuenta de inicio de sesión de Windows.
[Idioma](#language) | El idioma predeterminado con el que se ejecutará la vista previa.
[TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion) | La versión de los binarios de la WebView2 en tiempo de ejecución para que sea compatible con la aplicación de llamada.
[CoreWebView2EnvironmentOptions](#corewebview2environmentoptions) | Inicializa una nueva instancia de la clase CoreWebView2EnvironmentOptions.

Se proporciona una implementación predeterminada en WebView2EnvironmentOptions. h.

## Miembros

#### AdditionalBrowserArguments 

AdditionalBrowserArguments se puede especificar para cambiar el comportamiento de la vista en WebView.

> cadena pública [AdditionalBrowserArguments](#additionalbrowserarguments)

Se pasarán al proceso de explorador como parte de la línea de comandos. Consulte [Ejecutar cromo con marcas](https://aka.ms/RunChromiumWithFlags) para obtener más información acerca de los modificadores de la línea de comandos para el proceso del explorador. Si la aplicación se inicia con un modificador de línea de comandos, `--edge-webview-switches=xxx` el valor de ese modificador (XXX en el ejemplo anterior) también se anexará a la línea de comandos del proceso del explorador. Algunos conmutadores como los `--user-data-dir` de WebView son internos y importantes. Estos conmutadores se ignorarán incluso si se especifican. Si se especifican los mismos modificadores varias veces, se gana la última. No hay ningún intento de combinar los distintos valores del mismo modificador, excepto para las características deshabilitado y habilitado. Las características especificadas por `--enable-features` y se `--disable-features` combinarán con lógica simple: las características serán la Unión de las características especificadas y las características integradas, y si una característica está deshabilitada, se quitará de la lista de características habilitadas. El valor de la línea de comandos del proceso de la aplicación `--edge-webview-switches` se procesa después de que se procese el parámetro additionalBrowserArguments. Ciertas características están deshabilitadas internamente y no se pueden habilitar. Si se produjo un error de análisis en los modificadores especificados, se ignorarán. El valor predeterminado es ejecutar el proceso del explorador sin ningún marcador adicional.

#### IsSingleSignOnUsingOSPrimaryAccountEnabled 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

La propiedad IsSingleSignOnUsingOSPrimaryAccountEnabled se usa para habilitar el inicio de sesión único con recursos de Azure Active Directory (AAD) dentro de la vista Web, usando la cuenta de inicio de sesión de Windows y el inicio de sesión único con los sitios web asociados a la cuenta de inicio de sesión de Windows.

> Public bool [IsSingleSignOnUsingOSPrimaryAccountEnabled](#issinglesignonusingosprimaryaccountenabled)

El valor predeterminado es deshabilitado. Las aplicaciones de la plataforma universal de Windows también deben declarar la [funcionalidad restringida](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) de enterpriseCloudSSO para que funcione el inicio de sesión único.

#### Idioma 

El idioma predeterminado con el que se ejecutará la vista previa.

> [lenguaje](#language) de cadenas pública

Se aplica a ius del explorador, como menús contextuales y cuadros de diálogo. También se aplica al encabezado HTTP Accept-Languages que la vista Web envía a los sitios Web. Está en el formato de `language[-country]` donde `language` es el código de 2 Letras de ISO 639 y `country` es el código de 2 letras de ISO 3166.

#### TargetCompatibleBrowserVersion 

La versión de los binarios de la WebView2 en tiempo de ejecución para que sea compatible con la aplicación de llamada.

> cadena pública [TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion)

De forma predeterminada, la versión de tiempo de ejecución de Edge WebView2 que corresponde a la versión del SDK que usa la aplicación. El formato de este valor es el mismo que el formato de la propiedad BrowserVersionString y otros valores de BrowserVersion. Solo se respeta la parte de versión del valor BrowserVersion. El sufijo de canal, si existe, se pasa por alto. La versión de los binarios de tiempo de ejecución de WebView2 que se usó en realidad puede ser diferente de la TargetCompatibleBrowserVersion especificada. Solo se garantiza que son compatibles. Puedes comprobar la versión real en la propiedad BrowserVersionString de la CoreWebView2Environment.

#### CoreWebView2EnvironmentOptions 

Inicializa una nueva instancia de la clase CoreWebView2EnvironmentOptions.

> Public [CoreWebView2EnvironmentOptions](#corewebview2environmentoptions)(String additionalBrowserArguments, lenguaje de cadenas, String targetCompatibleBrowserVersion)

##### Parameters
* `additionalBrowserArguments` AdditionalBrowserArguments se puede especificar para cambiar el comportamiento de la vista en WebView. 

* `language` El idioma predeterminado con el que se ejecutará la vista previa. 

* `targetCompatibleBrowserVersion` La versión de los binarios de la WebView2 en tiempo de ejecución para que sea compatible con la aplicación de llamada.

