---
description: Agregar y administrar usuarios de la organización en el Microsoft Edge para ayudar a administrar la cuenta del Centro de partners.  Habilite a los demás miembros del equipo para publicar Microsoft Edge en el sitio web de Microsoft Edge complementos con su cuenta del Centro de partners.
title: Agregar usuarios al programa Microsoft Edge usuario
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/27/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 1909ff45b2286698c90007eb6e5bb0671b4d5c07
ms.sourcegitcommit: dc445eae30234af1ad3fa42645aabb940529912b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2021
ms.locfileid: "11934343"
---
# <a name="add-users-to-the-microsoft-edge-program"></a>Agregar usuarios al programa Microsoft Edge usuario

<!-- better? # Add users to your Partner Center account -->
<!-- todo globally: "Microsoft Edge program", or other term? -->

Para ayudar a administrar Microsoft Edge extensiones, puede agregar más usuarios a una cuenta existente del Centro de partners.  Para administrar Microsoft Edge, el propietario principal de la cuenta del Centro de partners debe ser una cuenta de Microsoft (MSA).

Una cuenta de Microsoft (MSA) es una Outlook.com, Live.com o Hotmail.com cuenta.  Para obtener información general, vea [Types of accounts related to publishing Microsoft Edge extensions](create-dev-account.md#types-of-accounts-related-to-publishing-microsoft-edge-extensions).


<!-- ====================================================================== -->
## <a name="making-sure-you-have-a-partner-center-account-with-a-microsoft-account-msa-as-the-primary-owner"></a>Asegurarse de que tiene una cuenta del Centro de partners con una cuenta de Microsoft (MSA) como propietario principal

Para crear una cuenta del Centro de partners que pueda publicar extensiones de Microsoft Edge, debe tener una cuenta de Microsoft (MSA), ya sea mediante la creación de una directamente o mediante el uso de sus credenciales GitHub cuenta personal.  

Después de que tu cuenta del Centro de partners pueda publicar Microsoft Edge extensiones, puedes vincular la cuenta del Centro de partners a un inquilino de Azure Active Directory (Azure AD).  Un inquilino vinculado de Active Directory permite a los usuarios agregados iniciar sesión en su cuenta de desarrollador del Centro de partners mediante sus cuentas de trabajo.

Los distintos programas del Centro de partners requieren distintos tipos de cuentas:

*  El Microsoft Edge (como el programa Windows desarrollador) requiere una cuenta de desarrollador del Centro _de_ partners.  Una cuenta de desarrollador del Centro de partners tiene un propietario principal que es una cuenta de Microsoft (MSA).

*  En cambio, Azure Marketplace requiere una cuenta comercial del Centro _de_ partners.  (Para inscribirse, el usuario debe iniciar sesión con su cuenta de trabajo).

Vea también estos artículos en la documentación del Centro de partners:
*  [Administrar tu cuenta del Centro de partners](/partner-center/partner-center-account-setup)
*  [Ventajas de pertenencia a Microsoft Partner Network](/partner-center/mpn-overview)


<!-- ====================================================================== -->
## <a name="step-1-enroll-in-the-microsoft-edge-program-on-partner-center"></a>Paso 1: Inscribirse en el programa Microsoft Edge en el Centro de partners

<!-- todo: consider moving entire Step 1 section into create-dev-account.md -->

En primer lugar, determine si tiene una cuenta del Centro de partners.  Si tiene una cuenta del Centro de partners, determine si el propietario principal es una cuenta de Microsoft (MSA), que es necesaria para unirse al programa Microsoft Edge, para administrar Microsoft Edge extensiones.  A continuación, siga los pasos de la sección que se aplica al tipo de cuenta del Centro de partners.

### <a name="if-you-dont-have-a-partner-center-account"></a>Si no tiene una cuenta del Centro de partners

1.  Use una cuenta de Microsoft (MSA) para registrarse con el programa Microsoft Edge, siguiendo los pasos del artículo Registrar como desarrollador de Microsoft Edge [extensión][DeveloperRegistration].<!-- = create-dev-account.md-->  Como se mencionó en ese artículo, puede usar su cuenta GitHub para crear una cuenta de Microsoft (MSA).

A continuación, [realice el paso 2: Asociar Azure Active Directory con su cuenta Microsoft Edge programa a](#step-2-associate-azure-active-directory-with-your-microsoft-edge-program-account) continuación.


### <a name="if-the-primary-owner-of-your-partner-center-account-isnt-a-microsoft-account-msa"></a>Si el propietario principal de la cuenta del Centro de partners no es una cuenta de Microsoft (MSA)

Para que una cuenta del Centro de partners administre Microsoft Edge extensiones, el propietario principal de la cuenta del Centro de partners debe ser una cuenta de Microsoft (MSA).

Para determinar si el propietario principal de la cuenta del Centro de partners es una cuenta de Microsoft (MSA):

1. Use la cuenta de Microsoft (MSA) que corresponde a su cuenta comercial del Centro de partners para iniciar sesión en su cuenta comercial del Centro de partners.

1. Vaya a **Configuración de la cuenta**Administración de  >  [usuarios][UserMGMT] en el Centro de partners.

1. Compruebe si el propietario principal de la cuenta del Centro de partners es una cuenta de Microsoft (MSA).  Si el propietario principal no es una cuenta de Microsoft (MSA), significa que se trata de una cuenta comercial del Centro de partners en lugar de una cuenta de desarrollador del Centro _de_ partners. __

1. Use una cuenta de Microsoft (MSA) (no una cuenta de Microsoft de trabajo (MSA) o una cuenta de Microsoft educativa (MSA)) para registrarse con el programa Microsoft Edge, siguiendo los pasos descritos en Registrar como desarrollador de extensión de [Microsoft Edge][DeveloperRegistration]<!-- = create-dev-account.md-->.

A continuación, [realice el paso 2: Asociar Azure Active Directory con su cuenta Microsoft Edge programa a](#step-2-associate-azure-active-directory-with-your-microsoft-edge-program-account) continuación.


### <a name="if-the-primary-owner-of-your-partner-center-account-is-a-microsoft-account-msa"></a>Si el propietario principal de la cuenta del Centro de partners es una cuenta de Microsoft (MSA)

1. Si ya ha iniciado sesión en el Centro de partners con su cuenta de Microsoft (MSA) de trabajo, salga de sesión.  El Microsoft Edge en el Centro de partners no admite la inscripción mediante una cuenta de Microsoft (MSA) de trabajo o una cuenta microsoft educativa (MSA).

1. Usa la cuenta de Microsoft (MSA) que corresponde a tu cuenta de desarrollador del Centro de partners para iniciar sesión en tu cuenta de desarrollador del Centro de partners.

1. Vaya a **Configuración de la cuenta**Administración de  >  [usuarios][UserMGMT] en el Centro de partners.

1. Descubra quién es el propietario principal de la cuenta de desarrollador del Centro de partners.

1. Compruebe que el propietario principal de la cuenta de desarrollador del Centro de partners es un usuario de la cuenta de Microsoft (MSA).  No debe ser una cuenta de Microsoft (MSA) de trabajo o una cuenta de Microsoft educativa (MSA).

1. Hacer que el propietario principal de la cuenta de desarrollador del Centro de partners se registre en el programa Microsoft Edge siguiendo los pasos descritos en Registrar como desarrollador de Microsoft Edge [extensión][DeveloperRegistration]<!-- = create-dev-account.md-->.

A continuación, [realice el paso 2: Asociar Azure Active Directory con su cuenta Microsoft Edge programa a](#step-2-associate-azure-active-directory-with-your-microsoft-edge-program-account) continuación.


<!-- ====================================================================== -->
## <a name="step-2-associate-azure-active-directory-with-your-microsoft-edge-program-account"></a>Paso 2: Asociar Azure Active Directory con su cuenta Microsoft Edge programa

A continuación, vinculará los inquilinos de Azure Active Directory (inquilinos de Azure AD) con su cuenta del programa Microsoft Edge, para habilitar la administración de Microsoft Edge extensiones.  Puede usar el Azure Active Directory agregar usuarios a su cuenta Microsoft Edge programa y administrar esos usuarios en esa cuenta.  Puede agregar usuarios individuales, grupos de usuarios o Azure Active Directory aplicaciones.

Para poder agregar usuarios a su cuenta del programa de Microsoft Edge y administrar esos usuarios en esa cuenta, primero debe asociar la cuenta del programa de Microsoft Edge con el inquilino de Azure Active Directory de la organización (inquilino de Azure AD).  Si su organización ya usa Office 365 otros servicios empresariales de Microsoft, ya tiene un inquilino de Azure AD.  De lo contrario, puede crear un nuevo inquilino de Azure AD de forma gratuita.  Para crear un inquilino de AD, consulte [Create a brand new Azure AD to associate with your Partner Center account][AssociateAzureADPCnew] en el artículo Associate Azure Active Directory with your Partner Center _account_.

Consulta También consulta Asociar Azure Active Directory con tu cuenta del Centro de [partners,][AssociateAzureADPC]en la Windows de UWP.  La asociación de un inquilino de Azure AD con una cuenta de programa de Microsoft Edge en el Centro de partners funciona de la misma manera que asociar un espacio empresarial con el programa para desarrolladores Windows aplicaciones.

> [!IMPORTANT]
> Si ha agregado usuarios después de asociar el inquilino de Azure AD con su cuenta de Microsoft en el Centro de partners, tenga en cuenta que el cambio de roles o permisos de los usuarios no es compatible actualmente.  Sin embargo, puede seguir agregando tantos usuarios como necesite [][UserManagementPartnerCenter] y usar la opción de filtro de la sección de administración de usuarios para localizar administradores de roles específicos.


<!-- ====================================================================== -->
## <a name="step-3-add-users-groups-and-azure-active-directory-applications-to-your-account"></a>Paso 3: Agregar usuarios, grupos y Azure Active Directory aplicaciones a su cuenta

Después de configurar la asociación de Azure Active Directory, en el Centro de partners puede agregar usuarios en **Configuración**de cuenta  >  **Administración de usuarios**.  Cada usuario tiene acceso completo a las extensiones disponibles en el programa.  También puede agregar grupos de usuarios o agregar aplicaciones Azure Active Directory, para concederles acceso a su cuenta del Centro de partners.

Para obtener más información sobre cómo agregar usuarios, consulta [Agregar usuarios,][AddAzure] grupos y aplicaciones de Azure AD en la Windows de UWP.


<!-- ====================================================================== -->
## <a name="contact-us"></a>Ponte en contacto con nosotros 

Si necesita ayuda o ayuda para asociar su cuenta de Azure Active Directory u [otras][ContactEdgeExtensions]consultas relacionadas, vaya a Contacto Microsoft Edge de extensiones .


<!-- ====================================================================== -->
## <a name="see-also"></a>Consulta también

*  [Inicio rápido: configurar un inquilino:](/azure/active-directory/develop/quickstart-create-new-tenant) información general sobre Azure Active Directory (Azure AD), en la documentación de Active Directory.
<!-- contrasts "Work and school accounts, or personal Microsoft accounts" -->


<!-- ====================================================================== -->
<!-- links -->
[DeveloperRegistration]: ./create-dev-account.md "Registrarse como desarrollador de Microsoft Edge extensión | Microsoft Docs"
[ContactEdgeExtensions]: ./contact-extensions-team.md "Compatibilidad Microsoft Edge extensiones de contacto | Microsoft Docs"

<!-- DMC/windows/uwp -->
[AssociateAADWithPartnerCenterAccount]: /windows/uwp/publish/associate-azure-ad-with-partner-center

[CreateNewAzureAD]: /windows/uwp/publish/associate-azure-ad-with-partner-center#create-a-brand-new-azure-ad-to-associate-with-your-partner-center-account

[AddAADUsersGroups]: /windows/uwp/publish/add-users-groups-and-azure-ad-applications

[AssociateAzureADPC]: /windows/uwp/publish/associate-azure-ad-with-partner-center "Asocie Azure Active Directory con su cuenta del Centro de partners | Microsoft Docs"

[AssociateAzureADPCnew]: /windows/uwp/publish/associate-azure-ad-with-partner-center#create-a-brand-new-azure-ad-to-associate-with-your-partner-center-account "Crear una nueva cuenta de Azure AD para asociarla a tu cuenta del Centro de partners: asocia Azure Active Directory con la cuenta del Centro de partners | Microsoft Docs"

[AddAzure]: /windows/uwp/publish/add-users-groups-and-azure-ad-applications "Agregar usuarios, grupos y aplicaciones de Azure AD | Microsoft Docs"

<!-- non-DMC -->
[MicrosoftAccount]: https://account.microsoft.com/account "Cuenta de Microsoft"

[UserManagementPartnerCenter]: https://partner.microsoft.com/dashboard/account/v3/usermanagement
[UserMGMT]: https://partner.microsoft.com/dashboard/account/v3/usermanagement "Centro de partners de Microsoft | Configuración de la cuenta | Administración de usuarios"

[WindowsCommunityEverythingAboutMicrosoftAccounts]: https://community.windows.com/stories/everything-you-need-to-know-about-microsoft-accounts "Todo lo que necesita saber acerca de las cuentas de Microsoft | Windows Community"
