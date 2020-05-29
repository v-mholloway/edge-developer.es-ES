---
description: Usa Windows Runtime (WinRT) para llamar a las API de Windows nativas desde tu aplicación de JavaScript.
title: Windows Runtime (WinRT) para JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Windows Runtime, WinRT, PWA, JavaScript
ms.openlocfilehash: 4ca92323a85a1e90896b4de26778f7cf7dfc9a11
ms.sourcegitcommit: e07de36ee9fbe20422ffc2c62b98839851e1b02b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2020
ms.locfileid: "10604027"
---
# Windows Runtime (WinRT) para JavaScript  

[Windows Runtime](/windows/uwp/get-started/universal-application-platform-guide#how-the-universal-windows-platform-relates-to-windows-runtime-apis) \ (o simplemente WinRT \) es la colección de API nativas que potencian las aplicaciones de la [plataforma universal de Windows](/windows/uwp/get-started/universal-application-platform-guide) \ (UWP \) que se ejecutan en todas las [familias de dispositivos de Windows 10](/uwp/extension-sdks/device-families-overview).  Las API de WinRT se proyectan en varios idiomas diferentes, entre los que se incluyen C#, C++, Visual Basic y JavaScript.  

Como desarrollador web, puedes solicitar estas API de Windows nativas de JavaScript cuando tu aplicación web se [ejecuta como una aplicación de Windows 10 instalada](../progressive-web-apps-edgehtml/windows-features.md#set-up-and-run-your-universal-windows-app) en el `wwahost.exe` proceso, en lugar de hacerlo en el explorador \).  Además, el sitio web que se ejecuta como una aplicación de Windows 10 también puede usar el control [WebView de Microsoft Edge](#webview) para mostrar contenido Web remoto y local y API de [MSApp](#msapp) para el control de secuencias y BLOB, entre otras cosas.  

Estas son las áreas de espacio de nombres WinRT de nivel superior disponibles para todas las aplicaciones de Windows 10:  

| Espacio de nombres WinRT | Descripción |  
|:--- |:--- |  
| [AI](/uwp/api/windows.AI.MachineLearning.Preview) \ (versión preliminar \) | Contiene clases que permiten a las aplicaciones cargar modelos de aprendizaje de máquinas, vincular datos como entradas y evaluar los resultados.  |  
| [ApplicationModel](/uwp/api/windows.applicationmodel) | Proporciona a una aplicación acceso a la funcionalidad básica del sistema y a la información en tiempo de ejecución sobre el paquete de la aplicación, y controla las operaciones de suspensión.  |  
| [Datos](/uwp/api/windows.data.html) | Proporciona clases de utilidades para trabajar con varios formatos de datos, como HTML, JSON, PDF, texto y XML.  |  
| [Dispositivos](/uwp/api/windows.devices) | Este espacio de nombres proporciona acceso a los proveedores de dispositivos de bajo nivel, incluidos ADC, GPIO, I2 C, PWM y SPI.  |  
| [Foundation](/uwp/api/windows.foundation) | Habilita la funcionalidad fundamental de Windows en tiempo de ejecución, incluida la administración de operaciones asincrónicas y el acceso a almacenes de propiedades.  Este espacio de nombres también define tipos de valor comunes que representan el identificador uniforme de recursos \ (URI \), fechas y horas, medidas en 2D y otros valores básicos.  |  
| [Juegos](/uwp/api/windows.gaming.input) |Proporciona acceso a la entrada del dispositivo de juego, la barra de juego, la supervisión de juegos y la conversación de juego.  |  
| [Globalization](/uwp/api/windows.globalization) | Proporciona compatibilidad de globalización para perfiles de idiomas, regiones geográficas y calendarios internacionales.  |  
| [Gráficos](/uwp/api/windows.graphics) | Proporciona tipos de datos básicos que contienen información sobre cómo dibujar gráficos.  Estas estructuras de datos suelen usarse para definir cómo se dibujan las superficies grandes al usar la clase CompositionVirtualDrawingSurface.  |  
| [Administración](/uwp/api/windows.management) | Proporciona capacidades para forzar una sincronización desde un dispositivo de administración de dispositivos móviles \ (MDM \) al servidor.  Este protocolo de sincronización de MDM se basa en el estándar de administración de dispositivos Open Mobile Alliance.  |  
| [Multimedia](/uwp/api/windows.media) |Proporciona clases para crear y trabajar con elementos multimedia, como fotos, grabaciones de audio y vídeos.  |  
| [Redes](/uwp/api/windows.networking) |Proporciona acceso a nombres de host y puntos de conexión que usan las aplicaciones de red.  |  
| [Percepción](/uwp/api/windows.perception) |Contiene clases para percibir el entorno del usuario, lo que permite que las aplicaciones encuentren información sobre el dispositivo en relación con las superficies y los hologramas del usuario.  |  
| [Seguridad](/uwp/api/windows.security.authentication.identity) | Proporciona clases para la autenticación de usuarios, la administración de credenciales, las operaciones criptográficas y las características de protección de datos empresariales.  |  
| [Servicios](/uwp/api/windows.services.cortana) |Proporciona acceso a los servicios de Microsoft para Cortana, mapas, Microsoft Store y el contenido del \ (plan \) dirigido.  |  
| [Almacenamiento](/uwp/api/windows.storage) |Proporciona clases para administrar archivos, carpetas y configuración de aplicaciones.  |  
| [Sistema](/uwp/api/windows.system) |Habilita la funcionalidad del sistema, como el inicio de aplicaciones, la obtención de información sobre un usuario y la generación de perfiles de memoria.  |  
| [Interfaz de usuario](/uwp/api/windows.ui) | Proporciona a una aplicación acceso a la funcionalidad básica del sistema y a la información en tiempo de ejecución de la interfaz de usuario.  **Nota**: las API en el `Windows.UI.Xaml` espacio de nombres no están disponibles para las aplicaciones JavaScript \ (que pueden usar las tecnologías basadas en estándares web equivalentes \).  |  
| [Web](/uwp/api/windows.web) | Proporciona información sobre los errores resultantes de las operaciones del servicio Web.  |  

Para obtener más información sobre el uso, consulta [usar Windows Runtime en JavaScript](./using-the-windows-runtime-in-javascript.md).  Para obtener información sobre cómo ejecutar el sitio web como una aplicación de Windows, pruebe el tutorial [personalizar el PWA para Windows](../progressive-web-apps/windows-features.md) .  

## WebView  

El control [WebView de Microsoft Edge](../webview.md) te permite hospedar contenido web dentro de tu aplicación de Windows 10.  Esto es similar a usar un `<iframe>` , pero proporciona muchas [más características y control](../hosting/webview.md#webview-versus-iframe) sobre la experiencia.  

## MSApp  

El objeto global [MSApp](./reference/msapp.md) \ ( `window.MSApp` \) proporciona funciones de ayuda interordenadas para aplicaciones de Windows 10 basadas en JavaScript, como utilidades para convertir entre tipos de objetos de WinRT equivalentes y basados en estándares web.  
