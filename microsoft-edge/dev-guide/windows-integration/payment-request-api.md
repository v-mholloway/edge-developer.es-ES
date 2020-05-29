---
description: Más información sobre cómo APIenables Microsoft Edge para actuar como intermediario entre comerciantes, consumidores y formas de pago de consumidores almacenados en la nube.
title: 'Guía de desarrollo: API de solicitud de pago'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: 75c596570a222336a4ba0c371acb8770f97804ee
ms.sourcegitcommit: e690bb4d1cb9e73c93b468c9f55d91ea6fb6c654
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/10/2020
ms.locfileid: "10574946"
---
# API de solicitud de pago

Las ventas de comercio electrónico continúan creciendo a un ritmo rápido. Según [eMarketer](https://www.emarketer.com/), las ventas digitales de 2018 se preparan para aumentar en un 23% a partir de los niveles medidos en 2013.  A pesar de que los consumidores y las empresas disfrutan de la comodidad de las ventas de comercio electrónico, los desafíos siguen.  Hoy, cada propietario de un sitio web de comercio electrónico debe invertir tiempo para desarrollar los flujos de pago y las reglas de validación de pago de alta calidad.  Los consumidores necesitan navegar por diferentes flujos de pago y volver a introducir la misma información de pago y envío en todos los sitios donde se tiendan.  Esto puede resultar lento y frustrante para los consumidores, lo que lleva a una alta tasa de abandono del carro de la compra y ha disminuido las ventas de comerciantes. Se abandona el [cálculo](http://baymard.com/lists/cart-abandonment-rate) de los comerciantes entre el 60% y el 70% de los carros de la compra.      

La [API de solicitud de pago](https://w3.org/TR/payment-request/) Estandariza el proceso de desprotección de pago. Esta API requiere menos personalización para los desarrolladores web y proporciona una experiencia más rápida, coherente y, por lo tanto, confusa para los consumidores.  Como los consumidores pueden seleccionar los instrumentos de pago y las direcciones de envío de su cuenta de Microsoft, tienen que introducir menos datos para completar las compras, lo que reduce el tiempo y la entrada de datos necesarios para completar el pago.   

La [API de solicitud de pago](https://w3.org/TR/payment-request/) es un estándar entre exploradores abierto que permite que los exploradores actúen como intermediario entre comerciantes, consumidores y las formas de pago (por ejemplo, tarjetas de crédito) que los consumidores hayan almacenado en la nube. 
  
En Resumen, al usar la [API de solicitud de pago](https://w3.org/TR/payment-request/), los clientes pueden comprar en sitios web de comerciante de forma normal.  Cuando esté listo para pagar, el sitio web de comerciante llama a la API de **solicitud de pago** para crear una **solicitud de pago** y transmite la información de pago correspondiente (por ejemplo, las formas de pago admitidas, el importe de compra, la moneda, etc.) al explorador.

![Construcción de solicitud de pago](./../media/payment_request_construct.png)

El explorador autentica al usuario, permite al usuario seleccionar una forma de pago admitida en un archivo y procesa los detalles de pago. El explorador vuelve a enviar los detalles de la información de pago al sitio web del comerciante, de modo que el comerciante pueda completar el pago.  Además de recibir información de pago, el comerciante puede optar por recibir la información de envío como parte de la **solicitud de pago**.  

![Construcción de respuesta de pago](./../media/payment_response_construct.png)

Para ver la API de solicitud de pago en acción, así como para obtener información general sobre cómo usarla, consulte este vídeo.

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]


> [!NOTE]
> La API de solicitud de pago es compatible con la compilación de Microsoft Edge 14992 +.


## Crear una solicitud de pago 
Las páginas web crean una **solicitud de pago** generalmente cuando el usuario inicia un proceso de pago haciendo clic en el botón comprar.  El **Payment Request** [constructor](https://msdn.microsoft.com/library/mt790440) de la solicitud de pago incluye methodData, detalles y opciones. 

```js
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```

El [`methodData`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parámetro contiene una lista de las formas de pago y las redes aceptadas por el sitio web y los datos específicos de cualquier método de pago asociado. En Microsoft Edge, esta lista coincide con las formas de pago admitidas que el comprador ha guardado en su cuenta de Microsoft y da como resultado la lista "pagar con" en la experiencia de usuario de pago.

![La lista "paga con" en la experiencia de usuario de Microsoft Wallet](./../media/pay_with.png)

```js
var supportedInstruments = [{
    supportedMethods: ['basic-card'],
    data: {
        supportedNetworks: ['visa', 'mastercard', 'amex'],
        supportedTypes: ['credit'] 
    }         
}]; 
```

El [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parámetro contiene información que el comerciante desea transmitir al cliente sobre la transacción.  Estos incluyen elementos de Resumen de pedidos como total, impuestos, cantidad de envío y otros elementos de nivel de resumen que afectan al monto del pago. No se pretende que se ordenen los artículos de línea. 
  
El [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parámetro también se usa para definir las opciones de envío disponibles para el cliente cuando sea necesario.  A continuación, se incluyen más detalles en la **solicitud de pago** . 

Cada [`detail`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) línea incluye una etiqueta para la moneda y la cantidad.  

> [!NOTE]
> La **solicitud de pago** no calcula la suma o el total de estas cantidades.  El sitio web del comerciante es responsable de garantizar que el total de los elementos de línea sea correcto.   


![Subtotal, envío, impuestos y detalles totales](./../media/show_details.png)

```js
var details = {
    total: {
        label: 'Total (USD)',
        amount: {currency: 'USD', value: '193.98'}
    },
    displayItems: [{
        label: 'Subtotal',
        amount: {currency: 'USD', value: '174.99'}
    }, {
        label: 'Taxes',
        amount: {currency: "USD", value: '18.99'}
    }],
};  
```

[`PaymentRequest`](https://msdn.microsoft.com/library/mt790440)no admite reembolsos, por lo que los importes deben ser siempre positivos; los elementos individuales de la lista pueden ser negativos, como los descuentos. 

El explorador representará las etiquetas a medida que las define y represente automáticamente el formato de moneda correcto basándose en la configuración regional del cliente. Tenga en cuenta que las etiquetas se deben representar en el mismo idioma que el contenido. 

El [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parámetro define los datos que la página web desea que se devuelva de la **solicitud de pago**. Esto también define los datos que es necesario recopilar, incluyendo si el envío, la dirección de correo electrónico o el número de teléfono son obligatorios.

![Lista desplegable de direcciones de correo electrónico](./../media/email_snippet.png)


```js
var options =
    {
        requestPayerEmail: true
    }; 
``` 

## Mostrar la solicitud de pago

La [`show()`](https://msdn.microsoft.com/library/mt790448) Página Web llama al método para permitir que el usuario interactúe con la interfaz de usuario de **solicitud de pago** .  El [`show()`](https://msdn.microsoft.com/library/mt790448) método devuelve una promesa que se resolverá cuando el usuario autorice la solicitud de pago.  

```js
paymentRequest.show().then(paymentInstrumentResponse => {

paymentInstrumentResponse.complete('success').then().catch(error => {
    handlePaymentRequestError(error); 
});
```

![Confirmar y pagar detalles](./../media/pay_screen_default.png)

## Anulando una solicitud de pago
 
La [`abort()`](https://msdn.microsoft.com/library/mt790437) Página Web puede llamar al método en cualquier momento después de que [`show()`](https://msdn.microsoft.com/library/mt790448) se llame al método, hasta el punto donde se resuelva la promesa.  El [`abort()`](https://msdn.microsoft.com/library/mt790437) método hará que el navegador anule la **solicitud de pago** y cierre la interfaz de usuario de la **solicitud de pago** .  Por ejemplo, una página web puede optar por anular si el usuario no completó la transacción en el período de tiempo requerido.

```js
payment.abort();
``` 

## Respuesta de pago
Cuando el cliente apruebe la **solicitud de pago**, se devolverá una **respuesta de pago** al sitio Web. La **respuesta de pago** incluye lo siguiente: 

 Propiedad      | Descripción | Obligatorio | Información adicional
|---------------|-----------------|-------|-----------------|
[`methodName`](https://msdn.microsoft.com/library/mt790656) | El identificador de la forma de pago seleccionada por el usuario | Y | | 
[`details`](https://msdn.microsoft.com/library/mt790655) | Un objeto JSON que incluye todos los datos que el comerciante necesita para procesar la transacción con la forma de pago seleccionada o un token de pago | Y | [Tarjeta básica](https://go.microsoft.com/fwlink/?linkid=834965) Diccionario: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress; | 
[`shippingAddress`](https://msdn.microsoft.com/library/mt790445) | La dirección de envío seleccionada por el usuario  |  Opcional. Obligatorio cuando [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) es **verdadero**  | Diccionario de direcciones: país; addressLine; sección urbanas dependentLocality; Código sortingCode; languageCode; Organización remite llamar |
[`shippingOption`](https://msdn.microsoft.com/library/mt790446) | El identificador de la opción de envío seleccionada | Opcional. Obligatorio cuando [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) es **verdadero**  | | 
[`payerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | El nombre proporcionado por el usuario  | Opcional. Obligatorio cuando [`requestPayerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) es **verdadero** | |
[`payerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | La dirección de correo electrónico seleccionada por el usuario | Opcional. Obligatorio cuando [`requestPayerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) es **verdadero**  | |
[`PayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | El número de teléfono seleccionado por el usuario | Opcional. Obligatorio cuando [`requestPayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) es **verdadero** | |

El [`details`](https://msdn.microsoft.com/library/mt790655#PaymentRequest_params) objeto JSON de la **respuesta de pago** contendrá los datos de pago requeridos por el comerciante para procesar un pago. En su forma más simple, la respuesta será una carga de [tarjeta básica](https://go.microsoft.com/fwlink/?linkid=834965) que contenga detalles de tarjetas de pago de texto no cifrado. En caso de que los comerciantes dispongan de un acuerdo con socios de asistencia y de procesadores adicionales para que puedan prestar asistencia a los pagos, el comerciante puede exigir una carga que el procesador pueda manejar. Estos pueden tomar la forma de un token de procesador/puerta de enlace o un instrumento de pago cifrado. Estas formas de pago están fuera del alcance de este documento y se tratarán en la documentación específica para el procesador. Además, para recibir una respuesta de [tarjeta básica](https://go.microsoft.com/fwlink/?linkid=834965) , el desarrollador necesita una incorporación de datos adicional a Microsoft, a diferencia de otras formas de pago del procesador o de la puerta de enlace que pueden requerir incorporación de claves de cifrado o solicitar autorización (OAuth). 

Al recibir la **respuesta de pago**, el sitio Web envía la información de pago a su procesador de pagos.  El explorador mostrará una página de giro mientras se está procesando el pago.

![La página que se muestra cuando se está procesando el pago](./../media/loading_screen.png)

Una vez completado el pago, la página web llama al [`complete()`](https://msdn.microsoft.com/library/mt790642) método y pasa un valor de **éxito** o **error**.  El [`complete()`](https://msdn.microsoft.com/library/mt790642) método informa al explorador de que la compra ha finalizado y se debe mostrar la pantalla de interfaz de usuario de terminación correspondiente según el valor de **éxito** o **error**. 

![La interfaz de usuario que se muestra cuando la compra ](./../media/response_payment-request_complete.png)
![ se ha realizado correctamente la interfaz de usuario mostrada cuando se produjo un error](./../media/response_payment-request_failure.png)

## Solicitud de pago con envío

### Dirección de envío

Para las ventas que requieren el envío de mercancías físicas, se necesita una dirección de envío.  Para incluir una dirección de envío, establezca `requestShipping = True` el [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parámetro de la solicitud.   

Cuando el usuario seleccione o actualice la dirección de envío, el [`onshippingaddresschange`](https://msdn.microsoft.com/library/mt790442) evento se ejecutará.  El sitio web, mediante un detector de eventos, tendrá en cuenta el cambio y podrá validar la dirección, recalcular los gastos de envío y los impuestos, y actualizar [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) para reflejar los cargos cambiados y las opciones de envío disponibles para la dirección seleccionada (si corresponde). 

### Opciones de envío 

Las opciones de envío se pueden presentar al cliente agregando [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) al [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parámetro.  Se puede establecer un valor predeterminado mediante `selected = True` la configuración de una de las opciones de envío. 
 
Cuando el usuario seleccione o actualice el shippingOptions, [`onshippingoptionchange`](https://msdn.microsoft.com/library/mt790436) se ejecutará el evento.  El sitio web, mediante un detector de eventos, tendrá en cuenta el cambio y podrá actualizar el [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parámetro con el monto de envío correcto.   

```js
var details = {
    total: {
        label: 'Total (USD)',
        amount: {currency: 'USD', value: '193.98'}
    },
    displayItems: [{
         label: 'Subtotal',
         amount: {currency: 'USD', value: '174.99'}
        }, {
            label: 'Shipping',
            amount: {currency: 'USD', value: '0.00'}
        }, {
            label: 'Taxes',
            amount: {currency: "USD", '18.99'}
    }],
    shippingOptions: [{
        id: 'STANDARD',
        label: 'Standard – FREE (5-6 Business days)',
        amount: {currency: 'USD', value: '0.00'},
        selected: true
    }, {
        id: 'EXPEDITED',
        label: 'Two-Day Shipping',
        amount: {currency: 'USD', value: '7.00'}
    }]
};
        
var options = {
    requestShipping: true,
    requestPayerEmail: true
}; 
 
```

## Referencia de API
[API de solicitud de pago](https://msdn.microsoft.com/library/mt790447)

## Estadístico
[API de solicitud de pago](https://w3.org/TR/payment-request/)
