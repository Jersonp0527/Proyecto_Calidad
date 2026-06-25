# Plan de Gestión de Proyecto
## Aplicación de Gestión de Residuos – WasteTrack
**Versión:** 1.0  
**Fecha de emisión:** 2026-06-24  
**Identificador único:** PMP-WT-2025-v1.0  
**Organización emisora:** Grupo 09 – Calidad de Software 2025-2  
**Profesor:** Albeiro Espinosa Bedoya, Ph.D., M.Sc.

---

## Página de firmas

| Rol | Nombre | Firma | Fecha |
|-----|--------|-------|-------|
| Jefe de Proyecto | ________________________ | _________ | ________ |
| Líder técnico | ________________________ | _________ | ________ |
| Responsable de calidad | ________________________ | _________ | ________ |
| Docente revisor | Albeiro Espinosa Bedoya | _________ | ________ |

---

## Historial de cambios

| Versión | Fecha | Páginas modificadas | Descripción del cambio |
|---------|-------|---------------------|------------------------|
| 1.0 | 2026-06-24 | Todas | Versión inicial del PMP |

---

## Prefacio

Este documento es el Plan de Gestión de Proyecto (PMP) para el desarrollo de **WasteTrack**, una aplicación móvil y web de gestión de residuos urbanos. Está redactado conforme a la norma **ISO/IEC/IEEE 16326:2009** y es el documento rector de todas las actividades de planificación, ejecución y control del proyecto.

**Audiencia:** Equipo de desarrollo, docente asesor y evaluadores del curso Calidad de Software 2025-2.

El PMP es un documento vivo; se actualiza ante cambios de alcance, cronograma o recursos y toda revisión queda registrada en el historial de cambios.

---

## Tabla de contenidos

1. Resumen del proyecto  
2. Referencias  
3. Definiciones  
4. Contexto del proyecto  
5. Planificación del proyecto  
6. Evaluación y control del proyecto  
7. Entrega del producto  
8. Planes de procesos de soporte  

---

## 1. Resumen del proyecto (Cláusula 1 del PMP)

### 1.1 Propósito, alcance y objetivos (Subcláusula 1.1.1)

**Propósito**  
Desarrollar una plataforma digital (web + móvil) que integre a ciudadanos, administradores de residuos y autoridades locales para optimizar la recolección y tratamiento de residuos urbanos, fomentando una cultura de responsabilidad ambiental.

**Alcance**  
- Aplicación web y móvil multiplataforma.  
- Área geográfica: ciudad piloto (áreas urbanas).  
- Actores cubiertos: ciudadanos, administradores de residuos, autoridades locales.  
- Excluido: gestión de residuos industriales o rurales; integraciones con sistemas de terceros fuera del piloto.

**Objetivos específicos**

| # | Objetivo | Indicador de éxito |
|---|----------|--------------------|
| O1 | Crear sistema de notificaciones en tiempo real para recolección | Latencia de notificación ≤ 2 s |
| O2 | Implementar módulo de información sobre reciclaje y separación | Disponible en versión 1.0 |
| O3 | Implementar sistema de análisis de datos para autoridades | Panel funcional con datos históricos |
| O4 | Optimizar rutas de recolección | Reducción ≥ 15 % en costos operacionales (piloto) |
| O5 | Incrementar tasa de reciclaje ciudadano | Incremento medible en ciudad piloto |

---

### 1.2 Supuestos y restricciones (Subcláusula 1.1.2)

**Supuestos**
- El cliente (municipio piloto) provee datos geográficos de rutas actuales.
- Los ciudadanos disponen de smartphone con Android ≥ 8.0 o iOS ≥ 13.
- El equipo tiene acceso continuo a internet y herramientas de desarrollo.
- Los servidores en la nube estarán disponibles desde el mes 3.

**Restricciones**
- Duración fija: **6 meses** (enero – junio 2026).
- Presupuesto fijo académico; sin contratación externa.
- Stack tecnológico definido: React, Node.js, base de datos NoSQL.
- El sistema debe cumplir normativas medioambientales locales aplicables.

---

### 1.3 Entregables del proyecto (Subcláusula 1.1.3)

| Entregable | Descripción | Fecha límite |
|------------|-------------|--------------|
| E1 – Documento de requisitos | Requisitos funcionales, no funcionales y de calidad completos | Fin mes 1 |
| E2 – Prototipos UI/UX | Wireframes y mockups validados con usuarios | Fin mes 2 |
| E3 – Release Alfa | Backend funcional + módulo ciudadanos | Fin mes 3 |
| E4 – Release Beta | Sistema completo con módulos administrador y autoridades | Fin mes 4 |
| E5 – Informe de pruebas | Resultados de pruebas unitarias, integración y usuario | Fin mes 5 |
| E6 – Sistema desplegado | Aplicación en producción en ciudad piloto | Fin mes 6 |
| E7 – PMP actualizado | Versión final del plan con lecciones aprendidas | Fin mes 6 |

---

### 1.4 Resumen de cronograma y presupuesto (Subcláusula 1.1.4)

**Cronograma resumido**

```
Mes 1: Investigación y levantamiento de requisitos
Mes 2: Diseño de arquitectura y UI/UX
Mes 3: Desarrollo – Módulo ciudadanos y backend base
Mes 4: Desarrollo – Módulo administrador y autoridades
Mes 5: Pruebas, corrección de defectos y optimización
Mes 6: Despliegue, piloto y cierre
```

**Presupuesto estimado**

| Categoría | Estimado |
|-----------|----------|
| Recursos humanos (4 desarrolladores × 6 meses) | Valorizado en créditos académicos |
| Infraestructura cloud (servidor, BD, CI/CD) | $150 USD/mes × 4 meses = $600 USD |
| Herramientas y licencias | $0 (herramientas open source) |
| Pruebas con usuarios | $50 USD (compensaciones piloto) |
| **Total** | **≈ $650 USD** |

---

### 1.5 Evolución del plan (Subcláusula 1.2)

El PMP se revisará al cierre de cada fase. Las actualizaciones requerirán aprobación del jefe de proyecto y del docente asesor. Los cambios significativos al alcance activan el proceso de control de cambios (Sección 6.2).

---

## 2. Referencias (Cláusula 2 del PMP)

| Ref | Documento |
|-----|-----------|
| [1] | ISO/IEC/IEEE 16326:2009 – Systems and software engineering – Life cycle processes – Project management |
| [2] | ISO/IEC 12207:2008 – Software life cycle processes |
| [3] | ISO/IEC 25010:2011 – Systems and software Quality Requirements and Evaluation (SQuaRE) |
| [4] | ISO 10006:2003 – Quality management in projects |
| [5] | Grupo09_aplicacion-de-gestion-de-residuos-wastetrack.pdf – Descripción del proyecto |
| [6] | React Documentation – https://react.dev |
| [7] | Node.js Documentation – https://nodejs.org |

---

## 3. Definiciones (Cláusula 3 del PMP)

| Término | Definición |
|---------|------------|
| **WasteTrack** | Nombre del sistema de gestión de residuos urbanos objeto de este proyecto |
| **PMP** | Plan de Gestión de Proyecto (Project Management Plan) |
| **WBS** | Estructura de Desglose del Trabajo (Work Breakdown Structure) |
| **Ciudadano** | Usuario final que reporta y consulta información de recolección |
| **Administrador de residuos** | Operador que gestiona rutas y responde reportes |
| **Autoridad local** | Ente gubernamental con acceso al panel de análisis y políticas |
| **Release Alfa** | Primera versión funcional con funcionalidades básicas para prueba interna |
| **Release Beta** | Versión completa para prueba con usuarios reales antes del despliegue |
| **Sprint** | Ciclo de desarrollo iterativo de 2 semanas |

---

## 4. Contexto del proyecto (Cláusula 4 del PMP)

### 4.1 Modelo de proceso (Subcláusula 4.1)

Se adopta un ciclo de vida **iterativo-incremental** con marcos de **Scrum** adaptado:

- Sprints de 2 semanas.
- Revisión de Sprint al final de cada iteración.
- Backlog priorizado por valor de negocio y riesgo técnico.
- 3 sprints por mes en promedio.
- Entregables incrementales al final de cada fase.

**Fases del ciclo de vida:**

```
[Investigación] → [Diseño] → [Desarrollo] → [Pruebas] → [Despliegue] → [Cierre]
```

### 4.2 Plan de mejora de procesos (Subcláusula 4.2)

- Retrospectiva al final de cada sprint.
- Métricas de velocidad de equipo rastreadas por sprint.
- Revisión mensual de métricas de calidad.

### 4.3 Plan de infraestructura (Subcláusula 4.3)

| Componente | Tecnología | Detalle |
|------------|------------|---------|
| Frontend web | React 18+ | SPA, despliegue en Vercel |
| Aplicación móvil | React Native | Android + iOS |
| Backend | Node.js + Express | API REST |
| Base de datos | MongoDB (NoSQL) | Colecciones: usuarios, residuos, rutas, reportes |
| Autenticación | JWT + OAuth 2.0 | — |
| CI/CD | GitHub Actions | Despliegue automático en rama main |
| Almacenamiento | AWS S3 o similar | Imágenes de reportes |
| Monitoreo | Grafana + Prometheus | Disponibilidad y performance |

### 4.4 Métodos, herramientas y técnicas (Subcláusula 4.4)

| Área | Herramienta |
|------|-------------|
| Gestión de proyecto | GitHub Projects / Trello |
| Control de versiones | Git + GitHub |
| Diseño UI/UX | Figma |
| Documentación | Markdown + Notion |
| Pruebas unitarias | Jest (backend) + React Testing Library (frontend) |
| Pruebas de integración | Supertest |
| Pruebas de rendimiento | k6 |
| Análisis estático | ESLint + Prettier |
| Revisión de código | Pull Requests con mínimo 1 aprobador |

### 4.5 Plan de aceptación del producto (Subcláusula 4.5)

El producto se aceptará cuando cumpla **todos** los criterios siguientes:

| Criterio | Meta |
|----------|------|
| Tiempo de respuesta de búsqueda y notificación | ≤ 2 segundos |
| Tiempo de carga de pantalla | ≤ 3 segundos en condiciones óptimas |
| Disponibilidad del sistema | ≥ 99 % |
| Satisfacción de usabilidad (encuesta usuarios) | ≥ 85 % de evaluación positiva |
| Cobertura de pruebas unitarias | ≥ 80 % |
| Defectos críticos abiertos en entrega | 0 |

### 4.6 Organización del proyecto (Subcláusula 4.6)

```
Jefe de Proyecto
├── Líder de Desarrollo Frontend
│   └── Desarrollador(es) React / React Native
├── Líder de Desarrollo Backend
│   └── Desarrollador(es) Node.js / MongoDB
├── Responsable de Calidad (QA)
│   └── Analista de pruebas
└── Diseñador UX/UI
```

**Interfaces externas:** Docente asesor (revisión quincenal), municipio piloto (retroalimentación en pruebas).  
**Interfaces internas:** Reunión de equipo semanal (standup diario de 15 min).

**Autoridades y responsabilidades:**

| Rol | Responsabilidad principal |
|-----|--------------------------|
| Jefe de Proyecto | Cronograma, riesgos, comunicación con stakeholders |
| Líder Frontend | Arquitectura UI, revisión de código frontend |
| Líder Backend | Arquitectura API, revisión de código backend |
| QA | Plan de pruebas, reporte de defectos, métricas de calidad |
| UX/UI | Wireframes, pruebas de usabilidad, guía de estilos |

---

## 5. Planificación del proyecto (Cláusula 5 del PMP)

### 5.1 Iniciación del proyecto

| Actividad | Descripción | Responsable |
|-----------|-------------|-------------|
| Kick-off | Reunión inicial con equipo y stakeholders | Jefe de Proyecto |
| Configuración de repositorio | GitHub org, branches, pipelines CI/CD | Líder Backend |
| Configuración de ambientes | Dev, Staging, Producción | Líder Backend |
| Incorporación del equipo | Accesos, herramientas, onboarding | Jefe de Proyecto |

### 5.2 Plan de estimación

Método: **Puntos de función + Story Points (Planning Poker)**

**Estimación de Story Points por módulo:**

| Módulo | Story Points estimados |
|--------|----------------------|
| Autenticación y perfiles de usuario | 13 |
| Reporte de necesidad de recolección (ciudadanos) | 8 |
| Notificaciones en tiempo real (push + web) | 13 |
| Módulo de información de reciclaje | 5 |
| Gestión de rutas de recolección (administrador) | 21 |
| Estadísticas en tiempo real (administrador) | 13 |
| Panel de control y análisis histórico (autoridades) | 21 |
| API REST base + autenticación JWT | 13 |
| Integración y despliegue | 8 |
| **Total** | **115 SP** |

Velocidad estimada del equipo: **20 SP/sprint** → 6 sprints de desarrollo (3 meses) + buffer.

### 5.3 Plan de personal

| Rol | # personas | Dedicación | Meses |
|-----|-----------|------------|-------|
| Jefe de Proyecto | 1 | 25 % | 1–6 |
| Desarrollador Frontend | 1 | 100 % | 2–5 |
| Desarrollador Backend | 1 | 100 % | 2–5 |
| Desarrollador Full Stack | 1 | 100 % | 2–5 |
| Diseñador UX/UI | 1 | 50 % | 1–3 |
| QA / Analista de pruebas | 1 | 50 % | 4–5; 100 % mes 5 |

### 5.4 Plan de adquisición de recursos

| Recurso | Tipo | Cuándo | Responsable |
|---------|------|--------|-------------|
| Servidor cloud (AWS/GCP/Azure) | Infraestructura | Inicio mes 3 | Jefe de Proyecto |
| Cuenta MongoDB Atlas | Infraestructura | Inicio mes 2 | Líder Backend |
| Licencia Figma (equipo) | Herramienta | Inicio mes 1 | UX/UI |
| Dispositivos de prueba (Android/iOS) | Hardware | Inicio mes 4 | QA |

### 5.5 Plan de capacitación del equipo

| Tema | Audiencia | Cuándo |
|------|-----------|--------|
| React Native (móvil) | Desarrolladores Frontend | Mes 1 |
| MongoDB agregaciones avanzadas | Backend | Mes 1–2 |
| Pruebas con k6 (performance) | QA | Mes 4 |
| Grafana – dashboards de monitoreo | QA + Jefe Proyecto | Mes 5 |

### 5.6 Estructura de Desglose del Trabajo (WBS)

```
WasteTrack
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

| Mes | Semana | Actividad principal | Entregable |
|-----|--------|--------------------| -----------|
| **1** | 1–2 | Kick-off, levantamiento de requisitos | Acta de inicio |
| **1** | 3–4 | Análisis de sistemas, documentación SRS | E1 – Documento de requisitos |
| **2** | 5–6 | Diseño de arquitectura y base de datos | Diagrama de arquitectura |
| **2** | 7–8 | Diseño UI/UX, wireframes, validación | E2 – Prototipos validados |
| **3** | 9–10 | Config CI/CD, autenticación, módulo ciudadanos (v1) | Sprint review |
| **3** | 11–12 | Módulo ciudadanos completo + notificaciones | E3 – Release Alfa |
| **4** | 13–14 | Módulo administrador (rutas + estadísticas) | Sprint review |
| **4** | 15–16 | Módulo autoridades (panel) + integración total | E4 – Release Beta |
| **5** | 17–18 | Pruebas unitarias e integración, corrección | Reporte de defectos |
| **5** | 19–20 | Pruebas rendimiento + usabilidad, corrección final | E5 – Informe de pruebas |
| **6** | 21–22 | Despliegue en producción, piloto ciudad | Sistema en producción |
| **6** | 23–24 | Evaluación piloto, lecciones aprendidas, cierre | E6 + E7 |

### 5.8 Asignación de recursos por actividad (extracto)

| Actividad | Frontend | Backend | QA | UX | JP |
|-----------|----------|---------|----|----|-----|
| Requisitos | ✓ | ✓ | ✓ | ✓ | ✓ |
| Diseño arquitectura | ✓ | ✓ | — | ✓ | ✓ |
| Desarrollo módulos | ✓ | ✓ | — | — | — |
| Pruebas | — | — | ✓ | ✓ | — |
| Despliegue | ✓ | ✓ | ✓ | — | ✓ |

### 5.9 Asignación presupuestaria

| Fase | % del presupuesto | USD estimado |
|------|-------------------|--------------|
| Investigación y diseño | 15 % | $98 |
| Desarrollo | 30 % | $195 |
| Infraestructura (meses 3–6) | 45 % | $293 |
| Pruebas y despliegue | 10 % | $65 |
| **Total** | **100 %** | **$650** |

---

## 6. Evaluación y control del proyecto (Cláusula 6 del PMP)

### 6.1 Plan de gestión de requisitos

- Los requisitos se documentan en el SRS y se rastrean en la tabla de trazabilidad.
- Toda solicitud de cambio de requisito pasa por el proceso de control de cambios (6.2).
- Los requisitos se priorizan con técnica MoSCoW (Must/Should/Could/Won't).

### 6.2 Plan de control de cambios de alcance

1. Se registra la solicitud de cambio (Change Request – CR).  
2. El jefe de proyecto evalúa impacto en tiempo, costo y calidad.  
3. Se presenta al docente asesor si el impacto supera 1 sprint o $50 USD.  
4. Se aprueba o rechaza y se actualiza el PMP y backlog.

### 6.3 Plan de control del cronograma

- Revisión semanal del avance real vs. planificado.
- Índice de Rendimiento del Cronograma (SPI): alerta si SPI < 0.9.
- Acciones correctivas: reasignación de recursos o reducción de alcance en sprints futuros.

### 6.4 Plan de control del presupuesto

- Reporte mensual de gasto real vs. presupuestado.
- Índice de Rendimiento de Costo (CPI): alerta si CPI < 0.9.
- Reserva de contingencia: 10 % del presupuesto total ($65 USD).

### 6.5 Plan de aseguramiento de calidad

**Métricas de calidad rastreadas continuamente:**

| Métrica | Meta | Frecuencia de medición |
|---------|------|----------------------|
| Tiempo de respuesta (búsqueda / notificación) | ≤ 2 s | Cada sprint |
| Tiempo de carga de pantalla | ≤ 3 s | Cada sprint |
| Disponibilidad del sistema | ≥ 99 % | Mensual (desde mes 3) |
| Satisfacción de usabilidad | ≥ 85 % evaluación positiva | Prueba beta (mes 5) |
| Cobertura de pruebas unitarias | ≥ 80 % | Cada sprint |
| Densidad de defectos | < 5 defectos/KLOC | Cada sprint |
| Tiempo de actividad (uptime) | ≥ 99 % | Continuo (Grafana) |

**Actividades de aseguramiento:**
- Revisión de código por pares (pull request obligatorio).
- Análisis estático automático en CI/CD (ESLint).
- Ejecución automática de suite de pruebas en cada push.
- Revisión periódica de métricas de mantenibilidad del código.

### 6.6 Plan de cierre del proyecto

| Actividad de cierre | Responsable | Cuándo |
|---------------------|-------------|--------|
| Aceptación formal del sistema por cliente piloto | Jefe de Proyecto | Semana 23 |
| Documentación de lecciones aprendidas | Todo el equipo | Semana 23 |
| Versión final del PMP | Jefe de Proyecto | Semana 24 |
| Archivo de todos los artefactos del proyecto | QA | Semana 24 |
| Presentación final al docente | Todo el equipo | Semana 24 |

---

## 7. Entrega del producto (Cláusula 7 del PMP)

| Componente | Descripción | Destinatario |
|------------|-------------|-------------|
| Código fuente | Repositorio GitHub completo | Equipo + Docente |
| Aplicación web | URL de producción | Municipio piloto |
| Aplicación móvil | APK Android + TestFlight iOS | Usuarios piloto |
| Manual de usuario | Guía por tipo de actor | Ciudadanos / Admins / Autoridades |
| Manual de despliegue | Instrucciones técnicas de instalación | Equipo técnico municipio |
| Informe final de calidad | Métricas, resultados de pruebas, cobertura | Docente |

---

## 8. Planes de procesos de soporte (Cláusula 8 del PMP)

### 8.1 Gestión de decisiones

Las decisiones técnicas o de gestión con impacto mayor se documentan con el formato:  
**[Decisión] – [Alternativas consideradas] – [Criterio de selección] – [Fecha] – [Responsable]**

Decisiones significativas se revisan en la reunión semanal de equipo y se archivan en el repositorio del proyecto.

### 8.2 Gestión de riesgos

**Proceso:** Identificar → Analizar → Planificar respuesta → Monitorear

**Registro de riesgos:**

| ID | Riesgo | Prob. | Impacto | Severidad | Estrategia | Responsable |
|----|--------|-------|---------|-----------|------------|-------------|
| R01 | Rotación o baja disponibilidad de un miembro del equipo | Media | Alto | Alto | Mitigar: documentación continua; backup de conocimiento | Jefe Proyecto |
| R02 | Requisitos ambiguos o cambiantes por parte del municipio piloto | Alta | Alto | Alto | Mitigar: sesiones de validación frecuentes; CR formal | Jefe Proyecto |
| R03 | Fallas en infraestructura cloud | Baja | Alto | Medio | Contingencia: plan de recuperación, backups diarios | Líder Backend |
| R04 | Rendimiento insuficiente (tiempos de respuesta > 3 s) | Media | Medio | Medio | Mitigar: pruebas de carga con k6 desde mes 4 | QA |
| R05 | Baja adopción por ciudadanos en el piloto | Media | Medio | Medio | Mitigar: campaña de comunicación y onboarding simple | UX/UI |
| R06 | Deuda técnica acumulada que retrasa entregas | Media | Alto | Alto | Mitigar: revisiones de código en cada sprint, refactoring planificado | Líderes técnicos |
| R07 | Incumplimiento del plazo de 6 meses | Baja | Alto | Alto | Contingencia: reducir alcance de módulo autoridades a MVP | Jefe Proyecto |

### 8.3 Gestión de configuración

- **Repositorio:** GitHub (rama `main` protegida; PRs requeridos).  
- **Estrategia de ramas:** GitFlow (`main`, `develop`, `feature/*`, `hotfix/*`).  
- **Versionado:** Semántico (MAJOR.MINOR.PATCH).  
- **Baseline:** Se establece baseline al cierre de cada fase.  
- **Control de cambios:** Todo cambio a baseline requiere PR aprobado por ≥ 1 revisor.  
- **CCB (Change Control Board):** Jefe de Proyecto + Líder técnico afectado.

### 8.4 Gestión de la información

| Tipo de información | Repositorio | Acceso | Frecuencia de actualización |
|--------------------|-------------|--------|----------------------------|
| Código fuente | GitHub | Equipo | Continuo |
| Documentación técnica | GitHub /docs | Equipo | Por sprint |
| Backlog y tareas | GitHub Projects | Equipo | Semanal |
| Reportes de calidad | Carpeta compartida | Equipo + Docente | Por sprint |
| Comunicaciones formales | Email institucional | Equipo + Docente | Según necesidad |
| Actas de reunión | Notion / carpeta compartida | Equipo | Después de cada reunión |

**Política de retención:** Todos los artefactos del proyecto se conservan en repositorio GitHub por mínimo 2 años después del cierre.

### 8.5 Documentación

Documentos mínimos requeridos:

| Documento | Versión mínima | Responsable |
|-----------|---------------|-------------|
| PMP (este documento) | 1.0 | Jefe de Proyecto |
| Especificación de Requisitos (SRS) | 1.0 | Todo el equipo |
| Documento de Arquitectura | 1.0 | Líderes técnicos |
| Plan de Pruebas | 1.0 | QA |
| Manual de Usuario | 1.0 | UX/UI + QA |
| Informe final de calidad | 1.0 | QA |

---

## Apéndice A – Matriz de trazabilidad de requisitos (extracto)

| ID Req | Descripción | Tipo | Módulo | Prueba asociada |
|--------|-------------|------|--------|-----------------|
| RF-01 | Creación de perfil de ciudadano | Funcional | Ciudadanos | TC-001 |
| RF-02 | Reporte de necesidad de recolección | Funcional | Ciudadanos | TC-002 |
| RF-03 | Notificaciones en tiempo real | Funcional | Ciudadanos | TC-003 |
| RF-04 | Gestión de rutas de recolección | Funcional | Administrador | TC-010 |
| RF-05 | Estadísticas en tiempo real | Funcional | Administrador | TC-011 |
| RF-06 | Panel de análisis histórico | Funcional | Autoridades | TC-020 |
| RNF-01 | Tiempo de carga ≤ 3 s | No funcional (rendimiento) | Transversal | TC-P-001 |
| RNF-02 | Disponibilidad ≥ 99.9 % | No funcional (disponibilidad) | Infraestructura | TC-P-002 |
| RNF-03 | Accesibilidad WCAG 2.1 AA | No funcional (usabilidad) | Transversal | TC-U-001 |
| RNF-04 | Compatibilidad Android ≥ 8.0 e iOS ≥ 13 | No funcional (compatibilidad) | Móvil | TC-C-001 |
| RCA-01 | Respuesta ≤ 2 s para búsqueda y notificación | Calidad | Transversal | TC-P-003 |
| RCA-02 | Satisfacción usabilidad ≥ 85 % | Calidad | Transversal | TC-U-002 |
| RCA-03 | Cobertura pruebas unitarias ≥ 80 % | Calidad | Transversal | Cobertura CI/CD |

---

*Documento elaborado bajo los lineamientos de ISO/IEC/IEEE 16326:2009 para el curso Calidad de Software 2025-2.*  
*Versión 1.0 — Junio 2026*
