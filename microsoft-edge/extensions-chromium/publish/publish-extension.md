---
description: Publicar extensiones de Microsoft Edge (cromo) en el almacén de complementos de Microsoft Edge.
title: Publicar la extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: 4f8433e74c0fd6dab3278792b94cf3cbaac05d2c
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015754"
---
# Publicar la extensión  

Después de completar el desarrollo y las pruebas de su extensión, es posible que esté listo para distribuir la extensión con el catálogo de complementos de Microsoft Edge.  Como alternativa, si tienes una extensión de cromo existente que deseas que esté disponible para los usuarios de Microsoft Edge, puedes [migrar tu extensión de cromo existente][PortChromiumExtension] a Microsoft Edge.  

La publicación de la extensión en el catálogo de complementos de Microsoft Edge aumenta el alcance de la extensión y la pone a disposición de los usuarios finales.  En este tema se describe el proceso para enviar su extensión al catálogo de complementos de Microsoft Edge.  

## Antes de comenzar  

En este momento, deberías tener preparado un prototipo de trabajo de tu extensión.  Para obtener información sobre cómo crear una extensión, consulte el [tutorial de introducción][ExtensionsGettingStarted].  

Para publicar su extensión en el sitio web de complementos de Microsoft Edge, debe tener una cuenta de desarrollador activa en el [centro de socios][MicrosoftPartnerCenter].  Para abrir una nueva cuenta de desarrollador y registrarse en el programa de complementos de Microsoft Edge, siga el proceso mencionado en la guía de [registro para desarrolladores][DeveloperRegistration] .  

Crear un archivo zip que represente el paquete de extensión.  El paquete de extensión debe incluir los siguientes archivos.  

*   El manifiesto de la extensión especifica los detalles como el nombre de la extensión, la descripción breve, los permisos y el idioma predeterminado.  
*   Imágenes y otros archivos necesarios para su extensión.  

Los siguientes campos del manifiesto se incluyen automáticamente en los detalles de la descripción de la tienda y no se pueden modificar desde la página de listas de tiendas, que se describe más adelante en este tema.  Asegúrate de que los campos estén rellenados para que coincidan con tu visualización preferida en la página de detalles de la tienda, antes de cargar el paquete al centro de socios.  Para obtener un ejemplo del código necesario para el archivo de manifiesto, revise los conceptos básicos del archivo de manifiesto.  

*   `Name` campo en el archivo de manifiesto, que es el **nombre para mostrar** en la página de detalles de la tienda.  
*   `Description` campo en el archivo de manifiesto, que es la **Descripción breve** de la página de detalles de la tienda.  Proporciona una descripción breve y breve para mostrar en la parte superior de la lista para tu extensión.  Cuando se incluye, la descripción breve especificada en el archivo de manifiesto de la extensión se muestra en la descripción de la tienda.  Si no se incluye una descripción breve en el archivo de manifiesto, se muestran las primeras líneas de la descripción.  Debes proporcionar una breve descripción para evitar repeticiones de contenido en la página de descripción de la tienda.  

## Enviar la extensión al almacén de complementos de Microsoft Edge  

Para enviar su extensión al [centro de Partners][MicrosoftPartnerCenter], siga estos pasos.  

#### Paso 1: iniciar una nueva presentación  

Vaya al [panel del programador][MicrosoftPartnerCenter] y seleccione **crear nueva extensión** en la página **Descripción general** .  

#### Paso 2: cargar el paquete de extensiones  

Use la página **paquetes** para cargar el archivo zip de su paquete de extensión.  Solo puedes cargar un paquete a la vez.  No puedes continuar con el envío si la carga del paquete no se realiza correctamente en la página **paquetes** .  

Cargue el paquete arrastrando el paquete al campo cargar o seleccionando **examinar los archivos**.  Una vez que se cargue el paquete, se validará el paquete.  Una vez que la validación se complete correctamente, revise los detalles de la extensión y, después, haga clic en **siguiente** para continuar.  Si hay errores de validación, solucione los problemas e intente cargar de nuevo.  

#### Paso 3: proporcionar detalles de disponibilidad  

En la página **disponibilidad** , escriba la siguiente información sobre la disponibilidad de la extensión.  

##### Visibilidad  

Elija una de las siguientes opciones de visibilidad para definir si su extensión es reconocible en el catálogo de complementos de Microsoft Edge.  

*   `Public` \ (valor predeterminado \)  
    Público permite que todos los usuarios puedan descubrir las extensiones mediante la búsqueda, navegar en el catálogo de complementos de Microsoft Edge o usar la dirección URL de la lista en el almacén de complementos de Microsoft Edge.  La dirección URL del anuncio está disponible en el panel del centro del Partner en la página **Descripción general** de la extensión.  

*   `Hidden`  
    Oculto quita las extensiones de los resultados de búsqueda o navega en el catálogo de complementos de Microsoft Edge.  Para distribuir las extensiones ocultas en el almacén de complementos de Microsoft Edge, debe compartir la dirección URL de la lista en la extensión con sus clientes.  

> [!NOTE]
> Puedes cambiar la visibilidad de tu extensión de **Public** a **Hidden**.  Los usuarios que instalaron la extensión mientras la visibilidad se estableció como pública mantendrán el acceso a la extensión y recibirán las actualizaciones que haga que estén disponibles a través del sitio web de complementos de Microsoft Edge.  

##### Mercados  

Define los mercados específicos en los que planeas ofrecer tu extensión.  De forma predeterminada, se han seleccionado todos los mercados en los que se han añadido mercados futuros.  También puede elegir mercados específicos seleccionando **cambiar mercados**.  Anule la selección de mercados individuales para excluirlos, o seleccione **anular la selección de todo** y, después, agregue mercados individuales de su elección.  

> [!NOTE]
> Puedes cambiar los mercados en los que se ofrece tu extensión.  Los usuarios que instalaron la extensión mientras estaba disponible en su mercado conservan el acceso a la extensión.  Sin embargo, los usuarios ya no tienen acceso a ninguna actualización futura que se envíe al catálogo de complementos de Microsoft Edge.  

Seleccione **Guardar** para continuar a la sección **propiedades** .  

#### Paso 4: seleccionar las propiedades de la extensión  

En la **Página propiedades**, escriba la siguiente información para especificar las propiedades de la extensión.  Las propiedades se muestran a los usuarios en el catálogo de complementos de Microsoft Edge.  

| Nombre de la propiedad de extensión | Descripción |  
|:--- |:--- |  
| Category \ (requerido \) | La categoría que mejor describe tu extensión.  El listado de tu extensión en la categoría adecuada ayuda a los usuarios a encontrar tu extensión fácilmente y a entender más acerca de ella.  |  
| Requisitos de la política de privacidad \ (requerido \) | Indique si su extensión accede, recopila o transmite cualquier tipo de información personal.  La extensión puede dar error en el paso de certificación si eliges **sí** y no proporcionas un `Privacy policy URL` .  |  
| Dirección URL de la directiva de privacidad | Una dirección URL de política de privacidad válida para comunicar la conformidad de su extensión con las leyes y regulaciones de privacidad.  Usted es responsable de asegurar que su extensión cumpla con las leyes y regulaciones de privacidad, y para proporcionar una dirección URL válida de la política de privacidad, si es necesario.  Proporciona una dirección URL de la política de privacidad Si tu extensión accede, transmite o recopila información personal.  Para determinar si su extensión requiere una política de privacidad, vaya al [contrato para programadores de Microsoft Edge][MicrosoftAppDeveloperAgreement] y [Complementos Microsoft Edge directivas para desarrolladores de catálogos][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  |  
| Dirección URL del sitio web | Una página web que proporciona información adicional sobre la extensión.  El `Website URL` debe apuntar a una página de su propio sitio web, no a la lista de sitios web de la extensión en el catálogo de complementos de Microsoft Edge.  El `Website URL` permite a los usuarios obtener más información sobre su extensión, sus características y cualquier otra información relevante.  |  
| Detalles de contacto de soporte técnico | La dirección URL de su página web de soporte o la dirección de correo electrónico para ponerse en contacto con el equipo de soporte técnico.  |  
| Contenido para adultos | Casilla para especificar si su extensión incluye contenido adulto.  La clasificación de extensión ayuda a determinar el grupo de edad adecuado de la audiencia de destino de la extensión.  Para determinar si su extensión tiene contenido maduro, vaya a [Complementos de catálogo de Microsoft Edge y directivas para programadores de catálogo][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  |  

Seleccione **Guardar** para continuar a la sección de registros de la **tienda** .  

#### Paso 5: agregar detalles de descripción de la tienda para su extensión  

La información proporcionada en la siguiente sección se muestra a los usuarios que visitan su registro en el catálogo de complementos de Microsoft Edge.  Aunque algunos campos son opcionales, debe proporcionar la mayor cantidad de información posible.  Los detalles mínimos necesarios para tu extensión para el registro en la tienda, para cada uno de los idiomas mencionados en tu paquete de extensión, son el logotipo de la **Descripción** y el **almacén de extensiones**.  

> [!NOTE]
> Los detalles de la descripción mínima requerida de la tienda deben completarse para cada idioma mencionado en el paquete zip de extensión.  Para agregar o quitar idiomas en la descripción de la tienda en el catálogo de complementos de Microsoft Edge, debe modificar la lista de idiomas admitidos por la extensión en el paquete de extensiones, crear un nuevo paquete de extensión y volver a cargarlo.  

| Nombre de propiedad de la descripción de la tienda | Descripción |  
|:--- |:--- |  
| Idiomas de la descripción de la tienda \ (requerido \) | Seleccione un idioma en la lista desplegable **idiomas** y escriba los detalles de la descripción de la tienda para ese idioma.  Las extensiones que admiten varios idiomas deben proporcionar una página de descripción de la tienda para cada idioma admitido.  |  
| Nombre para mostrar \ (requerido \) | El nombre de la extensión especificada en el archivo de manifiesto de la extensión.  Para cambiar el nombre para mostrar de la tienda después del envío, puede actualizar el nombre en el archivo de manifiesto, crear un nuevo paquete de extensión y, a continuación, volver a cargarlo.  |  
| Descripción \ (requerido \) | El campo Descripción se centra en explicar qué hace la extensión, por qué los usuarios deben instalarla u otra información relevante que los usuarios necesitan conocer.  Debe tener menos de 10.000 caracteres.  |  
| Logotipo del almacén de extensiones \ (requerido \) | Una imagen que representa el logotipo de su compañía o extensión con una relación de aspecto de 1 y el tamaño recomendado de 300 x 300 píxeles.  |  
| Pequeño mosaico de promociones \ (opcional \) | La `Small promotional tile` imagen se usa para mostrar tu extensión junto con otras extensiones de la tienda.  El tamaño de la imagen debe ser de 440 x 280 píxeles.  |  
| Capturas de pantallas \ (opcional \) | Puedes enviar un máximo de 10 capturas de pantallas que describan la funcionalidad de tu extensión en detalle.  El tamaño de las capturas de pantallas debe ser de 640 x 480 píxeles o de 1280 x 800 píxeles.  |  
| Icono de promoción grande \ (opcional \) | Los mosaicos de promociones grandes se usan en la tienda para destacar las extensiones en el sitio web de complementos de Microsoft Edge.  Las imágenes, si se envían, son visibles para los usuarios.  El tamaño de los archivos PNG debe ser de 1400 x 560 píxeles.  |  
| Dirección URL de vídeo de YouTube \ (opcional \) | Puedes incluir un vídeo de YouTube promocional de tu extensión.  El `YouTube video URL` vídeo se muestra en la página de descripción de la tienda de tu extensión.  |  
| Descripción breve \ (requerido \) | Para editar una descripción breve, debe actualizar el campo de descripción en el archivo de manifiesto del paquete de extensión y volver a cargarla.  |  
| Términos de búsqueda \ (opcional \) | Los términos de búsqueda son frases o palabras únicas que ayudan a los usuarios a descubrir su extensión al buscar en el catálogo de complementos de Microsoft Edge.  Los términos de búsqueda no se muestran a los usuarios.  |  

##### Requisitos de dirección URL de vídeo de YouTube  

Asegúrate de que tu video cumpla con los siguientes requisitos.  

*   Compruebe que el contenido del vídeo de YouTube cumple con el tema [directivas para desarrolladores de catálogos de Microsoft Edge addons][MicrosoftEdgeAddonsCatalogDeveloperPolicies] .  
*   Desactivar los anuncios en el vídeo.  Para obtener más información, vaya a [configurar los formatos de anuncio predeterminados y los][GoogleYoutubeAnswer2531367Topic7072227] [anuncios en vídeos incrustados][GoogleYoutubeAnswer132596].  
*   Activar la incrustación de los vídeos.  Para obtener más información, vaya a [Insertar vídeos & listas de reproducción][GoogleYoutubeAnswer171780].  

Realice los siguientes pasos para enviar la dirección URL de vídeo de YouTube de su vídeo.  

1.  En YouTube, busque el vídeo que desea agregar a la página de descripción de la tienda.  
1.  En el vídeo, elija **compartir**  >  **Embed**.  
1.  Copie el código HTML que se muestra.  
1.  En la página Detalles de descripción de la tienda, pegue el código HTML en el `YouTube video URL` campo.  

##### Requisitos de términos de búsqueda  

Los términos de búsqueda deben cumplir los siguientes requisitos.  

*   Puede escribir términos de búsqueda para usar hasta un máximo de 21 palabras.  Tanto si se usan como palabras, frases o como una combinación de ambas, solo se permiten 21 palabras como máximo.  
*   Hasta un máximo de siete términos de búsqueda: una sola palabra o frases.  Cada término de búsqueda tiene un límite de caracteres de 30 caracteres.  

#### Paso 6: completar el envío  

En la página **enviar la extensión** , agregue notas para la certificación para ayudar a probar la extensión.  

##### Notas para certificación (opcional)  

Al enviar la extensión, use la página **notas para el certificado** para proporcionar información adicional a los evaluadores de certificación.  La información adicional ayuda a garantizar que tu extensión se pruebe correctamente.  Si la extensión no se ha probado por completo, puede dar error de certificación.  

Asegúrese de incluir la siguiente información, según sea necesario.  

*   Nombres de usuario y contraseñas para cuentas de prueba.  
*   Pasos para tener acceso a las características ocultas o bloqueadas.  
*   Se esperaban diferencias en la funcionalidad según la configuración de la región o del usuario.  
*   Si el envío es una actualización de una extensión existente, incluya información sobre los cambios realizados en la extensión.  
*   Cualquier información adicional que los evaluadores deben comprender sobre su envío.  

Después de proporcionar la información, seleccione **publicar** para enviar la extensión al catálogo de complementos de Microsoft Edge.  Tu envío continúa en el paso de certificación.  El proceso de certificación puede demorar hasta siete días hábiles después de su envío.  

Cuando el envío pase la certificación, la extensión se publicará en el catálogo de complementos de Microsoft Edge.  El estado de la extensión en el panel del centro de Partners cambia a `In the Store` .  

> [!NOTE]
> Si estás enfrentando cualquier problema en el proceso de envío o de registro, envíanos [un vale de][ExtensionsSupportForm] soporte técnico o envía un mensaje de correo electrónico a [ext_dev_support@microsoft.com](mailto:ext_dev_support@microsoft.com).  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Introducción a Microsoft Edge (cromo) | Microsoft docs"  
[DeveloperRegistration]: ./create-dev-account.md "Registrarse como desarrollador de Microsoft Edge Extensions | Microsoft docs"  
[PortChromiumExtension]: ../developer-guide/port-chrome-extension.md "Migra tu extensión de cromo a Microsoft Edge | Microsoft docs"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Directivas para desarrolladores de catálogos de Microsoft Edge addons | Microsoft docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Acuerdo de desarrollador de aplicaciones | Microsoft docs"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de socios"  

[ExtensionsSupportForm]: https://support.microsoft.com/supportrequestform/e7a381be-9c9a-fafb-ed76-262bc93fd9e4 "Extensiones nuevas solicitud de asistencia | Soporte técnico de Microsoft"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Establecer los formatos de anuncio predeterminados para la ayuda de YouTube"  

[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anuncios en vídeos insertados: ayuda de YouTube"
[GoogleYoutubeAnswer171780]: https://support.google.com/youtube/answer/171780 "Insertar vídeos & listas de reproducción-ayuda de YouTube"  
