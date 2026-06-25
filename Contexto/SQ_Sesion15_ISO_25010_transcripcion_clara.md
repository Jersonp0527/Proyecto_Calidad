# SQ - Sesión 15: ISO/IEC 25010

**Curso:** Calidad de Software  
**Código:** 3007849  
**Profesor:** Albeiro Espinosa Bedoya, Ph.D. Ms.C.  
**Facultad:** Facultad de Minas, Sede Medellín  
**Tema:** ISO 25010

---

## Nota de lectura

Este documento organiza en formato Markdown el contenido del archivo original sobre **ISO/IEC 25010**. La información técnica se conserva, pero se presenta con estructura, tablas y explicaciones sencillas para facilitar la comprensión de una persona que no conoce el tema.

Las secciones tituladas **“Explicación sencilla”** son aclaraciones agregadas para facilitar el aprendizaje. No reemplazan el contenido original.

---

## Agenda original

1. Referencias

> **Observación de calidad:** aunque la agenda original solo menciona “Referencias”, el material desarrolla varios temas: ISO/IEC 25000 SQuaRE, ISO/IEC 25010, ISO/IEC 25020, ISO/IEC 25022, ISO/IEC 25023 e integración de estas normas.

---

# 1. ¿Por qué necesitamos estándares de calidad de software?

## El problema real

En los proyectos de software suelen aparecer problemas como:

- Aplicaciones lentas, con errores frecuentes o difíciles de usar.
- Dificultad para saber si un sistema es realmente de calidad.
- Falta de claridad sobre qué medir y cómo comparar productos.

## La respuesta

**ISO/IEC 25000 — SQuaRE** proporciona un lenguaje común y un marco sistemático para **definir, medir y evaluar la calidad del software**.

## Caso motivador

Una universidad evalúa tres sistemas LMS distintos. Sin un estándar, cada evaluador usa criterios distintos y llegan a conclusiones contradictorias.

Con **SQuaRE** se tienen:

- Criterios objetivos.
- Métricas comparables.
- Decisión justificada.

## Explicación sencilla

Un estándar de calidad sirve para que todos evalúen el software con las mismas reglas. Sin un estándar, una persona puede decir que un sistema es bueno porque “se ve bonito”, otra porque “es rápido” y otra porque “no falla”. Con ISO/IEC 25000 se define qué aspectos revisar y cómo medirlos.

---

# 2. ¿Qué es ISO/IEC 25000 (SQuaRE)?

## Definición clave

**SQuaRE** significa **Software Product Quality Requirements and Evaluation**.

Es una familia de normas ISO/IEC que establece un marco integral para **especificar, medir y evaluar la calidad de productos software**.

## Evolución histórica

| Norma anterior | Evolución | Norma actual |
|---|---|---|
| ISO/IEC 9126 | → | ISO/IEC 25000 |
| 1991–2001 | evolución | 2005–hoy |
| Modelo básico | → | Marco completo e integrado |

## Dos perspectivas complementarias

| Perspectiva | Qué observa |
|---|---|
| Calidad del producto | Atributos técnicos medibles del software. |
| Calidad en uso | Experiencia real del usuario al interactuar con el software. |

## Explicación sencilla

La familia ISO/IEC 25000 no se queda solo en preguntar si el programa funciona. También ayuda a revisar si el usuario puede usarlo bien, si el sistema responde rápido, si protege los datos, si se puede mantener, si se puede instalar en distintos entornos y si realmente sirve para el propósito para el que fue creado.

---

# 3. Estructura de la familia ISO/IEC 25000

| Norma | Nombre | Responde a... |
|---|---|---|
| 25010 | Modelo de calidad del software | ¿Qué medir? |
| 25020 | Guía de medición de calidad | ¿Cómo medir? |
| 25022 | Medición de calidad en uso | ¿Cómo lo vive el usuario? |
| 25023 | Medición de calidad del producto | ¿Cómo es el producto? |
| 25030 | Requisitos de calidad | ¿Qué exigir? |
| 25040 | Evaluación del producto software | ¿Cómo evaluar? |

## Enfoque de la sesión

Para esta sesión se trabajan principalmente:

- **ISO/IEC 25010:** modelo de calidad.
- **ISO/IEC 25020:** medición.
- **ISO/IEC 25022:** calidad en uso.
- **ISO/IEC 25023:** calidad del producto.

## Explicación sencilla

La familia ISO/IEC 25000 funciona como una caja de herramientas. Cada norma cumple una función diferente. Primero se define qué significa calidad, luego se decide cómo medirla, después se revisa cómo vive el usuario el sistema y también cómo se comporta técnicamente el producto.

---

# 4. ISO/IEC 25010: modelo de calidad - visión general

ISO/IEC 25010 organiza la calidad desde dos grandes perspectivas:

1. **Calidad del producto.**
2. **Calidad en uso.**

## 4.1. Calidad del producto

Se refiere a los atributos del software en sí mismo.

Las 8 características de calidad del producto son:

1. Adecuación funcional.
2. Eficiencia de desempeño.
3. Compatibilidad.
4. Usabilidad.
5. Fiabilidad.
6. Seguridad.
7. Mantenibilidad.
8. Portabilidad.

## 4.2. Calidad en uso

Se refiere a la experiencia del usuario con el sistema.

Las 5 características de calidad en uso son:

1. Eficacia.
2. Productividad.
3. Seguridad en uso.
4. Satisfacción.
5. Contexto de uso.

## Analogía del material

- **Calidad del producto** = ficha técnica del auto.
- **Calidad en uso** = cómo se siente manejarlo.

## Explicación sencilla

Un sistema puede estar técnicamente bien construido, pero ser difícil de usar. Por eso ISO/IEC 25010 mira dos lados: el lado técnico del software y el lado de la experiencia real del usuario.

---

# 5. ISO/IEC 25010: las 8 características del producto

| Característica | ¿Qué evalúa? | Ejemplo práctico |
|---|---|---|
| Adecuación funcional | ¿Hace lo que debe hacer? | El carrito de compras calcula el total correctamente. |
| Eficiencia de desempeño | ¿Usa bien los recursos? | La página carga en menos de 2 segundos con 5 000 usuarios. |
| Compatibilidad | ¿Convive con otros sistemas? | La API bancaria integra con apps de terceros. |
| Usabilidad | ¿Es fácil de usar y aprender? | Un estudiante inscribe cursos sin manual. |
| Fiabilidad | ¿Falla poco y se recupera bien? | El LMS está disponible 99.9 % durante exámenes. |
| Seguridad | ¿Protege datos e identidades? | Historial clínico cifrado en telemedicina. |
| Mantenibilidad | ¿Es fácil de modificar? | Actualizar impuestos en 2 horas sin romper módulos. |
| Portabilidad | ¿Funciona en distintos entornos? | App móvil en Android, iOS y web. |

## Explicación sencilla

Estas 8 características ayudan a revisar el software como producto. No basta con que tenga funciones. También debe ser rápido, seguro, confiable, fácil de usar, compatible con otros sistemas, fácil de mantener y capaz de funcionar en diferentes entornos.

---

# 6. ISO/IEC 25010: subcaracterísticas clave

| Característica | Subcaracterísticas |
|---|---|
| Adecuación funcional | Completitud, corrección, adecuación. |
| Eficiencia de desempeño | Comportamiento temporal, utilización de recursos, capacidad. |
| Usabilidad | Aprendibilidad, operabilidad, accesibilidad, protección ante errores. |
| Fiabilidad | Madurez, disponibilidad, tolerancia a fallos, recuperabilidad. |
| Seguridad | Confidencialidad, integridad, no-repudio, autenticidad, trazabilidad. |
| Mantenibilidad | Analizabilidad, modificabilidad, testabilidad. |
| Portabilidad | Adaptabilidad, instalabilidad, reemplazabilidad. |

## Reflexión rápida del material

¿Cuál característica priorizarías al evaluar una app de pagos digitales? ¿Y un sistema de nómina empresarial? ¿Por qué?

## Explicación sencilla

Cada característica se puede descomponer en aspectos más concretos. Por ejemplo, “seguridad” no es una sola cosa: incluye confidencialidad, integridad, autenticidad y trazabilidad. Esto permite evaluar la calidad de forma más precisa.

---

# 7. ISO/IEC 25010 en acción: e-commerce

## Escenario

Evaluar la calidad de una tienda en línea con **50 000 usuarios diarios**.

## Características prioritarias

- **Eficiencia:** tiempo de carga de catálogos.
- **Seguridad:** cifrado de pagos con tarjeta.
- **Fiabilidad:** disponibilidad en temporadas altas.
- **Usabilidad:** flujo de compra intuitivo.

## Preguntas de evaluación

- ¿Responde en menos de 1 segundo bajo carga de Black Friday?
- ¿Sigue el estándar PCI-DSS para tarjetas?
- ¿El usuario completa la compra sin errores?
- ¿Se recupera ante caída del servidor de pagos?

## Clave de diseño instruccional

Antes de medir, siempre se responde:

> ¿Qué características son críticas en este contexto?

## Explicación sencilla

No todos los sistemas necesitan priorizar lo mismo. En una tienda en línea es clave que el sistema sea rápido, seguro para los pagos, estable en temporadas de alto tráfico y fácil de usar para comprar sin complicaciones.

---

# 8. ISO/IEC 25020: ¿cómo medir la calidad?

## Propósito central

ISO/IEC 25020 proporciona un **modelo de referencia de medición (MRM)** que conecta las características de calidad con métricas concretas y criterios de decisión.

## Flujo de medición

```text
Requisito de calidad → Característica (25010) → Métrica (25020) → Evaluación → Decisión
```

## Tipos de métricas

| Tipo de métrica | Descripción | Ejemplo |
|---|---|---|
| Directas | Se miden de forma objetiva. | Tiempo de respuesta en milisegundos. |
| Derivadas | Se calculan a partir de otras métricas. | Promedio de respuesta por transacción. |
| Subjetivas | Se basan en percepción. | Escala de satisfacción de 1 a 5. |

## Error común

Medir todo sin priorizar.

## Buena práctica

Seleccionar solo las métricas alineadas con los objetivos del proyecto.

## Explicación sencilla

Medir calidad no significa medir cualquier cosa. Primero se define qué se quiere evaluar, luego se escoge la métrica adecuada y después se toma una decisión con base en datos.

---

# 9. ISO/IEC 25020: ejemplo de banca digital

## Sistema

App de banco móvil con **200 000 usuarios activos**.

| Característica | Métrica | Tipo | Criterio |
|---|---|---|---|
| Eficiencia | Tiempo de login | Directa | < 2 s |
| Eficiencia | Tiempo promedio/transacción | Derivada | < 3 s |
| Fiabilidad | Disponibilidad mensual | Directa | ≥ 99.9 % |
| Seguridad | Intentos de autenticación fallida | Directa | < 0.01 % |
| Usabilidad | Satisfacción percibida (encuesta) | Subjetiva | ≥ 4.2/5 |

## Explicación sencilla

En una app bancaria se mide la rapidez para ingresar, la rapidez para hacer operaciones, la disponibilidad del servicio, la seguridad en la autenticación y la percepción de los usuarios. Cada métrica tiene un criterio que permite decidir si el sistema cumple o no.

---

# 10. ISO/IEC 25022: calidad en uso - perspectiva del usuario

## Definición

La **calidad en uso** mide el grado en que un sistema permite a los usuarios alcanzar sus objetivos de forma **eficaz, eficiente y satisfactoria** en un contexto de uso específico.

## Las 5 características de calidad en uso

| Característica | ¿Qué mide? | Métrica típica |
|---|---|---|
| Eficacia | ¿El usuario logra su objetivo? | % tareas completadas. |
| Productividad | ¿Con qué esfuerzo? | Tiempo promedio por tarea. |
| Seguridad en uso | ¿Hay riesgos para el usuario o datos? | N.º de errores críticos. |
| Satisfacción | ¿Le gusta usar el sistema? | Escala Likert en encuesta. |
| Contexto de uso | ¿Importa el entorno? | Condiciones: red, dispositivo, etc. |

## Diferencia clave

| Tipo de calidad | Pregunta central |
|---|---|
| Calidad del producto | ¿Funciona bien técnicamente? |
| Calidad en uso | ¿Funciona bien para el usuario? |

Un sistema puede tener 0 errores técnicos y aun así tener mala calidad en uso si los usuarios no logran sus tareas.

## Explicación sencilla

La calidad en uso se centra en la experiencia real. Por ejemplo, un sistema puede no presentar errores técnicos, pero si los usuarios se confunden, se demoran demasiado o abandonan la tarea, entonces la calidad en uso es baja.

---

# 11. ISO/IEC 25022 en acción: Sistema LMS universitario

## Escenario

Evaluar la calidad en uso del LMS para **8 000 estudiantes**.

| Característica | Métrica definida | Resultado |
|---|---|---|
| Eficacia | % estudiantes que inscriben asignaturas sin ayuda | 91 % ✓ |
| Productividad | Tiempo promedio de inscripción completa | 4 min 20 s ✗ (meta: 3 min) |
| Seguridad en uso | Inscripciones incorrectas sin confirmación de error | 3 % ✗ |
| Satisfacción | Encuesta al final del proceso (1–5) | 3.8 / 5 ✗ (meta: 4.0) |

## Conclusiones del análisis

- El flujo de inscripción es lento → rediseñar UX del módulo de búsqueda de materias.
- Faltan mensajes de error claros → implementar validaciones en tiempo real.

## Pregunta de reflexión

¿Cómo afecta el contexto de uso, por ejemplo estudiante en móvil vs. escritorio, a estas métricas?

## Explicación sencilla

El ejemplo muestra que el sistema no está totalmente mal: el 91 % logra inscribir asignaturas sin ayuda. Sin embargo, hay problemas en tiempo, errores y satisfacción. Por eso la solución no es “reconstruir todo”, sino mejorar puntos específicos del flujo de inscripción.

---

# 12. ISO/IEC 25023: medición de la calidad del producto

## Propósito

ISO/IEC 25023 proporciona métricas concretas para evaluar las características de calidad definidas en ISO/IEC 25010. Esto permite comparaciones objetivas entre versiones o sistemas.

## Proceso de medición en 5 pasos

1. Seleccionar la característica de calidad a evaluar.
2. Identificar los atributos medibles que la reflejan.
3. Elegir métricas directas, derivadas o subjetivas.
4. Recolectar datos siguiendo procedimientos estandarizados.
5. Comparar resultados con criterios predefinidos → decisión.

## Explicación sencilla

ISO/IEC 25023 ayuda a convertir conceptos generales de calidad en datos concretos. Por ejemplo, si se quiere medir fiabilidad, se puede usar la tasa de fallos; si se quiere medir eficiencia, se puede usar el tiempo de respuesta.

---

# 13. ISO/IEC 25023: ejemplos de métricas por característica

| Característica | Métrica | Unidad |
|---|---|---|
| Fiabilidad | Tasa de fallos | Fallos / 1 000 horas. |
| Eficiencia | Tiempo de respuesta | ms / operación. |
| Usabilidad | Tiempo de aprendizaje | Horas de capacitación. |
| Mantenibilidad | Tiempo de implementación de cambio | Horas / cambio. |
| Portabilidad | Tasa de instalaciones exitosas | % plataformas compatibles. |

## Explicación sencilla

Cada característica puede medirse con una unidad concreta. Eso permite comparar sistemas o versiones. Por ejemplo, si una versión tarda 500 ms por operación y otra tarda 2 000 ms, se puede demostrar con datos cuál tiene mejor eficiencia.

---

# 14. ISO/IEC 25023 en acción: Plataforma de telemedicina

## Escenario

Auditoría de calidad antes del despliegue en **30 hospitales**.

| Característica | Métrica | Criterio | Resultado |
|---|---|---|---|
| Funcionalidad | Exactitud de diagnóstico asistido por IA | ≥ 97 % | 98.2 % ✓ |
| Seguridad | Vulnerabilidades críticas en auditoría | 0 | 0 ✓ |
| Fiabilidad | MTBF (tiempo medio entre fallos) | ≥ 720 h | 850 h ✓ |
| Mantenibilidad | Tiempo para actualización de emergencia | ≤ 4 h | 3.2 h ✓ |
| Portabilidad | Instalaciones exitosas (Win/Linux/iOS) | 100 % | 97 % ✗ |

## Acción derivada

Problema en instalación iOS → revisar dependencias de la librería de cifrado antes del despliegue.

## Buena práctica

Documentar criterios de aceptación antes de medir. No ajustar el criterio después de ver los resultados.

## Explicación sencilla

Este ejemplo muestra cómo las métricas ayudan a tomar decisiones. La plataforma cumple en funcionalidad, seguridad, fiabilidad y mantenibilidad, pero falla en portabilidad. Por tanto, antes de desplegar en hospitales, se debe corregir el problema de instalación en iOS.

---

# 15. Integración ISO 25010-25023: el ciclo completo

| Norma | Rol en el ciclo | Pregunta central | Produce |
|---|---|---|---|
| 25010 | Modelo de referencia | ¿Qué es calidad? | Características y subcaracterísticas. |
| 25020 | Guía metodológica | ¿Cómo medir? | Métricas, indicadores, criterios. |
| 25022 | Evaluación centrada en el usuario | ¿Cómo lo vive el usuario? | Métricas de eficacia y satisfacción. |
| 25023 | Evaluación del producto | ¿Cómo es el software? | Métricas técnicas objetivas. |

## Flujo integrado aplicado a un sistema académico

1. **25010** → Se identifican usabilidad y fiabilidad como características críticas.
2. **25020** → Se definen métricas: tiempo de respuesta, tasa de fallos, satisfacción.
3. **25023** → Se mide: 1.8 s promedio, 0 caídas en 30 días.
4. **25022** → Se mide: 91 % eficacia, satisfacción 4.1/5.
5. **Resultado** → Plan de mejora fundamentado en datos.

## Explicación sencilla

Las normas se complementan. Primero se define qué se entiende por calidad, luego se decide cómo medirla, después se revisa el producto técnicamente y también la experiencia del usuario. El resultado final no debe ser una opinión, sino un plan de mejora basado en evidencia.

---

# 16. Referencias

El material incluye una sección de referencias, pero no presenta referencias bibliográficas detalladas en las diapositivas visibles. La diapositiva 20 aparece con el título **“Referencias (1/1)”**, sin contenido adicional visible.

---

# 17. Información de contacto del profesor

**Albeiro Espinosa Bedoya, Ph.D. Ms.C.**  
Profesor Asociado  
**Email:** aespinos@unal.edu.co  
**Instagram:** @albeiroespinosabedoya  
**Departamento:** Departamento de Ciencias de la Computación y de la Decisión, Facultad de Minas  
**Dirección:** Av. 80 #65-223, Bloque M8A, Of. 204  
**Teléfono:** +57 604 4255384

---

# 18. Síntesis final para estudiar

ISO/IEC 25010 permite entender **qué significa calidad de software**. Esta calidad no se limita a que el programa funcione, sino que también incluye desempeño, seguridad, usabilidad, confiabilidad, mantenibilidad y portabilidad.

ISO/IEC 25020 ayuda a definir **cómo medir** esa calidad. ISO/IEC 25022 se centra en la **calidad en uso**, es decir, en cómo el usuario realmente vive el sistema. ISO/IEC 25023 permite medir la **calidad del producto** mediante métricas técnicas.

En conjunto, estas normas permiten evaluar software con criterios objetivos, comparar alternativas y justificar decisiones con datos.

---

# 19. Glosario básico

| Término | Explicación sencilla |
|---|---|
| Software | Programa o sistema informático que realiza funciones para un usuario u organización. |
| Calidad de software | Grado en que el software cumple requisitos técnicos y satisface las necesidades del usuario. |
| ISO/IEC 25000 | Familia de normas para especificar, medir y evaluar calidad de software. |
| SQuaRE | Nombre de la familia ISO/IEC 25000. Significa Software Product Quality Requirements and Evaluation. |
| ISO/IEC 25010 | Norma que define el modelo de calidad del software. |
| ISO/IEC 25020 | Norma que orienta cómo medir la calidad. |
| ISO/IEC 25022 | Norma enfocada en medir la calidad en uso. |
| ISO/IEC 25023 | Norma enfocada en medir la calidad del producto software. |
| Métrica | Medida usada para evaluar un aspecto de calidad. |
| Criterio | Valor o condición que indica si el resultado cumple o no cumple. |
| Fiabilidad | Capacidad del sistema de funcionar sin fallos y recuperarse si ocurren. |
| Usabilidad | Facilidad con la que una persona puede aprender y usar el sistema. |
| Portabilidad | Capacidad del sistema de funcionar en distintos entornos. |
| Mantenibilidad | Facilidad para analizar, modificar y probar el software. |
| Calidad en uso | Experiencia real del usuario al usar el sistema en un contexto determinado. |

