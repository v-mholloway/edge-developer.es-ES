---
description: Introducción a la depuración remota Windows 10 dispositivos
title: Introducción a la depuración remota de Windows 10 dispositivos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/23/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, remoto, depuración, windows 10, windows, portal de dispositivos
ms.openlocfilehash: e3f60f07ba96aaed8cd9d7348eee1b0a846faecf
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519285"
---
# <a name="get-started-with-remote-debugging-windows-10-devices"></a>Introducción a la depuración remota de Windows 10 dispositivos  

Depuración remota de contenido en directo en Windows 10 dispositivo desde el equipo Windows o macOS.  En este tutorial se le enseñarán las siguientes tareas.  

*   Configura el dispositivo Windows 10 para la depuración remota y conéctate a él desde el equipo de desarrollo.  
*   Inspeccione y depure el contenido en directo Windows 10 dispositivo desde el equipo de desarrollo.  
*   Difusión en pantalla del contenido Windows 10 dispositivo en una instancia de DevTools en el equipo de desarrollo.  
    
## <a name="step-1-set-up-the-host-debuggee-machine"></a>Paso 1: Configurar el host (máquina de depuración)  

El host o el equipo de depuración es Windows 10 dispositivo que desea depurar.  Puede ser un dispositivo remoto al que es difícil acceder físicamente o puede que no tenga periféricos de teclado y mouse, lo que dificulta la interacción con las DevTools de Microsoft Edge en ese dispositivo.  Para configurar el equipo host \(debuggee\), debe completar las siguientes acciones.  

*   Instalar y configurar [Microsoft Edge (Chromium)][MicrosoftEdgeMain]  
*   Instalar las [herramientas remotas para Microsoft Edge (Beta)][MicrosoftStoreApps9p6cmfv44zlt] desde el [Microsoft Store][MicrosoftStoreAppsWindows]  
*   Activar [el modo de desarrollador][WindowsAppsGetStartedEnableYourDeviceForDevelopment] y habilitar Device [Portal][WindowsUwpDebugTestPerfDevicePortal]  
    
### <a name="install-and-configure-microsoft-edge-chromium"></a>Instalar y configurar Microsoft Edge (Chromium)  

Si aún no lo ha hecho, instale Microsoft Edge \(Chromium\) desde [esta página][MicrosoftEdgeMain].  Si usa una versión preinstalada de Microsoft Edge en el equipo host \(debuggee\), compruebe que tiene Microsoft Edge \(Chromium\) y no Microsoft Edge \(EdgeHTML\).  Una forma rápida de comprobar es cargar en el explorador y confirmar que el número de versión `edge://settings/help` es 75 o superior.  

Ahora vaya a `edge://flags` en Microsoft Edge \(Chromium\).  En **Marcas de búsqueda**, escriba Habilitar la **depuración remota a**través de Windows Device Portal .  Establece esa marca en **Habilitado**.  A continuación, elija **el botón** Reiniciar para reiniciar Microsoft Edge \(Chromium\).  

:::image type="complex" source="../media/remote-debugging-windows-media-edge-flags-on-host.msft.png" alt-text="Establecer la opción Habilitar depuración remota mediante Windows de Device Portal en Habilitado" lightbox="../media/remote-debugging-windows-media-edge-flags-on-host.msft.png":::
   Establecer la **marca Habilitar depuración remota Windows Device Portal** en **Habilitado**  
:::image-end:::  

### <a name="install-the-remote-tools-for-microsoft-edge-beta"></a>Instalar las herramientas remotas para Microsoft Edge (Beta)  

Instale las [herramientas remotas para Microsoft Edge (Beta)][MicrosoftStoreApps9p6cmfv44zlt] desde el [Microsoft Store][MicrosoftStoreAppsWindows].  

> [!NOTE]
> El **botón** Obtener de herramientas remotas [para Microsoft Edge (Beta)][MicrosoftStoreApps9p6cmfv44zlt] puede deshabilitarse si se encuentra en Windows 10 versión 1809 o anterior.  Para configurar el equipo host \(debuggee\), debe ejecutarse Windows 10 versión 1903 o posterior.  Actualice el equipo host \(debuggee\) para adquirir las herramientas remotas [para Microsoft Edge (Beta).][MicrosoftStoreApps9p6cmfv44zlt]  

:::image type="complex" source="../media/remote-debugging-windows-media-remote-tools-in-store.msft.png" alt-text="Herramientas remotas para Microsoft Edge \(Beta\) en el Microsoft Store" lightbox="../media/remote-debugging-windows-media-remote-tools-in-store.msft.png":::
   Herramientas [remotas para Microsoft Edge (Beta)][MicrosoftStoreApps9p6cmfv44zlt] en el [Microsoft Store][MicrosoftStoreAppsWindows]  
:::image-end:::  

Inicie el cuadro de diálogo Herramientas remotas [para Microsoft Edge (Beta)][MicrosoftStoreApps9p6cmfv44zlt] y, si se le solicita, acepte el cuadro de diálogo de permisos de la aplicación.  Ahora puede cerrar las Herramientas remotas para [Microsoft Edge (Beta)][MicrosoftStoreApps9p6cmfv44zlt] y no es necesario que la abra para futuras sesiones de depuración remota.

### <a name="activate-developer-mode-and-enable-device-portal"></a>Activar el modo de desarrollador y habilitar Device Portal  

Si está en una red WiFi, asegúrese de que la red esté marcada como **Dominio** o **Privado**.  Puedes comprobar el estado abriendo la **aplicación Seguridad de Windows,** eligiendo firewall **&** protección de red y comprobando si la red aparece como una red de dominio o **una red** privada. ****  

Si aparece como **Public**, vaya **a Configuración**Network &  >  **Internet**  >  **Wi-Fi**, **** elija en la **** red y cambie el botón Perfil de red a Privado .  

Ahora, abre la **Configuración** aplicación.  En **Buscar una configuración,** escriba `Developer settings` y elija.  Alternar en **el modo de desarrollador**.  Ahora puedes activar el **Portal de** dispositivos estableciendo Activar diagnóstico remoto a través de conexiones de red de **área local** en **On**.  A continuación, puede activar opcionalmente **la** autenticación para que el dispositivo \(debugger\) del cliente proporcione las credenciales correctas para conectarse a este dispositivo.  

> [!NOTE]
> Si **activa el diagnóstico remoto a través de conexiones de red de área local.** estaba activado anteriormente, debe desactivarlo y volver a activarlo para que **Device Portal** funcione con las Herramientas remotas para [Microsoft Edge (Beta).][MicrosoftStoreApps9p6cmfv44zlt]  Si no **se muestra** una sección Para desarrolladores en **Configuración,** es posible que **Device Portal** ya esté activado, por lo que intenta reiniciar el Windows 10 dispositivo en su lugar.

:::image type="complex" source="../media/remote-debugging-windows-media-host-settings.msft.png" alt-text="La Configuración con el modo de desarrollador y el Portal de dispositivos configurados" lightbox="../media/remote-debugging-windows-media-host-settings.msft.png":::
   La **Configuración** con el **modo de desarrollador** y el Portal de **dispositivos configurados**  
:::image-end:::  

Tenga en cuenta la dirección IP de la máquina y el puerto de conexión que **se muestran Conectar con:**.  La dirección IP de la imagen siguiente es `192.168.86.78` y el puerto de conexión es `50080` .  

:::image type="complex" source="../media/remote-debugging-windows-media-host-settings-ip-address.msft.png" alt-text="Tenga en cuenta la dirección IP y el puerto de conexión en el Configuración" lightbox="../media/remote-debugging-windows-media-host-settings-ip-address.msft.png":::
   Tenga en cuenta la dirección IP y el puerto de conexión en el **Configuración**  
:::image-end:::  

Escribes la información en el dispositivo \(debugger\) del cliente en la [siguiente sección](#step-2-set-up-the-client-debugger-machine).  Abra pestañas en Microsoft Edge y aplicaciones web progresivas [(PWA)][DevtoolsProgressiveWebApps] en el equipo host \(debuggee\) que desea depurar desde el equipo \(depurador\) del cliente.  

## <a name="step-2-set-up-the-client-debugger-machine"></a>Paso 2: Configurar el cliente (máquina depuradora)  

El cliente o el equipo depurador es el dispositivo desde el que desea depurar.  Este dispositivo puede ser tu máquina de desarrollo diaria o puede ser tu PC o MacBook cuando trabajes desde casa.  

Para configurar la máquina \(debugger\) del cliente, instale Microsoft Edge \(Chromium\) desde esta página si aún no lo ha hecho. [][MicrosoftEdgeMain]  Si usa una versión preinstalada de Microsoft Edge en el equipo host \(debuggee\), compruebe que tiene Microsoft Edge \(Chromium\) y no Microsoft Edge \(EdgeHTML\).  Una forma rápida de comprobar es cargar en el explorador y confirmar que el número de versión `edge://settings/help` es 75 o superior.  

Ahora vaya a `edge://flags` en Microsoft Edge \(Chromium\).  En **Marcas de búsqueda**, escriba Habilitar la depuración Windows dispositivo remoto en **edge://inspect**.  Establece esa marca en **Habilitado**.  A continuación, elija **el botón** Reiniciar para reiniciar Microsoft Edge \(Chromium\).  

:::image type="complex" source="../media/remote-debugging-windows-media-edge-flags-on-client.msft.png" alt-text="Establecer la opción Habilitar la depuración Windows dispositivo remoto mediante edge://inspect en Habilitado" lightbox="../media/remote-debugging-windows-media-edge-flags-on-client.msft.png":::
   Establecer la **opción Habilitar la depuración Windows dispositivo remoto mediante edge://inspect** en **Habilitado**  
:::image-end:::  

Ahora vaya a la `edge://inspect` página en Microsoft Edge \(Chromium\).  De forma predeterminada, debería estar en la **sección Dispositivos.**  En **Conectar a**un dispositivo Windows remoto, escriba la dirección IP y el puerto de conexión del equipo host \(debuggee\) en el cuadro de texto siguiendo este patrón: http:// : `IP address` `connection port` .  Ahora elija **Conectar a Dispositivo**.  

:::image type="complex" source="../media/remote-debugging-windows-media-edge-inspect.msft.png" alt-text="La edge://inspect en el cliente" lightbox="../media/remote-debugging-windows-media-edge-inspect.msft.png":::
   La `edge://inspect` página del cliente  
:::image-end:::  

Si configura la autenticación para el equipo host \(debuggee\), **** se **** le pedirá que escriba el nombre de usuario y la contraseña para que el equipo \(depurador\) del cliente se conecte correctamente.  

### <a name="using-https-instead-of-http"></a>Usar https en lugar de http  

Si desea conectarse al equipo host \(debuggee\) en lugar de , debe navegar a en Microsoft Edge en el equipo `https` `http` `http://IP address:50080/config/rootcertificate` \(depurador\) del cliente.  Esto descarga automáticamente un certificado de seguridad denominado `rootcertificate.cer` .

Elija `rootcertificate.cer` .  Se abre la herramienta [Windows Administrador de certificados][DotnetFrameworkWcfFeatureDetailsHowToViewCertificatesWithMmcSnapInViewCertificatesWithCertificateManagerTool].

Elija **Instalar certificado...**, asegúrese de que el usuario **actual** está activado y elija **Siguiente**.  Ahora elija **Colocar todos los certificados en el siguiente almacén** y elija **Examinar...**.  Elija el **almacén Entidades de certificación raíz de** confianza y elija **Aceptar**.  Elija **Siguiente** y, a continuación, **elija Finalizar**.  Si se le solicita, confirme que desea instalar este certificado en el almacén de entidades de certificación **raíz de** confianza.

Ahora, al conectarse al equipo host \(debuggee\) desde el equipo cliente \(depurador\) mediante la página, debe usar `edge://inspect` un valor `connection port` diferente.  De forma predeterminada, para Windows escritorio, Device Portal usa `50080` como `connection port` for `http` .  For `https` , el Portal de dispositivos usa así que siga este `50043` patrón: https:// : en la `IP address` `50043` `edge://inspect` página.  [Obtenga más información sobre los puertos predeterminados usados por Device Portal][WindowsUwpDebugTestPerfDevicePortalSetup].  

> [!NOTE]
> El puerto predeterminado para es y el puerto predeterminado es, pero no siempre es el caso de Device Portal en puertos de notificaciones de escritorio en el intervalo `http` `50080` `https` `50043` efímero \(\>50.000\) para evitar colisiones con las notificaciones de puerto existentes en el dispositivo.  Para obtener más información, vaya a la sección [Puerto Configuración][WindowsUwpDebugTestPerfDevicePortalDesktopRegistryBasedConfigurationForDevicePortal] para Device Portal en Windows escritorio.  

## <a name="step-3-debug-content-on-the-host-from-the-client"></a>Paso 3: Depurar contenido en el host desde el cliente  

Si el equipo cliente \(debugger\) se conecta correctamente al equipo host \(debuggee\), la página del cliente ahora muestra una lista de las pestañas de Microsoft Edge y cualquier PWA abierto en el `edge://inspect` host.  

:::image type="complex" source="../media/remote-debugging-windows-media-edge-inspect-connected.msft.png" alt-text="La edge://inspect del cliente muestra las pestañas de Microsoft Edge y PWA en el host" lightbox="../media/remote-debugging-windows-media-edge-inspect-connected.msft.png":::
   La `edge://inspect` página del cliente muestra las pestañas de Microsoft Edge y PWA en el host  
:::image-end:::  

Determine el contenido que desea depurar y elija **inspeccionar**.  El Microsoft Edge DevTools se abre en una nueva pestaña y se proyecta el contenido del equipo host \(debuggee\) al equipo \(depurador\) del cliente.  Ahora puede usar toda la potencia del Microsoft Edge DevTools en el cliente para el contenido que se ejecuta en el host.  Obtenga más información sobre cómo usar el Microsoft Edge DevTools [aquí][DevtoolsIndex].  

:::image type="complex" source="../media/remote-debugging-windows-media-devtools-client.msft.png" alt-text="El Microsoft Edge DevTools en el cliente depurando una pestaña en Microsoft Edge en el host" lightbox="../media/remote-debugging-windows-media-devtools-client.msft.png":::
   El [Microsoft Edge DevTools][DevtoolsIndex] en el cliente depurando una pestaña en Microsoft Edge en el host  
:::image-end:::  

### <a name="inspect-elements"></a>Inspeccionar elementos  

Por ejemplo, intente inspeccionar un elemento.  Vaya a la **herramienta Elementos** de la instancia de DevTools en el cliente y mantenga el mouse sobre un elemento para resaltarlo en la ventanilla del dispositivo host.  

También puedes pulsar un elemento en la pantalla del dispositivo host para elegirlo en la **herramienta** Elementos.  Elija **Seleccionar elemento** en la instancia de DevTools en el cliente y, a continuación, pulse el elemento en la pantalla del dispositivo host.  

> [!NOTE]
> **Select Element** está deshabilitado después del primer toque, por lo que debes volver a activarlo cada vez que quieras usar esta característica.  

> [!IMPORTANT]
> El **panel Escuchas de eventos** de la herramienta **Elementos** está en blanco Windows 10 versión 1903.  Este es un problema conocido y el equipo planea corregir el panel **Escuchas** de eventos en una actualización de mantenimiento a Windows 10 versión 1903.  

## <a name="step-4-screencast-your-host-screen-to-your-client-device"></a>Paso 4: Difusión en pantalla de la pantalla host al dispositivo cliente  

De forma predeterminada, la instancia de DevTools en el cliente tiene la difusión de pantalla activada, lo que le permite ver el contenido en el dispositivo host en la instancia de DevTools en el dispositivo cliente.  Elija **Alternar difusión en** pantalla para desactivar o activar esta característica.  

:::image type="complex" source="../media/remote-debugging-windows-media-toggle-screencast.msft.png" alt-text="El botón Alternar difusión en pantalla del Microsoft Edge DevTools en el cliente" lightbox="../media/remote-debugging-windows-media-toggle-screencast.msft.png":::
   Botón **Alternar difusión** en pantalla en Microsoft Edge DevTools en el cliente  
:::image-end:::  

Puedes interactuar con la difusión en pantalla de varias maneras:  
*   Las opciones se traducen en pulsaciones, lo que dispara los eventos táctiles adecuados en el dispositivo.  
*   Las pulsaciones de teclas del equipo se envían al dispositivo.  
*   Para simular un gesto de pellizco, mantén `Shift` presionado mientras arrastras.  
*   Para desplazarse, use el trackpad o la rueda del mouse o fling con el puntero del mouse.  

Algunas notas de las difusión en pantalla:  
*   Los difusión en pantalla solo muestran el contenido de la página.  Las partes transparentes de la difusión en pantalla representan interfaces de dispositivo, como la barra de direcciones Microsoft Edge, la barra de tareas Windows 10 o el Windows 10 teclado.  
*   Las difusión en pantalla afectan negativamente a las tasas de fotogramas.  Deshabilite la difusión por pantalla al medir desplazamientos o animaciones para obtener una imagen más precisa del rendimiento de la página.  
*   Si la pantalla del dispositivo host se bloquea, el contenido de la difusión en pantalla desaparece.  Desbloquea la pantalla del dispositivo host para reanudar automáticamente la difusión por pantalla.  

## <a name="known-issues"></a>Problemas conocidos  

El **panel Escuchas de eventos** de la herramienta **Elementos** está en blanco Windows 10 versión 1903.  El equipo tiene previsto corregir el panel **Escuchas de** eventos en una actualización de mantenimiento a Windows 10 versión 1903.  

El **panel Cookies** del panel **Aplicación** está en blanco Windows 10 versión 1903.  El equipo tiene previsto corregir el **panel Cookies** en una actualización de servicio a Windows 10 versión 1903.  

La **herramienta Auditorías,** la herramienta Vista **** **** **3D,** la sección Dispositivos emulados de **** **Configuración**y el panel de árbol Accesibilidad de la herramienta Elementos no funcionan actualmente como se esperaba.  El equipo planea corregir las herramientas enumeradas en una actualización futura de Microsoft Edge.  

El explorador de archivos no se inicia desde DevTools en la **herramienta Orígenes** ni en el **panel** Seguridad al depurar de forma remota.  El equipo planea corregir las herramientas en una actualización futura de Microsoft Edge.  

<!-- links -->

[DevtoolsIndex]: ../index.md "Introducción a Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Depurar aplicaciones web progresivas | Microsoft Docs"  

[DotnetFrameworkWcfFeatureDetailsHowToViewCertificatesWithMmcSnapInViewCertificatesWithCertificateManagerTool]: /dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in#view-certificates-with-the-certificate-manager-tool "Ver certificados con la herramienta Administrador de certificados: Cómo: Ver certificados con el complemento MMC | Microsoft Docs"  

[WindowsAppsGetStartedEnableYourDeviceForDevelopment]: /windows/apps/get-started/enable-your-device-for-development "Habilitar el dispositivo para desarrollo | Microsoft Docs"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Windows Información general del Portal de dispositivos | Microsoft Docs"  
[WindowsUwpDebugTestPerfDevicePortalSetup]: /windows/uwp/debug-test-perf/device-portal#setup "Configuración: Windows información general del Portal de dispositivos | Microsoft Docs"  
[WindowsUwpDebugTestPerfDevicePortalDesktopRegistryBasedConfigurationForDevicePortal]: /windows/uwp/debug-test-perf/device-portal-desktop#registry-based-configuration-for-device-portal "Configuración basada en el Registro para Device Portal: Device Portal for Windows Desktop | Microsoft Docs"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Descargar nuevo Microsoft Edge explorador"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Windows Aplicaciones | Microsoft Store"  

[MicrosoftStoreApps9p6cmfv44zlt]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Herramientas remotas para Microsoft Edge (Beta) | Microsoft Store"  
