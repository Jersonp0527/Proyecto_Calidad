Facultad de Minas
Sede Medellín

Calidad de Software

3007849

Albeiro Espinosa Bedoya, Ph.D. Ms.C.
Profesor Asociado

Ejemplo Evaluación Calidad

Facultad de Minas
Sede Medellín

Diap. 2

Agenda (1/1)

1. Referencias

Facultad de Minas
Sede Medellín

Diap. 3

¿Qué es un CMS?

Definición
Un Sistema Gestor de Contenidos (CMS) permite crear, editar, gestionar y publicar contenido digital
(texto, imágenes, video) en sitios web sin necesidad de programar.

¿Cómo funciona? El servidor genera la página dinámicamente cada vez que un usuario la solicita: toma el
contenido de la base de datos y lo presenta con la plantilla definida.

Ventaja clave: reduce los costos de gestión respecto a páginas estáticas y no requiere conocimientos de
HTML para publicar contenido.

Ejemplos conocidos:

WordPress → blogs y sitios corporativos
Joomla! → portales complejos e intranets
Drupal → sitios institucionales y gubernamentales

Facultad de Minas
Sede Medellín

Diap. 4

CMS Joomla! y CMS Drupal (1/2)

CMS Joomla!

Es un CMS de código abierto distribuido bajo licencia GPL. Permite crear sitios web
elegantes, dinámicos e interactivos sin necesidad de conocimientos técnicos avanzados.
Facilita también la creación de sistemas internos (Intranets).

Facultad de Minas
Sede Medellín

Diap. 5

CMS Joomla! y CMS Drupal (2/2)

CMS Drupal

Es un CMS dinámico. El contenido textual y la configuración se almacenan en una base
de datos. Al acceder a una página, el servidor genera dinámicamente su contenido. No
se requiere conocimiento de HTML para crear o editar páginas.

Facultad de Minas
Sede Medellín

Diap. 6

¿Por qué comparar Joomla! y Drupal?

Problema real
Supón que debes elegir un CMS para el portal de la Subsecretaría de Planificación. ¿Cómo
decides cuál es mejor de forma objetiva?

La solución: aplicar un marco de evaluación basado en métricas, siguiendo las normas
ISO/IEC, que permita comparar ambos sistemas de manera sistemática y repetible.

Joomla!

Drupal

Fácil de usar

Gran comunidad

Muchos módulos listos

Facultad de Minas
Sede Medellín

Muy flexible

Seguridad robusta

Ideal para sitios grandes

Diap. 7

Base normativa: estándares ISO/IEC

El marco de evaluación se apoya en tres normas complementarias:

ISO/IEC 25010 Define las características de calidad del software: funcionalidad,

confiabilidad, usabilidad, eficiencia, mantenibilidad y portabilidad. Es la base para
construir el árbol de requerimientos.

ISO/IEC 25040 Proporciona el proceso de evaluación: cómo planificar, ejecutar y

documentar la evaluación desde el punto de vista del evaluador.

ISO/IEC 25020 Define el modelo de medición: qué medir, cómo medir y cómo

retroalimentar el proceso para mejorarlo.

En resumen
25010 dice qué es calidad. 25040 dice cómo evaluar. 25020 dice cómo medir.

Facultad de Minas
Sede Medellín

Diap. 8

¿Qué es un Marco de Evaluación?

Concepto
Un marco de evaluación es un conjunto de pasos ordenados que permiten comparar sistemas de forma
justa, objetiva y repetible, evitando decisiones basadas en preferencias personales.

¿Por qué es importante?

Permite justificar técnicamente la elección ante terceros.

Puede replicarse para evaluar otras herramientas en el futuro.

Produce un indicador global numérico que sintetiza múltiples criterios en un solo valor comparable.

Facultad de Minas
Sede Medellín

Diap. 9

Marco de Evaluación (1/2)

El marco de evaluación se dividió en cuatro etapas:

1. Determinación del Árbol de Requerimiento de Calidad.
2. Especificación de Métricas.
3. Medición de Atributos.
4. Cálculo de las Subcaracterísticas y Características.

Facultad de Minas
Sede Medellín

Diap. 10

Marco de Evaluación (2/2)

Objetivo general: Realizar un análisis comparativo entre Joomla y Drupal, definiendo
métricas que permitan comparar su calidad.

Objetivos específicos:

Facilitar la selección del CMS mediante una evaluación objetiva.

Determinar niveles de funcionalidad, usabilidad y eficiencia.

Facultad de Minas
Sede Medellín

Diap. 11

Las 4 Etapas del Marco — Visión General

#

Etapa

¿Qué se hace?

Especificación de Métricas

1 Árbol de Requerimientos
2
3 Medición de Atributos
Cálculo de Resultados
4

Se define qué se va a medir
Se define cómo se va a medir
Se mide cada atributo en cada CMS
Se agrega y se obtiene el indicador
global

Idea clave
Cada etapa depende de la anterior. Sin un árbol de requerimientos claro no se pueden
definir buenas métricas; sin buenas métricas, la medición no es confiable.

Facultad de Minas
Sede Medellín

Diap. 12

Etapa 1 — ¿Qué es un Árbol de Requerimientos?

Definición
Estructura jerárquica que descompone las características de calidad (ISO/IEC 25010) en
sub-características y luego en atributos medibles.

Tres niveles:

Característica → Sub-característica → Atributo cuantificable

Ejemplo concreto de este caso:

Funcionalidad → Gestor de Módulos → ¿Existe editor WYSIWYG instalado por defecto?

¿Por qué una estructura de árbol?
Organiza los criterios de lo general a lo específico, garantizando que cada aspecto relevante quede
representado y sea medible.

Facultad de Minas
Sede Medellín

Diap. 13

Etapa 1: Árbol de Requerimiento de Calidad (1/5)

1. Funcionalidad

1.1. Aspectos del gestor de Módulos
1.1.1. Existencia de Módulos

1.1.1.1. Módulos instalados por defecto
1.1.1.2. Módulos Activados por defecto

1.1.2. Disponibilidad de Módulos

1.1.2.1. Editor HTML tipo WYSIWYG
1.1.2.2. Reproductor de video FLV
1.1.2.3. Galería de Imágenes
1.1.2.4. Reproductor de Audio
1.1.2.5. Formulario de Contactos

Facultad de Minas
Sede Medellín

Diap. 14

Etapa 1: Árbol de Requerimiento de Calidad (2/5)

1.2. Aspectos del gestor de Plantillas

1.2.1. Capacidad para el manejo de Plantillas para el Sitio y el Administrador
1.2.2. Plantillas para el Sitio

1.2.2.1. Plantillas por defecto para el Sitio
1.2.2.2. Plantillas Modificables para el Sitio

1.2.3. Plantillas para el Administrador

1.2.3.1. Plantillas por defecto para el Administrador
1.2.3.2. Plantillas Modificables para el Administrador

1.2.4. Plantillas del Gestor de Contenidos

1.2.4.1. Plantillas para el Sitio del Total Instaladas por Defecto
1.2.4.2. Plantillas para el Administrador del Total Instaladas por Defecto

Facultad de Minas
Sede Medellín

Diap. 15

Etapa 1: Árbol de Requerimiento de Calidad (3/5)

1.3. Aspectos de Seguridad

1.3.1. Capacidad para Definir Roles
1.3.2. Capacidad para Administrar permisos

1.4. Aspectos de Búsqueda

1.4.1. Implementación del Buscador del Sitio
1.4.2. Visibilidad del Buscador del Sitio

Facultad de Minas
Sede Medellín

Diap. 16

Etapa 1: Árbol de Requerimiento de Calidad (4/5)

2. Usabilidad

2.1. Pasos Instalación

2.1.1. Instalación del CMS
2.1.2. Instalación de Módulo
2.1.3. Instalación de Plantillas

2.2. Lenguajes por defecto
2.3. Facilidad en el Manejo de Módulos

2.3.1. Facilidad en la instalación de Nuevos Módulos
2.3.2. Facilidad en la Configuración de Módulos

Facultad de Minas
Sede Medellín

Diap. 17

Etapa 1: Árbol de Requerimiento de Calidad (5/5)

3. Eficiencia

3.1. Cache Activado

3.1.1. Peticiones Atendidas por Segundo
3.1.2. Tiempo requerido por petición
3.1.3. Tasa de Transferencia

3.2. Cache Desactivado

3.2.1. Peticiones Atendidas por Segundo
3.2.2. Tiempo requerido por petición
3.2.3. Tasa de Transferencia

Facultad de Minas
Sede Medellín

Diap. 18

Etapa 2: Especificación de Métricas

Definición
Una métrica convierte una observación (conteo, sí/no, tiempo) en un valor normalizado entre 0 % y 100 %
que permite comparar atributos de distinta naturaleza.

Ejemplo — “Módulos instalados por defecto”:

Valor =

Módulos instalados por defecto
Total de módulos esperados

× 100 %

Escala de aceptabilidad:

Rango

Nivel

Significado

[0 %, 40 %)
[40 %, 60 %)
[60 %, 100 %]

Insatisfactorio
Marginal
Satisfactorio

El atributo no cumple los requisitos
Cumplimiento parcial
Cumple los requisitos

Facultad de Minas
Sede Medellín

0%40%60%100%InsatisfactorioMarginalSatisfactorioDiap. 19

Etapa 3 — ¿Cómo se leen las tablas?

Instrucción de lectura
Cada fila es un atributo hoja del árbol (Etapa 1). El porcentaje indica qué tan bien cumple el CMS ese
atributo según la métrica de la Etapa 2. Estos valores se llaman Indicadores Elementales (IE).

Ejemplo de interpretación (usando la escala real):

Atributo

Joomla Drupal Nivel

Editor WYSIWYG (1.1.2.1)
Definir Roles (1.3.1)
Lenguajes (2.2)

99 %
0 %
80 %

0 %
100 %
50 %

Sat. / Insat.
Insat. / Sat.
Sat. / Marginal

Importante
Un 0 % no significa que el CMS sea malo en general: puede significar que esa funcionalidad no viene
incluida por defecto, pero podría instalarse como extensión.

Facultad de Minas
Sede Medellín

Diap. 20

Etapa 3: Medición de Atributos - Joomla (1/2)

Tabla 1: Evaluación de atributos de Joomla

Atributos

1.1.1.1 Módulos instalados por defecto
1.1.1.2 Módulos Activados por defecto
1.1.2.1 Editor HTML tipo WYSIWYG
1.1.2.2 Reproductor de video FLV
1.1.2.3 Galería de Imágenes
1.1.2.4 Reproductor de Audio
1.1.2.5 Formulario de Contactos
1.2.1 Capacidad para el manejo de Plantillas para el Sitio y el Administrador
1.2.2.1 Plantillas por defecto para el Sitio
1.2.2.2 Plantillas Modificables para el Sitio
1.2.3.1 Plantillas por defecto para el Administrador
1.2.3.2 Plantillas Modificables para el Administrador
1.2.4.1 Plantillas para el Sitio del Total Instaladas por Defecto
1.2.4.2 Plantillas para el Administrador del Total Instaladas por Defecto
1.3.1 Capacidad para Definir Roles
1.3.2 Capacidad para Administrar permisos
1.4.1 Implementación del Buscador del Sitio
1.4.2 Visibilidad del Buscador del Sitio

Joomla

80.00 %
21.74 %
99.00 %
0.00 %
33.00 %
0.00 %
33.00 %
99.00 %
40.00 %
50.00 %
60.00 %
100.00 %
66.66 %
33.33 %
0.00 %
100.00 %
33.00 %
100.00 %

Facultad de Minas
Sede Medellín

Diap. 21

Etapa 3: Medición de Atributos - Joomla (2/2)

Tabla 2: Evaluación de atributos de Joomla (cont.)

Atributos

2.1.1 Instalación del CMS
2.1.2 Instalación de Módulo
2.1.3 Instalación de Plantillas
2.2 Lenguajes por defecto
2.3.1 Facilidad en la instalación de Nuevos Módulos
2.3.2 Facilidad en la Configuración de Módulos
3.1.1 Peticiones Atendidas por Segundo
3.1.2 Tiempo requerido por petición
3.1.3 Tasa de Transferencia
3.2.1 Peticiones Atendidas por Segundo
3.2.2 Tiempo requerido por petición
3.2.3 Tasa de Transferencia

Joomla

60.00 %
60.00 %
60.00 %
80.00 %
100.00 %
100.00 %
50.00 %
50.00 %
60.00 %
50.00 %
50.00 %
60.00 %

Facultad de Minas
Sede Medellín

Diap. 22

Etapa 3: Medición de Atributos - Drupal (1/2)

Tabla 3: Evaluación de atributos de Drupal

Atributos

1.1.1.1 Módulos instalados por defecto
1.1.1.2 Módulos Activados por defecto
1.1.2.1 Editor HTML tipo WYSIWYG
1.1.2.2 Reproductor de video FLV
1.1.2.3 Galería de Imágenes
1.1.2.4 Reproductor de Audio
1.1.2.5 Formulario de Contactos
1.2.1 Capacidad para el manejo de Plantillas para el Sitio y el Administrador
1.2.2.1 Plantillas por defecto para el Sitio
1.2.2.2 Plantillas Modificables para el Sitio
1.2.3.1 Plantillas por defecto para el Administrador
1.2.3.2 Plantillas Modificables para el Administrador
1.2.4.1 Plantillas para el Sitio del Total Instaladas por Defecto
1.2.4.2 Plantillas para el Administrador del Total Instaladas por Defecto
1.3.1 Capacidad para Definir Roles
1.3.2 Capacidad para Administrar permisos
1.4.1 Implementación del Buscador del Sitio
1.4.2 Visibilidad del Buscador del Sitio

Drupal

60.00 %
66.66 %
0.00 %
0.00 %
0.00 %
0.00 %
33.00 %
99.00 %
80.00 %
100.00 %
80.00 %
100.00 %
100.00 %
100.00 %
100.00 %
100.00 %
33.00 %
100.00 %

Facultad de Minas
Sede Medellín

Diap. 23

Etapa 3: Medición de Atributos - Drupal (2/2)

Tabla 4: Evaluación de atributos de Drupal (cont.)

Atributos

2.1.1 Instalación del CMS
2.1.2 Instalación de Módulo
2.1.3 Instalación de Plantillas
2.2 Lenguajes por defecto
2.3.1 Facilidad en la instalación de Nuevos Módulos
2.3.2 Facilidad en la Configuración de Módulos
3.1.1 Peticiones Atendidas por Segundo
3.1.2 Tiempo requerido por petición
3.1.3 Tasa de Transferencia
3.2.1 Peticiones Atendidas por Segundo
3.2.2 Tiempo requerido por petición
3.2.3 Tasa de Transferencia

Drupal

60.00 %
60.00 %
60.00 %
50.00 %
50.00 %
50.00 %
80.00 %
80.00 %
90.00 %
50.00 %
50.00 %
30.00 %

Facultad de Minas
Sede Medellín

Diap. 24

Etapa 4 — El modelo de agregación LSP

¿Qué es el modelo LSP?
Logic Scoring of Preference (LSP) es un modelo de agregación que combina los indicadores elementales
(IE) en un Indicador Global (IG), respetando los pesos y relaciones lógicas entre criterios. Los pesos los
asigna quien diseña la evaluación reflejando el nivel de importancia, es subjetivo.

Fórmula de media de potencia pesada:

IG(r) = P1 · IE1 + P2 · IE2 + · · · + Pm · IEm

Donde:

∑

Pi = peso asignado a cada atributo o sub-característica (

IEi = valor medido para ese atributo (entre 0 y 1)

Pi = 1)

Aplicación
Los IE de los atributos hoja se agregan en sub-características, luego en características (Funcionalidad,
Usabilidad, Eficiencia), y finalmente en el Indicador Global de Preferencia.

Facultad de Minas
Sede Medellín

Diap. 25

Etapa 4: Cálculo de Subcaracterísticas y Características (1/4)

1. Funcionalidad:

Facultad de Minas
Sede Medellín

Peso  IE - Joomla  IE - Drupal1. Funcionalidad0,4053,0971,301.1. Aspectos del gestor de Módulos0,3056,4239,541.1.1. Existencia de Módulos0,6065,4461,501.1.1.1. Módulos instalados por defecto0,7580,0060,001.1.1.2. Módulos Ac�vados por defecto0,2521,7466,001.1.2. Disponibilidad de Módulos0,4042,906,601.1.2.1. Editor HTML �po WYSIWYG0,3099,000,001.1.2.2. Reproductor de video FLV0,200,000,001.1.2.3. Galería de Imágenes0,2033,000,001.1.2.4. Reproductor de Audio0,100,000,001.1.2.5. Formulario de Contactos0,2033,0033,001.2. Aspectos del gestor de Plan�llas0,2067,7094,101.2.1. Capacidad para el manejo de Plan�llas para el Si�o y el Administrador0,3099,0099,001.2.2. Plan�llas para el Si�o0,2043,0086,001.2.2.1. Plan�llas por defecto para el Si�o0,7040,0080,001.2.2.2. Plan�llas Modiﬁcables para el Si�o0,3050,00100,001.2.3. Plan�llas para el Administrador0,2072,0086,001.2.3.1. Plan�llas por defecto para el Administrador0,7060,0080,001.2.3.2. Plan�llas Modiﬁcables para el Administrador0,30100,00100,001.2.4. Plan�llas del Gestor de Contenidos0,3050,00100,001.2.4.1. Plan�llas para el Si�o del Total Instaladas por Defecto0,5066,66100,001.2.4.2. Plan�llas para el Administrador del Total Instaladas por Defecto0,5033,33100,001.3. Aspectos de Seguridad0,3040,00100,001.3.1. Capacidad para Deﬁnir Roles0,600,00100,001.3.2. Capacidad para Administrar permisos0,40100,00100,001.4. Aspectos de Búsqueda0,2053,1053,101.4.1. Implementación del Buscador del Si�o0,7033,0033,001.4.2. Visibilidad del Buscador del Si�o0,30100,00100,001.1.1.11.1.1.20.750.25∑0.61.1.11.1.2.11.1.2.21.1.2.31.1.2.41.1.2.50.30.20.20.10.2∑0.41.1.2∑0.31.11.2.10.31.2.2.11.2.2.20.70.3∑0.21.2.21.2.3.11.2.3.20.70.3∑0.21.2.31.2.4.11.2.4.20.50.5∑0.31.2.4∑0.21.21.3.11.3.20.60.4∑0.31.31.4.11.4.20.70.3∑0.21.4∑1Diap. 26

Etapa 4: Cálculo de Subcaracterísticas y Características (2/4)

2. Usabilidad:

Facultad de Minas
Sede Medellín

Peso  IE - Joomla  IE - Drupal2. Usabilidad0,4076,0055,002.1. Pasos Instalación0,5060,0060,002.1.1. Instalación del CMS0,4060,0060,002.1.2. Instalación de Módulo0,3060,0060,002.1.3. Instalación de Plan�llas0,3060,0060,002.2. Lenguajes por defecto0,2080,0050,002.3. Facilidad en el Manejo de Módulos0,30100,0050,002.3.1. Facilidad en la instalación de Nuevos Módulos0,50100,0050,002.3.2. Facilidad en la Conﬁguración de Módulos0,50100,0050,002.1.12.1.22.1.30.40.30.3∑2.12.20.22.3.12.3.20.50.5∑2.30.50.3∑2Diap. 27

Etapa 4: Cálculo de Subcaracterísticas y Características (3/4)

3. Eficiencia:

Facultad de Minas
Sede Medellín

Peso  IE - Joomla  IE - Drupal3. Eﬁciencia0,2053,0067,403.1. Cache Ac�vado0,6053,0083,003.1.1. Pe�ciones Atendidas por Segundo0,4050,0080,003.1.2. Tiempo requerido por pe�ción0,3050,0080,003.1.3. Tasa de Transferencia0,3060,0090,003.2. Cache Desac�vado0,4053,0044,003.2.1. Pe�ciones Atendidas por Segundo0,4050,0050,003.2.2. Tiempo requerido por pe�ción0,3050,0050,003.2.3. Tasa de Transferencia0,3060,0030,003.1.10.43.1.20.33.1.30.3∑3.10.63.2.10.43.2.20.33.2.30.3∑3.20.4∑3Diap. 28

Etapa 4: Cálculo de Subcaracterísticas y Características (4/4)

4. Características de alto nivel:

Facultad de Minas
Sede Medellín

Preferencia de Calidad Global62,2364,00Peso  IE - Joomla  IE - Drupal1. Funcionalidad0,4053,0971,302. Usabilidad0,4076,0055,003. Eﬁciencia0,2053,0067,401230.40.40.2∑PreferenciaDiap. 29

Etapa 4 — Resultados de la Agregación LSP (1/2)

Resultados por característica y sub-característica:

Característica / Sub-característica

Joomla!

Drupal

1. Funcionalidad

1.1 Gestor de Módulos
1.2 Gestor de Plantillas
1.3 Seguridad
1.4 Búsqueda

2. Usabilidad

2.1 Pasos de Instalación
2.2 Lenguajes por defecto
2.3 Facilidad en Módulos

3. Eficiencia

3.1 Caché Activado
3.2 Caché Desactivado

53.09 %
56.42 %
67.70 %
40.00 %
53.10 %

76.00 %
60.00 %
80.00 %
100.00 %

53.00 %
53.00 %
53.00 %

71.30 %
39.54 %
94.10 %
100.00 %
53.10 %

55.00 %
60.00 %
50.00 %
50.00 %

67.40 %
83.00 %
44.00 %

Facultad de Minas
Sede Medellín

Diap. 30

Etapa 4 — Resultados de la Agregación LSP (2/2)

Indicador Global de Preferencia:

Indicador Global
Nivel

Joomla!

62,23 %

Drupal

64.00 %

Satisfactorio Satisfactorio

Lectura del resultado
Ambos CMS alcanzan un nivel satisfactorio, al superar el umbral del 60 %. Drupal obtiene
una valoración ligeramente superior (64.00 %) frente a Joomla! (62.23 %), con una
diferencia de 1.77 puntos porcentuales, lo que indica un desempeño global muy similar.

Facultad de Minas
Sede Medellín

Diap. 31

Análisis Detallado por Característica

Funcionalidad — Drupal gana (71.30 % vs 53.09 %)

Drupal destaca en seguridad (100 %) y gestión de plantillas (94.10 %).

Drupal ofrece mayor flexibilidad para la definición de roles y permisos.

Joomla! presenta mejor valoración en la gestión de módulos (56.42 % vs 39.54 %).

Usabilidad — Joomla! gana (76.00 % vs 55.00 %)

Joomla! facilita la administración de módulos (100 % vs 50 %).

Joomla! dispone de una mayor cantidad de idiomas instalados por defecto.

Ambos CMS presentan una complejidad similar en el proceso de instalación.

Eficiencia — Drupal gana (67.40 % vs 53.00 %)

Con caché activado, Drupal alcanza un mejor desempeño (83 % vs 53 %).

Joomla! mantiene resultados estables independientemente del uso de caché.

Conclusión práctica
Ambos CMS alcanzan un nivel satisfactorio. Joomla! destaca por su facilidad de uso y administración, mientras que
Drupal sobresale en funcionalidad, seguridad y rendimiento.

Facultad de Minas
Sede Medellín

Diap. 32

Síntesis del Proceso Completo

Etapa

Pregunta clave

Producto

1
2
3
4

¿Qué evalúo?
¿Cómo lo mido?
¿Cuánto obtiene cada sistema?
¿Cuál es mejor globalmente?

Árbol de requerimientos
Métricas normalizadas (0–100 %)
Indicadores Elementales (IE)
Indicador Global LSP

Lección aprendida
La calidad no es absoluta: depende del contexto y los requerimientos del proyecto. Un CMS puede ganar
en usabilidad y perder en eficiencia simultáneamente.
Para recordar
El proceso de cuatro etapas es reutilizable: se puede aplicar para comparar cualquier par de herramientas
de software, como veremos en los ejercicios a continuación.

Facultad de Minas
Sede Medellín

Diap. 33

¿Cómo aplicar el marco en los ejercicios?

Para cada ejercicio, sigue estos cinco pasos:

1. Árbol de requerimientos: Define las características (funcionalidad, usabilidad, eficiencia…) y

desglósalas en atributos concretos y medibles.

2. Métricas: Para cada atributo, define una fórmula o escala que convierta la observación en un porcentaje

normalizado.

3. Medición: Instala/prueba cada herramienta y registra los valores (Indicadores Elementales) en una

tabla.

4. Cálculo: Aplica la fórmula de agregación con los pesos asignados y obtén el Indicador Global para cada

herramienta.

5. Conclusión: Indica cuál es preferible según el contexto y justifica la respuesta usando la escala de

aceptabilidad.

Escala de referencia
[0 %, 40 %) Insatisfactorio

Facultad de Minas
Sede Medellín

[40 %, 60 %) Marginal

[60 %, 100 %] Satisfactorio

Diap. 34

Ejercicio Taller: Bloc de Notas vs Notepad++ (1/1)

Contexto: Un equipo IT debe elegir un editor de texto ligero para tareas técnicas.

Objetivo: Aplicar un marco de evaluación comparativa con base en la norma ISO/IEC
25010 (funcionalidad y usabilidad).

Facultad de Minas
Sede Medellín

1. Referencias

Facultad de Minas
Sede Medellín

Diap. 35

Referencias (1/1)

Facultad de Minas
Sede Medellín

Albeiro Espinosa Bedoya, Ph.D. Ms.C.
Profesor Asociado
Email:aespinos@unal.edu.co
Instagram: @albeiroespinosabedoya

Departamento de Ciencias de la Computación y de la
Decisión, Facultad de Minas
Dirección: Av. 80 #65-223, Bloque M8A, Of. 204
Teléfono: +57 604 4255384

Facultad de Minas
Sede Medellín

