# Plan de Gestión de Proyecto

## Aplicación de Gestión de Residuos – WasteTrack

**Fecha de emisión:** 2026-06-24

**Identificador único:** PMP-WT-2025-v2.0

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

- Retrospectiva al final de cada sprint.

- Métricas de velocidad de equipo rastreadas por sprint.

- Revisión mensual de métricas de calidad.

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

### Métricas de calidad rastreadas continuamente (ISO/IEC 25010:2011)

Las métricas se organizan según las 8 características de calidad de ISO/IEC 25010:

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

**Actividades de aseguramiento:** - Revisión de código por pares (pull request obligatorio).

- Análisis estático automático en CI/CD (ESLint). - Ejecución automática de suite de pruebas en cada push. - Revisión periódica de métricas de mantenibilidad del código.

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

Documento elaborado bajo los lineamientos de ISO/IEC/IEEE 16326:2009 para el curso Calidad de Software 2025-2. Versión 1.0 — Junio 2026
