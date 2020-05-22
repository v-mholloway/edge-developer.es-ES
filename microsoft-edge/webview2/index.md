---
description: Hospedar contenido web en la aplicación Win32 con el control de WebView 2 de Microsoft Edge
title: Control WebView2 de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, control del explorador, HTML Edge, Windows Forms, WinForms, WPF, .NET
ms.openlocfilehash: 4f28ef64bb2936bc6c9a089ea2574070738fc79d
ms.sourcegitcommit: 8f5c9255dadc2a9bb22c3201d15b57d84851fe64
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "10671641"
---
# Introducción a Microsoft Edge WebView2 (versión preliminar)  

El control Microsoft Edge WebView2 permite incrustar tecnologías web \ (HTML, CSS y JavaScript \) en las aplicaciones nativas.  El control WebView2 usa [Microsoft Edge (cromo)](https://www.microsoftedgeinsider.com) como motor de representación para mostrar el contenido web en aplicaciones nativas.  Con WebView2, puedes incrustar código web en diferentes partes de tu aplicación nativa o compilar toda la aplicación nativa dentro de una sola vista Web.  Para obtener información sobre cómo empezar a crear una aplicación de WebView2, consulte [Introducción](./index.md#getting-started).  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="¿Qué es la vista previa?":::
   ¿Qué es la vista previa?  
:::image-end:::  

> [!NOTE]
> La vista previa de WebView2 está pensada para el prototipo anticipado y para recopilar comentarios con el fin de ayudar a dar forma a la API.  El equipo de WebView de Microsoft Edge no recomienda usar la vista previa en las aplicaciones de producción porque es posible que se [produzcan cambios importantes](./releasenotes.md).  

## Enfoque de aplicaciones híbridas  

Los programadores suelen tener que elegir entre crear una aplicación web o una aplicación nativa.  La decisión depende del equilibrio entre el alcance y el potencial de energía.  Las aplicaciones web permiten un amplio alcance.  Como desarrollador web, puede volver a usar la mayoría, si no todo el código, en todas las plataformas.  Las aplicaciones nativas, sin embargo, usan las capacidades de toda la plataforma nativa.  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web Native":::
   Web Native  
:::image-end:::  

Las aplicaciones híbridas permiten a los desarrolladores disfrutar de lo mejor de ambos mundos.  Los programadores de aplicaciones híbridas se benefician de la Ubiquity y fortaleza de la plataforma web, así como de la potencia y capacidades completas de la plataforma nativa.  

## Beneficios de WebView2   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Motivos de la vista en vista previa":::
   Motivos de la vista en vista previa  
:::image-end:::  

:::row:::
   :::column span="1":::
      **Ecosistema web \ & Aptitudes**  
      Use toda la plataforma web, bibliotecas, herramientas y talento que existen en el ecosistema Web.  
   :::column-end:::
   :::column span="1":::
      **Innovación rápida**  
      El desarrollo web permite una implementación e iteración más rápidas.  
   :::column-end:::
   :::column span="1":::
      **Compatibilidad con Windows 7, 8, 10**  
      Compatibilidad con una experiencia de usuario coherente en Windows 7, 8 y 10.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **Capacidades nativas**  
      Acceder al conjunto completo de API nativas.  
   :::column-end:::
   :::column span="1":::
      **Uso compartido de código**  
      Agregar código web a su código base permite un aumento de la reutilización en varias plataformas.  
   :::column-end:::
   :::column span="1":::
      **Soporte técnico de Microsoft**  
      Microsoft proporciona soporte técnico y agrega nuevas solicitudes de características cuando WebView2 se publica como GA.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **Distribución de hoja perenne**  
      Use una versión actualizada de cromo con actualizaciones de plataforma y revisiones de seguridad regulares.  
   :::column-end:::
   :::column span="1":::
      **Fijo** \ (próximamente \)  
      Elija empaquetar los bits de cromo en la aplicación.  
   :::column-end:::
   :::column span="1":::
      **Adopción incremental**  
      Agregue componentes Web por partes a la aplicación.  
   :::column-end:::
:::row-end:::  

## Tareas iniciales  

Para compilar y probar la aplicación con el control WebView2, debe tener instalado tanto [Microsoft Edge (cromo)](https://www.microsoftedgeinsider.com/download) como el [SDK de WebView2](https://aka.ms/webviewnuget) .  Seleccione una de las siguientes opciones para comenzar.  

*   [Introducción a Win32 C/C++](./gettingstarted/win32.md)  
*   [Introducción a WPF](./gettingstarted/wpf.md)  
*   [Introducción a WinForms](./gettingstarted/winforms.md)  

El repositorio de [muestras de WebView2](https://github.com/MicrosoftEdge/WebView2Samples) contiene ejemplos que muestran todas las características de los SDK de WebView2 y los patrones de uso de API. A medida que se agregan más características al SDK de WebView2, se actualizarán las aplicaciones de ejemplo.   

## Plataformas compatibles  

Una vista previa para desarrolladores está disponible en los siguientes entornos de programación.  

*   C/C++ Win32  
*   .NET Framework 4.6.2 o posterior  
*   .NET Core 3,0 o posterior  
*   [WinUI 3,0](/uwp/toolkits/winui3/)  

Debe ejecutar Windows 10, Windows 8,1, Windows 8, Windows 7, Windows Server 2016, Windows Server 2012/2012R2 o Windows Server 2008 R2.   

## Pasos siguientes  

Para obtener información más detallada sobre cómo crear e implementar aplicaciones de WebView2, desproteja nuestra documentación conceptual<!-- and how-to guides-->.  

#### Conceptos  

*   [SDK de WebView2 y versiones de Microsoft Edge](./concepts/versioning.md)
*   [Distribuir aplicaciones de WebView2](./concepts/distribution.md)  
 
#### Guías de procedimientos  

*   [Depurar WebView2 con DevTools y la depuración de scripts de Visual Studio](./howto/debug.md)  
*   [Automatizar y depurar WebView2 con Microsoft EdgeDriver](./howto/webdriver.md)  

<!--todo: add how-tos when available  -->  

## Ponerse en contacto con el equipo de WebView2  

Ayuda a crear una experiencia WebView2 más rica compartiendo tus comentarios.  Visita el repositorio de [comentarios](https://aka.ms/webviewfeedback) de WebView para enviar solicitudes de características o informes de errores.  También es un buen lugar para buscar problemas conocidos.  

> [!NOTE]
> Durante la vista previa del desarrollador, el equipo de WebView de Microsoft Edge también recopila datos para ayudar a crear una vista previa mejorada.  Los usuarios pueden desactivar la recopilación de datos de WebView desplazándose a `edge://settings/privacy` en el explorador Microsoft Edge y desactivando la recopilación de datos del explorador.  
