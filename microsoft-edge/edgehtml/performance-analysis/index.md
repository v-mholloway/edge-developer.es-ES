---
description: Use las herramientas de desarrollo F12 para analizar el rendimiento general de los sitios Web.
title: Análisis de rendimiento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 7a5f9fd0-90a9-43db-b271-178c06da5896
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e585d07ebae547319c16b6eea579ad26ffb84ce3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236390"
---
# Análisis de rendimiento  

Si no está familiarizado con el rendimiento, debe consultar la [Guía de F12 DevTools](../devtools-guide/index.md).
Las [herramientas F12](../devtools-guide/index.md) integradas en Microsoft Edge se pueden usar para analizar el rendimiento general de un sitio Web.  Proporciona capacidades similares (pero más limitadas) a [Windows performance Toolkit](/windows-hardware/test/wpt/index) desde el mismo derecho en el explorador.  

Si desea un análisis más profundo del rendimiento del explorador, el equipo de Microsoft Edge usa el [Windows performance Toolkit](/windows-hardware/test/wpt/index) (WPT).  WPT fue creado por el equipo de Windows para realizar un análisis exhaustivo del rendimiento del programa.  Abarca los límites entre JavaScript del sitio web y el código nativo de Microsoft Edge, lo que permite que se puedan ver en la misma herramienta.  WPT se puede usar para:  

*   Medir el tiempo de CPU de que se toma el software para completar el trabajo  
*   Calcular la memoria asignada por el software  
*   Mostrar los detalles de descarga de archivos desde servidores remotos  
*   Medir la velocidad de fotogramas.  

Para empezar a usar el kit de rendimiento de Windows para analizar su sitio web, primero deberá descargar [Windows 10 Assessment and Deployment Kit (ADK)](https://developer.microsoft.com/windows/hardware/windows-assessment-deployment-kit).  Seleccione la opción *Windows performance Toolkit* durante la instalación:  

![Opciones de instalación de ADK](./media/adk-installoptions.png)  

Aquí describiremos cómo grabar y analizar un seguimiento de rendimiento.  
Para obtener más información sobre lo que se incluye en el kit de herramientas de rendimiento de Windows, consulte la documentación completa de [WPT](/windows-hardware/test/wpt/index).  

## Grabar un seguimiento  

A continuación, configure el escenario de usuario y prepárese para recopilar una traza con la grabadora de rendimiento de Windows.  
A continuación se explica cómo generar perfiles de su escenario web con la *grabadora de rendimiento de Windows (WPR)*.  

### 1. preparar el entorno para recopilar un seguimiento de rendimiento  

Cierre todos los programas que se estén ejecutando para evitar el ruido en la traza que va a grabar.  Idealmente, el único software en ejecución será Windows performance Recorder (WPR) y el explorador.  

### 2. Inicie el grabador de rendimiento de Windows (WPR) y seleccione las opciones  

Inicie el grabador de rendimiento de Windows y asegúrese de que esté expandida la **opción más opciones** de alternancia.  Seleccione las casillas *Explorador perimetral* y análisis de escenario de *respuesta html* .  

![Opciones de registro de rendimiento de Windows](./media/wprui-options.png)  

#### Sugerencias y trucos para recopilar seguimientos  

*   Intenta mantener la actividad en segundo plano en un valor mínimo requerido.  Los procesos en segundo plano pueden sesgar el rendimiento percibido y las características de rendimiento real y afectar a los resultados.  Lo ideal es que no haya otras aplicaciones en ejecución junto al explorador y la WPR.  
*   Identifique los escenarios que está analizando e intente mantenerlos lo más atómicos posible.  Por ejemplo, si su sitio tiene problemas de rendimiento al cargar la página, desplazarse y seleccionar algo en una tabla, separe los problemas en tres escenarios:  
    *   Carga de página (desde el inicio de la navegación a la carga de página completada)  
    *   Scroll  
    *   Selección de algo en la tabla  
*   Si un escenario implica navegar hasta un sitio, considere la posibilidad de comenzar el escenario en acerca de: en blanco.  Empezando por: Blank evitará la sobrecarga de la página anterior.  Si implica navegar fuera de un sitio, vaya a acerca de: en blanco para completar el escenario.  Esto mantendrá el ruido de otros sitios fuera del seguimiento, a menos que la interacción específica entre los sitios sea el problema en investigación.  

### 3. grabar el escenario  

Haga clic en **iniciar** para empezar a grabar.  La herramienta informará el tamaño del búfer que está usando para ayudarle a prever el tamaño del archivo generado.  Realice el escenario de usuario que desea medir y, a continuación, haga clic en **Guardar** para detener la grabación y guardar el seguimiento.  Guardar inmediatamente después de finalizar el escenario le ayudará a minimizar el tamaño del archivo de seguimiento.  

![Inicio de grabación de rendimiento de Windows](./media/wprui-recording.png)  

La herramienta WPR indica que la información de seguimiento se ha guardado correctamente:  

![Inicio de registro de rendimiento de Windows: guardado completado](./media/wprui-savecomplete.png)  

## Analizar un seguimiento  

Ahora que ha recopilado los datos de rendimiento, puede analizar el seguimiento con el analizador de rendimiento de Windows para ver qué optimizaciones se pueden realizar.  
A continuación se explica cómo analizar los datos de rendimiento de su escenario Web.  

### 1. abrir el analizador de rendimiento de Windows (WPA)  

Inicie el analizador de rendimiento de Windows y abra el `.etl` archivo que se va a analizar (**archivo**  >  **abierto...**).  

### 2. cargar símbolos y aplicar el perfil de *análisis HTML*  

> [!WARNING]
> La carga de símbolos por primera vez necesitará una descarga grande y tardará mucho tiempo en una conexión a Internet normal.  

Cargue los símbolos seleccionando **seguimiento**  >  de los**símbolos de carga** en el menú.  Los símbolos se almacenarán en la caché de disco y las trazas futuras cargarán los símbolos mucho más rápido.  

Puede cargar símbolos mucho más rápido si limita la carga a Microsoft Edge y al host de aplicaciones Web.  Seleccione **seguimiento**  >  **configurar símbolos** y restrinja la **configuración de carga** a solo `MicrosoftEdgeCP.exe` y `WWAHost.exe` .  

![Restricciones de símbolos](./media/wpa-symbolrestrictions.png)  

Una vez que los símbolos comienzan a cargarse, aplica el *Perfil de análisis HTML* (se aplican los**perfiles**  >  **...**  >  **Examinar catálogo...**  >  **HtmlResponsivenessAnalysis. wpaProfile**)  
El perfil cargará varios gráficos y tablas para el análisis.  Para casi todas las investigaciones de sitios web, recomendamos comenzar con este perfil.  

![Panorama general](./media/wpa-bigpicture.png)  

#### Perfil de análisis de respuesta HTML  

El perfil de análisis de la *respuesta HTML* proporciona cuatro pestañas:  

**Panorama general** : es útil para confirmar que no hay orígenes inesperados de actividad de la CPU y que el explorador usa todos los recursos disponibles.  Compruebe el uso de la CPU y asegúrese de que ningún proceso contribuya significativamente al uso de la CPU que no sea el explorador.  

**Análisis de tramas** : esta sección se usa para análisis básicos.  El gráfico *uso de CPU (con atributos)* permite comprender rápidamente los subsistemas responsables del uso de la CPU.  Dividir los ejemplos en la tabla de *uso de CPU (muestreada)* en el *subproceso de interfaz de usuario html* es útil para identificar cuellos de botella de rendimiento crítico.  

**Marcadores de seguimiento** : esta sección muestra todos los marcadores de seguimiento provenientes del explorador (Microsoft Edge), incluido *msWriteProfilerMark*, que proporciona puntos precisos para medir el código.  Para ver el seguimiento de *msWriteProfilerMark* , desplácese hacia abajo hasta el gráfico  *eventos genéricos* y seleccione **HTML msWriteProfilerMark** en el menú desplegable.  

**Análisis de retardo de subprocesos** : los programadores de Microsoft Edge suelen usar esta pestaña para investigar Cuándo un subproceso está bloqueado y en espera.  En raras ocasiones, también puede ser útil para los programadores de Internet.  

### 3. zoom para quitar el informe detallado de seguimiento  

Para centrar el análisis, quite las secciones de *Resumen de seguimiento* finales vacías de los gráficos.  Desde cualquiera de los gráficos que se muestran en ese momento:  
*   Haga clic en el inicio de los datos del gráfico que desea investigar  
*   Espera, arrastra y suelta para seleccionar la región deseada  
*   Haga clic con el botón derecho y seleccione **zoom**  

El zoom se aplicará a todos los gráficos y gráficos de la pestaña activa.  

![Zoom posterior](./media/wpa-postzoom.png)  

### 4. investigar qué está ocupando los ciclos de CPU  

 La tabla uso de la **CPU (muestreada)** en la pestaña **análisis de trama** es donde probablemente ocurrirá la mayor parte del análisis.  Puede expandir los distintos procesos para identificar el código JavaScript y del explorador más intensivo de Compute.  A menudo, un único bit de JavaScript es responsable de un problema de rendimiento y tomarse el tiempo para optimizarlo puede hacer una diferencia significativa.  

### 5. profundice en cualquier código JavaScript de baja velocidad  

Conclusión el análisis de la llamada DOM puede resultar útil para identificar al código de JavaScript responsable de tomar la mayoría de tiempo durante el escenario.  Esto es especialmente útil cuando muchas de las llamadas de nivel superior vuelven a usar las mismas bibliotecas de JavaScript.  

Empiece por mirar el *uso de la CPU (muestreada) por proceso, subproceso, actividad, pila*.  Haga clic en cualquier celda de la columna **pila** .  Presione *Ctrl + F* y busque *ExternalFunctionThunk*.  

> [!NOTE] 
> Esto solo funciona si ha cargado correctamente los símbolos.  

![Buscar ExternalFunctionThunk](./media/wpa-externalfunctionthunk.png)  

Investigue las líneas con *ExternalFunctionThunk*.  Esta es la interfaz del motor de JavaScript de Chakra al motor de Microsoft Edge.  Muestra dónde se relaciona el código del explorador con la ejecución de JavaScript.  Haga clic con el botón derecho en la línea y seleccione **Ver destinatarios**  >  **por módulo** para ver una lista ponderada de las funciones más largas del motor de explorador.  

![Ver destinatarios](./media/wpa-viewcallees.png)  

Para identificar todo el código JavaScript que llama a una API específica, haga clic con el botón derecho en ella y seleccione **ver llamadas**  >  **por función** y expanda el árbol para ver y comparar los pesos relativos.  
