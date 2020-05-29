---
title: Información de versión de JavaScript
description: Comparar la compatibilidad con JavaScript en Microsoft Edge, en Microsoft Store y en Internet Explorer
ms.date: 03/05/2020
ms.prod: microsoft-edge
ms.topic: language-reference
author: MSEdgeTeam
ms.author: msedgedevrel
keywords: Edge, IE, Chakra, JScript, WWA, almacenar aplicaciones
ms.custom: seodec18
ms.openlocfilehash: 0edc5769cf80ae9a7ac741c0f478f9ca639d935f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573338"
---
# Información de versión de JavaScript  

La compatibilidad con JavaScript varía según Microsoft Edge, las aplicaciones de Microsoft Store y los distintos modos de documento de Internet Explorer. Para obtener más información sobre el control de versiones de código de documento de IE, consulte [*definir la compatibilidad de documentos*](https://go.microsoft.com/fwlink/p/?LinkId=208537).  

En la siguiente tabla se resume la compatibilidad de JavaScript en Internet Explorer, Microsoft Edge y las aplicaciones de Microsoft Store.  
  
> [!IMPORTANT]
> Las características experimentales \ (habilitado en *About: flags*\) están indicadas por "exp". En algunos casos, la compatibilidad de las aplicaciones de la *tienda* varía entre las aplicaciones Windows 8 \ (V8 \) y Windows 10 \ (V10 \), y el escritorio de Windows \ (Win \) y Windows Phone \ (teléfono \), tal como se indica.  
  
 | Elemento de lenguaje | Peculiaridades, estándares de Internet Explorer 6, estándares de Internet Explorer 7 | Estándares de Internet Explorer 8 | Estándares de Internet Explorer 9 | Estándares de Internet Explorer 10 | Estándares de Internet Explorer 11 | Microsoft Edge | Almacenar aplicaciones |  
 |:--- |:--- |:--- |:--- |:--- |:--- |:--- |:--- |  
| [__proto \ _ \ _ propiedad (objeto)](/scripting/javascript/reference/proto-property-object-javascript) | N | N | N | N | Y | Y | V8 (Win): N <br /> v 8.1 (Win): Y <br /> v 8.1 (teléfono): Y |  
| [$1... $9 propiedades (RegExp)](/scripting/javascript/reference/dollar-1-dot-dot-dot-dollar-9-properties-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propiedad 0n](/scripting/javascript/reference/0-dot-dot-dot-n-properties-arguments-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función ABS](/scripting/javascript/reference/math-abs-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función ACOS](/scripting/javascript/reference/math-acos-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función Acosh](/scripting/javascript/reference/math-acosh-function-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Objeto ActiveXObject](/scripting/javascript/reference/activexobject-object-javascript) | Y | Y | Y | Y | Y | Y | N |  
| [Operador de asignación y suma (+ =)](/scripting/javascript/reference/addition-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de suma (+)](/scripting/javascript/reference/addition-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Apply](/scripting/javascript/reference/apply-method-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto arguments](/scripting/javascript/reference/arguments-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [arguments (propiedad)](/scripting/javascript/reference/arguments-property-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto Array](/scripting/javascript/reference/array-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función array. from (matriz)](/scripting/javascript/reference/array-from-function-array-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Función array. isArray](/scripting/javascript/reference/array-isarray-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Array. of (matriz)](/scripting/javascript/reference/array-of-function-array-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Objeto ArrayBuffer](/scripting/javascript/reference/arraybuffer-object) | N | N | N | Y | Y | Y | Y |  
| [Funciones](/scripting/javascript/functions-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Función Asin](/scripting/javascript/reference/math-asin-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función Object. Assign (objeto)](/scripting/javascript/reference/object-assign-function-object-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Operador de asignación (=)](/scripting/javascript/reference/assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función atan](/scripting/javascript/reference/math-atan-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función ATAN2](/scripting/javascript/reference/math-atan2-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método atEnd](/scripting/javascript/reference/atend-method-enumerator-javascript) | Y | Y | Y | Y | Y | Y | N |  
| [Método BIND](/scripting/javascript/reference/bind-method-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Operador de asignación and bit a bit (&=)](/scripting/javascript/reference/bitwise-and-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador and bit a bit (&)](/scripting/javascript/reference/bitwise-and-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de desplazamiento a la izquierda bit a bit (< \ <)](/scripting/javascript/reference/bitwise-left-shift-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador NOT bit a bit (~)](/scripting/javascript/reference/bitwise-not-operator-decrement-tilde-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de asignación OR bit a bit (&#124;=)](/scripting/javascript/reference/bitwise-or-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador OR bit a bit (&#124;)](/scripting/javascript/reference/bitwise-or-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de desplazamiento a la derecha bit a bit (>>)](/scripting/javascript/reference/bitwise-right-shift-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de asignación de tu bit a bit (^ =)](/scripting/javascript/reference/bitwise-xor-assignment-operator-decrement-hat-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de tu bit a bit (^)](/scripting/javascript/reference/bitwise-xor-operator-decrement-hat-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Blink (método)](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Bold (método)](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto Boolean](/scripting/javascript/reference/boolean-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrucción break](/scripting/javascript/reference/break-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método de llamada](/scripting/javascript/reference/call-method-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propiedad de destinatario](/scripting/javascript/reference/callee-property-arguments-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propiedad de llamador](/scripting/javascript/reference/caller-property-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrucción Catch](/scripting/javascript/reference/try-dot-dot-dot-catch-dot-dot-dot-finally-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función Ceil](/scripting/javascript/reference/math-ceil-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método charAt](/scripting/javascript/reference/charat-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método charCodeAt](/scripting/javascript/reference/charcodeat-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrucción Class](/scripting/javascript/reference/class-statement-javascript) | N | N | N | N | N | Exp. | v 8.1: N <br /> V10: EXP. |  
| [Método codePointAt (cadena)](/scripting/javascript/reference/codepointat-method-string-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Operador de comas (,)](/scripting/javascript/reference/comma-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [(Instrucción de comentario de una sola línea)](/scripting/javascript/reference/comment-statements-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [/*.. \ */(Instrucción de comentario de varias líneas)](/scripting/javascript/reference/comment-statements-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operadores de comparación](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método compile](/scripting/javascript/reference/compile-method-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método concat (matriz)](/scripting/javascript/reference/concat-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método concat (cadena)](/scripting/javascript/reference/concat-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Compilación condicional](/scripting/javascript/advanced/conditional-compilation-javascript) | Y | Y | Y | Y | N | N | N |  
| [Variables de compilación condicional](/scripting/javascript/advanced/conditional-compilation-variables-javascript) | Y | Y | Y | Y | N | N | N |  
| [Operador condicional ternario (?:)](/scripting/javascript/reference/conditional-ternary-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [constructor (propiedad)](/scripting/javascript/reference/constructor-property-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrucción const](/scripting/javascript/reference/const-statement-javascript) | N | N | N | N | Y | Y | V8 (Win): N <br /> v 8.1 (Win): Y <br /> v 8.1 (teléfono): Y |  
| [Instrucción continue](/scripting/javascript/reference/continue-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función cos](/scripting/javascript/reference/math-cos-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [crear función](/scripting/javascript/reference/object-create-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Objeto DataView](/scripting/javascript/reference/dataview-object) | N | N | N | Y | Y | Y | Y |  
| [Objeto Date](/scripting/javascript/reference/date-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Depurar objeto](/scripting/javascript/reference/debug-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propiedad Debug. setNonUserCodeExceptions](/scripting/javascript/reference/debug-setnonusercodeexceptions-property) | N | N | N | Y | Y | Y | Y |  
| [Propiedad Debug. setNonUserCodeExceptions](/scripting/javascript/reference/debug-setnonusercodeexceptions-property) | N | N | N | Y | Y | Y | Y |  
| [Instrucción Debugger](/scripting/javascript/reference/debugger-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función decodeURI](/scripting/javascript/reference/decodeuri-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función DecodeURIComponent](/scripting/javascript/reference/decodeuricomponent-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de decremento (--)](/scripting/javascript/reference/increment-and-decrement-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Funciones](/scripting/javascript/functions-javascript) | N | N | N | N | N | Exp. | v 8.1: N <br /> V10: EXP. |  
| [Función defineProperties](/scripting/javascript/reference/object-defineproperties-function-javascript) | N | Ordenada | Y | Y | Y | Y | Y |  
| [Función defineProperty](/scripting/javascript/reference/object-defineproperty-function-javascript) | N | Ordenada | Y | Y | Y | Y | Y |  
| [eliminar operador](/scripting/javascript/reference/delete-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Descripción (propiedad)](/scripting/javascript/reference/description-property-error-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Dimensions](/scripting/javascript/reference/dimensions-method-vbarray-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de asignación y división (/=)](/scripting/javascript/reference/division-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de división (/)](/scripting/javascript/reference/division-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [do... Instrucción while](/scripting/javascript/reference/do-dot-dot-dot-while-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante E](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función encodeURI](/scripting/javascript/reference/encodeuri-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función de componente encodeURI](/scripting/javascript/reference/encodeuricomponent-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Entries (matriz)](/scripting/javascript/reference/entries-method-array-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Objeto Enumerator](/scripting/javascript/reference/enumerator-object-javascript) | Y | Y | Y | Y | Y | Y | N |  
| [Constantes de número](/scripting/javascript/reference/number-constants-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Operador de igualdad (= =)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto de error](/scripting/javascript/reference/error-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propiedad stack (error)](/scripting/javascript/reference/stack-property-error-javascript) | N | N | N | Y | Y | Y | Y |  
| [Propiedad stackTraceLimit (error)](/scripting/javascript/reference/stacktracelimit-property-error-javascript) | N | N | N | Y | Y | Y | Y |  
| [Función escape](/scripting/javascript/reference/escape-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función eval](/scripting/javascript/reference/eval-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Exec](/scripting/javascript/reference/exec-method-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [todos los métodos](/scripting/javascript/reference/every-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Función exp](/scripting/javascript/reference/math-exp-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Fill (método) (matriz)](/scripting/javascript/reference/fill-method-array-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Método de filtro](/scripting/javascript/reference/filter-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Instrucción Finally](/scripting/javascript/reference/try-dot-dot-dot-catch-dot-dot-dot-finally-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [findIndex (método) (matriz)](/scripting/javascript/reference/findindex-method-array-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Método Fixed](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto Float32Array](/scripting/javascript/reference/float32array-object) | N | N | N | Y | Y | Y | Y |  
| [Objeto Float64Array](/scripting/javascript/reference/float64array-object) | N | N | N | Y | Y | Y | Y |  
| [Función MULTIPLO. inferior](/scripting/javascript/reference/math-floor-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [fontcolor (método)](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [FontSize (método)](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrucción for](/scripting/javascript/reference/for-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método forEach](/scripting/javascript/reference/foreach-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [para... in (instrucción)](/scripting/javascript/reference/for-dot-dot-dot-in-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [para... de instrucción](/scripting/javascript/reference/for-dot-dot-dot-of-statement-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Función Freeze](/scripting/javascript/reference/object-freeze-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Función fromCharCode](/scripting/javascript/reference/string-fromcharcode-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función fromCodePoint](/scripting/javascript/reference/string-fromcodepoint-function-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Objeto de función](/scripting/javascript/reference/function-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrucción function](/scripting/javascript/reference/function-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Productores](/scripting/javascript/advanced/iterators-and-generators-javascript) | N | N | N | N | N | Exp. | v 8.1: N <br /> V10: EXP. |  
| [getDate (método)](/scripting/javascript/reference/getdate-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getDay](/scripting/javascript/reference/getday-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [getFullYear (método)](/scripting/javascript/reference/getfullyear-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getHours](/scripting/javascript/reference/gethours-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [getItem (método)](/scripting/javascript/reference/getitem-method-vbarray-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [getMilliseconds (método)](/scripting/javascript/reference/getmilliseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [getMinutes (método)](/scripting/javascript/reference/getminutes-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getMonth](/scripting/javascript/reference/getmonth-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función GetObject](/scripting/javascript/reference/getobject-function-javascript) | Y | Y | N | N | N | N | N |  
| [Función getOwnPropertyDescriptor](/scripting/javascript/reference/object-getownpropertydescriptor-function-javascript) | N | Ordenada | Y | Y | Y | Y | Y |  
| [Función getOwnPropertyNames](/scripting/javascript/reference/object-getownpropertynames-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Función getPrototypeOf](/scripting/javascript/reference/object-getprototypeof-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [getSeconds (método)](/scripting/javascript/reference/getseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getTime](/scripting/javascript/reference/gettime-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getTimezoneOffset](/scripting/javascript/reference/gettimezoneoffset-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [getUTCDate (método)](/scripting/javascript/reference/getutcdate-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getUTCDay](/scripting/javascript/reference/getutcday-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getUTCFullYear](/scripting/javascript/reference/getutcfullyear-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getUTCHours](/scripting/javascript/reference/getutchours-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getUTCMilliseconds](/scripting/javascript/reference/getutcmilliseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getUTCMinutes](/scripting/javascript/reference/getutcminutes-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getUTCMonth](/scripting/javascript/reference/getutcmonth-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [getUTCSeconds (método)](/scripting/javascript/reference/getutcseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getVarDate](/scripting/javascript/reference/getvardate-method-date-javascript) | Y | Y | Y | Y | Y | Y | N |  
| [getYear (método)](/scripting/javascript/reference/getyear-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto global](/scripting/javascript/reference/global-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propiedad global](/scripting/javascript/reference/global-property-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador mayor que (>)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador mayor o igual que (>=)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método hasOwnProperty](/scripting/javascript/reference/hasownproperty-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Métodos de etiquetas HTML](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función hypot](/scripting/javascript/reference/math-hypot-function-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Operador de identidad (= = =)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Si... Instrucción else](/scripting/javascript/reference/if-dot-dot-dot-else-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [ignoreCase (propiedad)](/scripting/javascript/reference/ignorecase-property-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función imul](/scripting/javascript/reference/math-imul-function-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Operador in](/scripting/javascript/reference/in-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [incluye el método (cadena)](/scripting/javascript/reference/includes-method-string-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Operador de incremento (+ +)](/scripting/javascript/reference/increment-and-decrement-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [index (propiedad)](/scripting/javascript/reference/index-property-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método IndexOf (matriz)](/scripting/javascript/reference/indexof-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método IndexOf (String)](/scripting/javascript/reference/indexof-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de desigualdad (! =)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante de infinito](/scripting/javascript/reference/infinity-constant-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Input Property ($ _)](/scripting/javascript/reference/input-property-dollar-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador instanceof](/scripting/javascript/reference/instanceof-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto Int8Array](/scripting/javascript/reference/int8array-object) | N | N | N | Y | Y | Y | Y |  
| [Objeto Int16Array](/scripting/javascript/reference/int16array-object) | N | N | N | Y | Y | Y | Y |  
| [Objeto Int32Array](/scripting/javascript/reference/int32array-object) | N | N | N | Y | Y | Y | Y |  
| [Objeto de Collator Intl. Collator](/scripting/javascript/reference/intl-collator-object-javascript) | N | N | N | N | Y | Y | V8 (Win): N <br /> v 8.1 (Win): Y <br /> v 8.1 (teléfono): Y |  
| [Objeto Intl. DateTimeFormat](/scripting/javascript/reference/intl-datetimeformat-object-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Objeto Intl. NumberFormat](/scripting/javascript/reference/intl-numberformat-object-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Función isFinite](/scripting/javascript/reference/isfinite-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función isArray](/scripting/javascript/reference/array-isarray-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Función IsExtensible](/scripting/javascript/reference/object-isextensible-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Función isFrozen](/scripting/javascript/reference/object-isfrozen-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Función isInteger](/scripting/javascript/reference/number-isinteger-function-number-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Función isNaN](/scripting/javascript/reference/isnan-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función isNaN (número)](/scripting/javascript/reference/number-isnan-function-number-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Formato de fecha ISO](/scripting/javascript/date-and-time-strings-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método IsPrototypeOf](/scripting/javascript/reference/isprototypeof-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función isSealed](/scripting/javascript/reference/object-issealed-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Italic (método)](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Iteradores](/scripting/javascript/advanced/iterators-and-generators-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Método Item](/scripting/javascript/reference/item-method-enumerator-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método join](/scripting/javascript/reference/join-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto JSON](/scripting/javascript/reference/json-object-javascript) | N | Y | Y | Y | Y | Y | Y |  
| [Función Keys](/scripting/javascript/reference/object-keys-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método Keys (matriz)](/scripting/javascript/reference/keys-method-array-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Instrucción con etiqueta](/scripting/javascript/reference/labeled-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [lastIndex (propiedad)](/scripting/javascript/reference/lastindex-property-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método lastIndexOf (matriz)](/scripting/javascript/reference/lastindexof-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método lastIndexOf (cadena)](/scripting/javascript/reference/lastindexof-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [lastMatch ($&)](/scripting/javascript/reference/lastmatch-property-dollar-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [lastParen ($ +) (propiedad)](/scripting/javascript/reference/lastparen-property-dollar-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método LBound](/scripting/javascript/reference/lbound-method-vbarray-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propiedad leftContext ($ ')](/scripting/javascript/reference/leftcontext-property-dollar-grave-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de asignación de desplazamiento a la izquierda (<<=)](/scripting/javascript/reference/left-shift-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Length (propiedad, argumentos)](/scripting/javascript/reference/length-property-arguments-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Length (propiedad, matriz)](/scripting/javascript/reference/length-property-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Length (propiedad, función)](/scripting/javascript/reference/length-property-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Length (propiedad, String)](/scripting/javascript/reference/length-property-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador menor que (<)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador menor o igual que (<=)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrucción Let](/scripting/javascript/reference/let-statement-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Link (método)](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante LN2](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante LN10](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método localeCompare](/scripting/javascript/reference/localecompare-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función log](/scripting/javascript/reference/math-log-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante LOG2E](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante LOG10E](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador lógico AND (&&)](/scripting/javascript/reference/logical-and-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador lógico NOT (!)](/scripting/javascript/reference/logical-not-operator-decrement-exclpt-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador lógico OR (&#124;&#124;)](/scripting/javascript/reference/logical-or-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Map (método)](/scripting/javascript/reference/map-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Objeto Map](/scripting/javascript/reference/map-object-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Método match](/scripting/javascript/reference/match-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto Math](/scripting/javascript/reference/math-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función Max](/scripting/javascript/reference/math-max-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [MAX_VALUE constante](/scripting/javascript/reference/number-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propiedad de mensaje](/scripting/javascript/reference/message-property-error-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función min](/scripting/javascript/reference/math-min-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [MIN_VALUE constante](/scripting/javascript/reference/number-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de asignación de resto (% =)](/scripting/javascript/reference/modulus-assignment-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de resto (%)](/scripting/javascript/reference/modulus-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método moveFirst](/scripting/javascript/reference/movefirst-method-enumerator-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método moveNext](/scripting/javascript/reference/movenext-method-enumerator-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propiedad Multiline](/scripting/javascript/reference/multiline-property-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de asignación de multiplicación (* =)](/scripting/javascript/reference/multiplication-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de multiplicación (*)](/scripting/javascript/reference/multiplication-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Name (propiedad)](/scripting/javascript/reference/name-property-error-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante NaN (global)](/scripting/javascript/reference/nan-constant-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [NaN (constante) (número)](/scripting/javascript/reference/number-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [NEGATIVE_INFINITY constante](/scripting/javascript/reference/number-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [nuevo operador](/scripting/javascript/reference/new-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de no identidad (! = =)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función Now](/scripting/javascript/reference/date-now-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Objeto Number](/scripting/javascript/reference/number-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Number (propiedad)](https://developer.mozilla.org/docs/Web/JavaScript/Microsoft_Extensions/Error.number) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto Object](/scripting/javascript/reference/object-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Prioridad de operador](/scripting/javascript/operator-subtractprecedence-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función Date. Parse](/scripting/javascript/reference/date-parse-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función JSON. Parse](/scripting/javascript/reference/json-parse-function-javascript) | N | Y | Y | Y | Y | Y | Y |  
| [Función parseFloat](/scripting/javascript/reference/parsefloat-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [parseInt (función)](/scripting/javascript/reference/parseint-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante PI](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Pop](/scripting/javascript/reference/pop-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [POSITIVE_INFINITY constante](/scripting/javascript/reference/number-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Pow (función)](/scripting/javascript/reference/math-pow-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función preventExtensions](/scripting/javascript/reference/object-preventextensions-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Objeto Promise](/scripting/javascript/reference/promise-object-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Propiedad prototype](/scripting/javascript/reference/prototype-property-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método propertyIsEnumerable](/scripting/javascript/reference/propertyisenumerable-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto proxy](/scripting/javascript/reference/proxy-object-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Método push](/scripting/javascript/reference/push-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función RANDOM](/scripting/javascript/reference/math-random-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función RAW](/scripting/javascript/reference/string-raw-function-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Método reducir](/scripting/javascript/reference/reduce-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método reduceRight](/scripting/javascript/reference/reduceright-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Objeto RegExp](/scripting/javascript/reference/regexp-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto regular Expression](/scripting/javascript/reference/regular-expression-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Sintaxis de las expresiones regulares](https://msdn.microsoft.com/ab0766e1-7037-45ed-aa23-706f58358c0e) | Y | Y | Y | Y | Y | Y | Y |  
| [Marcador de expresión regular/y](/scripting/javascript/reference/regular-expression-object-javascript) | N | N | N | N | N | Exp. | v 8.1: N <br /> V10: EXP. |  
| [Método REPEAT (cadena)](/scripting/javascript/reference/repeat-method-string-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Método Replace](/scripting/javascript/reference/replace-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Funciones](/scripting/javascript/functions-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Instrucción return](/scripting/javascript/reference/return-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Reverse](/scripting/javascript/reference/reverse-method-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [rightContext ($ ') (propiedad)](/scripting/javascript/reference/rightcontext-property-dollar-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de asignación de desplazamiento a la derecha (>>=)](/scripting/javascript/reference/right-shift-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función redondear](/scripting/javascript/reference/math-round-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [ScriptEngine (función)](/scripting/javascript/reference/scriptengine-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [ScriptEngineBuildVersion (función)](/scripting/javascript/reference/scriptenginebuildversion-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [ScriptEngineMajorVersion (función)](/scripting/javascript/reference/scriptenginemajorversion-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [ScriptEngineMinorVersion (función)](/scripting/javascript/reference/scriptengineminorversion-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función Seal](/scripting/javascript/reference/object-seal-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método de búsqueda](/scripting/javascript/reference/search-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Definir objeto](/scripting/javascript/reference/set-object-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Método setDate](/scripting/javascript/reference/setdate-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [setFullYear (método)](/scripting/javascript/reference/setfullyear-method-date-javascript) |  | Y | Y | Y | Y | Y | Y |  
| [Método setHours](/scripting/javascript/reference/sethours-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setMilliseconds](/scripting/javascript/reference/setmilliseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setMinutes](/scripting/javascript/reference/setminutes-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setMonth](/scripting/javascript/reference/setmonth-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setSeconds](/scripting/javascript/reference/setseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [setTime (método)](/scripting/javascript/reference/settime-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setUTCDate](/scripting/javascript/reference/setutcdate-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setUTCFullYear](/scripting/javascript/reference/setutcfullyear-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setUTCHours](/scripting/javascript/reference/setutchours-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setUTCMilliseconds](/scripting/javascript/reference/setutcmilliseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setUTCMinutes](/scripting/javascript/reference/setutcminutes-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setUTCMonth](/scripting/javascript/reference/setutcmonth-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setUTCSeconds](/scripting/javascript/reference/setutcseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setYear](/scripting/javascript/reference/setyear-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Shift](/scripting/javascript/reference/shift-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función seno](/scripting/javascript/reference/math-sin-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método slice (matriz)](/scripting/javascript/reference/slice-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método slice (cadena)](/scripting/javascript/reference/slice-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método pequeño](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [algún método](/scripting/javascript/reference/some-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método sort](/scripting/javascript/reference/sort-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propiedad Source](/scripting/javascript/reference/source-property-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Splice](/scripting/javascript/reference/splice-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Split](/scripting/javascript/reference/split-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Funciones](/scripting/javascript/functions-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Función sqrt](/scripting/javascript/reference/math-sqrt-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [SQRT1_2 constante](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante SQRT2](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [usar la Directiva STRICT](/scripting/javascript/reference/use-strict-directive) | N | N | N | Y | Y | Y | Y |  
| [Strike (método)](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto String](/scripting/javascript/reference/string-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función JSON. stringify](/scripting/javascript/reference/json-stringify-function-javascript) | N | Y | Y | Y | Y | Y | Y |  
| [Sub (método)](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [substr (método)](/scripting/javascript/reference/substr-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método substring](/scripting/javascript/reference/substring-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de asignación y resta (-=)](/scripting/javascript/reference/subtraction-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de resta (-)](/scripting/javascript/reference/subtraction-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [SUP (método)](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrucción switch](/scripting/javascript/reference/switch-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto Symbol](/scripting/javascript/reference/symbol-object-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Función tan](/scripting/javascript/reference/math-tan-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Cadenas de plantilla](/scripting/javascript/advanced/template-strings-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Método de prueba](/scripting/javascript/reference/test-method-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Esta declaración](/scripting/javascript/reference/this-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrucción throw](/scripting/javascript/reference/throw-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [toArray (método)](/scripting/javascript/reference/toarray-method-vbarray-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toDateString](/scripting/javascript/reference/todatestring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [toExponential (método)](/scripting/javascript/reference/toexponential-method-number-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toFixed](/scripting/javascript/reference/tofixed-method-number-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toGMTString](/scripting/javascript/reference/togmtstring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toISOString](/scripting/javascript/reference/toisostring-method-date-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método toJSON](/scripting/javascript/reference/tojson-method-date-javascript) | N | Y | Y | Y | Y | Y | Y |  
| [Método toLocaleDateString](/scripting/javascript/reference/tolocaledatestring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toLocaleLowercase](/scripting/javascript/reference/tolocalelowercase-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [toLocaleString (método)](/scripting/javascript/reference/tolocalestring-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toLocaleTimeString](/scripting/javascript/reference/tolocaletimestring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toLocaleUppercase](/scripting/javascript/reference/tolocaleuppercase-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toLowerCase](/scripting/javascript/reference/tolowercase-method-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [toPrecision (método)](/scripting/javascript/reference/toprecision-method-number-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toString](/scripting/javascript/reference/tostring-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toTimeString](/scripting/javascript/reference/totimestring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toUpperCase](/scripting/javascript/reference/touppercase-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [toUTCString (método)](/scripting/javascript/reference/toutcstring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método trim](/scripting/javascript/reference/trim-method-string-javascript) | N | N | Y | Y | Y | Y | Y |  
| [try (instrucción)](/scripting/javascript/reference/try-dot-dot-dot-catch-dot-dot-dot-finally-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador typeof](/scripting/javascript/reference/typeof-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [UBound (método)](/scripting/javascript/reference/ubound-method-vbarray-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto Uint8Array](/scripting/javascript/reference/uint8array-object) | N | N | N | Y | Y | Y | Y |  
| [Objeto Uint16Array](/scripting/javascript/reference/uint16array-object) | N | N | N | Y | Y | Y | Y |  
| [Objeto Uint32Array](/scripting/javascript/reference/uint32array-object) | N | N | N | Y | Y | Y | Y |  
| [Objeto Uint8ClampedArray](/scripting/javascript/reference/uint8clampedarray-object-javascript) | N | N | N | N | Y | Y | V8: no <br /> v 8.1 (Win): sí <br /> v 8.1 (teléfono): no <br /> V10: Y |  
| [Operador unario de negación (-)](/scripting/javascript/reference/subtraction-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante no definida](/scripting/javascript/reference/undefined-constant-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función unescape](/scripting/javascript/reference/unescape-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Caracteres de escape de puntos de código Unicode](/scripting/javascript/advanced/special-characters-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Método unshift](/scripting/javascript/reference/unshift-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de asignación y desplazamiento a la derecha sin signo (>>>=)](/scripting/javascript/reference/unsigned-right-shift-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de desplazamiento a la derecha sin signo (>>>)](/scripting/javascript/reference/unsigned-right-shift-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [usar la Directiva STRICT](/scripting/javascript/reference/use-strict-directive) | N | N | N | Y | Y | Y | Y |  
| [Función UTC](/scripting/javascript/reference/date-utc-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método valueto](/scripting/javascript/reference/valueof-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Values (matriz)](/scripting/javascript/reference/values-method-array-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Instrucción var](/scripting/javascript/reference/var-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto VBArray](/scripting/javascript/reference/vbarray-object-javascript) | Y | Y | Y | Y | Y | Y | N |  
| [Operador void](/scripting/javascript/reference/void-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto WeakMap](/scripting/javascript/reference/weakmap-object-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Objeto WeakSet](/scripting/javascript/reference/weakset-object-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Instrucción while](/scripting/javascript/reference/while-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto WinRTError](/scripting/javascript/reference/winrterror-object-javascript) | N | N | N | Y | Y | Y | Y |  
| [Instrucción with](/scripting/javascript/reference/with-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Función Write](/scripting/javascript/reference/debug-write-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [writeln (función)](/scripting/javascript/reference/debug-writeln-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
  
 \ * Admite objetos DOM, pero no objetos definidos por el usuario.  Los `enumerable` atributos y se `configurable` pueden especificar, pero no se usan.  
