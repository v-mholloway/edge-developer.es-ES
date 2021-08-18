---
description: Obtenga información sobre cómo agregar y administrar usuarios de su organización en el programa Microsoft Edge usuario
title: Registrar su organización para el Microsoft Edge en el Centro de partners
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/30/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: e3db05067cd9a741a6034781a8b4ef821d05c2bb
ms.sourcegitcommit: 936f084e4e6b70b2553cc522622bf8e442cd6bf2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/18/2021
ms.locfileid: "11906970"
---
# <a name="add-and-manage-users-from-your-organization-on-to-the-microsoft-edge-program"></a>Agregar y administrar usuarios de la organización en el programa Microsoft Edge usuario

Para agregar y administrar usuarios en el programa Microsoft Edge para administrar extensiones, ahora puede asociar su cuenta del Centro de partners con la cuenta del centro de Azure Active Directory.

## <a name="step-1-enroll-in-the-microsoft-edge-program-on-partner-center"></a>Paso 1: Inscribirse en el programa Microsoft Edge en el Centro de partners

Si no tiene una cuenta y es nuevo en el Centro de partners, continúe con el paso **1**. Si tiene una cuenta para desarrolladores del Centro de partners, continúe con el paso **2**.

1. Si es nuevo en el Centro de partners y no tiene __ una cuenta, o si tiene una cuenta comercial existente con el Centro de partners (vea el paso **2.c** a continuación), use una cuenta de MSA para registrarse con el programa Microsoft Edge. Siga los pasos de [Register as a Microsoft Edge extensions developer][DeveloperRegistration]. 

1. Si tienes una cuenta de desarrollador registrada en el Centro de partners, usa la cuenta de Microsoft (MSA) correspondiente para iniciar sesión en tu cuenta de desarrollador. A continuación, inscríbete Microsoft Edge programa. El Microsoft Edge en el Centro de partners no admite la **inscripción directamente** con una cuenta laboral o educativa. 
    1. **Si ya ha iniciado sesión en el Centro de partners con**su cuenta de trabajo, debe iniciar sesión como propietario principal. Si no es el propietario, vaya a [Administración de usuarios][UserMGMT] para buscar el propietario principal de la cuenta.
    1. Compruebe que el propietario principal es un usuario de MSA (Hotmail/Live/Outlook). Pida al propietario de la cuenta que se registre en el programa Microsoft Edge Complementos mediante los pasos descritos en Inscribir en el programa Microsoft Edge para [el Centro de partners][DeveloperRegistration].
    1. Si su organización no tiene una cuenta de MSA (Hotmail/Live/Outlook) como propietario principal, debe registrarse para el programa Microsoft Edge con una cuenta de MSA. Esto sucede cuando la organización tiene una cuenta comercial en el Centro de partners. Siga los pasos de [Inscribir en el programa Microsoft Edge para el Centro de partners][DeveloperRegistration].

Una vez configurada la cuenta, continúe con la sección siguiente para vincular los inquilinos de Azure AD con esta cuenta para la administración de extensiones.

## <a name="step-2-associate-azure-active-directory-with-your-account"></a>Paso 2: Asociar Azure Active Directory con su cuenta

Puede usar Azure Active Directory para agregar y administrar usuarios en la cuenta Microsoft Edge programa. Puede agregar usuarios individuales, grupos de usuarios o aplicaciones de Azure AD. 

### <a name="associate-azure-active-directory-with-your-account"></a>Asociar Azure Active Directory con su cuenta

Para agregar y administrar usuarios de cuentas, primero debe asociar la cuenta con los usuarios de la Azure Active Directory. Si la organización ya usa Office365 u otros servicios empresariales de Microsoft, ya tienes AzureAD. De lo contrario, puede crear un nuevo inquilino de Azure AD de forma gratuita. Para obtener más información, vaya [a Asociar Azure Active Directory con la cuenta del Centro de partners | Microsoft Docs][AssociateAzureADPCnew].

Vaya a [Asociar Azure Active Directory con su cuenta del Centro de partners][AssociateAzureADPC] para obtener más información. Aunque el tema se centra en el programa Windows desarrollador de aplicaciones, la asociación de un inquilino funciona del mismo modo para el Microsoft Edge programa.

> [!IMPORTANT]
> Si ha agregado usuarios después de asociar su cuenta de Azure AD con su cuenta de Microsoft en el Centro de partners, tenga en cuenta que el cambio de roles o permisos de los usuarios no se admite actualmente. Sin embargo, puede seguir agregando tantos usuarios como necesite [][UserManagementPartnerCenter] y usar la opción de filtro de la sección de administración de usuarios para localizar administradores de roles específicos.

## <a name="step-3-add-users-groups-and-azure-ad-applications-to-your-account"></a>Paso 3: Agregar usuarios, grupos y aplicaciones de Azure AD a tu cuenta

Una vez configurada la asociación de Azure AD, en el Centro de partners puede agregar usuarios en **Configuración**de la cuenta  >  **Administración de usuarios**. Cada usuario tiene acceso completo a las extensiones disponibles en el programa. También puede agregar grupos de usuarios y aplicaciones de Azure AD para concederles acceso a su cuenta del Centro de partners. Para obtener más información acerca de cómo agregar usuarios, vea [Agregar usuarios, grupos y aplicaciones de Azure AD][AddAzure].

## <a name="contact-us"></a>Ponte en contacto con nosotros 

Si necesita ayuda o ayuda para asociar su cuenta de Azure AD u [otras][ContactEdgeExtensions] consultas relacionadas, vaya a Póngase en contacto con el soporte técnico de extensiones de Microsoft Edge y busque el contacto de soporte técnico relevante para su consulta.


<!-- links -->

[AssociateAADWithPartnerCenterAccount]: https://docs.microsoft.com/windows/uwp/publish/associate-azure-ad-with-partner-center

[CreateNewAzureAD]: https://docs.microsoft.com/windows/uwp/publish/associate-azure-ad-with-partner-center#create-a-brand-new-azure-ad-to-associate-with-your-partner-center-account

[UserManagementPartnerCenter]: https://partner.microsoft.com/dashboard/account/v3/usermanagement

[AddAADUsersGroups]: https://docs.microsoft.com/windows/uwp/publish/add-users-groups-and-azure-ad-applications

[ContactEdgeExtensions]: ./contact-extensions-team.md "Compatibilidad con extensiones perimetrales de | Microsoft Docs"

[WindowsCommunityEverythingAboutMicrosoftAccounts]:  https://community.windows.com/stories/everything-you-need-to-know-about-microsoft-accounts "Todo lo que necesita saber acerca de las cuentas de Microsoft | Windows Community"

[MicrosoftAccount]:  https://account.microsoft.com/account "Cuenta de Microsoft"

[DeveloperRegistration]: ./create-dev-account.md "Registrarse como desarrollador Microsoft Edge extensiones de | Microsoft Docs"

[AssociateAzureADPC]: /windows/uwp/publish/associate-azure-ad-with-partner-center "Asocie Azure Active Directory con su cuenta del Centro de partners | Microsoft Docs"

[AssociateAzureADPCnew]: /windows/uwp/publish/associate-azure-ad-with-partner-center#create-a-brand-new-azure-ad-to-associate-with-your-partner-center-account "Asocie Azure Active Directory con su cuenta del Centro de partners | Microsoft Docs"

[AddAzure]: /windows/uwp/publish/add-users-groups-and-azure-ad-applications "Agregar usuarios, grupos y aplicaciones de Azure AD | Microsoft Docs"

[UserMGMT]: https://partner.microsoft.com/dashboard/account/v3/usermanagement "Centro de partners de Microsoft | Configuración de la cuenta | Administración de usuarios"
