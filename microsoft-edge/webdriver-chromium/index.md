---
description: Obtenga información sobre cómo probar su sitio web o aplicación en Microsoft Edge o automatizar el explorador con WebDriver.
title: Usar WebDriver (Chromium) para la automatización de pruebas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desarrollo web, html, css, javascript, programador, webdriver, se sintaxis, pruebas, herramientas, automatización, prueba
ms.openlocfilehash: 295985734d93c5912922be22c0af0c0e33e00a54
ms.sourcegitcommit: 070a60f634908eea0e29e260331f9fc0aa85ee78
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/30/2021
ms.locfileid: "11306251"
---
# Usar WebDriver (Chromium) para la automatización de pruebas  

WebDriver permite a los desarrolladores crear pruebas automatizadas que simulan la interacción del usuario.  Las pruebas y simulaciones de WebDriver difieren de las pruebas unitarias de JavaScript porque WebDriver:  

*   Accede a la funcionalidad y la información que no están disponibles para JavaScript que se ejecuta en exploradores.  
*   Simula eventos de usuario o eventos de nivel de sistema operativo de forma más precisa.  
*   Administra varias ventanas, pestañas y páginas web en una sola sesión de prueba.  
*   Ejecuta varias sesiones de Microsoft Edge en un equipo específico.  
    
En la siguiente sección se describe cómo empezar a usar WebDriver para Microsoft Edge \(Chromium\).  

## Instalar Microsoft Edge (Chromium)  

Asegúrese de instalar [Microsoft Edge (Chromium).][MicrosoftEdge]  Para confirmar que tiene Microsoft Edge \(Chromium\) instalado, vaya a y compruebe que el número de versión sea la `edge://settings/help` versión 75 o posterior.  

## Descargar controlador de Microsoft Edge  

Para comenzar las pruebas de automatización, siga estos pasos para asegurarse de que la versión de WebDriver que instale coincida con la versión del explorador.  

1.  Navegue para `edge://settings/help` obtener la versión de Microsoft Edge.  
    
    :::image type="complex" source="./media/edge-version.png" alt-text="El número de compilación de Microsoft Edge Canary el 14 de enero de 2020":::
       El número de compilación de Microsoft Edge Canary el 14 de enero de 2020
    :::image-end:::  
    
1.  Navegue a la página [de descargas de controladores de Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads] y descargue el controlador que coincida con el número de versión de Microsoft Edge.  
    
    :::image type="complex" source="./media/edge-driver-install.png" alt-text="La sección Descargas de la página Controlador de Microsoft Edge":::
       La sección Descargas de la [página Controlador de Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver]
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge (EdgeHTML), see [Microsoft WebDriver for Microsoft Edge (EdgeHTML)][Webdriver].  
    -->  

## Elegir un enlace de idioma de WebDriver  

El último componente que debes descargar es un controlador de cliente específico del idioma para traducir el código \(Python, Java, C\#, Ruby, JavaScript\) en comandos que el controlador de Microsoft Edge ejecuta en Microsoft Edge \(Chromium\).  

[Descargue el enlace de idioma de WebDriver de su elección.][SeleniumDownloads]  El equipo de Microsoft Edge recomienda [Usar 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] o posterior, porque es compatible con Microsoft Edge \(Chromium\).  Sin embargo, puedes controlar Microsoft Edge \(Chromium\) en todas las versiones anteriores de Se sint, incluida la versión estable actual de Se sint 3.  

> [!IMPORTANT]
> Si anteriormente estaba automatizando o probando Microsoft Edge \(Chromium\) usando y clases, el código de WebDriver no se ejecuta en `ChromeDriver` `ChromeOptions` Microsoft Edge versión 80 o posterior.  Para solucionar este problema, actualice las pruebas para usar la `EdgeOptions` clase y descargue el controlador de Microsoft [Edge.][MicrosoftDeveloperEdgeToolsWebdriver]  

### Usar Se desenlaz 3  

Si ya [usas Seleán 3,][|::ref1::|]es posible que ya tienes pruebas de explorador y quieras agregar cobertura para Microsoft Edge \(Chromium\) sin cambiar la versión de Sende.  Para usar [Seprocesamiento 3][|::ref2::|] para escribir pruebas automatizadas tanto para Microsoft Edge \(EdgeHTML\) como para Microsoft Edge \(Chromium\), instala el paquete [Herramientas de Seprocesamiento][GithubMicrosoftEdgeSeleniumTools] para Microsoft Edge para usar el controlador actualizado.  Las clases y las clases incluidas en las herramientas son totalmente compatibles con `EdgeDriver` `EdgeDriverService` los equivalentes integrados en Se siny 4.  

Siga los pasos siguientes para agregar [las Herramientas de selenio para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] y Se [siny 3][|::ref3::|] al proyecto.  

#### [C#](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

Agregue los [paquetes Microsoft.Edge.Setools y][NugetPackagesMicrosoftEdgeSeleniumtools] [Setools.WebDriver][NugetPackagesSeleniumWebdriver31410] a su proyecto .NET con la CLI de [NuGet][NugetCLI] [o Visual Studio][VisualStudio].  

#### [Python](#tab/python/)  

<a id="selenium-tools-install"></a>  

Usa [pip][PythonPip] para instalar los [paquetes msedge-seprocesamiento-tools][PythonSeleniumTools] y [se siny.][PythonSelenium]  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [Java](#tab/java/)  

<a id="selenium-tools-install"></a>  

Si el Java usa Maven, agrega [msedge-se javascript-tools-java][SonatypeMavenRepositorySearch] haciendo frente a la siguiente dependencia en el `pom.xml` archivo:  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

El Java paquete también está disponible para descargar directamente en la página [Herramientas de disponibilidad para versiones de Microsoft Edge.][GithubMicrosoftEdgeSeleniumToolsReleases]  

#### [JavaScript](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

Use [npm][JavaScript|::ref4::|] para instalar los [paquetes edge-seprocesamiento-tools][JavaScriptSeleniumTools] y [seprocesamiento-webdriver.][JavaScriptSelenium]  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## Automatizar Microsoft Edge (Chromium) con WebDriver  

Para automatizar un explorador con WebDriver, primero debe iniciar una sesión de WebDriver con el enlace de idioma de WebDriver que prefiera.  Una sesión es una única instancia en ejecución de un explorador que se puede controlar mediante comandos de WebDriver.  Al iniciar una sesión de WebDriver se inicia una nueva instancia del explorador.  El explorador que se inicia permanece abierto hasta que cierra la sesión de WebDriver.  

El siguiente contenido le guiará a través del uso de Se a continuación para iniciar una sesión de WebDriver con Microsoft Edge \(Chromium\).  Puede ejecutar estos ejemplos con Se siny 3 o 4.  Para usar con Se desenlaz 3, se debe instalar el paquete [Herramientas de sesón][GithubMicrosoftEdgeSeleniumTools] para Microsoft Edge.  

### Automatización de Microsoft Edge (Chromium)  

Sende usa la `EdgeDriver` clase para administrar una sesión de Microsoft Edge \(Chromium\). Para iniciar una sesión y automatizar Microsoft Edge \(Chromium\), cree un nuevo objeto y pásle un objeto con la `EdgeDriver` `EdgeOptions` propiedad establecida en `UseChromium` `true` .  

#### [C#](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [Python](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [Java](#tab/java/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

La clase solo admite Microsoft Edge (Chromium) y no `EdgeDriver` admite Microsoft Edge (EdgeHTML). Para el uso básico, puede crear una `EdgeDriver` sin proporcionar `EdgeOptions` .  

```java
EdgeDriver driver = new EdgeDriver();
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
> Si el administrador de TI ha establecido la directiva [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] en , El controlador de Microsoft Edge no puede impulsar Microsoft Edge (Chromium) porque el controlador usa las `2` [][MicrosoftDeveloperEdgeToolsWebdriver] [DevTools de Microsoft Edge][DevtoolsIndex].  Asegúrate de [que la directiva DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] esté establecida en o para automatizar `0` Microsoft Edge `1` (Chromium).  

### Elección de binarios de explorador específicos (solo chromium)  

Puede iniciar una sesión de WebDriver con archivos binarios específicos de Microsoft Edge \(Chromium\).  Por ejemplo, puede ejecutar pruebas con los canales de vista previa de [Microsoft Edge,][MicrosoftedgeinsiderDownload] como Microsoft Edge Beta.  

#### [C#](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [Python](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [Java](#tab/java/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [JavaScript](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### Personalización del servicio de controladores de Microsoft Edge  

#### [C#](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Cuando se crea una instancia de clase mediante clase, crea e inicia la clase adecuada para `EdgeDriver` `EdgeOptions` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) o Microsoft Edge \(Chromium\).  

Si quieres crear una, crea una configurada `EdgeDriverService` para Microsoft Edge \(Chromium\) mediante el `CreateChromiumService()` método.  Es posible que le sea útil cuando necesite agregar personalizaciones. Por ejemplo, el siguiente código inicia la salida del registro detallado.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
>No es necesario proporcionar el objeto `EdgeOptions` al pasar a la `EdgeDriverService` `EdgeDriver` instancia.  La clase usa las opciones predeterminadas para `EdgeDriver` Microsoft Edge \(EdgeHTML\) o Microsoft Edge \(Chromium\) en función del servicio que proporciones.  
> Sin embargo, si desea proporcionar ambos y clases, asegúrese de que ambos están configurados `EdgeDriverService` para la misma versión de Microsoft `EdgeOptions` Edge.  Por ejemplo, no es posible usar una clase predeterminada de Microsoft Edge \(EdgeHTML\) y propiedades `EdgeDriverService` chromium en la `EdgeOptions` clase.  La `EdgeDriver` clase produce un error para evitar el uso de diferentes versiones.  

#### [Python](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Al usar Python, `Edge` el objeto crea y administra el archivo `EdgeService` .  Para configurar el `EdgeService` , pase argumentos adicionales al objeto como se indica en el siguiente `Edge` código.  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [Java](#tab/java/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Usa el `createDefaultService()` método para crear una configuración para Microsoft Edge `EdgeDriverService` \(Chromium\). Los servicios de controladores Java se personalizan mediante Java propiedades del sistema. Por ejemplo, el siguiente código usa la `"webdriver.edge.verboseLogging"` propiedad para habilitar la salida del registro detallado.  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [JavaScript](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Al usar JavaScript, cree y configure una `Service` con la `ServiceBuilder` clase.  Opcionalmente, puedes pasar el objeto al objeto, que inicia `Service` `Driver` \(y detiene\) el servicio por ti.  
Para configurar el `Service` método , ejecute otro método en la clase antes de usar el `ServiceBuilder` `build()` método.  A continuación, `service` pase el parámetro como en el `Driver.createSession()` método.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### Usar Chromium-Specific opciones  

Si estableces la propiedad en , puedes usar la clase para tener acceso a las mismas propiedades y métodos específicos de Chromium que se usan al automatizar otros exploradores `UseChromium` `true` `EdgeOptions` chromium. [][WebdriverCapabilitiesEdgeOptions]  

#### [C#](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [Python](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [Java](#tab/java/)  

<a id="using-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
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
> Si la propiedad se establece en , no podrá usar propiedades y métodos para `UseChromium` `true` Microsoft Edge \(EdgeHTML\).  

## Opciones de instalación adicionales de WebDriver  

### Resalte  

Si [usas a Cargoy][Chocolatey] como administrador de paquetes, instala el controlador de Microsoft Edge ejecutando el siguiente comando.  

```console
choco install selenium-chromium-edge-driver
```  

Para obtener más información, consulta [Se chromium Edge Driver en Odbcy][ChocolateyPackagesSeleniumChromiumEdgeDriver].  

### Docker  

Si usa [Docker,][DockerHub]descargue una imagen preconfigurada con Microsoft Edge \(Chromium\) y el controlador [de Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] preinstalados ejecutando el siguiente comando.  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Para obtener más información, vaya al [contenedor msedgedriver en Docker Hub.][DockerHubMsedgedriver]  

## Pasos siguientes

Para obtener más información sobre WebDriver y cómo escribir pruebas automatizadas de WebDriver con Serío, vaya a la documentación [de Se automatri.][SeleniumDocumentation]  

## Contactar al equipo de Microsoft Edge DevTools  

El equipo de Microsoft Edge está deseando escuchar sus comentarios sobre el uso de WebDriver, Se sin embargo y Microsoft Edge.  Para enviar al equipo sus preguntas **** y comentarios, elija el icono Enviar comentarios en las DevTools de Microsoft Edge o envíe un tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="El icono Enviar comentarios en Las DevTools de Microsoft Edge" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   El **icono Enviar comentarios** en Las DevTools de Microsoft Edge  
:::image-end:::  

<!-- links -->  

[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Herramientas de desarrollo de Microsoft Edge (Chromium) | Microsoft Docs"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Funcionalidades y opciones de EdgeOptions | Microsoft Docs"  
<!--[Webdriver]: ../edgehtml/webdriver/index.md "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability - Microsoft Edge - Directivas | Microsoft Docs"  

[Chocolatey]: https://chocolatey.org "| Software Desalbado"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Controlador de borde Se chromium | Resalte"  

[DockerHub]: https://hub.docker.com "Docker Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Docker Hub"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-seprocesamiento-tools | GitHub"  
[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-seprocesamiento-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SehidánHQ/sehidán | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-seprocesamiento-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "se siny-webdriver | npm"  

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "WebDriver | Microsoft Developer"  
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Descargas- WebDriver | Microsoft Developer"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Descargar el nuevo explorador Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet.CommandLine | Galería de NuGet"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.Setools | Galería de NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Se siny.WebDriver 3.141.0 | Galería de NuGet"  
[NugetPackagesSeleniumWebdriver400alpha07]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha07 "Se siny.WebDriver 4.0.0-alpha07 | Galería de NuGet"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-seprocesamiento-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "se siny | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SenioHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "El proyecto de automatización del explorador Se de Se siny:: Documentación para Se a."  
[SeleniumDownloads]: https://selenium.dev/downloads "Descargas | Se sindón"  

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "Sonatype Maven Central Repository Search | com.microsoft.edge:msedge-se javascript-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Explorador sin cabeza | Wikipedia"  
