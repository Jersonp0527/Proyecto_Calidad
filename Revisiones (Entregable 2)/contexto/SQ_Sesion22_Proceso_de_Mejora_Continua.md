Facultad de Minas
Sede Medellín

Calidad de Software

3007849

Albeiro Espinosa Bedoya, Ph.D. Ms.C.
Profesor Asociado

Mejora del Proceso de Software

Facultad de Minas
Sede Medellín

Diap. 2

Agenda (1/1)

1. CMMI

2. Referencias

Facultad de Minas
Sede Medellín

Diap. 3

¿Por qué hablar de mejora continua?

Pregunta de reflexión
¿Alguna vez han usado una app que “siempre está mejorando” con cada actualización?
¿Qué la hace mejor con el tiempo?

Los procesos de software son susceptibles a errores, ineficiencias y variaciones.

La mejora continua es la disciplina que responde a esa realidad.

Facultad de Minas
Sede Medellín

Diap. 4

Concepto general

Definición
La mejora continua es un enfoque sistemático para optimizar procesos, productos y
servicios a lo largo del tiempo.

En ingeniería de software busca incrementar:

• la calidad del producto,
• la eficiencia del proceso,
• la satisfacción del cliente.

Ejemplo: una app de banca digital que reduce sus tiempos de carga en cada versión.

Facultad de Minas
Sede Medellín

Diap. 5

Origen: Kaizen y calidad total

Kaizen (japonés): “cambio para mejor”.

Su aplicación moderna en software deriva
de:

• calidad total,
• gestión por procesos.

Idea clave
Mejorar en pequeños pasos, de forma
constante, en vez de grandes cambios
aislados.

Facultad de Minas
Sede Medellín

Diap. 6

Importancia en el desarrollo de software

Una cultura de mejora continua permite:

Reducir defectos en etapas tempranas.

Aumentar la previsibilidad del proceso.

Mejorar la productividad y satisfacción del equipo.

Facultad de Minas
Sede Medellín

Diap. 7

El ciclo PDCA (Deming)

Figura 1: Diagrama diagrama_001

Facultad de Minas
Sede Medellín

1. Planificar: identificar problemas y

proponer soluciones.

2. Hacer: implementar los cambios.
3. Verificar: medir resultados.
4. Actuar: estandarizar o reiniciar el ciclo.

PlanificarHacerVerificarActuarDiap. 8

Normas ISO relevantes

Norma
ISO/IEC 9001:2015
ISO/IEC 12207:2017
ISO/IEC 15504 (SPICE)
ISO/IEC 330xx

Enfoque
Gestión de la calidad
Ciclo de vida del software
Evaluación de procesos
Evolución del modelo SPICE

Error común
Adoptar una norma solo “en el papel” sin integrarla al proceso real de trabajo.

Facultad de Minas
Sede Medellín

Diap. 9

Gestión por procesos e indicadores

La organización identifica, mide y optimiza sus procesos clave.

La mejora continua se integra al ciclo de vida del software.

Se mide mediante KPI (indicadores clave de desempeño).

Indicadores típicos
Tasa de defectos por módulo · cumplimiento de cronograma · retrabajo y esfuerzo ·
satisfacción del usuario final.

Facultad de Minas
Sede Medellín

Diap. 10

Técnicas de análisis de causas

Análisis causa-efecto (Ishikawa).

Los 5 porqués.

Benchmarking de procesos.

Métricas históricas.

Figura 2: Diagrama diagrama_003

Facultad de Minas
Sede Medellín

Aumento de defectosPersonasFalta de capacitaciónProcesoSin política de cobertura mínimaHerramientasCI inactiva para métricasDiap. 11

Agile y mejora continua

Scrum y Kanban incorporan la mejora continua mediante:

Retrospectivas.

Inspección y adaptación.

Retroalimentación frecuente del cliente.

Buena práctica
Cerrar cada sprint con acciones concretas y medibles surgidas de la retrospectiva.

Facultad de Minas
Sede Medellín

Diap. 12

DevOps y mejora continua

DevOps amplía la mejora continua hacia:

Continuous Integration (integración continua).

Continuous Delivery (entrega continua).

Automatización de la retroalimentación entre desarrollo y operaciones.

Error común
Automatizar el despliegue pero no automatizar las métricas de calidad ni las pruebas.

Facultad de Minas
Sede Medellín

Diap. 13

Control estadístico y automatización

El control estadístico detecta variaciones anómalas (p. ej. gráficos de control de
defectos por iteración).

Las herramientas de CI permiten:

• monitorear calidad del código,
• generar métricas automáticas (cobertura, bugs, complejidad),
• retroalimentar en tiempo real.

La revisión de código entre pares fortalece el conocimiento técnico del equipo.

Facultad de Minas
Sede Medellín

Diap. 14

Buenas prácticas vs. errores comunes

Buenas prácticas

Medir antes y después de cada cambio.

Capacitar al equipo en las técnicas que se van a aplicar.

Automatizar la recolección de métricas.

Errores comunes

Cambiar el proceso sin datos que lo respalden.

Tratar la mejora continua como un evento único, no un ciclo.

Facultad de Minas
Sede Medellín

Diap. 15

Caso 1: Sistema web financiero – Contexto

Una empresa mediana desarrolla un sistema web financiero. Se detecta un aumento de
defectos en producción y retrasos en las entregas.

Problema inicial

Defectos en producción: 18 por cada 1000 LOC.

Cobertura de pruebas unitarias: 42 %.

Corrección de errores: 3.5 días en promedio.

Sin estandarización en revisiones de código.

Facultad de Minas
Sede Medellín

Diap. 16

Ishikawa

Figura 3: Diagrama de Ishikawa

Facultad de Minas
Sede Medellín

Diap. 17

Caso 1: Aplicación del ciclo PDCA

1. Planificar: Ishikawa + 5 porqués → falta capacitación, sin política de cobertura, CI

inactiva.

2. Hacer: pipeline CI/CD con SonarQube, capacitación en TDD, política de cobertura

mínima 70 %.

3. Verificar: revisiones semanales de métricas, dashboards de SonarQube.
4. Actuar: cobertura mínima formalizada al 75 %, pipeline automático en cada commit.

Facultad de Minas
Sede Medellín

Diap. 18

Caso 1: Resultados

Métrica
Cobertura de pruebas
Defectos / 1000 LOC
Corrección de errores
Duplicación de código

Antes
42 %
18
3.5 días
8.4 %

Después
78 %
9
1.8 días
4.1 %

Lección aprendida
La capacitación fue clave; las métricas automatizadas generaron transparencia y
compromiso.

Facultad de Minas
Sede Medellín

Diap. 19

Caso 2: Banca digital – Contexto

Un sistema de préstamos bancarios presenta retrasos en el procesamiento de
solicitudes y errores en el cálculo de intereses.

Errores de cálculo: 6 por cada 100 operaciones.

Tiempo de respuesta: 5.8 segundos.

Exactitud de cálculo: 94 %.

Satisfacción del cliente: 60 %.

Facultad de Minas
Sede Medellín

Diap. 20

Análisis con los 5 Porqués (1/2)

1. ¿Por qué hay errores en los cálculos?
Porque los valores de tasa de interés se redondean incorrectamente.

2. ¿Por qué se redondean incorrectamente?
Porque el módulo de cálculo usa una librería matemática obsoleta.

3. ¿Por qué se usa una librería obsoleta?
Porque no se ha revisado ni actualizado el componente desde hace un año.

Facultad de Minas
Sede Medellín

Diap. 21

Análisis con los 5 Porqués (2/2)

4. ¿Por qué no se revisó el componente?
Porque no existe un proceso formal de mantenimiento preventivo del código.

5. ¿Por qué no hay proceso formal de mantenimiento?
Porque la organización no tiene políticas de calidad que contemplen revisión periódica
de componentes críticos.

Causa raíz:
Ausencia de un proceso estandarizado de revisión y mantenimiento de componentes
críticos.

Facultad de Minas
Sede Medellín

Diap. 22

Caso 2: Análisis con los 5 porqués

Causa raíz
Ausencia de un proceso estandarizado de
revisión y mantenimiento de
componentes críticos.

Figura 4: Diagrama diagrama_004

Facultad de Minas
Sede Medellín

Errores en cálculosRedondeo incorrectoLibrería obsoletaSin revisión del componenteSin proceso demantenimiento preventivoDiap. 23

Caso 2: Plan y resultados

Plan: política de revisión (ISO/IEC 12207), migración a librería certificada, pruebas
automáticas de precisión, monitoreo en CI/CD.

Métrica
Errores / 100 operaciones
Exactitud del cálculo
Tiempo de respuesta
Satisfacción del cliente

Antes Después

6
94 %
5.8 s
60 %

1.5
99.2 %
4.1 s
88 %

Facultad de Minas
Sede Medellín

Diap. 24

Análisis de resultados

Las métricas confirman la eficacia del plan de mejora.

El tiempo de respuesta mejoró en un 30 %.

La reducción de defectos validó la migración tecnológica.

Facultad de Minas
Sede Medellín

1. CMMI

Facultad de Minas
Sede Medellín

Diap. 25

¿Cómo sabemos qué tan madura es una organización de software?

Pregunta de reflexión
Si dos empresas desarrollan la misma app bancaria, ¿por qué una entrega con menos
defectos y más previsibilidad que la otra?

CMMI responde a esa pregunta con un marco de madurez de procesos.

Facultad de Minas
Sede Medellín

Diap. 26

Origen de CMMI

Desarrollado por el SEI (Carnegie Mellon) en los años 90.

Nace como CMM-SW para mejorar el software del Departamento de Defensa de
EE.UU.

Basado en el CMM de los años 80; se publica como CMMI-SE/SW en 2002.

Hoy es uno de los marcos de mejora de procesos más usados en ingeniería de
software y otros sectores.

Facultad de Minas
Sede Medellín

Diap. 27

¿Qué es CMMI?

Definición
CMMI (Capability Maturity Model Integration) es un marco de mejora de procesos que
orienta cómo desarrollar y mejorar los procesos de ingeniería de software y otros
campos.

Se organiza en cinco niveles de madurez: el nivel 1 es el menos maduro y el 5 el
más maduro.

Cada nivel se apoya en el anterior con procesos más rigurosos y definidos.

Provee buenas prácticas para procesos más eficientes, eficaces y predecibles.

Facultad de Minas
Sede Medellín

Diap. 28

Constelaciones de CMMI

Constelación
CMMI-DEV
CMMI-SVC
CMMI-ACQ

Enfoque
Desarrollo de productos y servicios
Prestación de servicios y satisfacción del cliente
Adquisición y gestión de proveedores/contratos

Clave
Comparten un núcleo de prácticas comunes; cada organización elige la constelación más
cercana a su negocio.

Facultad de Minas
Sede Medellín

Diap. 29

Representación escalonada (staged) (1/2)

Figura 5: Diagrama diagrama_006

Facultad de Minas
Sede Medellín

Mide la madurez de toda la
organización.

Cada nivel exige cumplir un conjunto
fijo de áreas de proceso.

Útil para comparar organizaciones
entre sí.

1. Inicial2. Gestionado3. Definido4. Cuant. gestionado5. En optimizaciónDiap. 30

Representación escalonada (staged) (2/2)

Facultad de Minas
Sede Medellín

Diap. 31

Representación continua

Figura 6: Diagrama diagrama_007

Facultad de Minas
Sede Medellín

Mide la capacidad de cada área de
proceso por separado.

Permite mejorar procesos específicos a
su propio ritmo.

Útil cuando el negocio prioriza ciertas
áreas (ej. requisitos, calidad).

0. Incompleto1. Realizado2. Gestionado3. DefinidoDiap. 32

Estructura de CMMI: áreas de proceso

Figura 7: Diagrama diagrama_008

Facultad de Minas
Sede Medellín

Diap. 33

Categoría: Ingeniería

REQM – Gestión de Requisitos

RD – Desarrollo de Requisitos

TS – Solución Técnica

PI – Integración del Producto

VER – Verificación

VAL – Validación

Ejemplo aplicado
En un módulo de pagos móviles, RD asegura que los requisitos del cliente (límites,
seguridad, tiempos de respuesta) se documenten y validen antes de codificar.

Facultad de Minas
Sede Medellín

Diap. 34

Área de proceso: Desarrollo de Requisitos (RD)

Propósito
Producir y analizar los requisitos del cliente, del producto y de sus componentes.

SG 1: Desarrollar los requisitos del cliente.

SG 2: Desarrollar los requisitos del producto.

SG 3: Analizar y validar los requisitos.

Facultad de Minas
Sede Medellín

Diap. 35

Metas genéricas (GG) e institucionalización

GG 1: Lograr los objetivos específicos del área de proceso.

GG 2: Institucionalizar un proceso gestionado.

GG 3: Institucionalizar un proceso definido.

GG 4: Institucionalizar un proceso gestionado cuantitativamente.

GG 5: Institucionalizar un proceso en optimización.

Clave
Las metas genéricas conectan cada área de proceso con los niveles de
madurez/capacidad vistos antes.

Facultad de Minas
Sede Medellín

Diap. 36

Ventajas de usar CMMI

Mejora de la calidad de los procesos (menos defectos y repeticiones).

Mayor eficacia y productividad.

Mejor gestión de riesgos.

Mejor gestión de recursos.

Mejora de la satisfacción del cliente.

Mejor toma de decisiones basada en datos.

Ejemplo aplicado
Una empresa de banca digital reduce incidentes en producción al identificar cuellos de
botella en su proceso de pruebas usando prácticas de CMMI.

Facultad de Minas
Sede Medellín

Diap. 37

Escalonado vs. continuo: ¿cuándo usar cada uno?

Mide
Comparación
Flexibilidad

Escalonado
Madurez organizacional
Entre organizaciones
Ruta fija por niveles

Continuo
Capacidad por área
Entre procesos propios
Prioriza áreas clave

Facultad de Minas
Sede Medellín

Diap. 38

Buenas prácticas vs. errores comunes

Buenas prácticas

Elegir la constelación (DEV/SVC/ACQ) según el negocio real.

Vincular cada área de proceso a metas genéricas de institucionalización.

Errores comunes

Perseguir un nivel de madurez como sello sin cambiar el trabajo diario.

Ignorar la representación continua cuando solo se necesita mejorar un área puntual.

Facultad de Minas
Sede Medellín

Diap. 39

Caso: implementación de CMMI 2.0 en una fintech

Una empresa que desarrolla un sistema de
banca digital decide implementar CMMI
2.0 tras detectar retrasos e inconsistencias
entre equipos.

Facultad de Minas
Sede Medellín

Figura 8: Diagrama diagrama_009

1. Diagnóstico2. Alcance3. Diseño TO-BE4. PAL5. Piloto6. Ajustes7. EscalamientoDiap. 40

Fase 1-2: Diagnóstico y alcance

Diagnóstico: comparar el proceso actual con las mejores prácticas de CMMI e
identificar brechas, con todas las partes interesadas.

Alcance: definir qué áreas de proceso se cubren, el nivel de madurez objetivo,
proyectos piloto, recursos y plazos.

Facultad de Minas
Sede Medellín

Diap. 41

Fase 3-4: Diseño TO-BE y construcción de la PAL

Diseño TO-BE: rediseñar flujos, roles y métricas de desempeño; validar con los
interesados.

Construcción de la PAL (Process Asset Library): plantillas, guías y procesos
documentados, alineados a CMMI y con gestión de acceso/control.

Facultad de Minas
Sede Medellín

Diap. 42

Fase 5-6: Piloto y ajustes

Piloto: implementar el proceso mejorado en un entorno controlado y medir su
efectividad.

Ajustes: refinar el proceso con base en resultados del piloto; capacitar y
comprometer al equipo.

Facultad de Minas
Sede Medellín

Diap. 43

Fase 7: Escalamiento e institucionalización

Expandir la implementación a otros proyectos y áreas.

Asegurar que el proceso se mantenga de forma continua (institucionalización,
GG2-GG5).

Evaluaciones periódicas y mejoras adicionales basadas en desempeño.

Facultad de Minas
Sede Medellín

2. Referencias

Facultad de Minas
Sede Medellín

Diap. 44

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

