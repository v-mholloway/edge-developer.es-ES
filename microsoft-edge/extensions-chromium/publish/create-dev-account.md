---
description: Obtenga información sobre cómo registrar una cuenta de desarrollador del Centro de partners para publicar extensiones en el Microsoft Edge de complementos.
title: Registrarse como desarrollador de extensiones de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/27/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 3edeefc8b05506a3fc75de829e3da30288344ee1
ms.sourcegitcommit: dc445eae30234af1ad3fa42645aabb940529912b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2021
ms.locfileid: "11934350"
---
# <a name="register-as-a-microsoft-edge-extension-developer"></a>Registrarse como desarrollador de extensiones de Microsoft Edge

Si no es nuevo en el Centro de partners, este artículo le ayudará a crear una cuenta del Centro de partners a través de la cual puede enviar extensiones de Microsoft Edge al sitio web de Microsoft Edge complementos [.](https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home)

Si tiene una cuenta del Centro de partners, pero el propietario principal de la cuenta no es una cuenta de Microsoft (MSA), este artículo le ayudará a crear y vincular una cuenta adecuada.  Este artículo le ayudará a crear una cuenta de Microsoft (MSA) si no tiene una y le ayudará a vincular la cuenta de Microsoft (MSA) a su cuenta del Centro de partners.

Para agregar y administrar usuarios en el programa Microsoft Edge para administrar extensiones, puede asociar su cuenta del Centro de partners con el inquilino de Azure Active Directory (Azure AD) de su organización.


<!-- ====================================================================== -->
## <a name="types-of-accounts-related-to-publishing-microsoft-edge-extensions"></a>Tipos de cuentas relacionadas con la publicación Microsoft Edge extensiones

| Tipo de cuenta | Descripción |
|---|---|
| _Cuenta de Microsoft (MSA)_ | Una Outlook.com, Live.com o Hotmail.com cuenta. |
| _GitHub cuenta_ | Una cuenta de usuario en GitHub.com.  Puede usar su cuenta personal GitHub para iniciar sesión en el Centro de partners: se creará una cuenta de Microsoft (MSA). |
| _Cuenta del Centro de partners,_ _cuenta de desarrollador del Centro de partners_ | Una _cuenta del Centro de_ partners es una cuenta en partner.microsoft.com.  Para enviar Microsoft Edge, necesita una cuenta de desarrollador del Centro de _partners,_ que es una cuenta del Centro de partners que tiene una cuenta de Microsoft (MSA) como propietario principal. |
| _Microsoft Edge Cuenta del programa_ | Permite a varios usuarios trabajar con Microsoft Edge en el Centro de partners. |
| _Azure Active Directory_, _cuenta de AD_, Azure _AD_ | Una Azure Active Directory cuenta. |
| _Azure Active Directory inquilino ,_ _inquilino de AAD_ | Un _inquilino_ representa una organización.  Un inquilino es una instancia dedicada de Azure AD que un desarrollador de aplicaciones o organización recibe al principio de una relación con Microsoft. |


<!-- ====================================================================== -->
## <a name="before-you-begin"></a>Antes de empezar

Para enviar una extensión al sitio Microsoft Edge complementos, debe estar registrado como desarrollador con el Microsoft Edge web.  Puede registrarse para el programa Microsoft Edge en el Centro de partners.  Para registrarse en el Microsoft Edge, necesita una cuenta de Microsoft (MSA).  Si no tiene una cuenta de Microsoft (MSA), cree una.  Una forma de crear una cuenta de Microsoft (MSA) es usar la cuenta de GitHub existente para iniciar sesión en el Centro de partners: los cuadros de diálogo le ayudan a crear automáticamente una cuenta de Microsoft (MSA).

> [!NOTE]
> No hay ninguna cuota de registro para enviar extensiones al Microsoft Edge programa.

Si no tiene una cuenta del Centro de partners o tiene una cuenta del Centro de partners, pero su propietario principal no es una cuenta de Microsoft (MSA), debe:
*  Use una cuenta de Microsoft existente (MSA)) para registrarse con el Microsoft Edge cliente.
*  Crear una nueva cuenta de Microsoft (MSA).  Una cuenta de Microsoft (MSA) es una Outlook.com, Live.com o Hotmail.com cuenta.

Para crear una cuenta de Microsoft (MSA):

1. Decida si desea usar su cuenta de GitHub existente para crear una cuenta de Microsoft (MSA).  Consulte [Publicar Microsoft Edge extensiones mediante una cuenta GitHub .](github.md)

1. Si no usa su cuenta de GitHub para crear la cuenta de Microsoft (MSA), vaya [a account.microsoft.com][MicrosoftAccount].

1. Seleccione **Crear una cuenta de Microsoft**.

1. Complete los pasos de registro.

Si tiene una cuenta del Centro de partners para la que el propietario principal es una cuenta de Microsoft (MSA), use esa cuenta de Microsoft (MSA) para iniciar sesión en su cuenta del Centro de partners.  A continuación, inscríbete Microsoft Edge programa.

> [!NOTE]
> El Microsoft Edge no admite actualmente el registro con una cuenta laboral o educativa.  Debe registrarse con una cuenta de Microsoft (MSA) y, a continuación, vincular los inquilinos de Azure AD con esa cuenta para poder administrar extensiones.


<!-- ====================================================================== -->
## <a name="enroll-in-the-microsoft-edge-program-on-partner-center"></a>Inscribirse en el Microsoft Edge en el Centro de partners

<!-- 1.  Navigate to the [webpage about Partner Center](https://partner.microsoft.com).  You might see a "Join the Microsoft Partner Network" page with a **Become a partner** button, or a "Welcome back" page with a **Visit Partner Center** button.  Select the **Become a partner** button or the **Visit Partner Center** button. -->

1.  Vaya a la página [de inicio de sesión](https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd)del desarrollador del Centro de partners y, a continuación, seleccione Centro de **partners.**

1.  Si tiene una cuenta de Microsoft (MSA), úsela para iniciar sesión en el Centro de partners.  Una cuenta de Microsoft (MSA) es una Outlook.com, Live.com o Hotmail.com cuenta.  A continuación, rellene el Microsoft Edge de registro del programa mediante la tabla siguiente.

1.  Si no tiene una cuenta de Microsoft (MSA), cree una nueva cuenta de Microsoft (MSA) directamente o inicie sesión en el Centro de partners con su cuenta de GitHub mediante el paso siguiente.  La cuenta del Centro de partners debe tener un propietario principal que sea una cuenta de Microsoft (MSA).  Si desea iniciar sesión en el Centro de partners con su cuenta de GitHub personal existente, abra el artículo Publicar extensiones [de Microsoft Edge](github.md) mediante una cuenta GitHub en una nueva pestaña o ventana y siga los pasos.  Su GitHub se vinculará a una cuenta de Microsoft (MSA) creada automáticamente cuyas credenciales puede usar para registrarse para el Microsoft Edge programa.

1.  Después de iniciar sesión, se muestra un formulario de registro para inscribirse en el Microsoft Edge registro.  Use la tabla siguiente para ayudarle a rellenar el formulario de registro.

    :::row:::
       :::column span="1":::
          **País o región de la cuenta**  
       :::column-end:::
       :::column span="2":::
          Este campo es el lugar donde vive o donde se encuentra su empresa.  
          
          > [!IMPORTANT]
          > Después de la inscripción, el valor de este campo es de solo lectura.  
          
       :::column-end:::
    :::row-end:::
    :::row:::
       :::column span="1":::
          **Tipo de cuenta**  
       :::column-end:::
       :::column span="2":::
          El Microsoft Edge en el [Centro de partners][MicrosoftPartnerCenter] ofrece cuentas individuales y de empresa. Las cuentas se describen detalladamente en las siguientes viñetas.  Ambos tipos de cuenta permiten publicar extensiones en el Microsoft Edge de complementos.  
          
          > [!IMPORTANT]
          > Después de la inscripción, no podrá cambiar el valor de este campo.  
          
          *   **Cuenta individual**  
              Una cuenta individual es adecuada para un desarrollador que no está asociado a una empresa. El proceso de comprobación de la cuenta es más corto e implica comprobar que el nombre para mostrar del editor está disponible.  

          *   **Cuenta de empresa**  
              Una cuenta de empresa está asociada a una organización o empresa. El proceso de comprobación de la cuenta es más largo e implica la confirmación de que está autorizado a crear la cuenta para su empresa.  La duración del proceso puede variar de unos pocos días a unas pocas semanas.  Su empresa puede recibir llamadas telefónicas de socios de verificación de Microsoft.
              
       :::column-end:::
    :::row-end:::
    :::row:::
       :::column span="1":::
          **Publisher nombre para mostrar**  
       :::column-end:::
       :::column span="2":::
          Este campo contiene el nombre que se muestra en el sitio Microsoft Edge de complementos.  Para usar un nombre determinado, ese nombre debe estar disponible y debe tener los derechos para usarlo.  Las cuentas de la empresa deben usar el nombre comercial registrado de la organización.  
          
          > [!NOTE]
          > La longitud máxima de este campo es de cincuenta (50) caracteres.  
          
       :::column-end:::
    :::row-end:::
    :::row:::
       :::column span="1":::
          **Detalles de contacto**  
       :::column-end:::
       :::column span="2":::
          Este campo contiene cualquier información de contacto que Microsoft usa para ponerse en contacto con usted sobre cualquier problema de cuenta. Una vez completado el registro, recibirá una confirmación por correo electrónico. Para una cuenta de empresa, debe usar la dirección de correo electrónico registrada asociada a su organización.  
       :::column-end:::
    :::row-end:::
    :::row:::
       :::column span="1":::
          **Aprobador de empresa**  
       :::column-end:::
       :::column span="2":::
          Para una cuenta de empresa, debe proporcionar la información de contacto del aprobador de la compañía.  La información de contacto incluye el nombre, la dirección de correo electrónico y el número de teléfono.  Como parte del proceso de comprobación, Microsoft se pone en contacto con el aprobador de la empresa especificado para asegurarse de que la extensión pertenece a su organización.  
       :::column-end:::
    :::row-end:::
    
1.  Antes de enviar el formulario de registro, lea y acepte los términos y condiciones del [Microsoft Edge Developer Agreement][MicrosoftAppDeveloperAgreement].

1.  Para completar la inscripción, seleccione **Finalizar**.


<!-- ====================================================================== -->
## <a name="next-steps"></a>Pasos siguientes

Para mostrar el estado de comprobación, vaya al [Centro de partners][MicrosoftPartnerCenter] y, a continuación, seleccione Configuración de la **cuenta**.  Continúe compilando, probar y preparar los envíos mientras espera a que se complete el proceso de comprobación.

*  [Publicación de una extensión][ExtensionsChromiumPublishExtension]

*  [Conceptos de extensión y arquitectura][ExtensionsChromiumGettingStartedIndex]

*  [Agregar usuarios al programa Microsoft Edge:][AddandManageUsers] agregar usuarios adicionales al Microsoft Edge y a la cuenta de desarrollador del Centro de partners.  Para habilitar la adición de usuarios, asocie la cuenta de Azure Active Directory de la organización con su cuenta de Microsoft (MSA) en el Centro de partners.


<!-- ====================================================================== -->
## <a name="see-also"></a>Consulta también

*  [Inicio rápido: configurar un inquilino:](/azure/active-directory/develop/quickstart-create-new-tenant) información general sobre Azure Active Directory (Azure AD), en la documentación de Active Directory.


<!-- links -->
[AddandManageUsers]: ./aad-account.md "Agregar usuarios al Microsoft Edge de | Microsoft Docs"
[ExtensionsChromiumGettingStartedIndex]: ../getting-started/index.md "Conceptos de extensión y arquitectura | Microsoft Docs"
[ExtensionsChromiumPublishExtension]: ./publish-extension.md "Publicar una Microsoft Edge de | Microsoft Docs"
[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Contrato de desarrollador de aplicaciones | Microsoft Docs"
<!-- external links -->
[MicrosoftAccount]: https://account.microsoft.com/account "Cuenta de Microsoft"
[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de partners"
