---
description: Más información sobre cómo APIenables Microsoft Edge para actuar como intermediario entre comerciantes, consumidores y formas de pago de consumidores almacenados en la nube.
title: 'API de solicitud de pago: Guía para desarrolladores'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: 338940ab6f7e6bb04c6d5a8cc6ff0a198e7afbcc
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941851"
---
# API de solicitud de pago (EdgeHTML)  

> [!NOTE]
> En este artículo se describe el flujo de trabajo admitido en la [versión heredada de Microsoft Edge][MicrosoftSupport44533505].  Microsoft Edge \ (cromo \) admite la API de solicitud de pago con una implementación diferente según el proyecto de cromo.  

Las ventas de comercio electrónico continúan creciendo a un ritmo rápido.  Según [eMarketer](https://www.emarketer.com), las ventas digitales de 2018 se preparan para aumentar en un 23% a partir de los niveles medidos en 2013.  A pesar de que los consumidores y las empresas disfrutan de la comodidad de las ventas de comercio electrónico, los desafíos siguen.  Hoy, cada propietario de un sitio web de comercio electrónico debe invertir tiempo para desarrollar los flujos de pago y las reglas de validación de pago de alta calidad.  Los consumidores necesitan navegar por diferentes flujos de pago y volver a introducir la misma información de pago y envío en todos los sitios donde se tiendan.  Esto puede resultar lento y frustrante para los consumidores, lo que lleva a una alta tasa de abandono del carro de la compra y ha disminuido las ventas de comerciantes.  Se abandona el [cálculo](http://baymard.com/lists/cart-abandonment-rate) de los comerciantes entre el 60% y el 70% de los carros de la compra.  

La [API de solicitud de pago](https://w3.org/TR/payment-request) Estandariza el proceso de desprotección de pago.  Esta API requiere menos personalización para los desarrolladores web y proporciona una experiencia más rápida, coherente y, por lo tanto, confusa para los consumidores.  Como los consumidores pueden seleccionar los instrumentos de pago y las direcciones de envío de su cuenta de Microsoft, tienen que introducir menos datos para completar las compras, lo que reduce el tiempo y la entrada de datos necesarios para completar el pago.  

La [API de solicitud de pago](https://w3.org/TR/payment-request) es un estándar entre exploradores abierto que permite que los exploradores actúen como intermediario entre comerciantes, consumidores y las formas de pago \ (como tarjetas de crédito \) que los consumidores hayan almacenado en la nube.  
  
En Resumen, al usar la [API de solicitud de pago](https://w3.org/TR/payment-request), los clientes pueden comprar en sitios web de comerciante de forma normal.  Cuando esté listo para pagar, el sitio web de comerciante llama a la API de **solicitud de pago** para crear una **solicitud de pago** y pasa la información de pago correspondiente \ (como las formas de pago admitidas, la cantidad de compra, la moneda, etc. \) al explorador.  

:::image type="complex" source="../media/payment_request_construct.png" alt-text="Construcción de solicitud de pago" lightbox="../media/payment_request_construct.png":::
   Construcción de solicitud de pago  
:::image-end:::  

El explorador autentica al usuario, permite al usuario seleccionar una forma de pago admitida en un archivo y procesa los detalles de pago.  El explorador vuelve a enviar los detalles de la información de pago al sitio web del comerciante, de modo que el comerciante pueda completar el pago.  Además de recibir información de pago, el comerciante puede optar por recibir la información de envío como parte de la **solicitud de pago**.  

:::image type="complex" source="../media/payment_response_construct.png" alt-text="Construcción de respuesta de pago" lightbox="../media/payment_response_construct.png":::
   Construcción de respuesta de pago  
:::image-end:::  

Para ver la API de solicitud de pago en acción, así como para obtener información general sobre cómo usarla, consulte este vídeo.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]  

> [!NOTE]
> La API de solicitud de pago es compatible con la compilación 14992 o posterior de Microsoft Edge.  

## Crear una solicitud de pago  

Las páginas web crean una **solicitud de pago** generalmente cuando el usuario inicia un proceso de pago haciendo clic en el botón comprar.  El **Payment Request** [constructor](/previous-versions/mt790440(v=vs.85)) de la solicitud de pago incluye methodData, detalles y opciones.  

```javascript
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```  

El parámetro [methodData](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) contiene una lista de las formas de pago y las redes aceptadas por el sitio web y los datos específicos de cualquier método de pago asociado.  En Microsoft Edge, esta lista coincide con las formas de pago admitidas que el comprador ha guardado en su cuenta de Microsoft y da como resultado la lista "pagar con" en la experiencia de usuario de pago.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_with.png" alt-text="La lista pagar con de la experiencia de usuario de Microsoft Wallet" lightbox="../media/pay_with.png":::
         La lista **pagar con** de la experiencia de usuario de Microsoft Wallet  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var supportedInstruments = [{
          supportedMethods: ['basic-card'],
          data: {
              supportedNetworks: ['visa', 'mastercard', 'amex'],
              supportedTypes: ['credit'] 
          }         
      }]; 
      ```  
   :::column-end:::
:::row-end:::  

El parámetro de [detalles](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) contiene información que el comerciante desea transmitir al cliente sobre la transacción.  Estos incluyen elementos de Resumen de pedidos como total, impuestos, cantidad de envío y otros elementos de nivel de resumen que afectan al monto del pago.  No se pretende que se ordenen los artículos de línea.  
  
El parámetro de [detalles](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) también se usa para definir las opciones de envío disponibles para el cliente cuando sea necesario.  A continuación, se incluyen más detalles en la **solicitud de pago** .  

Cada línea de [detalle](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) incluye una etiqueta para la moneda y la cantidad.  

> [!NOTE]
> La **solicitud de pago** no calcula la suma o el total de estas cantidades.  El sitio web del comerciante es responsable de garantizar que el total de los elementos de línea sea correcto.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/show_details.png" alt-text="Subtotal, envío, impuestos y detalles totales" lightbox="../media/show_details.png":::
         Subtotal, envío, impuestos y detalles totales  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
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
   :::column-end:::
:::row-end:::  

[PaymentRequest](/previous-versions/mt790440(v=vs.85)) no admite reembolsos, por lo que los importes deben ser siempre positivos; los elementos individuales de la lista pueden ser negativos, como los descuentos.  

El explorador representará las etiquetas a medida que las define y represente automáticamente el formato de moneda correcto basándose en la configuración regional del cliente.  Tenga en cuenta que las etiquetas se deben representar en el mismo idioma que el contenido.  

El parámetro [Options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) define los datos que la página web desea que se devuelva de la **solicitud de pago**.  Esto también define los datos que es necesario recopilar, incluidos los envíos, la dirección de correo electrónico, el número de teléfono o todos.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/email_snippet.png" alt-text="Lista desplegable de dirección de correo electrónico" lightbox="../media/email_snippet.png":::
         Lista desplegable de dirección de correo electrónico  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var options =
          {
              requestPayerEmail: true
          }; 
      ```  
   :::column-end:::
:::row-end:::  

## Mostrar la solicitud de pago  

La página web llama al método [Show ()](/previous-versions/mt790448(v=vs.85)) para permitir que el usuario interactúe con la interfaz de usuario de **solicitud de pago** .  El método [Show ()](/previous-versions/mt790448(v=vs.85)) devuelve una promesa que se resolverá cuando el usuario autorice la solicitud de pago.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_screen_default.png" alt-text="Confirmar y pagar detalles" lightbox="../media/pay_screen_default.png":::
         Confirmar y pagar detalles  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      paymentRequest.show().then(paymentInstrumentResponse => {
          paymentInstrumentResponse.complete('success').then().catch(error => {
              handlePaymentRequestError(error); 
      });
      ```  
   :::column-end:::
:::row-end:::  

## Anulando una solicitud de pago  
 
La página web puede llamar al método [Abort ()](/previous-versions/mt790437(v=vs.85)) en cualquier momento después de llamar al método [Show ()](/previous-versions/mt790448(v=vs.85)) hasta el punto en el que se resuelve la promesa.  El método [Abort ()](/previous-versions/mt790437(v=vs.85)) hará que el navegador anule la **solicitud de pago** y cierre la interfaz de usuario de la solicitud de **pago** .  Por ejemplo, una página web puede optar por anular si el usuario no completó la transacción en el período de tiempo requerido.  

```javascript
payment.abort();
```  

## Respuesta de pago  
Cuando el cliente apruebe la **solicitud de pago**, se devolverá una **respuesta de pago** al sitio Web.  La **respuesta de pago** incluye lo siguiente:  

 Propiedad      | Descripción | Obligatorio | Información adicional
|---------------|-----------------|-------|-----------------|
[nombreDeMétodo](/previous-versions/mt790656(v=vs.85)) | El identificador de la forma de pago seleccionada por el usuario | Y | |   
[details](/previous-versions/mt790655(v=vs.85)) | Un objeto JSON que incluye todos los datos que el comerciante necesita para procesar la transacción con la forma de pago seleccionada o un token de pago | Y | [Tarjeta básica](https://w3c.github.io/payment-method-basic-card) Diccionario: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress; |   
[shippingAddress](/previous-versions/mt790445(v=vs.85)) | La dirección de envío seleccionada por el usuario  |  Opcional.  Requerido cuando [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) es `True`  | Diccionario de direcciones: país; addressLine; sección urbanas dependentLocality; Código sortingCode; languageCode; Organización remite llamar |  
[shippingOption](/previous-versions/mt790446(v=vs.85)) | El identificador de la opción de envío seleccionada | Opcional.  Requerido cuando [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) es `True`  | |   
[payerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | El nombre proporcionado por el usuario  | Opcional.  Requerido cuando [requestPayerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) es `True` | |  
[payerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | La dirección de correo electrónico seleccionada por el usuario | Opcional.  Requerido cuando [requestPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) es `True`  | |  
[PayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | El número de teléfono seleccionado por el usuario | Opcional.  Requerido cuando [requestPayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) es `True` | |  

El objeto JSON [Details](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) de la **respuesta de pago** contendrá los datos de pago requeridos por el comerciante para procesar un pago.  En su forma más simple, la respuesta será una carga de [tarjeta básica](https://w3c.github.io/payment-method-basic-card) que contenga detalles de tarjetas de pago de texto no cifrado.  En caso de que los comerciantes dispongan de un acuerdo con socios de asistencia y de procesadores adicionales para que puedan prestar asistencia a los pagos, el comerciante puede exigir una carga que el procesador pueda manejar.  Estos pueden tomar la forma de un token de procesador/puerta de enlace o un instrumento de pago cifrado.  Estas formas de pago están fuera del alcance de este documento y se tratarán en la documentación específica para el procesador.  Además, para recibir una respuesta de [tarjeta básica](https://w3c.github.io/payment-method-basic-card) , el desarrollador necesita una incorporación de datos adicional a Microsoft, a diferencia de otras formas de pago específicas del procesador o de la puerta de enlace, que pueden requerir incorporación de claves de cifrado o solicitar autorización \ (OAuth \).  

Al recibir la **respuesta de pago**, el sitio Web envía la información de pago a su procesador de pagos.  El explorador mostrará una página de giro mientras se está procesando el pago.  

:::image type="complex" source="../media/loading_screen.png" alt-text="La página que se muestra cuando se está procesando el pago" lightbox="../media/loading_screen.png":::
   La página que se muestra cuando se está procesando el pago  
:::image-end:::  

Una vez completado el pago, la página web llama al método [Complete ()](/previous-versions/mt790642(v=vs.85)) y pasa el valor **Success** o **failed**.  El método [Complete ()](/previous-versions/mt790642(v=vs.85)) informa al explorador de que la compra ha finalizado y se debe mostrar la pantalla de interfaz de usuario de terminación correspondiente según el valor de **éxito** o **error**.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_complete.png" alt-text="La interfaz de usuario mostrada cuando la compra se realizó correctamente" lightbox="../media/response_payment-request_complete.png":::
         La interfaz de usuario mostrada cuando la compra se realizó correctamente  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_failure.png" alt-text="La interfaz de usuario que se muestra cuando se produjo un error en la compra" lightbox="../media/response_payment-request_failure.png":::
         La interfaz de usuario que se muestra cuando se produjo un error en la compra  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Solicitud de pago con envío  

### Dirección de envío  

Para las ventas que requieren el envío de mercancías físicas, se necesita una dirección de envío.  Para incluir una dirección de envío, establezca `requestShipping = True` el parámetro [Options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) de la solicitud.  

Cuando el usuario seleccione o actualice la dirección de envío, se ejecutará el evento [onshippingaddresschange](/previous-versions/mt790442(v=vs.85)) .  El sitio web, mediante un detector de eventos, tendrá en cuenta el cambio y podrá validar la dirección, calcular de nuevo los gastos de envío y los impuestos, y actualizar [shippingOptions](/previous-versions/mt790440(v=vs.85)) para reflejar los cargos modificados y las opciones de envío disponibles para la dirección seleccionada \ (si corresponde \).  

### Opciones de envío  

Las opciones de envío se pueden presentar al cliente agregando [shippingOptions](/previous-versions/mt790440(v=vs.85)) al parámetro de [detalles](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) .  Se puede establecer un valor predeterminado mediante `selected = True` la configuración de una de las opciones de envío.  
 
Cuando el usuario seleccione o actualice el shippingOptions, se ejecutará el evento [onshippingoptionchange](/previous-versions/mt790436(v=vs.85)) .  El sitio web, mediante un detector de eventos, será consciente del cambio y podrá actualizar el parámetro de [detalles](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) con el monto de envío correcto.  

```javascript
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

[API de solicitud de pago](/previous-versions/mt790447(v=vs.85))  

## Estadístico
[API de solicitud de pago](https://w3.org/TR/payment-request)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "¿Qué es Microsoft Edge heredado?"  
