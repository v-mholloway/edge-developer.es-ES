---
description: Publicar extensiones de Microsoft Edge (Chromium) en la Tienda de complementos de Microsoft Edge
title: Publicar la extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones de explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: b03a74d1faef914298729020e3c9ca4d465e0443
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327683"
---
# Publicar la extensión  

Después de desarrollar y probar la extensión, estás listo para distribuir la extensión. Usa el catálogo de complementos de Microsoft Edge para distribuir la extensión.  Para liberar la extensión de Chromium existente para los usuarios de Microsoft Edge, vaya a [portabilidad de la extensión de Chromium existente.][PortChromiumExtension]  

Publique la extensión en el catálogo de complementos de Microsoft Edge para aumentar su alcance y que esté disponible para los usuarios de Microsoft Edge.  En este artículo se proporciona el proceso para enviar la extensión al catálogo de complementos de Microsoft Edge.  

## Antes de comenzar  

Debería tener listo un prototipo funcional de la extensión.  Para obtener información sobre cómo crear una extensión, consulte el [tutorial de introducción.][ExtensionsGettingStarted]  

Para publicar la extensión en el catálogo de complementos de Microsoft Edge, usa tu cuenta de desarrollador activa en el [Centro de partners.][MicrosoftPartnerCenter]  Si no tienes una cuenta de desarrollador, crea una nueva cuenta de desarrollador.  Para abrir una nueva cuenta de desarrollador y registrarse en el programa de complementos de Microsoft Edge, vaya al [registro del desarrollador.][DeveloperRegistration]  

Crea un archivo zip que represente el paquete de extensión.  El paquete de extensión debe incluir los siguientes archivos.  

*   El manifiesto de extensión que especifica detalles como el nombre de la extensión, la descripción breve, los permisos y el idioma predeterminado.  
*   Imágenes y otros archivos necesarios para la extensión.  

Los siguientes campos del manifiesto se incluyen automáticamente en los detalles de la descripción de la tienda.  Los campos son de solo lectura en la página **de des listados de la** Tienda.  La página de desecciones de la tienda se describe más adelante en este artículo.  Asegúrate de que los valores de campo coincidan con tu visualización preferida en la página de detalles de la tienda antes de cargar el paquete en el Centro de partners.  Para obtener un ejemplo del código necesario para el archivo de manifiesto, revise los conceptos básicos del archivo de manifiesto.  

*   `Name` en el archivo de manifiesto, que es el **nombre para mostrar en** la página de detalles del almacén.  
*   `Description` en el archivo de manifiesto, que es la **descripción breve** en la página de detalles del almacén.  Proporciona una descripción breve y pegadía para mostrarla en la parte superior de la descripción de la extensión.  Cuando se incluye, la descripción breve especificada en el archivo de manifiesto de extensión se muestra en la descripción de la tienda.  Si no se incluye una descripción breve en el archivo de manifiesto, se muestran las primeras líneas de descripción.  Proporciona una breve descripción para evitar la repetición de contenido en la página de descripción de la tienda.  

## Enviar la extensión a la tienda de complementos de Microsoft Edge  

Para enviar la extensión al [Centro de partners,][MicrosoftPartnerCenter]sigue estos pasos.  

#### Paso 1: Iniciar un nuevo envío  

Vaya al panel [del desarrollador][MicrosoftPartnerCenter] y elija Crear nueva **extensión en** la **página** Información general.  

#### Paso 2: Cargar el paquete de extensión  

Usa la **página** Paquetes para cargar el archivo zip del paquete de extensión.  Solo puedes cargar un paquete a la vez.  No puedes continuar con el envío si la carga del paquete no se realiza correctamente en la **página Paquetes.**  

Para cargar el paquete, elija y arrastre el paquete al campo de carga. También puede elegir Examinar **los archivos.**  Una vez cargado el paquete, el paquete se valida.  Una vez que la validación se realiza correctamente, revise los detalles de la extensión y, a continuación, elija **Siguiente** para continuar.  Si hay errores de validación, resuelva los problemas e intente cargarlo de nuevo.  

#### Paso 3: Proporcionar detalles de disponibilidad  

En la **página** Disponibilidad, escriba la siguiente información sobre la disponibilidad de la extensión.  

##### Visibilidad  

Elige una de las siguientes opciones de visibilidad para definir si la extensión se puede detectar en el catálogo de complementos de Microsoft Edge.  

*   `Public` \(default\)  
    Público permite a todos los usuarios descubrir la extensión a través de la búsqueda, la exploración en el catálogo de complementos de Microsoft Edge o el uso de la dirección URL de la descripción de la extensión en la tienda de complementos de Microsoft Edge.  La dirección URL de descripción está disponible en el panel del Centro de partners en la página Información **general de** la extensión.  
    
*   `Hidden`  
    Oculto quita las extensiones de los resultados de búsqueda o la exploración en el catálogo de complementos de Microsoft Edge.  Para distribuir extensiones ocultas en la tienda de complementos de Microsoft Edge, debes compartir la dirección URL de descripción a la extensión con tus clientes.  
    
> [!NOTE]
> Puede cambiar la visibilidad de la extensión **de Pública** a **Oculta.**  Los usuarios que instalaron la extensión mientras la visibilidad se estableció en pública conservan el acceso a la extensión y reciben las actualizaciones que esté disponible a través del sitio web de complementos de Microsoft Edge.  

##### Mercados  

Define los mercados específicos en los que tienes previsto ofrecer tu extensión.  La configuración predeterminada para los mercados es todos los mercados y eso incluye los mercados futuros que se agregan más adelante.  Para elegir mercados específicos, elija **Cambiar mercados.**  Alterna los mercados individuales para excluir cada uno de ellos o elige Anular la selección **de** todos y, a continuación, agrega mercados individuales de tu elección.  

> [!NOTE]
> Puedes cambiar los mercados en los que se ofrece la extensión.  Un usuario que instala la extensión mientras está disponible en el mercado del usuario conserva el acceso a la extensión.  Sin embargo, el usuario no tiene acceso a ninguna actualización futura enviada al catálogo de complementos de Microsoft Edge.  

Seleccione **Guardar** para continuar en la **sección** Propiedades.  

#### Paso 4: Seleccionar propiedades para la extensión  

En la **página Propiedades,** escriba la siguiente información para especificar las propiedades de la extensión.  Las propiedades se muestran a los usuarios en el catálogo de complementos de Microsoft Edge.  

| Nombre de propiedad de extensión | Descripción |  
|:--- |:--- |  
| Categoría \(obligatorio\) | La categoría que mejor describe la extensión.  Enumerar la extensión en la categoría correcta ayuda a los usuarios a encontrar la extensión fácilmente y comprender más al respecto.  |  
| Requisitos de directiva de privacidad \(obligatorio\) | Indica si la extensión accede, recopila o transmite información personal.  Es posible que la extensión no pase el paso de certificación si elige **Sí** y no proporciona un `Privacy policy URL` archivo .  |  
| Dirección URL de la directiva de privacidad | Una dirección URL de directiva de privacidad válida para comunicar cómo su extensión sigue las leyes y normativas de privacidad.  Usted es responsable de garantizar que la extensión siga las leyes y normativas de privacidad.  También es responsable de proporcionar una dirección URL de directiva de privacidad si su extensión accede, transmite o recopila información personal.  Para determinar si la extensión requiere una directiva de privacidad, vaya al Contrato para desarrolladores de [Microsoft Edge][MicrosoftAppDeveloperAgreement] y a las directivas de desarrollador del catálogo de complementos de [Microsoft Edge.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  |  
| Dirección URL del sitio web | Una página web que proporciona información adicional sobre la extensión.  Debe apuntar a una página en su propio sitio web, no a la lista web de su extensión en el catálogo de complementos `Website URL` de Microsoft Edge.  Ayuda `Website URL` a los usuarios a obtener más información sobre la extensión, sus características y cualquier otra información relevante.  |  
| Detalles de contacto de soporte técnico | La dirección URL de la página web de soporte técnico o la dirección de correo electrónico para ponerse en contacto con el equipo de soporte técnico.  |  
| Contenido de madurez | Casilla para especificar si la extensión incluye contenido para adultos.  La clasificación de extensiones ayuda a determinar el grupo de edad adecuado de la audiencia de destino de la extensión.  Para ayudar a determinar si la extensión tiene contenido de madurez, vaya a las directivas de desarrollador del catálogo de complementos [de Microsoft Edge.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  |  

Selecciona **Guardar para** continuar en la sección de **desecciones de la** Tienda.  

> [!Important]
> El nombre del desarrollador o la organización, la dirección URL del sitio web y los detalles de contacto de soporte técnico que envió durante el registro se muestran a los usuarios en la tienda de complementos de Microsoft Edge.  

#### Paso 5: Agregar detalles de descripción de la Tienda para la extensión  

La información proporcionada en la sección siguiente se muestra a los usuarios que revisan tu descripción en el catálogo de complementos de Microsoft Edge.  Aunque algunos campos son opcionales, debe proporcionar tanta información como sea posible.  Para enumerar la extensión en la tienda, se requieren los siguientes detalles.  

*   **Descripción** de cada idioma del paquete de extensión.  
*   **Logotipo de la Tienda de** extensiones para cada idioma del paquete de extensión.  
    
> [!NOTE]
> Los detalles mínimos necesarios de la descripción de la tienda deben rellenarse para al menos uno de los idiomas mencionados en el paquete zip de extensión.  Para agregar o quitar idiomas en la descripción de la tienda **** en el catálogo de complementos de Microsoft Edge, usa la lista desplegable Agregar un idioma en la página de desecciones **de la** Tienda.  Además, puedes elegir duplicar los activos de un idioma en otros usando el botón de funcionalidad duplicada en la página de detalles del idioma.  

| Nombre de la propiedad de detalles del idioma | Descripción |  
|:--- |:--- |  
| Nombre para mostrar \(required\) | La `name` extensión especificada en el archivo de manifiesto de la extensión.  Para cambiar el nombre para mostrar de la tienda después del envío, puedes actualizar el nombre en el archivo de manifiesto, crear un nuevo paquete de extensión y, a continuación, volver a cargarlo.  |  
| Descripción \(required\) | El campo se centra en explicar lo que hace la extensión, por qué los usuarios deben instalarla u otra información relevante que los usuarios `description` necesitan conocer.  Debe tener menos de 10.000 caracteres.  |  
| Logotipo de la Tienda de extensiones \(required\) | Imagen que representa tu empresa o con una relación de aspecto de 1 y un tamaño recomendado de `extension logo` 300 x 300 píxeles.  Además, puedes elegir copiar el activo de un idioma a todos los demás idiomas con el botón duplicado.  El botón se encuentra después del campo después de cargar el logotipo para el idioma.  |  
| Icono promocional pequeño \(opcional\) | La `Small promotional tile` imagen se usa para mostrar la extensión junto con otras extensiones en la tienda.  El tamaño de la imagen debe ser de 440 x 280 píxeles.  Además, puedes elegir copiar el activo de un idioma a todos los demás idiomas con el botón duplicado.  El botón se encuentra siguiendo el campo después de cargar un icono promocional para el idioma.  |  
| Capturas de pantalla \(optional\) | Puede enviar un máximo de 10 `screenshots` describiendo la funcionalidad de la extensión en detalle.  El tamaño de las capturas de pantalla debe ser de 640 x 480 píxeles o de 1280 x 800 píxeles.  Además, puedes elegir copiar el activo de un idioma a todos los demás idiomas con el botón duplicado.  El botón se encuentra después del campo después de cargar al menos uno para el idioma.|  
| Icono promocional grande \(opcional\) | `Large promotion tiles` se usan en la tienda para tener extensiones más destacadas en el sitio web de complementos de Microsoft Edge.  Las imágenes, si se envían, son visibles para los usuarios.  El tamaño de los archivos PNG debe ser de 1400 x 560 píxeles.  Además, puedes elegir copiar el activo de un idioma a todos los demás idiomas con el botón duplicado.  El botón se encuentra siguiendo el campo después de cargar un icono promocional para el idioma.  |  
| Url de vídeo de YouTube \(opcional\) | Puedes incluir un vídeo promocional de YouTube de tu extensión.  El `YouTube video URL` vídeo se muestra en la página de descripción de la tienda de la extensión.  |  
| Descripción breve \(required\) | Para editar el campo , debe actualizar el campo de descripción en el archivo de manifiesto del paquete de extensión y `short description` volver a cargarlo.  |  
| Términos de búsqueda \(opcional\) | `Search terms` son palabras o frases únicas que ayudan a los usuarios a descubrir la extensión al buscar en el Catálogo de complementos de Microsoft Edge.  Los términos de búsqueda no se muestran a los usuarios.  |  

##### Requisitos de url de vídeo de YouTube  

Asegúrese de que el vídeo cumple los siguientes requisitos.  

*   Compruebe que el contenido del vídeo de YouTube se base en las directivas de desarrollador del catálogo de complementos [de Microsoft Edge.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  
*   Desactiva los anuncios en el vídeo.  Para obtener más información, ve a [Establecer los formatos de anuncios][GoogleYoutubeAnswer2531367Topic7072227] predeterminados y [anuncios en vídeos incrustados.][GoogleYoutubeAnswer132596]  
*   Activa la inserción de los vídeos.  Para obtener más información, vaya a [Insertar vídeos & listas de reproducción.][GoogleYoutubeAnswer171780]  
    
Para enviar la dirección URL de vídeo de YouTube del vídeo, siga estos pasos.  

1.  En YouTube, busca el vídeo que quieras agregar a la página de descripción de la tienda.  
1.  En el vídeo, elija **Compartir**  >  **insertar**.  
1.  Copie el código HTML que se muestra.  
1.  En la página de detalles de la descripción de la tienda, pegue el código HTML en el `YouTube video URL` campo.  
    
##### Requisitos de términos de búsqueda  

Los términos de búsqueda deben cumplir los siguientes requisitos.  

*   Puede escribir términos de búsqueda para usar hasta un máximo de 21 palabras.  Tanto si se usa como palabras individuales, frases o una combinación de ambas, solo se permite un máximo de 21 palabras.  
*   Hasta un máximo de siete términos de búsqueda: una sola palabra o frases.  Cada término de búsqueda tiene un límite de caracteres de 30 caracteres.  
    
#### Paso 6: Completar el envío  

On the **Submit your extension** page, add notes for certification to help test your extension.  

##### Notas para la certificación (opcional)  

Al enviar la extensión, use la **página Notas para** la certificación para proporcionar información adicional a los evaluadores de certificación.  La información adicional ayuda a garantizar que la extensión se prueba correctamente.  Si la extensión no se ha probado completamente, puede que no se pueda realizar la certificación.  

Asegúrese de incluir la siguiente información, según sea necesario.  

*   Nombres de usuario y contraseñas para cuentas de prueba.  
*   Pasos para acceder a características ocultas o bloqueadas.  
*   Se esperaban diferencias en la funcionalidad basada en la región u otra configuración de usuario.  
*   Si el envío es una actualización de una extensión existente, incluye información sobre los cambios realizados en la extensión.  
*   Cualquier información adicional que los evaluadores deben comprender sobre el envío.  

Después de proporcionar la información, elija **Publicar** para enviar la extensión al catálogo de complementos de Microsoft Edge.  El envío continúa con el paso de certificación.  El proceso de certificación puede tardar hasta siete días laborables después del envío.  

Cuando el envío pasa la certificación, la extensión se publica en el catálogo de complementos de Microsoft Edge.  El estado de la extensión en el panel del Centro de partners cambia a `In the Store` .  

> [!NOTE]
> Si se produce algún problema en el proceso de [][ExtensionsSupportForm] envío o [registro,][MailtoExtDevSupportMicrosoftCom]envíe un vale de soporte técnico en La nueva solicitud de soporte técnico de Extensiones o envíe un correo electrónico a ext_dev_support@microsoft.com .  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Introducción a las extensiones de Microsoft Edge (Chromium) | Microsoft Docs"  
[DeveloperRegistration]: ./create-dev-account.md "Regístrate como desarrollador de extensiones de Microsoft Edge | Microsoft Docs"  
[PortChromiumExtension]: ../developer-guide/port-chrome-extension.md "Port your Chromium extension to Microsoft Edge | Microsoft Docs"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Directivas de desarrollador del catálogo de complementos de Microsoft Edge | Microsoft Docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Acuerdo para desarrolladores de aplicaciones | Microsoft Docs"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de partners"  

[ExtensionsSupportForm]: https://support.microsoft.com/supportrequestform/e7a381be-9c9a-fafb-ed76-262bc93fd9e4 "Extensiones Nuevas solicitudes de soporte | Soporte técnico de Microsoft"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Establecer los formatos de anuncio predeterminados | Ayuda de YouTube"  

[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anuncios en vídeos incrustados | Ayuda de YouTube"  
[GoogleYoutubeAnswer171780]: https://support.google.com/youtube/answer/171780 "Insertar vídeos & listas de reproducción | Ayuda de YouTube"  

[MailtoExtDevSupportMicrosoftCom]: mailto:ext_dev_support@microsoft.com "Enviar correo electrónico a ext_dev_support@microsoft.com" 
