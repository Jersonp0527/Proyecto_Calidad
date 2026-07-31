# Plan de Gestión de Proyecto

## Aplicación de Gestión de Residuos – WasteTrack

**Fecha de emisión:** 2026-07-31

**Identificador único:** PMP-WT-2025-v2.1

**Organización emisora:** Grupo 09 – Calidad de Software 2025-2

**Profesor:** Albeiro Espinosa Bedoya, Ph.D., M.Sc.

## Tabla de contenidos

1.   Resumen del proyecto

2.   Referencias

3.   Definiciones

4.   Contexto del proyecto

5.   Planificación del proyecto

6.   Evaluación y control del proyecto

7.   Entrega del producto

8.   Planes de procesos de soporte

## 1. Resumen del proyecto (Cláusula 1 del PMP)

### 1.1 Propósito, alcance y objetivos (Subcláusula 1.1.1)

### Propósito

Desarrollar una plataforma digital (web + móvil) que integre a ciudadanos, administradores de residuos y autoridades locales para optimizar la recolección y tratamiento de residuos urbanos, fomentando una cultura de responsabilidad ambiental.

### Alcance

- Aplicación web y móvil multiplataforma.

- Área geográfica: ciudad piloto (áreas urbanas).

- Actores cubiertos: ciudadanos, administradores de residuos, autoridades locales.

- Excluido: gestión de residuos industriales o rurales; integraciones con sistemas de terceros fuera del piloto.

### Objetivos específicos

```text
# Objetivo                                             Indicador de éxito
O1 Crear sistema de notificaciones en tiempo real      Latencia de notificación ≤ 2 s
   para recolección
O2 Implementar módulo de información sobre             Disponible en versión 1.0
   reciclaje y separación
O3 Implementar sistema de análisis de datos para       Panel funcional con datos históricos
   autoridades
O4 Optimizar rutas de recolección                      Reducción ≥ 15 % en costos
                                                       operacionales (piloto)
O5 Incrementar tasa de reciclaje ciudadano             Incremento medible en ciudad piloto
```

### 1.2 Supuestos y restricciones (Subcláusula 1.1.2)

Supuestos - El cliente (municipio piloto) provee datos geográficos de rutas actuales. - Los ciudadanos disponen de smartphone con Android ≥ 8.0 o iOS ≥ 13. - El equipo tiene acceso continuo a internet y herramientas de desarrollo. - Los servidores en la nube estarán disponibles desde el mes 3. Restricciones - Duración fija: 6 meses (enero – junio 2026). - Presupuesto fijo académico; sin contratación externa. - Stack tecnológico definido: React, Node.js, base de datos NoSQL.

- El sistema debe cumplir normativas medioambientales locales aplicables.

### 1.3 Entregables del proyecto (Subcláusula 1.1.3)

```text
                                                                                   Fecha
Entregable                   Descripción                                           límite
E1 – Documento de            Requisitos funcionales, no funcionales y de calidad   Fin mes 1
requisitos                   completos
E2 – Prototipos UI/UX        Wireframes y mockups validados con usuarios           Fin mes 2
E3 – Release Alfa            Backend funcional + módulo ciudadanos                 Fin mes 3
E4 – Release Beta            Sistema completo con módulos administrador y          Fin mes 4
                             autoridades
E5 – Informe de pruebas      Resultados de pruebas unitarias, integración y        Fin mes 5
                             usuario
E6 – Sistema desplegado      Aplicación en producción en ciudad piloto             Fin mes 6
E7 – PMP actualizado         Versión final del plan con lecciones aprendidas       Fin mes 6
```

### 1.4 Resumen de cronograma y presupuesto (Subcláusula 1.1.4)

### Cronograma resumido por sprints (12 sprints × 2 semanas)

```text
Sprint  Semanas  Fase           Actividades principales                              Entregable
S01     1–2      Análisis       Kick-off, levantamiento de requisitos con             Acta de inicio
                                stakeholders
S02     3–4      Análisis       Análisis de sistemas existentes, documentación SRS   E1 – SRS
S03     5–6      Diseño         Diseño de arquitectura del sistema y base de datos   Diagrama arquitectura
S04     7–8      Diseño         Diseño UI/UX, wireframes, validación con usuarios    E2 – Prototipos
S05     9–10     Desarrollo     Config. CI/CD, módulo autenticación, ciudadanos v1   Build inicial
S06     11–12    Desarrollo     Módulo ciudadanos completo + notificaciones push     E3 – Release Alfa
S07     13–14    Desarrollo     Módulo administrador: rutas y estadísticas           Sprint Review
S08     15–16    Desarrollo     Módulo autoridades + integración total               E4 – Release Beta
S09     17–18    Pruebas        Pruebas unitarias e integración, corrección          Reporte defectos
S10     19–20    Pruebas        Pruebas rendimiento (k6) + usabilidad, corrección    E5 – Informe pruebas
S11     21–22    Despliegue     Despliegue producción, inicio piloto en ciudad       Sistema en producción
S12     23–24    Cierre         Evaluación piloto, lecciones aprendidas, cierre      E6 + E7
```

### Presupuesto estimado

Salario de referencia: **$5.032.812 COP/mes** (Ingeniero de Software Sénior, promedio 220 muestras. Fuente: Computrabajo Colombia – Salarios de Informática y Telecomunicaciones, 2025).

```text
Categoría                                                          Estimado (COP)
Recursos humanos – Jefe de Proyecto (25 % × 6 meses)              $ 7.549.218
Recursos humanos – Desarrollador Frontend (100 % × 4 meses)       $20.131.248
Recursos humanos – Desarrollador Backend (100 % × 4 meses)        $20.131.248
Recursos humanos – Desarrollador Full Stack (100 % × 4 meses)     $20.131.248
Recursos humanos – Diseñador UX/UI (50 % × 3 meses)               $ 7.549.218
Recursos humanos – Analista QA (variable × 2 meses)               $ 7.549.218
Subtotal Recursos Humanos (5 técnicos + JP)                       $83.041.398
Infraestructura cloud (servidor, BD, CI/CD) – 4 meses             $ 2.580.000
Herramientas y licencias (open source)                            $         0
Pruebas con usuarios (compensaciones piloto)                      $   215.000
Reserva de contingencia (10 %)                                    $ 8.583.640
Total                                                             $94.420.038
```

### 1.5 Evolución del plan (Subcláusula 1.2)

El PMP se revisará al cierre de cada fase. Las actualizaciones requerirán aprobación del jefe de proyecto y del docente asesor. Los cambios significativos al alcance activan el proceso de control de cambios (Sección 6.2).

## 2. Referencias (Cláusula 2 del PMP)

```text
Ref Documento
[1] ISO/IEC/IEEE 16326:2009 – Systems and software engineering – Life cycle processes
    – Project management
[2] ISO/IEC 12207:2008 – Software life cycle processes
[3] ISO/IEC 25010:2011 – Systems and software Quality Requirements and Evaluation
    (SQuaRE)
[4] ISO 10006:2003 – Quality management in projects
[5] Grupo09_aplicacion-de-gestion-de-residuos-wastetrack.pdf – Descripción del
    proyecto
[6] React Documentation – https://react.dev
[7] Node.js Documentation – https://nodejs.org
[8] ISO/IEC 9126:2001 – Software engineering – Product quality (reemplazado por ISO/IEC 25010)
[9] ISO/IEC 25020:2019 – SQuaRE – Measurement reference model and guide
[10] ISO/IEC 25022:2016 – SQuaRE – Measurement of quality in use
[11] ISO/IEC 25023:2016 – SQuaRE – Measurement of system and software product quality
[12] ISO/IEC 12207:2017 – Systems and software engineering – Software life cycle processes
[13] ISO 9001:2015 – Quality management systems – Requirements
[14] CMMI-DEV v2.0 – CMMI Institute (Carnegie Mellon / Isaca)
[15] Deming, W. E. – Out of the Crisis – MIT Press, 1986 (ciclo PDCA)
```

## 3. Definiciones (Cláusula 3 del PMP)

```text
Término                      Definición
```

```text
Término                       Definición
WasteTrack                    Nombre del sistema de gestión de residuos urbanos objeto de
                              este proyecto
PMP                           Plan de Gestión de Proyecto (Project Management Plan)
WBS                           Estructura de Desglose del Trabajo (Work Breakdown
                              Structure)
Ciudadano                     Usuario final que reporta y consulta información de
                              recolección
Administrador de              Operador que gestiona rutas y responde reportes
residuos
Autoridad local               Ente gubernamental con acceso al panel de análisis y políticas
Release Alfa                  Primera versión funcional con funcionalidades básicas para
                              prueba interna
Release Beta                  Versión completa para prueba con usuarios reales antes del
                              despliegue
Sprint                        Ciclo de desarrollo iterativo de 2 semanas
```

## 4. Contexto del proyecto (Cláusula 4 del PMP)

### 4.0 Sistema de Gestión de Calidad (SGC)

El SGC de WasteTrack define la política, los objetivos y el mapa de procesos que rigen el aseguramiento y control de calidad durante todo el ciclo de vida del proyecto, conforme a ISO 10006:2003, ISO/IEC 25010:2011 e ISO/IEC 12207:2008.

#### Política de calidad

WasteTrack se compromete a entregar un sistema de software que cumpla los requisitos funcionales y no funcionales acordados, mediante desarrollo iterativo con Scrum adaptado, verificación continua en cada sprint y mejora sistemática basada en métricas, asegurando la satisfacción del usuario y la conformidad con ISO/IEC 25010, ISO/IEC 12207 e ISO/IEC/IEEE 16326.

#### Objetivos de calidad

```text
#    Objetivo                               Indicador de medición                     Meta
OC1  Fiabilidad del sistema                 Disponibilidad del servicio               ≥ 99 %
OC2  Eficiencia de rendimiento              Tiempo de respuesta API/notificaciones     ≤ 2 s
OC3  Usabilidad                             Satisfacción de usuario (encuesta)        ≥ 85 % positivo
OC4  Mantenibilidad                         Cobertura de pruebas unitarias            ≥ 80 %
OC5  Seguridad                              Vulnerabilidades críticas OWASP en entrega 0
OC6  Adecuación funcional                  Requisitos cubiertos en cada release       ≥ 95 %
```

#### Mapa de procesos del SGC

```text
┌────────────────────────────────────────────────────────────────────────────┐
│                        PROCESOS ESTRATÉGICOS                               │
│  Política de calidad │ Planificación (PMP/ISO 16326) │ Revisión gerencial  │
│  (ISO 10006)         │ Gestión de riesgos            │ Auditorías internas  │
└──────────────────────────────┬─────────────────────────────────────────────┘
                               │
┌──────────────────────────────▼─────────────────────────────────────────────┐
│                   PROCESOS OPERATIVOS / MISIONALES                         │
│          (ISO/IEC 12207:2008 — Procesos Técnicos)                          │
│                                                                            │
│  Definición     Diseño      Implementación   Integración    Transición     │
│  de requisitos ─► arq. ──►  (codificación) ─►  y pruebas ─► (despliegue) │
│        │                         │                 │                       │
│     Verificación ◄───────────────┘         Validación                     │
└──────────────────────────────┬─────────────────────────────────────────────┘
                               │
┌──────────────────────────────▼─────────────────────────────────────────────┐
│                        PROCESOS DE APOYO                                   │
│  Gestión de configuración │ Medición │ Gestión de información              │
│  Gestión de calidad (QA)  │ V&V      │ Gestión de decisiones               │
│  (ISO 16326 §8)           │ Revisiones y auditorías │ Control de cambios  │
└────────────────────────────────────────────────────────────────────────────┘
```

#### Procesos del ciclo de vida aplicados — ISO/IEC 12207:2008

```text
Categoría                         Proceso aplicado                         Fase / Sprint
Procesos técnicos                 Definición de requisitos de partes        Mes 1 (S01–S02)
                                  interesadas
                                  Análisis de requisitos del sistema         Mes 1 (S02)
                                  Diseño arquitectónico                      Mes 2 (S03)
                                  Diseño detallado (UI/UX + BD)             Mes 2 (S04)
                                  Implementación (codificación)              Meses 3–4 (S05–S08)
                                  Integración del sistema                    Mes 4 (S07–S08)
                                  Verificación (pruebas unitarias)          Continuo (S05–S10)
                                  Validación (pruebas usuario + perf.)      Mes 5 (S09–S10)
                                  Transición / Despliegue                    Mes 6 (S11)

Procesos de gestión técnica       Planificación del proyecto (PMP)          Todo el proyecto
                                  Evaluación y control del proyecto          Todo el proyecto
                                  Gestión de decisiones                      Todo el proyecto
                                  Gestión de riesgos                         Todo el proyecto
                                  Gestión de configuración                   Desde Mes 1
                                  Gestión de información                     Todo el proyecto
                                  Medición (métricas por sprint)            Por sprint

Procesos organizacionales         Gestión de calidad (SGC)                  Todo el proyecto
de apoyo                          Gestión de infraestructura                 Meses 1–3
                                  Revisiones y auditorías                    Por fase
```

### 4.1 Modelo de proceso (Subcláusula 4.1)

Se adopta un ciclo de vida iterativo-incremental con marcos de Scrum adaptado:

- Sprints de 2 semanas.

- Revisión de Sprint al final de cada iteración.

- Backlog priorizado por valor de negocio y riesgo técnico.

- 3 sprints por mes en promedio.

- Entregables incrementales al final de cada fase.

### Fases del ciclo de vida

```text
[Investigación] → [Diseño] → [Desarrollo] → [Pruebas] → [Despliegue] →
[Cierre]
```

### 4.2 Plan de mejora de procesos (Subcláusula 4.2)

#### 4.2.1 Enfoque y principio Kaizen

La mejora continua es un enfoque sistemático para optimizar procesos, productos y servicios a lo largo del tiempo; en ingeniería de software busca incrementar la calidad del producto, la eficiencia del proceso y la satisfacción del cliente (ISO/IEC 12207:2017, §6.4). Siguiendo el principio **Kaizen** ("cambio para mejor"), WasteTrack aplica mejoras en pequeños pasos constantes durante cada sprint, en lugar de grandes cambios aislados, reforzando la cultura de calidad del equipo a lo largo de todo el ciclo de vida.

#### 4.2.2 Ciclo PDCA (Deming) aplicado a WasteTrack

El ciclo **PDCA** (Plan–Do–Check–Act) de Deming estructura la mejora continua del proceso en cada sprint y en cada revisión de fase:

```text
Fase PDCA    Actividad en WasteTrack                                          Responsable
Planificar   Retrospectiva al cierre de sprint: análisis Ishikawa de          Jefe de Proyecto
             problemas detectados; propuesta de acciones de mejora             + equipo
             concretas y actualización del backlog de mejoras de proceso.
Hacer        Implementar los cambios acordados en el sprint siguiente:         Equipo técnico
             nuevas políticas de cobertura, refactoring planificado,
             ajuste de pipelines CI/CD, capacitación puntual al equipo.
Verificar    Revisar métricas de calidad del §6.5 al cierre del sprint:        QA
             cobertura de pruebas, densidad de defectos, SPI, CPI;
             comparar con metas definidas en los objetivos OC1–OC6.
Actuar       Estandarizar las prácticas que mejoraron el proceso en la         Jefe de Proyecto
             Process Asset Library (PAL del proyecto); si los resultados
             no mejoran, reiniciar el ciclo con análisis más profundo.
```

> **Referencia:** Deming, W. E. – *Out of the Crisis* [15]; ISO/IEC 12207:2017, §6.4.

#### 4.2.3 Normas ISO aplicables al proceso de mejora

```text
Norma                    Enfoque                              Aplicación en WasteTrack
ISO 9001:2015            Gestión de la calidad                SGC definido en §4.0 del PMP;
                                                              política y objetivos OC1–OC6
ISO/IEC 12207:2017       Ciclo de vida del software           Mapa de procesos técnicos y
                                                              de apoyo documentado en §4.0;
                                                              proceso de medición por sprint
ISO/IEC 15504 (SPICE)    Evaluación de procesos               Marco de referencia para
                                                              evaluaciones futuras de madurez;
                                                              complementa CMMI (§4.2.7)
ISO/IEC 330xx            Evolución del modelo SPICE           Evolución aplicable a mejoras de
                                                              largo plazo posteriores al piloto
```

> **Error común a evitar:** adoptar una norma solo "en el papel" sin integrarla al trabajo diario del equipo (ISO/IEC 12207:2017).

#### 4.2.4 Técnicas de análisis de causa raíz

Cuando una métrica de calidad supera su umbral de alerta (ver §6.5), se aplican las siguientes técnicas antes de proponer acciones de mejora:

- **Diagrama causa-efecto (Ishikawa):** categorías Personas / Proceso / Herramientas / Datos. Se construye en la retrospectiva del sprint afectado.
- **Los 5 porqués:** a partir del síntoma detectado, se pregunta "¿por qué?" cinco veces en cadena hasta identificar la causa raíz.
- **Benchmarking de procesos:** comparación de métricas actuales con sprints anteriores del mismo proyecto.
- **Métricas históricas:** gráficos de control de defectos por iteración para detectar variaciones anómalas.

**Plantilla Ishikawa para retrospectiva WasteTrack:**

```text
Categoría      Factores de ejemplo en el contexto WasteTrack
Personas       Falta de capacitación en React Native; rotación de miembro del equipo
Proceso        Sin política de cobertura mínima; revisiones de código omitidas en sprint
Herramientas   CI inactiva para métricas; dependencia geoespacial sin pruebas previas
Datos          Requisitos ambiguos del municipio piloto; datos de prueba incompletos
```

#### 4.2.5 Agile y DevOps para mejora continua

- **Scrum (retrospectivas):** cada sprint cierra con una retrospectiva estructurada donde el equipo identifica qué salió bien, qué se debe mejorar y define acciones concretas y medibles para el sprint siguiente. Las acciones quedan registradas en el backlog de mejoras de proceso (PAL).
- **Inspección y adaptación:** las revisiones de sprint con stakeholders (municipio piloto, docente asesor) generan retroalimentación frecuente que retroalimenta el backlog de producto y el proceso.
- **DevOps – CI/CD:** el pipeline de GitHub Actions (§4.3) amplía la mejora continua hacia la automatización de métricas de calidad: cobertura de código, análisis estático (ESLint + SAST), detección de vulnerabilidades y pruebas regresivas automáticas en cada push.

> **Buena práctica:** cerrar cada sprint con acciones concretas y medibles surgidas de la retrospectiva. **Error a evitar:** automatizar el despliegue sin automatizar las métricas de calidad ni las pruebas (S22, Diap. 12).

#### 4.2.6 KPI de mejora continua

Los indicadores clave de desempeño del proceso se rastrean sprint a sprint y se revisan en la reunión mensual de métricas de calidad:

```text
KPI                                        Meta              Frecuencia             Responsable
Tasa de defectos por módulo (def./KLOC)    < 5               Cada sprint (CI/CD)    QA
Cumplimiento de cronograma (SPI)           ≥ 0.90            Cada sprint            Jefe de Proyecto
Retrabajo (% esfuerzo corrección /         < 15 %            Mensual                QA + JP
  esfuerzo total)
Satisfacción del usuario final             ≥ 85 % positivo   Mes 5 (beta) + S12     QA / UX
Cobertura de pruebas unitarias             ≥ 80 %            Cada sprint (CI/CD)    QA
Velocidad del equipo (SP/sprint)           ≥ 18 SP           Cada sprint            Jefe de Proyecto
```

#### 4.2.7 Modelo CMMI de referencia

**Definición:** CMMI (Capability Maturity Model Integration), desarrollado por el SEI (Carnegie Mellon), es un marco de mejora de procesos que orienta cómo desarrollar y mejorar los procesos de ingeniería de software. Se organiza en cinco niveles de madurez y provee buenas prácticas para procesos más eficientes, eficaces y predecibles [14].

**Constelación aplicable — CMMI-DEV:** dado que WasteTrack es un proyecto de desarrollo de producto software, se aplica la constelación **CMMI-DEV** (Desarrollo de productos y servicios). Las constelaciones CMMI-SVC (servicios) y CMMI-ACQ (adquisición) no corresponden al contexto del proyecto.

**Representación escalonada (staged) — 5 niveles de madurez organizacional:**

```text
Nivel   Nombre                         Descripción
1       Inicial                        Procesos impredecibles; éxito depende de personas
                                       clave; sin procesos formales
2       Gestionado                     Procesos planificados, ejecutados y controlados
                                       proyecto a proyecto; compromisos establecidos
3       Definido                       Procesos estandarizados en toda la organización;
                                       adaptados desde un conjunto de procesos estándar
4       Cuantitativamente gestionado   Procesos controlados estadísticamente; variaciones
                                       detectadas y corregidas con datos cuantitativos
5       En optimización                Mejora continua proactiva mediante innovación;
                                       causas de variación identificadas y eliminadas
```

**Nivel auto-declarado de WasteTrack:** **Nivel 2 – Gestionado**, coherente con la naturaleza académica del proyecto: PMP definido, backlog priorizado, métricas rastreadas por sprint y gestión de riesgos documentada. La ruta a Nivel 3 requeriría estandarización de procesos a nivel organizacional (grupo/empresa).

**Representación continua — niveles de capacidad por área de proceso:**

```text
Nivel   Nombre       Descripción
0       Incompleto   El proceso no se realiza o no logra sus objetivos específicos
1       Realizado    El proceso logra sus objetivos específicos
2       Gestionado   El proceso está planificado, monitoreado y controlado
3       Definido     El proceso sigue una definición organizacional estándar
```

**Áreas de proceso relevantes (CMMI-DEV) mapeadas a WasteTrack:**

```text
Área de proceso               Sigla   Descripción resumida                Sprint / Fase
Gestión de Requisitos         REQM    Gestionar requisitos y sus cambios  S01–S02 y todo el proyecto
Desarrollo de Requisitos      RD      SG1 cliente · SG2 producto ·        S01–S02 (§5.7)
                                      SG3 análisis y validación
Solución Técnica              TS      Diseño de componentes y soluciones  S03–S04 (arquitectura)
Integración del Producto      PI      Integrar componentes del sistema     S07–S08 (§5.7)
Verificación                  VER     Pruebas unitarias e integración      Continuo S05–S10
Validación                    VAL     Pruebas con usuarios y rendimiento   S09–S10 (§5.7)
```

**Metas genéricas (GG) e institucionalización:**

```text
GG 1   Lograr los objetivos específicos del área de proceso
GG 2   Institucionalizar un proceso gestionado  ← nivel actual WasteTrack (Nivel 2)
GG 3   Institucionalizar un proceso definido
GG 4   Institucionalizar un proceso gestionado cuantitativamente
GG 5   Institucionalizar un proceso en optimización
```

#### 4.2.8 Caso ilustrativo de mejora continua — módulo de rutas WasteTrack

Como referencia de aplicación práctica del ciclo PDCA, se presenta el siguiente escenario para el Sprint S07 (módulo administrador – gestión de rutas geoespaciales, 21 SP):

**Problema detectado:** en la revisión del Sprint S07 se identifica un aumento de defectos en el módulo de rutas — el de mayor complejidad del backlog.

**Análisis con Ishikawa + 5 porqués:**

```text
¿Por qué aumentaron los defectos en el módulo de rutas?
→ Porque la librería geoespacial no fue probada previamente en el stack del equipo.
¿Por qué no fue probada?
→ Porque no existe política de prueba de dependencias nuevas antes de integrarlas.
¿Por qué no existe esa política?
→ Porque el proceso de integración de dependencias no está estandarizado.
¿Por qué no está estandarizado?
→ Porque no hay checklist de incorporación de nuevas librerías en el pipeline CI/CD.
¿Por qué no hay checklist?
→ Porque la organización (equipo académico) no tiene proceso formal de evaluación
   de dependencias — causa raíz identificada.
```

**Aplicación del ciclo PDCA:**

```text
Fase        Acción aplicada en WasteTrack
Planificar  Ishikawa en retro S07 + 5 porqués → política de cobertura ≥ 80 %
            para módulos ≥ 15 SP; incorporar checklist de dependencias al pipeline
Hacer       Actualizar pipeline CI/CD con umbral de cobertura; pair programming
            en S08 para el módulo de rutas afectado; capacitación en librería
Verificar   Revisión semanal de métricas Jest coverage + análisis estático
Actuar      Política de cobertura formalizada en PAL; checklist de dependencias
            incorporado como paso obligatorio en pull request template
```

**Resultado esperado (referencia):**

```text
Métrica                      Antes (S07)   Después (S08)
Cobertura de pruebas         < 50 %        ≥ 80 %
Defectos por KLOC            Alta          < 5 def./KLOC
Tiempo de corrección defecto Largo         Reducido (< 1.8 días ref.)
Duplicación de código        No medida     Controlada (análisis estático)
```

> **Lección aprendida (S22, Caso 1):** la capacitación fue clave; las métricas automatizadas generan transparencia y compromiso del equipo.

#### 4.2.9 Buenas prácticas y errores comunes

```text
Buenas prácticas                                    Errores comunes a evitar
Medir antes y después de cada cambio de proceso     Cambiar el proceso sin datos que lo respalden
Capacitar al equipo en las técnicas a aplicar       Tratar la mejora continua como evento único,
Automatizar la recolección de métricas (CI/CD)        no como un ciclo permanente
Cerrar cada sprint con acciones concretas y         Adoptar una norma solo "en el papel"
  medibles surgidas de la retrospectiva             Perseguir un nivel CMMI como sello sin cambiar
Vincular cada área de proceso CMMI a metas            el trabajo diario del equipo
  genéricas de institucionalización (GG1–GG5)       Ignorar la representación continua de CMMI
Elegir la constelación CMMI según el negocio          cuando solo se necesita mejorar un área puntual
  real (DEV para WasteTrack)
```

### 4.3 Plan de infraestructura (Subcláusula 4.3)

```text
Componente           Tecnología               Detalle
Frontend web         React 18+                SPA, despliegue en Vercel
Aplicación móvil React Native                 Android + iOS
```

```text
Componente         Tecnología               Detalle
Backend            Node.js + Express        API REST
Base de datos      MongoDB (NoSQL)          Colecciones: usuarios, residuos, rutas, reportes
Autenticación      JWT + OAuth 2.0          —
CI/CD              GitHub Actions           Despliegue automático en rama main
Almacenamiento     AWS S3 o similar         Imágenes de reportes
Monitoreo          Grafana + Prometheus     Disponibilidad y performance
```

### 4.4 Métodos, herramientas y técnicas (Subcláusula 4.4)

```text
Área                           Herramienta
Gestión de proyecto            GitHub Projects / Trello
Control de versiones           Git + GitHub
Diseño UI/UX                   Figma
Documentación                  Markdown + Notion
Pruebas unitarias              Jest (backend) + React Testing Library (frontend)
Pruebas de integración         Supertest
Pruebas de rendimiento         k6
Análisis estático              ESLint + Prettier
Revisión de código             Pull Requests con mínimo 1 aprobador
```

### 4.5 Plan de aceptación del producto (Subcláusula 4.5)

El producto se aceptará cuando cumpla todos los criterios siguientes:

```text
Criterio                                                Meta
Tiempo de respuesta de búsqueda y notificación          ≤ 2 segundos
Tiempo de carga de pantalla                             ≤ 3 segundos en condiciones óptimas
Disponibilidad del sistema                              ≥ 99 %
Satisfacción de usabilidad (encuesta usuarios)          ≥ 85 % de evaluación positiva
Cobertura de pruebas unitarias                          ≥ 80 %
Defectos críticos abiertos en entrega                   0
```

### 4.6 Organización del proyecto (Subcláusula 4.6)

Jefe de Proyecto

```text
├── Líder de Desarrollo Frontend
│   └── Desarrollador(es) React / React Native
├── Líder de Desarrollo Backend
│   └── Desarrollador(es) Node.js / MongoDB
├── Responsable de Calidad (QA)
│   └── Analista de pruebas
└── Diseñador UX/UI
Interfaces externas: Docente asesor (revisión quincenal), municipio piloto
(retroalimentación en pruebas).
Interfaces internas: Reunión de equipo semanal (standup diario de 15 min).
```

### Autoridades y responsabilidades

```text
Rol                      Responsabilidad principal
Jefe de Proyecto         Cronograma, riesgos, comunicación con stakeholders
Líder Frontend           Arquitectura UI, revisión de código frontend
Líder Backend            Arquitectura API, revisión de código backend
QA                       Plan de pruebas, reporte de defectos, métricas de calidad
UX/UI                    Wireframes, pruebas de usabilidad, guía de estilos
```

> **Fuente de los roles:** Los roles están definidos a partir de la **Guía de Scrum** (Schwaber & Sutherland, 2020) — adaptada al contexto académico con roles técnicos diferenciados por especialidad — y de las responsabilidades genéricas de gestión de proyecto establecidas en **ISO/IEC 12207:2008, §6.2** (Proceso de gestión del proyecto). La asignación de autoridades sigue la estructura de interfaces internas y responsabilidades descrita en **ISO/IEC/IEEE 16326:2009, subcláusulas 4.6.2 y 4.6.3**.

## 5. Planificación del proyecto (Cláusula 5 del PMP)

### 5.1 Iniciación del proyecto

```text
Actividad                    Descripción                                      Responsable
Kick-off                     Reunión inicial con equipo y stakeholders        Jefe de Proyecto
Configuración de repositorio GitHub org, branches, pipelines CI/CD            Líder Backend
Configuración de ambientes Dev, Staging, Producción                           Líder Backend
Incorporación del equipo     Accesos, herramientas, onboarding                Jefe de Proyecto
```

### 5.2 Plan de estimación

Se aplican dos métodos complementarios conforme a ISO/IEC/IEEE 16326:2009 (subcláusula 5.1.1) y las técnicas vistas en clase:

1. **Método abstracto/funcional:** Análisis de Puntos de Función (FPA – IFPUG) — estima el tamaño funcional del sistema de forma independiente del equipo.

2. **Método técnico basado en equipo:** Planning Poker — el equipo de n = 5 técnicos estima el esfuerzo relativo por historia de usuario en Story Points, aportando la perspectiva de quienes construirán el sistema.

#### 5.2.1 Análisis de Puntos de Función (FPA)

### Paso 1 – Identificación y clasificación de funciones

Archivos Lógicos Internos (ILF) — datos controlados por WasteTrack

```text
ILF                                                RET DET Complejidad         PF
Usuarios (ciudadanos, admins, autoridades)         3     10    Media           10
Reportes de recolección                            2     8     Media           10
Rutas de recolección (con datos geoespaciales) 4         15    Alta            15
Notificaciones push                                1     6     Baja            7
Contenido de información de reciclaje              1     5     Baja            7
```

```text
ILF                                             RET DET Complejidad PF
Estadísticas e historial de análisis            3   12  Alta        15
Total ILF                                                           64
```

Archivos de Interfaz Externa (EIF) — datos de sistemas externos

```text
EIF                                                     RET DET    Complejidad   PF
Datos georreferenciados del municipio piloto            1      5   Baja          5
Servicio OAuth 2.0 (autenticación externa)              1     3    Baja          5
AWS S3 (almacenamiento de imágenes de reportes) 1              3   Baja          5
Total EIF                                                                        15
```

Entradas Externas (EI) — procesos que modifican datos internos

```text
EI                                                          FTR    DET   Complejidad   PF
Registro y actualización de perfil de usuario               1      5     Baja          3
Inicio de sesión (OAuth 2.0 + JWT)                          1      4     Baja          3
Crear reporte de recolección (foto + geolocalización)       2      8     Media         4
Actualizar estado de reporte (administrador)                2      7     Media         4
Crear / editar ruta de recolección                          3      12    Alta          6
Cargar contenido de información de reciclaje                2      6     Media         4
Configurar parámetros del panel de autoridad                2      8     Media         4
Registrar token de notificación push                        1      5     Baja          3
Total EI                                                                               31
```

Salidas Externas (EO) — salidas con procesamiento complejo

```text
EO                                               FTR DET     Complejidad   PF
Dashboard de análisis histórico (autoridades) 4        15    Alta          7
Reporte de rutas optimizadas (administrador) 3         10    Alta          7
Notificación push en tiempo real                 2     6     Media         5
Informe estadístico de reciclaje                 3     8     Media         5
Total EO                                                                   24
```

Consultas Externas (EQ) — consultas simples sin modificación de datos

```text
EQ                                                FTR DET Complejidad       PF
Consultar estado de recolección (ciudadano)       1       4     Baja        3
Ver perfil de usuario                             1       5     Baja        3
Ver información de reciclaje                      1       4     Baja        3
Consultar historial de reportes propios           2       6     Media       4
Ver estadísticas en tiempo real (administrador) 2         8     Media       4
Total EQ                                                                    17
```

### Paso 2 – Puntos de Función Sin Ajustar (UFP)

UFP = ILF + EIF + EI + EO + EQ UFP = 64 + 15 + 31 + 24 + 17 = 151

### Paso 3 – Factor de Ajuste de Valor (VAF)

```text
                                      Valor (0–
#   Factor de ajuste                  5)          Justificación
1   Comunicación de datos             4           API REST + WebSockets para
                                                  notificaciones push
2   Procesamiento distribuido         3           Web + móvil + nube (cloud)
3   Nivel de desempeño                4           Requisito: latencia ≤ 2 s
4   Disponibilidad del software       5           Requisito: ≥ 99 % uptime
5   Volumen de transacciones          3           Ciudad piloto; escala moderada
6   Ingreso interactivo               4           Múltiples formularios en móvil y web
7   Interfaz de usuario               4           3 tipos de usuario + dashboards de
                                                  análisis
8   Actualización en línea            4           Reportes y notificaciones en tiempo
                                                  real
9   Complejidad interna               3           Optimización de rutas con datos
                                                  geoespaciales
10 Reusabilidad                       2           Componentes React compartidos
11 Facilidad de instalación           3           CI/CD automatizado con GitHub
                                                  Actions
12 Complejidad externa de             3           OAuth + AWS S3 + FCM
   procesamiento
13 Multiplicidad                      2           Un municipio piloto (escalable)
14 Adaptabilidad                      3           Arquitectura modular y mantenible
TDI = 4+3+4+5+3+4+4+4+3+2+3+3+2+3 = 47
```

VAF = 0,65 + (0,01 × 47) = 1,12

### Paso 4 – Puntos de Función Ajustados (FP)

FP = UFP × VAF = 151 × 1,12 ≈ 169 FP

### Paso 5 – Factor de productividad

Según los valores industriales típicos, WasteTrack combina características de “Aplicación móvil enterprise” (12–25 h/FP) y “Plataforma cloud-native” (8–15 h/FP). Dado que el equipo es académico con experiencia media en React/Node.js y primera exposición a React Native, se selecciona 12 h/FP como valor conservador dentro del rango inferior.

### Paso 6 – Esfuerzo total estimado

E_FPA = FP × Factor de productividad E_FPA = 169 × 12 = 2.028 horas

### Paso 7 – Distribución del esfuerzo por fase

```text
Fase                         %        Horas estimadas
Análisis y requisitos        20 %     406 h
Diseño                       20 %     406 h
Desarrollo / programación    35 %     710 h
Pruebas                      20 %     406 h
Despliegue                   5%       101 h
Total                        100 %    2.028 h
```

**Esfuerzo total FPA:** E_FPA = 169 FP × 12 h/FP = **2.028 horas**

**Duración en meses-persona:** 2.028 / 160 = 12,68 meses-persona

**Duración calendario con n = 5 técnicos (capacidad paralela):**

Con n = 5 personas técnicas trabajando en paralelo durante la fase de desarrollo (meses 2–5) y un factor de eficiencia del 65 % (descontando reuniones, revisiones y coordinación):

```text
Capacidad efectiva mensual = n × h/mes × eficiencia
                           = 5 × 160 × 0,65
                           = 520 h/mes

Duración de la fase de desarrollo = E_FPA / Capacidad_mensual
                                  = 2.028 / 520
                                  ≈ 3,9 meses
```

El resultado confirma que la fase técnica cabe en 4 meses (Meses 2–5). El cronograma total de 6 meses incluye el mes de análisis y requisitos (Mes 1) y el mes de despliegue y cierre (Mes 6), que no son paralelizables en su totalidad.

**Utilización del equipo** (sobre capacidad total disponible de 2.640 h): 2.061 / 2.640 × 100 = **78,1 %**, conservando un margen de gestión del 21,9 % para imprevistos y cambios controlados.

#### 5.2.2 Planning Poker – Estimación técnica por equipo

Planning Poker es una técnica ágil de estimación por consenso donde cada integrante del equipo técnico evalúa independientemente el esfuerzo relativo de cada historia de usuario usando la escala Fibonacci (1, 2, 3, 5, 8, 13, 21). Complementa a FPA aportando la perspectiva técnica de quienes construirán el sistema (n = 5 técnicos).

### Reglas de la sesión

- Cada participante revela su estimación simultáneamente (sin influencia previa).
- Si la variación entre estimaciones supera un nivel de la escala Fibonacci, se abre debate y se vota de nuevo.
- El valor consensuado es la mediana del grupo.
- **Moderador:** Jefe de Proyecto (sin voto, rol Scrum Master).
- **Participantes votantes (n = 5):** Desarrollador Frontend, Desarrollador Backend, Desarrollador Full Stack, Analista QA, Diseñador UX/UI.

### Resultado de la sesión de Planning Poker

```text
Historia de Usuario                            D.Front  D.Back  D.Full  QA   UX   Consenso SP
Autenticación y perfiles de usuario            13       8       13      8    13   13
Reporte de recolección (foto + geoloc.)        8        8       5       8    5    8
Notificaciones push en tiempo real             13       13      21      13   13   13
Módulo de información de reciclaje             5        5       5       3    5    5
Gestión de rutas de recolección (admin)        21       21      21      21   21   21
Estadísticas en tiempo real (admin)            13       13      8       13   8    13
Panel de análisis histórico (autoridades)      21       21      21      13   21   21
API REST base + autenticación JWT              13       13      8       13   8    13
Integración y despliegue CI/CD                 8        5       8       8    5    8
Total Story Points                                                                 115 SP
```

### Conversión SP → horas (n = 5 técnicos)

Con n = 5 personas técnicas en sprints de 2 semanas:

```text
Capacidad bruta por sprint  = 5 personas × 80 h/sprint = 400 h
Factor de eficiencia (65 %) = 400 × 0,65 = 260 h netos/sprint
Velocidad establecida        = 20 SP/sprint
Factor de conversión         = 260 h / 20 SP = 13 h/SP
```

**Esfuerzo técnico puro (desarrollo):** E_PP = 115 SP × 13 h/SP = **1.495 horas**

**Esfuerzo total con overhead del proceso** (40 % adicional por análisis, gestión de proyecto, pruebas y despliegue):

```text
E_PP_total = 1.495 × 1,40 = 2.093 horas
```

### Duración calendario con n = 5 técnicos

```text
Capacidad mensual efectiva = 5 × 160 × 0,65 = 520 h/mes

Duración de la fase técnica = E_PP_total / Capacidad_mensual
                            = 2.093 / 520
                            ≈ 4,0 meses
```

El resultado es consistente con los 4 meses planificados para la fase de desarrollo (Meses 2–5), lo que valida la estimación de Planning Poker con el cronograma definido.

#### 5.2.3 Consolidación de estimaciones

```text
Método                                Esfuerzo estimado   Base del cálculo
FPA – estimación funcional            2.028 h             169 FP × 12 h/FP
Planning Poker – estimación técnica   2.093 h             115 SP × 13 h/SP × 1,40 (overhead)
Estimación definitiva (promedio)      2.061 h             Diferencia < 4 %; alta convergencia
```

La convergencia entre métodos (diferencia < 4 %) valida la estimación con alta confiabilidad. FPA aporta la perspectiva funcional (qué debe construirse), mientras Planning Poker aporta la perspectiva técnica del equipo (cómo se construirá con n = 5 personas). Se adopta **2.061 horas** como línea base de esfuerzo.

```text
Parámetro                              Valor
Puntos de Función ajustados (FP)       169 FP
Story Points consensuados (PP)         115 SP
Esfuerzo total estimado                2.061 h
Capacidad disponible del equipo        2.640 h (6 meses)
Utilización del equipo                 78,1 %
Margen de gestión                      21,9 %
Cronograma resultante                  6 meses (viable; fase de desarrollo ≈ 4 meses con n=5)
```

#### 5.2.4 Planificación de sprints (Story Points)

Los Story Points provienen de la sesión de Planning Poker (§5.2.2) y se usan para la planificación táctica de los sprints de desarrollo (S05–S10). La velocidad de 20 SP/sprint se justifica con **n = 5 técnicos**:

- Capacidad bruta: 5 personas × 8 h/día × 10 días hábiles = **400 h/sprint**
- Eficiencia efectiva (65 %): 400 × 0,65 = **260 h netos/sprint**
- Factor de conversión: 260 / 20 SP = **13 h/SP**

```text
Módulo                                                    Story Points   FP equivalente
Autenticación y perfiles de usuario                       13             18 FP
Reporte de necesidad de recolección (ciudadanos)          8              11 FP
Notificaciones en tiempo real (push + web)                13             18 FP
Módulo de información de reciclaje                        5              7 FP
Gestión de rutas de recolección (administrador)           21             30 FP
Estadísticas en tiempo real (administrador)               13             18 FP
Panel de control y análisis histórico (autoridades)       21             30 FP
API REST base + autenticación JWT                         13             18 FP
Integración y despliegue                                  8              19 FP
Total                                                     115 SP         169 FP
```

**Velocidad:** 20 SP/sprint × 6 sprints de desarrollo = 120 SP (buffer de 5 SP para correcciones).

### Aclaración sobre la línea base de Story Points

La línea base total del proyecto es de 115 Story Points. Esta cifra incluye 107 Story Points asociados directamente a funcionalidades del producto y 8 Story Points correspondientes a integración, configuración técnica, despliegue y estabilización. Todos los documentos contractuales y de planificación deberán utilizar esta misma línea base.

### 5.3 Plan de personal

```text
Rol                           # personas    Dedicación      Meses
Jefe de Proyecto              1             25 %            1–6
Desarrollador Frontend        1             100 %           2–5
Desarrollador Backend         1             100 %           2–5
Desarrollador Full Stack      1             100 %           2–5
Diseñador UX/UI               1             50 %            1–3
```

```text
Rol                      # personas Dedicación Meses
QA / Analista de pruebas 1          50 %       4–5; 100 % mes 5
```

### Capacidad estimada por rol

```text
                             Dedicación         Periodo de                 Capacidad
Rol                          promedio           participación              estimada
Jefe de proyecto             25 %               6 meses                    240 h
Diseñador UX/UI              50 %               3 meses                    240 h
Desarrollador frontend       100 %              4 meses                    640 h
Desarrollador backend        100 %              4 meses                    640 h
Desarrollador full stack     100 %              4 meses                    640 h
Analista QA                  Variable           3 meses                    240 h
Capacidad total              —                  —                          2.640 h
estimada
```

### 5.4 Plan de adquisición de recursos

```text
Recurso                                   Tipo              Cuándo          Responsable
Servidor cloud (AWS/GCP/Azure)            Infraestructura   Inicio mes 3    Jefe de Proyecto
Cuenta MongoDB Atlas                      Infraestructura   Inicio mes 2    Líder Backend
Licencia Figma (equipo)                   Herramienta       Inicio mes 1    UX/UI
Dispositivos de prueba (Android/iOS)      Hardware          Inicio mes 4    QA
```

### 5.5 Plan de capacitación del equipo

```text
Tema                                  Audiencia                   Cuándo
React Native (móvil)                  Desarrolladores Frontend    Mes 1
MongoDB agregaciones avanzadas        Backend                     Mes 1–2
Pruebas con k6 (performance)          QA                          Mes 4
Grafana – dashboards de monitoreo     QA + Jefe Proyecto          Mes 5
```

### 5.6 Estructura de Desglose del Trabajo (WBS)

WasteTrack

```text
├── 1. Gestión del Proyecto
│   ├── 1.1 Planificación y PMP
│   ├── 1.2 Seguimiento y control
│   └── 1.3 Cierre del proyecto
├── 2. Investigación y Requisitos
│   ├── 2.1 Levantamiento de requisitos con stakeholders
│   ├── 2.2 Análisis de sistemas existentes
│   └── 2.3 Documentación de requisitos (SRS)
├── 3. Diseño
│   ├── 3.1 Diseño de arquitectura del sistema
│   ├── 3.2 Diseño de base de datos
│   ├── 3.3 Diseño UI/UX (wireframes + prototipos)
│   └── 3.4 Validación de diseño con usuarios
├── 4. Desarrollo
│   ├── 4.1 Configuración de entorno y CI/CD
│   ├── 4.2 Módulo de autenticación y perfiles
│   ├── 4.3 Módulo ciudadanos (reportes + notificaciones)
│   ├── 4.4 Módulo de información de reciclaje
│   ├── 4.5 Módulo administrador (rutas + estadísticas)
│   ├── 4.6 Módulo autoridades (panel + análisis)
│   └── 4.7 Integración frontend-backend
├── 5. Pruebas
│   ├── 5.1 Pruebas unitarias
│   ├── 5.2 Pruebas de integración
│   ├── 5.3 Pruebas de rendimiento (k6)
│   ├── 5.4 Pruebas de usabilidad con usuarios reales
│   └── 5.5 Corrección de defectos
└── 6. Despliegue
    ├── 6.1 Configuración de producción
    ├── 6.2 Piloto en ciudad seleccionada
    └── 6.3 Documentación final y entrega
```

### 5.7 Cronograma detallado

```text
Sprint  Mes  Semanas  Actividad principal                                    Entregable
S01     1    1–2      Kick-off, levantamiento de requisitos con stakeholders  Acta de inicio
S02     1    3–4      Análisis de sistemas existentes, documentación SRS      E1 – SRS
S03     2    5–6      Diseño de arquitectura del sistema y base de datos      Diagrama arquitectura
S04     2    7–8      Diseño UI/UX, wireframes, validación con usuarios       E2 – Prototipos validados
S05     3    9–10     Config CI/CD, módulo autenticación/perfiles,            Build inicial /
                      módulo ciudadanos v1 (13 SP)                           Sprint Review
S06     3    11–12    Módulo ciudadanos completo + notificaciones push        E3 – Release Alfa
                      (13 + 8 SP)
S07     4    13–14    Módulo administrador: gestión de rutas (21 SP)          Sprint Review
S08     4    15–16    Estadísticas admin (13 SP) + módulo autoridades         E4 – Release Beta
                      (21 SP) + integración total
S09     5    17–18    Pruebas unitarias e integración (todos los módulos),    Reporte de defectos
                      corrección de defectos prioritarios
S10     5    19–20    Pruebas de rendimiento k6 (API REST base 13 SP) +       E5 – Informe de pruebas
                      pruebas de usabilidad, corrección final
S11     6    21–22    Despliegue en producción (Integración/CI 8 SP),         Sistema en producción
                      inicio piloto en ciudad seleccionada
S12     6    23–24    Evaluación del piloto, lecciones aprendidas, cierre     E6 + E7
                      formal del proyecto
```

**Total:** 12 sprints × 2 semanas = 24 semanas (6 meses). Sprints S05–S10 son de desarrollo activo (115 SP en 6 sprints ≈ 19,2 SP/sprint ≈ 20 SP/sprint con buffer).

### 5.8 Asignación de recursos por actividad (extracto)

```text
Actividad             Frontend Backend QA UX JP
Requisitos            ✓            ✓          ✓ ✓ ✓
Diseño arquitectura ✓           ✓          —    ✓    ✓
```

```text
Actividad              Frontend Backend QA UX JP
Desarrollo módulos     ✓        ✓       — — —
Pruebas                —             —        ✓    ✓    —
Despliegue             ✓             ✓        ✓    —    ✓
```

### 5.9 Asignación presupuestaria

El presupuesto del proyecto WasteTrack se calcula en **pesos colombianos (COP)** usando como referencia el salario promedio de Ingeniero de Software Sénior publicado en **Computrabajo Colombia – Salarios de Informática y Telecomunicaciones**: **$5.032.812 COP/mes** (basado en 220 muestras salariales, 2025). Para la infraestructura cloud se aplica una tasa de referencia de **$4.300 COP/USD** (2025-2026).

```text
Rol / Categoría                                          Cálculo                     Presupuesto (COP)
Jefe de Proyecto (25 % × 6 meses)                       5.032.812 × 0,25 × 6        $  7.549.218
Desarrollador Frontend (100 % × 4 meses)                5.032.812 × 1,00 × 4        $ 20.131.248
Desarrollador Backend (100 % × 4 meses)                 5.032.812 × 1,00 × 4        $ 20.131.248
Desarrollador Full Stack (100 % × 4 meses)              5.032.812 × 1,00 × 4        $ 20.131.248
Diseñador UX/UI (50 % × 3 meses)                        5.032.812 × 0,50 × 3        $  7.549.218
Analista QA (50 % mes 4 + 100 % mes 5 = 1,5 mes eff.)  5.032.812 × 0,75 × 2        $  7.549.218
Subtotal recursos humanos                                —                            $ 83.041.398
Infraestructura cloud (servidor, BD, CI/CD) × 4 meses   $150 USD × 4 × 4.300        $  2.580.000
Herramientas y licencias (open source)                   —                           $          0
Pruebas con usuarios (compensaciones piloto)             $50 USD × 4.300             $    215.000
Reserva de contingencia (10 %)                           (83.041.398+2.795.000)×0,10 $  8.583.640
Total del proyecto                                       —                            $ 94.420.038
```

**Distribución del esfuerzo humano por fase:**

```text
Fase                              % esfuerzo   Horas asociadas   Costo personal (COP)
Investigación, análisis y diseño  40 %          825 h             $ 33.216.559
Desarrollo e integración          35 %          722 h             $ 29.064.489
Pruebas, despliegue y cierre      25 %          514 h             $ 20.760.350
Total esfuerzo humano             100 %         2.061 h           $ 83.041.398
```

Fuente salarial: [Computrabajo Colombia – Salarios de Informática y Telecomunicaciones](https://co.computrabajo.com/salarios-de-informatica-y-telecom?by=averageDesc()) (consulta 2025).

### 5.10 Dependencias entre actividades

La siguiente tabla describe las relaciones de precedencia entre las actividades del WBS. Las actividades del camino crítico están marcadas con ★.

```text
ID     Actividad                                                Predecesoras            Mes
A01    ★ Kick-off y acta de inicio                              —                       1
A02    ★ Levantamiento de requisitos con stakeholders           A01                     1
```

```text
ID     Actividad                                               Predecesoras            Mes
A03    ★ Documentación SRS                                     A02                     1
A04    ★ Diseño de arquitectura del sistema                    A03                     2
A05    Diseño de base de datos                                 A04                     2
A06    Diseño UI/UX (wireframes)                               A03                     2
A07    Validación de diseño con usuarios                       A06                     2
A08    ★ Configuración entorno y CI/CD                         A04                     3
A09    ★ Módulo de autenticación y perfiles                    A05, A08                3
A10    ★ Módulo ciudadanos (reportes + notificaciones)         A09                     3–4
A11    Módulo de información de reciclaje                      A09                     3–4
A12    ★ Módulo administrador (rutas + estadísticas)           A10                     4
A13    ★ Módulo autoridades (panel + análisis)                 A12                     4
A14    ★ Integración frontend-backend                          A10, A11, A12, A13      4
A15    Pruebas unitarias (continuas por módulo)                A09 en adelante        3–5
A16    ★ Pruebas de integración                                A14                    5
A17    Pruebas de rendimiento k6                               A16                     5
A18    Pruebas de usabilidad con usuarios                      A14                     5
A19    ★ Corrección de defectos críticos                       A16, A17, A18           5
A20    ★ Despliegue en producción                              A19                     6
A21    ★ Piloto ciudad (E6)                                    A20                     6
A22    Documentación final y lecciones aprendidas (E7)         A21                    6
```

**Camino crítico:** A01 → A02 → A03 → A04 → A08 → A09 → A10 → A12 → A13 → A14 → A16 → A19 → A20 → A21

### Verificación del camino crítico

El camino crítico fue determinado a partir de las dependencias y duraciones planificadas. Las actividades con holgura total igual a cero se consideran críticas.

Duración

```text
ID  Actividad                              estimada      Predecesora      Holgura Estado
A01 Kick-off y acta de inicio              1 semana      —                0       Crítica
A02 Levantamiento de requisitos            2 semanas     A01              0       Crítica
    con stakeholders
A03 Documentación SRS                      1 semana      A02              0         Crítica
A04 Diseño de arquitectura del             2 semanas     A03              0         Crítica
    sistema
```

Duración

```text
ID  Actividad                            estimada          Predecesora      Holgura Estado
A08 Configuración entorno y CI/CD        3 semanas         A04              0       Crítica
A09 Módulo de autenticación y            2 semanas         A05, A08         0       Crítica
    perfiles
A10 Módulo ciudadanos (reportes +        3 semanas         A09              0        Crítica
    notificaciones)
A12 Módulo administrador (rutas +        2 semanas         A10              0        Crítica
    estadísticas)
A13 Módulo autoridades (panel +          2 semanas         A12              0        Crítica
    análisis)
A14 Integración frontend-backend         2 semanas         A10, A11, A12,   0        Crítica
                                                           A13
A16    Pruebas de integración            1 semana          A14              0        Crítica
A19    Corrección de defectos críticos   1 semana          A16, A17, A18    0        Crítica
A20    Despliegue en producción          1 semana          A19              0        Crítica
A21    Piloto ciudad (E6)                1 semana          A20              0        Crítica
```

Cualquier retraso en una actividad con holgura igual a cero genera un retraso equivalente en la fecha final del proyecto, salvo que se apliquen medidas de compresión del cronograma.

## 6. Evaluación y control del proyecto (Cláusula 6 del PMP)

### 6.1 Plan de gestión de requisitos

- Los requisitos se documentan en el SRS y se rastrean en la tabla de trazabilidad.

- Toda solicitud de cambio de requisito pasa por el proceso de control de cambios (6.2).

- Los requisitos se priorizan con técnica MoSCoW (Must/Should/Could/Won’t).

### 6.2 Plan de control de cambios de alcance

1. Se registra la solicitud de cambio (Change Request – CR).

2.   El jefe de proyecto evalúa impacto en tiempo, costo y calidad.

3.   Se presenta al docente asesor si el impacto supera 1 sprint o $50 USD.

4.   Se aprueba o rechaza y se actualiza el PMP y backlog.

### 6.3 Plan de control del cronograma

- Revisión semanal del avance real vs. planificado.

- Índice de Rendimiento del Cronograma (SPI): alerta si SPI < 0.9.

- Acciones correctivas: reasignación de recursos o reducción de alcance en sprints futuros.

### 6.4 Plan de control del presupuesto

- Reporte mensual de gasto real vs. presupuestado.

- Índice de Rendimiento de Costo (CPI): alerta si CPI < 0.9.

- Reserva de contingencia: 10 % del presupuesto total ($65 USD).

### 6.5 Plan de aseguramiento de calidad

#### 6.5.1 Marco normativo de calidad (ISO/IEC 25000 SQuaRE)

La evaluación de la calidad del producto WasteTrack se apoya en la familia de normas **ISO/IEC 25000 – SQuaRE** (Software Product Quality Requirements and Evaluation), que actualiza y amplía la norma ISO/IEC 9126 [8]:

```text
Norma           Nombre                              Pregunta central            Produce
ISO/IEC 25010   Modelo de calidad del software      ¿Qué es calidad?            Características y
                                                                                subcaracterísticas
ISO/IEC 25020   Guía de medición de calidad         ¿Cómo medir?                Métricas, indicadores
                                                                                y criterios
ISO/IEC 25022   Medición de calidad en uso          ¿Cómo lo vive el usuario?   Métricas de eficacia
                                                                                y satisfacción
ISO/IEC 25023   Medición de calidad del producto    ¿Cómo es el software?       Métricas técnicas
                                                                                objetivas
ISO/IEC 25030   Requisitos de calidad               ¿Qué exigir?                Especificación de
                                                                                requisitos de calidad
ISO/IEC 25040   Evaluación del producto software    ¿Cómo evaluar?              Proceso de evaluación
```

> **Flujo integrado:** 25010 define qué medir → 25020 define cómo medir → 25023 mide el producto → 25022 mide la experiencia del usuario → el resultado es un plan de mejora basado en evidencia.

#### 6.5.2 Método GQM: 5 pasos de evaluación de calidad (ISO 9126 — aplicables al proyecto)

El método GQM (Goal–Question–Metric) estructurado en ISO 9126 define **5 pasos** para evaluar la calidad durante el ciclo de desarrollo. El paso 1 se realiza en el análisis de requisitos; los pasos 2–5 se repiten en cada actividad del ciclo de vida (ISO/IEC 12207).

**Paso 1: Identificación de los requisitos de calidad**

Para cada característica y subcaracterística del modelo de calidad se asigna un peso de necesidad (Alto / Medio / Bajo) que permite centrar los esfuerzos evaluativos en las subcaracterísticas más importantes para WasteTrack.

*Calidad en uso:*

```text
Característica en uso    Peso (Alto / Medio / Bajo)   Justificación WasteTrack
Eficacia                 Alto                         Ciudadanos deben lograr reportar sin asistencia
Productividad            Medio                        Tiempo de tarea relevante pero no crítico
Seguridad en uso         Alto                         Errores en reportes afectan gestión municipal
Satisfacción             Alto                         Adopción ciudadana depende de UX positiva
Contexto de uso          Medio                        Red móvil variable; dispositivos heterogéneos
```

*Calidad externa e interna (ISO/IEC 25010):*

```text
Característica              Subcaracterística              Peso
Adecuación funcional        Completitud funcional          Alto
                            Corrección funcional           Alto
                            Adecuación funcional           Alto
Eficiencia de desempeño     Comportamiento temporal        Alto
                            Utilización de recursos        Medio
                            Capacidad                      Medio
Compatibilidad              Coexistencia                   Medio
                            Interoperabilidad              Medio
Usabilidad                  Aprendibilidad                 Medio
                            Operabilidad                   Alto
                            Accesibilidad                  Alto
                            Protección ante errores        Medio
Fiabilidad                  Madurez                        Alto
                            Disponibilidad                 Alto
                            Tolerancia a fallos            Alto
                            Recuperabilidad                Alto
Seguridad                   Confidencialidad               Alto
                            Integridad                     Alto
                            No-repudio                     Medio
                            Autenticidad                   Alto
                            Trazabilidad                   Medio
Mantenibilidad              Analizabilidad                 Alto
                            Modificabilidad                Alto
                            Testabilidad                   Alto
Portabilidad                Adaptabilidad                  Medio
                            Instalabilidad                 Medio
                            Reemplazabilidad               Bajo
```

**Paso 2: Especificación de la evaluación**

Para cada subcaracterística se identifican las métricas aplicables y los niveles requeridos. La tabla completa de métricas con nivel requerido y resultado real de la evaluación se presenta en §6.5.3 (calidad del producto) y §6.5.4 (calidad en uso). En la columna "Resultado real" se registra el valor medido al cierre del sprint o fase correspondiente.

> **Nota (ISO 9126):** es posible que algunas filas estén vacías en actividades tempranas del ciclo de desarrollo, ya que no todas las subcaracterísticas pueden medirse desde el inicio.

**Paso 3: Diseño de la evaluación**

Plan de medición por subcaracterística clave, entregables a evaluar y tipos de métricas aplicables:

```text
Subcaracterística          Entregables a evaluar       Métricas int.        Métricas ext.       Métricas cal. en uso
Completitud funcional      E1-SRS·E3-Alfa·E4-Beta      Trazabilidad RF      % RF cubiertos      N/A
                                                       · Cobertura CP       por release
Corrección funcional       E4-Beta · E5-Pruebas        Densidad             Defectos críticos   N/A
                                                       defectos/KLOC        = 0
Disponibilidad             E6-Producción · S12         N/A                  Uptime ≥ 99 %       Eficacia usuario
                                                                            · MTBF · MTTR
Comportamiento temporal    E3-Alfa · E4-Beta           Complejidad          T. resp. API        N/A
                                                       ciclomática          · Throughput
Operabilidad               E2-Prototipos·E5-Pruebas    N/A                  Tasa éxito tareas   Satisfacción ·
                                                                                                Productividad
Confidencialidad           E4-Beta · E6-Producción     Análisis SAST        Vulns OWASP         Seguridad en uso
                                                       (100 % cobertura)    Top 10 = 0
```

**Paso 4: Ejecución de la evaluación**

Este paso se aplica durante cada sprint de desarrollo (S05–S10) y en el piloto (S12). Se ejecuta el plan de medición del Paso 3 y se completan las columnas "Resultado real" de las tablas de §6.5.3 y §6.5.4. El pipeline CI/CD (GitHub Actions + ESLint + Jest) automatiza la recolección de métricas internas en cada push. La serie de normas **ISO/IEC 14598** se usa como guía para planificar y ejecutar el proceso de medición.

**Paso 5: Retroalimentación a la organización**

Una vez completadas todas las mediciones, los resultados se incluyen en el Informe final de calidad (§7 — entregable al docente). Se identifican las áreas en que la calidad debe mejorar para que el producto satisfaga las necesidades del usuario. Los resultados se integran al proceso **Verificar / Actuar** del ciclo PDCA (§4.2.2) y al cálculo del Indicador Global de Preferencia LSP (§6.5.5).

#### 6.5.3 Métricas de calidad del producto (ISO/IEC 25023)

Las métricas se organizan según las 8 características de calidad de ISO/IEC 25010 (ISO/IEC 25023:2016 [11]). Tipo de métrica según ISO/IEC 25020 [9]: **directa** (medida objetiva), **derivada** (calculada) o **subjetiva** (percepción). La columna "Resultado real" se completa al cierre de cada sprint / fase.

```text
Característica ISO 25010     Métrica                                  Meta               Frecuencia
Adecuación funcional         % de requisitos cubiertos por release    ≥ 95 %             Por release
                             Defectos críticos abiertos en entrega    0                  Por release
Eficiencia de rendimiento    Tiempo de respuesta API / notificación   ≤ 2 s              Cada sprint
                             Tiempo de carga de pantalla              ≤ 3 s              Cada sprint
                             Throughput API bajo carga                ≥ 100 req/s        Sprint 9–10
Compatibilidad               Pruebas en matriz dispositivos           100 % pass         Sprint 9–10
                             (Android ≥ 8.0, iOS ≥ 13, web)
Usabilidad                   Satisfacción de usuario (encuesta)       ≥ 85 % positivo    Mes 5 (beta)
                             Tasa de éxito en tareas clave            ≥ 90 %             Mes 5 (beta)
Fiabilidad                   Disponibilidad del sistema               ≥ 99 %             Mensual (mes 3+)
                             MTBF (tiempo medio entre fallos)         ≥ 720 h            Mes 6 (piloto)
                             MTTR (tiempo medio de recuperación)      ≤ 4 h              Mes 6 (piloto)
Seguridad                    Vulnerabilidades críticas OWASP Top 10   0                  Sprint 8–10
                             Cobertura de análisis estático (SAST)    100 %              Cada sprint (CI)
Mantenibilidad               Cobertura de pruebas unitarias           ≥ 80 %             Cada sprint
                             Complejidad ciclomática por función      ≤ 10               Cada sprint
                             Densidad de defectos                     < 5 defectos/KLOC  Cada sprint
Portabilidad                 Tiempo de despliegue automatizado        ≤ 30 min           Sprint 11
```

> **Referencia:** ISO/IEC 25023:2016 [11]; ISO/IEC 25020:2019 [9].

#### 6.5.4 Métricas de calidad en uso (ISO/IEC 25022)

La calidad en uso mide el grado en que el sistema permite a los usuarios alcanzar sus objetivos de forma eficaz, eficiente y satisfactoria en el contexto de uso real (ISO/IEC 25022:2016). Se evalúa durante las pruebas de usabilidad (S10) y el piloto (S12):

```text
Característica       Métrica definida                                  Meta           Sprint / Fase
Eficacia             % ciudadanos que crean reporte sin asistencia     ≥ 90 %         S10 · S12
Productividad        Tiempo promedio de creación de reporte            ≤ 60 s         S10 · S12
Seguridad en uso     Reportes duplicados o erróneos sin confirmación   < 2 %          S10 · S12
Satisfacción         Encuesta post-tarea (escala Likert 1–5)           ≥ 4.2 / 5      S10 · S12
                     (equivale al ≥ 85 % positivo declarado en OC3)
Contexto de uso      Pruebas en red móvil 3G/4G · Android ≥ 8.0       100 % pass     S10
                     · iOS ≥ 13 (condiciones declaradas en §1.2)
```

> **Diferencia clave (S15):** un sistema puede tener 0 errores técnicos y aun así tener baja calidad en uso si los usuarios no logran sus tareas. Esta tabla complementa la de §6.5.3. **Referencia:** ISO/IEC 25022:2016 [10].

#### 6.5.5 Marco de evaluación de 4 etapas + agregación LSP

Siguiendo el marco de evaluación basado en ISO/IEC 25010, 25020 y 25040, se define un proceso auto-evaluativo de 4 etapas que se ejecuta al cierre del piloto (Sprint S12):

**Etapa 1 — Árbol de requerimientos de calidad WasteTrack**

Estructura jerárquica que descompone las características de calidad en subcaracterísticas y atributos cuantificables (Característica → Subcaracterística → Atributo medible):

```text
1. Adecuación funcional

   1.1 Completitud funcional
       1.1.1 Cobertura de requisitos del SRS (% RF cubiertos en release final)
       1.1.2 Cobertura de casos de uso verificados (% casos de prueba pasados)

   1.2 Corrección funcional
       1.2.1 Defectos críticos en entrega a producción (número)
       1.2.2 Densidad de defectos por módulo (defectos / KLOC)

2. Usabilidad

   2.1 Operabilidad del ciudadano
       2.1.1 Tasa de éxito en creación de reporte sin asistencia (%)
       2.1.2 Tiempo promedio de creación de reporte (segundos)

   2.2 Satisfacción percibida
       2.2.1 Puntuación en encuesta post-piloto (escala 1–5)

3. Fiabilidad

   3.1 Disponibilidad
       3.1.1 Uptime del sistema durante el período de piloto (%)

   3.2 Recuperabilidad
       3.2.1 MTTR – Tiempo medio de recuperación ante fallo (horas)
       3.2.2 MTBF – Tiempo medio entre fallos (horas)
```

**Etapa 2 — Especificación de métricas**

Una métrica convierte una observación (conteo, sí/no, tiempo) en un valor normalizado entre 0 % y 100 % que permite comparar atributos de distinta naturaleza.

```text
Atributo   Fórmula de normalización (0 % – 100 %)
1.1.1      (RF cubiertos / RF totales del SRS) × 100 %
1.1.2      (CP pasados / CP totales ejecutados) × 100 %
1.2.1      100 % si defectos_críticos = 0;  0 % si defectos_críticos ≥ 1
1.2.2      máx(0,  (1 − densidad / 5) × 100 %)     [referencia: meta < 5 def./KLOC]
2.1.1      (reportes exitosos / intentos totales) × 100 %
2.1.2      mín(100,  (60 / t_promedio_segundos) × 100 %)     [ideal ≤ 60 s]
2.2.1      (puntaje_promedio / 5) × 100 %
3.1.1      uptime directamente en %
3.2.1      mín(100,  (4 / MTTR_horas) × 100 %)     [ideal ≤ 4 h]
3.2.2      mín(100,  (MTBF_horas / 720) × 100 %)   [meta ≥ 720 h]
```

**Escala de aceptabilidad:**

```text
Rango           Nivel            Significado
[0 %, 40 %)     Insatisfactorio  El atributo no cumple los requisitos
[40 %, 60 %)    Marginal         Cumplimiento parcial
[60 %, 100 %]   Satisfactorio    Cumple los requisitos
```

**Etapa 3 — Medición de atributos (Indicadores Elementales)**

Tabla para registrar los Indicadores Elementales (IE) al cierre del piloto (S12). Los valores se completan durante la ejecución del Paso 4 del método GQM (§6.5.2):

```text
Atributo   Descripción                                IE (%)   Fuente de medición
1.1.1      Cobertura de requisitos del SRS            ____     SRS + Backlog sprint S11
1.1.2      Cobertura de casos de uso verificados      ____     Reporte CI/CD (Jest coverage)
1.2.1      Defectos críticos en entrega               ____     Rastreo de defectos QA
1.2.2      Densidad de defectos por módulo            ____     Análisis estático / SonarQube
2.1.1      Tasa de éxito en creación de reporte       ____     Pruebas de usabilidad S10 (QA)
2.1.2      Tiempo promedio de creación de reporte     ____     Pruebas de usabilidad S10 (QA)
2.2.1      Puntuación encuesta post-piloto            ____     Encuesta Likert S12
3.1.1      Uptime del sistema                         ____     Grafana + Prometheus (S11–S12)
3.2.1      MTTR                                       ____     Grafana (mes 6 / piloto)
3.2.2      MTBF                                       ____     Grafana (mes 6 / piloto)
```

**Etapa 4 — Cálculo con modelo de agregación LSP**

El modelo **LSP (Logic Scoring of Preference)** combina los indicadores elementales en un Indicador Global (IG) mediante la fórmula de media de potencia pesada:

```text
IG = P1 · IE1 + P2 · IE2 + … + Pm · IEm     (con ΣPi = 1)
```

Donde `Pi` es el peso asignado a cada característica o subcaracterística e `IEi` es el valor medido (entre 0 y 1). Los pesos reflejan la importancia relativa según la política de calidad del §4.0 y los objetivos OC1–OC6:

```text
Característica / Subcaracterística       Peso    IE (%)   IG parcial
1. Adecuación funcional                  0.35    ____     ____
   1.1 Completitud funcional             0.60
       1.1.1 Cobertura requisitos SRS    0.60    ____
       1.1.2 Cobertura casos de uso      0.40    ____
   1.2 Corrección funcional              0.40
       1.2.1 Defectos críticos           0.70    ____
       1.2.2 Densidad defectos           0.30    ____
2. Usabilidad                            0.25    ____     ____
   2.1 Operabilidad ciudadano            0.60
       2.1.1 Tasa éxito reporte          0.50    ____
       2.1.2 Tiempo promedio reporte     0.50    ____
   2.2 Satisfacción percibida            0.40
       2.2.1 Encuesta post-piloto        1.00    ____
3. Fiabilidad                            0.25    ____     ____
   3.1 Disponibilidad                    0.60
       3.1.1 Uptime sistema              1.00    ____
   3.2 Recuperabilidad                   0.40
       3.2.1 MTTR                        0.40    ____
       3.2.2 MTBF                        0.60    ____
4. Eficiencia de desempeño               0.10    ____     ____
   (atributo directo: tiempo resp. API — IE de §6.5.3)
5. Seguridad                             0.05    ____     ____
   (atributo directo: vulns OWASP = 0 → 100 % — IE de §6.5.3)

ΣPi = 0.35 + 0.25 + 0.25 + 0.10 + 0.05 = 1.00

IG = 0.35·IG1 + 0.25·IG2 + 0.25·IG3 + 0.10·IG4 + 0.05·IG5 = ____
```

**Criterio de aceptación adicional:** el Indicador Global de Preferencia debe alcanzar **IG ≥ 60 %** (nivel Satisfactorio) al cierre del piloto (Sprint S12). Este criterio complementa los criterios de aceptación del producto definidos en §4.5.

> **Referencia:** ISO/IEC 25040; marco de evaluación LSP (S16, Diap. 9–34); ISO/IEC 25020:2019 [9].

#### 6.5.6 Actividades de aseguramiento

- Revisión de código por pares (pull request obligatorio con mínimo 1 aprobador).
- Análisis estático automático en CI/CD (ESLint + análisis SAST).
- Ejecución automática de suite de pruebas en cada push a rama develop y main.
- Revisión periódica de métricas de mantenibilidad del código (cobertura, complejidad ciclomática, duplicación).

### 6.6 Plan de cierre del proyecto

```text
Actividad de cierre                                      Responsable           Cuándo
Aceptación formal del sistema por cliente piloto         Jefe de Proyecto      Semana 23
Documentación de lecciones aprendidas                    Todo el equipo        Semana 23
Versión final del PMP                                    Jefe de Proyecto      Semana 24
Archivo de todos los artefactos del proyecto             QA                    Semana 24
Presentación final al docente                            Todo el equipo        Semana 24
```

## 7. Entrega del producto (Cláusula 7 del PMP)

```text
Componente             Descripción                           Destinatario
Código fuente          Repositorio GitHub completo           Equipo + Docente
Aplicación web         URL de producción                     Municipio piloto
```

```text
Componente               Descripción                          Destinatario
Aplicación móvil         APK Android + TestFlight iOS         Usuarios piloto
Manual de usuario        Guía por tipo de actor               Ciudadanos / Admins /
                                                              Autoridades
Manual de                Instrucciones técnicas de            Equipo técnico municipio
despliegue               instalación
Informe final de         Métricas, resultados de pruebas,      Docente
calidad                  cobertura
```

## 8. Planes de procesos de soporte (Cláusula 8 del PMP)

### 8.1 Gestión de decisiones

Las decisiones técnicas o de gestión con impacto mayor se documentan con el formato: [Decisión] – [Alternativas consideradas] – [Criterio de selección] – [Fecha] – [Responsable] Decisiones significativas se revisan en la reunión semanal de equipo y se archivan en el repositorio del proyecto.

### 8.2 Gestión de riesgos

**Proceso:** Identificar → Analizar → Plani icar respuesta → Monitorear

### Registro de riesgos

```text
ID  Riesgo                  Prob. Impacto Severidad Estrategia                 Responsable
R01 Rotación o baja         Media Alto    Alto      Mitigar:                   Jefe
    disponibilidad de                               documentación              Proyecto
    un miembro del                                  continua; backup
    equipo                                          de conocimiento
R02 Requisitos              Alta  Alto    Alto      Mitigar: sesiones          Jefe
    ambiguos o                                      de validación              Proyecto
    cambiantes por                                  frecuentes; CR
    parte del                                       formal
    municipio piloto
R03 Fallas en               Baja     Alto      Medio        Contingencia:      Líder
    infraestructura                                         plan de            Backend
    cloud                                                   recuperación,
                                                            backups diarios
R04 Rendimiento             Media Medio        Medio        Mitigar: pruebas   QA
    insuficiente                                            de carga con k6
    (tiempos de                                             desde mes 4
    respuesta > 3 s)
```

```text
ID  Riesgo                 Prob. Impacto Severidad Estrategia                    Responsable
R05 Baja adopción por      Media Medio   Medio     Mitigar: campaña              UX/UI
    ciudadanos en el                               de comunicación
    piloto                                         y onboarding
                                                   simple
R06 Deuda técnica          Media Alto    Alto      Mitigar:                      Líderes
    acumulada que                                  revisiones de                 técnicos
    retrasa entregas                               código en cada
                                                   sprint, refactoring
                                                   planificado
R07 Incumplimiento         Baja  Alto    Alto      Contingencia:                 Jefe
    del plazo de 6                                 reducir alcance de            Proyecto
    meses                                          módulo
                                                   autoridades a
                                                   MVP
```

### 8.3 Gestión de configuración

- Repositorio: GitHub (rama main protegida; PRs requeridos).

- Estrategia de ramas: GitFlow (main, develop, feature/*, hotfix/*).

- Versionado: Semántico (MAJOR.MINOR.PATCH).

- Baseline: Se establece baseline al cierre de cada fase.

- Control de cambios: Todo cambio a baseline requiere PR aprobado por ≥ 1 revisor.

- CCB (Change Control Board): Jefe de Proyecto + Líder técnico afectado.

### 8.4 Gestión de la información

Frecuencia de

```text
Tipo de información      Repositorio                Acceso          actualización
Código fuente            GitHub                     Equipo          Continuo
Documentación            GitHub /docs               Equipo          Por sprint
técnica
Backlog y tareas         GitHub Projects            Equipo          Semanal
Reportes de calidad      Carpeta compartida         Equipo +        Por sprint
                                                    Docente
Comunicaciones           Email institucional        Equipo +        Según necesidad
formales                                            Docente
Actas de reunión         Notion / carpeta           Equipo          Después de cada
                         compartida                                 reunión
```

**Política de retención:** Todos los artefactos del proyecto se conservan en repositorio GitHub por mínimo 2 años después del cierre.

### 8.5 Documentación

### Documentos mínimos requeridos

```text
Documento                            Versión mínima     Responsable
PMP (este documento)                 1.0                Jefe de Proyecto
Especificación de Requisitos (SRS)   1.0                Todo el equipo
Documento de Arquitectura            1.0                Líderes técnicos
Plan de Pruebas                      1.0                QA
Manual de Usuario                    1.0                UX/UI + QA
Informe final de calidad             1.0                QA
```

### Apéndice A – Matriz de trazabilidad de requisitos (extracto)

```text
ID                                                                            Prueba
Req   Descripción                    Tipo                     Módulo          asociada
RF-01 Creación de perfil de          Funcional                Ciudadanos      TC-001
      ciudadano
RF-02 Reporte de necesidad de        Funcional                Ciudadanos      TC-002
      recolección
RF-03 Notificaciones en tiempo       Funcional                Ciudadanos      TC-003
      real
RF-04 Gestión de rutas de            Funcional                Administrador   TC-010
      recolección
RF-05 Estadísticas en tiempo         Funcional                Administrador   TC-011
      real
RF-06 Panel de análisis histórico    Funcional                Autoridades     TC-020
RNF- Tiempo de carga ≤ 3 s           No funcional             Transversal     TC-P-001
01                                   (rendimiento)
RNF- Disponibilidad ≥ 99.9 %         No funcional             Infraestructura TC-P-002
02                                   (disponibilidad)
RNF- Accesibilidad WCAG 2.1          No funcional             Transversal     TC-U-001
03    AA                             (usabilidad)
RNF- Compatibilidad Android ≥        No funcional             Móvil           TC-C-001
04    8.0 e iOS ≥ 13                 (compatibilidad)
RCA- Respuesta ≤ 2 s para            Calidad                  Transversal     TC-P-003
01    búsqueda y notificación
RCA- Satisfacción usabilidad ≥       Calidad                  Transversal     TC-U-002
```

```text
ID                                                                         Prueba
Req    Descripción                 Tipo                    Módulo          asociada
02     85 %
RCA-   Cobertura pruebas           Calidad                 Transversal     Cobertura
03     unitarias ≥ 80 %                                                    CI/CD
```

Documento elaborado bajo los lineamientos de ISO/IEC/IEEE 16326:2009 para el curso Calidad de Software 2025-2. Versión 2.1 — Julio 2026. Incorpora métricas de calidad (ISO/IEC 25000 SQuaRE, GQM, LSP) y proceso de mejora continua (PDCA, CMMI) conforme a Sesiones 14, 15, 16 y 22.
