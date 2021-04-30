---
description: Hacer que tu PWA sea más reconocible publicando en Microsoft Store
title: Publicar la aplicación web progresiva en Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicaciones web progresivas, PWA, Edge, Windows, Microsoft Store
ms.openlocfilehash: 5e78e909187408566219ffe80779bb9221b585fa
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2021
ms.locfileid: "11527085"
---
# <a name="publish-your-progressive-web-app-to-the-microsoft-store"></a>Publicar la aplicación web progresiva en Microsoft Store  

Publicar la aplicación web progresiva \(PWA\) en [Microsoft Store][WindowsUwpPublishIndex] ofrece las siguientes ventajas.  

:::row:::
   :::column span="1":::
      **Detectabilidad**  
   :::column-end:::
   :::column span="2":::
      Los usuarios buscan aplicaciones de forma natural en la tienda de aplicaciones.  Cuando publicas en Microsoft Store, millones de usuarios de Windows pueden descubrir tu PWA junto con otras aplicaciones de Windows.  La Tienda muestra aplicaciones a través de categorías, colecciones curadas y mucho más.  Los portales de detección de aplicaciones proporcionan una experiencia de exploración y compra fácil para los posibles usuarios de la aplicación.  Incluso puedes mejorar [la descripción de la Tienda][WindowsUwpPublishAppScreenshotsImages] con capturas de pantalla, una imagen de héroe y tráileres de vídeo.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Fiabilidad**  
   :::column-end:::
   :::column span="2":::
      Los clientes de Windows saben que pueden confiar en sus compras y descargas de Microsoft Store, ya que se adhieren a los rigurosos estándares de calidad [y seguridad de][LegalWindowsAgreementsStorePolicies]Microsoft.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Instalación sencilla**  
   :::column-end:::
   :::column span="2":::
      La Microsoft Store proporciona una experiencia de instalación coherente y fácil de usar en [todas las aplicaciones de Windows 10.][MicrosoftStoreAppsWindows]  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Análisis de aplicaciones**  
   :::column-end:::
   :::column span="2":::
      El [panel del Centro de partners de Windows][WindowsUwpPublishIndex] te proporciona análisis [detallados][WindowsUwpPublishAnalytics] sobre el estado de la aplicación, el uso y mucho más.  
   :::column-end:::
:::row-end:::  

Para publicar tu PWA en Microsoft Store, no es necesario realizar cambios en el código.  En su lugar, creas una reserva de aplicación, empaquetas tu PWA y envías el paquete a la Tienda.  En las secciones siguientes se explican los pasos.   

## <a name="create-an-app-reservation"></a>Crear una reserva de aplicación  

[El Centro de partners de Windows][MicrosoftPartnerDashboardWindowsOverview] es el centro para que envíes la aplicación a la Microsoft Store.  

Para crear una reserva de aplicación, complete las siguientes acciones.  

1.  Para mostrar los programas inscritos, realice las siguientes acciones.  
    1.  Inicie sesión en el Centro de partners de Windows con su cuenta microsoft y vaya al [Panel del Centro de partners.][MicrosoftPartnerDashboardHome]  
    1.  Navegar a **Windows & Xbox**  
        *   Si se muestra & Xbox de **Windows,** la aplicación ya está registrada.  
        *   Si **Windows & xbox** no se muestra, elige Agregar **programa**.  
    
    :::image type="complex" source="./media/windows-partner-center-add-program.msft.png" alt-text="Agregar un programa en el panel del Centro de partners de Windows" lightbox="./media/windows-partner-center-add-program.msft.png":::
       Agregar un programa en el panel del Centro de partners de Windows
    :::image-end:::  
    
1.  Para inscribirse en el programa de desarrolladores, realice las siguientes acciones.  
    1.  Navega a **Windows & Xbox**.  
    1.  Elija **Introducción**.  
    1.  Sigue las instrucciones.  
1.  Ahora, tu cuenta está inscrita en el programa para desarrolladores de aplicaciones. Para crear una reserva de aplicación, complete las siguientes acciones.  
    1.  Navega a **Windows & Xbox**.  
    1.  Elija **Información general**Crear una nueva  >  **aplicación**.  
    1.  Escriba el nombre de la aplicación en el símbolo del sistema.  
    1.  Elija `Reserve product name` .  
        
    :::image type="complex" source="./media/windows-partner-center-create-app.msft.png" alt-text="Crear una reserva de aplicación en el Centro de partners de Windows" lightbox="./media/windows-partner-center-create-app.msft.png":::
       Crear una reserva de aplicación en el Centro de partners de Windows  
    :::image-end:::  
    
1.  Para mostrar los detalles del editor para su uso en la sección [Empaquetar su PWA,](#package-your-pwa-for-the-store) elija **Product management**  >  **Product Identity**.  
    
    :::image type="complex" source="./media/windows-partner-center-publisher-info.msft.png" alt-text="Copiar la información del editor desde el Centro de partners de Windows" lightbox="./media/windows-partner-center-publisher-info.msft.png":::
       Copiar la información del editor desde el Centro de partners de Windows  
    :::image-end:::  
    
1.  Copie y guarde los siguientes valores.  
    *   **Id. de paquete**  
    *   **Id. de publicador**  
    *   **Nombre para mostrar del editor**  
        
## <a name="package-your-pwa-for-the-store"></a>Empaquetar tu PWA para la Tienda 

Ahora que ya tienes la información de publicación de aplicaciones, genera un paquete de aplicación de Windows para tu PWA.

Para generar un paquete de aplicación, complete las siguientes acciones.  

1.  Vaya al [Generador de PWA][PwabuilderMain].  
1.  Escriba la dirección URL de su PWA.  
1.  Elija **Start**  >  **Build My PWA**  >  **Windows**  >  **Options**.  
1.  Pegue los siguientes valores que guardó en la [sección Crear una reserva de](#create-an-app-reservation) aplicación.  
    *   **Id. de paquete**  
    *   **Id. de publicador**  
    *   **Nombre para mostrar del editor**  
        
    :::image type="complex" source="./media/pwabuilder-publisher-info.msft.png" alt-text="Pegar información del editor en PWABuilder" lightbox="./media/pwabuilder-publisher-info.msft.png":::
       Pegar información del editor en PWABuilder  
    :::image-end:::  
    
1.  Elija **Listo**.  
1.  Para descargar el paquete de la aplicación de Windows, elija **Descargar**.

La descarga es un `.zip` archivo que contiene un archivo y un `.msixbundle` `.classic.appxbundle` archivo.  Los dos paquetes de aplicaciones permiten que tu PWA se ejecute en una amplia variedad de versiones de Windows.  Para obtener más información, vaya [a ¿Qué es un paquete clásico?][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd].  

### <a name="submit-your-app-package-to-the-store"></a>Enviar el paquete de la aplicación a la Tienda  

Para enviar la aplicación a la Tienda, complete las siguientes acciones.  

1.  Navegar al [Centro de partners de Windows][MicrosoftPartnerDashboardWindowsOverview] 
1.  Elige tu aplicación.  
1.  Elija **Iniciar el envío**.  
    
    :::image type="complex" source="./media/windows-partner-center-start-submission.msft.png" alt-text="Iniciar un nuevo envío de aplicación en el Centro de partners de Windows" lightbox="./media/windows-partner-center-start-submission.msft.png":::
       Iniciar un nuevo envío de aplicación en el Centro de partners de Windows  
    :::image-end:::  
    
1.  Complete los siguientes mensajes para obtener información sobre la aplicación.
    *   pricing  
    *   clasificación por edades  
    *   y mucho más  
        
1.  En el **símbolo del** sistema Paquetes, elija el archivo y los `.msixbundle` que `.classic.appxbundle` generó en la sección [Empaquetar su PWA.](#package-your-pwa-for-the-store)  
    
Después de completar el envío, se revisa la aplicación, normalmente en un plazo de entre 24 y 48 horas.  Después de recibir la aprobación, tu PWA está disponible en Microsoft Store.  

## <a name="see-also"></a>Consulte también  

PWABuilder proporciona más documentación que le ayudará a obtener su PWA en Microsoft Store.  

*   [Probar y enviar el paquete de la aplicación de PWA][GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]  
*   [Publicar un nuevo PWA en la Tienda][GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]  
*   [Actualizar una aplicación de la Tienda existente a un PWA][GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]  
*   [Recomendaciones de imagen para las PWA en la Tienda][GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]  
*   [Explicador de empaquetado de aplicaciones][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]  

<!-- links -->  

[LegalWindowsAgreementsStorePolicies]: /legal/windows/agreements/store-policies "Directivas de Microsoft Store | Microsoft Docs"  

[WindowsUwpPublishAnalytics]: /windows/uwp/publish/analytics "Analizar el rendimiento de la aplicación | Microsoft Docs"  
[WindowsUwpPublishAppScreenshotsImages]: /windows/uwp/publish/app-screenshots-and-images "Capturas de pantalla, imágenes y tráileres de la aplicación | Microsoft Docs"  
[WindowsUwpPublishIndex]: /windows/uwp/publish/index "Publicar aplicaciones y juegos de Windows | Microsoft Docs"  

[MicrosoftPartnerDashboardHome]: https://partner.microsoft.com/dashboard/home "Inicio | Centro de partners de Microsoft"  
[MicrosoftPartnerDashboardWindowsOverview]: https://partner.microsoft.com/dashboard/windows/overview "Recursos para partners | Centro de partners de Microsoft"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Windows Apps | Microsoft Store"  

[WindowsBlogWindowsdeveloperHostedAppModel]: https://blogs.windows.com/windowsdeveloper/hosted-app-model "Hosted App Model | Blog para desarrolladores de Windows"  

[GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/classic-package.md "¿Qué es un paquete clásico? | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/image-recommendations.md "Recomendaciones de imagen para paquetes de PWA de Windows | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/next-steps.md "Pasos siguientes para obtener tu PWA en microsoft store | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/publish-new-app.md "Publicar una nueva aplicación en la tienda | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/update-existing-app.md "Actualizar una aplicación existente en la tienda | GitHub"  

[PwabuilderMain]: https://www.pwabuilder.com "PWABuilder"  
