---
description: Más información sobre cómo APIenables Microsoft Edge para actuar como intermediario entre comerciantes, consumidores y formas de pago de consumidores almacenados en la nube.
title: 'Guía de desarrollo: API de solicitud de pago'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/30/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: b082e311dcbe5cff3101f084e7ff2c145e6e83df
ms.sourcegitcommit: 19ef1422733ef1fd051d2b4f0263ce191e8d67bc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/31/2020
ms.locfileid: "10902867"
---
# <span data-ttu-id="627fa-104">API de solicitud de pago (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="627fa-104">Payment Request API (EdgeHTML)</span></span>

> [!NOTE]
> <span data-ttu-id="627fa-105">En este artículo se describe el flujo de trabajo admitido en la [versión heredada de Microsoft Edge][MicrosoftSupport44533505].</span><span class="sxs-lookup"><span data-stu-id="627fa-105">This article describes the workflow supported in the [legacy version of Microsoft Edge][MicrosoftSupport44533505].</span></span>  <span data-ttu-id="627fa-106">Microsoft Edge \ (cromo \) admite la API de solicitud de pago con una implementación diferente según el proyecto de cromo.</span><span class="sxs-lookup"><span data-stu-id="627fa-106">Microsoft Edge \(Chromium\) supports the Payment Request API with a different implementation based on the Chromium project.</span></span>  

<span data-ttu-id="627fa-107">Las ventas de comercio electrónico continúan creciendo a un ritmo rápido.</span><span class="sxs-lookup"><span data-stu-id="627fa-107">E-commerce sales continue growing at a rapid pace.</span></span> <span data-ttu-id="627fa-108">Según [eMarketer](https://www.emarketer.com/), las ventas digitales de 2018 se preparan para aumentar en un 23% a partir de los niveles medidos en 2013.</span><span class="sxs-lookup"><span data-stu-id="627fa-108">According to [eMarketer](https://www.emarketer.com/), by 2018 digital sales are forecasted to increase by 23% from the levels measured in 2013.</span></span>  <span data-ttu-id="627fa-109">A pesar de que los consumidores y las empresas disfrutan de la comodidad de las ventas de comercio electrónico, los desafíos siguen.</span><span class="sxs-lookup"><span data-stu-id="627fa-109">While consumers and businesses enjoy the convenience of e-commerce sales, challenges remain.</span></span>  <span data-ttu-id="627fa-110">Hoy, cada propietario de un sitio web de comercio electrónico debe invertir tiempo para desarrollar los flujos de pago y las reglas de validación de pago de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="627fa-110">Today each e-commerce website owner needs to invest time to develop high quality payment checkout flows and validation rules.</span></span>  <span data-ttu-id="627fa-111">Los consumidores necesitan navegar por diferentes flujos de pago y volver a introducir la misma información de pago y envío en todos los sitios donde se tiendan.</span><span class="sxs-lookup"><span data-stu-id="627fa-111">Consumers need to navigate different payment checkout flows and re-enter the same payment and shipping information on every site where they shop.</span></span>  <span data-ttu-id="627fa-112">Esto puede resultar lento y frustrante para los consumidores, lo que lleva a una alta tasa de abandono del carro de la compra y ha disminuido las ventas de comerciantes.</span><span class="sxs-lookup"><span data-stu-id="627fa-112">This can be time consuming and frustrating for consumers, leading to a high rate of shopping cart abandonment and decreased sales for merchants.</span></span> <span data-ttu-id="627fa-113">Se abandona el [cálculo](http://baymard.com/lists/cart-abandonment-rate) de los comerciantes entre el 60% y el 70% de los carros de la compra.</span><span class="sxs-lookup"><span data-stu-id="627fa-113">Merchants [estimate](http://baymard.com/lists/cart-abandonment-rate) between 60% and 70% of shopping carts are abandoned.</span></span>      

<span data-ttu-id="627fa-114">La [API de solicitud de pago](https://w3.org/TR/payment-request/) Estandariza el proceso de desprotección de pago.</span><span class="sxs-lookup"><span data-stu-id="627fa-114">The [Payment Request API](https://w3.org/TR/payment-request/) standardizes the payment checkout process.</span></span> <span data-ttu-id="627fa-115">Esta API requiere menos personalización para los desarrolladores web y proporciona una experiencia más rápida, coherente y, por lo tanto, confusa para los consumidores.</span><span class="sxs-lookup"><span data-stu-id="627fa-115">This API requires less customization for web developers and provides a faster, more consistent, and therefore, less confusing experience for consumers.</span></span>  <span data-ttu-id="627fa-116">Como los consumidores pueden seleccionar los instrumentos de pago y las direcciones de envío de su cuenta de Microsoft, tienen que introducir menos datos para completar las compras, lo que reduce el tiempo y la entrada de datos necesarios para completar el pago.</span><span class="sxs-lookup"><span data-stu-id="627fa-116">Because consumers can select payment instruments and shipping addresses from their Microsoft account, they are required to enter less data to complete purchases which reduces the time and data entry required to complete a payment.</span></span>   

<span data-ttu-id="627fa-117">La [API de solicitud de pago](https://w3.org/TR/payment-request/) es un estándar entre exploradores abierto que permite que los exploradores actúen como intermediario entre comerciantes, consumidores y las formas de pago (por ejemplo, tarjetas de crédito) que los consumidores hayan almacenado en la nube.</span><span class="sxs-lookup"><span data-stu-id="627fa-117">The [Payment Request API](https://w3.org/TR/payment-request/) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and the payment methods (e.g. credit cards) that consumers have stored in the cloud.</span></span> 
  
<span data-ttu-id="627fa-118">En Resumen, al usar la [API de solicitud de pago](https://w3.org/TR/payment-request/), los clientes pueden comprar en sitios web de comerciante de forma normal.</span><span class="sxs-lookup"><span data-stu-id="627fa-118">In summary, when using the [Payment Request API](https://w3.org/TR/payment-request/), customers shop on merchant websites as normal.</span></span>  <span data-ttu-id="627fa-119">Cuando esté listo para pagar, el sitio web de comerciante llama a la API de **solicitud de pago** para crear una **solicitud de pago** y transmite la información de pago correspondiente (por ejemplo, las formas de pago admitidas, el importe de compra, la moneda, etc.) al explorador.</span><span class="sxs-lookup"><span data-stu-id="627fa-119">When ready to pay, the merchant website calls the **Payment Request** API to create a **Payment Request** and passes the relevant payment information (e.g. supported payment methods, purchase amount, currency, etc.) to the browser.</span></span>

![Construcción de solicitud de pago](./../media/payment_request_construct.png)

<span data-ttu-id="627fa-121">El explorador autentica al usuario, permite al usuario seleccionar una forma de pago admitida en un archivo y procesa los detalles de pago.</span><span class="sxs-lookup"><span data-stu-id="627fa-121">The browser authenticates the user, enables the user to select a supported payment method on file, and processes the payment details.</span></span> <span data-ttu-id="627fa-122">El explorador vuelve a enviar los detalles de la información de pago al sitio web del comerciante, de modo que el comerciante pueda completar el pago.</span><span class="sxs-lookup"><span data-stu-id="627fa-122">The browser then sends the payment information details back to the merchant website, so that the merchant can complete the payment.</span></span>  <span data-ttu-id="627fa-123">Además de recibir información de pago, el comerciante puede optar por recibir la información de envío como parte de la **solicitud de pago**.</span><span class="sxs-lookup"><span data-stu-id="627fa-123">In addition to receiving payment information, the merchant can also elect to receive shipping information as part of the **Payment Request**.</span></span>  

![Construcción de respuesta de pago](./../media/payment_response_construct.png)

<span data-ttu-id="627fa-125">Para ver la API de solicitud de pago en acción, así como para obtener información general sobre cómo usarla, consulte este vídeo.</span><span class="sxs-lookup"><span data-stu-id="627fa-125">To see the Payment Request API in action, as well as get an overview of how to use it, check out this video.</span></span>

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]


> [!NOTE]
> <span data-ttu-id="627fa-126">La API de solicitud de pago es compatible con la compilación de Microsoft Edge 14992 +.</span><span class="sxs-lookup"><span data-stu-id="627fa-126">The Payment Request API is supported in Microsoft Edge build 14992+.</span></span>


## <span data-ttu-id="627fa-127">Crear una solicitud de pago</span><span class="sxs-lookup"><span data-stu-id="627fa-127">Creating a Payment Request</span></span> 
<span data-ttu-id="627fa-128">Las páginas web crean una **solicitud de pago** generalmente cuando el usuario inicia un proceso de pago haciendo clic en el botón comprar.</span><span class="sxs-lookup"><span data-stu-id="627fa-128">Web pages create a **Payment Request** typically when the user initiates a payment process by clicking a "buy" button.</span></span>  <span data-ttu-id="627fa-129">El **Payment Request** [constructor](https://msdn.microsoft.com/library/mt790440) de la solicitud de pago incluye methodData, detalles y opciones.</span><span class="sxs-lookup"><span data-stu-id="627fa-129">The **Payment Request** [constructor](https://msdn.microsoft.com/library/mt790440) includes methodData, details, and options.</span></span> 

```js
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```

<span data-ttu-id="627fa-130">El [`methodData`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parámetro contiene una lista de las formas de pago y las redes aceptadas por el sitio web y los datos específicos de cualquier método de pago asociado.</span><span class="sxs-lookup"><span data-stu-id="627fa-130">The [`methodData`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter contains a list of the payment methods and networks accepted by the website and any associated payment method specific data.</span></span> <span data-ttu-id="627fa-131">En Microsoft Edge, esta lista coincide con las formas de pago admitidas que el comprador ha guardado en su cuenta de Microsoft y da como resultado la lista "pagar con" en la experiencia de usuario de pago.</span><span class="sxs-lookup"><span data-stu-id="627fa-131">In Microsoft Edge, this list is matched with the supported payment methods that the shopper has saved in their Microsoft account and results in the "pay with" list in the payment user experience.</span></span>

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

<span data-ttu-id="627fa-133">El [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parámetro contiene información que el comerciante desea transmitir al cliente sobre la transacción.</span><span class="sxs-lookup"><span data-stu-id="627fa-133">The [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter contains information that the merchant wishes to convey to the customer about the transaction.</span></span>  <span data-ttu-id="627fa-134">Estos incluyen elementos de Resumen de pedidos como total, impuestos, cantidad de envío y otros elementos de nivel de resumen que afectan al monto del pago.</span><span class="sxs-lookup"><span data-stu-id="627fa-134">These include order summary items like total, tax, shipping amount, and other summary level items impacting the payment amount.</span></span> <span data-ttu-id="627fa-135">No se pretende que se ordenen los artículos de línea.</span><span class="sxs-lookup"><span data-stu-id="627fa-135">These are not intended to be order line items.</span></span> 
  
<span data-ttu-id="627fa-136">El [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parámetro también se usa para definir las opciones de envío disponibles para el cliente cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="627fa-136">The [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter is also used to define shipping options available to the customer when required.</span></span>  <span data-ttu-id="627fa-137">A continuación, se incluyen más detalles en la **solicitud de pago** .</span><span class="sxs-lookup"><span data-stu-id="627fa-137">More details are included in the **Payment Request** with Shipping section below.</span></span> 

<span data-ttu-id="627fa-138">Cada [`detail`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) línea incluye una etiqueta para la moneda y la cantidad.</span><span class="sxs-lookup"><span data-stu-id="627fa-138">Each [`detail`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) line includes a label for the currency and the amount.</span></span>  

> [!NOTE]
> <span data-ttu-id="627fa-139">La **solicitud de pago** no calcula la suma o el total de estas cantidades.</span><span class="sxs-lookup"><span data-stu-id="627fa-139">The **Payment Request** does not calculate the sum or total of these amounts.</span></span>  <span data-ttu-id="627fa-140">El sitio web del comerciante es responsable de garantizar que el total de los elementos de línea sea correcto.</span><span class="sxs-lookup"><span data-stu-id="627fa-140">It is the responsibility of the merchant's website to ensure that the line items total correctly.</span></span>   


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

<span data-ttu-id="627fa-142">[`PaymentRequest`](https://msdn.microsoft.com/library/mt790440)no admite reembolsos, por lo que los importes deben ser siempre positivos; los elementos individuales de la lista pueden ser negativos, como los descuentos.</span><span class="sxs-lookup"><span data-stu-id="627fa-142">[`PaymentRequest`](https://msdn.microsoft.com/library/mt790440) does not support refunds, so the amounts should always be positive; individual list items can be negative, such as discounts.</span></span> 

<span data-ttu-id="627fa-143">El explorador representará las etiquetas a medida que las define y represente automáticamente el formato de moneda correcto basándose en la configuración regional del cliente.</span><span class="sxs-lookup"><span data-stu-id="627fa-143">The browser will render the labels as you define them and automatically render the correct currency formatting based on the customer's locale.</span></span> <span data-ttu-id="627fa-144">Tenga en cuenta que las etiquetas se deben representar en el mismo idioma que el contenido.</span><span class="sxs-lookup"><span data-stu-id="627fa-144">Note that the labels should be rendered in the same language as your content.</span></span> 

<span data-ttu-id="627fa-145">El [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parámetro define los datos que la página web desea que se devuelva de la **solicitud de pago**.</span><span class="sxs-lookup"><span data-stu-id="627fa-145">The [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter defines data the web page wants returned from the **Payment Request**.</span></span> <span data-ttu-id="627fa-146">Esto también define los datos que es necesario recopilar, incluyendo si el envío, la dirección de correo electrónico o el número de teléfono son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="627fa-146">This also defines the data that needs to be collected, including if shipping, email address, and/or phone number are required.</span></span>

![Lista desplegable de direcciones de correo electrónico](./../media/email_snippet.png)


```js
var options =
    {
        requestPayerEmail: true
    }; 
``` 

## <span data-ttu-id="627fa-148">Mostrar la solicitud de pago</span><span class="sxs-lookup"><span data-stu-id="627fa-148">Showing the Payment Request</span></span>

<span data-ttu-id="627fa-149">La [`show()`](https://msdn.microsoft.com/library/mt790448) Página Web llama al método para permitir que el usuario interactúe con la interfaz de usuario de **solicitud de pago** .</span><span class="sxs-lookup"><span data-stu-id="627fa-149">The [`show()`](https://msdn.microsoft.com/library/mt790448) method is called by the web page to allow the user to interact with the **Payment Request** user interface.</span></span>  <span data-ttu-id="627fa-150">El [`show()`](https://msdn.microsoft.com/library/mt790448) método devuelve una promesa que se resolverá cuando el usuario autorice la solicitud de pago.</span><span class="sxs-lookup"><span data-stu-id="627fa-150">The [`show()`](https://msdn.microsoft.com/library/mt790448) method returns a Promise that will be resolved when the user authorizes the payment request.</span></span>  

```js
paymentRequest.show().then(paymentInstrumentResponse => {

paymentInstrumentResponse.complete('success').then().catch(error => {
    handlePaymentRequestError(error); 
});
```

![Confirmar y pagar detalles](./../media/pay_screen_default.png)

## <span data-ttu-id="627fa-152">Anulando una solicitud de pago</span><span class="sxs-lookup"><span data-stu-id="627fa-152">Aborting a Payment Request</span></span>
 
<span data-ttu-id="627fa-153">La [`abort()`](https://msdn.microsoft.com/library/mt790437) Página Web puede llamar al método en cualquier momento después de que [`show()`](https://msdn.microsoft.com/library/mt790448) se llame al método, hasta el punto donde se resuelva la promesa.</span><span class="sxs-lookup"><span data-stu-id="627fa-153">The [`abort()`](https://msdn.microsoft.com/library/mt790437) method can be called by the web page any time after the [`show()`](https://msdn.microsoft.com/library/mt790448) method is called, up until the point where the Promise is resolved.</span></span>  <span data-ttu-id="627fa-154">El [`abort()`](https://msdn.microsoft.com/library/mt790437) método hará que el navegador anule la **solicitud de pago** y cierre la interfaz de usuario de la **solicitud de pago** .</span><span class="sxs-lookup"><span data-stu-id="627fa-154">The [`abort()`](https://msdn.microsoft.com/library/mt790437) method will cause the browser to abort the **Payment Request** and close the **Payment Request** user interface.</span></span>  <span data-ttu-id="627fa-155">Por ejemplo, una página web puede optar por anular si el usuario no completó la transacción en el período de tiempo requerido.</span><span class="sxs-lookup"><span data-stu-id="627fa-155">For example, a web page may choose to abort if the user did not complete the transaction in the required amount of time.</span></span>

```js
payment.abort();
``` 

## <span data-ttu-id="627fa-156">Respuesta de pago</span><span class="sxs-lookup"><span data-stu-id="627fa-156">Payment Response</span></span>
<span data-ttu-id="627fa-157">Cuando el cliente apruebe la **solicitud de pago**, se devolverá una **respuesta de pago** al sitio Web.</span><span class="sxs-lookup"><span data-stu-id="627fa-157">When the customer approves the **Payment Request**, a **Payment Response** is returned to the website.</span></span> <span data-ttu-id="627fa-158">La **respuesta de pago** incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="627fa-158">The **Payment Response** includes the following:</span></span> 

 <span data-ttu-id="627fa-159">Propiedad</span><span class="sxs-lookup"><span data-stu-id="627fa-159">Property</span></span>      | <span data-ttu-id="627fa-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="627fa-160">Description</span></span> | <span data-ttu-id="627fa-161">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="627fa-161">Required</span></span> | <span data-ttu-id="627fa-162">Información adicional</span><span class="sxs-lookup"><span data-stu-id="627fa-162">Additional Info</span></span>
|---------------|-----------------|-------|-----------------|
[`methodName`](https://msdn.microsoft.com/library/mt790656) | <span data-ttu-id="627fa-163">El identificador de la forma de pago seleccionada por el usuario</span><span class="sxs-lookup"><span data-stu-id="627fa-163">The ID for the payment method selected by the user</span></span> | <span data-ttu-id="627fa-164">Y</span><span class="sxs-lookup"><span data-stu-id="627fa-164">Y</span></span> | | 
[`details`](https://msdn.microsoft.com/library/mt790655) | <span data-ttu-id="627fa-165">Un objeto JSON que incluye todos los datos que el comerciante necesita para procesar la transacción con la forma de pago seleccionada o un token de pago</span><span class="sxs-lookup"><span data-stu-id="627fa-165">A JSON object that includes all of the data the merchant requires to process the transaction using the selected payment method or a payment token</span></span> | <span data-ttu-id="627fa-166">Y</span><span class="sxs-lookup"><span data-stu-id="627fa-166">Y</span></span> | <span data-ttu-id="627fa-167">[Tarjeta básica](https://go.microsoft.com/fwlink/?linkid=834965) Diccionario: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span><span class="sxs-lookup"><span data-stu-id="627fa-167">[Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) Dictionary: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span></span> | 
[`shippingAddress`](https://msdn.microsoft.com/library/mt790445) | <span data-ttu-id="627fa-168">La dirección de envío seleccionada por el usuario</span><span class="sxs-lookup"><span data-stu-id="627fa-168">The shipping address selected by the user</span></span>  |  <span data-ttu-id="627fa-169">Opcional.</span><span class="sxs-lookup"><span data-stu-id="627fa-169">Optional.</span></span> <span data-ttu-id="627fa-170">Obligatorio cuando [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) es **verdadero**</span><span class="sxs-lookup"><span data-stu-id="627fa-170">Required when [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | <span data-ttu-id="627fa-171">Diccionario de direcciones: país; addressLine; sección urbanas dependentLocality; Código sortingCode; languageCode; Organización remite llamar</span><span class="sxs-lookup"><span data-stu-id="627fa-171">Address dictionary: country; addressLine; region; city; dependentLocality; postalCode; sortingCode; languageCode; organization; recipient; phone</span></span> |
[`shippingOption`](https://msdn.microsoft.com/library/mt790446) | <span data-ttu-id="627fa-172">El identificador de la opción de envío seleccionada</span><span class="sxs-lookup"><span data-stu-id="627fa-172">The ID for the selected shipping option</span></span> | <span data-ttu-id="627fa-173">Opcional.</span><span class="sxs-lookup"><span data-stu-id="627fa-173">Optional.</span></span> <span data-ttu-id="627fa-174">Obligatorio cuando [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) es **verdadero**</span><span class="sxs-lookup"><span data-stu-id="627fa-174">Required when [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | | 
[`payerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="627fa-175">El nombre proporcionado por el usuario</span><span class="sxs-lookup"><span data-stu-id="627fa-175">The name provided by the user</span></span>  | <span data-ttu-id="627fa-176">Opcional.</span><span class="sxs-lookup"><span data-stu-id="627fa-176">Optional.</span></span> <span data-ttu-id="627fa-177">Obligatorio cuando [`requestPayerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) es **verdadero**</span><span class="sxs-lookup"><span data-stu-id="627fa-177">Required when [`requestPayerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span> | |
[`payerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="627fa-178">La dirección de correo electrónico seleccionada por el usuario</span><span class="sxs-lookup"><span data-stu-id="627fa-178">The email address selected by the user</span></span> | <span data-ttu-id="627fa-179">Opcional.</span><span class="sxs-lookup"><span data-stu-id="627fa-179">Optional.</span></span> <span data-ttu-id="627fa-180">Obligatorio cuando [`requestPayerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) es **verdadero**</span><span class="sxs-lookup"><span data-stu-id="627fa-180">Required when [`requestPayerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | |
[`PayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="627fa-181">El número de teléfono seleccionado por el usuario</span><span class="sxs-lookup"><span data-stu-id="627fa-181">The phone number selected by the user</span></span> | <span data-ttu-id="627fa-182">Opcional.</span><span class="sxs-lookup"><span data-stu-id="627fa-182">Optional.</span></span> <span data-ttu-id="627fa-183">Obligatorio cuando [`requestPayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) es **verdadero**</span><span class="sxs-lookup"><span data-stu-id="627fa-183">Required when [`requestPayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span> | |

<span data-ttu-id="627fa-184">El [`details`](https://msdn.microsoft.com/library/mt790655#PaymentRequest_params) objeto JSON de la **respuesta de pago** contendrá los datos de pago requeridos por el comerciante para procesar un pago.</span><span class="sxs-lookup"><span data-stu-id="627fa-184">The [`details`](https://msdn.microsoft.com/library/mt790655#PaymentRequest_params) JSON object in the **Payment Response** will contain the payment data required by the merchant to process a payment.</span></span> <span data-ttu-id="627fa-185">En su forma más simple, la respuesta será una carga de [tarjeta básica](https://go.microsoft.com/fwlink/?linkid=834965) que contenga detalles de tarjetas de pago de texto no cifrado.</span><span class="sxs-lookup"><span data-stu-id="627fa-185">In its simplest form, the response will be a [Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) payload containing cleartext payment card details.</span></span> <span data-ttu-id="627fa-186">En caso de que los comerciantes dispongan de un acuerdo con socios de asistencia y de procesadores adicionales para que puedan prestar asistencia a los pagos, el comerciante puede exigir una carga que el procesador pueda manejar.</span><span class="sxs-lookup"><span data-stu-id="627fa-186">Where merchants have arrangements with additional gateway/processor partners for them to provide payments support, the merchant may require a payload the processor can handle.</span></span> <span data-ttu-id="627fa-187">Estos pueden tomar la forma de un token de procesador/puerta de enlace o un instrumento de pago cifrado.</span><span class="sxs-lookup"><span data-stu-id="627fa-187">These can take the shape of a processor/gateway token or an encrypted payment instrument.</span></span> <span data-ttu-id="627fa-188">Estas formas de pago están fuera del alcance de este documento y se tratarán en la documentación específica para el procesador.</span><span class="sxs-lookup"><span data-stu-id="627fa-188">These payment methods are outside the scope of this document and will be covered in documentation specific to the processor.</span></span> <span data-ttu-id="627fa-189">Además, para recibir una respuesta de [tarjeta básica](https://go.microsoft.com/fwlink/?linkid=834965) , el desarrollador necesita una incorporación de datos adicional a Microsoft, a diferencia de otras formas de pago del procesador o de la puerta de enlace que pueden requerir incorporación de claves de cifrado o solicitar autorización (OAuth).</span><span class="sxs-lookup"><span data-stu-id="627fa-189">Additionally, to receive a [Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) response, no additional onboarding to Microsoft is required by the developer, unlike other processor/gateway specific payment methods which may require encryption key onboarding or request authorization (oauth).</span></span> 

<span data-ttu-id="627fa-190">Al recibir la **respuesta de pago**, el sitio Web envía la información de pago a su procesador de pagos.</span><span class="sxs-lookup"><span data-stu-id="627fa-190">Upon receiving the **Payment Response**, the website submits the payment information to their payment processor.</span></span>  <span data-ttu-id="627fa-191">El explorador mostrará una página de giro mientras se está procesando el pago.</span><span class="sxs-lookup"><span data-stu-id="627fa-191">The browser will display a spinner page while the payment is being processed.</span></span>

![La página que se muestra cuando se está procesando el pago](./../media/loading_screen.png)

<span data-ttu-id="627fa-193">Una vez completado el pago, la página web llama al [`complete()`](https://msdn.microsoft.com/library/mt790642) método y pasa un valor de **éxito** o **error**.</span><span class="sxs-lookup"><span data-stu-id="627fa-193">Once the payment is complete, the web page calls the [`complete()`](https://msdn.microsoft.com/library/mt790642) method and passes a value of **success** or **fail**.</span></span>  <span data-ttu-id="627fa-194">El [`complete()`](https://msdn.microsoft.com/library/mt790642) método informa al explorador de que la compra ha finalizado y se debe mostrar la pantalla de interfaz de usuario de terminación correspondiente según el valor de **éxito** o **error**.</span><span class="sxs-lookup"><span data-stu-id="627fa-194">The [`complete()`](https://msdn.microsoft.com/library/mt790642) method informs the browser that the purchase is finished and the appropriate terminating UI screen should be shown depending on the value of **success** or **fail**.</span></span> 

![<span data-ttu-id="627fa-195">La interfaz de usuario que se muestra cuando la compra ](./../media/response_payment-request_complete.png)
![ se ha realizado correctamente la interfaz de usuario mostrada cuando se produjo un error</span><span class="sxs-lookup"><span data-stu-id="627fa-195">The UI displayed when the purchase succeeded](./../media/response_payment-request_complete.png)
![The UI displayed when the purchase failed</span></span>](./../media/response_payment-request_failure.png)

## <span data-ttu-id="627fa-196">Solicitud de pago con envío</span><span class="sxs-lookup"><span data-stu-id="627fa-196">Payment Request with Shipping</span></span>

### <span data-ttu-id="627fa-197">Dirección de envío</span><span class="sxs-lookup"><span data-stu-id="627fa-197">Shipping Address</span></span>

<span data-ttu-id="627fa-198">Para las ventas que requieren el envío de mercancías físicas, se necesita una dirección de envío.</span><span class="sxs-lookup"><span data-stu-id="627fa-198">For sales that require shipping physical goods, a shipping address is required.</span></span>  <span data-ttu-id="627fa-199">Para incluir una dirección de envío, establezca `requestShipping = True` el [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parámetro de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="627fa-199">To include a shipping address, set `requestShipping = True` in the [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter of the request.</span></span>   

<span data-ttu-id="627fa-200">Cuando el usuario seleccione o actualice la dirección de envío, el [`onshippingaddresschange`](https://msdn.microsoft.com/library/mt790442) evento se ejecutará.</span><span class="sxs-lookup"><span data-stu-id="627fa-200">When the user selects or updates the shipping address, the [`onshippingaddresschange`](https://msdn.microsoft.com/library/mt790442) event will run.</span></span>  <span data-ttu-id="627fa-201">El sitio web, mediante un detector de eventos, tendrá en cuenta el cambio y podrá validar la dirección, recalcular los gastos de envío y los impuestos, y actualizar [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) para reflejar los cargos cambiados y las opciones de envío disponibles para la dirección seleccionada (si corresponde).</span><span class="sxs-lookup"><span data-stu-id="627fa-201">The website, using an event listener, will be aware of the change and can then validate the address, re-calculate shipping costs and taxes, and update [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) to reflect the changed costs and shipping options available for the address selected (if applicable).</span></span> 

### <span data-ttu-id="627fa-202">Opciones de envío</span><span class="sxs-lookup"><span data-stu-id="627fa-202">Shipping Options</span></span> 

<span data-ttu-id="627fa-203">Las opciones de envío se pueden presentar al cliente agregando [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) al [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parámetro.</span><span class="sxs-lookup"><span data-stu-id="627fa-203">Shipping options can be presented to the customer by adding [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) to the [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter.</span></span>  <span data-ttu-id="627fa-204">Se puede establecer un valor predeterminado mediante `selected = True` la configuración de una de las opciones de envío.</span><span class="sxs-lookup"><span data-stu-id="627fa-204">A default can be established by setting `selected = True` for one of the shipping options.</span></span> 
 
<span data-ttu-id="627fa-205">Cuando el usuario seleccione o actualice el shippingOptions, [`onshippingoptionchange`](https://msdn.microsoft.com/library/mt790436) se ejecutará el evento.</span><span class="sxs-lookup"><span data-stu-id="627fa-205">When the user selects or updates the shippingOptions, the [`onshippingoptionchange`](https://msdn.microsoft.com/library/mt790436) event will run.</span></span>  <span data-ttu-id="627fa-206">El sitio web, mediante un detector de eventos, tendrá en cuenta el cambio y podrá actualizar el [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parámetro con el monto de envío correcto.</span><span class="sxs-lookup"><span data-stu-id="627fa-206">The website, using an event listener, will be aware of the change and can update the [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter with the correct shipping amount.</span></span>   

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

## <span data-ttu-id="627fa-207">Referencia de API</span><span class="sxs-lookup"><span data-stu-id="627fa-207">API Reference</span></span>
[<span data-ttu-id="627fa-208">API de solicitud de pago</span><span class="sxs-lookup"><span data-stu-id="627fa-208">Payment Request API</span></span>](https://msdn.microsoft.com/library/mt790447)

## <span data-ttu-id="627fa-209">Estadístico</span><span class="sxs-lookup"><span data-stu-id="627fa-209">Specification</span></span>
[<span data-ttu-id="627fa-210">API de solicitud de pago</span><span class="sxs-lookup"><span data-stu-id="627fa-210">Payment Request API</span></span>](https://w3.org/TR/payment-request/)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "¿Qué es Microsoft Edge heredado?"  
