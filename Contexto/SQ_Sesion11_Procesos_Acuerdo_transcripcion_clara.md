# SQ Sesión 11 - Procesos de Acuerdo

**Curso:** Calidad de Software  
**Código:** 3007849  
**Docente:** Albeiro Espinosa Bedoya, Ph.D. Ms.C.  
**Tema:** Gestión de Proveedores y Acuerdos  
**Facultad:** Facultad de Minas - Sede Medellín, Universidad Nacional de Colombia

---

## Propósito de esta transcripción

Este documento organiza el contenido de la sesión en formato Markdown, manteniendo la información académica del material original y agregando explicaciones sencillas para facilitar la comprensión de una persona que no conoce el tema.

> **Nota de lectura:** Las secciones marcadas como **Contenido base** corresponden a la información del archivo original. Las secciones marcadas como **Explicación sencilla** son aclaraciones pedagógicas agregadas para entender mejor los conceptos, sin reemplazar ni modificar el contenido original.

---

## Agenda

1. Procesos de Acuerdo
2. El contrato
3. Tipos de Contratos de Software
4. Ejercicios
5. Referencias

---

# 1. Procesos de Acuerdo

## 1.1. Marco conceptual de los procesos de acuerdo

### Contenido base

**Definición:** Los procesos de acuerdo son los procesos que establecen, mantienen y concluyen acuerdos formales entre dos partes: una que adquiere, es decir, el **cliente**, y otra que suministra, es decir, el **proveedor**, un producto o servicio de software.

**Procesos involucrados:**

1. **Proceso de Adquisición (Acquisition Process):** ejecutado por el cliente o adquiriente.
2. **Proceso de Suministro (Supply Process):** ejecutado por el proveedor o contratista.

### Explicación sencilla

Un proceso de acuerdo explica cómo se organiza la relación entre quien **necesita comprar o contratar** un software y quien **lo va a construir, vender, entregar o mantener**.

En términos simples:

| Parte | Rol | Qué hace |
|---|---|---|
| Cliente o adquiriente | Compra o solicita el software | Define la necesidad, pide propuestas, selecciona proveedor y acepta entregables. |
| Proveedor o contratista | Suministra el software o servicio | Presenta propuesta, desarrolla o entrega el producto, da soporte y cumple el contrato. |

---

## 1.2. Relación con otros procesos

### Contenido base

Los procesos de acuerdo interactúan con:

- Los **procesos de gestión de proyectos**, como planificación, control y aseguramiento de calidad.
- Los **procesos técnicos**, como análisis de requisitos, desarrollo, validación y entrega.

**Resultado esperado:** Un acuerdo formal y documentado, como contrato, convenio u orden de compra, que define responsabilidades, entregables, criterios de aceptación y condiciones de pago.

### Explicación sencilla

Un contrato de software no vive aislado. Está conectado con la gestión del proyecto y con las actividades técnicas. Por ejemplo, si el contrato dice que el proveedor debe entregar un módulo de inventarios, entonces el equipo técnico debe analizar requisitos, diseñar, programar, probar y entregar ese módulo.

El resultado más importante es dejar por escrito:

- qué se va a entregar;
- quién es responsable de cada parte;
- cómo se sabrá que el producto está bien hecho;
- cuándo se entrega;
- cuánto se paga;
- qué pasa si hay retrasos, errores o incumplimientos.

---

## 1.3. Proceso de Adquisición (Acquisition Process)

### Objetivo y alcance

### Contenido base

**Objetivo:** Obtener un producto, servicio o sistema que satisfaga una necesidad expresada por el cliente, mediante un acuerdo formal con un proveedor.

**Actividades principales según ISO/IEC/IEEE 12207:2017:**

1. **Preparación de la adquisición:** identificación de necesidades, elaboración de especificaciones, definición de criterios de selección y presupuesto.
2. **Solicitud y selección de proveedor:** emisión de la solicitud de oferta, conocida como **RFP**, evaluación de propuestas y selección del proveedor.
3. **Gestión del contrato:** negociación, seguimiento del desempeño, control de entregas y gestión de cambios.
4. **Finalización del contrato:** verificación de cumplimiento, aceptación del producto o servicio y cierre administrativo.

**Entradas típicas:** necesidad del cliente, requisitos de software, presupuesto y plan de adquisición.

**Salidas típicas:** contrato firmado, plan de gestión de la adquisición y actas de aceptación.

### Explicación sencilla

La adquisición es el proceso desde la mirada del **cliente**. El cliente identifica una necesidad y busca quién pueda resolverla.

Ejemplo: una empresa necesita un sistema para controlar inventarios. Primero define qué necesita, luego solicita propuestas, compara proveedores, firma un contrato y finalmente revisa si el producto entregado cumple lo acordado.

---

## 1.4. Diagrama de flujo del proceso de adquisición

### Contenido base

Flujo del proceso:

1. Identificar necesidad del sistema.
2. Preparar especificaciones y criterios de selección.
3. Emitir solicitud de oferta (**RFP**).
4. Evaluar propuestas de proveedores.
5. Decidir si hay proveedor seleccionado.
   - Si la respuesta es **sí**, negociar y firmar contrato.
   - Si la respuesta es **no**, repetir proceso de solicitud.
6. Monitorear cumplimiento y calidad.
7. Recibir y aceptar entregables.
8. Cerrar contrato.

**Interpretación:** El proceso de adquisición se orienta a asegurar que la organización cliente obtenga un producto que cumpla los requisitos establecidos, mediante un proceso transparente y controlado de contratación.

### Explicación sencilla

La adquisición no consiste solamente en comprar. Es un proceso controlado para evitar contratar a ciegas. Por eso se revisan propuestas, se comparan opciones y se hace seguimiento al cumplimiento del proveedor.

```text
Necesidad del cliente
        ↓
Especificaciones y criterios
        ↓
Solicitud de oferta - RFP
        ↓
Evaluación de proveedores
        ↓
¿Proveedor seleccionado?
   ├─ Sí → Contrato → Seguimiento → Entrega → Cierre
   └─ No → Repetir solicitud
```

---

## 1.5. Ejemplo aplicado: adquisición de un sistema de gestión hospitalaria

### Contenido base

**Escenario:** Un hospital público requiere un sistema de información clínica interoperable con el Ministerio de Salud.

**Aplicación del proceso de adquisición:**

- **Preparación:** El área de TI redacta un pliego con requisitos funcionales, módulos e interoperabilidad **HL7/FHIR**.
- **Solicitud:** Se emite una **RFP** pública a empresas especializadas en software médico.
- **Selección:** Se evalúan las ofertas considerando precio, cumplimiento normativo y experiencia previa.
- **Contrato:** Se establece un contrato de precio fijo con cláusulas de penalidad por incumplimiento.
- **Cierre:** Tras la entrega del sistema, se realiza validación funcional y acta de aceptación final.

**Relación con otros procesos:**

- **Aseguramiento de calidad:** revisión del plan **SQAP** del proveedor.
- **Gestión de proyectos:** control de hitos y entregables.

### Explicación sencilla

En este ejemplo, el hospital actúa como cliente. No solo quiere comprar un sistema, sino asegurarse de que el sistema sea compatible con estándares del sector salud, cumpla normas y funcione adecuadamente.

Términos importantes:

| Término | Significado sencillo |
|---|---|
| RFP | Solicitud formal de propuesta. El cliente le pide a varios proveedores que presenten una oferta. |
| HL7/FHIR | Estándares usados para que sistemas de salud puedan intercambiar información clínica. |
| SQAP | Plan de aseguramiento de la calidad del software. Sirve para revisar cómo el proveedor garantizará la calidad. |
| Acta de aceptación | Documento donde el cliente deja constancia de que recibe y acepta el producto. |

---

## 1.6. Proceso de Suministro (Supply Process)

### Objetivo y propósito

### Contenido base

**Objetivo:** Proveer un producto o servicio conforme a los requisitos establecidos en el acuerdo con el cliente, asegurando su calidad, cumplimiento técnico y contractual.

**Propósito en la norma:** El proceso de suministro describe las actividades que realiza el proveedor o contratista para preparar, ejecutar y entregar el producto o servicio comprometido.

**Ámbito de aplicación:**

- Desarrollo de software a la medida.
- Suministro de software comercial o **SaaS**.
- Servicios de mantenimiento o soporte técnico.

### Explicación sencilla

El suministro es el mismo acuerdo, pero visto desde el lado del **proveedor**. El proveedor debe cumplir lo prometido en el contrato: desarrollar, entregar, documentar, probar y dar soporte.

---

## 1.7. Relación del proceso de suministro con otros procesos

### Contenido base

El proceso de suministro:

- Inicia a partir de la firma del contrato de adquisición.
- Se apoya en los procesos técnicos: desarrollo, integración, verificación y validación.
- Alimenta los procesos de gestión: seguimiento, aseguramiento de calidad, entrega y cierre.

### Explicación sencilla

Cuando se firma el contrato, el proveedor comienza a trabajar formalmente. Para cumplir, necesita planificar el proyecto, analizar los requisitos, desarrollar el producto, hacer pruebas, corregir errores, entregar y cerrar el contrato.

---

## 1.8. Actividades principales del proceso de suministro

### Contenido base

De acuerdo con ISO/IEC/IEEE 12207:2017, las actividades del proceso incluyen:

1. **Iniciación del suministro:** preparar el plan del proyecto del proveedor, definir recursos, cronograma y procedimientos de control.
2. **Análisis de requisitos del cliente:** comprender y validar los requisitos del contrato, identificando posibles ambigüedades o inconsistencias.
3. **Desarrollo o provisión del producto/servicio:** implementar las actividades técnicas conforme al plan, incluyendo diseño, codificación, pruebas y documentación.
4. **Verificación y aceptación interna:** comprobar que el producto cumple con los requisitos antes de entregarlo al cliente.
5. **Entrega y soporte:** preparar la entrega formal, transferencia de conocimiento, capacitación y soporte postventa.
6. **Cierre del suministro:** documentar las lecciones aprendidas y cumplir las obligaciones contractuales finales.

**Entradas típicas:** contrato firmado, requisitos del cliente, plan de proyecto y recursos técnicos.

**Salidas típicas:** producto o servicio entregado, documentación técnica, informe de cumplimiento y acta de aceptación.

### Explicación sencilla

El proveedor no debe limitarse a programar. Debe gestionar todo el ciclo de entrega: entender lo contratado, planificar, desarrollar, probar, documentar, capacitar y cerrar correctamente.

---

## 1.9. Flujo general del proceso de suministro

### Contenido base

Flujo del proceso:

1. Recibir contrato y requisitos del cliente.
2. Preparar plan del proyecto de suministro.
3. Analizar requisitos y resolver ambigüedades.
4. Desarrollar o proveer el producto/servicio.
5. Realizar pruebas internas y control de calidad.
6. Entregar producto al cliente.
7. Verificar si cumple criterios de aceptación.
   - Si cumple, registrar aceptación y soporte postventa.
   - Si no cumple, implementar correcciones y reenviar entrega.
8. Documentar lecciones aprendidas y cerrar contrato.

**Interpretación:** El proveedor no solo entrega el producto, sino que gestiona el proyecto, asegura la calidad y mantiene la trazabilidad entre los requisitos y los entregables, cumpliendo con los compromisos contractuales y normativos.

### Explicación sencilla

El proveedor debe revisar internamente el producto antes de entregarlo. Si el cliente no lo acepta, debe corregir y volver a entregar. Esto evita que el cierre del contrato sea solo una formalidad y lo convierte en una verificación real de cumplimiento.

```text
Contrato y requisitos
        ↓
Plan del proveedor
        ↓
Análisis de requisitos
        ↓
Desarrollo / provisión
        ↓
Pruebas internas y calidad
        ↓
Entrega al cliente
        ↓
¿Cumple criterios?
   ├─ Sí → Aceptación + soporte → Cierre
   └─ No → Correcciones → Nueva entrega
```

---

## 1.10. Ejemplo aplicado: proveedor de software educativo

### Contenido base

**Escenario:** Una empresa de desarrollo, **EduSoft S.A.S.**, firma un contrato con una universidad para suministrar una plataforma de aprendizaje virtual personalizada.

**Aplicación del proceso de suministro:**

- **Inicio:** El proveedor revisa los requisitos funcionales y define su plan de desarrollo basado en entregas iterativas, también llamadas **sprints**.
- **Desarrollo:** Se implementan módulos de autenticación, cursos y evaluación continua.
- **Verificación:** Se ejecutan pruebas de integración y usabilidad, con informes entregados al cliente.
- **Entrega:** La universidad recibe la versión estable, se capacita al personal y se emite el acta de aceptación.
- **Cierre:** El proveedor archiva la documentación, actualiza su repositorio de lecciones aprendidas y prepara soporte de garantía.

**Resultados:** Contrato cumplido, software operativo, usuarios capacitados y relación de confianza fortalecida entre proveedor y cliente.

### Explicación sencilla

En este caso, EduSoft es el proveedor. Su responsabilidad no termina al entregar la plataforma. También debe probarla, capacitar a los usuarios, entregar documentación, registrar aprendizajes y preparar soporte.

---

## 1.11. Relación entre procesos de adquisición y suministro

### Contenido base

**Visión integrada:** Los procesos de adquisición y suministro son complementarios y representan las dos caras del mismo acuerdo contractual.

**Correspondencias clave:**

| Adquisición - Cliente | Suministro - Proveedor |
|---|---|
| Define requisitos y criterios de aceptación | Comprende y planifica su cumplimiento |
| Evalúa propuestas | Presenta propuesta técnica y económica |
| Negocia y firma el contrato | Acepta condiciones contractuales |
| Supervisa ejecución | Ejecuta y reporta avances |
| Acepta entregables | Entrega y soporta producto |
| Cierra el contrato | Documenta y transfiere conocimiento |

**Importancia:** La correcta sincronización entre ambos procesos reduce riesgos de incumplimiento, sobrecostos y conflictos contractuales.

### Explicación sencilla

El cliente y el proveedor deben trabajar coordinadamente. Si el cliente no define bien lo que quiere, el proveedor puede entregar algo que no era lo esperado. Si el proveedor no reporta avances o no entiende los requisitos, el proyecto puede atrasarse, costar más o terminar en conflicto.

---

## 1.12. Interacción bidireccional entre cliente y proveedor

### Contenido base

El diagrama de relación entre adquisición y suministro muestra estos momentos:

1. **Inicio del acuerdo**
   - Solicitud de propuesta (**RFP**).
   - Propuesta técnica y económica.
   - Firma del contrato.
2. **Planificación y ejecución**
   - Plan del proyecto y cronograma.
   - Entregables parciales.
   - Retroalimentación o aceptación intermedia.
3. **Cierre del contrato**
   - Entrega final y documentación.
   - Aprobación y cierre del contrato.

**Interpretación:** Este diagrama muestra la interacción bidireccional entre las partes a lo largo del ciclo contractual. Ambos procesos, adquisición y suministro, se ejecutan en paralelo, garantizando transparencia, cumplimiento técnico y trazabilidad documental.

### Explicación sencilla

El acuerdo no es una secuencia donde primero actúa uno y luego el otro. En realidad, cliente y proveedor interactúan durante todo el proyecto: uno solicita, el otro propone; uno revisa, el otro entrega; uno acepta, el otro documenta y soporta.

---

## 1.13. Síntesis comparativa de los procesos de acuerdo

### Contenido base

**Resumen general según ISO/IEC/IEEE 12207:2017:**

| Proceso de Adquisición | Proceso de Suministro |
|---|---|
| Identifica la necesidad de un producto o servicio. | Atiende la necesidad formulada por el cliente. |
| Prepara la RFP y evalúa ofertas. | Elabora propuesta técnica y económica. |
| Negocia y firma el contrato. | Planifica la ejecución del contrato. |
| Supervisa cumplimiento contractual. | Ejecuta, controla y reporta avances. |
| Acepta los entregables. | Entrega, documenta y soporta el producto. |
| Finaliza el acuerdo y archiva lecciones. | Cierra contrato y transfiere conocimiento. |

**Punto clave:** Ambos procesos deben ser coherentes y sincronizados; los entregables de uno constituyen las entradas del otro.

### Explicación sencilla

Lo que hace el cliente genera trabajo para el proveedor. Y lo que entrega el proveedor debe ser revisado y aceptado por el cliente. Por eso, ambos procesos son dependientes.

---

## 1.14. Buenas prácticas en la ejecución de los procesos de acuerdo

### Contenido base

**Recomendaciones según la experiencia en proyectos reales:**

- Definir con precisión el alcance antes de firmar el contrato, porque esto minimiza conflictos posteriores.
- Establecer métricas de aceptación objetivas y medibles desde el inicio del acuerdo.
- Mantener trazabilidad entre requisitos, cláusulas contractuales y entregables del proyecto.
- Involucrar al área de calidad (**SQA**) para revisar los términos técnicos y asegurar cumplimiento normativo.
- Fomentar la comunicación continua entre el cliente y el proveedor durante todo el ciclo del contrato.
- Registrar lecciones aprendidas para mejorar acuerdos futuros y fortalecer la gestión del conocimiento.

**Relación con otros procesos de ISO/IEC/IEEE 12207:**

- Gestión de proyectos.
- Aseguramiento de la calidad.
- Verificación y validación.
- Gestión de la configuración y liberaciones.

### Explicación sencilla

Una buena contratación de software exige claridad desde el inicio. Mientras más ambiguo sea el contrato, más probables serán los problemas. Las buenas prácticas buscan evitar frases vagas como “el sistema debe ser fácil de usar” sin explicar cómo se medirá esa facilidad de uso.

Ejemplo de criterio medible:

- Poco claro: “El sistema debe ser rápido”.
- Más claro: “El sistema debe responder las consultas principales en menos de 3 segundos bajo una carga de 100 usuarios concurrentes”.

---

# 2. El contrato

## 2.1. Tipos de contratos de software

### Contenido base

Los contratos de software pueden ser:

- Contrato de precio fijo.
- Costo más porcentaje de costo.
- Costo más tarifa fija.
- De riesgo compartido.

Cada tipo de contrato tiene un perfil de riesgo diferente para el proveedor y el cliente.

### Explicación sencilla

El tipo de contrato define cómo se paga el trabajo y quién asume más riesgo si cambian el alcance, el tiempo o los costos.

| Tipo de contrato | Idea básica | Riesgo principal |
|---|---|---|
| Precio fijo | Se acuerda un valor cerrado por el producto o servicio. | El proveedor asume más riesgo si calculó mal el esfuerzo. |
| Costo más porcentaje de costo | El cliente paga los costos reales más un porcentaje adicional. | El cliente asume más riesgo porque el costo puede crecer. |
| Costo más tarifa fija | El cliente paga los costos reales más una tarifa fija acordada. | El cliente asume variación de costos, pero la ganancia del proveedor está más controlada. |
| Riesgo compartido | Cliente y proveedor comparten beneficios y pérdidas según resultados. | Ambos dependen del desempeño y del cumplimiento de objetivos. |

---

## 2.2. Contrato de desarrollo de software

### Contenido base

Este contrato se celebra en **[Ciudad, País]**, a **[Fecha]**, entre:

- **[Nombre de la empresa contratante]**, con domicilio en **[Dirección completa]**, representada por **[Nombre del representante legal]**, en adelante **“Cliente”**.
- **[Nombre del proveedor de desarrollo de software]**, con domicilio en **[Dirección completa]**, representada por **[Nombre del representante legal]**, en adelante **“Proveedor”**.

**Preámbulo:** El Cliente desea contratar los servicios del Proveedor para el desarrollo de un software específico según las especificaciones detalladas en este Contrato.

### Explicación sencilla

Esta parte identifica a las dos partes del contrato. También explica la razón general del acuerdo: el cliente necesita un software y el proveedor será contratado para desarrollarlo.

---

## 2.3. Cláusula 1: Objeto del contrato

### Contenido base

El Proveedor se compromete a desarrollar un software denominado **“[Nombre del Software]”** conforme a las especificaciones y requerimientos detallados en el **Anexo 1** de este Contrato, correspondiente a las especificaciones del proyecto.

### Explicación sencilla

El objeto del contrato responde a la pregunta: **¿qué se está contratando?**

Debe quedar claro el producto que se va a desarrollar y el documento donde están sus requisitos.

---

## 2.4. Cláusula 2: Alcance de los servicios

### Contenido base

El Proveedor realizará los siguientes servicios:

- **Fase de Diseño:** análisis de requisitos, diseño de la arquitectura del software y creación de prototipos.
- **Fase de Desarrollo:** programación y desarrollo del software conforme a las especificaciones.
- **Fase de Pruebas:** realización de pruebas de calidad, validación y corrección de errores.
- **Fase de Implementación:** instalación y puesta en funcionamiento del software en los sistemas del Cliente.
- **Mantenimiento y Soporte:** provisión de soporte técnico post-lanzamiento por un período de **[especificar duración]**.

### Explicación sencilla

El alcance define lo que sí está incluido en el contrato. Esto es vital para evitar discusiones posteriores sobre actividades no contempladas.

---

## 2.5. Cláusula 3: Plazos de entrega

### Contenido base

El desarrollo del software se llevará a cabo en las siguientes fases, con los siguientes plazos de entrega:

- **Fase de Diseño:** **[Fecha de inicio]** a **[Fecha de finalización]**.
- **Fase de Desarrollo:** **[Fecha de inicio]** a **[Fecha de finalización]**.
- **Fase de Pruebas:** **[Fecha de inicio]** a **[Fecha de finalización]**.
- **Fase de Implementación:** **[Fecha de inicio]** a **[Fecha de finalización]**.

El Proveedor se compromete a cumplir con los plazos establecidos. En caso de retrasos no justificados, el Cliente tendrá derecho a solicitar penalizaciones según lo establecido en este contrato.

### Explicación sencilla

Aquí se fija el calendario. No basta con decir “se entregará pronto”. Deben quedar fechas concretas para cada fase.

---

## 2.6. Cláusula 4: Precio y condiciones de pago

### Contenido base

El Cliente pagará al Proveedor la cantidad total de **[Monto Total]** por el desarrollo del software, que se distribuirá en los siguientes pagos:

1. **[Porcentaje] %** al inicio del proyecto.
2. **[Porcentaje] %** al finalizar la Fase de Diseño.
3. **[Porcentaje] %** al finalizar la Fase de Desarrollo.
4. **[Porcentaje] %** al finalizar la Fase de implementación y entrega final.

Los pagos se realizarán mediante transferencia bancaria a la cuenta proporcionada por el Proveedor, dentro de **[número de días]** días después de la recepción de la factura correspondiente.

### Explicación sencilla

Esta cláusula indica cuánto se paga, cuándo se paga y bajo qué condiciones. Es recomendable asociar pagos a hitos verificables, no solo a fechas.

---

## 2.7. Cláusula 5: Propiedad intelectual

### Contenido base

El Cliente será el propietario exclusivo de todos los derechos de propiedad intelectual relacionados con el software desarrollado, incluidos, pero no limitados a, derechos de autor, marcas registradas, patentes y secretos comerciales.

El Proveedor transferirá todos los derechos sobre el software al Cliente, una vez completado el proyecto y realizado el pago total.

### Explicación sencilla

Esta cláusula define quién será dueño del software. Es una de las partes más delicadas de un contrato de desarrollo, porque puede incluir código fuente, documentación, diseños, marcas o componentes reutilizables.

---

## 2.8. Cláusula 6: Confidencialidad

### Contenido base

El Proveedor se compromete a mantener la confidencialidad sobre toda la información y documentación proporcionada por el Cliente durante el desarrollo del software.

Esta obligación de confidencialidad persistirá por **[X años]** después de la finalización del contrato.

### Explicación sencilla

El proveedor puede tener acceso a información sensible del cliente. Esta cláusula obliga a protegerla incluso después de terminado el contrato.

---

## 2.9. Cláusula 7: Garantía y soporte

### Contenido base

El Proveedor garantiza que el software estará libre de defectos materiales y funcionará conforme a las especificaciones durante un período de **[X meses/años]** después de la entrega final. Durante este período, el Proveedor proporcionará soporte técnico sin costo adicional.

### Explicación sencilla

La garantía cubre defectos del software después de entregado. El soporte define cómo se atenderán problemas, dudas o fallas.

---

## 2.10. Cláusula 8: Penalizaciones por retrasos

### Contenido base

Si el Proveedor no cumple con los plazos establecidos para la entrega de las fases del proyecto, el Cliente tendrá derecho a imponer una penalización equivalente a **[X %]** del valor total del contrato por cada semana de retraso.

### Explicación sencilla

Esta cláusula busca proteger al cliente frente a retrasos injustificados. La penalización debe estar claramente definida para evitar interpretaciones.

---

## 2.11. Cláusula 9: Terminación anticipada

### Contenido base

El Cliente podrá terminar este contrato de forma anticipada si:

- El Proveedor no cumple con los plazos y las condiciones de entrega de manera significativa.
- El Proveedor incumple cualquier otra obligación esencial establecida en este contrato.
- En caso de terminación anticipada, el Cliente deberá pagar por los servicios ya prestados hasta la fecha de terminación.

### Explicación sencilla

Esta cláusula explica cuándo puede terminarse el contrato antes de tiempo y qué obligaciones económicas se mantienen.

---

## 2.12. Cláusula 10: Resolución de disputas

### Contenido base

Cualquier disputa derivada de este contrato será resuelta mediante **[mediación/arbitraje]** en **[ciudad o país]**, conforme a las leyes de **[jurisdicción]**.

### Explicación sencilla

Si hay conflicto, esta cláusula dice cómo se resolverá: mediante mediación, arbitraje u otro mecanismo definido por las partes.

---

## 2.13. Cláusula 11: Ley aplicable

### Contenido base

Este contrato se regirá e interpretará de acuerdo con las leyes de **[país o jurisdicción]**.

### Explicación sencilla

Indica qué marco legal se usará para interpretar el contrato. Esto es especialmente importante si cliente y proveedor están en ciudades o países diferentes.

---

## 2.14. Cláusula 12: Disposiciones generales

### Contenido base

- **Modificaciones:** Cualquier modificación a este contrato debe ser acordada por ambas partes y reflejada por escrito.
- **Independencia de las Cláusulas:** Si alguna de las cláusulas de este contrato es considerada nula o inaplicable, las demás cláusulas seguirán siendo válidas.

### Explicación sencilla

Estas disposiciones evitan cambios informales y protegen la validez del contrato si una cláusula específica llega a fallar.

---

## 2.15. Firmas

### Contenido base

**[Nombre del Cliente]**  
Cliente  
Fecha: _______________

**[Nombre del Proveedor]**  
Proveedor  
Fecha: _______________

### Explicación sencilla

La firma formaliza la aceptación del contrato por ambas partes.

---

# 3. Ejercicios

## 3.1. Ejercicio práctico: elaboración de un mini contrato de suministro

### Contenido base

**Contexto:** Una empresa local desea desarrollar un módulo de control de inventarios como parte de su sistema **ERP**.

**Actividad en grupos:**

1. Seleccionen un tipo de contrato adecuado: precio fijo, costo más porcentaje, riesgo compartido, etc.
2. Definan brevemente:
   - Objeto del contrato.
   - Entregables principales.
   - Criterios de aceptación.
   - Cláusulas de penalidad o soporte.
3. Elaboren un diagrama simple, en **PlantUML** o manual, que represente el flujo de interacción entre cliente y proveedor.
4. Presenten su propuesta al grupo, explicando las decisiones tomadas.

**Objetivo del ejercicio:** Aplicar los conceptos de la norma ISO/IEC/IEEE 12207:2017 a un caso realista, reforzando la comprensión práctica de los procesos de acuerdo.

### Explicación sencilla

El ejercicio busca que los estudiantes pasen de la teoría a la práctica. No se trata solo de definir un contrato, sino de justificar por qué ese tipo de contrato es adecuado para el caso.

Términos útiles:

| Término | Significado sencillo |
|---|---|
| ERP | Sistema que integra procesos de una empresa, como inventarios, compras, ventas, contabilidad o recursos humanos. |
| PlantUML | Herramienta que permite crear diagramas usando texto. |
| Criterios de aceptación | Condiciones que debe cumplir el producto para que el cliente lo reciba formalmente. |

---

# 4. Referencias y datos de contacto

## 4.1. Referencias

### Contenido base

**Referencias (1/1)**

El material incluye una sección de referencias, sin detalle bibliográfico adicional en la transcripción textual extraída.

## 4.2. Datos de contacto del docente

### Contenido base

**Albeiro Espinosa Bedoya, Ph.D. Ms.C.**  
Profesor Asociado  
Email: aespinos@unal.edu.co  
Instagram: @albeiroespinosabedoya  
Departamento de Ciencias de la Computación y de la Decisión, Facultad de Minas  
Dirección: Av. 80 #65-223, Bloque M8A, Of. 204  
Teléfono: +57 604 4255384

---

# 5. Glosario básico de la sesión

| Concepto | Explicación sencilla |
|---|---|
| Acuerdo | Documento o compromiso formal entre cliente y proveedor. |
| Adquisición | Proceso que realiza el cliente para obtener un producto o servicio. |
| Suministro | Proceso que realiza el proveedor para entregar un producto o servicio. |
| Cliente | Parte que necesita, compra o contrata el software. |
| Proveedor | Parte que desarrolla, entrega o mantiene el software. |
| RFP | Solicitud formal de propuesta enviada a posibles proveedores. |
| Entregable | Producto, documento, módulo o resultado que debe entregar el proveedor. |
| Criterio de aceptación | Condición verificable para decidir si un entregable cumple. |
| Trazabilidad | Relación documentada entre requisitos, contrato, entregables y pruebas. |
| SQA | Aseguramiento de la calidad del software. |
| SaaS | Software como servicio, normalmente accedido por internet. |
| ERP | Sistema empresarial integrado para gestionar procesos organizacionales. |
| Penalización | Consecuencia económica o contractual por incumplimiento. |
| Acta de aceptación | Documento que confirma la recepción y aprobación de un entregable. |

---

# 6. Lectura final integradora

Los procesos de acuerdo permiten organizar formalmente la relación entre un cliente y un proveedor de software. Según la lógica de ISO/IEC/IEEE 12207:2017, el cliente ejecuta el proceso de adquisición y el proveedor ejecuta el proceso de suministro. Ambos procesos deben estar sincronizados porque las decisiones de una parte afectan directamente las obligaciones de la otra.

Un contrato de software bien elaborado debe definir con claridad el objeto, alcance, entregables, plazos, pagos, criterios de aceptación, propiedad intelectual, confidencialidad, soporte, penalizaciones, resolución de disputas y cierre. Cuando estos elementos quedan ambiguos, aumentan los riesgos de incumplimiento, retrasos, sobrecostos y conflictos contractuales.

Desde la perspectiva de calidad de software, la gestión de proveedores y acuerdos no es solo un asunto administrativo o jurídico. También es una práctica de aseguramiento de calidad, porque permite alinear requisitos, entregables, pruebas, aceptación y responsabilidades desde el inicio del proyecto.
