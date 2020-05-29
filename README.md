# Documentación de Microsoft Edge

## Código de conducta de Microsoft Open Source

Este proyecto ha adoptado el [código de conducta de Microsoft Open Source](https://opensource.microsoft.com/codeofconduct/).
Para obtener más información, consulta las [preguntas más frecuentes sobre el código de conducta](https://opensource.microsoft.com/codeofconduct/faq/) o ponte en contacto con [opencode@microsoft.com](mailto:opencode@microsoft.com) preguntas o comentarios adicionales.

## Avisos legales
Microsoft y sus colaboradores te conceden una licencia para la documentación de Microsoft y otros contenidos de este repositorio bajo la [licencia pública de Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/legalcode), consulta el archivo [LICENSE](LICENSE), y concédete una licencia para cualquier código del repositorio bajo la [Licencia MIT](https://opensource.org/licenses/MIT), consulta el archivo [LICENSE-CODE](LICENSE-CODE).

Microsoft, Windows, Microsoft Azure y otros productos y servicios Microsoft a los que se hace referencia en la documentación pueden ser marcas comerciales o marcas registradas de Microsoft en los Estados Unidos y en otros países o regiones.
Las licencias para este proyecto no te conceden derechos para usar los nombres, logotipos o marcas comerciales de Microsoft.
Encontrará las directrices generales de la marca comercial de Microsoft en https://go.microsoft.com/fwlink/?LinkID=254653 .

Puede encontrar la información de privacidad enhttps://privacy.microsoft.com

Microsoft y sus colaboradores se reservan todos los demás derechos, ya sea bajo sus respectivos derechos de autor, patentes o marcas comerciales, y tanto de manera implícita, explícita como de otro modo.

## Autores

Este es el repositorio de **documentación** de Microsoft Edge hospedado en [https://docs.microsoft.com/microsoft-edge/](https://docs.microsoft.com/microsoft-edge/) .

Si deseas ver la cobertura nueva o enviar comentarios, considera la posibilidad de [**contribuir**](/CONTRIBUTING.md).  Puede editar el contenido existente, agregar contenido nuevo o simplemente crear nuevos [problemas](https://github.com/MicrosoftDocs/edge-developer/issues). Echemos un vistazo a sus sugerencias y trabajaremos conjuntamente para incorporarlas en los documentos.

Busque los datos de la [`Status`](https://dev.windows.com/microsoft-edge/platform/status/) página en: https://github.com/MicrosoftEdge/Status . La `Status` página proporciona el último estado de implementación y planes futuros para las características de plataforma web de Microsoft Edge.

### Convenciones

- Al agregar una página, debe agregar una entrada para ella en [TOC.MD](microsoft-edge/toc.md) para que aparezca.
- Una carpeta puede contener más carpetas o `readme.md` s
- Los nombres de directorio o carpeta se separan con guiones (por ejemplo, `f12-tools` ) y en minúsculas. Se usan en las direcciones URL del sitio de docs.microsoft.com. No uses guiones de subrayado ni PascalCase/camelCase.

### Otros elementos de texto

Estos otros elementos de texto tienen estilos disponibles:

* Listas sin ordenar
* Tener viñetas normales
   * También puede anidar viñetas.
   * Las listas de viñetas deben tener más de una entrada.
* Muy estándar

1. Listas ordenadas.
2. Usa la numeración de estilo occidental estándar de OL.
3. Solo debe usarse cuando una lista tiene realmente un orden.

_________________________

Hay reglas horizontales disponibles. Te sugerimos que lo uses con moderación para reducir la aglomeración.
No combine reglas horizontales con etiquetas de encabezado; algunos estilos de línea ya usados para la jerarquía visual.

### Mostrar código

Puede usar `code` la sintaxis de Markdown alineada (con los retrofijos).

O puede mostrar bloques de código como este:

```css
body {
    background: #fff;
}
```

### Tablas

| Puedes     | usar encabezados | en tablas    |
|-------------|-------------|-------------:|
| Alineado a la izquierda| A menos que un #  | 456          |
| Valor de texto  | Más texto   | $0,00        |

### Notas

Use las notas con moderación. Se trata de bloques diseñados para resaltar la información de "no-que te falten".

Tenemos cuatro versiones diferentes de las notas con estilo actualmente:
- NOTA
- APARECERÁ
- SOBRE
- IMPORTANTE

Respectivamente, tienen el siguiente aspecto:

![Patrones de notas](./media/notes.png)

```
> [!WARNING]
> Hello. Yes. I am a warning note that has been automagically created. My text may wrap to more than one line when the Markdown is parsed, but I must include all my information within a single (sometimes very long line) in the Markdown itself.```

For multi-line blockquote notes, use a > in front of each line of the notes as seen in the example below.

```


### Imágenes

Las imágenes deben almacenarse en una `media` carpeta y se hace referencia a ellas con una ruta de acceso relativa:

`![Note patterns](media/notes.png)`
