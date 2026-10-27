# Historias de usuario de búsqueda

| Campo | Valor |
| --- | --- |
| Proyecto | Proyecto Simbiosis |
| Fecha | [dd/mm/aaaa] |
| Versión | [Versión de trabajo] |
| Estado | Borrador |

## Fuentes comunes

- [Acta de UC-21 Buscar recetas](../captura/acta-acuerdos-uc-21-buscar-recetas.md), v1.1, Vigente.
- [Catálogo de requisitos](catalogo-requisitos.md), UR-08 y FR pertinentes.
- [Modelo de casos de uso](../modelos/modelo-casos-de-uso.md), UC-21.

## Épica de búsqueda

Como persona usuaria registrada, quiero buscar recetas mediante texto, ingredientes incluidos y exclusión de ingredientes, para localizar recetas que se ajusten a mis necesidades y preferencias
## Justificación de la división

La búsqueda por texto, por ingredientes incluidos y por exclusión de ingredientes aportan valor de forma independiente porque permiten encontrar recetas mediante criterios distintos. Separarlas en historias facilita su implementación y validación manteniendo la funcionalidad global de búsqueda.

## US-01

**Título:Buscar recetas mediante texto

Como persona usuaria registrada, quiero buscar recetas mediante una palabra o frase, para localizar recetas relacionadas con un tema o preparación concreta

**Fuentes:** UR-08; UC-21; FR-085; acta, apartado 2.

### Criterios de aceptación

- **CA-01** Dado que existen recetas publicadas que contienen la palabra «pollo» en su título o contenido, cuando el usuario introduce «pollo» en el campo de búsqueda, entonces el sistema muestra las recetas relacionadas con dicho término.

- **CA-02** Dado que existen recetas publicadas relacionadas con la frase «tarta de queso», cuando el usuario introduce dicha frase en el campo de búsqueda, entonces el sistema muestra las recetas relacionadas con la frase introducida.

- **CA-03** Dado que no existe ninguna receta asociada al término buscado, cuando el usuario ejecuta la búsqueda, entonces el sistema informa de que no se han encontrado resultados.

## US-02

**Título:** Buscar recetas por ingredientes incluidos

Como usuario, quiero buscar recetas por ingredientes seleccionados, para encontrar recetas que contengan ingredientes de los que dispongo o deseo consumir.

**Fuentes:** UR-08; UC-21; FR-086; acta, apartado 2.

### Criterios de aceptación

- **CA-01.** Dado que existen recetas que contienen los ingredientes seleccionados, cuando el usuario selecciona uno o varios ingredientes e inicia la búsqueda, entonces el sistema muestra únicamente recetas que contienen todos los ingredientes seleccionados.
- **CA-02.** Dado que una receta no contiene alguno de los ingredientes seleccionados, cuando el usuario realiza la búsqueda, entonces dicha receta no aparece en los resultados.
- **CA-03.** Dado que no existen recetas que contengan todos los ingredientes seleccionados, cuando el usuario ejecuta la búsqueda, entonces el sistema informa de que no se han encontrado resultados.

## US-03

**Título:** Excluir ingredientes de la búsqueda

Como usuario, quiero excluir ingredientes de mis búsquedas, para evitar recetas que contengan ingredientes no deseados o incompatibles con mis necesidades.

**Fuentes:** UR-08; UC-21; FR-087 ; acta, apartado 2.

### Criterios de aceptación

- **CA-01.** Dado que existen recetas que contienen cebolla y recetas que no la contienen, cuando el usuario excluye el ingrediente «cebolla», entonces el sistema no muestra recetas que contengan dicho ingrediente..
- **CA-02.** Dado que existen recetas que cumplen los criterios de búsqueda y exclusión, cuando el usuario ejecuta la búsqueda, entonces el sistema muestra únicamente las recetas que no contienen ninguno de los ingredientes excluidos..
- **CA-03.** Dado que la búsqueda no devuelve resultados debido a los criterios aplicados, cuando el usuario ejecuta la búsqueda, entonces el sistema informa de que no se han encontrado resultados y proporciona alternativas relacionadas o correcciones ortográficas cuando estén disponibles..

## Revisión INVEST

La revisión abarca US-01, US-02 y US-03. «Aplicado» indica si se ha realizado la comprobación. «Cumple» indica si todas las historias cumplen el criterio. Si alguna no lo cumple, indicar «No» e identificar la historia y el motivo en la justificación. Si no se ha realizado la comprobación o faltan datos, indicar «Pendiente» en «Cumple».

| Criterio | Pregunta de revisión | Aplicado | Cumple | Justificación |
| --- | --- | --- | --- | --- |
| Independiente | ¿Puede implementarse cada historia y ofrecer un resultado útil sin implementar antes las otras historias del conjunto? Puede compartir infraestructura con ellas. | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Negociable | ¿Cada historia explica qué necesita la persona y deja margen para discutir los detalles de la solución, respetando los acuerdos confirmados? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Valiosa | ¿La parte «para…» de cada historia explica el beneficio que obtiene la persona al usar esa capacidad? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Estimable | ¿Están claros el alcance y los datos necesarios para estimar el trabajo de cada historia? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Pequeña | ¿Se centra cada historia en una única capacidad de alcance manejable? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Comprobable | ¿Los criterios de aceptación de cada historia describen acciones y resultados observables que permiten distinguir un comportamiento correcto de uno incorrecto? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |

## Dudas pendientes

[Cuestiones pendientes de aclaración. Si no quedan cuestiones, indicar «Ninguna».]
