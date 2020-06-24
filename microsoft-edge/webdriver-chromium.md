---
description: Obtenga información sobre cómo probar su sitio web o aplicación en Microsoft Edge o automatizar el explorador con Webdriver.
title: WebDriver (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador, WebDrive, Selenium, pruebas, herramientas, automatización, prueba
ms.openlocfilehash: c60095373be337307225f28d320cae19174531a7
ms.sourcegitcommit: 1b5dfc5a2c7130b3abc6b4545fcaaae0b0897148
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/23/2020
ms.locfileid: "10757583"
---
# Usar Webdriver (cromo) para automatización de prueba  

Webdriver permite a los desarrolladores crear pruebas automatizadas que simulan la interacción del usuario.  Las pruebas y simuladores de WebDrive se diferencian de las pruebas unitarias de JavaScript por las siguientes razones: 
*   Accede a la funcionalidad y la información que no están disponibles para JavaScript que se ejecuta en exploradores.  
*   Simula eventos de usuario o eventos a nivel de OS de forma más precisa.  
*   Administra las pruebas en varias ventanas, pestañas y páginas web en una sola sesión de prueba.  
*   Ejecuta varias sesiones de Microsoft Edge en un equipo específico.  

En la siguiente sección se describe cómo empezar a usar Webdriver para Microsoft Edge \ (cromo \).  

## Instalar Microsoft Edge (cromo)  

Asegúrate de instalar [Microsoft Edge (cromo)][MicrosoftEdge].  Para confirmar que tiene Microsoft Edge (cromo) instalado, vaya a `edge://settings/help` en el explorador y compruebe que el número de versión es la versión 75 o posterior.  

## Descargar el controlador Microsoft Edge  

Para empezar a automatizar las pruebas, siga estos pasos para asegurarse de que la versión de Webdriver que instale coincide con la versión del explorador.  

1.  Vaya a `edge://settings/help` para obtener la versión de Edge.  
    
    :::image type="complex" source="./media/webdriver-chromium/edge-version.png" alt-text="El número de compilación para Microsoft Edge Canarias el 14 de enero de 2020":::
       Figura 1.  El número de compilación para Microsoft Edge Canarias el 14 de enero de 2020
    :::image-end:::  
    
1.  Vaya a la página de [descargas del controlador de Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads] y descargue el controlador que coincida con el número de versión de Edge.  
    
    :::image type="complex" source="./media/webdriver-chromium/edge-driver-install.png" alt-text="Sección de descargas de la página del controlador de Microsoft Edge":::
       Figura 2.  Sección de descargas de la página del [controlador de Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver]
    :::image-end:::  
    
    > [!NOTE] 
    > Para obtener más información sobre la automatización de prueba con Microsoft Edge (EdgeHTML), vea [Microsoft Webdriver para Microsoft Edge (EdgeHTML)][Webdriver].  

## Elegir un enlace de idioma de controlador  

El último componente que debe descargar es un controlador de cliente específico del idioma para traducir su código \ (Python, Java, C \ #, Ruby, JavaScript \) en comandos el controlador de Microsoft Edge se ejecuta en Microsoft Edge \ (cromo \).  

[Descargue el enlace de idioma de Webdrives que prefiera][SeleniumDownloads].  El equipo de Microsoft Edge recomienda [Selenium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] o posterior, porque es compatible con Microsoft Edge \ (cromo \).  Sin embargo, puedes controlar Microsoft Edge \ (cromo \) en todas las versiones anteriores de Selenium, incluida la versión estable actual de Selenium 3.  

> [!IMPORTANT]
> Si anteriormente estabas automatizando o probando Microsoft Edge \ (cromo \) mediante `ChromeDriver` `ChromeOptions` clases, el código de Webdriver no se ejecuta en Microsoft edge versión 80 o posterior.  Para solucionar este problema, actualiza las pruebas para usar la `EdgeOptions` clase e instalar el [controlador Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver].  

### Usar Selenium 3  

Si ya usas [Selenium 3][|::ref1::|], es posible que tengas pruebas de explorador existentes y quieras agregar cobertura para Microsoft Edge \ (cromo \) sin cambiar tu versión de Selenium.  Para usar [Selenium 3][|::ref2::|] para escribir pruebas automatizadas de Microsoft Edge \ (EdgeHTML \) y Microsoft Edge \ (cromo \), instale el paquete [de herramientas de Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] para usar el controlador actualizado.  Las `EdgeDriver` `EdgeDriverService` clases y incluidas en las herramientas son totalmente compatibles con los equivalentes integrados en Selenium 4.  

Siga estos pasos para agregar las [herramientas de Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] y [Selenium 3][|::ref3::|] al proyecto.

#### [C#](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

Agrega los paquetes [Microsoft. Edge. SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] y [Selenium. Webdriver][NugetPackagesSeleniumWebdriver31410] a tu proyecto de .net mediante la [CLI de NuGet][NugetCLI] o [Visual Studio][VisualStudio].

#### [Fundación](#tab/python/)  

<a id="selenium-tools-install"></a>  

Use [PIP][PythonPip] para instalar el [msedge-Selenium-herramientas][PythonSeleniumTools] y paquetes de [Selenium][PythonSelenium] :

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [JavaScript](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

Use [NPM][JavaScript|::ref4::|] para instalar los paquetes [Edge-Selenium-Tools][JavaScriptSeleniumTools] y [Selenium-Webdriver][JavaScriptSelenium] :

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## Usar Microsoft Edge (cromo) con Webdriver

Puede ejecutar los siguientes ejemplos con Selenium 3 o 4.  Para usar con Selenium 3, el paquete [de herramientas de Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] debe estar instalado.  

### Uso básico  

Para usar con Microsoft Edge \ (EdgeHTML \), simplemente cree una instancia predeterminada de la `EdgeDriver` clase.

#### [C#](#tab/c-sharp/)  

<a id="basic-usage-code"></a>  

```csharp
var driver = new EdgeDriver();
```  

#### [Fundación](#tab/python/)  

<a id="basic-usage-code"></a>  

```python
driver = Edge()
```  

#### [JavaScript](#tab/javascript/)  

<a id="basic-usage-code"></a>  

```javascript
let driver = edge.Driver.createSession();
```  

* * *  

### Conduciendo Microsoft Edge (cromo)  

Para usar con Microsoft Edge \ (cromo \), cree una `EdgeDriver` clase nueva y pásele el `EdgeOptions` objeto con la `UseChromium` propiedad establecida en `true` .  

#### [C#](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [Fundación](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [JavaScript](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> Si la directiva [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] se establece en `2` , el [controlador Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] no podrá conducir a [Microsoft Edge (cromo)][MicrosoftEdge] porque el controlador usa la DevTools de [Microsoft Edge][DevToolsMain].  Asegúrate de establecer la [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] política de DeveloperToolsAvailability `0` o `1` para automatizar [Microsoft Edge (cromo)][MicrosoftEdge].  

### Elección de archivos binarios de explorador específicos (solo cromo)  

Puede usar la `EdgeOptions` clase con binarios específicos de Microsoft Edge (cromo).  Por ejemplo, puede ejecutar pruebas usando los [canales de Microsoft Edge Preview][MicrosoftedgeinsiderDownload] , como Microsoft Edge beta.  

#### [C#](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [Fundación](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [JavaScript](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### Personalizar el servicio del controlador Microsoft Edge  

#### [C#](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Cuando `EdgeDriver` se crea una instancia de clase con `EdgeOptions` Class, se crea e inicia la `EdgeDriverService` clase adecuada para Microsoft Edge \ (EdgeHTML \) o Microsoft Edge \ (cromo \).  

Si desea crear un `EdgeDriverService` , cree uno configurado para Microsoft Edge \ (cromo \) con el `CreateChromiumService()` método.  Es posible que le resulte útil para personalizaciones adicionales, como habilitar la salida de registro detallado en el siguiente código.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
>No es necesario proporcionar el `EdgeOptions` objeto cuando se pasa `EdgeDriverService` a la `EdgeDriver` instancia. La `EdgeDriver` clase usa las opciones predeterminadas para Microsoft Edge \ (EdgeHTML \) o Microsoft Edge \ (cromo \) según el servicio que proporcionaste.  
> Sin embargo, si desea proporcionar ambos `EdgeDriverService` y `EdgeOptions` clases, asegúrese de que ambos están configurados para la misma versión de Microsoft Edge.  Por ejemplo, no es posible usar una clase predeterminada de Microsoft Edge (EdgeHTML) `EdgeDriverService` y propiedades de cromo en la `EdgeOptions` clase.  La `EdgeDriver` clase produce un error para evitar el uso de versiones diferentes.  

#### [Fundación](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Al usar Python, el `Edge` objeto crea y administra el `EdgeService` .  Para configurar el `EdgeService` , pase argumentos adicionales al `Edge` objeto, tal y como se indica en el siguiente código.  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [JavaScript](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Al usar JavaScript, cree y configure una `Service` con la `ServiceBuilder` clase.  De manera opcional, puede pasar el `Service` objeto al `Driver` objeto que inicia y detiene el servicio por usted.  
Para configurar el `Service` , ejecute métodos adicionales en la `ServiceBuilder` clase antes de usar el `build()` método.  Después, pasa el `service` as como un parámetro en el `Driver.createSession()` método.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * * 

### Usar opciones específicas de cromo  

Si establece la `UseChromium` propiedad en `true` , puede usar la `EdgeOptions` clase para obtener acceso a las mismas [propiedades y métodos específicos del cromo][SeleniumWebDriverChromeoptionsClass] que cuando automatiza otros exploradores de cromo.  

#### [C#](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [Fundación](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [JavaScript](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```

* * *  
> [!NOTE]
> Si la `UseChromium` propiedad se establece en `true` , no podrá usar propiedades y métodos para Microsoft Edge \ (EdgeHTML \).  

## Opciones adicionales de instalación de Webdriver  

### Chocolate  

Si usas [chocolate][Chocolatey] como el administrador de paquetes, instala el controlador Microsoft Edge ejecutando el siguiente comando.  

```console
choco install selenium-chromium-edge-driver
```  

Para obtener más información, consulta el [controlador de Selenium de cromo en chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].  

### Docker  

Si usas el [acoplador][DockerHub], descarga una imagen preconfigurada con Microsoft Edge \ (cromo \) y el [controlador de Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] preinstalado ejecutando el siguiente comando.  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Para obtener más información, consulte [contenedor en el concentrador de acoplamiento][DockerHubMsedgedriver].  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

El equipo de Microsoft Edge está ansioso por escuchar tus comentarios sobre el uso de Webdriver, Selenium y Microsoft Edge.  Use el icono de **comentarios** en las [@EdgeDevTools][TwitterTweetEdgeDevTools] de Microsoft Edge DevTools o Tweet para que el equipo sepa lo que piensa.  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="El icono de comentarios en el DevTools de Microsoft Edge":::
   El icono de **comentarios** en el DevTools de Microsoft Edge  
:::image-end:::  

<!-- image links -->  

<!-- links -->  

[DevToolsMain]: ./devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"
[Webdriver]: ./webdriver.md "Webdriver (EdgeHTML) | Microsoft docs"  

[DeployedgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability-Microsoft Edge-Policies | Microsoft docs"  

[Chocolatey]: https://chocolatey.org "Chocolate | Software de chocolate"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Controlador de borde de cromo de Selenium | Chocolate"  

[DockerHub]: https://hub.docker.com "Concentrador de acoplamiento"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Concentrador de acoplamiento"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "Microsoft/Edge-Selenium-Tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/Selenium | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "NPM"
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/Edge-Selenium-Tools | NPM"
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "Selenium-Webdriver | NPM"

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "Controlador WebDrive | Microsoft Developer"
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Descargas: Webdriver | Microsoft Developer"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Descargar nuevo explorador Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar los canales de Insider de Microsoft Edge"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet. CommandLine | Galería de NuGet"
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft. Edge. SeleniumTools | Galería de NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium. WebDrive 3.141.0 | Galería de NuGet"  
[NugetPackagesSeleniumWebdriver400alpha05]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha05 "Selenium. WebDrive 4.0.0-alpha05 | Galería de NuGet"  

[PythonPip]: https://pypi.org/project/pip/ "PIP | PyPI"
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-Selenium-herramientas | PyPI"
[PythonSelenium]: https://pypi.org/project/selenium/ "Selenium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDownloads]: https://selenium.dev/downloads "Descargas | Selenium"  
[SeleniumWebDriverChromeoptionsClass]: https://www.selenium.dev/selenium/docs/api/dotnet/?topic=html/T_OpenQA_Selenium_Chrome_ChromeOptions.htm "Clase ChromeOptions: Webdriver | Selenium"  

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"

[W3CWebdriver]: https://w3.org/TR/webdriver2 "Controlador WebDrive"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Explorador sin periféricos | Wikipedia"  
