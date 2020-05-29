---
description: Haga que su extensión sea accesible para diferentes idiomas y pruebe las cadenas de idioma con la guía de internacionalización.
title: Extensiones-internacionalización
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: d1f553d0e3e39192e68665fe6720daa811777c0b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573601"
---
# <span data-ttu-id="aed71-104">Internacionalización</span><span class="sxs-lookup"><span data-stu-id="aed71-104">Internationalization</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="aed71-105">Para que la extensión sea accesible para una variedad de personas distintas, es importante que se desarrolle con otros países en mente.</span><span class="sxs-lookup"><span data-stu-id="aed71-105">In order to make your extension accessible to a variety of different people, it is important to develop with other countries in mind.</span></span> <span data-ttu-id="aed71-106">Las extensiones de Microsoft Edge le permiten agregar diferentes cadenas de idioma a las extensiones para que su idioma pueda cambiarse fácilmente.</span><span class="sxs-lookup"><span data-stu-id="aed71-106">Microsoft Edge extensions allows you to add different language strings to your extensions so that their language can easily be changed.</span></span>

<span data-ttu-id="aed71-107">Para obtener más información sobre cómo internacionalizar su extensión, consulte la [Guía de internacionalización](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization)de MDN.</span><span class="sxs-lookup"><span data-stu-id="aed71-107">For more information on internationalizing your extension, check out MDN's [Internationalization guide](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization).</span></span>


## <span data-ttu-id="aed71-108">Probar idiomas</span><span class="sxs-lookup"><span data-stu-id="aed71-108">Testing languages</span></span>

<span data-ttu-id="aed71-109">Para probar las cadenas de idioma, primero debe establecer el idioma de Windows en el idioma que quiera probar.</span><span class="sxs-lookup"><span data-stu-id="aed71-109">To test your language strings, you first need to set the Windows display language to the language that you want to test for.</span></span>

<span data-ttu-id="aed71-110">Siga los pasos que se indican a continuación para cambiar el idioma de Windows:</span><span class="sxs-lookup"><span data-stu-id="aed71-110">Follow the steps below to change the Windows display language:</span></span>

1. <span data-ttu-id="aed71-111">Abra la aplicación configuración.</span><span class="sxs-lookup"><span data-stu-id="aed71-111">Open the Settings app.</span></span>

   ![aplicación de configuración](./../media/loc-settings.png)
2. <span data-ttu-id="aed71-113">Selecciona "tiempo & idioma".</span><span class="sxs-lookup"><span data-stu-id="aed71-113">Select "Time & language".</span></span>
3. <span data-ttu-id="aed71-114">Selecciona "idioma & región".</span><span class="sxs-lookup"><span data-stu-id="aed71-114">Select "Region & language".</span></span>
4. <span data-ttu-id="aed71-115">Seleccione "+ agregar un idioma" para agregar el idioma a la lista de idiomas posibles.</span><span class="sxs-lookup"><span data-stu-id="aed71-115">Select "+ Add a language" to add the language to the list of possible languages.</span></span>
5. <span data-ttu-id="aed71-116">Elija el idioma de la lista "idiomas" que desea probar.</span><span class="sxs-lookup"><span data-stu-id="aed71-116">Choose the language from the "Languages" list that you want to test.</span></span>
6. <span data-ttu-id="aed71-117">Selecciona el botón "establecer como predeterminado" (es posible que tengas que reiniciar el equipo).</span><span class="sxs-lookup"><span data-stu-id="aed71-117">Select the "Set as default" button (you may need to restart your PC).</span></span>
7. <span data-ttu-id="aed71-118">Abra Microsoft Edge y compruebe que las cadenas definidas para la configuración regional aparecen de la forma esperada.</span><span class="sxs-lookup"><span data-stu-id="aed71-118">Open Microsoft Edge and verify that the strings defined for the locale appear as expected.</span></span>

<span data-ttu-id="aed71-119">Al usar la propiedad [NavigatorLanguage. Language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) , puede comprobar que el idioma que Microsoft Edge ha determinado como el idioma de Windows es correcto.</span><span class="sxs-lookup"><span data-stu-id="aed71-119">By using the [NavigatorLanguage.language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) property, you can verify that the language Microsoft Edge has determined to be the Windows display language is correct.</span></span>

<span data-ttu-id="aed71-120">Haz clic en el botón de la CodePen siguiente para ver el idioma de visualización de tu explorador.</span><span class="sxs-lookup"><span data-stu-id="aed71-120">Click the button in the CodePen below to see the display language of your browser.</span></span>

<iframe height='300' scrolling='no' title='<span data-ttu-id="aed71-121">Obtener configuración regional</span><span class="sxs-lookup"><span data-stu-id="aed71-121">Get locale</span></span>' src='//codepen.io/MSEdgeDev/embed/VaRWwR/?height=300&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="aed71-122">Consulta la pluma <a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'> para obtener la configuración regional </a> de MSEdgeDev ( <a href='http://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) en <a href='http://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="aed71-122">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'>Get locale</a>by MSEdgeDev (<a href='http://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='http://codepen.io'>CodePen</a>.</span></span>
</iframe>
