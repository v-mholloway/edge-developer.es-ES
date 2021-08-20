---
description: Referencia de la API de complementos, para que los puntos de conexión rest automaticen las actualizaciones de publicación de los complementos que se envían al sitio web Microsoft Edge complementos.
title: Microsoft Edge Referencia de api de complementos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/19/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador, api de complementos, api de publicación
ms.openlocfilehash: beaeabf21b4502edd029a17c6ae8e550544e0aa6
ms.sourcegitcommit: 1edba4737118613dc63a0846d2049dded2342f87
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "11909368"
---
# <a name="microsoft-edge-add-ons-api-reference-under-development"></a>Microsoft Edge Referencia de API de complementos (en desarrollo)

> [!NOTE]
> Este artículo es una solicitud de comentarios.  La API Microsoft Edge complementos aún no está disponible para pruebas y la página Publicar API aún no está disponible en el Centro de partners.  La API Microsoft Edge complementos está en desarrollo activo y la hoja de ruta sigue evolucionando en función de los cambios del mercado y los comentarios de los clientes.  Los planes descritos aquí no son exhaustivos y están sujetos a cambios.

Esta es la referencia de extremo rest para la API Microsoft Edge complementos.  Esta API automatiza las actualizaciones de publicación de los complementos que se han enviado al sitio web Microsoft Edge complementos.

Para obtener información general, vaya a [Using the Microsoft Edge Add-ons API][UsingAddonsAPI].


<!-- ====================================================================== -->
## <a name="get-the-list-of-products"></a>Obtener la lista de productos

Obtiene una lista de todos los productos que pertenecen a la cuenta.  

### <a name="request"></a>Solicitud

| Método | URI de solicitud |
|---|---|
| `GET` | `/products` |

#### <a name="uri-parameters"></a>Parámetros de URI

Ninguna.

#### <a name="request-headers"></a>Encabezados de solicitud

* Obligatorio.  `Authorization: Bearer <auth token>`

#### <a name="request-body"></a>Cuerpo de la solicitud

Ninguna.

### <a name="response"></a>Respuesta

La respuesta incluye una lista de productos, con detalles para cada producto.  La plantilla para esta respuesta es la siguiente.

```json
[
    {
        "id": "<productID1>",
        "name": "<Name of Product 1>",
        "status": "In review",
        "lastUpdatedDate": "7/19/2021"
    },
    {
        "id": "<productID2>",
        "name": "<Name of Product 2>",
        "status": "In the store",
        "lastUpdatedDate": "5/21/2021"
    }
]
```

Para la primera versión de un producto, el campo de estado tiene los siguientes valores:
*  En borrador
*  En revisión
*  En la Tienda, o Error

Para envíos posteriores, recibirá uno de los siguientes valores:
*  En revisión
*  En la Tienda, o Error

#### <a name="status-codes"></a>Códigos de estado

Esta API tiene los siguientes códigos de estado esperado.

| Código de estado HTTP | Descripción |
|---|---|
| 200 | La solicitud está bien |
| 4XX | Para obtener más información, vea [Códigos de error](#error-codes). |
| 5XX | Para obtener más información, vea [Códigos de error](#error-codes). |


<!-- ====================================================================== -->
## <a name="upload-a-package-to-update-an-existing-submission"></a>Upload un paquete para actualizar un envío existente

Carga un paquete para actualizar un borrador de envío existente de un producto de complemento.

### <a name="request"></a>Solicitud

| Método | URI de solicitud |
|---|---|
| `PUT` | `/products/{productID}/submissions/draft/package` |

#### <a name="uri-parameters"></a>Parámetros de URI

| Parámetro de URI | Descripción |
|---|---|
| `productID` | Obligatorio.  El identificador de producto del producto al que debe cargarse el paquete. |

#### <a name="request-headers"></a>Encabezados de solicitud

*  Obligatorio.  `Authorization: Bearer <auth token>`

*  Obligatorio.  `Content-Type: application/zip`

#### <a name="request-body"></a>Cuerpo de la solicitud

* `<Zip package>`

### <a name="response"></a>Respuesta

#### <a name="response-headers"></a>Encabezados de respuesta

*  Ubicación: `/products/{productID}/submissions/draft/package/operations/{operationID}`

#### <a name="status-codes"></a>Códigos de estado

Esta API tiene los siguientes códigos de estado esperado.

| Código de estado HTTP | Descripción |
|---|---|
| 202 | La solicitud se acepta para el procesamiento, pero el procesamiento no se ha completado. |
| 4XX | Consulte [Códigos de error](#error-codes). |
| 5XX | Consulte [Códigos de error](#error-codes). |


<!-- ====================================================================== -->
## <a name="check-the-status-of-a-package-upload"></a>Comprobar el estado de una carga de paquete

Obtiene el estado de la carga del paquete.

### <a name="request"></a>Solicitud

| Método | URI de solicitud |
|---|---|
| `GET` | `/products/{productID}/submissions/draft/package/operations/{operationID}` |

#### <a name="uri-parameters"></a>Parámetros de URI

| Parámetro de URI | Descripción |
|---|---|
| `operationID` | Obligatorio.  Identificador de operación de la solicitud de carga enviada en el paso anterior.  Esta información está disponible en el encabezado de respuesta.

#### <a name="request-headers"></a>Encabezados de solicitud

* Obligatorio.  `Authorization: Bearer <auth token>`

#### <a name="request-body"></a>Cuerpo de la solicitud

Ninguna.

### <a name="response"></a>Respuesta

Hay varias respuestas para distintos escenarios.

#### <a name="response-when-the-operation-is-still-in-progress"></a>Respuesta cuando la operación todavía está en curso

```json
{
    "id": "{operationID}",
    "status": "IN-PROGRESS",
    "message": "The package upload is in progress. Please check the status after some time."
}
```

#### <a name="response-when-the-operation-succeeds"></a>Respuesta cuando la operación se realiza correctamente

```json
{
    "id": "{operationID}",
    "status": "SUCCESS",
    "message": "Package upload successfully completed. Please proceed with publishing."
}
```

#### <a name="response-when-the-operation-fails-with-errors"></a>Respuesta cuando se produce un error en la operación con errores

```json
{
    "id": "{operationID}",
    "status": "FAILED",
    "message": "The package upload failed. Please fix the errors and make the request again.",
    "errors": [
       {
           "id": "MANIFEST_FILE_MISSING",
           "message": "Zip file must contain a manifest.json file."
       },
       {
           "id": "SIZE_LIMIT_EXCEEDED",
           "message": "Zip file size must not exceed 500MB."
       }
    ]
}
```

#### <a name="response-headers"></a>Encabezados de respuesta

Ninguna.

#### <a name="status-codes"></a>Códigos de estado

Esta API tiene los siguientes códigos de estado esperado.

| Código de estado HTTP | Descripción |
|---|---|
| 200 | La solicitud es correcta. |
| 4XX | Consulte [Códigos de error](#error-codes). |
| 5XX | Consulte [Códigos de error](#error-codes). |


<!-- ====================================================================== -->
## <a name="publish-the-product-draft-submission"></a>Publicar el envío de borrador de producto

Publica el borrador actual del producto en Microsoft Edge complementos.

### <a name="request"></a>Solicitud

| Método | URI de solicitud |
|---|---|
| `POST` | `/products/{productID}/submissions` |

#### <a name="uri-parameters"></a>Parámetros de URI


| Parámetro de URI | Descripción |
|---|---|
| `productID` | Obligatorio.  El identificador de producto del producto cuyo borrador debe publicarse. |

#### <a name="request-headers"></a>Encabezados de solicitud

* Obligatorio.  `Authorization: Bearer <auth token>`

#### <a name="request-body"></a>Cuerpo de la solicitud

`<Notes for certification>`, en formato de texto sin formato.

### <a name="response"></a>Respuesta

#### <a name="response-headers"></a>Encabezados de respuesta

* Ubicación: `/products/{productID}/submissions/operations/{operationID}`

#### <a name="status-codes"></a>Códigos de estado

Esta API tiene los siguientes códigos de estado esperado.

| Código de estado HTTP | Descripción |
|---|---|
| 202 | La solicitud se acepta para el procesamiento, pero el procesamiento no se ha completado. |
| 4XX | Consulte [Códigos de error](#error-codes). |
| 5XX | Consulte [Códigos de error](#error-codes). |


<!-- ====================================================================== -->
## <a name="check-the-publishing-status"></a>Comprobar el estado de publicación

Comprueba el estado de la operación de publicación.

### <a name="request"></a>Solicitud

| Método | URI de solicitud |
|---|---|
| `GET` | `/products/{productID}/submissions/operations/{operationID}` |

#### <a name="uri-parameters"></a>Parámetros de URI

Ninguna.

#### <a name="request-headers"></a>Encabezados de solicitud

* Obligatorio.  `Authorization: Bearer <auth token>`

#### <a name="request-body"></a>Cuerpo de la solicitud

Ninguna.

### <a name="response"></a>Respuesta

Se puede llamar a una API de estado de operación `GET` en los siguientes escenarios.  En todos los escenarios válidos, `200 OK` se devuelve, con mensajes de estado diferentes.

#### <a name="response-when-there-is-nothing-new-to-be-published"></a>Respuesta cuando no hay nada nuevo que publicar

```json
{
    "id": "{operationID}",
    "status": "NOTHING-TO-PUBLISH",
    "message": "There is no draft available to publish. Please update the draft before publishing."
}
```

#### <a name="response-when-there-is-an-in-review-submission-for-the-same-product"></a>Respuesta cuando hay un envío en revisión para el mismo producto

```json
{
    "id": "{operationID}",
    "status": "CONFLICT",
    "message": "There is another in-review submission for this product. Please wait for that submission to be completed before triggering a new publish."
}
```

#### <a name="response-when-the-publish-call-succeeds"></a>Respuesta cuando la llamada de publicación se realiza correctamente

```json
{
    "id": "{operationID}",
    "status": "IN-REVIEW",
    "message": "The draft has been successfully submitted and is in review. The review may take up to 7 business days."
}
```

#### <a name="response-when-the-publish-call-fails-with-an-irrecoverable-failure"></a>Respuesta cuando se produce un error en la llamada de publicación con un error irrecuperable

```json
{
    "id": "{operationID}",
    "status": "FAILED",
    "message": "The operation failed due to an unknown error. Please re-trigger the publish call."
}
```

#### <a name="response-headers"></a>Encabezados de respuesta

Ninguna.

#### <a name="status-codes"></a>Códigos de estado

Esta API tiene los siguientes códigos de estado esperado.

| Código de estado HTTP | Descripción |
|---|---|
| 200 | La solicitud es correcta. |
| 4XX | Consulte [Códigos de error](#error-codes). |
| 5XX | Consulte [Códigos de error](#error-codes). |


<!-- ====================================================================== -->
## <a name="error-codes"></a>Códigos de error

Esta es una lista de códigos de error comunes y posibles razones.  Para obtener una lista completa, vaya a Códigos de [error REST][PartnerCenterErrorCodes] del Centro de partners o Lista de códigos de estado [HTTP][WikipediaListOfStatusCodes].

### <a name="4xx-client-error"></a>4xx: Error de cliente

| Mensaje | Descripción | Escenario de ejemplo |
|---|---|---|
| 400 Solicitud mala | El servidor no comprende la solicitud. | No hay ningún paquete (archivo zip) en el cuerpo.  O bien, `Content-Type` falta el encabezado o su valor es incorrecto. |
| Sin autorización 401 | La página de solicitud necesita una autorización. | Falta el token de autenticación, expira o no es válido. |
| 404 No encontrado | El servidor no puede encontrar la página solicitada. | El especificado o no es válido o no pertenece al desarrollador `productID` `operationID` que realiza la solicitud. |
| Tiempo de espera de solicitud 408 | La solicitud tardó más de lo que el servidor estaba preparado para esperar. | Hubo un tiempo de espera al cargar un paquete. |
| 429 Demasiadas solicitudes | El usuario envió demasiadas solicitudes. | Se enviaron demasiadas solicitudes y se limitaron. |

### <a name="5xx-server-error"></a>5xx: error del servidor

| Mensaje  | Descripción  | Escenario de ejemplo |
|---|---|---|
| Error de servidor interno de 500 | La solicitud no se completó. | El servidor ha cumplido una condición inesperada. |


## <a name="see-also"></a>Vea también

*  [Uso de la API Microsoft Edge complementos][UsingAddonsAPI]


<!-- links -->
[UsingAddonsAPI]: using-addons-api.md "Uso de la API Microsoft Edge complementos | Microsoft Docs"
<!-- external links -->
[PartnerCenterErrorCodes]: /partner-center/develop/error-codes "Códigos de error REST del Centro de partners | Microsoft Docs "
[WikipediaListOfStatusCodes]: https://en.wikipedia.org/wiki/List_of_HTTP_status_codes "Lista de códigos de estado HTTP | Wikipedia"
