---
title: Introducción a la depuración remota dispositivos con Windows 10
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, remoto, depuración, Windows 10, Windows, portal de dispositivos
ms.openlocfilehash: b944e1f16d4c26f4db83e3eb131f1da8ea938c97
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573897"
---
# Introducción a la depuración remota dispositivos con Windows 10  

Depure contenido en vivo de forma remota en un dispositivo con Windows 10 desde el equipo con Windows o macOS.  Este tutorial le enseña a:  

*   Configure el dispositivo Windows 10 para la depuración remota y conéctese a él desde el equipo de desarrollo.  
*   Inspeccione y depure contenido en vivo en el dispositivo Windows 10 desde el equipo de desarrollo.  
*   Contenido de screencast de su dispositivo Windows 10 en una instancia de DevTools en el equipo de desarrollo.  

## Paso 1: configurar el host (equipo de depuración)  

El host o la máquina depurada es el dispositivo de Windows 10 que desea depurar.  Puede ser un dispositivo remoto que sea difícil de acceder físicamente o puede que no tenga periféricos de teclado y ratón, lo que dificulta la interacción con el DevTools de Microsoft Edge en ese dispositivo.  Para configurar el equipo de host (depurado), tendrá que:  

*   Instalar y configurar [Microsoft Edge (cromo)](https://www.microsoft.com/edge)  
*   Instalar [herramientas remotas para Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) desde [Microsoft Store](https://www.microsoft.com/store/apps/windows)  
*   Activar el [modo de desarrollador](https://docs.microsoft.com/windows/uwp/get-started/enable-your-device-for-development) y habilitar el portal de [dispositivos](https://docs.microsoft.com/windows/uwp/debug-test-perf/device-portal)  

### Instalar y configurar Microsoft Edge (cromo)  

Si todavía no lo ha hecho, instale Microsoft Edge (cromo) en [esta página](https://www.microsoft.com/edge).  Si está usando una versión preinstalada de Microsoft Edge en el equipo de host (depurado), compruebe que tiene Microsoft Edge (cromo) y no Microsoft Edge (EdgeHTML).  Una forma rápida de comprobar es cargar `edge://settings/help` en el explorador y confirmar que el número de versión es 75 o superior.  

Ahora, vaya a `edge://flags` en Microsoft Edge (cromo).  En **marcas de búsqueda**, escriba **Habilitar depuración remota a través de Windows Device portal**.  Establezca el marcador en **habilitado**.  Después, haga clic en el botón **reiniciar** para reiniciar Microsoft Edge (cromo).  

> ##### Figura 1  
> Configuración de la opción **Habilitar depuración remota mediante Windows Device portal** en **habilitado**  
> ![Configuración de la opción Habilitar depuración remota mediante Windows Device portal en habilitado](./windows-media/edge-flags-on-host.png)  

### Instalar herramientas remotas para Microsoft Edge (beta)  

Instale las [herramientas remotas de Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) en [Microsoft Store](https://www.microsoft.com/store/apps/windows).  

> [!NOTE]
> El botón **obtener** de las [herramientas remotas de Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) puede estar deshabilitado si estás en Windows 10 versión 1809 o versiones anteriores.  Para configurar el equipo de host (depurado), debe estar ejecutando Windows 10 versión 1903 o posterior.  Actualiza el equipo de host (depurado) para adquirir las [herramientas remotas de Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT).  

> ##### Figura 2  
> [Herramientas remotas para Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) en [Microsoft Store](https://www.microsoft.com/store/apps/windows)  
> ![Herramientas remotas para Microsoft Edge (beta) en Microsoft Store](./windows-media/remote-tools-in-store.png)  

Inicia las [herramientas remotas de Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) y, si se le solicita, acepta el cuadro de diálogo de permisos en la aplicación. Ahora puede cerrar las [herramientas remotas de Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) y no es necesario que esté abierta para futuras sesiones de depuración remota.

### Activar el modo de desarrollador y habilitar el portal de dispositivos  

Si estás en una red WiFi, asegúrate de que la red esté marcada como **dominio** o **privada**.  Para comprobarlo, abra la aplicación de **seguridad de Windows** , haga clic en **firewall & protección de red** y compruebe si su red aparece como red de **dominio** o como red **privada** .  

Si se muestra como **público**, vaya a **configuración**  >  **red & Internet**  >  **Wi-Fi**, haga clic en su red y cambie el botón **Perfil de red** a **privado**.  

Ahora, abra la aplicación **configuración** .  En **buscar una configuración**, escriba la **configuración de desarrollador** y selecciónela.  Activar o desactivar el **modo para programadores**.  Ahora puede habilitar el **portal de dispositivos** configurando **Activar diagnósticos remotos a través de conexiones de red de área local** en **activado**.  Después, puede activar de forma opcional la **autenticación** para que el dispositivo cliente (depurador) deba proporcionar las credenciales correctas para conectarse a este dispositivo.  

> [!NOTE]
> Si **activa los diagnósticos remotos a través de conexiones de red de área local.** se habilitó, debe deshabilitarla y habilitarla de nuevo para que **Device portal** funcione con [herramientas remotas para Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT). Si no ve una sección **para desarrolladores** en **configuración**, es posible que el **portal de dispositivos** ya esté habilitado para intentar reiniciar el dispositivo Windows 10.

> ##### Imagen 3  
> La aplicación **configuración** con el **modo de desarrollador** y el portal de **dispositivos** configurado  
> ![La aplicación configuración con el modo de desarrollador y el portal de dispositivos configurado](./windows-media/host-settings.png)  

Anote la dirección IP de la máquina y el puerto de conexión aparecen en **conectar usando:**.  La dirección IP de la imagen siguiente es `192.168.86.78` y el puerto de conexión es `50080` .  

> ##### Imagen 4  
> Anote la dirección IP y el puerto de conexión en la **configuración**  
> ![Anote la dirección IP y el puerto de conexión en la configuración](./windows-media/host-settings-ip-address.png)  

Escribirás esta información en el dispositivo cliente (depurador) de la [siguiente sección](#step-2-set-up-the-client-debugger-machine).  Abra las pestañas de Microsoft Edge y las [aplicaciones web progresivas (PWAs)](../progressive-web-apps.md) en el equipo de host (depurado) que desea depurar desde el equipo del cliente (depurador).  

## Paso 2: configurar el cliente (equipo de depuración)  

El cliente o el equipo depurador es el dispositivo desde el que desea depurar.  Este dispositivo puede ser su equipo de desarrollo diario o puede ser su equipo PC o MacBook al trabajar desde casa.  

Para configurar el equipo cliente (depurador), instala Microsoft Edge (cromo) desde [esta página](https://www.microsoft.com/edge) si aún no lo has hecho.  Si está usando una versión preinstalada de Microsoft Edge en el equipo de host (depurado), compruebe que tiene Microsoft Edge (cromo) y no Microsoft Edge (EdgeHTML).  Una forma rápida de comprobar es cargar `edge://settings/help` en el explorador y confirmar que el número de versión es 75 o superior.  

Ahora, vaya a `edge://flags` en Microsoft Edge (cromo).  En **marcas de búsqueda**, escriba **Habilitar la depuración de dispositivos remotos de Windows en Edge://Inspect**.  Establezca el marcador en **habilitado**.  Después, haga clic en el botón **reiniciar** para reiniciar Microsoft Edge (cromo).  

> ##### Imagen 5  
> Configurar la **depuración de dispositivos de Windows remotos mediante** la marca Edge://Inspect en **habilitado**  
> ![Configurar la depuración de dispositivos de Windows remotos mediante la marca edge://inspect en habilitado](./windows-media/edge-flags-on-client.png)  

Ahora, vaya a la `edge://inspect` página en Microsoft Edge (cromo).  De forma predeterminada, debe estar en la sección **dispositivos** .  En **conectar con un dispositivo Windows remoto**, escriba la dirección IP y el puerto de conexión del equipo de host (de depuración) en el cuadro de texto siguiendo este patrón: http:// `IP address` : `connection port` .  Ahora, haga clic en **conectar con el dispositivo**.  

> ##### Imagen 6  
> La `edge://inspect` página en el cliente  
> ![La página edge://inspect en el cliente](./windows-media/edge-inspect.png)  

Si configura la autenticación para el equipo de host (depurado), se le pedirá que escriba el **nombre de usuario** y la **contraseña** para que el equipo cliente (depurador) se conecte correctamente.  

### Usar https en lugar de http  

Si desea conectar con el equipo de host (depurado) mediante en `https` lugar de `http` , debe Navgiate `http://IP address:50080/config/rootcertificate` en Microsoft Edge en el equipo del cliente (depurador). Se descargará automáticamente un certificado de seguridad denominado `rootcertificate.cer` .

Haga clic en activado `rootcertificate.cer` . Se abrirá la [herramienta Administrador de certificados de Windows](https://docs.microsoft.com/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in#view-certificates-with-the-certificate-manager-tool).

Haga clic en **instalar certificado...**, asegúrese de que el **usuario actual** está seleccionado y haga clic en **siguiente**. Ahora, seleccione **colocar todos los certificados en el siguiente almacén** y haga clic en **examinar...**. Seleccione el almacén de **entidades emisoras de certificados raíz de confianza** y haga clic en **Aceptar**. Haz clic en **Siguiente** y, después, en **Finalizar**. Si se le solicita, confirme que desea instalar este certificado en el almacén de **entidades emisoras de certificados raíz de confianza** .

Ahora, al conectarse al equipo de host (depurado) desde el equipo cliente (depurador) con la `edge://inspect` página, debe usar un `connection port` valor diferente.  De forma predeterminada, para las ventanas de escritorio, el portal `50080` de dispositivos usará como el `connection port` para `http` .  `https`En el caso de, el portal de dispositivos `50043` se usa para seguir este patrón: https:// `IP address` : `50043` en la `edge://inspect` página.  [Más información sobre los puertos predeterminados usados por Device portal](https://docs.microsoft.com/windows/uwp/debug-test-perf/device-portal#setup).  

> [!NOTE]
> El puerto predeterminado para `http` is `50080` y el puerto predeterminado para `https` es, `50043` pero esto no siempre es el caso de que el portal de dispositivos en los puertos de notificaciones de escritorio en el intervalo efímero (>50.000) Evite las colisiones con las notificaciones de puertos existentes en el dispositivo.  Para obtener más información, consulta la sección [configuración de puertos](https://docs.microsoft.com/windows/uwp/debug-test-perf/device-portal-desktop#registry-based-configuration-for-device-portal) de Device portal en el escritorio de Windows.  

## Paso 3: depurar el contenido en el host desde el cliente  

Si el equipo cliente (depurador) se conecta correctamente al equipo de host (depurado), la `edge://inspect` página del cliente mostrará ahora una lista de las pestañas de Microsoft Edge y cualquier PWAs abierta en el host.  

> ##### Imagen 7  
> La `edge://inspect` página del cliente muestra las pestañas de Microsoft Edge y PWAs en el host.  
> ![La página edge://inspect en el cliente muestra las pestañas en Microsoft Edge y PWAs en el host.](./windows-media/edge-inspect-connected.png)  

Determine el contenido que desea depurar y haga clic en **inspeccionar**.  El DevTools de Microsoft Edge se abrirá en una nueva pestaña y mostrará el contenido del equipo de host (depurado) en el equipo cliente (depurador).  Ahora puede usar toda la potencia de Microsoft Edge DevTools en el cliente para el contenido que se ejecuta en el host.  Para obtener más información sobre cómo usar Microsoft Edge DevTools [aquí](../../devtools-guide-chromium.md).  

> ##### Imagen 8  
> [Microsoft Edge DevTools](../../devtools-guide-chromium.md) en el cliente depurar una pestaña en Microsoft Edge en el host  
> ![Microsoft Edge DevTools en el cliente depurar una pestaña en Microsoft Edge en el host](./windows-media/devtools-client.png)  

### Inspeccionar elementos  

Por ejemplo, intenta inspeccionar un elemento.  Vaya al panel **elementos** de la instancia de DevTools en el cliente y mantenga el mouse sobre un elemento para resaltarlo en el área de visualización del dispositivo host.  

También puede puntear en un elemento de la pantalla del dispositivo host para seleccionarlo en el panel **elementos** .  Haga clic en **Seleccionar elemento** en la instancia de DevTools en el cliente y, a continuación, puntee en el elemento de la pantalla del dispositivo host.  Ten en cuenta que el **elemento Select** se deshabilita después del primer toque, por lo que deberás volver a habilitarlo cada vez que quieras usar esta característica.  

> [!IMPORTANT]
> El panel de **escuchas de eventos** del panel **elementos** está en blanco en la versión 1903 de Windows 10.  Este es un problema conocido y corregiremos el panel de **detectores de eventos** en una actualización de mantenimiento a la versión 1903 de Windows 10.  

## Paso 4: screencasts la pantalla de host a su dispositivo cliente  

De forma predeterminada, la instancia de DevTools en el cliente activará el screencasts, lo que le permitirá ver el contenido en el dispositivo host en la instancia de DevTools en el dispositivo cliente.  Haga clic en **activar la screencast** para activar o desactivar esta característica.  

> ##### Imagen 9  
> Botón de alternancia de la **screencast** en Microsoft Edge DevTools en el cliente  
> ![Botón de alternancia de la screencast en Microsoft Edge DevTools en el cliente](./windows-media/toggle-screencast.png)  

Puede interactuar con el screencast de varias maneras:  
*   Los clics se traducen en pulsaciones, lo que desencadena eventos táctiles adecuados en el dispositivo.  
*   Las pulsaciones de tecla de tu equipo se envían al dispositivo.  
*   Para simular un gesto de reducir, espera `Shift` mientras arrastra.  
*   Para desplazarse, use el panel táctil o la rueda del mouse, o Fling con el puntero del mouse.  

Algunas notas en los screencasts:  
*   Los screencasts solo muestran el contenido de la página.  Partes transparentes del screencast representan interfaces de dispositivo, como la barra de direcciones de Microsoft Edge, la barra de tareas de Windows 10 o el teclado de Windows 10.  
*   Los screencasts afectan negativamente a las tarifas de fotogramas.  Deshabilite el screencasts y mida los desplazamientos o animaciones para obtener una imagen más precisa del rendimiento de la página.  
*   Si la pantalla del dispositivo de hospedaje se bloquea, el contenido del screencast desaparece.  Desbloquee la pantalla del dispositivo host para reanudar automáticamente el screencast.  

## Problemas conocidos  

El panel de **escuchas de eventos** del panel **elementos** está en blanco en la versión 1903 de Windows 10.  Corregiremos el panel de **detectores de eventos** en una actualización de mantenimiento de la versión 1903 de Windows 10.  

El panel **cookies** en el panel de la **aplicación** está en blanco en la versión 1903 de Windows 10.  Corregiremos el panel de **cookies** en una actualización de mantenimiento de Windows 10, versión 1903.  

El panel **auditorías** , el panel **vista 3D** , la **sección dispositivos emulados** de **configuración**y el panel de **árbol de accesibilidad** en el panel **elementos** no funcionan actualmente de la forma esperada.  Corregiremos estas herramientas en una futura actualización de Microsoft Edge.  

El explorador de archivos no se inicia desde el DevTools en el panel de **fuentes** o en el panel de **seguridad** cuando se realiza la depuración remota.  Corregiremos estas herramientas en una futura actualización de Microsoft Edge.  
