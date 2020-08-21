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
# <span data-ttu-id="8b8fe-104">API de solicitud de pago (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="8b8fe-104">Payment Request API (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="8b8fe-105">En este artículo se describe el flujo de trabajo admitido en la [versión heredada de Microsoft Edge][MicrosoftSupport44533505].</span><span class="sxs-lookup"><span data-stu-id="8b8fe-105">This article describes the workflow supported in the [legacy version of Microsoft Edge][MicrosoftSupport44533505].</span></span>  <span data-ttu-id="8b8fe-106">Microsoft Edge \ (cromo \) admite la API de solicitud de pago con una implementación diferente según el proyecto de cromo.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-106">Microsoft Edge \(Chromium\) supports the Payment Request API with a different implementation based on the Chromium project.</span></span>  

<span data-ttu-id="8b8fe-107">Las ventas de comercio electrónico continúan creciendo a un ritmo rápido.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-107">E-commerce sales continue growing at a rapid pace.</span></span>  <span data-ttu-id="8b8fe-108">Según [eMarketer](https://www.emarketer.com), las ventas digitales de 2018 se preparan para aumentar en un 23% a partir de los niveles medidos en 2013.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-108">According to [eMarketer](https://www.emarketer.com), by 2018 digital sales are forecasted to increase by 23% from the levels measured in 2013.</span></span>  <span data-ttu-id="8b8fe-109">A pesar de que los consumidores y las empresas disfrutan de la comodidad de las ventas de comercio electrónico, los desafíos siguen.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-109">While consumers and businesses enjoy the convenience of e-commerce sales, challenges remain.</span></span>  <span data-ttu-id="8b8fe-110">Hoy, cada propietario de un sitio web de comercio electrónico debe invertir tiempo para desarrollar los flujos de pago y las reglas de validación de pago de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-110">Today each e-commerce website owner needs to invest time to develop high quality payment checkout flows and validation rules.</span></span>  <span data-ttu-id="8b8fe-111">Los consumidores necesitan navegar por diferentes flujos de pago y volver a introducir la misma información de pago y envío en todos los sitios donde se tiendan.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-111">Consumers need to navigate different payment checkout flows and re-enter the same payment and shipping information on every site where they shop.</span></span>  <span data-ttu-id="8b8fe-112">Esto puede resultar lento y frustrante para los consumidores, lo que lleva a una alta tasa de abandono del carro de la compra y ha disminuido las ventas de comerciantes.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-112">This can be time consuming and frustrating for consumers, leading to a high rate of shopping cart abandonment and decreased sales for merchants.</span></span>  <span data-ttu-id="8b8fe-113">Se abandona el [cálculo](http://baymard.com/lists/cart-abandonment-rate) de los comerciantes entre el 60% y el 70% de los carros de la compra.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-113">Merchants [estimate](http://baymard.com/lists/cart-abandonment-rate) between 60% and 70% of shopping carts are abandoned.</span></span>  

<span data-ttu-id="8b8fe-114">La [API de solicitud de pago](https://w3.org/TR/payment-request) Estandariza el proceso de desprotección de pago.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-114">The [Payment Request API](https://w3.org/TR/payment-request) standardizes the payment checkout process.</span></span>  <span data-ttu-id="8b8fe-115">Esta API requiere menos personalización para los desarrolladores web y proporciona una experiencia más rápida, coherente y, por lo tanto, confusa para los consumidores.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-115">This API requires less customization for web developers and provides a faster, more consistent, and therefore, less confusing experience for consumers.</span></span>  <span data-ttu-id="8b8fe-116">Como los consumidores pueden seleccionar los instrumentos de pago y las direcciones de envío de su cuenta de Microsoft, tienen que introducir menos datos para completar las compras, lo que reduce el tiempo y la entrada de datos necesarios para completar el pago.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-116">Because consumers can select payment instruments and shipping addresses from their Microsoft account, they are required to enter less data to complete purchases which reduces the time and data entry required to complete a payment.</span></span>  

<span data-ttu-id="8b8fe-117">La [API de solicitud de pago](https://w3.org/TR/payment-request) es un estándar entre exploradores abierto que permite que los exploradores actúen como intermediario entre comerciantes, consumidores y las formas de pago \ (como tarjetas de crédito \) que los consumidores hayan almacenado en la nube.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-117">The [Payment Request API](https://w3.org/TR/payment-request) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and the payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  
  
<span data-ttu-id="8b8fe-118">En Resumen, al usar la [API de solicitud de pago](https://w3.org/TR/payment-request), los clientes pueden comprar en sitios web de comerciante de forma normal.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-118">In summary, when using the [Payment Request API](https://w3.org/TR/payment-request), customers shop on merchant websites as normal.</span></span>  <span data-ttu-id="8b8fe-119">Cuando esté listo para pagar, el sitio web de comerciante llama a la API de **solicitud de pago** para crear una **solicitud de pago** y pasa la información de pago correspondiente \ (como las formas de pago admitidas, la cantidad de compra, la moneda, etc. \) al explorador.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-119">When ready to pay, the merchant website calls the **Payment Request** API to create a **Payment Request** and passes the relevant payment information \(such as supported payment methods, purchase amount, currency, and so on\) to the browser.</span></span>  

:::image type="complex" source="../media/payment_request_construct.png" alt-text="Construcción de solicitud de pago" lightbox="../media/payment_request_construct.png":::
   <span data-ttu-id="8b8fe-121">Construcción de solicitud de pago</span><span class="sxs-lookup"><span data-stu-id="8b8fe-121">Payment request construct</span></span>  
:::image-end:::  

<span data-ttu-id="8b8fe-122">El explorador autentica al usuario, permite al usuario seleccionar una forma de pago admitida en un archivo y procesa los detalles de pago.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-122">The browser authenticates the user, enables the user to select a supported payment method on file, and processes the payment details.</span></span>  <span data-ttu-id="8b8fe-123">El explorador vuelve a enviar los detalles de la información de pago al sitio web del comerciante, de modo que el comerciante pueda completar el pago.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-123">The browser then sends the payment information details back to the merchant website, so that the merchant can complete the payment.</span></span>  <span data-ttu-id="8b8fe-124">Además de recibir información de pago, el comerciante puede optar por recibir la información de envío como parte de la **solicitud de pago**.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-124">In addition to receiving payment information, the merchant can also elect to receive shipping information as part of the **Payment Request**.</span></span>  

:::image type="complex" source="../media/payment_response_construct.png" alt-text="Construcción de respuesta de pago" lightbox="../media/payment_response_construct.png":::
   <span data-ttu-id="8b8fe-126">Construcción de respuesta de pago</span><span class="sxs-lookup"><span data-stu-id="8b8fe-126">Payment response construct</span></span>  
:::image-end:::  

<span data-ttu-id="8b8fe-127">Para ver la API de solicitud de pago en acción, así como para obtener información general sobre cómo usarla, consulte este vídeo.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-127">To see the Payment Request API in action, as well as get an overview of how to use it, check out this video.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]  

> [!NOTE]
> <span data-ttu-id="8b8fe-128">La API de solicitud de pago es compatible con la compilación 14992 o posterior de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-128">The Payment Request API is supported in Microsoft Edge build 14992 or newer.</span></span>  

## <span data-ttu-id="8b8fe-129">Crear una solicitud de pago</span><span class="sxs-lookup"><span data-stu-id="8b8fe-129">Creating a Payment Request</span></span>  

<span data-ttu-id="8b8fe-130">Las páginas web crean una **solicitud de pago** generalmente cuando el usuario inicia un proceso de pago haciendo clic en el botón comprar.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-130">Web pages create a **Payment Request** typically when the user initiates a payment process by clicking a "buy" button.</span></span>  <span data-ttu-id="8b8fe-131">El **Payment Request** [constructor](/previous-versions/mt790440(v=vs.85)) de la solicitud de pago incluye methodData, detalles y opciones.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-131">The **Payment Request** [constructor](/previous-versions/mt790440(v=vs.85)) includes methodData, details, and options.</span></span>  

```javascript
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```  

<span data-ttu-id="8b8fe-132">El parámetro [methodData](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) contiene una lista de las formas de pago y las redes aceptadas por el sitio web y los datos específicos de cualquier método de pago asociado.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-132">The [methodData](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter contains a list of the payment methods and networks accepted by the website and any associated payment method specific data.</span></span>  <span data-ttu-id="8b8fe-133">En Microsoft Edge, esta lista coincide con las formas de pago admitidas que el comprador ha guardado en su cuenta de Microsoft y da como resultado la lista "pagar con" en la experiencia de usuario de pago.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-133">In Microsoft Edge, this list is matched with the supported payment methods that the shopper has saved in their Microsoft account and results in the "pay with" list in the payment user experience.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_with.png" alt-text="La lista pagar con de la experiencia de usuario de Microsoft Wallet" lightbox="../media/pay_with.png":::
         <span data-ttu-id="8b8fe-135">La lista **pagar con** de la experiencia de usuario de Microsoft Wallet</span><span class="sxs-lookup"><span data-stu-id="8b8fe-135">The **pay with** list in the Microsoft Wallet user experience</span></span>  
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

<span data-ttu-id="8b8fe-136">El parámetro de [detalles](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) contiene información que el comerciante desea transmitir al cliente sobre la transacción.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-136">The [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter contains information that the merchant wishes to convey to the customer about the transaction.</span></span>  <span data-ttu-id="8b8fe-137">Estos incluyen elementos de Resumen de pedidos como total, impuestos, cantidad de envío y otros elementos de nivel de resumen que afectan al monto del pago.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-137">These include order summary items like total, tax, shipping amount, and other summary level items impacting the payment amount.</span></span>  <span data-ttu-id="8b8fe-138">No se pretende que se ordenen los artículos de línea.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-138">These are not intended to be order line items.</span></span>  
  
<span data-ttu-id="8b8fe-139">El parámetro de [detalles](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) también se usa para definir las opciones de envío disponibles para el cliente cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-139">The [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter is also used to define shipping options available to the customer when required.</span></span>  <span data-ttu-id="8b8fe-140">A continuación, se incluyen más detalles en la **solicitud de pago** .</span><span class="sxs-lookup"><span data-stu-id="8b8fe-140">More details are included in the **Payment Request** with Shipping section below.</span></span>  

<span data-ttu-id="8b8fe-141">Cada línea de [detalle](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) incluye una etiqueta para la moneda y la cantidad.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-141">Each [detail](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) line includes a label for the currency and the amount.</span></span>  

> [!NOTE]
> <span data-ttu-id="8b8fe-142">La **solicitud de pago** no calcula la suma o el total de estas cantidades.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-142">The **Payment Request** does not calculate the sum or total of these amounts.</span></span>  <span data-ttu-id="8b8fe-143">El sitio web del comerciante es responsable de garantizar que el total de los elementos de línea sea correcto.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-143">It is the responsibility of the merchant's website to ensure that the line items total correctly.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/show_details.png" alt-text="Subtotal, envío, impuestos y detalles totales" lightbox="../media/show_details.png":::
         <span data-ttu-id="8b8fe-145">Subtotal, envío, impuestos y detalles totales</span><span class="sxs-lookup"><span data-stu-id="8b8fe-145">Subtotal, shipping, taxes, and total details</span></span>  
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

<span data-ttu-id="8b8fe-146">[PaymentRequest](/previous-versions/mt790440(v=vs.85)) no admite reembolsos, por lo que los importes deben ser siempre positivos; los elementos individuales de la lista pueden ser negativos, como los descuentos.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-146">[PaymentRequest](/previous-versions/mt790440(v=vs.85)) does not support refunds, so the amounts should always be positive; individual list items can be negative, such as discounts.</span></span>  

<span data-ttu-id="8b8fe-147">El explorador representará las etiquetas a medida que las define y represente automáticamente el formato de moneda correcto basándose en la configuración regional del cliente.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-147">The browser will render the labels as you define them and automatically render the correct currency formatting based on the customer's locale.</span></span>  <span data-ttu-id="8b8fe-148">Tenga en cuenta que las etiquetas se deben representar en el mismo idioma que el contenido.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-148">Note that the labels should be rendered in the same language as your content.</span></span>  

<span data-ttu-id="8b8fe-149">El parámetro [Options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) define los datos que la página web desea que se devuelva de la **solicitud de pago**.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-149">The [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter defines data the web page wants returned from the **Payment Request**.</span></span>  <span data-ttu-id="8b8fe-150">Esto también define los datos que es necesario recopilar, incluidos los envíos, la dirección de correo electrónico, el número de teléfono o todos.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-150">This also defines the data that needs to be collected, including if shipping, email address, phone number or all are required.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/email_snippet.png" alt-text="Lista desplegable de dirección de correo electrónico" lightbox="../media/email_snippet.png":::
         <span data-ttu-id="8b8fe-152">Lista desplegable de dirección de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="8b8fe-152">Email address dropdown</span></span>  
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

## <span data-ttu-id="8b8fe-153">Mostrar la solicitud de pago</span><span class="sxs-lookup"><span data-stu-id="8b8fe-153">Showing the Payment Request</span></span>  

<span data-ttu-id="8b8fe-154">La página web llama al método [Show ()](/previous-versions/mt790448(v=vs.85)) para permitir que el usuario interactúe con la interfaz de usuario de **solicitud de pago** .</span><span class="sxs-lookup"><span data-stu-id="8b8fe-154">The [show()](/previous-versions/mt790448(v=vs.85)) method is called by the web page to allow the user to interact with the **Payment Request** user interface.</span></span>  <span data-ttu-id="8b8fe-155">El método [Show ()](/previous-versions/mt790448(v=vs.85)) devuelve una promesa que se resolverá cuando el usuario autorice la solicitud de pago.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-155">The [show()](/previous-versions/mt790448(v=vs.85)) method returns a Promise that will be resolved when the user authorizes the payment request.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_screen_default.png" alt-text="Confirmar y pagar detalles" lightbox="../media/pay_screen_default.png":::
         <span data-ttu-id="8b8fe-157">Confirmar y pagar detalles</span><span class="sxs-lookup"><span data-stu-id="8b8fe-157">Confirm and pay details</span></span>  
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

## <span data-ttu-id="8b8fe-158">Anulando una solicitud de pago</span><span class="sxs-lookup"><span data-stu-id="8b8fe-158">Aborting a Payment Request</span></span>  
 
<span data-ttu-id="8b8fe-159">La página web puede llamar al método [Abort ()](/previous-versions/mt790437(v=vs.85)) en cualquier momento después de llamar al método [Show ()](/previous-versions/mt790448(v=vs.85)) hasta el punto en el que se resuelve la promesa.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-159">The [abort()](/previous-versions/mt790437(v=vs.85)) method can be called by the web page any time after the [show()](/previous-versions/mt790448(v=vs.85)) method is called, up until the point where the Promise is resolved.</span></span>  <span data-ttu-id="8b8fe-160">El método [Abort ()](/previous-versions/mt790437(v=vs.85)) hará que el navegador anule la **solicitud de pago** y cierre la interfaz de usuario de la solicitud de **pago** .</span><span class="sxs-lookup"><span data-stu-id="8b8fe-160">The [abort()](/previous-versions/mt790437(v=vs.85)) method will cause the browser to abort the **Payment Request** and close the **Payment Request** user interface.</span></span>  <span data-ttu-id="8b8fe-161">Por ejemplo, una página web puede optar por anular si el usuario no completó la transacción en el período de tiempo requerido.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-161">For example, a web page may choose to abort if the user did not complete the transaction in the required amount of time.</span></span>  

```javascript
payment.abort();
```  

## <span data-ttu-id="8b8fe-162">Respuesta de pago</span><span class="sxs-lookup"><span data-stu-id="8b8fe-162">Payment Response</span></span>  
<span data-ttu-id="8b8fe-163">Cuando el cliente apruebe la **solicitud de pago**, se devolverá una **respuesta de pago** al sitio Web.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-163">When the customer approves the **Payment Request**, a **Payment Response** is returned to the website.</span></span>  <span data-ttu-id="8b8fe-164">La **respuesta de pago** incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8b8fe-164">The **Payment Response** includes the following:</span></span>  

 <span data-ttu-id="8b8fe-165">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8b8fe-165">Property</span></span>      | <span data-ttu-id="8b8fe-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b8fe-166">Description</span></span> | <span data-ttu-id="8b8fe-167">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8b8fe-167">Required</span></span> | <span data-ttu-id="8b8fe-168">Información adicional</span><span class="sxs-lookup"><span data-stu-id="8b8fe-168">Additional Info</span></span>
|---------------|-----------------|-------|-----------------|
[<span data-ttu-id="8b8fe-169">nombreDeMétodo</span><span class="sxs-lookup"><span data-stu-id="8b8fe-169">methodName</span></span>](/previous-versions/mt790656(v=vs.85)) | <span data-ttu-id="8b8fe-170">El identificador de la forma de pago seleccionada por el usuario</span><span class="sxs-lookup"><span data-stu-id="8b8fe-170">The ID for the payment method selected by the user</span></span> | <span data-ttu-id="8b8fe-171">Y</span><span class="sxs-lookup"><span data-stu-id="8b8fe-171">Y</span></span> | |   
[<span data-ttu-id="8b8fe-172">details</span><span class="sxs-lookup"><span data-stu-id="8b8fe-172">details</span></span>](/previous-versions/mt790655(v=vs.85)) | <span data-ttu-id="8b8fe-173">Un objeto JSON que incluye todos los datos que el comerciante necesita para procesar la transacción con la forma de pago seleccionada o un token de pago</span><span class="sxs-lookup"><span data-stu-id="8b8fe-173">A JSON object that includes all of the data the merchant requires to process the transaction using the selected payment method or a payment token</span></span> | <span data-ttu-id="8b8fe-174">Y</span><span class="sxs-lookup"><span data-stu-id="8b8fe-174">Y</span></span> | <span data-ttu-id="8b8fe-175">[Tarjeta básica](https://w3c.github.io/payment-method-basic-card) Diccionario: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span><span class="sxs-lookup"><span data-stu-id="8b8fe-175">[Basic Card](https://w3c.github.io/payment-method-basic-card) Dictionary:  cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span></span> |   
[<span data-ttu-id="8b8fe-176">shippingAddress</span><span class="sxs-lookup"><span data-stu-id="8b8fe-176">shippingAddress</span></span>](/previous-versions/mt790445(v=vs.85)) | <span data-ttu-id="8b8fe-177">La dirección de envío seleccionada por el usuario</span><span class="sxs-lookup"><span data-stu-id="8b8fe-177">The shipping address selected by the user</span></span>  |  <span data-ttu-id="8b8fe-178">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-178">Optional.</span></span>  <span data-ttu-id="8b8fe-179">Requerido cuando [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) es</span><span class="sxs-lookup"><span data-stu-id="8b8fe-179">Required when [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | <span data-ttu-id="8b8fe-180">Diccionario de direcciones: país; addressLine; sección urbanas dependentLocality; Código sortingCode; languageCode; Organización remite llamar</span><span class="sxs-lookup"><span data-stu-id="8b8fe-180">Address dictionary:  country; addressLine; region; city; dependentLocality; postalCode; sortingCode; languageCode; organization; recipient; phone</span></span> |  
[<span data-ttu-id="8b8fe-181">shippingOption</span><span class="sxs-lookup"><span data-stu-id="8b8fe-181">shippingOption</span></span>](/previous-versions/mt790446(v=vs.85)) | <span data-ttu-id="8b8fe-182">El identificador de la opción de envío seleccionada</span><span class="sxs-lookup"><span data-stu-id="8b8fe-182">The ID for the selected shipping option</span></span> | <span data-ttu-id="8b8fe-183">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-183">Optional.</span></span>  <span data-ttu-id="8b8fe-184">Requerido cuando [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) es</span><span class="sxs-lookup"><span data-stu-id="8b8fe-184">Required when [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | |   
[<span data-ttu-id="8b8fe-185">payerName</span><span class="sxs-lookup"><span data-stu-id="8b8fe-185">payerName</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="8b8fe-186">El nombre proporcionado por el usuario</span><span class="sxs-lookup"><span data-stu-id="8b8fe-186">The name provided by the user</span></span>  | <span data-ttu-id="8b8fe-187">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-187">Optional.</span></span>  <span data-ttu-id="8b8fe-188">Requerido cuando [requestPayerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) es</span><span class="sxs-lookup"><span data-stu-id="8b8fe-188">Required when [requestPayerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True` | |  
[<span data-ttu-id="8b8fe-189">payerEmail</span><span class="sxs-lookup"><span data-stu-id="8b8fe-189">payerEmail</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="8b8fe-190">La dirección de correo electrónico seleccionada por el usuario</span><span class="sxs-lookup"><span data-stu-id="8b8fe-190">The email address selected by the user</span></span> | <span data-ttu-id="8b8fe-191">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-191">Optional.</span></span>  <span data-ttu-id="8b8fe-192">Requerido cuando [requestPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) es</span><span class="sxs-lookup"><span data-stu-id="8b8fe-192">Required when [requestPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | |  
[<span data-ttu-id="8b8fe-193">PayerPhone</span><span class="sxs-lookup"><span data-stu-id="8b8fe-193">PayerPhone</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="8b8fe-194">El número de teléfono seleccionado por el usuario</span><span class="sxs-lookup"><span data-stu-id="8b8fe-194">The phone number selected by the user</span></span> | <span data-ttu-id="8b8fe-195">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-195">Optional.</span></span>  <span data-ttu-id="8b8fe-196">Requerido cuando [requestPayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) es</span><span class="sxs-lookup"><span data-stu-id="8b8fe-196">Required when [requestPayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True` | |  

<span data-ttu-id="8b8fe-197">El objeto JSON [Details](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) de la **respuesta de pago** contendrá los datos de pago requeridos por el comerciante para procesar un pago.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-197">The [details](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) JSON object in the **Payment Response** will contain the payment data required by the merchant to process a payment.</span></span>  <span data-ttu-id="8b8fe-198">En su forma más simple, la respuesta será una carga de [tarjeta básica](https://w3c.github.io/payment-method-basic-card) que contenga detalles de tarjetas de pago de texto no cifrado.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-198">In its simplest form, the response will be a [Basic Card](https://w3c.github.io/payment-method-basic-card) payload containing cleartext payment card details.</span></span>  <span data-ttu-id="8b8fe-199">En caso de que los comerciantes dispongan de un acuerdo con socios de asistencia y de procesadores adicionales para que puedan prestar asistencia a los pagos, el comerciante puede exigir una carga que el procesador pueda manejar.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-199">Where merchants have arrangements with additional gateway/processor partners for them to provide payments support, the merchant may require a payload the processor can handle.</span></span>  <span data-ttu-id="8b8fe-200">Estos pueden tomar la forma de un token de procesador/puerta de enlace o un instrumento de pago cifrado.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-200">These can take the shape of a processor/gateway token or an encrypted payment instrument.</span></span>  <span data-ttu-id="8b8fe-201">Estas formas de pago están fuera del alcance de este documento y se tratarán en la documentación específica para el procesador.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-201">These payment methods are outside the scope of this document and will be covered in documentation specific to the processor.</span></span>  <span data-ttu-id="8b8fe-202">Además, para recibir una respuesta de [tarjeta básica](https://w3c.github.io/payment-method-basic-card) , el desarrollador necesita una incorporación de datos adicional a Microsoft, a diferencia de otras formas de pago específicas del procesador o de la puerta de enlace, que pueden requerir incorporación de claves de cifrado o solicitar autorización \ (OAuth \).</span><span class="sxs-lookup"><span data-stu-id="8b8fe-202">Additionally, to receive a [Basic Card](https://w3c.github.io/payment-method-basic-card) response, no additional onboarding to Microsoft is required by the developer, unlike other processor/gateway specific payment methods which may require encryption key onboarding or request authorization \(oAuth\).</span></span>  

<span data-ttu-id="8b8fe-203">Al recibir la **respuesta de pago**, el sitio Web envía la información de pago a su procesador de pagos.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-203">Upon receiving the **Payment Response**, the website submits the payment information to their payment processor.</span></span>  <span data-ttu-id="8b8fe-204">El explorador mostrará una página de giro mientras se está procesando el pago.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-204">The browser will display a spinner page while the payment is being processed.</span></span>  

:::image type="complex" source="../media/loading_screen.png" alt-text="La página que se muestra cuando se está procesando el pago" lightbox="../media/loading_screen.png":::
   <span data-ttu-id="8b8fe-206">La página que se muestra cuando se está procesando el pago</span><span class="sxs-lookup"><span data-stu-id="8b8fe-206">The page displayed when the payment is being processed</span></span>  
:::image-end:::  

<span data-ttu-id="8b8fe-207">Una vez completado el pago, la página web llama al método [Complete ()](/previous-versions/mt790642(v=vs.85)) y pasa el valor **Success** o **failed**.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-207">Once the payment is complete, the web page calls the [complete()](/previous-versions/mt790642(v=vs.85)) method and passes a value of **success** or **fail**.</span></span>  <span data-ttu-id="8b8fe-208">El método [Complete ()](/previous-versions/mt790642(v=vs.85)) informa al explorador de que la compra ha finalizado y se debe mostrar la pantalla de interfaz de usuario de terminación correspondiente según el valor de **éxito** o **error**.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-208">The [complete()](/previous-versions/mt790642(v=vs.85)) method informs the browser that the purchase is finished and the appropriate terminating UI screen should be shown depending on the value of **success** or **fail**.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_complete.png" alt-text="La interfaz de usuario mostrada cuando la compra se realizó correctamente" lightbox="../media/response_payment-request_complete.png":::
         <span data-ttu-id="8b8fe-210">La interfaz de usuario mostrada cuando la compra se realizó correctamente</span><span class="sxs-lookup"><span data-stu-id="8b8fe-210">The UI displayed when the purchase succeeded</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_failure.png" alt-text="La interfaz de usuario que se muestra cuando se produjo un error en la compra" lightbox="../media/response_payment-request_failure.png":::
         <span data-ttu-id="8b8fe-212">La interfaz de usuario que se muestra cuando se produjo un error en la compra</span><span class="sxs-lookup"><span data-stu-id="8b8fe-212">The UI displayed when the purchase failed</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="8b8fe-213">Solicitud de pago con envío</span><span class="sxs-lookup"><span data-stu-id="8b8fe-213">Payment Request with Shipping</span></span>  

### <span data-ttu-id="8b8fe-214">Dirección de envío</span><span class="sxs-lookup"><span data-stu-id="8b8fe-214">Shipping Address</span></span>  

<span data-ttu-id="8b8fe-215">Para las ventas que requieren el envío de mercancías físicas, se necesita una dirección de envío.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-215">For sales that require shipping physical goods, a shipping address is required.</span></span>  <span data-ttu-id="8b8fe-216">Para incluir una dirección de envío, establezca `requestShipping = True` el parámetro [Options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-216">To include a shipping address, set `requestShipping = True` in the [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter of the request.</span></span>  

<span data-ttu-id="8b8fe-217">Cuando el usuario seleccione o actualice la dirección de envío, se ejecutará el evento [onshippingaddresschange](/previous-versions/mt790442(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8b8fe-217">When the user selects or updates the shipping address, the [onshippingaddresschange](/previous-versions/mt790442(v=vs.85)) event will run.</span></span>  <span data-ttu-id="8b8fe-218">El sitio web, mediante un detector de eventos, tendrá en cuenta el cambio y podrá validar la dirección, calcular de nuevo los gastos de envío y los impuestos, y actualizar [shippingOptions](/previous-versions/mt790440(v=vs.85)) para reflejar los cargos modificados y las opciones de envío disponibles para la dirección seleccionada \ (si corresponde \).</span><span class="sxs-lookup"><span data-stu-id="8b8fe-218">The website, using an event listener, will be aware of the change and can then validate the address, re-calculate shipping costs and taxes, and update [shippingOptions](/previous-versions/mt790440(v=vs.85)) to reflect the changed costs and shipping options available for the address selected \(if applicable\).</span></span>  

### <span data-ttu-id="8b8fe-219">Opciones de envío</span><span class="sxs-lookup"><span data-stu-id="8b8fe-219">Shipping Options</span></span>  

<span data-ttu-id="8b8fe-220">Las opciones de envío se pueden presentar al cliente agregando [shippingOptions](/previous-versions/mt790440(v=vs.85)) al parámetro de [detalles](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) .</span><span class="sxs-lookup"><span data-stu-id="8b8fe-220">Shipping options can be presented to the customer by adding [shippingOptions](/previous-versions/mt790440(v=vs.85)) to the [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter.</span></span>  <span data-ttu-id="8b8fe-221">Se puede establecer un valor predeterminado mediante `selected = True` la configuración de una de las opciones de envío.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-221">A default can be established by setting `selected = True` for one of the shipping options.</span></span>  
 
<span data-ttu-id="8b8fe-222">Cuando el usuario seleccione o actualice el shippingOptions, se ejecutará el evento [onshippingoptionchange](/previous-versions/mt790436(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8b8fe-222">When the user selects or updates the shippingOptions, the [onshippingoptionchange](/previous-versions/mt790436(v=vs.85)) event will run.</span></span>  <span data-ttu-id="8b8fe-223">El sitio web, mediante un detector de eventos, será consciente del cambio y podrá actualizar el parámetro de [detalles](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) con el monto de envío correcto.</span><span class="sxs-lookup"><span data-stu-id="8b8fe-223">The website, using an event listener, will be aware of the change and can update the [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter with the correct shipping amount.</span></span>  

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

## <span data-ttu-id="8b8fe-224">Referencia de API</span><span class="sxs-lookup"><span data-stu-id="8b8fe-224">API Reference</span></span>  

[<span data-ttu-id="8b8fe-225">API de solicitud de pago</span><span class="sxs-lookup"><span data-stu-id="8b8fe-225">Payment Request API</span></span>](/previous-versions/mt790447(v=vs.85))  

## <span data-ttu-id="8b8fe-226">Estadístico</span><span class="sxs-lookup"><span data-stu-id="8b8fe-226">Specification</span></span>
[<span data-ttu-id="8b8fe-227">API de solicitud de pago</span><span class="sxs-lookup"><span data-stu-id="8b8fe-227">Payment Request API</span></span>](https://w3.org/TR/payment-request)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "¿Qué es Microsoft Edge heredado?"  
