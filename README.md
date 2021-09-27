# Persuadí 2018

Programa para Extracción de Estadísticas de Redes Sociales sobre Unidades Audiovisuales Distribuidas en Internet

## ¿Qué hace este conjunto de scripts en Python?

Permite extraer estadísticas desde los exports de CSV de Facebook Insight y Youtube Analytics. También desde la Open Graph API de Facebook y de Youtube Data Api v3.

Resguardar los datos en una base de datos utilizando Directus APi y MySQL Server.

Luego poder mostrar los datos en algún formato imprimible con Codeigniter

`Esta versión utilizada en 2018 es antigua.`

## ¿Por qué está publicado este contenido?

Porque el resultado de la ejecución de este software es y fue insumo para la redacción de documentación de transparencia y gestión de una entidad pública.

Porque sirve de ayuda memoria, puesto que cada vez que es necesario extraer la información de las APIs de estas plataformas, las mismas fueron actualizadas, o deprecaron la API que había sido utilizada, el código presente sirve de base para no comenzar de cero.

Por si es de interés para alguien que necesite automatizar ciertas tareas. [Ver Notas Aclaratorias](###-Notas-Aclaratorias:)

## ¿Cómo funciona?

Persuadí lee datos de CSV exportado de los motores de analíticas de Facebook, Youtube y Vimeo, los incorpora a una base de datos a través de un API (en el caso de esta implementación utilizando Directus v6 o v7), centraliza la información fragmentada y luego posee una plantilla html que adaptada a otra aplicación web, puede generar un informe PDF con todos los activos digitales que fueron publicados en dichas redes sociales o plataformas.

## ¿Para qué fue utilizado Persuadi en UNITV?

Fue utilizado para generar un informe automático que contiene un listado de todos los activos digitales (principalmente contenido audiovisual), su principal información estadísticas (reproducciones, impresiones, me gusta, compartidos) y su metadata asociada (miniatura, título, descripción) publicado por UNITV durante el año 2018.

## ¿Qué ayudó a resolver?

Durante los años previos los informes se realizaban manualmente y solo obtenían una vista global de los rendimientos obtenidos por el canal o los perfiles de UNITV en las diversas redes sociales. Con la aplicación de este Script, se obtuvo un listado con información individual de cada video publicado.

Dicho informe sirvió también para la auditoría interna de la institución, el informe anual de la Dirección y para tener control preciso y censable sobre pertenencias intangibles de la Universidad de General Sarmiento (institución a la que pertenece UNITV).

Se puede ver un ejemplo del informe producido automáticamente en los anexos del [Informe De Activos Digitales](https://github.com/logosfera-zero/Persuadi/blob/informe_2018/Informe%20Final%20PDF/02_Anexo_1.pdf)

De forma concreta, Persuadí asiste en la ingesta de datos, que por ejemplo en el caso de Facebook se encuentran segmentados:

Durante 2018 Facebook solo permitía exportar y descargar información de publicaciones propias en Fanpage de un intervalo de tiempo de 180 días. Lo que obligó a importar los datos de múltiples archivos CSV.

Por otro lado, la información también se encuentra segmentada con respecto al tipo de definición de objeto que decidamos utilizar en Facebook para obtener datos. Esto es que en el caso de los videos, Facebook entrega cierta inforamción si se solicita una query con el ID del video sobre el extremo de la api relacionado con un posteo (_Post_) que si lo referenciamos como un _video_.


### Notas Aclaratorias:

El código de este repositorio **NO** fue refactoreado para su reutilización, sino que sus comentarios y su documentación pueden servir para que sean utilizados fragmentos del mismos.

Este desarrollo se realizó en el plazo de una semana, ante la exigencia desproporcionada de la entidad que solicitó la entrega del informe en un lapso de tiempo muy breve para el relevo más de 500 activos distribuidos en tres plataformas externas. Por esto mismo es que:

- Se está refactoreando el código para evitar publicar malas prácticas. A medida que se resuelvan y se puedan agregar comentarios adecuados, se irá publicando.
- Los anexos del informe que contienen la información formateada y detallada, no tiene un bonito diseño puesto que era priomordial la entrega de la propia información. A pesar de no ser un lindo diseño, el mismo es funcional y se agrega la escueta plantilla utilizada en su momento.

Persuadí posee otros requisitos adicionales para ser completamente funcional. [Ver Requisitos de esta implementación](##-Requisitos-de-esta-implementación)


## Requisitos de esta implementación

## Pasos para utilizar




    Pendiente de redacción

Mientras se continúa con la redacción de este Readme, se pueden obtener más detalles técnicos en el cuerpo del [informe](https://github.com/logosfera-zero/Persuadi/blob/informe_2018/Informe%20Final%20PDF/01_Informe.pdf)

### Facebook

1. Exportar los CSV necesarios sobre datos de "Publicaciones" desde Facebook Analytics.
