---
description: Aprende a probar tu sitio web o aplicación en Microsoft Edge o automatizar el explorador con WebDriver
title: Usar WebDriver (Chromium) para la automatización de pruebas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/24/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desarrollo web, html, css, javascript, programador, webdriver, selenio, pruebas, herramientas, automatización, prueba
ms.openlocfilehash: a1ec308fc1412ead27c4776ce0ccc2e873376652
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624678"
---
# <a name="use-webdriver-chromium-for-test-automation"></a>Usar WebDriver (Chromium) para la automatización de pruebas  

WebDriver permite a los desarrolladores crear pruebas automatizadas que simulan la interacción del usuario.  Las pruebas y simulaciones de WebDriver difieren de las pruebas unitarias de JavaScript de las siguientes maneras.  

*   Tiene acceso a la funcionalidad y la información que no están disponibles para JavaScript que se ejecuta en exploradores.  
*   Simula eventos de usuario o eventos de nivel de sistema operativo con mayor precisión.  
*   Administra varias ventanas, pestañas y páginas web en una sola sesión de prueba.  
*   Ejecuta varias sesiones de Microsoft Edge en un equipo específico.  


## <a name="relationship-between-webdriver-and-other-software"></a>Relación entre WebDriver y otro software

Para automatizar Microsoft Edge webDriver para simular la interacción del usuario, necesita tres componentes:

*  Microsoft Edge
*  Microsoft Edge Driver
*  Un marco de pruebas de WebDriver

La relación funcional entre estos componentes es la siguiente.

| Tecnología | Rol |
|---|---|
| WebDriver | Un estándar W3C para un protocolo de cable de plataforma e idioma neutro.  Este protocolo permite que los programas fuera de proceso indiquen de forma remota el comportamiento de los exploradores web. |
| Microsoft Edge Driver | Implementación de Microsoft del protocolo WebDriver específicamente para Microsoft Edge.  Los autores de pruebas escriben pruebas que usan comandos de WebDriver que Microsoft Edge driver recibe.  Microsoft Edge A continuación, el controlador es responsable de comunicar ese comando al explorador. |
| Un marco de pruebas de WebDriver | Los autores de pruebas usan un marco de pruebas para escribir pruebas de extremo a extremo y automatizar exploradores.  Proporciona una interfaz específica del idioma que traduce el código en comandos que Microsoft Edge Driver se ejecuta en Microsoft Edge \(Chromium\).  Los marcos de prueba de WebDriver existen para todas las plataformas e idiomas principales.  Uno de estos marcos es Selenio. |
| Controlador de Internet Explorer | Una implementación del protocolo WebDriver específicamente para Internet Explorer.  Para ejecutar pruebas de un extremo a otro heredadas para Internet Explorer, se recomienda usar el controlador de Internet Explorer. |

En las secciones siguientes se describe cómo empezar a usar WebDriver para Microsoft Edge \(Chromium\).  


## <a name="install-microsoft-edge-chromium"></a>Instalar Microsoft Edge (Chromium)  

Asegúrese de instalar [Microsoft Edge (Chromium).][MicrosoftEdge]  Para confirmar que tiene Microsoft Edge \(Chromium\) instalado, vaya a y compruebe que el número de versión es `edge://settings/help` 75 o posterior.


## <a name="download-microsoft-edge-driver"></a>Descargar Microsoft Edge Driver

Para empezar a automatizar las pruebas, siga estos pasos para asegurarse de que la versión de WebDriver que instale coincida con la versión del explorador.  

1.  Busque la versión de Microsoft Edge.  
    1.  Vaya a `edge://settings/help`.  
        
        :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="El número de compilación Microsoft Edge el 15 de abril de 2021" lightbox="./media/microsoft-edge-version.msft.png":::
           El número de compilación Microsoft Edge el 15 de abril de 2021  
        :::image-end:::  
        
1.  Vaya a [Microsoft Edge controlador][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].  
1.  Vaya a **Obtener la versión más reciente**.  
1.  Elija la compilación del canal que coincida con el número de versión de Microsoft Edge.  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="La sección Obtener la versión más reciente en la página Microsoft Edge driver" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       La **sección Obtener la versión más** reciente en la página web Microsoft Edge [driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  
    :::image-end:::  
   
    
## <a name="choose-a-webdriver-testing-framework"></a>Elegir un marco de pruebas de WebDriver

Después de descargar Microsoft Edge driver, el último componente que debe descargar es un marco de pruebas de WebDriver. Los autores de pruebas usan marcos de prueba de WebDriver para escribir pruebas de un extremo a otro y automatizar exploradores. El marco proporciona una interfaz específica del idioma que convierte el código (como Python, Java, C#, Ruby o JavaScript) en comandos que Microsoft Edge Driver se ejecuta en Microsoft Edge \(Chromium\). Los marcos de prueba de WebDriver existen para todas las plataformas e idiomas principales.


En este artículo se proporcionan instrucciones para usar el marco selenio, pero puede usar cualquier biblioteca, marco y lenguaje de programación compatible con WebDriver.  Para realizar las mismas tareas con un marco de pruebas de WebDriver distinto de Selenio, consulte la documentación oficial para su marco de elección.

Si usa Selenio, el equipo de Microsoft Edge recomienda [Selenio 4.0.0-beta2][NugetPackagesSeleniumWebdriver400beta02] o posterior, ya que esa versión de Selenio admite Microsoft Edge \(Chromium\).  Sin embargo, puede controlar Microsoft Edge \(Chromium\) en todas las versiones anteriores de Selenio, incluida la versión estable actual de Selenio 3.  

> [!IMPORTANT]
> Si ha automatizado o probado anteriormente Microsoft Edge \(Chromium\) mediante y clases, el código de WebDriver no se ejecuta en `ChromeDriver` `ChromeOptions` Microsoft Edge versión 80 o posterior.  Para solucionar el problema, actualice las pruebas para usar la `EdgeOptions` clase y descargue Microsoft Edge [driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].  

### <a name="using-selenium-4"></a>Uso de Selenio 4

El marco de pruebas de Selenium WebDriver se puede usar en cualquier plataforma y está disponible para Java, Python, C#, Ruby y JavaScript.

Selenium 4 tiene compatibilidad integrada con Microsoft Edge (Chromium).  Para instalar Selenio 4, vaya a [Instalación de bibliotecas de Selenio][SeleniumInstallingLibraries].

Si usa Selenio 4, no necesita usar Herramientas de Selenio para Microsoft Edge.  Las herramientas de selenio Microsoft Edge son solo para Selenium 3.  Si intenta usar Selenium 4 con Selenium Tools para Microsoft Edge e intenta crear una nueva instancia, se `EdgeDriver` produce el siguiente error: `System.MissingMethodException: 'Method not found: 'OpenQA.Selenium.Remote.DesiredCapabilities OpenQA.Selenium.DriverOptions.GenerateDesiredCapabilities(Boolean)'` .  

Si usa Selenio 4 y obtiene este error, quite del proyecto y asegúrese de que está usando el oficial y las clases del `Microsoft.Edge.SeleniumTools` `EdgeOptions` espacio de `EdgeDriver` `OpenQA.Selenium.Edge` nombres.

### <a name="using-selenium-3"></a>Uso de Selenio 3  

Si ya usa [Selenio 3,][|::ref1::|]es posible que tenga pruebas de explorador existentes y desee agregar cobertura para Microsoft Edge \(Chromium\) sin cambiar su versión de Selenio.  Para usar [Selenio 3][|::ref2::|] para escribir pruebas automatizadas para Microsoft Edge \(EdgeHTML\) y Microsoft Edge \(Chromium\), instale el paquete [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] para usar el controlador actualizado.  Las clases y incluidas en las herramientas son totalmente compatibles con `EdgeDriver` `EdgeDriverService` los equivalentes integrados en Selenio 4.  

Si usa Selenio 3, siga estos pasos para agregar las Herramientas de [Selenio para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] y [Selenio 3][|::ref3::|] al proyecto.

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

Agregue los [paquetes Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] y [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] al proyecto de [.NuGet][NugetCLI] NET con la CLI o Visual Studio [.][VisualStudio]  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="selenium-tools-install"></a>  

Use [pip][PythonPip] para instalar los [paquetes msedge-selenium-tools][PythonSeleniumTools] y [selenio.][PythonSelenium]  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="selenium-tools-install"></a>  

Si el Java usa Maven, copie y pegue la siguiente dependencia en el archivo para `pom.xml` agregar [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

El Java también está disponible para descargar directamente en la página [Herramientas de selenio para Microsoft Edge versiones.][GithubMicrosoftEdgeSeleniumToolsReleases]  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

Use [npm][JavaScript|::ref4::|] para instalar los paquetes [edge-selenium-tools][JavaScriptSeleniumTools] y [selenium-webdriver.][JavaScriptSelenium]  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  


## <a name="automate-microsoft-edge-chromium-with-webdriver"></a>Automatizar Microsoft Edge (Chromium) con WebDriver  

Para automatizar un explorador con WebDriver, primero debe iniciar una sesión de WebDriver con el marco de prueba de WebDriver preferido.  Una sesión es una única instancia en ejecución de un explorador controlado mediante comandos de WebDriver.  Inicie una sesión de WebDriver para iniciar una nueva instancia del explorador.  La instancia del explorador iniciada permanece abierta hasta que cierre la sesión de WebDriver.  

El siguiente contenido le guiará a través del uso de Selenium para iniciar una sesión de WebDriver con Microsoft Edge \(Chromium\).  Puede ejecutar estos ejemplos con Selenio 3 o 4.  Para usar WebDriver con Selenium 3, se debe instalar el paquete [selenio Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package.  

> [!NOTE]
> En este artículo se proporcionan instrucciones para usar el marco selenio, pero puede usar cualquier biblioteca, marco y lenguaje de programación compatible con WebDriver.  Para realizar las mismas tareas con otro marco, consulte la documentación oficial para su marco de elección.

### <a name="automate-microsoft-edge-chromium"></a>Automatizar Microsoft Edge (Chromium)  

Selenio usa la `EdgeDriver` clase para administrar una sesión Microsoft Edge \(Chromium\).  Para iniciar una sesión y automatizar Microsoft Edge \(Chromium\), cree un nuevo objeto y pásalo un objeto con la propiedad `EdgeDriver` `EdgeOptions` establecida en `UseChromium` `true` .  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options = options)
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

La clase solo admite Microsoft Edge \(Chromium\) y no admite `EdgeDriver` Microsoft Edge \(EdgeHTML\).  Para el uso básico, puede crear un `EdgeDriver` sin proporcionar `EdgeOptions` .  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> Si el administrador de TI ha establecido la directiva [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] en , el controlador de Microsoft Edge no puede conducir `2` Microsoft Edge \(Chromium\), ya que el controlador usa [Microsoft Edge DevTools][DevtoolsIndex]. [][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  Asegúrese de [que la directiva DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] está establecida en o para automatizar Microsoft Edge `0` `1` (Chromium).  

### <a name="choose-specific-browser-binaries-chromium-only"></a>Elegir archivos binarios de explorador específicos (solo Chromium explorador)  

Puede iniciar una sesión de WebDriver con archivos binarios Microsoft Edge \(Chromium\).  Por ejemplo, puede ejecutar pruebas con los canales [Microsoft Edge vista previa,][MicrosoftedgeinsiderDownload] como Microsoft Edge Beta.  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options = options)
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <a name="customize-the-microsoft-edge-driver-service"></a>Personalizar el servicio Microsoft Edge controladores  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Cuando se usa la clase para crear una instancia de clase, se crea e inicia la clase adecuada para `EdgeOptions` `EdgeDriver` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) o Microsoft Edge \(Chromium\).  

Si desea crear un , use el método para crear uno configurado para `EdgeDriverService` `CreateChromiumService()` Microsoft Edge \(Chromium\).  El `CreateChromiumService()` método es útil cuando necesita agregar personalizaciones.  Por ejemplo, el siguiente código inicia una salida de registro detallada.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
>No es necesario proporcionar el objeto `EdgeOptions` al pasar a la `EdgeDriverService` `EdgeDriver` instancia.  La clase usa las opciones predeterminadas para `EdgeDriver` Microsoft Edge \(EdgeHTML\) o Microsoft Edge \(Chromium\) en función del servicio que proporcione.  
> Sin embargo, si desea proporcionar ambos y clases, asegúrese de que ambos están `EdgeDriverService` `EdgeOptions` configurados para la misma versión de Microsoft Edge.  Por ejemplo, puede usar una clase Microsoft Edge \(EdgeHTML\) predeterminada y Chromium `EdgeDriverService` propiedades de la `EdgeOptions` clase.  La `EdgeDriver` clase genera un error para evitar el uso de versiones diferentes.  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Cuando se usa Python, `Edge` el objeto crea y administra el archivo `EdgeService` .  Para configurar `EdgeService` el argumento , pase argumentos adicionales al objeto como se indica en el código `Edge` siguiente.  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Use el `createDefaultService()` método para crear una configuración para Microsoft Edge `EdgeDriverService` \(Chromium\).  Use Java del sistema para personalizar los servicios de controladores en Java.  Por ejemplo, el siguiente código usa la `"webdriver.edge.verboseLogging"` propiedad para activar la salida de registro detallado.  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Cuando use JavaScript, cree y configure una `Service` con la `ServiceBuilder` clase.  Opcionalmente, puede pasar el objeto al objeto, que inicia `Service` `Driver` \(y detiene\) el servicio por usted.  
Para configurar `Service` el método , ejecute otro método en la clase antes de usar el `ServiceBuilder` `build()` método.  A continuación, `service` pase el parámetro as a en el `Driver.createSession()` método.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <a name="use-chromium-specific-options"></a>Usar Chromium-Specific opciones  

Si establece la propiedad en , puede usar la clase para tener acceso a las mismas propiedades y métodos específicos de Chromium que se usan al automatizar otros exploradores Chromium `UseChromium` `true` `EdgeOptions` web. [][WebdriverCapabilitiesEdgeOptions]  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> Si la propiedad está establecida en , no puede usar propiedades y métodos `UseChromium` `true` para Microsoft Edge \(EdgeHTML\).  


## <a name="other-webdriver-installation-options"></a>Otras opciones de instalación de WebDriver  

### <a name="docker"></a>Docker  

Si usa [Docker,][DockerHub]ejecute el siguiente comando para descargar una imagen preconfigurada con Microsoft Edge \(Chromium\) y [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] preinstalado.  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Para obtener más información, vaya al [contenedor msedgedriver en Docker Hub][DockerHubMsedgedriver].  


## <a name="testing-internet-explorer"></a>Probar Internet Explorer

Para probar los sitios que requieren Internet Explorer, use [El controlador de Internet Explorer][GithubSeleniumHqWikiIEDriver] con Internet Explorer.  El proyecto Selenio mantiene el controlador de Internet Explorer.  Aunque Microsoft Edge admite el modo IE, no puedes usar Microsoft Edge driver con Microsoft Edge para probar sitios en modo IE.


## <a name="application-guard"></a>Protección de aplicaciones

Los sitios de confianza que usan Protección de aplicaciones de Microsoft Defender (Protección de aplicaciones) se pueden automatizar con Microsoft Edge controlador.

Los sitios que no son de confianza que usan Application Guard no se pueden automatizar ni manipular con Microsoft Edge controlador.  Application Guard inicia sitios que no son de confianza en un contenedor y este contenedor no expone el puerto de depuración remota que Microsoft Edge Driver debe comunicarse con el sitio.

El administrador de la empresa define los sitios de confianza, incluidos los recursos en la nube y las redes internas.  Los sitios que no están en la lista de sitios de confianza se consideran no confiables.  Microsoft Edge El controlador puede automatizar las ventanas de InPrivate y los sitios de la lista de sitios de confianza.

Para obtener más información acerca de Application Guard, vaya a: 

*  [Compatibilidad de Microsoft Edge para la Protección de aplicaciones de Microsoft Defender][DeployedgeMicrosoftEdgeSecurityWindowsDefenderApplicationGuard]
*  [Protección de aplicaciones de Microsoft Defender general][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]


## <a name="see-also"></a>Vea también

*  [Documentación de Selenio:][SeleniumDocumentation] información sobre WebDriver en el contexto de Selenio y cómo escribir pruebas automatizadas de WebDriver con Selenio.


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

El Microsoft Edge está deseando escuchar sus comentarios acerca del uso de WebDriver, marcos de prueba de WebDriver (como Selenio) y Microsoft Edge.  Para enviar al equipo sus preguntas **** y comentarios, elija el icono Enviar comentarios en el Microsoft Edge DevTools o envíe un [tweet][TwitterTweetEdgeDevTools]@EdgeDevTools .  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="El icono Enviar comentarios en las Herramientas de desarrollo del borde de Microsoft Edge" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   El **icono Enviar comentarios** en el Microsoft Edge DevTools  
:::image-end:::  


<!-- links -->  
[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Funcionalidades y EdgeOptions | Microsoft Docs"  
<!-- external links -->
[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability - Microsoft Edge- Directivas | Microsoft Docs"  
[DeployedgeMicrosoftEdgeSecurityWindowsDefenderApplicationGuard]: /deployedge/microsoft-edge-security-windows-defender-application-guard "Microsoft Edge compatibilidad con Protección de aplicaciones de Microsoft Defender | Microsoft Docs"

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Protección de aplicaciones de Microsoft Defender (Windows 10): Windows seguridad | Microsoft Docs"  

[DockerHub]: https://hub.docker.com "Docker Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Concentrador de Docker"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-selenium-tools | GitHub"  
[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-selenium-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SelenioHQ/selenio | GitHub"  
[GithubSeleniumHqWikiIEDriver]: https://github.com/SeleniumHQ/selenium/wiki/InternetExplorerDriver "Controlador de Internet Explorer: selenio | GitHub"

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-selenium-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "selenium-webdriver | npm"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "Microsoft Edge Controlador | Microsoft Edge Programador"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Descargar nuevo Microsoft Edge explorador"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet. CommandLine | NuGet Galería"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.SeleniumTools | NuGet Galería"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium.WebDriver 3.141.0 | NuGet Galería"  
[NugetPackagesSeleniumWebdriver400beta02]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-beta2 "Selenium.WebDriver 4.0.0-beta2 | NuGet Galería"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-selenium-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "selenio | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "La automatización del explorador selenio Project | Documentación para Selenio"  
[SeleniumInstallingLibraries]: https://www.selenium.dev/documentation/en/selenium_installation/installing_selenium_libraries "Instalación de bibliotecas selenio | Selenio"

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "Sonatype Maven Central Repository Search | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Explorador sin cabeza | Wikipedia"  
