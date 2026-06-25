# Calidad de Software - Proceso Plan Proyecto

**Fuente:** Presentación `SQ_Sesion06_Proceso_Proyecto.pdf`  
**Institución:** Universidad Nacional de Colombia - Facultad de Minas, Sede Medellín  
**Curso:** Calidad de Software - 3010440  
**Profesor:** Albeiro Espinosa Bedoya, Ph.D. Ms.C.  
**Tema:** Proceso Plan Proyecto

---

## Nota editorial

Este documento es una transcripción organizada en Markdown del material original. Se conserva la información académica de las diapositivas y se agregan notas aclaratorias marcadas como **Explicación sencilla**, para que una persona sin conocimiento previo pueda entender el contenido.

La leyenda institucional **“Facultad de Minas - Sede Medellín”** aparece de forma repetida en el material original como encabezado o pie de página. Para evitar ruido visual, no se repite en cada sección; queda registrada aquí como parte de la fuente.

---

## Glosario mínimo para empezar

- **Proyecto de software:** trabajo organizado para crear, mejorar, mantener o entregar un sistema de software.
- **Planificación del proyecto:** proceso de definir qué se hará, con qué recursos, en qué tiempo, con qué presupuesto y bajo qué riesgos.
- **Requerimiento:** necesidad, condición o funcionalidad que el cliente o usuario espera del sistema.
- **Alcance:** límites del proyecto; define qué incluye y qué no incluye.
- **Cronograma:** calendario de actividades, tiempos, hitos y dependencias.
- **Costo / presupuesto:** recursos económicos necesarios para ejecutar el proyecto.
- **Calidad de software:** grado en que el software cumple requisitos, funciona bien y satisface necesidades.
- **Riesgo:** situación incierta que puede afectar el proyecto positiva o negativamente.
- **Stakeholder / parte interesada:** persona, grupo u organización afectada por el proyecto o con interés en él.
- **EDT / WBS:** Estructura de Desglose del Trabajo; forma de dividir un proyecto grande en partes manejables.
- **FPA:** Function Point Analysis, o Análisis de Puntos de Función.
- **PF / FP:** Puntos de Función; medida del tamaño funcional de un sistema de software.
- **UFP:** Unadjusted Function Points; puntos de función sin ajustar.
- **VAF:** Value Adjustment Factor; factor de ajuste de valor.
- **TDI:** Total Degree of Influence; suma de factores de influencia.
- **EI:** External Input; entrada externa.
- **EO:** External Output; salida externa.
- **EQ:** External Inquiry; consulta externa.
- **ILF:** Internal Logical File; archivo lógico interno.
- **EIF:** External Interface File; archivo de interfaz externa.

---

# Agenda

## Agenda (1/3)

1. Proceso de Planificación del Proyecto
2. Introducción al Proceso de Planificación del Proyecto
3. Análisis de Requerimientos y Alcance
4. Planificación del Cronograma
5. Estimación de Costos y Presupuesto
6. Planificación de la Calidad

## Agenda (2/3)

7. Gestión de Riesgos
8. Planificación de Comunicaciones y Partes Interesadas
9. Integración y Plan de Gestión del Proyecto
10. Conclusiones
11. Estimación de Esfuerzos
12. ¿por qué es importante estimar el esfuerzo en un proyecto de software?
13. Métodos para estimar el esfuerzo en proyectos de software

## Agenda (3/3)

14. Método de análisis de puntos de función - FPA
15. Pasos para el cálculo de los PF
16. Ejemplo
17. Referencias

**Explicación sencilla:**  
La presentación tiene dos grandes partes. La primera explica cómo se planifica un proyecto de software. La segunda explica cómo se estima el esfuerzo necesario para construirlo, especialmente usando el método de Puntos de Función.

---

# 1. Proceso de Planificación del Proyecto

## Definición y Propósito (1/3)

### ISO/IEC/IEEE 12207 - Procesos del Ciclo de Vida del Software

La presentación ubica la **Planificación del Proyecto (6.3.1)** dentro de los procesos del ciclo de vida del software según la norma **ISO/IEC/IEEE 12207**.

### Procesos en Contexto de Sistema

#### Procesos de Acuerdo

- Proceso de Adquisición (6.1.1)
- Proceso de Suministro (6.1.2)

#### Procesos Organizacionales

- Gestión del Modelo de Ciclo de Vida (6.2.1)
- Gestión de Infraestructura (6.2.2)
- Gestión de Portafolio de Proyectos (6.2.3)
- Gestión de Recursos Humanos (6.2.4)
- Gestión de la Calidad (6.2.5)

#### Procesos de Proyecto

- **Planificación del Proyecto (6.3.1)**
- Evaluación y Control del Proyecto (6.3.2)
- Gestión de Decisiones (6.3.3)
- Gestión de Riesgos (6.3.4)
- Gestión de Configuración (6.3.5)
- Gestión de la Información (6.3.6)
- Medición (6.3.7)

#### Procesos Técnicos

- Definición de Requisitos de las Partes Interesadas (6.4.1)
- Análisis de Requisitos del Sistema (6.4.2)
- Diseño Arquitectónico del Sistema (6.4.3)
- Implementación (6.4.4)
- Integración del Sistema (6.4.5)
- Pruebas de Calificación del Sistema (6.4.6)
- Instalación del Software (6.4.7)
- Soporte a la Aceptación del Software (6.4.8)
- Operación del Software (6.4.9)
- Mantenimiento del Software (6.4.10)
- Retiro del Software (6.4.11)

### Procesos Específicos de Software

#### Procesos de Implementación

- Implementación de Software (7.1.1)
- Análisis de Requisitos de Software (7.1.2)
- Diseño Arquitectónico de Software (7.1.3)
- Diseño Detallado de Software (7.1.4)
- Construcción de Software (7.1.5)
- Integración de Software (7.1.6)
- Pruebas de Calificación de Software (7.1.7)

#### Procesos de Soporte

- Gestión de Documentación de Software (7.2.1)
- Gestión de Configuración de Software (7.2.2)
- Aseguramiento de la Calidad de Software (7.2.3)
- Verificación de Software (7.2.4)
- Validación de Software (7.2.5)
- Revisión de Software (7.2.6)
- Auditoría de Software (7.2.7)
- Resolución de Problemas de Software (7.2.8)

#### Procesos de Reutilización

- Ingeniería de Dominio (7.3.1)
- Gestión de Activos Reutilizables (7.3.2)
- Gestión del Programa de Reutilización (7.3.3)

**Figura 1:** Ubicación del proceso.

**Explicación sencilla:**  
La norma ISO/IEC/IEEE 12207 organiza todo lo que puede pasar durante la vida de un software: desde comprarlo o construirlo, hasta operarlo, mantenerlo y retirarlo. Dentro de esa organización, la planificación del proyecto aparece como un proceso clave porque define cómo se va a ejecutar el trabajo.

---

## Definición y Propósito (2/3)

El **Proceso de Planificación del Proyecto** es el conjunto de actividades orientadas a definir el alcance, objetivos, recursos, cronograma, costos y riesgos de un proyecto de tecnología. Su propósito es establecer una **línea base de gestión** que sirva de guía para la ejecución, monitoreo y control del proyecto, asegurando que los entregables cumplan con los requisitos de las partes interesadas.

**Explicación sencilla:**  
Planificar significa responder preguntas básicas antes de iniciar: qué se va a hacer, para qué, con quién, cuánto costará, cuánto tardará, qué puede salir mal y cómo se controlará. La **línea base de gestión** es como el punto de referencia contra el cual se revisa si el proyecto va bien o se está desviando.

---

## Definición y Propósito (3/3)

### Project Planning Process - ISO/IEC/IEEE 12207

| Entradas | Actividades | Salidas |
|---|---|---|
| 1. Acuerdo contractual o mandato del proyecto | 1. Iniciación de la planificación (analizar contrato/mandato) | 1. Plan de Proyecto de Software (Project Management Plan) |
| 2. Requisitos del cliente y del sistema | 2. Definición del alcance y objetivos; WBS preliminar | 2. Planes subsidiarios: requisitos, SQA, configuración, riesgos, V\ |
| 3. Políticas y estándares organizacionales | 3. Identificación de tareas, entregables y dependencias | 3. Cronograma detallado (WBS, duraciones, hitos) |
| 4. Modelos de ciclo de vida y metodologías | 4. Estimación de recursos, esfuerzo y costos (técnicas) | 4. Estimación de recursos y presupuesto; reservas |
| 5. Recursos disponibles (personal, herramientas, presupuesto) | 5. Desarrollo del cronograma; identificación del camino crítico | 5. Registro de supuestos y restricciones |
| 6. Lecciones aprendidas y repositorio de procesos | 6. Planificación de la organización: roles y responsabilidades | 6. Lista de riesgos iniciales y estrategias de respuesta |
| 7. Restricciones y supuestos iniciales | 7. Planificación de la gestión de riesgos (identificar y analizar) | 7. Matriz de roles y responsabilidades (p.ej. RACI) |
| 8. Riesgos identificados preliminarmente | 8. Planificación de la calidad y la configuración | 8. Línea base y elementos para el seguimiento y control |
| 9. Entradas de otras disciplinas (arquitectura, hardware) | 9. Planificación de comunicaciones y gestión de stakeholders |  |
|  | 10. Revisión, consolidación y aprobación del Plan del Proyecto |  |

**Figura 2:** Proceso de Planificación del Proyecto.

**Explicación sencilla:**  
Todo proceso tiene **entradas**, **actividades** y **salidas**. Las entradas son la información inicial. Las actividades son el trabajo de análisis y planificación. Las salidas son los documentos y acuerdos que permiten ejecutar y controlar el proyecto.

---

## Relación con el PMBOK

En el marco del **PMBOK**, el proceso de planificación es un grupo de procesos que abarca todas las áreas de conocimiento:

- Alcance, Cronograma, Costos, Calidad, Recursos, Comunicaciones, Riesgos, Adquisiciones, Partes Interesadas e Integración.
- Cada área requiere desarrollar planes subsidiarios que se integran en el **Plan de Gestión del Proyecto**.

**Explicación sencilla:**  
PMBOK es una guía de buenas prácticas para gestionar proyectos. En esa guía, planificar no es una sola tarea: incluye muchas áreas. Por ejemplo, no basta con definir fechas; también hay que definir costos, riesgos, calidad, comunicaciones y responsables.

---

## Recopilación de Requerimientos

- Identificación de las necesidades del cliente y de los usuarios finales.
- Técnicas: entrevistas, encuestas, talleres, prototipos.
- Resultado: **Documentación de Requerimientos** y **Matriz de Trazabilidad de Requerimientos**.

**Explicación sencilla:**  
Antes de construir software hay que entender qué necesitan los usuarios. Para eso se hacen entrevistas, encuestas, talleres o prototipos. La matriz de trazabilidad sirve para verificar que cada necesidad tenga seguimiento durante el proyecto.

---

## Definición del Alcance

- Elaboración de la **Declaración de Alcance** (Declaración de Alcance del Proyecto).
- Identificación de entregables, criterios de aceptación y exclusiones.
- Desarrollo de la **Estructura de Desglose del Trabajo (EDT)** para descomponer el trabajo en componentes manejables.

**Explicación sencilla:**  
Definir el alcance evita confusiones. Dice qué se entregará, cómo se aceptará y qué cosas quedan por fuera. La EDT ayuda a dividir el trabajo grande en partes pequeñas para poder gestionarlo mejor.

---

## Desarrollo del Cronograma

- Secuenciación de actividades y estimación de duraciones.
- Métodos: **Método de la Ruta Crítica (CPM)**, **Técnica de Evaluación y Revisión de Programas (PERT)**.
- Uso de herramientas como Gantt o diagramas de red.

**Explicación sencilla:**  
El cronograma organiza las actividades en el tiempo. También muestra qué tareas dependen de otras. La ruta crítica ayuda a identificar las actividades que, si se retrasan, retrasan todo el proyecto.

---

## Estimación de Costos

- Identificación de recursos necesarios (humanos, materiales, tecnológicos).
- Técnicas: análoga, paramétrica, ascendente (bottom-up), análisis de tres puntos.
- Desarrollo del **Linea Base de Costos** para el seguimiento financiero.

**Explicación sencilla:**  
Estimar costos es calcular cuánto dinero se necesita. Se consideran personas, equipos, herramientas, licencias, infraestructura y otros recursos. La línea base de costos permite comparar el gasto real con lo planeado.

---

## Gestión del Presupuesto

- Definición de reservas para contingencias y gestión.
- Integración con el cronograma para generar curvas de gasto (**S-Curves**).
- Uso de indicadores como **Gestión del Valor Ganado (EVM)** para control futuro.

**Explicación sencilla:**  
El presupuesto no solo dice cuánto se va a gastar, sino cuándo se va a gastar. Las reservas ayudan a responder ante imprevistos. EVM permite comparar avance, tiempo y costo.

---

## Enfoque de Calidad

- Identificación de estándares de calidad aplicables (ISO 9001, ISO/IEC 25010).
- Definición de métricas de calidad de software: Densidad de defectos, cobertura de código, confiabilidad.
- Planificación de auditorías y revisiones técnicas.

**Explicación sencilla:**  
La calidad se planifica desde el inicio. No se trata solo de probar al final, sino de definir estándares, métricas, revisiones y controles para saber si el software cumple lo esperado.

---

## Identificación y Análisis de Riesgos

- Registro de riesgos (**Risk Register**) con causas, efectos y responsables.
- Análisis cualitativo: probabilidad e impacto.
- Análisis cuantitativo: simulación Monte Carlo, árboles de decisión.

**Explicación sencilla:**  
Un riesgo es algo que podría pasar y afectar el proyecto. Se registra qué lo causa, qué consecuencia tendría y quién lo debe gestionar. Luego se analiza qué tan probable es y qué tan grave sería.

---

## Plan de Respuesta

- Estrategias: evitar, transferir, mitigar o aceptar riesgos.
- Definición de **Planes de contingencia** y **Planes alternativos**.
- Establecimiento de indicadores de activación (**Disparadores**).

**Explicación sencilla:**  
No basta con identificar riesgos; también hay que decidir qué hacer con ellos. Algunas veces se evita el riesgo, otras se reduce, se transfiere o se acepta. Los disparadores son señales que indican cuándo activar un plan.

---

## Gestión de las Comunicaciones

- Identificación de las necesidades de información de cada parte interesada.
- Definición de formatos, frecuencia y canales de comunicación.
- Uso de matrices RACI y herramientas colaborativas.

**Explicación sencilla:**  
Cada persona necesita información diferente. No todos requieren el mismo nivel de detalle. La gestión de comunicaciones define qué se informa, a quién, cuándo y por qué canal.

---

## Gestión de Partes Interesadas

- Análisis de poder e interés de los stakeholders.
- Estrategias de involucramiento: informar, consultar, colaborar.
- Actualización periódica del **Plan de participación de interesados**.

**Explicación sencilla:**  
Las partes interesadas pueden influir en el proyecto. Algunas tienen mucho poder de decisión; otras tienen alto interés. Por eso se define cómo involucrarlas: informarles, consultarles o trabajar con ellas.

---

## Integración de Planes Subsidiarios

- Consolidación de todos los planes en el **Plan de Gestión del Proyecto**.
- Asegurar consistencia entre alcance, cronograma, costos y calidad.
- Establecer mecanismos de control de cambios.

**Explicación sencilla:**  
Cada área tiene su propio plan, pero todos deben encajar. Si cambia el alcance, probablemente cambien el cronograma, los costos y los riesgos. Por eso se necesita control de cambios.

---

## Ejemplo de Diagrama de Integración

El diagrama muestra que el **Plan de Proyecto** integra cuatro componentes principales:

- Alcance
- Cronograma
- Costos
- Calidad

**Figura 3:** Enter Caption.

**Explicación sencilla:**  
El plan del proyecto no es un documento aislado. Une lo que se hará, cuándo se hará, cuánto costará y con qué nivel de calidad se espera entregar.

---

## Síntesis

La planificación es la base del éxito de los proyectos de software e infraestructura TIC. Un plan sólido permite anticipar problemas, optimizar recursos y alinear las expectativas de las partes interesadas, reduciendo riesgos y aumentando la probabilidad de alcanzar los objetivos estratégicos.

**Explicación sencilla:**  
Un proyecto con buena planificación tiene más posibilidades de terminar bien. No elimina todos los problemas, pero permite preverlos y responder mejor.

---

# 11. Estimación de Esfuerzos

## Estimación del Esfuerzo (1/3)

La estimación del esfuerzo de software es el proceso de estimar la cantidad de tiempo, coste y recursos necesarios para desarrollar y entregar un proyecto de software. Implica analizar varios aspectos del proyecto, como su alcance, complejidad, requisitos y recursos disponibles, para hacer predicciones informadas sobre el esfuerzo necesario para completar el proyecto con éxito.

**Explicación sencilla:**  
Estimar esfuerzo significa calcular cuántas horas, personas y recursos se necesitan para terminar un software. No es adivinar; es hacer una predicción basada en información del proyecto.

---

## Estimación del Esfuerzo (2/3)

El objetivo de la estimación del esfuerzo de software es ayudar a los jefes de proyecto y a los equipos de desarrollo a planificar y gestionar sus recursos con eficacia, y garantizar que el proyecto se complete a tiempo y dentro del presupuesto. Existen varios métodos y técnicas para la estimación del esfuerzo de software, como el juicio experto, el análisis de datos históricos y los modelos algorítmicos.

**Explicación sencilla:**  
La estimación sirve para organizar el equipo, definir fechas realistas y controlar el presupuesto. Se puede estimar con experiencia de expertos, datos de proyectos anteriores o modelos matemáticos.

---

## Estimación del Esfuerzo (3/3)

La estimación del esfuerzo puede realizarse en distintas fases del ciclo de vida del desarrollo de software, como la planificación del proyecto, el análisis de requisitos, el diseño y la implementación. La precisión de la estimación depende de varios factores, como la calidad e integridad de la información disponible, la experiencia de los estimadores y la complejidad y novedad del proyecto.

**Explicación sencilla:**  
Mientras más información exista, más precisa puede ser la estimación. Al inicio del proyecto hay más incertidumbre; a medida que se entiende mejor el sistema, la estimación mejora.

---

## Precisión de las estimaciones vs fase del proyecto

**Figura 4:** Precisión de las estimaciones vs fase del proyecto.

La figura compara la precisión de las estimaciones a lo largo de las fases del proyecto:

1. Viabilidad
2. Planificación y requisitos
3. Diseño General
4. Diseño Detallado
5. Desarrollo y test
6. Entrega

La gráfica muestra que, en fases tempranas, la variación o incertidumbre de la estimación es mayor. A medida que el proyecto avanza, la estimación tiende a acercarse más al valor real.

**Explicación sencilla:**  
Al principio se sabe poco, por eso es más fácil equivocarse al estimar. Cuando ya hay requisitos, diseño y avance técnico, la estimación se vuelve más confiable.

---

# 12. ¿por qué es importante estimar el esfuerzo en un proyecto de software?

## importancia de estimar el esfuerzo (1/6)

Estimar el esfuerzo en un proyecto de software es crucial por varias razones:

**Explicación sencilla:**  
La estimación permite tomar decisiones antes y durante el proyecto. Sin estimación, no se sabe si el tiempo, el dinero o el equipo son suficientes.

---

## importancia de estimar el esfuerzo (2/6)

### Planificación y asignación de recursos

La estimación del esfuerzo de software ayuda a los jefes de proyecto y a los equipos de desarrollo a planificar el calendario del proyecto y a asignar los recursos de forma eficaz. Al saber cuánto esfuerzo se requiere para cada tarea, pueden asignar tareas a los miembros adecuados del equipo y programarlas para garantizar que el proyecto se complete a tiempo y dentro del presupuesto.

**Explicación sencilla:**  
Saber cuánto esfuerzo toma cada tarea ayuda a decidir quién la hace, cuándo la hace y cuánto tiempo necesita.

---

## importancia de estimar el esfuerzo (3/6)

### Presupuestar

La estimación del esfuerzo también ayuda a presupuestar el proyecto. Con una estimación precisa, los gestores de proyectos pueden determinar los recursos y el presupuesto necesarios para el proyecto. También pueden comparar el esfuerzo real realizado con el estimado para asegurarse de que el proyecto se mantiene dentro del presupuesto.

**Explicación sencilla:**  
Si se estima mal el esfuerzo, se puede calcular mal el dinero. Comparar lo estimado con lo real ayuda a controlar desviaciones.

---

## importancia de estimar el esfuerzo (4/6)

### Gestión de riesgos

La estimación del esfuerzo puede ayudar a identificar posibles riesgos en el proyecto. Por ejemplo, si la estimación de una tarea concreta es significativamente superior a lo previsto, podría indicar un riesgo en el proyecto, y el equipo puede investigarlo y tomar las medidas adecuadas para mitigarlo.

**Explicación sencilla:**  
Una tarea que parece requerir demasiado esfuerzo puede ser una señal de alerta: tal vez es más compleja, falta información o requiere más recursos.

---

## importancia de estimar el esfuerzo (5/6)

### Comunicación con las partes interesadas

Una estimación precisa del esfuerzo puede ayudar a establecer expectativas realistas con las partes interesadas. Permite al equipo comunicar a los interesados la fecha de entrega estimada, los hitos del proyecto y los posibles riesgos.

**Explicación sencilla:**  
La estimación ayuda a decirle al cliente o a la dirección qué se puede esperar, cuándo se entregará y qué riesgos existen.

---

## importancia de estimar el esfuerzo (6/6)

### Medición del rendimiento

Por último, la estimación del esfuerzo es esencial para medir el rendimiento del equipo. Al comparar el esfuerzo estimado con el esfuerzo real realizado, el equipo puede identificar áreas en las que necesita mejorar la precisión de su estimación y optimizar sus procesos para futuros proyectos.

**Explicación sencilla:**  
Después de ejecutar el proyecto, comparar lo estimado con lo real permite aprender y mejorar futuras estimaciones.

---

# 13. Métodos para estimar el esfuerzo en proyectos de software

## Principales métodos de estimacion (1/6)

Existen varios métodos para estimar el esfuerzo en proyectos de software, cada uno con sus propias ventajas e inconvenientes. Los más importantes son:

**Explicación sencilla:**  
No hay un único método perfecto. La elección depende del tipo de proyecto, la información disponible y la experiencia del equipo.

---

## Principales métodos de estimacion (2/6)

### Juicio de expertos

El juicio de expertos consiste en obtener estimaciones de personas con amplia experiencia en proyectos de software similares. Este método es rápido y fácil de aplicar, pero la precisión de la estimación depende de la pericia y experiencia de los expertos.

**Explicación sencilla:**  
Se consulta a personas que ya han hecho proyectos parecidos. Es rápido, pero puede fallar si el experto se equivoca o si el proyecto actual no se parece tanto a los anteriores.

---

## Principales métodos de estimacion (3/6)

### Estimación análoga

La estimación análoga consiste en utilizar datos históricos de proyectos de software similares para estimar el esfuerzo necesario para el proyecto actual. Este método es útil cuando se carece de información detallada sobre el proyecto actual, pero su precisión depende de la similitud del proyecto histórico con el actual.

**Explicación sencilla:**  
Se toma un proyecto anterior parecido como referencia. Si el proyecto pasado y el actual son muy similares, la estimación puede ser útil.

---

## Principales métodos de estimacion (4/6)

### Estimación paramétrica

La estimación paramétrica consiste en utilizar modelos estadísticos para estimar el esfuerzo necesario para tareas o actividades específicas en función de su tamaño, complejidad y otros factores. Este método es útil para proyectos con tareas y actividades bien definidas, pero su precisión depende de la exactitud del modelo.

**Explicación sencilla:**  
Se usan fórmulas o modelos basados en variables como tamaño, complejidad o número de funcionalidades. Funciona mejor cuando hay datos confiables.

---

## Principales métodos de estimacion (5/6)

### Estimación en tres puntos

La estimación en tres puntos consiste en obtener tres estimaciones para cada tarea o actividad: optimista, más probable y pesimista. A continuación, estas estimaciones se utilizan para calcular el esfuerzo previsto necesario para la tarea o actividad. Este método es útil para proyectos con un alto grado de incertidumbre, pero puede llevar mucho tiempo obtener tres estimaciones para cada tarea.

**Explicación sencilla:**  
Para cada tarea se calcula un escenario bueno, uno normal y uno malo. Esto permite considerar la incertidumbre, aunque toma más tiempo.

---

## Principales métodos de estimacion (6/6)

### Estimación ágil

La estimación ágil implica el uso de técnicas como historias de usuario, puntos de historia y velocidad para estimar el esfuerzo de forma iterativa e incremental. Este método es útil para metodologías ágiles de desarrollo de software y proyectos con requisitos cambiantes, pero su precisión depende de la experiencia y habilidad del equipo en el uso de estas técnicas.

**Explicación sencilla:**  
En proyectos ágiles se estima por partes pequeñas y se ajusta con la experiencia del equipo. Es útil cuando los requisitos cambian o evolucionan.

---

# 14. Método de análisis de puntos de función - FPA

## Método de análisis de puntos de función - FPA (1/10)

El **Análisis de Puntos de Función (FPA)** es un método de medición del tamaño del software que cuantifica la funcionalidad proporcionada al usuario basándose en su interacción con el software. El FPA proporciona una medida del tamaño y la complejidad del software y puede utilizarse como base para estimar el esfuerzo y el coste necesarios para el desarrollo, el mantenimiento y la mejora del software.

**Explicación sencilla:**  
FPA mide el tamaño de un software según lo que el usuario puede hacer con él. No mide líneas de código, sino funciones visibles para el usuario.

---

## Método de análisis de puntos de función - FPA (2/10)

El concepto básico de FPA es identificar y categorizar las funciones proporcionadas por el software en cinco tipos de puntos de función:

**Explicación sencilla:**  
FPA clasifica las funcionalidades del sistema en cinco grupos. Cada grupo representa una forma distinta en que el sistema recibe, entrega, consulta o administra información.

---

## Método de análisis de puntos de función - FPA (3/10)

### Entradas Externas (EI)

**Definición:** Procesos donde datos ingresan al sistema para mantener información interna.

**Cómo identificarlas:**

- Los datos modifican archivos internos (crear, actualizar, eliminar).
- Provienen de formularios, APIs o cargas externas.
- Incluyen validaciones y reglas de negocio.

**Tips:**

- Si cambia el estado del sistema -> es EI.
- Ejemplo: Registrar cliente, actualizar pedido.

**Explicación sencilla:**  
Una EI ocurre cuando alguien o algo ingresa información que cambia los datos internos del sistema.

---

## Método de análisis de puntos de función - FPA (4/10)

### Salidas Externas (EO)

**Definición:** Procesos donde el sistema envía información hacia afuera con procesamiento.

**Cómo identificarlas:**

- Incluyen cálculos, agregaciones o lógica compleja.
- Generan reportes o archivos.

**Tips:**

- Si hay transformación significativa de datos -> es EO.
- Ejemplo: Reportes financieros.

**Explicación sencilla:**  
Una EO es una salida del sistema que no solo muestra datos, sino que los procesa, calcula o transforma.

---

## Método de análisis de puntos de función - FPA (5/10)

### Consultas Externas (EQ)

**Definición:** Interacciones sin modificación de datos y con lógica mínima.

**Cómo identificarlas:**

- Solo recuperan y muestran datos.
- No realizan cálculos complejos.

**Tips:**

- Si solo consulta sin transformar mucho -> es EQ.
- Ejemplo: Buscar cliente, ver estado de pedido.

**Explicación sencilla:**  
Una EQ es una consulta simple: el usuario pide información y el sistema la muestra sin cambiar datos ni hacer cálculos complejos.

---

## Método de análisis de puntos de función - FPA (6/10)

### Archivos Lógicos Internos (ILF)

**Definición:** Datos mantenidos y controlados por el sistema.

**Cómo identificarlos:**

- El sistema crea, actualiza y elimina estos datos.
- Representan entidades principales del negocio.

**Tips:**

- Si el sistema es dueño de los datos -> es ILF.
- Ejemplo: Base de datos de clientes, productos.

**Explicación sencilla:**  
Un ILF es un conjunto de datos que el propio sistema administra. Por ejemplo, clientes, productos o pedidos.

---

## Método de análisis de puntos de función - FPA (7/10)

### Archivos de Interfaz Externa (EIF)

**Definición:** Datos usados por el sistema pero mantenidos por otro sistema.

**Cómo identificarlos:**

- Solo se consultan (no se modifican).
- Provienen de sistemas externos.

**Tips:**

- Si los datos pertenecen a otro sistema -> es EIF.
- Ejemplo: Catálogo externo de monedas.

**Explicación sencilla:**  
Un EIF es información que el sistema usa, pero que no controla. Por ejemplo, una base de datos de otro sistema.

---

## Método de análisis de puntos de función - FPA (8/10)

### Reglas Mentales

- ¿Se modifican datos internos? -> EI
- ¿Sale información con procesamiento? -> EO
- ¿Solo consulta simple? -> EQ
- ¿El sistema es dueño de los datos? -> ILF
- ¿Datos de otro sistema? -> EIF

**Explicación sencilla:**  
Estas preguntas rápidas ayudan a clasificar cada funcionalidad en la categoría correcta.

---

## Método de análisis de puntos de función - FPA (9/10)

A cada punto de función se le asigna una ponderación basada en su complejidad, y los puntos de función totales para el software se calculan sumando los puntos de función ponderados para cada una de las cinco categorías. Los puntos de función resultantes proporcionan una medida estandarizada del tamaño y la complejidad del software, que puede utilizarse como base para la estimación, la evaluación comparativa y el análisis de la productividad.

**Explicación sencilla:**  
No todas las funciones pesan igual. Una funcionalidad simple suma menos puntos que una compleja. Al sumar los puntos, se obtiene una medida del tamaño funcional del software.

---

## Método de análisis de puntos de función - FPA (10/10)

El análisis de puntos de función se utiliza ampliamente en organizaciones de desarrollo de software para apoyar la estimación, medición y gestión de proyectos. Proporciona una forma coherente y objetiva de medir el tamaño y la complejidad del software, lo que puede ayudar a mejorar la precisión y la fiabilidad de las estimaciones de software, y apoyar una mejor toma de decisiones a lo largo del ciclo de vida de desarrollo de software.

**Explicación sencilla:**  
FPA ayuda a estimar de forma más objetiva, porque se basa en funciones identificables y no solo en opiniones.

---

# 15. Pasos para el cálculo de los PF

## Pasos para el cálculo de los PF (1/7)

### Paso 1

Descomponer la aplicación a construir, en funciones elementales a implementar. Para esto se puede utilizar:

1. Técnicas de descomposición funcional
2. Diagramas de flujos de datos
3. Listado de las funciones a contemplar

**Explicación sencilla:**  
Primero se divide el sistema en funcionalidades pequeñas. Esto permite contarlas y clasificarlas mejor.

---

## Pasos para el cálculo de los PF (2/7)

### Paso 2

| Tipo de función | Baja | Media | Alta |
|---|---:|---:|---:|
| EI (External Input) | 3 | 4 | 6 |
| EO (External Output) | 4 | 5 | 7 |
| EQ (External Inquiry) | 3 | 4 | 6 |
| ILF (Internal Logical File) | 7 | 10 | 15 |
| EIF (External Interface File) | 5 | 7 | 10 |

**Tabla 1:** Pesos estándar IFPUG por tipo de función y complejidad.

**Explicación sencilla:**  
Cada tipo de función tiene un peso. Si la función es baja, media o alta en complejidad, suma una cantidad diferente de puntos.

---

## Pasos para el cálculo de los PF (3/7)

### Paso 3

Obtener el total de puntos de función para la aplicación completa:

```text
TotalCuenta = Σ Cuenta
```

**Explicación sencilla:**  
Se suman todos los puntos de función contados antes del ajuste.

---

## Pasos para el cálculo de los PF (4/7)

### Paso 4: Factores de ajuste Fi

| Aspecto | Descripción |
|---|---|
| 1. Comunicación de datos | ¿Se requiere implementar mecanismos de comunicación de datos? |
| 2. Procesamiento distribuido | ¿Existen funciones que requieran de procesamiento distribuido? |
| 3. Nivel de desempeño | ¿Es crítico el desempeño del sistema para el éxito de la gestión? |
| 4. Disponibilidad del software | ¿El sistema será ejecutado en un ambiente operativo existente y fuertemente utilizado? |
| 5. Volumen de transacciones | ¿Es grande el número de transacciones que el sistema deberá soportar? |
| 6. Ingreso interactivo | ¿Requiere el sistema un alto y sofisticado nivel de ingreso interactivo de datos al sistema? |
| 7. Interfaz de usuario | ¿Es muy compleja y variada la interfaz hacia el usuario (múltiples pantallas, help línea, amistosidad, etc.)? |
| 8. Actualización en línea | ¿Se actualiza la B.D. en línea, esto es, a partir de actualizaciones interactivas? |
| 9. Complejidad interna | ¿Existen un alto nivel de programación de reglas de excepción, cálculos complejos, etc.? |
| 10. Reusabilidad | ¿Se ha de diseñar el software para ser re-utilizado en otros proyectos? |
| 11. Facilidad de instalación | ¿Están incluidas en el diseño de la solución la conversión de datos y la implementación? |
| 12. Complejidad externa de procesamiento | ¿Qué tan complejas son las entradas, salidas y consultas del sistema? |
| 13. Multiplicidad | ¿El sistema deberá soportar múltiples instalaciones para diferentes organizaciones (o sucursales)? |
| 14. Adaptabilidad | ¿Se diseñó la solución para ser fácilmente modificable y mantenible? |

| Factor | Significado |
|---:|---|
| 0 | No presente |
| 1 | Incidental |
| 2 | Moderado |
| 3 | Medio |
| 4 | Significativo |
| 5 | Esencial |

**Explicación sencilla:**  
Después de contar funciones, se revisan 14 factores que pueden hacer el sistema más o menos complejo. Cada factor se califica de 0 a 5.

---

## Pasos para el cálculo de los PF (5/7)

### Paso 5

Calcular los Puntos de Función Totales:

```text
PF = TotalCuenta * (0,65 + 0,01 * Σ Fi)
                    i=1..14
```

**Explicación sencilla:**  
La cuenta inicial se ajusta según los 14 factores. Si los factores indican mucha complejidad, el resultado final de PF aumenta.

---

## Pasos para el cálculo de los PF (6/7)

### Paso 6: Valores típicos industriales del Factor de Productividad

**Factor de Productividad típico (horas por Punto de Función)**

| Contexto del Proyecto | Horas / FP |
|---|---:|
| Aplicación simple CRUD | 5-8 |
| Sistema empresarial mediano | 10-15 |
| Sistema empresarial complejo | 15-25 |
| Sistema bancario o regulado | 20-35 |
| Sistema de tiempo real | 20-40 |
| Aplicación móvil enterprise | 12-25 |
| Proyecto con arquitectura legacy | 18-30 |
| Plataformas cloud-native maduras | 8-15 |

**Observación:** Los valores anteriores son referencias industriales aproximadas y pueden variar según:

- experiencia del equipo,
- complejidad técnica,
- automatización DevOps,
- calidad requerida,
- dominio del negocio,
- integraciones externas,
- restricciones regulatorias.

**Explicación sencilla:**  
El factor de productividad indica cuántas horas toma construir un punto de función. No es igual para todos los proyectos: un sistema simple puede requerir pocas horas por punto; uno regulado o complejo puede requerir muchas más.

---

## Pasos para el cálculo de los PF (7/7)

### Paso 7

Finalmente, calcular el esfuerzo y duración del proyecto utilizando las siguientes ecuaciones:

```text
E = PF * Factor de Productividad                       (1)

Duracion = E / Numero de Personas                      (2)
```

**Explicación sencilla:**  
Primero se calculan las horas totales de esfuerzo. Luego se dividen entre el número de personas para estimar la duración aproximada.

---

# 16. Ejemplo

## Contexto del Sistema

**Sistema:** Plataforma de Reservas Médicas

| Objetivos del negocio | Usuarios principales |
|---|---|
| Digitalizar reservas médicas | Paciente |
| Automatizar pagos online | Médico |
| Centralizar agendas médicas | Administrador |
| Reducir ausencias mediante notificaciones | Sistema de pagos |
|  | Servicio de email |

**Explicación sencilla:**  
El ejemplo se basa en una plataforma para reservar citas médicas, pagar en línea, gestionar agendas y enviar notificaciones.

---

## Alcance Funcional

| Dentro del alcance | Fuera del alcance |
|---|---|
| Registro de usuarios | Historia clínica |
| Inicio de sesión | Telemedicina |
| Búsqueda de médicos | Nómina |
| Reserva de citas | Gestión hospitalaria |
| Cancelación de citas |  |
| Gestión de agenda médica |  |
| Procesamiento de pagos |  |
| Notificaciones automáticas |  |

**Explicación sencilla:**  
El sistema se limita a reservas, pagos, agendas y notificaciones. No incluye historia clínica, telemedicina, nómina ni gestión hospitalaria.

---

## Funciones Transaccionales - EI

### External Inputs (EI)

| EI | FTR | DET | Complejidad | PF |
|---|---:|---:|---|---:|
| Registrarse | 1 | 5 | Baja | 3 |
| Iniciar sesión | 1 | 4 | Baja | 3 |
| Reservar cita | 4 | 10 | Alta | 6 |
| Cancelar cita | 3 | 6 | Media | 4 |
| Gestionar agenda | 3 | 12 | Alta | 6 |

**Total EI = 22 PF**

**Explicación sencilla:**  
Estas son acciones donde el usuario ingresa datos que modifican el sistema, como registrarse o reservar una cita.

---

## Funciones Transaccionales - EO

### External Outputs (EO)

| EO | FTR | DET | Complejidad | PF |
|---|---:|---:|---|---:|
| Confirmación reserva | 3 | 5 | Baja | 4 |
| Notificación cancelación | 2 | 6 | Media | 5 |
| Resultado pago | 3 | 8 | Media | 5 |

**Total EO = 14 PF**

**Explicación sencilla:**  
Estas son salidas del sistema hacia el usuario o servicios externos, como una confirmación de reserva o el resultado de un pago.

---

## Funciones Transaccionales - EQ

### External Inquiries (EQ)

| EQ | FTR | DET | Complejidad | PF |
|---|---:|---:|---|---:|
| Buscar médico | 2 | 4 | Baja | 3 |
| Consultar citas | 2 | 6 | Media | 4 |

**Total EQ = 7 PF**

**Explicación sencilla:**  
Son consultas que muestran información sin modificarla.

---

## Funciones de Datos - ILF

### Internal Logical Files (ILF)

| ILF | RET | DET | Complejidad | PF |
|---|---:|---:|---|---:|
| Usuarios | 2 | 8 | Baja | 7 |
| Médicos | 2 | 6 | Baja | 7 |
| Citas | 3 | 8 | Baja | 7 |
| Pagos | 1 | 6 | Baja | 7 |

**Total ILF = 28 PF**

**Explicación sencilla:**  
Son los grupos de datos que el sistema administra directamente.

---

## Funciones de Datos - EIF

### External Interface Files (EIF)

| EIF | RET | DET | Complejidad | PF |
|---|---:|---:|---|---:|
| Servicio pagos | 1 | 3 | Baja | 5 |
| Servicio email | 1 | 3 | Baja | 5 |

**Total EIF = 10 PF**

**Explicación sencilla:**  
Son datos o servicios externos que el sistema consulta o usa, pero que no controla directamente.

---

## Cálculo de UFP

### Unadjusted Function Points

| Tipo | PF |
|---|---:|
| ILF | 28 |
| EIF | 10 |
| EI | 22 |
| EO | 14 |
| EQ | 7 |

```text
UFP = 28 + 10 + 22 + 14 + 7

UFP = 81
```

**Explicación sencilla:**  
Se suman todos los puntos de función antes del ajuste. En este caso, el sistema tiene 81 puntos de función sin ajustar.

---

## Cálculo del VAF (1/1)

| Característica | Influencia |
|---|---:|
| Comunicación de datos | 4 |
| Procesamiento distribuido | 3 |
| Performance | 4 |
| Tasa de transacciones | 4 |
| Entrada online | 5 |
| Eficiencia usuario | 4 |
| Actualización online | 5 |
| Procesamiento complejo | 3 |
| Reusabilidad | 3 |
| Facilidad operacional | 4 |
| Facilidad de cambio | 4 |

```text
TDI = 51
```

### Value Adjustment Factor

```text
VAF = 0,65 + (0,01 × TDI)

VAF = 0,65 + (0,01 × 51)

VAF = 1,16
```

**Explicación sencilla:**  
El VAF ajusta los puntos de función según la influencia de características técnicas y operativas. Aquí, el TDI es 51 y el VAF queda en 1,16.

---

## Puntos de Función Ajustados

```text
FP = UFP × VAF

FP = 81 × 1,16

FP = 93,96

FP ≈ 94
```

**Resultado final:**

```text
94 Puntos de Funcion
```

**Explicación sencilla:**  
El sistema pasa de 81 puntos sin ajustar a aproximadamente 94 puntos de función ajustados.

---

## Conversión a Esfuerzo

### Supuestos

- Productividad: 11 horas / FP
- Jornada mensual: 160 horas
- Equipo: 3 personas

```text
Horas = 94 × 11

Horas = 1034

Meses/persona = 1034 / 160

Meses/persona = 6,46
```

**Explicación sencilla:**  
Si cada punto de función requiere 11 horas, construir 94 puntos requiere 1034 horas. Dividido entre jornadas mensuales de 160 horas, da 6,46 meses-persona.

---

## Duración Estimada

```text
Duracion = 6,46 / 3

Duracion ≈ 2,2 meses
```

### Distribución del esfuerzo sugerido

| Actividad | Porcentaje |
|---|---:|
| Análisis | 20 % |
| Diseño | 20 % |
| Desarrollo | 35 % |
| Testing | 20 % |
| Despliegue | 5 % |

**Explicación sencilla:**  
Si el trabajo total es de 6,46 meses-persona y hay 3 personas, la duración estimada es de aproximadamente 2,2 meses. La distribución sugiere cómo repartir el esfuerzo entre análisis, diseño, desarrollo, pruebas y despliegue.

---

# 17. Referencias

## Referencias (1/1)

La diapositiva de referencias aparece sin referencias bibliográficas visibles en el material transcrito.

---

# Información de contacto incluida en la presentación

**Albeiro Espinosa Bedoya, Ph.D. Ms.C.**  
Profesor Asociado  
Email: aespinos@unal.edu.co  
Instagram: @albeiroespinosabedoya

**Departamento de Ciencias de la Computación y de la Decisión, Facultad de Minas**  
Dirección: Av. 80 #65-223, Bloque M8A, Of. 204  
Teléfono: +57 604 4255384

---

# Cierre conceptual del documento

El material presenta una ruta completa para entender cómo se planifica un proyecto de software y cómo se estima su esfuerzo. La idea central es que un proyecto no debería iniciar solo con una intención general, sino con una planificación estructurada que incluya alcance, requerimientos, cronograma, costos, calidad, riesgos, comunicaciones y partes interesadas. Luego, para estimar esfuerzo, se introducen métodos generales y se profundiza en el Análisis de Puntos de Función, que permite medir el tamaño funcional de un sistema y convertirlo en horas, costo o duración estimada.
