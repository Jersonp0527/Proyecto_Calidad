# Contrato de Desarrollo de Software

## Sistema WasteTrack – Gestión de Residuos Urbanos

**Identificador:** CONT-WT-2026-001

**Tipo de contrato:** Precio fijo

**Versión:** 1.1 (corregido conforme a PMP-WT-2025-v2.0 actualizado)

**Fecha de celebración:** Medellín, Colombia, 02 de enero de 2026

**Marco normativo:** ISO/IEC/IEEE 12207:2017 — Procesos de Acuerdo (Adquisición y Suministro)

**Aviso académico:** Este documento fue elaborado exclusivamente con fines académicos para la asignatura Calidad de Software. No constituye un contrato real ni acredita una relación jurídica con ninguna entidad pública o privada. Los nombres, identificaciones, cargos, direcciones, correos, valores y demás datos contractuales incluidos son ficticios, referenciales o simulados.

## Tabla de contenidos

```text
Sección                              Título
Identificación de las partes         Datos completos de Cliente y Proveedor
Cláusula 1                           Objeto del contrato
Cláusula 2                           Alcance de los servicios
Cláusula 3                           Entregables y plazos de entrega
Cláusula 4                           Precio y condiciones de pago
Cláusula 5                           Responsabilidades del Cliente
Cláusula 6                           Responsabilidades del Proveedor
Cláusula 7                           Criterios de aceptación
Cláusula 8                           Propiedad intelectual
Cláusula 9                           Gestión de cambios
Cláusula 10                          Garantías y soporte post-entrega
Cláusula 11                          Confidencialidad
Cláusula 12                          Penalidades por incumplimiento
Cláusula 13                          Terminación anticipada del contrato
Cláusula 14                          Resolución de disputas
Cláusula 15                          Ley aplicable y jurisdicción
Cláusula 16                          Disposiciones generales
Cláusula 17                          Cierre del contrato
Firmas                               Representantes legales y testigos
```

## Identificación de las partes

El presente contrato se celebra entre:

### EL CLIENTE (Adquiriente)

```text
Campo                Dato
Nombre               Secretaría de Medio Ambiente y Desarrollo Sostenible de Medellín
NIT                  890.980.716-1
Domicilio            Carrera 52 No. 42-29, Centro Administrativo La Alpujarra, Medellín,
                     Antioquia
Representante        Dr. Carlos Andrés Mejía Restrepo – Secretario de Medio Ambiente
legal
Correo de            secretaria.medioambiente@medellin.gov.co
contacto
En adelante          “El Cliente”
```

### EL PROVEEDOR (Suministrador)

```text
Campo                Dato
Nombre               Grupo 09 – WasteTrack Development Team
Organización         Universidad Nacional de Colombia – Sede Medellín, Facultad de Minas
Domicilio            Cra. 65 No. 59A-110, Bloque M8, Medellín, Antioquia
Representante        Jerson Patiño – Jefe de Proyecto del Grupo 09
Correo de contacto   grupo09.calidad@unal.edu.co
En adelante          “El Proveedor”
```

**Preámbulo:** El Cliente ha identificado la necesidad de contar con un sistema digital de gestión de residuos urbanos que optimice las rutas de recolección, facilite la participación ciudadana y provea herramientas de análisis para las autoridades locales. El Proveedor ha presentado una propuesta técnica y económica que satisface dicha necesidad. Ambas partes, actuando de buena fe, convienen en celebrar el presente contrato de desarrollo de software.

## Cláusula 1 – Objeto del contrato

El Proveedor se compromete a diseñar, desarrollar, probar e implementar el sistema denominado “WasteTrack”, una plataforma digital compuesta por una aplicación web y una aplicación móvil multiplataforma (Android e iOS), destinada a la gestión integral de residuos urbanos en la ciudad de Medellín. El sistema deberá integrar a ciudadanos, administradores de residuos y autoridades locales, conforme a las especificaciones detalladas en el Anexo 1 – Especificaciones Técnicas y Requisitos del Sistema, adjunto e incorporado a este contrato. El presente contrato se rige bajo las disposiciones del Proceso de Adquisición y el Proceso de Suministro definidos en la norma ISO/IEC/IEEE 12207:2017, sección 6.1 y 6.2 respectivamente, que gobiernan las responsabilidades y obligaciones de cada parte durante todo el ciclo de vida del acuerdo.

## Cláusula 2 – Alcance de los servicios

El Proveedor realizará las siguientes actividades y entregará los siguientes módulos funcionales:

### 2.1 Actividades incluidas en el contrato

```text
Fase                 Actividades
Análisis y           Levantamiento de requisitos funcionales y no funcionales; revisión con
requisitos           el Cliente; documento de especificación de requisitos
Diseño               Arquitectura del sistema; diseño de base de datos; wireframes y
                     mockups de interfaz de usuario validados
Desarrollo           Programación del backend (Node.js + Express), frontend web (React
                     18+) y aplicación móvil (React Native); integración con servicios
                     externos (OAuth 2.0, AWS S3, FCM)
Pruebas              Pruebas unitarias (cobertura ≥ 80 %), pruebas de integración, pruebas
                     de rendimiento y pruebas de usabilidad con usuarios reales
Implementación       Despliegue del sistema en infraestructura cloud; configuración de
                     CI/CD; puesta en marcha en ciudad piloto
Capacitación         Sesión de capacitación de 4 horas a administradores y autoridades
                     locales
Soporte post-        Soporte técnico gratuito por 3 meses posteriores a la entrega final
entrega
```

### 2.2 Módulos funcionales contratados

```text
                            Story
Módulo                      Points      Descripción
Autenticación y perfiles de 13 SP       Registro, inicio de sesión OAuth 2.0, gestión de
usuario                                 perfiles
Reporte de necesidad de     8 SP        Reporte ciudadano con foto y geolocalización
recolección
Notificaciones en tiempo    13 SP       Push notifications (FCM) y notificaciones web
real
Módulo de información de 5 SP           Contenido educativo sobre separación y reciclaje
reciclaje
```

```text
                              Story
Módulo                        Points     Descripción
Gestión de rutas de           21 SP      CRUD de rutas, validación de conflictos,
recolección                              optimización
Estadísticas en tiempo        13 SP      Dashboard operacional para administradores
real
Panel de análisis histórico   21 SP      Panel analítico avanzado para autoridades locales
API REST base +               13 SP      Infraestructura de backend y seguridad
autenticación JWT
Integración, despliegue y     8 SP       Configuración, integración técnica, despliegue y
estabilización                           estabilización del producto
Total                         115 SP     Equivalente a la línea base aprobada del proyecto y
                                         a 169 Puntos de Función Ajustados
```

### 2.3 Actividades excluidas del alcance

- Gestión de residuos industriales o rurales.

- Integración con sistemas de terceros distintos a los mencionados en el Anexo 1.

- Desarrollo de funcionalidades no especificadas en el presente contrato sin adenda autorizada.

- Suministro de hardware o dispositivos de usuario final.

## Cláusula 3 – Entregables y plazos de entrega

El Proveedor entregará los siguientes productos conforme al calendario establecido:

```text
                                                           Fecha
ID Entregable             Descripción                      límite       Criterio de entrega
E1 Documento de           Requisitos funcionales, no       31 de        Aprobación escrita
   requisitos             funcionales y de calidad         enero de     del Cliente
                          completos y aprobados            2026
E2 Prototipos UI/UX       Wireframes y mockups             28 de        Aprobación escrita
                          validados con al menos 5         febrero de   del Cliente
                          usuarios representativos         2026
E3 Release Alfa           Backend funcional + módulo       31 de        Supera suite de
                          ciudadanos desplegado en         marzo de     pruebas de
                          ambiente staging                 2026         integración
E4 Release Beta           Sistema completo con todos los   30 de        Supera pruebas
                          módulos en ambiente staging      abril de     funcionales y de
                                                           2026         usabilidad
E5 Informe de             Resultados de pruebas            31 de        Entregado en
   pruebas                unitarias, integración,          mayo de      formato .pdf o .md
                          rendimiento y usuario            2026
```

```text
                                                            Fecha
ID Entregable             Descripción                       límite        Criterio de entrega
E6 Sistema                Aplicación en producción en       30 de         Supera todos los
   desplegado             ciudad piloto, con datos reales   junio de      criterios de
                                                            2026          aceptación
                                                                          (Cláusula 7)
E7 Documentación          Manual de usuario, manual de      30 de         Entregado junto
   técnica final          administrador, documento de       junio de      con E6
                          arquitectura y PMP actualizado    2026
```

El Proveedor notificará al Cliente con al menos 5 días hábiles de anticipación ante la eventualidad de un retraso justificado. Los retrasos no notificados activarán las penalidades establecidas en la Cláusula 12.

## Cláusula 4 – Precio y condiciones de pago

### 4.1 Valor total del contrato

El valor total acordado por la prestación de los servicios descritos en este contrato es de **COP $94.420.038** (noventa y cuatro millones cuatrocientos veinte mil treinta y ocho pesos colombianos), conforme al esfuerzo estimado de **2.061 horas** a una tarifa efectiva de **$40.300 COP/hora** (tarifa base más overhead de coordinación y gestión de proyecto).

**Base salarial de referencia:** Salario promedio de Ingeniero de Software Sénior en Colombia: **$5.032.812 COP/mes** (Fuente: Computrabajo Colombia – Salarios de Informática y Telecomunicaciones, promedio de 220 muestras, 2025). Tarifa horaria base derivada: $5.032.812 ÷ 160 h/mes = $31.455 COP/h; tarifa efectiva incluyendo overhead de gestión: **$40.300 COP/h**.

**Nota de cálculo del esfuerzo:** La estimación fue derivada mediante dos métodos complementarios conforme a ISO/IEC/IEEE 16326:2009, §5.1.1:

- **FPA – Análisis de Puntos de Función** (método abstracto/funcional): 169 FP ajustados × 12 h/FP = **2.028 h**
- **Planning Poker** (método técnico basado en equipo de n = 5 técnicos): 115 SP × 13 h/SP × 1,40 overhead = **2.093 h**
- **Promedio consolidado:** **(2.028 + 2.093) / 2 = 2.061 h** (diferencia < 4 %, alta convergencia)

**Composición del valor total del contrato:**

```text
Componente                                                      Valor (COP)
Recursos humanos (5 técnicos + Jefe de Proyecto, 2.061 h)      $ 83.041.398
Infraestructura cloud (servidor, BD, CI/CD – 4 meses)          $  2.580.000
Herramientas y pruebas con usuarios (piloto)                   $    215.000
Reserva de contingencia (10 %)                                  $  8.583.640
Valor total del contrato                                        $ 94.420.038
```

El presupuesto de infraestructura, pruebas y la reserva de contingencia están incluidos en el valor total y son gestionados por el Proveedor. La reserva de contingencia no utilizada al cierre del proyecto será devuelta al Cliente conforme al Acta de Cierre (Cláusula 17).

### 4.2 Calendario de pagos

```text
Hito                  Condición de pago                                    Sprint(s) ref.  %    Valor (COP)
Pago inicial          A la firma del contrato                              —               20 % $ 18.884.008
Pago fase diseño      Entrega y aprobación de E1 (SRS) y E2               S01–S04         20 % $ 18.884.008
                      (Prototipos UI/UX validados)
Pago fase desarrollo  Entrega y aprobación de E3 (Release Alfa –           S05–S06         25 % $ 23.605.010
                      módulo ciudadanos + notificaciones)
Pago fase beta        Entrega y aprobación de E4 (Release Beta –           S07–S08         20 % $ 18.884.008
                      sistema completo integrado)
Pago final            Entrega y aprobación de E5 (Informe de pruebas),     S09–S12         15 % $ 14.163.004
                      E6 (Sistema en producción) y E7 (Documentación
                      técnica final), cumpliendo todos los criterios
                      de aceptación de la Cláusula 7
Total                                                                                      100% $ 94.420.038
```

### 4.3 Condiciones de pago

- Los pagos se realizarán mediante transferencia bancaria a la cuenta del Proveedor, dentro de los 15 días hábiles siguientes a la recepción de la factura y del acta de aceptación del entregable correspondiente.

- Cada factura deberá estar respaldada por el acta de aceptación firmada por el representante del Cliente.

- El Cliente no podrá retener pagos por razones ajenas al cumplimiento de los criterios de aceptación establecidos.

- En caso de mora en el pago, se aplicará una tasa de interés del 0,5 % mensual sobre el valor adeudado.

## Cláusula 5 – Responsabilidades del Cliente

El Cliente se compromete a:

1.   Suministrar información: Proveer al Proveedor los datos geográficos de rutas

actuales de recolección, la información organizacional y los contactos de los usuarios clave (administradores y autoridades) en un plazo máximo de 10 días hábiles a partir de la firma del contrato.

2.   Designar representante: Nombrar un representante técnico con autoridad para

aprobar entregables, revisar prototipos y validar requisitos. El representante designado es: [Nombre del representante técnico del Cliente].

3.   Participar en validaciones: Asistir a las sesiones de revisión de prototipos,

demostraciones de release y pruebas de usabilidad, en las fechas acordadas con el Proveedor.

4.   Responder en tiempo: Emitir aprobaciones o rechazos de entregables en un plazo

máximo de 5 días hábiles tras la recepción formal del entregable.

5.   Proveer entorno de pruebas: Facilitar acceso a usuarios reales de prueba para las

pruebas de usabilidad de los releases Alfa y Beta.

6.   Pagar conforme a calendario: Cumplir el calendario de pagos de la Cláusula 4, sin

demoras injustificadas.

7.   Gestionar cambios formalmente: Solicitar cambios de alcance exclusivamente a

través del procedimiento de Gestión de Cambios descrito en la Cláusula 9.

8.   No divulgar información del Proveedor: Mantener confidencialidad sobre los

métodos, herramientas y procesos de desarrollo del Proveedor durante y después del contrato.

## Cláusula 6 – Responsabilidades del Proveedor

El Proveedor se compromete a:

1.  Ejecutar conforme al plan: Desarrollar el sistema WasteTrack según el Plan de

Gestión de Proyecto (PMP-WT-2025-v2.0) y las especificaciones del Anexo 1.

2. Cumplir los plazos: Entregar cada hito en las fechas establecidas en la Cláusula 3,

notificando con anticipación cualquier desviación justificada.

3. Mantener calidad: Asegurar que el sistema cumpla los criterios de aceptación

definidos en la Cláusula 7 antes de cada entrega formal.

4. Reportar avances: Presentar informes de progreso quincenales al representante

técnico del Cliente, incluyendo métricas de velocidad del equipo, porcentaje de avance por módulo y estado de riesgos.

5. Gestionar defectos: Registrar, priorizar y corregir los defectos identificados

durante las pruebas. Los defectos críticos (impiden funcionalidad principal) deben corregirse en un plazo máximo de 5 días hábiles tras su reporte.

6. Aplicar control de calidad interno: Ejecutar revisiones de código (Pull Requests

con mínimo 1 aprobador), análisis estático (ESLint + Prettier), y pruebas automatizadas antes de cada entrega.

7. Documentar el sistema: Entregar documentación técnica completa (arquitectura,

API, manuales de usuario y administrador) como parte de los entregables E5, E6 y E7.

8. Capacitar al Cliente: Realizar una sesión de capacitación de 4 horas dirigida a los

administradores y autoridades locales designados por el Cliente.

9. Dar soporte post-entrega: Prestar soporte técnico gratuito durante 3 meses

después de la entrega final (E6), conforme a la Cláusula 10.

10. Proteger la confidencialidad: Mantener reserva sobre toda la información del

Cliente a la que tenga acceso durante la ejecución del contrato.

## Cláusula 7 – Criterios de aceptación

El sistema WasteTrack será formalmente aceptado cuando cumpla todos los criterios siguientes:

### 7.1 Criterios funcionales

```text
Criterio                                        Condición de cumplimiento
Todos los módulos funcionales contratados       Verificado mediante ejecución de los
deben estar operativos                          casos de prueba de aceptación definidos
                                                en el Anexo 2
```

```text
Criterio                                            Condición de cumplimiento
Los tres tipos de usuario (ciudadano,               0 defectos críticos abiertos en el
administrador, autoridad) deben poder realizar      momento de la entrega
sus flujos principales sin errores
Las reglas de negocio de gestión de rutas deben     Verificado mediante ejecución de casos
cumplirse sin excepción                             de prueba BN-PE, BN-VL, BN-TD del
                                                    módulo Gestión de Rutas
```

### 7.2 Criterios de calidad técnica (ISO/IEC 25010:2011)

Los criterios se organizan conforme a las 8 características de calidad de ISO/IEC 25010. El instrumento de medición de referencia es el Plan de Aseguramiento de Calidad del PMP-WT-2025-v2.0, Sección 6.5 (Anexo 4 de este contrato).

```text
Característica ISO 25010   Criterio de aceptación                              Meta
Adecuación funcional       Requisitos funcionales cubiertos por release         ≥ 95 %
                           Defectos críticos abiertos en entrega final           0
                           Defectos mayores abiertos en entrega final            ≤ 3 (con plan de
                                                                                corrección acordado)
Eficiencia de rendimiento  Tiempo de respuesta API y notificaciones              ≤ 2 s
                           Tiempo de carga de pantalla principal                 ≤ 3 s en condiciones
                                                                                estándar
                           Throughput API bajo carga                             ≥ 100 req/s
Compatibilidad             Pruebas en Android ≥ 8.0, iOS ≥ 13, navegadores web 100 % pass en matriz
                                                                                de dispositivos
Usabilidad                 Satisfacción de usuarios (encuesta post-prueba)       ≥ 85 % positivo
                           Tasa de éxito en tarea principal (crear reporte)      ≥ 90 %
Fiabilidad                 Disponibilidad en producción (30 días post-entrega)   ≥ 99 %
                           MTBF (tiempo medio entre fallos)                      ≥ 720 h
                           MTTR (tiempo medio de recuperación)                   ≤ 4 h
Seguridad                  Vulnerabilidades críticas OWASP Top 10                0
                           Cobertura de análisis estático SAST (ESLint/CI)       100 %
Mantenibilidad             Cobertura de pruebas unitarias (Jest/Istanbul)         ≥ 80 %
                           Complejidad ciclomática por función                   ≤ 10
Portabilidad               Tiempo de despliegue automatizado (pipeline CI/CD)    ≤ 30 min
```

### 7.3 Criterios de usabilidad

```text
Criterio                                                Meta
Satisfacción de usuarios en encuesta post-prueba        ≥ 85 % de evaluación positiva
Tiempo promedio para completar tarea principal          ≤ 3 minutos para usuario sin
(crear reporte)                                         entrenamiento
```

### 7.4 Trazabilidad de criterios de aceptación con casos de prueba

Los criterios de aceptación funcional (§7.1) están respaldados por el Plan de Pruebas de Aceptación contenido en el Anexo 2, el cual incluye 34 casos de prueba formalmente documentados para el módulo más complejo del sistema (Gestión de Rutas de Recolección, RF-04). La siguiente tabla muestra la correspondencia entre criterios contractuales, requisitos y pruebas:

```text
Criterio contractual                  Requisito       Casos de prueba asociados
Módulos funcionales operativos sin    RF-01 a RF-     BN-PE-01 (caso nominal), CB-CS-01,
defectos críticos                     06              CB-CD-06
Reglas de negocio de validación de    RN-01           BN-PE-02, BN-PE-03, BN-VL-01 a BN-
nombre                                                VL-04, CB-CC-01, CB-CC-02
Reglas de negocio de validación de    RN-02           BN-PE-04, BN-PE-05, BN-VL-05 a BN-
```

```text
Criterio contractual                   Requisito      Casos de prueba asociados
capacidad                                             VL-08, CB-CC-03, CB-CC-04
Reglas de negocio de validación de     RN-03          BN-PE-06, CB-CC-05
horario
Reglas de negocio de días de           RN-04          BN-PE-07, CB-CD-04
operación
Control de solapamiento de rutas       RN-05          BN-TD-01 a BN-TD-04, CB-CS-03, CB-
                                                      CD-05
Notificaciones push al                 RN-06          BN-PE-01, CB-CS-01, CB-CD-06
crear/modificar ruta
```

Esta trazabilidad garantiza que los criterios de aceptación del contrato sean verificables mediante pruebas objetivas, conforme a las buenas prácticas del Proceso de Suministro de ISO/IEC/IEEE 12207:2017 (§6.2.5 — verificación y aceptación).

### 7.5 Proceso de aceptación

1. El Proveedor entrega el artefacto y notifica formalmente al Cliente.

2. El Cliente dispone de 5 días hábiles para realizar la revisión.

3. Si el artefacto cumple todos los criterios aplicables, el Cliente firma el Acta de

Aceptación.

4. Si no cumple, el Cliente emite un Informe de Rechazos con los defectos específicos.

5. El Proveedor corrige y reenvía en un plazo máximo de 7 días hábiles.

6. Se repite el ciclo hasta la aceptación o hasta activarse las cláusulas de

incumplimiento.

## Cláusula 8 – Propiedad intelectual

1.   El Cliente será el propietario exclusivo de todos los derechos de propiedad

intelectual sobre el sistema WasteTrack desarrollado bajo este contrato, incluidos derechos de autor, código fuente, bases de datos, documentación técnica, diseños de interfaz y cualquier otro producto derivado.

2.   La transferencia de los derechos al Cliente se perfeccionará con la firma del Acta de

Aceptación Final (E6) y el recibo del pago final.

3.   El Proveedor conserva el derecho de mencionar el proyecto WasteTrack en su

portafolio académico y publicaciones científicas, previa autorización escrita del Cliente.

4.   Los componentes de código abierto (librerías open source) utilizados en el

desarrollo se rigen por sus respectivas licencias (MIT, Apache 2.0, etc.), las cuales el Proveedor declara en el Anexo 3 – Inventario de Dependencias de Terceros.

5.   Queda expresamente prohibido al Proveedor utilizar el código fuente del sistema

WasteTrack para otros proyectos o clientes sin autorización expresa del Cliente.

## Cláusula 9 – Gestión de cambios

Todo cambio al alcance, cronograma, presupuesto o requisitos del sistema deberá tramitarse mediante el siguiente procedimiento formal, alineado con el Proceso de Suministro de ISO/IEC/IEEE 12207:2017:

### 9.1 Procedimiento de solicitud de cambio

### Paso Actividad                                  Responsable         Plazo

```text
1      Emisión de la Solicitud de Cambio        Parte solicitante   En cualquier momento
       (SC) documentada con descripción,        (Cliente o
       justificación e impacto esperado         Proveedor)
2      Análisis de impacto en alcance, costo,   Proveedor           5 días hábiles
       cronograma y riesgos
3      Presentación del análisis al Cliente     Proveedor           7 días hábiles
       con opciones de implementación
4      Aprobación o rechazo formal de la        Cliente             5 días hábiles
       Solicitud de Cambio
5      Emisión de Adenda al Contrato si el      Ambas partes        Antes de iniciar la
       cambio implica modificación de                               implementación
       precio o plazo
6      Implementación y seguimiento del         Proveedor           Conforme al plan de
       cambio aprobado                                              implementación
                                                                    acordado
```

### 9.2 Principios de gestión de cambios

- Ningún cambio se implementará sin aprobación escrita del Cliente.

- Los cambios de alcance significativos (que incrementen el esfuerzo en más del 10 %) requerirán adenda contractual.

- El Proveedor no está obligado a implementar cambios de alcance sin la compensación económica correspondiente.

- El registro de todas las solicitudes de cambio (aprobadas o rechazadas) se mantendrá en el Registro de Control de Cambios, disponible para auditoría por ambas partes.

## Cláusula 10 – Garantías y soporte post-entrega

### 10.1 Período de garantía

El Proveedor garantiza que el sistema WasteTrack estará libre de defectos que impidan su correcto funcionamiento conforme a las especificaciones, durante un período de 6 meses contados a partir de la firma del Acta de Aceptación Final (E6).

### 10.2 Cobertura de la garantía

Durante el período de garantía, el Proveedor se compromete a:

- Corregir sin costo adicional todos los defectos que impidan el funcionamiento de las funcionalidades contratadas.

- Atender reportes de defectos en los plazos definidos según su severidad: Tiempo de Tiempo de

```text
Severidad Descripción                                     respuesta         resolución
Crítico      Impide funcionalidad principal del           4 horas hábiles   48 horas hábiles
             sistema
Mayor        Afecta significativamente funcionalidad      8 horas hábiles   5 días hábiles
             sin workaround
Menor        Problema estético o de usabilidad menor 24 horas hábiles 15 días hábiles
```

### 10.3 Exclusiones de garantía

La garantía no cubre:

- Defectos causados por modificaciones no autorizadas al código fuente realizadas por el Cliente.

- Problemas derivados de fallas en la infraestructura de terceros (AWS, OAuth providers, FCM).

- Cambios de funcionalidad solicitados después de la aceptación final (requieren nuevo contrato o adenda).

### 10.4 Soporte técnico

Los primeros 3 meses posteriores a la entrega final, el Proveedor prestará soporte técnico sin costo adicional, incluyendo:

- Atención de consultas técnicas de administradores del sistema.

- Asistencia en la configuración de nuevos usuarios.

- Monitoreo conjunto del sistema en producción durante el primer mes.

A partir del cuarto mes, el Cliente podrá contratar un plan de soporte extendido mediante adenda separada.

## Cláusula 11 – Confidencialidad

1.   Ambas partes se comprometen a tratar como información confidencial toda la

información técnica, comercial, estratégica u organizacional a la que accedan con ocasión de este contrato.

2.   La información confidencial incluye, de manera enunciativa y no taxativa: código

fuente, arquitectura del sistema, datos de usuarios, procesos internos del Cliente, datos de rutas de recolección, información financiera y cualquier dato personal al que se acceda.

3.   Las partes no podrán divulgar información confidencial a terceros sin autorización

escrita de la parte afectada.

4.   Esta obligación de confidencialidad persistirá por 5 años después de la

terminación del contrato.

5.   Se exceptúan de la confidencialidad: información de dominio público, información

requerida por autoridad judicial o administrativa competente, e información que la parte receptora ya poseía antes de este contrato.

6.   El Proveedor implementará medidas técnicas de protección de datos conforme a la

Ley 1581 de 2012 (Colombia) y sus decretos reglamentarios, para proteger los datos personales de los ciudadanos que se procesen a través del sistema.

## Cláusula 11A – Protección y tratamiento de datos personales

Las partes se comprometen a tratar los datos personales recolectados, almacenados o procesados por WasteTrack únicamente para las finalidades autorizadas dentro del proyecto. El Proveedor deberá:

1.   Implementar controles de acceso basados en roles.

2.   Aplicar cifrado a las comunicaciones y a la información sensible.

3.   Evitar el uso de datos personales para finalidades distintas de las autorizadas.

4.   Informar al Cliente sobre incidentes de seguridad que comprometan información.

5.   Eliminar o devolver los datos al finalizar el contrato, de acuerdo con las

instrucciones del Cliente.

6.   Garantizar que el personal y los posibles subcontratistas mantengan la

confidencialidad de la información. El Cliente será responsable de definir las finalidades autorizadas del tratamiento y de proporcionar los avisos y autorizaciones correspondientes.

## Cláusula 12 – Penalidades por incumplimiento

### 12.1 Penalidades por retraso del Proveedor

Si el Proveedor no cumple con las fechas de entrega establecidas en la Cláusula 3 sin causa justificada, el Cliente tendrá derecho a imponer:

```text
Duración del retraso            Penalidad
1 a 5 días hábiles              0,5 % del valor del hito retrasado
6 a 15 días hábiles             1,0 % del valor del hito retrasado por cada semana
```

```text
Duración del retraso             Penalidad
                                 adicional
Más de 30 días hábiles           El Cliente podrá dar por terminado el contrato conforme a
acumulados                       la Cláusula 13
```

El tope máximo de penalidades acumuladas no podrá exceder el 10 % del valor total del contrato.

### 12.2 Incumplimiento de criterios de aceptación

Si el sistema no cumple los criterios de aceptación de la Cláusula 7 tras 3 ciclos de revisión y corrección para un mismo entregable, el Cliente podrá:

- Solicitar reducción del precio acordado para ese entregable, proporcional a los criterios no cumplidos.

- Contratar a un tercero para completar la funcionalidad faltante, con cargo al Proveedor.

### 12.3 Penalidades por mora en el pago del Cliente

Si el Cliente incurre en mora en el pago de cualquier factura, se aplicará una tasa de interés del 0,5 % mensual sobre el saldo adeudado, conforme a lo establecido en la Cláusula 4.3.

## Cláusula 13 – Terminación anticipada del contrato

### 13.1 Terminación por incumplimiento del Proveedor

El Cliente podrá dar por terminado el contrato anticipadamente si:

- El Proveedor acumula más de 30 días hábiles de retraso en un mismo entregable sin causa justificada.

- El Proveedor incumple obligaciones esenciales (confidencialidad, propiedad intelectual) de forma grave e irreparable.

- El Proveedor entra en proceso de liquidación o se declara insolvente.

En este caso, el Cliente pagará únicamente el valor de los servicios efectivamente prestados y aceptados hasta la fecha de terminación.

### 13.2 Terminación por conveniencia del Cliente

El Cliente podrá terminar el contrato por razones de conveniencia, notificando al Proveedor con al menos 15 días hábiles de antelación. En este caso, el Cliente pagará:

- El valor de todos los entregables aceptados hasta la fecha.

- Una compensación equivalente al 10 % del valor de los entregables no iniciados, como reconocimiento de los costos de preparación del Proveedor.

### 13.3 Terminación por mutuo acuerdo

Las partes podrán acordar la terminación anticipada del contrato mediante documento escrito firmado por ambas, definiendo conjuntamente las condiciones económicas y las obligaciones pendientes.

## Cláusula 14 – Resolución de disputas

1.   Cualquier controversia derivada de este contrato será resuelta inicialmente

mediante negociación directa entre los representantes de las partes, en un plazo máximo de 15 días hábiles tras la manifestación del desacuerdo.

2.   Si la negociación directa no produce acuerdo, las partes acudirán a un proceso de

mediación ante el Centro de Conciliación, Arbitraje y Amigable Composición de la Cámara de Comercio de Medellín.

3.   Si la mediación fracasa, las disputas serán resueltas mediante arbitraje conforme a

las reglas de la Cámara de Comercio de Medellín, con sede en Medellín, Colombia.

4.   Durante el proceso de resolución de disputas, ambas partes continuarán

cumpliendo sus obligaciones contractuales en la medida de lo posible.

## Cláusula 15 – Ley aplicable y jurisdicción

Este contrato se regirá e interpretará de acuerdo con las leyes de la República de Colombia, incluyendo el Código Civil, el Código de Comercio y la normativa vigente en materia de protección de datos personales (Ley 1581 de 2012) y derechos de autor (Ley 23 de 1982 y sus modificaciones). Para todos los efectos, las partes se someten a la jurisdicción de los jueces y tribunales de la ciudad de Medellín, Antioquia.

## Cláusula 16 – Disposiciones generales

### 16.1 Modificaciones al contrato

Cualquier modificación al presente contrato deberá constar por escrito, estar firmada por los representantes autorizados de ambas partes y ser incorporada como adenda numerada. Las modificaciones verbales o por correo electrónico no producirán efectos jurídicos.

### 16.2 Independencia de cláusulas

Si alguna de las cláusulas de este contrato es declarada nula o inaplicable por autoridad competente, las demás cláusulas continuarán vigentes y producirán sus efectos jurídicos plenos.

### 16.3 Documentos que integran el contrato

Los siguientes documentos forman parte integral de este contrato:

### Anexo     Documento

### Anexo 1   Especificaciones Técnicas y Requisitos del Sistema WasteTrack

### Anexo 2   Plan de Pruebas de Aceptación (Casos de Prueba – Módulo Gestión de Rutas)

### Anexo 3   Inventario de Dependencias de Terceros y sus licencias

### Anexo 4   Plan de Gestión de Proyecto (PMP-WT-2025-v2.0)

En caso de conflicto entre el cuerpo del contrato y sus anexos, prevalece el cuerpo del contrato.

### 16.4 Relación con la norma ISO/IEC/IEEE 12207:2017

El presente contrato formaliza la relación entre el Proceso de Adquisición (ejecutado por El Cliente) y el Proceso de Suministro (ejecutado por El Proveedor) conforme a la norma ISO/IEC/IEEE 12207:2017. Ambas partes reconocen que sus responsabilidades, el ciclo de entrega, los criterios de aceptación y el cierre del contrato son coherentes con las actividades y resultados esperados por dicha norma.

### 16.5 Comunicaciones formales

Todas las comunicaciones formales (aprobaciones, rechazos, solicitudes de cambio, notificaciones de incumplimiento) deberán realizarse por escrito dirigidas a:

- Para el Cliente: secretaria.medioambiente@medellin.gov.co — Dr. Carlos Andrés Mejía Restrepo

- Para el Proveedor: grupo09.calidad@unal.edu.co — Jefe de Proyecto Grupo 09

## Cláusula 17 – Cierre del contrato

El contrato se considerará formalmente cerrado cuando:

1.   El Cliente haya firmado el Acta de Aceptación Final del sistema WasteTrack en

producción (E6 + E7).

2.   El Proveedor haya transferido al Cliente todos los artefactos contratados: código

fuente completo en repositorio, documentación técnica, credenciales de acceso a infraestructura y acta de transferencia de conocimiento.

3.   El Cliente haya realizado el pago final conforme a la Cláusula 4.

4.   Ambas partes hayan firmado el Acta de Cierre de Contrato, documento que da por

concluidas todas las obligaciones principales del presente acuerdo.

5.   El Proveedor haya entregado el informe de lecciones aprendidas, conforme a las

buenas prácticas del Proceso de Suministro de ISO/IEC/IEEE 12207:2017.

## Firmas

En constancia de haber leído, comprendido y aceptado todas las cláusulas del presente contrato, las partes firman en la ciudad de Medellín, Colombia, el día 02 de enero de 2026.

## POR EL CLIENTE

```text
Campo           Dato
Nombre y        Dr. Carlos Andrés Mejía Restrepo – Secretario de Medio Ambiente y
cargo           Desarrollo Sostenible de Medellín
Firma           _____________________________
Fecha           _____________________________
Huella          _____________________________
```

## POR EL PROVEEDOR

```text
Campo           Dato
Nombre y        Jefe de Proyecto – Grupo 09, WasteTrack Development Team, Universidad
cargo           Nacional de Colombia
Firma           _____________________________
Fecha           _____________________________
Huella          _____________________________
```

Testigos

```text
Testigo 1                                     Testigo 2
Nombre: ________________________              Nombre: ________________________
Documento: ________________________           Documento: ________________________
Firma: ________________________               Firma: ________________________
```

Contrato elaborado conforme a la norma ISO/IEC/IEEE 12207:2017 – Procesos de Acuerdo, en el marco del curso Calidad de Software 2025-2, Universidad Nacional de Colombia – Sede Medellín. Identificador: CONT-WT-2026-001.
