---
description: Extremos rest para automatizar las actualizaciones de publicación de complementos que se envían al sitio web Microsoft Edge complementos.
title: Uso de la API Microsoft Edge complementos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador, api de complementos, api de publicación
ms.openlocfilehash: 83d19d6fdc62153440873ea76e0aae2aadb76fbefcf81b43186b43c4c71262ab
ms.sourcegitcommit: 48101fb3ad5c688ce066e8a64c29fd9cbffdaaab
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/12/2021
ms.locfileid: "11881798"
---
# <a name="using-the-microsoft-edge-add-ons-api"></a>Uso de la API Microsoft Edge complementos

En este artículo, junto con la referencia Microsoft Edge API de complementos, se proporciona información general sobre la [API][AddonsAPIRef]de complementos Microsoft Edge propuesta.  Esperamos sus sugerencias y comentarios sobre los contratos de API propuestos.  Envíe sus comentarios como un [problema sobre la API de complementos][GitHubMicrosoftDocsEdgeDeveloperNewIssue].

La API Microsoft Edge complementos de Microsoft Edge proporciona un conjunto de puntos de conexión rest para publicar actualizaciones mediante programación en complementos enviados al sitio web Microsoft Edge complementos.  Puede usar estos puntos de conexión rest para automatizar el proceso de carga y publicación de complementos en el sitio web Microsoft Edge complementos.

La fecha provisional para la disponibilidad de las API es diciembre de 2021.


<!-- ====================================================================== -->
## <a name="terminology"></a>Terminología

| Término | Definición |
|---|---|
| _operación_ | Una operación REST como GET o PUT. |
| _id. de operación_ | El identificador de una operación REST. |
| _package_ | El `.zip` paquete que contiene los archivos del Microsoft Edge complemento. |
| _producto_ | Una Microsoft Edge o tema.  También se conoce como un Microsoft Edge _complemento_. |
| _Id. de producto_ | El identificador de producto del producto cuyo borrador debe publicarse.  El identificador del producto es un GUID de 32 caracteres asociado a un producto que se envía al Centro de partners.  Por ejemplo: `d34f98f5-f9b7-42b1-bebb-98707202b21d`. |
| _envío_ | Una actualización que se envía a un producto existente en el Centro de partners.  Cada actualización de un producto es un envío, independientemente de si el estado es `In Draft` `In Review` , o `In the Store` (publicado). |


<!-- ====================================================================== -->
## <a name="before-you-begin"></a>Antes de empezar

Para usar la API Microsoft Edge complementos, debe habilitar la API para su proyecto en el Centro de partners de Microsoft.

1. Visita el Centro de partners de Microsoft e inicia sesión en la cuenta desde la que ya has publicado un complemento.

1. En el **Microsoft Edge,** aparece una nueva página para **publicar API.**

1. Seleccione el **botón Crear credenciales de API** para generar las credenciales de la API.  Este paso puede tardar unos minutos.  Una vez habilitadas las API, **** se muestran en esta página el id. de **cliente,** el secreto de cliente y la dirección URL del **token** de autenticación.

1. Tenga en **cuenta clientID,** **Client Secret** y **Auth Token URL**.  Los usarás en el siguiente paso para obtener un token de acceso.


<!-- ====================================================================== -->
## <a name="retrieving-the-access-token"></a>Recuperación del token de acceso

Después de haber adquirido la autorización necesaria para la aplicación, obtenga tokens de acceso para las API.  Para obtener un token con la concesión de credenciales de cliente, envíe una solicitud POST a la dirección URL del token de autenticación.  La información del inquilino está disponible en la dirección URL que recibió en el **antes de comenzar los** pasos anteriores.

```rest
Endpoint: https://login.microsoftonline.com/{tenant}/oauth2/v2.0/token
Type: POST
Header Parameters: Content-Type: application/x-www-form-urlencoded
```

### <a name="sample-request"></a>Solicitud de ejemplo

```console
> curl \
-X POST \
-H "Content-Type: application/x-www-form-urlencoded" \
-d "client_id={$Client_ID}" \
-d "scope=https://addons.edge.microsoft.com/.default" \
-d "client_secret={$Client_Secret}" \
-d "grant_type=client_credentials" \
-v \
https://login.microsoftonline.com/{tenant}/oauth2/v2.0/token
```

### <a name="sample-response"></a>Respuesta de ejemplo

```json
{
  "token_type": "Bearer",
  "expires_in": 3599,
  "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsIng1dCI6Ik1uQ19WWmNBVGZNNXBP..."
}
```

Para obtener más información, vaya a Flujo de credenciales de cliente [de OAuth 2.0 en el Plataforma de identidad de Microsoft][AzureOAuthGetToken].


<!-- ====================================================================== -->
## <a name="using-the-api-endpoints"></a>Uso de los puntos de conexión de la API

Una vez que tenga un token de acceso, puede usar la API Microsoft Edge complementos.  Esta API expone puntos de conexión para obtener una lista de productos, actualizar productos y publicar productos.

> [!NOTE]
> Actualmente, no hay ninguna API para crear un nuevo producto o actualizar los metadatos de un producto, como una descripción.  Debe completar estas tareas manualmente en el Centro de partners de Microsoft.

Los ejemplos siguientes usan el dominio , que es un marcador de posición y puede reemplazarse `https://addons.edge.microsoft.com/api` cuando la API está disponible en producción.


<!-- ====================================================================== -->
## <a name="uploading-a-package-to-update-an-existing-submission"></a>Cargar un paquete para actualizar un envío existente

Use esta API para actualizar el paquete de un complemento.  Esta API carga un paquete para actualizar un borrador de envío existente de un producto de complemento.

```rest
Endpoint: /v1/products/$productID/submissions/draft/package
Type: PUT
Header Parameters: $TOKEN: the access token; Content-Type: application/zip
Body content: the package file to upload
```

`$productID` es el identificador del Microsoft Edge complemento que desea actualizar.  Puede obtener el identificador del producto de cualquiera de las siguientes maneras:

*  Inicie sesión en el Centro de partners de Microsoft.  Vaya a **Microsoft Edge > información general**y, a continuación, seleccione la extensión para la que desea el identificador del producto.  Se abre la página de introducción a la extensión.  El GUID de la dirección URL es el identificador del producto.

*  Llama a `/products` la API para obtener una lista de todos los productos y sus IDs de producto.  Para obtener más información acerca de la `/products` API, vaya [a Obtener la lista de productos](addons-api-reference.md#get-the-list-of-products).

### <a name="sample-request"></a>Solicitud de ejemplo

```console
> curl \
-H "Authorization: Bearer $TOKEN" \
-H "Content-Type: application/zip" \
-X PUT \
-T $FILE_NAME \
-v \
https://addons.edge.microsoft.com/api/v1/products/$productID/submissions/draft/package
```

Si la solicitud se ha hecho correctamente y se inició el proceso de actualización, recibirá un código `202 Accepted` de estado de respuesta con un `Location` encabezado.  Para averiguar el estado de la operación, realice `GET` solicitudes a la dirección URL en el `Location` encabezado.

Referencia de api: [Upload un paquete para actualizar un envío existente](addons-api-reference.md#upload-a-package-to-update-an-existing-submission)


<!-- ====================================================================== -->
## <a name="checking-the-status-of-a-package-upload"></a>Comprobar el estado de una carga de paquete

Use esta API para comprobar el estado de carga del paquete.

```rest
Endpoint: /v1/products/$productID/submissions/draft/package/operations/$operationID
Type: GET
Header Parameters: $TOKEN: the access token
```

### <a name="sample-request"></a>Solicitud de ejemplo

```console
> curl \
-H "Authorization: Bearer $TOKEN" \
-X GET \
-v \
https://addons.edge.microsoft.com/api/v1/products/$productID/submissions/draft/package/operations/$operationID
```

Referencia de api: [comprobar el estado de una carga de paquete](addons-api-reference.md#check-the-status-of-a-package-upload)


<!-- ====================================================================== -->
## <a name="publishing-the-submission"></a>Publicación del envío

Use esta API para publicar el borrador actual del producto en el sitio web Microsoft Edge complementos.

```rest
Endpoint: /v1/products/$productID/submissions
Type: POST
Header Parameters: $TOKEN: the access token
Body content: Notes for certification, in plain text format
```

### <a name="sample-request"></a>Solicitud de ejemplo

```console
> curl \
-H "Authorization: Bearer $TOKEN" \
-X POST \
-d "certificationNotes=text value" \
-v \
https://addons.edge.microsoft.com/api/v1/products/$productID/submissions
```

Si la solicitud se ha hecho correctamente y se inició el proceso de publicación, recibirá un código de estado de respuesta `202 Accepted` con un `Location` encabezado.   Para averiguar el estado de la operación, realice `GET` solicitudes a la dirección URL en el `Location` encabezado.

Referencia de api: [publicar el envío del borrador del producto](addons-api-reference.md#publish-the-product-draft-submission)


<!-- ====================================================================== -->
## <a name="checking-the-publishing-status"></a>Comprobación del estado de publicación

Use esta API para comprobar el estado de la operación de publicación.

```rest
Endpoint: /v1/products/$productID/submissions/operations/$operationID
Type: GET
Header Parameters: $TOKEN: the access token
```

### <a name="sample-request"></a>Solicitud de ejemplo

```console
> curl \
-H "Authorization: Bearer $TOKEN" \
-X GET \
-v \ https://addons.edge.microsoft.com/api/v1/products/$productID/submissions/operations/{operationID}
```

Referencia de api: [comprobar el estado de publicación](addons-api-reference.md#check-the-publishing-status)


<!-- links -->
[AddonsAPIRef]: addons-api-reference.md "Microsoft Edge Referencia de api de complementos | Microsoft Docs"
<!-- external links -->
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[Add-ons%20API] "Escriba comentarios sobre la API de complementos - MicrosoftDocs/edge-developer - GitHub"
[AzureOAuthGetToken]: /azure/active-directory/develop/v2-oauth2-client-creds-grant-flow#get-a-token "Flujo de credenciales de cliente de OAuth 2.0 en el Plataforma de identidad de Microsoft | Microsoft Docs"
