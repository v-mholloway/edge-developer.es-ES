# <a name="microsoft-edge-documentation"></a>Documentación de Microsoft Edge  

## <a name="microsoft-open-source-code-of-conduct"></a>Código de conducta de Microsoft Open Source  

Este proyecto ha adoptado el Código de [conducta de Código de código abierto de Microsoft](https://opensource.microsoft.com/codeofconduct).  
Para obtener más información, consulte [las preguntas](https://opensource.microsoft.com/codeofconduct/faq) más frecuentes sobre código de conducta o póngase en [contacto opencode@microsoft.com](mailto:opencode@microsoft.com) con cualquier pregunta o comentario adicional.  

## <a name="legal-notices"></a>Avisos legales  

Microsoft y los colaboradores le conceden una licencia para la documentación de Microsoft y otro contenido de este repositorio bajo la Licencia pública internacional de [Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/legalcode), navegue hasta el archivo [LICENSE](./LICENSE) y le conceda una licencia para cualquier código del repositorio bajo la licencia [MIT](https://opensource.org/licenses/MIT), navegue hasta el archivo [LICENSE-CODE.](./LICENSE-CODE)  

Microsoft, Windows, Microsoft Azure y otros productos y servicios Microsoft a los que se hace referencia en la documentación pueden ser marcas comerciales o marcas registradas de Microsoft en los Estados Unidos y en otros países o regiones.  
Las licencias para este proyecto no te conceden derechos para usar los nombres, logotipos o marcas comerciales de Microsoft.  
Las directrices generales de marcas comerciales de Microsoft pueden encontrarse en [https://go.microsoft.com/fwlink/?LinkID=254653](https://go.microsoft.com/fwlink/?LinkID=254653) .  

La información de privacidad se puede encontrar en [https://privacy.microsoft.com](https://privacy.microsoft.com) .  

Microsoft y sus colaboradores se reservan todos los demás derechos, ya sea bajo sus respectivos derechos de autor, patentes o marcas comerciales, y tanto de manera implícita, explícita como de otro modo.  

## <a name="contributing"></a>Contribuir  

Este es el repositorio de documentación **de** Microsoft Edge hospedado en [https://docs.microsoft.com/microsoft-edge/](https://docs.microsoft.com/microsoft-edge/index) .  

Si desea incluir una nueva cobertura o recibir comentarios, considere la posibilidad de [contribuir](./CONTRIBUTING.md).  Puede editar el contenido existente, agregar contenido nuevo o crear nuevos [problemas](https://github.com/MicrosoftDocs/edge-developer/issues).  El equipo de Microsoft Edge revisa sus sugerencias y trabaja para incorporar las sugerencias a los documentos.  

Busque los datos de la [página Estado](https://developer.microsoft.com/microsoft-edge/status) en:  [https://github.com/MicrosoftEdge/Status](https://github.com/MicrosoftEdge/Status) .  La página proporciona el estado de implementación más reciente y los planes futuros para las características de la plataforma `Status` web en Microsoft Edge.

### <a name="conventions"></a>Convenciones  

*   Al agregar una página, debe agregar una entrada para ella en [toc.md](./microsoft-edge/toc.yml) que aparezca.
*   Un directorio puede contener más directorios o `readme.md` s
*   Los nombres de carpeta o directorio están separados por guiones \(por ejemplo, `f12-tools` \) y en minúsculas.  Los directorios se usan en las direcciones URL del `docs.microsoft.com` sitio.  Evite usar guiones bajos, PascalCase o camelCase.  

### <a name="other-text-elements"></a>Otros elementos de texto  

Estos otros elementos de texto tienen el estilo disponible:  

*   Listas sin ordenar  
*   Tener viñetas regulares  
    *   También puede anidar viñetas.  
    *   Las listas de viñetas deben tener más de una entrada.  
*   Disposición estándar 

1.  Listas ordenadas.  
1.  Use numeración de estilo occidental normal.  
1.  Solo se debe usar cuando una lista realmente tiene orden.  

---  

Las reglas horizontales están disponibles.  Use las reglas horizontales con moderación para reducir el desorden.  
Evite usar reglas horizontales con etiquetas de título; algunos encabezados ya usan estilos de línea para la jerarquía visual.  

### <a name="displaying-code"></a>Mostrar código  

Puede usar la sintaxis `code` de Markdown en línea \(con los backticks\).  

O puede mostrar bloques de código.  El siguiente fragmento de código es un ejemplo css.  

```css
body {
    background: #fff;
}
```  

### <a name="tables"></a>Tablas  

| Usted puede | usar encabezados | en tablas |  
|:--- |:--- |:--- |  
| Alineado a la izquierda | A menos que un # | 456 |  
| Valor de texto | Más texto | $0,00 |  

### <a name="notes"></a>Notas  

Use notas con moderación.  Los bloques están diseñados para resaltar la información de "don't-miss-it".  

Cuatro versiones diferentes de notas tienen un estilo actual.  

*   NOTA  
*   ADVERTENCIA  
*   SUGERENCIA  
*   IMPORTANTE  

Respectivamente, las notas tienen el aspecto de los siguientes fragmentos de código.  

```md
> [!NOTE]
> This is a NOTE  
```  

```md
> [!WARNING]
> This is a WARNING  
```  

```md
> [!TIP]
> This is a TIP  
```  

```md
> [!IMPORTANT]
> This is IMPORTANT  
```  

![Patrones de nota](./media/notes.png)

Para las notas de bloque de varias líneas, use un carácter mayor que \( \) delante de cada línea de las notas como se muestra `>` en el ejemplo siguiente.  

```md
> This is a line in a blockquote.  
> My text may wrap to more than one line when the Markdown is parsed, but I must include all my information within a single \(sometimes very long line\) in the Markdown.  
> This is another line in a blockquote.  
```

### <a name="images"></a>Imágenes  

Las imágenes deben almacenarse en un directorio y hacer referencia a él con una ruta `media` de acceso relativa mediante el script de imagen.  

<!--  `![Note patterns](media/notes.png)`  -->  

```md
:::image type="complex" source="./media/notes.png" alt-text="Note patterns" lightbox="./media/notes.png":::
   Note patterns  
:::image-end:::  
```  
