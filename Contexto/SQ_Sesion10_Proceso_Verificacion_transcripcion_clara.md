# Calidad de Software - Proceso de Verificación

**Universidad Nacional de Colombia**  
**Facultad de Minas - Sede Medellín**  
**Curso:** Calidad de Software  
**Código:** 3010440  
**Profesor:** Albeiro Espinosa Bedoya, Ph.D. Ms.C.  
**Tema:** Proceso de Verificación

---

## Nota de organización del documento

Este documento transcribe y organiza el contenido del material **“Proceso de Verificación”** en formato Markdown.  
La información técnica, los ejemplos, las tablas, el código y las relaciones conceptuales se conservan.  
Además, se agregan explicaciones sencillas para que una persona sin conocimiento previo pueda comprender el tema desde lo básico hasta lo más complejo.

> **Importante:** Las secciones tituladas **“Explicación sencilla”** no reemplazan la información original. Solo la aclaran con palabras más directas.

---

# Tabla de contenido

1. [Agenda](#agenda)
2. [Idea general del tema](#idea-general-del-tema)
3. [Conceptos básicos antes de empezar](#conceptos-básicos-antes-de-empezar)
4. [Proceso de Verificación - ISO 12207](#1-proceso-de-verificación---iso-12207)
5. [Técnicas de Verificación](#2-técnicas-de-verificación)
6. [Técnicas Estáticas](#3-técnicas-estáticas)
7. [Técnicas Dinámicas](#4-técnicas-dinámicas)
8. [Pruebas de Caja Negra](#41-pruebas-de-caja-negra)
9. [Partición de Equivalencia](#42-partición-de-equivalencia)
10. [Análisis de Valores Límite](#43-análisis-de-valores-límite)
11. [Tabla de Decisión](#44-tabla-de-decisión)
12. [Pruebas de Caja Blanca](#45-pruebas-de-caja-blanca)
13. [Cobertura de Sentencias](#46-cobertura-de-sentencias)
14. [Cobertura de Decisiones](#47-cobertura-de-decisiones)
15. [Cobertura de Condiciones](#48-cobertura-de-condiciones)
16. [Referencias y datos de contacto](#5-referencias-y-datos-de-contacto)
17. [Resumen final del tema](#resumen-final-del-tema)
18. [Observaciones técnicas de calidad sobre el material](#observaciones-técnicas-de-calidad-sobre-el-material)

---

# Agenda

1. Proceso de Verificación - ISO 12207.
2. Técnicas de Verificación.
3. Técnicas Estáticas.
4. Técnicas Dinámicas.
5. Referencias.

---

# Idea general del tema

La **verificación de software** busca responder una pregunta central:

> **¿El producto que estamos construyendo cumple con los requisitos especificados?**

En otras palabras, la verificación revisa si los documentos, modelos, código, pruebas, componentes y demás productos del desarrollo están hechos correctamente según lo que se pidió.

No se trata solamente de “probar el programa al final”. También incluye revisar documentos, requisitos, diseños, código, planes de prueba y otros artefactos antes de que el sistema esté terminado.

---

# Conceptos básicos antes de empezar

## Software

Es el conjunto de programas, datos, documentos y procesos que permiten que un sistema informático funcione.

## Requisito

Es una condición, necesidad o característica que el sistema debe cumplir.  
Ejemplo: “El sistema debe permitir que el usuario inicie sesión con correo y contraseña”.

## Verificación

Es el proceso de confirmar que los productos y servicios cumplen los requisitos especificados.

## Defecto

Es un error, inconsistencia, omisión o incumplimiento encontrado en un artefacto de software.

## Artefacto

Es cualquier producto generado durante el desarrollo de software.  
Ejemplos:

- Documento de requisitos.
- Caso de uso.
- Diagrama.
- Código fuente.
- Plan de pruebas.
- Manual de usuario.

## Técnica estática

Es una técnica de verificación que se aplica **sin ejecutar el software**.  
Ejemplo: revisar un documento de requisitos o revisar código fuente manualmente.

## Técnica dinámica

Es una técnica de verificación que exige **ejecutar el software**.  
Ejemplo: hacer pruebas con datos de entrada y revisar la salida del sistema.

---

# 1. Proceso de Verificación - ISO 12207

## Ubicación del proceso en el ciclo de vida del software

El material ubica el proceso de **Verificación de Software (7.2.4)** dentro de la norma **ISO/IEC/IEEE 12207 – Procesos del Ciclo de Vida del Software**.

La clasificación general presentada es la siguiente:

## Procesos en Contexto de Sistema

### Procesos de Acuerdo

- Proceso de Adquisición (6.1.1).
- Proceso de Suministro (6.1.2).

### Procesos Organizacionales

- Gestión del Modelo de Ciclo de Vida (6.2.1).
- Gestión de Infraestructura (6.2.2).
- Gestión de Portafolio de Proyectos (6.2.3).
- Gestión de Recursos Humanos (6.2.4).
- Gestión de la Calidad (6.2.5).

### Procesos de Proyecto

- Planificación del Proyecto (6.3.1).
- Evaluación y Control del Proyecto (6.3.2).
- Gestión de Decisiones (6.3.3).
- Gestión de Riesgos (6.3.4).
- Gestión de Configuración (6.3.5).
- Gestión de la Información (6.3.6).
- Medición (6.3.7).

### Procesos Técnicos

- Definición de Requisitos de las Partes Interesadas (6.4.1).
- Análisis de Requisitos del Sistema (6.4.2).
- Diseño Arquitectónico del Sistema (6.4.3).
- Implementación (6.4.4).
- Integración del Sistema (6.4.5).
- Pruebas de Calificación del Sistema (6.4.6).
- Instalación del Software (6.4.7).
- Soporte a la Aceptación del Software (6.4.8).
- Operación del Software (6.4.9).
- Mantenimiento del Software (6.4.10).
- Retiro del Software (6.4.11).

## Procesos Específicos de Software

### Procesos de Implementación

- Implementación de Software (7.1.1).
- Análisis de Requisitos de Software (7.1.2).
- Diseño Arquitectónico de Software (7.1.3).
- Diseño Detallado de Software (7.1.4).
- Construcción de Software (7.1.5).
- Integración de Software (7.1.6).
- Pruebas de Calificación de Software (7.1.7).

### Procesos de Soporte

- Gestión de Documentación de Software (7.2.1).
- Gestión de Configuración de Software (7.2.2).
- Aseguramiento de la Calidad de Software (7.2.3).
- **Verificación de Software (7.2.4).**
- Validación de Software (7.2.5).
- Revisión de Software (7.2.6).
- Auditoría de Software (7.2.7).
- Resolución de Problemas de Software (7.2.8).

### Procesos de Reutilización

- Ingeniería de Dominio (7.3.1).
- Gestión de Activos Reutilizables (7.3.2).
- Gestión del Programa de Reutilización (7.3.3).

**Figura 1:** El proceso de Verificación en el Ciclo de Vida.

## Explicación sencilla

La norma ISO 12207 organiza todo lo que ocurre durante la vida de un software: desde comprarlo, planearlo, construirlo, probarlo, mantenerlo y retirarlo.  
Dentro de esa estructura, la **verificación** aparece como un proceso de soporte porque ayuda a asegurar que lo que se está construyendo cumple lo especificado.

---

## Proceso de Verificación de Software

### Propósito

Confirmar que productos y servicios cumplen requisitos especificados.

### Resultados esperados

- Estrategia de verificación definida y aplicada.
- Criterios de verificación identificados.
- Actividades de verificación ejecutadas.
- Defectos detectados y registrados.
- Resultados disponibles para cliente y partes interesadas.

### Actividades principales

#### Implementación de procesos

- Analizar criticidad, riesgos, recursos.
- Determinar necesidad de verificación e independencia.
- Establecer proceso de verificación.
- Seleccionar organización independiente, si aplica.
- Definir actividades y productos a verificar.
- Elaborar plan de verificación: actividades, recursos, cronograma.
- Aplicar plan y resolver no conformidades.

#### Verificación de requisitos

- Coherencia, factibilidad, trazabilidad.
- Cumplimiento de seguridad y criticidad.

#### Verificación de diseño

- Corrección y coherencia con requisitos.
- Flujo lógico, manejo de errores.
- Cumplimiento de requisitos críticos.

#### Verificación de código

- Trazabilidad al diseño y requisitos.
- Calidad, estándares, flujo de datos/control.
- Implementación de requisitos críticos.

#### Verificación de integración

- Integración completa de componentes y sistema.
- Ejecución según plan de integración.

#### Verificación de documentación

- Adecuación, completitud, coherencia.
- Preparación oportuna.
- Gestión de configuración.

**Figura 2:** Proceso de Verificación - Propósito.  
**Figura 3:** Proceso de Verificación - Resultados.  
**Figura 4:** Proceso de Verificación - Resultados - Implementación del Proceso.  
**Figura 5:** Proceso de Verificación - Artefactos sujetos a Verificación.

## Explicación sencilla

La verificación no revisa una sola cosa. Revisa varias partes del proyecto:

- Si los **requisitos** son claros y posibles de cumplir.
- Si el **diseño** responde a esos requisitos.
- Si el **código** sigue el diseño y los estándares.
- Si los componentes se **integran** correctamente.
- Si la **documentación** está completa y coherente.

Una forma simple de verlo es esta:

```text
Requisitos → Diseño → Código → Integración → Documentación
      ↓          ↓        ↓          ↓              ↓
   verificar  verificar verificar  verificar     verificar
```

---

# 2. Técnicas de Verificación

El material presenta las **Técnicas de Verificación (ISO/IEC/IEEE 29119-4)** organizadas en grandes grupos.

## Técnicas Estáticas

### Revisión de Documentación

- Revisión Informal.
- Revisión Técnica.
- Inspección Formal.
- Walkthroughs.

### Revisión de Código Fuente

- Análisis Manual.
- Revisión entre Pares.
- Checklist de Estándares.
- Análisis de Complejidad.

### Análisis Estático Automatizado

- Análisis Léxico.
- Análisis de Sintaxis.
- Análisis de Estilo de Código.
- Análisis de Dependencias.
- Análisis de Seguridad Estática.
- Herramientas CI/CD para Linting.
- Herramientas CI/CD para Linting (Pylint).

## Técnicas Dinámicas

### Pruebas de Caja Negra

- Partición de Equivalencia.
- Análisis de Valores Límite.
- Tabla de Decisión.
- Transición de Estados.
- Pruebas de Casos de Uso.
- Pruebas Basadas en Requisitos.
- Pruebas Exploratorias.

### Pruebas de Caja Blanca

- Cobertura de Sentencias.
- Cobertura de Decisiones.
- Cobertura de Condiciones.
- Cobertura de Caminos.
- Cobertura de Condiciones Mutuamente Exclusivas.
- Pruebas de Flujo de Datos.
- Pruebas de Condición Multiple.

### Pruebas de Integración

- Pruebas de Interfaces.
- Pruebas de Servicios.
- Pruebas de APIs.
- Pruebas de Integración de Componentes.

### Pruebas de Sistema

- Funcionales.
- No Funcionales.

### Pruebas de Aceptación

- Pruebas de Usuario.
- Pruebas de Negocio.
- Validación frente a Requisitos.

## Técnicas Formales

### Especificación Formal

- Z, VDM, B-Method.
- Lenguajes de Lógica (LTL, CTL).

### Verificación Formal

- Demostraciones Matemáticas.
- Model Checking.
- Análisis de Consistencia.

### Pruebas Basadas en Modelos (MBT)

- Modelos de Estados Finito.
- Árboles de Decisión.
- Diagramas de Actividad.
- Diagramas de Flujo de Datos.
- Automatización desde Modelos.

## Técnicas Basadas en la Experiencia

### Error Guessing - Suposición de Errores

- Pruebas Exploratorias.
- Heurísticas de Prueba.
- Ataques de Prueba Basados en Casos Reales.

### Test Tours - Tours de Prueba

- Tour de Interfaz.
- Tour de Entrada Invalida.
- Tour de Configuración.

## Técnicas Basadas en Riesgo

- Priorización de Pruebas por Impacto.
- Priorización por Probabilidad de Falla.
- Identificación de Riesgos Críticos.
- Diseño de Pruebas Mitigadoras.
- Matriz de Riesgo-Cobertura.

**Figura 6:** Técnicas de Verificación.  
**Figura 7:** Técnicas de Verificación - Estáticas.  
**Figura 8:** Técnicas de Verificación - Dinámicas.

## Explicación sencilla

Las técnicas de verificación se pueden entender así:

| Tipo de técnica | ¿Ejecuta el software? | ¿Qué revisa? | Ejemplo |
|---|---:|---|---|
| Estática | No | Documentos, requisitos, modelos, código | Revisar un caso de uso antes de programarlo |
| Dinámica | Sí | Comportamiento del sistema funcionando | Probar si una edad inválida genera error |
| Formal | No necesariamente | Propiedades matemáticas o modelos | Verificar lógicamente un modelo |
| Basada en experiencia | Depende | Posibles errores conocidos por experiencia | Imaginar fallos frecuentes del usuario |
| Basada en riesgo | Depende | Partes críticas o riesgosas del sistema | Probar primero pagos o seguridad |

---

# 3. Técnicas Estáticas

## Definición

Las técnicas estáticas son métodos de aseguramiento de la calidad que se aplican **sin ejecutar el software**.

Permiten detectar defectos en etapas tempranas del ciclo de vida, revisando artefactos como:

- Requisitos.
- Modelos.
- Código.
- Manuales.

Su objetivo es identificar:

- Inconsistencias.
- Ambigüedades.
- Omisiones.

## Explicación sencilla

Una técnica estática es como revisar un texto antes de publicarlo.  
No se necesita “ponerlo a funcionar”; basta con leerlo, analizarlo y compararlo contra reglas o criterios de calidad.

Ejemplo simple:

> Si un requisito dice “el sistema debe responder rápido”, hay una ambigüedad porque no se define qué significa “rápido”: ¿1 segundo?, ¿5 segundos?, ¿10 segundos?

---

## Revisión de Documentación

Consiste en analizar sistemáticamente los artefactos generados durante el desarrollo de software para:

- Verificar cumplimiento de estándares de calidad: claridad, consistencia, completitud.
- Asegurar comprensión por los interesados.
- Detectar errores antes de la implementación o pruebas.

Se aplica a:

- Requisitos.
- Casos de uso.
- Diagramas.
- Código.
- Planes de prueba.
- Manuales.

## Explicación sencilla

La revisión de documentación evita que el equipo construya software sobre documentos mal escritos, incompletos o confusos.

Si un requisito está mal redactado, el programador puede entender una cosa, el cliente otra y el tester otra. Eso genera errores costosos.

---

## Revisión Informal

Método simple y flexible para encontrar errores en documentos.

- **Participantes:** Autor y uno o varios revisores.
- **Estructura:** Sin proceso formal ni roles definidos.
- **Objetivo:** Localizar defectos evidentes, inconsistencias o problemas de claridad.
- **Ejemplos:** Borradores de requisitos, diagramas preliminares.
- **Ventajas:** rápida, económica, adaptable.
- **Limitaciones:** puede omitir defectos sutiles, depende de la experiencia de los revisores.

## Explicación sencilla

Es una revisión rápida. Sirve para detectar errores visibles, pero no garantiza profundidad.

Ejemplo:

> Un compañero lee un documento de requisitos y señala que falta explicar qué pasa si el usuario ingresa una contraseña incorrecta.

---

## Revisión Técnica

Introduce mayor formalidad para validar la corrección técnica del documento.

- **Participantes:** Autor, expertos técnicos, arquitectos, testers, usuarios.
- **Estructura:** Reunión planificada con agenda y checklist.
- **Objetivo:** Evaluar viabilidad de implementación y alineación con estándares.
- **Ejemplos:** Validación de modelos de datos, revisión de casos de prueba.
- **Ventajas:** detección temprana de errores de diseño, fomenta la comunicación.
- **Limitaciones:** requiere coordinación y tiempo.

## Explicación sencilla

Es una revisión más seria que la informal. Aquí se reúnen personas con conocimiento técnico para revisar si lo propuesto se puede construir bien.

Ejemplo:

> Antes de programar una base de datos, el equipo revisa si el modelo de datos está completo y si soporta las consultas que el sistema necesita.

---

## Inspección Formal

Técnica más rigurosa y estructurada, basada en el método de Fagan.

- **Roles:** Moderador, autor, lector, escriba, inspectores.
- **Proceso:** Planificación, preparación individual, reunión de inspección, reparación, seguimiento.
- **Objetivo:** Detectar inconsistencias, omisiones, violaciones de estándares o errores de lógica.
- **Ventajas:** alta tasa de detección de defectos, proceso medible.
- **Limitaciones:** mayor esfuerzo y costo, requiere planificación cuidadosa.

## Explicación sencilla

Es la revisión más formal. Cada persona tiene un rol y se sigue un proceso definido. Sirve cuando el artefacto es importante o crítico.

Ejemplo:

> Revisar formalmente los requisitos de un sistema bancario antes de construirlo, porque un error puede causar pérdidas económicas o riesgos de seguridad.

---

## Walkthroughs

El autor guía a los participantes a través del documento, explicando su propósito y decisiones de diseño.

- **Participantes:** Autor, equipo de desarrollo, testers, usuarios clave.
- **Estructura:** Reunión planificada, el autor conduce la sesión y responde preguntas.
- **Objetivo:** Compartir conocimiento, identificar defectos, obtener retroalimentación.
- **Ejemplos:** Presentación de interfaces, revisión de flujos de casos de uso.
- **Ventajas:** aprendizaje colectivo, colaboración.
- **Limitaciones:** requiere moderación para evitar discusiones abiertas.

## Explicación sencilla

En un walkthrough, quien creó el documento lo explica paso a paso. Los demás escuchan, preguntan y detectan posibles problemas.

Ejemplo:

> El analista muestra el flujo de “crear cuenta bancaria” y el equipo nota que no se contempló qué hacer si el documento de identidad ya existe.

---

# 4. Técnicas Dinámicas

## Definición

Las técnicas dinámicas requieren la ejecución del programa para detectar defectos.

Buscan validar el comportamiento del software en tiempo de ejecución, verificando que cumpla los requisitos funcionales y condiciones de uso.

Se clasifican en:

- **Pruebas de Caja Negra:** Basadas en entradas y salidas, sin conocimiento del código.
- **Pruebas de Caja Blanca:** Diseñadas con conocimiento de la estructura interna del software.

## Explicación sencilla

Las técnicas dinámicas se aplican cuando el software se puede ejecutar.  
Aquí no basta con leer documentos: se usan datos reales o simulados para observar cómo responde el sistema.

Ejemplo:

> Ingresar edad 16 en un sistema bancario y verificar si muestra el mensaje: “Edad mínima 18 años”.

---

# 4.1. Pruebas de Caja Negra

Evalúan el software a partir de entradas, salidas y especificaciones, sin considerar su estructura interna.

- **Objetivo:** Verificar que el sistema responda correctamente a entradas válidas, rechace entradas inválidas y cumpla requisitos.
- **Ventajas:** Independencia del código, participación de usuarios, validación funcional.
- **Limitaciones:** No detecta errores internos, puede requerir muchas pruebas.
- **Técnicas principales:** Partición de Equivalencia, Análisis de Valores Límite, Tabla de Decisión.

## Explicación sencilla

En caja negra, el tester no necesita saber cómo está programado el sistema. Solo necesita conocer:

- Qué datos se ingresan.
- Qué resultado se espera.

Ejemplo:

```text
Entrada: edad = 16
Resultado esperado: Error: Edad mínima 18 años
```

---

# 4.2. Partición de Equivalencia

Divide el dominio de entrada en clases de datos equivalentes para probar un representante de cada clase.

- **Pasos:** Identificar rangos, dividir en clases válidas e inválidas, elegir casos representativos.
- **Ejemplo:** Edad válida 18–65 años: probar 30 válido, 10 inválido, 70 inválido.
- **Ventaja:** reduce casos de prueba manteniendo alta cobertura.

## Explicación sencilla

Si muchos datos se comportan igual, no es necesario probarlos todos. Basta con escoger un ejemplo representativo.

Ejemplo:

- Si las edades 18, 20, 30, 40 y 65 son válidas, se puede elegir una edad representativa como 30.
- Si las edades menores de 18 son inválidas, se puede elegir 16.
- Si las edades mayores de 65 son inválidas, se puede elegir 70.

---

## Ejemplo: Partición de Equivalencia

### Contexto

Un sistema bancario valida que la edad para abrir una cuenta esté entre 18 y 65 años.

### Regla de negocio

```text
Válido: 18 ≤ edad ≤ 65.
Inválido: fuera del rango o no numérico.
```

---

## Paso 1. Identificar el dominio de entrada

- **Entrada:** valor de la edad del cliente.
- **Tipo:** entero, esperado en el rango [18, 65].

---

## Paso 2. Determinar las clases de equivalencia

### Clases válidas

- **C1:** Edad dentro del rango válido (18–65).

### Clases inválidas

- **C2:** Edad menor que 18.
- **C3:** Edad mayor que 65.
- **C4:** Valor no numérico.

---

## Paso 3. Seleccionar casos representativos

- **C1:** edad = 30.
- **C2:** edad = 16.
- **C3:** edad = 70.
- **C4:** edad = “abc”.

---

## Paso 4. Construcción de casos de prueba

| Caso | Entrada (edad) | Clase | Resultado esperado |
|---|---:|---|---|
| T1 | 30 | C1 | Registro aceptado |
| T2 | 16 | C2 | Error: Edad mínima 18 años |
| T3 | 70 | C3 | Error: Edad máxima 65 años |
| T4 | “abc” | C4 | Error: Ingrese un valor numérico válido |

## Explicación sencilla

Aquí se prueba un caso por cada clase. No se prueban todas las edades posibles, sino un representante de cada grupo.

---

# 4.3. Análisis de Valores Límite

Se centra en los valores extremos de los rangos de entrada o salida.

- **Pasos:** Identificar límites, probar valores en el límite y cercanos.
- **Ejemplo:** Edad 18–65: probar 18 y 65, además de 17 y 66.
- **Ventaja:** detecta defectos en validaciones de rangos y comparaciones.

## Explicación sencilla

Muchos errores ocurren justo en los bordes de un rango.

Ejemplo:

- Si la edad mínima válida es 18, hay que probar 17, 18 y 19.
- Si la edad máxima válida es 65, hay que probar 64, 65 y 66.

Esto ayuda a descubrir errores como usar `<` en vez de `≤`.

---

## Ejemplo: Análisis de Valores Límite

### Contexto

El sistema bancario valida que la edad para abrir una cuenta esté entre 18 y 65 años.

### Regla de negocio

```text
Válido: 18 ≤ edad ≤ 65.
Inválido: fuera del rango o no numérico.
```

---

## Paso 1. Identificar los límites del dominio

- **Mínimo permitido:** 18.
- **Máximo permitido:** 65.

---

## Paso 2. Definir valores críticos

**Principio:** Los defectos suelen ocurrir en los bordes del rango.

### Valores a probar

- **Límite inferior:** 17, 18, 19.
- **Límite superior:** 64, 65, 66.

---

## Paso 3. Casos de prueba representativos

| Caso | Entrada (edad) | Descripción | Resultado esperado |
|---|---:|---|---|
| T1 | 17 | Debajo del mínimo | Error: Edad mínima 18 |
| T2 | 18 | En el mínimo | Registro aceptado |
| T3 | 19 | Encima del mínimo | Registro aceptado |
| T4 | 64 | Debajo del máximo | Registro aceptado |
| T5 | 65 | En el máximo | Registro aceptado |
| T6 | 66 | Encima del máximo | Error: Edad máxima 65 |

---

## Paso 4. Comparación con Partición de Equivalencia

- **Partición de Equivalencia:** basta un valor dentro de cada clase, por ejemplo 30.
- **Análisis de Valores Límite:** se prueban los bordes: 17, 18, 19, 64, 65, 66.
- Se detectan errores comunes en el manejo de límites, como uso de `<` en lugar de `≤`.

---

## Paso 5. Representación visual de la Partición

```text
Inválido          Válido                  Inválido
   17     18     19   ...   64     65     66
          |-------------------------|
              Válido (18–65)

Límites analizados: 17, 18, 19, 64, 65, 66.
```

**Figura 9:** Representación visual de la Partición.

## Explicación sencilla

La partición de equivalencia ayuda a escoger grupos de datos.  
El análisis de valores límite se concentra en los bordes de esos grupos, porque ahí aparecen muchos errores.

---

# 4.4. Tabla de Decisión

Útil cuando el sistema depende de combinaciones de condiciones lógicas.

- Representa condiciones y acciones en una tabla.
- Cada combinación de condiciones define una regla de prueba.
- **Ejemplo:** Préstamo bancario: historial positivo Sí/No, ingreso > $2000 Sí/No, acciones de aprobación.
- **Ventaja:** identifica casos omitidos y valida la lógica de negocio.

## Explicación sencilla

Una tabla de decisión sirve cuando el resultado del sistema depende de varias condiciones al mismo tiempo.

Ejemplo simple:

```text
Si el cliente tiene historial positivo y gana más de $2000 → aprobar préstamo.
Si no cumple una condición importante → rechazar o pedir revisión.
```

---

## Ejemplo: Tabla de Decisión

### Contexto

Sistema de cálculo de primas de seguro para automóviles.

### Prima base

```text
Prima base: 500 USD.
```

### Reglas

1. Conductor < 25 años, masculino y no casado: recargo +1500 USD.
2. Conductor casado o femenino: descuento −200 USD.
3. Conductor entre 45 y 65 años: descuento adicional −100 USD.

---

## Código del ejemplo

```python
1  def calcular_prima(edad, genero, casado):
2      prima = 500
3      if (edad < 25) and (genero == 'masculino') and (not casado):
4          prima += 1500
5      else:
6          if casado or (genero == 'femenino'):
7              prima -= 200
8          if (edad > 45) and (edad < 65):
9              prima -= 100
10     return prima
```

---

## Paso 1. Identificar condiciones y acciones

### Condiciones (C)

- **C1:** Edad < 25.
- **C2:** Género = Masculino.
- **C3:** Casado = Sí.
- **C4:** 45 ≤ Edad ≤ 65.

### Acciones (A)

- **A1:** Recargo +1500.
- **A2:** Descuento −200.
- **A3:** Descuento −100.

---

## Paso 2. Construcción de la tabla de decisión

| Reglas | C1 Edad < 25 | C2 M | C3 Casado | C4 45–65 | A1 +1500 | A2 −200 | A3 −100 |
|---|---|---|---|---|---|---|---|
| R1 | S | S | N | N | X |  |  |
| R2 | N | - | S | N |  | X |  |
| R3 | N | N | N | N |  | X |  |
| R4 | N | - | - | S |  |  | X |
| R5 | N | S | N | S |  |  | X |
| R6 | N | - | S | S |  | X | X |

**Convenciones:** S = Sí, N = No, - = No importa, X = acción aplicada.

---

## Paso 3. Selección de casos de prueba

| Caso | Edad | Género | Casado | Resultado esperado |
|---|---:|---|---|---|
| T1 | 22 | M | No | Prima = 500 + 1500 = 2000 |
| T2 | 30 | F | Sí | Prima = 500 − 200 = 300 |
| T3 | 30 | M | No | Prima = 500 − 200 = 300 |
| T4 | 50 | M | No | Prima = 500 − 100 = 400 |
| T5 | 50 | M | No | Prima = 500 − 100 = 400 |
| T6 | 60 | F | Sí | Prima = 500 − 200 − 100 = 200 |

## Explicación sencilla

La tabla de decisión toma todas las condiciones importantes y muestra qué acción se debe aplicar en cada combinación.

En este ejemplo, el sistema revisa edad, género y estado civil para calcular la prima final.

---

# 4.5. Pruebas de Caja Blanca

Se diseñan con conocimiento de la estructura interna del software.

- **Objetivo:** Asegurar que cada parte del código se ejecute al menos una vez y siga el flujo lógico previsto.
- **Ventajas:** Detecta defectos en caminos poco usados, garantiza cobertura de condiciones.
- **Limitaciones:** Requiere esfuerzo de diseño y conocimientos de programación.
- **Métricas comunes:** Cobertura de Sentencias, Cobertura de Decisiones, Cobertura de Condiciones.

## Explicación sencilla

En caja blanca, quien prueba sí conoce cómo está construido el código.  
Por eso puede diseñar pruebas para recorrer líneas, decisiones y condiciones internas.

Ejemplo:

> Si el código tiene un `if` y un `else`, las pruebas deben intentar ejecutar ambas ramas.

---

# 4.6. Cobertura de Sentencias

Verifica que cada instrucción o línea de código se ejecute al menos una vez.

- **Pasos:** Identificar todas las sentencias, diseñar pruebas que las recorran.
- **Ejemplo:** En un `if/else`, provocar la ejecución de ambas ramas.
- **Ventaja:** asegura la ejecución de todo el código.
- **Limitación:** no cubre todas las combinaciones lógicas.

## Explicación sencilla

La cobertura de sentencias pregunta:

> ¿Todas las líneas importantes del código se ejecutaron al menos una vez?

Esto es útil, pero no suficiente, porque una línea puede ejecutarse sin que todas las combinaciones lógicas hayan sido probadas.

---

## Ejemplo - Cobertura de Sentencias

### Código base

```python
1  def calcular_prima(edad, genero, casado):
2      prima = 500
3      if (edad < 25) and (genero == 'masculino') and (not casado):
4          prima += 1500
5      else:
6          if casado or (genero == 'femenino'):
7              prima -= 200
8          if (edad > 45) and (edad < 65):
9              prima -= 100
10     return prima
```

### Diagrama de flujo textual

```text
① función calcular_prima(edad, genero, casado)
② prima = 500
③ edad < 25 y genero == 'masculino' y no casado
   ├─ sí → ④ prima += 1500 → ⑩ retornar prima
   └─ no → ⑥ casado o genero == 'femenino'
             ├─ sí → ⑦ prima -= 200
             └─ continuar
          ⑧ edad > 45 y edad < 65
             ├─ sí → ⑨ prima -= 100
             └─ continuar
          ⑩ retornar prima
```

**Figura 10:** Diagrama de Flujo.  
**Figura 11:** Diagrama de Flujo.  
**Figura 12:** Diagrama de Flujo.

### Caso de Prueba #1

```python
TC1: calcular_prima(20, "masculino", False)
```

### Caso de Prueba #2

```python
TC2: calcular_prima(50, "femenino", True)
```

## Explicación sencilla

El primer caso ejecuta la rama del recargo.  
El segundo caso ejecuta la rama del descuento y también puede activar el descuento por edad.

Con estos casos se busca cubrir las sentencias principales del código.

---

# 4.7. Cobertura de Decisiones

Comprueba que cada posible resultado, verdadero o falso, de las decisiones se ejecute al menos una vez.

- **Pasos:** Identificar decisiones (`if`, `switch`), diseñar pruebas para ambos resultados.
- **Ejemplo:** Para `if (x > 10)`, casos con `x > 10` y `x ≤ 10`.
- **Ventaja:** detecta defectos en ramas no cubiertas por la cobertura de sentencias.

## Explicación sencilla

La cobertura de decisiones pregunta:

> ¿Cada decisión del código fue probada tanto en verdadero como en falso?

Ejemplo:

```python
if edad > 18:
    aceptar()
else:
    rechazar()
```

Para cubrir la decisión se necesita:

- Un caso donde `edad > 18` sea verdadero.
- Un caso donde `edad > 18` sea falso.

---

## Ejemplo - Cobertura de Decisiones

### Casos de prueba presentados

```python
TC1: calcular_prima(20, "masculino", False)
TC2: calcular_prima(50, "femenino", True)
TC3: calcular_prima(30, "masculino", False)
TC4: calcular_prima(30, "masculino", True)
TC5: calcular_prima(44, "masculino", False)
TC6: calcular_prima(60, "femenino", False)
```

**Figura 13:** Enter Caption.  
**Figura 14:** Enter Caption.  
**Figura 15:** Enter Caption.

## Explicación sencilla

Estos casos buscan que las decisiones del código se evalúen en distintas direcciones:

- Entrar o no al primer `if`.
- Aplicar o no el descuento por casado/femenino.
- Aplicar o no el descuento por edad entre 45 y 65.

---

# 4.8. Cobertura de Condiciones

Garantiza que cada condición elemental dentro de una expresión booleana sea evaluada como verdadera y falsa.

- **Pasos:** Descomponer cada decisión en condiciones simples, diseñar pruebas que cubran todos los valores.
- **Ejemplo:** En `if (A && B)`, probar A y B en verdadero y falso de manera controlada.
- **Ventaja:** cobertura más fina que la de decisiones.
- **Limitación:** requiere más casos de prueba para lograr cobertura completa.

## Explicación sencilla

Una decisión puede estar formada por varias condiciones.

Ejemplo:

```python
if (edad < 25) and (genero == 'masculino') and (not casado):
```

Aquí hay tres condiciones:

1. `edad < 25`
2. `genero == 'masculino'`
3. `not casado`

La cobertura de condiciones busca que cada una sea verdadera y falsa al menos una vez.

---

## Casos de Prueba para Cobertura de Condiciones

| Caso | edad | género | casado | C1: edad < 25 | C2: masc | C3: not casado | C4: casado | C5: fem | C6: edad > 45 | C7: edad < 65 |
|---|---:|---|---|---|---|---|---|---|---|---|
| 1 | 20 | masculino | False | True | True | True | False | False | False | True |
| 2 | 30 | femenino | True | False | False | False | True | True | False | True |
| 3 | 50 | masculino | False | False | True | True | False | False | True | True |
| 4 | 70 | femenino | False | False | False | True | False | True | True | False |
| 5 | 45 | masculino | True | False | True | False | True | False | False | True |
| 6 | 65 | femenino | False | False | False | True | False | True | True | False |

**Tabla 1:** Casos de prueba y evaluación de condiciones atómicas.

---

## Casos donde cada condición se evalúa como verdadera

| Condición | Casos donde se evalúa como True |
|---|---|
| C1: edad < 25 | Caso 1 |
| C2: género == ’masculino’ | Casos 1, 3, 5 |
| C3: not casado | Casos 1, 3, 4, 6 |
| C4: casado | Casos 2, 5 |
| C5: género == ’femenino’ | Casos 2, 4, 6 |
| C6: edad > 45 | Casos 3, 4, 6 |
| C7: edad < 65 | Casos 1, 2, 3, 5 |

**Tabla 2:** Casos donde cada condición se evalúa como verdadera.

---

## Casos donde cada condición se evalúa como falsa

| Condición | Casos donde se evalúa como False |
|---|---|
| C1: edad < 25 | Casos 2, 3, 4, 5, 6 |
| C2: género == ’masculino’ | Casos 2, 4, 6 |
| C3: not casado | Casos 2, 5 |
| C4: casado | Casos 1, 3, 4, 6 |
| C5: género == ’femenino’ | Casos 1, 3, 5 |
| C6: edad > 45 | Casos 1, 2, 5 |
| C7: edad < 65 | Casos 4, 6 |

**Tabla 3:** Casos donde cada condición se evalúa como falsa.

## Explicación sencilla

La cobertura de condiciones es más detallada que la cobertura de decisiones.  
No basta con que una decisión completa sea verdadera o falsa; se revisa cada pedazo lógico de la decisión.

---

# 5. Referencias y datos de contacto

## Referencias

**Referencias (1/1)**

El material contiene una diapositiva titulada **Referencias (1/1)**, sin listado visible de referencias bibliográficas en el texto extraído.

## Datos de contacto

**Albeiro Espinosa Bedoya, Ph.D. Ms.C.**  
Profesor Asociado  
**Email:** aespinos@unal.edu.co  
**Instagram:** @albeiroespinosabedoya  
Departamento de Ciencias de la Computación y de la Decisión, Facultad de Minas  
**Dirección:** Av. 80 #65-223, Bloque M8A, Of. 204  
**Teléfono:** +57 604 4255384

---

# Resumen final del tema

La verificación de software permite comprobar que los productos del desarrollo cumplen los requisitos especificados.

El proceso puede aplicarse a diferentes artefactos:

- Requisitos.
- Diseño.
- Código.
- Integración.
- Documentación.

Las técnicas se dividen principalmente en:

| Tipo | Idea central | Ejemplo |
|---|---|---|
| Técnicas estáticas | Revisar sin ejecutar el software | Revisión de requisitos, inspección formal, walkthrough |
| Técnicas dinámicas | Probar ejecutando el software | Caja negra, caja blanca |
| Caja negra | Probar entradas y salidas sin mirar el código | Partición de equivalencia, valores límite, tabla de decisión |
| Caja blanca | Probar conociendo la estructura interna del código | Cobertura de sentencias, decisiones y condiciones |

## Ruta de comprensión recomendada

```text
1. Entender qué es verificación.
2. Diferenciar técnicas estáticas y dinámicas.
3. Comprender caja negra.
4. Practicar partición de equivalencia.
5. Practicar valores límite.
6. Comprender tablas de decisión.
7. Comprender caja blanca.
8. Diferenciar cobertura de sentencias, decisiones y condiciones.
```

---

# Observaciones técnicas de calidad sobre el material

Estas observaciones no modifican la transcripción; sirven para alertar posibles puntos de revisión desde una mirada de calidad de software.

1. En el ejemplo de **Tabla de Decisión**, el caso **T3** aparece como:

   ```text
   Edad: 30, Género: M, Casado: No → Prima = 500 − 200 = 300
   ```

   Sin embargo, según las reglas y el código presentado, un conductor masculino, no casado y de 30 años no cumple la condición de descuento por “casado o femenino”. Por tanto, el resultado esperado podría requerir revisión.

2. En la tabla de selección de casos de prueba, **T4** y **T5** aparecen con los mismos datos:

   ```text
   Edad: 50, Género: M, Casado: No → Prima = 500 − 100 = 400
   ```

   Esto puede ser intencional para cubrir reglas similares, pero también podría ser una duplicación que conviene revisar.

3. En la identificación de condiciones se presenta:

   ```text
   C4: 45 ≤ Edad ≤ 65
   ```

   Pero el código usa:

   ```python
   if (edad > 45) and (edad < 65):
   ```

   Es decir, el código excluye 45 y 65, mientras que la condición escrita los incluye. Este punto también conviene validarlo.

---

# Cierre

El proceso de verificación es clave en calidad de software porque permite encontrar defectos antes y durante la construcción del sistema.  
Mientras más temprano se detecta un error, menos costoso suele ser corregirlo.
