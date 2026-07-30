# Casos de Prueba – Módulo Gestión de Rutas de Recolección

## WasteTrack – Aplicación de Gestión de Residuos Urbanos

**Versión:** 1.0

**Fecha:** 2026-06-24

**Identificador:** CasosPrueba-WT-GRR-v1.0

**Elaborado por:** Grupo 09 – Calidad de Software 2025-2

**Docente:** Albeiro Espinosa Bedoya, Ph.D., M.Sc.

**Referencia normativa:** ISO/IEC/IEEE 12207 – Proceso de Verificación de Software (7.2.4)

## Índice de casos de prueba

```text
ID        Técnica              Regla            Descripción breve
BN-PE- Partición de            RN-              Ruta completamente válida — caso
01        Equivalencia         01/02/03/04      nominal
BN-PE- Partición de            RN-01            Nombre < 5 chars (clase inválida IN-02)
02        Equivalencia
BN-PE- Partición de            RN-01            Nombre > 100 chars (clase inválida IN-
03        Equivalencia                          03)
BN-PE- Partición de            RN-02            Capacidad = 0 (clase inválida IN-06)
04        Equivalencia
BN-PE- Partición de            RN-02            Capacidad = 750 (clase inválida IN-07)
05        Equivalencia
BN-PE- Partición de            RN-03            Hora inicio = hora fin (clase inválida IN-
06        Equivalencia                          11)
BN-PE- Partición de            RN-04            Lista de días vacía (clase inválida IN-13)
07        Equivalencia
BN-PE- Partición de            RN-01            Nombre vacío
08        Equivalencia
BN-PE- Partición de            RN-02            Capacidad no numérica
09        Equivalencia
BN-PE- Partición de            RN-02            Capacidad decimal cuando debe ser
10        Equivalencia                          entera
BN-PE- Partición de            RN-03            Hora de inicio posterior a hora de fin
11        Equivalencia
BN-PE- Partición de            RN-04            Lista de días nula
12        Equivalencia
BN-PE- Partición de            RN-05            Zona inexistente
13        Equivalencia
```

```text
ID       Técnica               Regla      Descripción breve
BN-VL-   Análisis de Valores   RN-01      Nombre 4 chars — justo por debajo del
01       Límite                           mínimo
BN-VL-   Análisis de Valores   RN-01      Nombre 5 chars — mínimo permitido
02       Límite
BN-VL-   Análisis de Valores   RN-01      Nombre 100 chars — máximo
03       Límite                           permitido
BN-VL-   Análisis de Valores   RN-01      Nombre 101 chars — justo por encima
04       Límite                           del máximo
BN-VL-   Análisis de Valores   RN-02      Capacidad 0 — justo por debajo del
05       Límite                           mínimo
BN-VL-   Análisis de Valores   RN-02      Capacidad 1 — mínimo permitido
06       Límite
BN-VL-   Análisis de Valores   RN-02      Capacidad 500 — máximo permitido
07       Límite
BN-VL-   Análisis de Valores   RN-02      Capacidad 501 — justo por encima del
08       Límite                           máximo
BN-TD-   Tabla de Decisión     RN-05      Misma zona + mismo día + horario
01                                        solapado → rechazar
BN-TD-   Tabla de Decisión     RN-05      Misma zona + mismo día + horarios
02                                        contiguos → crear
BN-TD-   Tabla de Decisión     RN-05      Misma zona + distinto día → crear
03
BN-TD-   Tabla de Decisión     RN-05      Distinta zona → crear
04
CB-CS-   Cobertura de          RN-01/06   Camino exitoso — L01–L18 (False
01       Sentencias                       branches)
CB-CS-   Cobertura de          RN-01/02   Camino error validación — L01–L11
02       Sentencias                       (True branches)
CB-CS-   Cobertura de          RN-05      Camino solapamiento — L12–L15
03       Sentencias
CB-CD-   Cobertura de          RN-01      D1=True (nombre inválido) + D5=True
01       Decisiones
CB-CD-   Cobertura de          RN-01/02   D1=False + D2=True (capacidad
02       Decisiones                       inválida)
CB-CD-   Cobertura de          RN-02/03   D2=False + D3=True (horario inválido)
03       Decisiones
CB-CD-   Cobertura de          RN-03/04   D3=False + D4=True (sin días)
04       Decisiones
CB-CD-   Cobertura de          RN-05      D4=False + D5=False + D7=True
```

```text
ID       Técnica                 Regla              Descripción breve
05       Decisiones                                 (solapamiento)
CB-CD-   Cobertura de            RN-01/06           D7=False → camino exitoso completo
06       Decisiones
CB-CC-   Cobertura de            RN-01              C1a=True (nombre < 5), C1b=False
01       Condiciones
CB-CC-   Cobertura de            RN-01              C1a=False, C1b=True (nombre > 100)
02       Condiciones
CB-CC-   Cobertura de            RN-02              C2a=True (capacidad < 1), C2b=False
03       Condiciones
CB-CC-   Cobertura de            RN-02              C2a=False, C2b=True (capacidad > 500)
04       Condiciones
CB-CC-   Cobertura de            RN-03              C3=True (horaInicio = horaFin)
05       Condiciones
CB-CC-   Cobertura de            RN-01/04           Todas las condiciones de validación en
06       Condiciones                                False
```

## 1. Justificación del módulo seleccionado

### 1.1 Módulo elegido

Gestión de Rutas de Recolección (Administrador) Endpoint: POST /api/rutas — función crearRuta()

### 1.2 Criterios de selección

```text
Criterio de
complejidad                Evidencia cuantitativa
Mayor peso en FPA          30 FP equivalentes — máximo entre todos los módulos (Sección
                           5.2.1 del PMP)
Mayor Story Points         21 SP — valor más alto de todos los módulos (Sección 5.2.4 del
                           PMP)
Clasificación UCP          “Complejo” con 10+ transacciones — mayor peso unitario en
                           UUCW
Número de reglas de        6 reglas (validación de nombre, capacidad, horario, días,
negocio                    solapamiento y notificación)
Impacto transversal        Afecta módulo ciudadanos (notificaciones push), estadísticas en
                           tiempo real y disponibilidad del servicio
Trazabilidad               Requisito RF-04, asociado a TC-010 en la Matriz de Trazabilidad
                           (Apéndice A del PMP)
```

### 1.3 Descripción funcional del módulo

El módulo permite al Administrador de residuos crear, editar y activar/desactivar rutas de recolección urbana. Cada ruta agrupa: nombre identificador, zona geográfica, días de operación, horario de inicio y fin, y capacidad de carga del vehículo asignado. El sistema impone validaciones de campo y prohíbe el solapamiento de horarios entre rutas de la misma zona en los mismos días. Al crear o modificar una ruta exitosamente, el sistema envía notificaciones automáticas push a los ciudadanos registrados en la zona afectada (RN-06).

## 2. Reglas de negocio del módulo

```text
ID
regla Descripción                                                   Campo afectado
RN-01 El nombre de la ruta debe tener entre 5 y 100 caracteres      nombre
RN-02 La capacidad de carga debe ser un entero entre 1 kg y         capacidadKg
      500 kg
RN-03 La hora de inicio debe ser estrictamente anterior a la        horaInicio, horaFin
      hora de fin
RN-04 Se debe seleccionar al menos un día de operación de la        dias
      semana
RN-05 No puede haber solapamiento de horarios entre rutas de        zona, dias,
      la misma zona en los mismos días                              horaInicio, horaFin
RN-06 Al crear o modificar una ruta exitosamente se envía           zona
      notificación push a ciudadanos de la zona
```

## 3. Pseudocódigo del módulo (base para pruebas de caja blanca)

**Nota sobre la caja blanca:** el siguiente pseudocódigo representa el diseño lógico previsto para la función crearRuta(). Los porcentajes presentados en este documento corresponden a cobertura teórica del modelo. Cuando la implementación definitiva esté disponible, la trazabilidad deberá actualizarse con la ruta del archivo, números de línea, commit analizado y reporte de cobertura generado por la herramienta de pruebas. El siguiente pseudocódigo representa la lógica de la función de creación de ruta en el backend Node.js + Express de WasteTrack. Las líneas están numeradas y las decisiones etiquetadas para referenciarlas en los casos de prueba.

```text
FUNCIÓN crearRuta(nombre, zona, dias, horaInicio, horaFin, capacidadKg,
activa):

  L01:   errores ← []
  L02: SI (longitud(nombre) < 5 OR longitud(nombre) > 100):    ← D1 [C1a OR
C1b]
  L03:   agregar "Nombre inválido: debe tener entre 5 y 100 caracteres" a
errores

  L04:   SI (capacidadKg < 1 OR capacidadKg > 500):               ← D2 [C2a OR
C2b]
  L05:     agregar "Capacidad inválida: debe estar entre 1 y 500 kg" a errores

  L06:   SI (horaInicio >= horaFin):                             ← D3 [C3]
  L07:     agregar "Hora de inicio debe ser anterior a hora de fin" a errores

  L08:   SI (dias ESTÁ VACÍO O dias ES NULO):                      ← D4 [C4]
  L09:     agregar "Debe seleccionar al menos un día" a errores

  L10:   SI (longitud(errores) > 0):                               ← D5 [C5]
  L11:     RETORNAR { exito: false, errores: errores }

  L12:   rutasExistentes ← BD.obtenerRutasPorZona(zona, dias)

  L13:   tieneSolapamiento ← rutasExistentes CONTIENE alguna ruta r     ← D6
[C6]
                DONDE (r.horaInicio < horaFin AND r.horaFin > horaInicio)

  L14: SI (tieneSolapamiento):                                  ← D7 [C7]
  L15:   RETORNAR { exito: false, errores: ["Conflicto de horario en la
zona"] }

  L16: nuevaRuta ← BD.guardarRuta(nombre, zona, dias, horaInicio, horaFin,
capacidadKg, activa)
  L17: NotificacionService.enviarAZona(zona, "Nueva ruta: " + nombre)
  L18: RETORNAR { exito: true, ruta: nuevaRuta }

FIN FUNCIÓN
```

### Diagrama de flujo de decisiones

```text
L01: errores = []
     ↓
L02: D1: longitud(nombre) fuera de [5, 100]?
     ├─ Sí → L03: push error nombre
     └─ No → continuar
     ↓
L04: D2: capacidadKg fuera de [1, 500]?
     ├─ Sí → L05: push error capacidad
     └─ No → continuar
     ↓
L06: D3: horaInicio >= horaFin?
     ├─ Sí → L07: push error horario
     └─ No → continuar
     ↓
L08: D4: dias vacío o nulo?
     ├─ Sí → L09: push error días
     └─ No → continuar
     ↓
L10: D5: errores.length > 0?
     ├─ Sí → L11: RETURN { exito: false }   ✗ SALIDA ERROR VALIDACIÓN
     └─ No → continuar
     ↓
L12: rutasExistentes = BD.obtenerRutasPorZona(zona, dias)
     ↓
L13: D6: tieneSolapamiento = rutasExistentes.some(r => ...)
     ↓
L14: D7: tieneSolapamiento?
     ├─ Sí → L15: RETURN { exito: false }   ✗ SALIDA ERROR SOLAPAMIENTO
     └─ No → continuar
     ↓
L16: BD.guardarRuta(...)
L17: NotificacionService.enviarAZona(...)
L18: RETURN { exito: true }                 ✓ SALIDA ÉXITO
```

## 4. Pruebas de Caja Negra

Las pruebas de caja negra se diseñan desde la especificación funcional, sin conocimiento de la estructura interna del código. Se aplican tres técnicas: Partición de Equivalencia, Análisis de Valores Límite y Tabla de Decisión.

### 4.1 Partición de Equivalencia

### Clases de equivalencia identificadas

```text
                      ID
Campo                 clase     Tipo       Descripción           Valor representativo
nombre                VN-01     Válida     5 ≤ longitud ≤ 100    “Ruta Norte Centro” (17
                                                                 chars)
nombre                IN-02     Inválida longitud < 5            “Rt” (2 chars)
nombre                IN-03     Inválida longitud > 100          cadena de 101 chars
nombre                IN-04     Inválida cadena vacía            “”
capacidadKg           VN-05     Válida   1 ≤ capacidad ≤         250
                                         500
capacidadKg           IN-06     Inválida capacidad < 1           0
capacidadKg           IN-07     Inválida capacidad > 500         750
capacidadKg           IN-08     Inválida valor no entero         “abc”
```

```text
                  ID
Campo             clase      Tipo     Descripción         Valor representativo
horaInicio /      VN-09      Válida   horaInicio <        “06:00” – “14:00”
horaFin                               horaFin
horaInicio /      IN-10      Inválida horaInicio >        “14:00” – “06:00”
horaFin                               horaFin
horaInicio /      IN-11      Inválida horaInicio =        “08:00” – “08:00”
horaFin                               horaFin
dias              VN-12      Válida   al menos 1 día      [“lunes”]
dias              IN-13      Inválida lista vacía         []
```

### BN-PE-01

```text
Campo            Detalle
ID               BN-PE-01
Módulo           Gestión de Rutas de Recolección – crear ruta
Tipo de prueba   Caja Negra – Partición de Equivalencia
Objetivo         Verificar que una ruta con todos los datos en clases válidas se crea
                 exitosamente (VN-01, VN-05, VN-09, VN-12)
Trazabilidad     RF-04 / RN-01, RN-02, RN-03, RN-04, RN-06
Precondiciones   Administrador autenticado. Sin rutas en “Zona Norte” los días
                 indicados.
Datos de         nombre: “Ruta Norte Centro” · zona: “Zona Norte” · dias:
entrada          [“lunes”,“miercoles”] · horaInicio: “06:00” · horaFin: “14:00” ·
                 capacidadKg: 250 · activa: true
Pasos            1. Autenticarse como administrador. 2. Ir a Gestión de Rutas → Nueva
                 Ruta. 3. Ingresar todos los datos válidos. 4. Confirmar creación.
Resultado        HTTP 201. Respuesta: { exito: true, ruta: { id, nombre: "Ruta
esperado         Norte Centro", ... } }. Ruta registrada en BD. Notificación push
                 enviada a ciudadanos de “Zona Norte”.
Resultado        —
obtenido
Estado           Pendiente
```

### BN-PE-02

```text
Campo            Detalle
ID               BN-PE-02
Módulo           Gestión de Rutas de Recolección – crear ruta
```

```text
Campo              Detalle
Tipo de prueba     Caja Negra – Partición de Equivalencia
Objetivo           Verificar que nombre con longitud < 5 (clase IN-02) genera error de
                   validación
Trazabilidad       RF-04 / RN-01
Precondiciones     Administrador autenticado.
Datos de entrada   nombre: “Rt” (2 chars — clase IN-02) · resto de campos válidos
Pasos              1. Autenticarse. 2. Ingresar nombre “Rt” con demás campos válidos. 3.
                   Confirmar.
Resultado          HTTP 400. { exito: false, errores: ["Nombre inválido: debe
esperado           tener entre 5 y 100 caracteres"] }. Ruta NO registrada en BD.
Resultado          —
obtenido
Estado             Pendiente
```

### BN-PE-03

```text
Campo            Detalle
ID               BN-PE-03
Módulo           Gestión de Rutas de Recolección – crear ruta
Tipo de prueba   Caja Negra – Partición de Equivalencia
Objetivo         Verificar que nombre con longitud > 100 (clase IN-03) genera error de
                 validación
Trazabilidad     RF-04 / RN-01
Precondiciones   Administrador autenticado.
Datos de entrada nombre: “Ruta de recoleccion zona norte ampliada para el mes de
                 enero del año dos mil veintiseis turno manana” (101 chars — clase IN-
                 03) · resto válidos
Pasos            1. Autenticarse. 2. Ingresar nombre de 101 caracteres. 3. Confirmar.
Resultado        HTTP 400. { exito: false, errores: ["Nombre inválido: debe
esperado         tener entre 5 y 100 caracteres"] }. Ruta NO registrada.
Resultado        —
obtenido
Estado           Pendiente
```

### BN-PE-04

```text
Campo               Detalle
ID                  BN-PE-04
```

```text
Campo              Detalle
Módulo             Gestión de Rutas de Recolección – crear ruta
Tipo de prueba     Caja Negra – Partición de Equivalencia
Objetivo           Verificar que capacidad = 0 (clase IN-06) genera error de validación
Trazabilidad       RF-04 / RN-02
Precondiciones     Administrador autenticado.
Datos de entrada   nombre: “Ruta Sur” (válido) · capacidadKg: 0 (clase IN-06) · resto
                   válidos
Pasos              1. Autenticarse. 2. Ingresar capacidad = 0. 3. Confirmar.
Resultado          HTTP 400. { exito: false, errores: ["Capacidad inválida:
esperado           debe estar entre 1 y 500 kg"] }. Ruta NO registrada.
Resultado          —
obtenido
Estado             Pendiente
```

### BN-PE-05

```text
Campo              Detalle
ID                 BN-PE-05
Módulo             Gestión de Rutas de Recolección – crear ruta
Tipo de prueba     Caja Negra – Partición de Equivalencia
Objetivo           Verificar que capacidad = 750 (clase IN-07, > 500) genera error de
                   validación
Trazabilidad       RF-04 / RN-02
Precondiciones     Administrador autenticado.
Datos de entrada   nombre: “Ruta Sur” (válido) · capacidadKg: 750 (clase IN-07) · resto
                   válidos
Pasos              1. Autenticarse. 2. Ingresar capacidad = 750. 3. Confirmar.
Resultado          HTTP 400. { exito: false, errores: ["Capacidad inválida:
esperado           debe estar entre 1 y 500 kg"] }. Ruta NO registrada.
Resultado          —
obtenido
Estado             Pendiente
```

### BN-PE-06

```text
Campo              Detalle
ID                 BN-PE-06
```

```text
Campo              Detalle
Módulo             Gestión de Rutas de Recolección – crear ruta
Tipo de prueba     Caja Negra – Partición de Equivalencia
Objetivo           Verificar que hora inicio = hora fin (clase IN-11) genera error de
                   validación
Trazabilidad       RF-04 / RN-03
Precondiciones     Administrador autenticado.
Datos de entrada   nombre: “Ruta Sur” (válido) · capacidadKg: 200 (válido) · horaInicio:
                   “08:00” · horaFin: “08:00” (clase IN-11) · dias: [“martes”]
Pasos              1. Autenticarse. 2. Ingresar hora inicio = hora fin = “08:00”. 3.
                   Confirmar.
Resultado          HTTP 400. { exito: false, errores: ["Hora de inicio debe ser
esperado           anterior a hora de fin"] }. Ruta NO registrada.
Resultado          —
obtenido
Estado             Pendiente
```

### BN-PE-07

```text
Campo              Detalle
ID                 BN-PE-07
Módulo             Gestión de Rutas de Recolección – crear ruta
Tipo de prueba     Caja Negra – Partición de Equivalencia
Objetivo           Verificar que lista de días vacía (clase IN-13) genera error de
                   validación
Trazabilidad       RF-04 / RN-04
Precondiciones     Administrador autenticado.
Datos de entrada   nombre: “Ruta Sur” (válido) · capacidadKg: 200 · horaInicio: “06:00” ·
                   horaFin: “14:00” · dias: [] (clase IN-13)
Pasos              1. Autenticarse. 2. No seleccionar ningún día. 3. Confirmar.
Resultado          HTTP 400. { exito: false, errores: ["Debe seleccionar al
esperado           menos un día"] }. Ruta NO registrada.
Resultado          —
obtenido
Estado             Pendiente
```

### BN-PE-08

```text
Campo               Detalle
```

```text
Campo                Detalle
ID                   BN-PE-08
Módulo               Gestión de Rutas de Recolección – crear ruta
Tipo de prueba       Caja Negra – Partición de Equivalencia
Objetivo             Verificar el rechazo de un nombre vacío
Trazabilidad         RF-04 / RN-01
Precondiciones       Administrador autenticado.
Datos de entrada     nombre: “” · demás campos válidos
Pasos                1. Autenticarse. 2. Dejar el nombre vacío. 3. Confirmar.
Resultado            HTTP 400. Rechazo de la solicitud con mensaje de nombre inválido.
esperado             Ruta NO registrada.
Resultado            —
obtenido
Estado               Pendiente
```

### BN-PE-09

```text
Campo                 Detalle
ID                    BN-PE-09
Módulo                Gestión de Rutas de Recolección – crear ruta
Tipo de prueba        Caja Negra – Partición de Equivalencia
Objetivo              Verificar el rechazo de una capacidad no numérica
Trazabilidad          RF-04 / RN-02
Precondiciones        Administrador autenticado.
Datos de entrada      capacidadKg: “abc” · demás campos válidos
Pasos                 1. Autenticarse. 2. Ingresar “abc” como capacidad. 3. Confirmar.
Resultado esperado    HTTP 400. Rechazo por tipo de dato inválido. Ruta NO registrada.
Resultado obtenido    —
Estado                Pendiente
```

### BN-PE-10

```text
Campo                Detalle
ID                   BN-PE-10
Módulo               Gestión de Rutas de Recolección – crear ruta
Tipo de prueba       Caja Negra – Partición de Equivalencia
Objetivo             Verificar el rechazo de una capacidad decimal cuando la regla exige
```

```text
Campo              Detalle
                   un entero
Trazabilidad       RF-04 / RN-02
Precondiciones     Administrador autenticado.
Datos de entrada   capacidadKg: 25.5 · demás campos válidos
Pasos              1. Autenticarse. 2. Ingresar capacidad 25.5. 3. Confirmar.
Resultado          HTTP 400. Rechazo porque la capacidad debe ser un número entero.
esperado           Ruta NO registrada.
Resultado          —
obtenido
Estado             Pendiente
```

### BN-PE-11

```text
Campo              Detalle
ID                 BN-PE-11
Módulo             Gestión de Rutas de Recolección – crear ruta
Tipo de prueba     Caja Negra – Partición de Equivalencia
Objetivo           Verificar el rechazo cuando la hora inicial es posterior a la hora final
Trazabilidad       RF-04 / RN-03
Precondiciones     Administrador autenticado.
Datos de entrada   horaInicio: “14:00” · horaFin: “06:00” · demás campos válidos
Pasos              1. Autenticarse. 2. Ingresar el horario invertido. 3. Confirmar.
Resultado          HTTP 400. Rechazo porque la hora inicial debe ser anterior a la hora
esperado           final. Ruta NO registrada.
Resultado          —
obtenido
Estado             Pendiente
```

### BN-PE-12

```text
Campo               Detalle
ID                  BN-PE-12
Módulo              Gestión de Rutas de Recolección – crear ruta
Tipo de prueba      Caja Negra – Partición de Equivalencia
Objetivo            Verificar el rechazo de una lista de días nula
Trazabilidad        RF-04 / RN-04
Precondiciones      Administrador autenticado.
```

```text
Campo                   Detalle
Datos de entrada        dias: null · demás campos válidos
Pasos                   1. Autenticarse. 2. Enviar dias como null. 3. Confirmar.
Resultado               HTTP 400. Rechazo por ausencia de días de operación. Ruta NO
esperado                registrada.
Resultado               —
obtenido
Estado                  Pendiente
```

### BN-PE-13

```text
Campo                   Detalle
ID                      BN-PE-13
Módulo                  Gestión de Rutas de Recolección – crear ruta
Tipo de prueba          Caja Negra – Partición de Equivalencia
Objetivo                Verificar el rechazo de una zona inexistente
Trazabilidad            RF-04 / RN-05
Precondiciones          Administrador autenticado. La zona enviada no existe en el catálogo
                        de zonas.
Datos de entrada        zona: “Zona Inexistente” · demás campos válidos
Pasos                   1. Autenticarse. 2. Ingresar una zona no registrada. 3. Confirmar.
Resultado               HTTP 400. Rechazo porque la zona no está registrada. Ruta NO
esperado                registrada.
Resultado               —
obtenido
Estado                  Pendiente
```

### 4.2 Análisis de Valores Límite

### Límites identificados

```text
Campo             Límite inferior Límite superior
nombre (longitud) 5 caracteres    100 caracteres
capacidadKg       1 kg            500 kg
```

### Valores a probar por cada límite: por debajo, en el límite, por encima.

### BN-VL-01

```text
Campo                Detalle
ID                   BN-VL-01
Módulo               Gestión de Rutas de Recolección – crear ruta
Tipo de prueba       Caja Negra – Análisis de Valores Límite
Objetivo             Verificar rechazo de nombre con longitud 4 (justo por debajo del
                     mínimo de 5)
Trazabilidad         RF-04 / RN-01
Precondiciones       Administrador autenticado.
Datos de entrada     nombre: “Ruta” (4 chars) · resto de campos válidos
Pasos                1. Autenticarse. 2. Ingresar nombre de 4 caracteres. 3. Confirmar.
Resultado            HTTP 400. Error: “Nombre inválido: debe tener entre 5 y 100
esperado             caracteres”.
Resultado            —
obtenido
Estado               Pendiente
```

### BN-VL-02

```text
Campo                Detalle
ID                   BN-VL-02
Módulo               Gestión de Rutas de Recolección – crear ruta
Tipo de prueba       Caja Negra – Análisis de Valores Límite
Objetivo             Verificar aceptación de nombre con longitud exactamente igual al
                     mínimo (5 chars)
Trazabilidad         RF-04 / RN-01
Precondiciones       Administrador autenticado. Sin rutas en conflicto.
Datos de entrada     nombre: “RutaN” (exactamente 5 chars) · resto válidos
Pasos                1. Autenticarse. 2. Ingresar nombre de 5 caracteres. 3. Confirmar.
Resultado            HTTP 201. Ruta creada exitosamente. El nombre de 5 caracteres es
esperado             aceptado.
Resultado            —
obtenido
Estado               Pendiente
```

### BN-VL-03

```text
Campo              Detalle
ID                 BN-VL-03
```

```text
Campo              Detalle
Módulo             Gestión de Rutas de Recolección – crear ruta
Tipo de prueba     Caja Negra – Análisis de Valores Límite
Objetivo           Verificar aceptación de nombre con longitud exactamente igual al
                   máximo (100 chars)
Trazabilidad       RF-04 / RN-01
Precondiciones     Administrador autenticado. Sin rutas en conflicto.
Datos de           nombre: “RutaNorteZonaUnoExtendidaParaOperacionesDeLunes
entrada            aViernesdeTurnoCompleto2026Municipio” + relleno hasta 100 chars ·
                   resto válidos
Pasos              1. Autenticarse. 2. Ingresar nombre de exactamente 100 caracteres. 3.
                   Confirmar.
Resultado          HTTP 201. Ruta creada exitosamente. El nombre de 100 caracteres es
esperado           aceptado.
Resultado          —
obtenido
Estado             Pendiente
```

### BN-VL-04

```text
Campo                 Detalle
ID                    BN-VL-04
Módulo                Gestión de Rutas de Recolección – crear ruta
Tipo de prueba        Caja Negra – Análisis de Valores Límite
Objetivo              Verificar rechazo de nombre con longitud 101 (justo por encima del
                      máximo)
Trazabilidad          RF-04 / RN-01
Precondiciones        Administrador autenticado.
Datos de entrada      nombre: cadena de exactamente 101 caracteres alfanuméricos ·
                      resto válidos
Pasos                 1. Autenticarse. 2. Ingresar nombre de 101 caracteres. 3. Confirmar.
Resultado             HTTP 400. Error: “Nombre inválido: debe tener entre 5 y 100
esperado              caracteres”.
Resultado             —
obtenido
Estado                Pendiente
```

### BN-VL-05

```text
Campo                Detalle
ID                   BN-VL-05
Módulo               Gestión de Rutas de Recolección – crear ruta
Tipo de prueba       Caja Negra – Análisis de Valores Límite
Objetivo             Verificar rechazo de capacidad = 0 (justo por debajo del mínimo de
                     1)
Trazabilidad         RF-04 / RN-02
Precondiciones       Administrador autenticado.
Datos de entrada     nombre: “Ruta Este” (válido) · capacidadKg: 0 · resto válidos
Pasos                1. Autenticarse. 2. Ingresar capacidad = 0. 3. Confirmar.
Resultado            HTTP 400. Error: “Capacidad inválida: debe estar entre 1 y 500 kg”.
esperado
Resultado obtenido —
Estado             Pendiente
```

### BN-VL-06

```text
Campo                  Detalle
ID                     BN-VL-06
Módulo                 Gestión de Rutas de Recolección – crear ruta
Tipo de prueba         Caja Negra – Análisis de Valores Límite
Objetivo               Verificar aceptación de capacidad = 1 (mínimo permitido)
Trazabilidad           RF-04 / RN-02
Precondiciones         Administrador autenticado. Sin rutas en conflicto.
Datos de entrada       nombre: “Ruta Este” (válido) · capacidadKg: 1 · resto válidos
Pasos                  1. Autenticarse. 2. Ingresar capacidad = 1. 3. Confirmar.
Resultado esperado     HTTP 201. Ruta creada exitosamente con capacidad = 1 kg.
Resultado obtenido     —
Estado                 Pendiente
```

### BN-VL-07

```text
Campo                 Detalle
ID                    BN-VL-07
Módulo                Gestión de Rutas de Recolección – crear ruta
Tipo de prueba        Caja Negra – Análisis de Valores Límite
Objetivo              Verificar aceptación de capacidad = 500 (máximo permitido)
```

```text
Campo                     Detalle
Trazabilidad              RF-04 / RN-02
Precondiciones            Administrador autenticado. Sin rutas en conflicto.
Datos de entrada          nombre: “Ruta Este” (válido) · capacidadKg: 500 · resto válidos
Pasos                     1. Autenticarse. 2. Ingresar capacidad = 500. 3. Confirmar.
Resultado esperado        HTTP 201. Ruta creada exitosamente con capacidad = 500 kg.
Resultado obtenido        —
Estado                    Pendiente
```

### BN-VL-08

```text
Campo                   Detalle
ID                      BN-VL-08
Módulo                  Gestión de Rutas de Recolección – crear ruta
Tipo de prueba          Caja Negra – Análisis de Valores Límite
Objetivo                Verificar rechazo de capacidad = 501 (justo por encima del
                        máximo)
Trazabilidad            RF-04 / RN-02
Precondiciones          Administrador autenticado.
Datos de entrada        nombre: “Ruta Este” (válido) · capacidadKg: 501 · resto válidos
Pasos                   1. Autenticarse. 2. Ingresar capacidad = 501. 3. Confirmar.
Resultado               HTTP 400. Error: “Capacidad inválida: debe estar entre 1 y 500 kg”.
esperado
Resultado obtenido      —
Estado                  Pendiente
```

### 4.3 Tabla de Decisión (Conflicto de horarios entre rutas)

### Condiciones evaluadas

```text
ID   Condición
C1   ¿La nueva ruta opera en la misma zona geográfica que una ruta existente?
C2   ¿La nueva ruta opera al menos un mismo día que la ruta existente?
C3   ¿Los horarios de ambas rutas se solapan? (nueva.inicio < existente.fin AND
     nueva.fin > existente.inicio)
```

### Acciones posibles

```text
ID   Acción
```

ID Acción A1 Crear ruta exitosamente (HTTP 201) A2 Rechazar por conflicto de horario (HTTP 409)

### Tabla de decisión

```text
Regla   C1 Misma zona   C2 Mismo día      C3 Horario solapado       Acción
R1      Sí              Sí                Sí                        A2 – Rechazar
R2      Sí              Sí                No                        A1 – Crear
R3      Sí              No                — (irrelevante)           A1 – Crear
R4      No              — (irrelevante)   — (irrelevante)           A1 – Crear
```

### BN-TD-01

```text
Campo            Detalle
ID               BN-TD-01
Módulo           Gestión de Rutas de Recolección – crear ruta
Tipo de prueba   Caja Negra – Tabla de Decisión
Objetivo         Verificar rechazo cuando misma zona + mismo día + horario solapado
                 (Regla R1)
Trazabilidad     RF-04 / RN-05
Precondiciones   Existe “Ruta A” en “Zona Norte”, dias: [“lunes”], horaInicio: “06:00”,
                 horaFin: “12:00”. Administrador autenticado.
Datos de entrada nombre: “Ruta B” · zona: “Zona Norte” (=C1) · dias: [“lunes”] (=C2) ·
                 horaInicio: “08:00” · horaFin: “14:00” (solapado con 06:00–12:00 =C3)
                 · capacidadKg: 200
Pasos            1. Autenticarse. 2. Intentar crear “Ruta B” con los datos indicados. 3.
                 Confirmar.
Resultado        HTTP 409. { exito: false, errores: ["Conflicto de horario en
esperado         la zona seleccionada"] }. “Ruta B” NO registrada.
Resultado        —
obtenido
Estado           Pendiente
```

### BN-TD-02

```text
Campo                Detalle
ID                   BN-TD-02
Módulo               Gestión de Rutas de Recolección – crear ruta
```

```text
Campo              Detalle
Tipo de prueba     Caja Negra – Tabla de Decisión
Objetivo           Verificar creación exitosa cuando misma zona + mismo día pero
                   horarios NO solapados (Regla R2)
Trazabilidad       RF-04 / RN-05
Precondiciones     Existe “Ruta A” en “Zona Norte”, dias: [“lunes”], horaInicio: “06:00”,
                   horaFin: “10:00”.
Datos de entrada   nombre: “Ruta B” · zona: “Zona Norte” · dias: [“lunes”] · horaInicio:
                   “10:00” · horaFin: “18:00” (contiguo, sin solapamiento) · capacidadKg:
                   300
Pasos              1. Autenticarse. 2. Crear “Ruta B” con horario contiguo al de “Ruta A”.
                   3. Confirmar.
Resultado          HTTP 201. “Ruta B” creada. Los horarios son contiguos (10:00 = fin de
esperado           Ruta A), no solapados.
Resultado          —
obtenido
Estado             Pendiente
```

### BN-TD-03

```text
Campo              Detalle
ID                 BN-TD-03
Módulo             Gestión de Rutas de Recolección – crear ruta
Tipo de prueba     Caja Negra – Tabla de Decisión
Objetivo           Verificar creación exitosa cuando misma zona pero distinto día (Regla
                   R3)
Trazabilidad       RF-04 / RN-05
Precondiciones     Existe “Ruta A” en “Zona Norte”, dias: [“lunes”], horaInicio: “06:00”,
                   horaFin: “14:00”.
Datos de entrada   nombre: “Ruta C” · zona: “Zona Norte” · dias: [“martes”] · horaInicio:
                   “06:00” · horaFin: “14:00” · capacidadKg: 250
Pasos              1. Autenticarse. 2. Crear “Ruta C” para martes. 3. Confirmar.
Resultado          HTTP 201. “Ruta C” creada. Sin conflicto: distinto día de operación.
esperado
Resultado          —
obtenido
Estado             Pendiente
```

### BN-TD-04

```text
Campo                Detalle
ID                   BN-TD-04
Módulo               Gestión de Rutas de Recolección – crear ruta
Tipo de prueba       Caja Negra – Tabla de Decisión
Objetivo             Verificar creación exitosa cuando distinta zona aunque mismo día y
                     mismo horario (Regla R4)
Trazabilidad         RF-04 / RN-05
Precondiciones       Existe “Ruta A” en “Zona Norte”, dias: [“lunes”], horaInicio: “06:00”,
                     horaFin: “14:00”.
Datos de entrada     nombre: “Ruta D” · zona: “Zona Sur” (distinta) · dias: [“lunes”] ·
                     horaInicio: “06:00” · horaFin: “14:00” · capacidadKg: 200
Pasos                1. Autenticarse. 2. Crear “Ruta D” en “Zona Sur”. 3. Confirmar.
Resultado            HTTP 201. “Ruta D” creada. Sin conflicto: zona diferente.
esperado
Resultado            —
obtenido
Estado               Pendiente
```

## 5. Pruebas de Caja Blanca

Las pruebas de caja blanca se diseñan con conocimiento de la estructura interna del pseudocódigo (Sección 3). Se aplican tres niveles de cobertura: Sentencias, Decisiones y Condiciones.

### 5.1 Cobertura de Sentencias

**Objetivo:** Ejecutar al menos una vez cada línea de código (L01–L18).

### Análisis de cobertura requerida

Rango de

```text
líneas           Condición para ejecutarlas
L01–L09          Cualquier entrada con al menos un campo inválido activa los push
                 correspondientes
L10–L11          Al menos un error acumulado en el array
L12–L15          Todos los campos válidos Y solapamiento existente
L16–L18          Todos los campos válidos Y sin solapamiento (camino exitoso)
```

### CB-CS-01

```text
Campo            Detalle
ID               CB-CS-01
Módulo           Gestión de Rutas – crearRuta()
Tipo de prueba   Caja Blanca – Cobertura de Sentencias
Objetivo         Ejecutar el camino exitoso: todas las sentencias L01, L02(No), L04(No),
                 L06(No), L08(No), L10(No), L12, L13, L14(No), L16, L17, L18
Trazabilidad     RF-04 / RN-01 a RN-06
Precondiciones   BD limpia: sin rutas en “Zona Sur”. Administrador autenticado.
Datos de         nombre: “Ruta Sur Centro” (15 chars) · zona: “Zona Sur” · dias:
entrada          [“miercoles”,“viernes”] · horaInicio: “07:00” · horaFin: “15:00” ·
                 capacidadKg: 300 · activa: true
Pasos            1. Invocar crearRuta("Ruta Sur Centro","Zona
                 Sur",["miercoles","viernes"],"07:00","15:00",300,true). 2.
                 Verificar respuesta. 3. Verificar registro en BD. 4. Verificar envío de
                 notificación a “Zona Sur”.
Líneas           L01, L02(false), L04(false), L06(false), L08(false), L10(false), L12, L13,
cubiertas        L14(false), L16, L17, L18
Resultado        { exito: true, ruta: { id: X, nombre: "Ruta Sur Centro", ...
esperado         } }. Notificación push enviada a ciudadanos de “Zona Sur”.
Resultado        —
obtenido
Estado           Pendiente
```

### CB-CS-02

```text
Campo            Detalle
ID               CB-CS-02
Módulo           Gestión de Rutas – crearRuta()
Tipo de prueba   Caja Blanca – Cobertura de Sentencias
Objetivo         Ejecutar el camino de error de validación: L01, L02(Sí→L03),
                 L04(Sí→L05), L06(No), L08(No), L10(Sı́→L11)
Trazabilidad     RF-04 / RN-01, RN-02
Precondiciones   Administrador autenticado.
Datos de         nombre: “Rt” (2 chars — inválido) · zona: “Zona Norte” · dias: [“lunes”] ·
entrada          horaInicio: “06:00” · horaFin: “14:00” · capacidadKg: 0 (inválido)
Pasos            1. Invocar crearRuta("Rt","Zona
                 Norte",["lunes"],"06:00","14:00",0,true). 2. Verificar respuesta.
Líneas           L01, L02(true→L03), L04(true→L05), L06(false), L08(false),
cubiertas        L10(true→L11)
```

```text
Campo              Detalle
Resultado          { exito: false, errores: ["Nombre inválido: debe tener entre
esperado           5 y 100 caracteres", "Capacidad inválida: debe estar entre 1
                   y 500 kg"] }. Sin escritura en BD.
Resultado          —
obtenido
Estado             Pendiente
```

### CB-CS-03

```text
Campo            Detalle
ID               CB-CS-03
Módulo           Gestión de Rutas – crearRuta()
Tipo de prueba   Caja Blanca – Cobertura de Sentencias
Objetivo         Ejecutar el camino de error por solapamiento: L01–L10(No), L12, L13,
                 L14(Sí→L15)
Trazabilidad     RF-04 / RN-05
Precondiciones BD tiene “Ruta Existente” en “Zona Norte”, dias: [“lunes”], horaInicio:
                 “06:00”, horaFin: “12:00”. Administrador autenticado.
Datos de         nombre: “Ruta Nueva” (válido) · zona: “Zona Norte” · dias: [“lunes”] ·
entrada          horaInicio: “09:00” · horaFin: “15:00” (se solapa 09:00–12:00) ·
                 capacidadKg: 200
Pasos            1. Invocar crearRuta("Ruta Nueva","Zona
                 Norte",["lunes"],"09:00","15:00",200,true). 2. Verificar
                 respuesta.
Líneas cubiertas L01, L02(false), L04(false), L06(false), L08(false), L10(false), L12, L13,
                 L14(true→L15)
Resultado        { exito: false, errores: ["Conflicto de horario en la zona
esperado         seleccionada"] }. Sin escritura en BD.
Resultado        —
obtenido
Estado           Pendiente
```

Cobertura teórica de sentencias prevista con CB-CS-01 + CB-CS-02 + CB-CS-03: 100 % (líneas L01–L18). Esta cobertura deberá confirmarse mediante la ejecución de las pruebas sobre la implementación definitiva.

### 5.2 Cobertura de Decisiones

**Objetivo:** Cada decisión D1–D7 debe evaluarse como verdadera Y como falsa en al menos un caso.

### Mapeo de decisiones a pruebas

```text
Decisión   Expresión                    True en    False en
D1         nombre fuera de [5,100]      CB-CD-01   CB-CD-02
D2         capacidad fuera de [1,500]   CB-CD-02   CB-CD-03
D3         horaInicio ≥ horaFin         CB-CD-03   CB-CD-04
D4         dias vacío/nulo              CB-CD-04   CB-CD-05
D5         errores.length > 0           CB-CD-01   CB-CD-05
D7         tieneSolapamiento            CB-CD-05   CB-CD-06
```

### CB-CD-01

```text
Campo                  Detalle
ID                     CB-CD-01
Módulo                 Gestión de Rutas – crearRuta()
Tipo de prueba         Caja Blanca – Cobertura de Decisiones
Objetivo               Forzar D1=True (nombre inválido) y D5=True (retorno temprano
                       por errores)
Trazabilidad           RF-04 / RN-01
Precondiciones         Administrador autenticado.
Datos de entrada       nombre: “Rt” (2 chars) · capacidadKg: 200 (válido) · horaInicio:
                       “06:00” · horaFin: “14:00” · dias: [“lunes”]
Pasos                  1. Invocar función con nombre de 2 caracteres y demás campos
                       válidos.
Decisiones             D1=True (L02 → rama Sı́ → L03). D5=True (L10 → rama Sı́ → L11).
verificadas
Resultado              { exito: false, errores: ["Nombre inválido..."] }. No se
esperado               alcanza L12.
Resultado              —
obtenido
Estado                 Pendiente
```

### CB-CD-02

```text
Campo                 Detalle
```

```text
Campo              Detalle
ID                 CB-CD-02
Módulo             Gestión de Rutas – crearRuta()
Tipo de prueba     Caja Blanca – Cobertura de Decisiones
Objetivo           Forzar D1=False (nombre válido) y D2=True (capacidad inválida)
Trazabilidad       RF-04 / RN-01, RN-02
Precondiciones     Administrador autenticado.
Datos de entrada   nombre: “Ruta Norte” (10 chars — válido) · capacidadKg: 600
                   (inválido) · horaInicio: “06:00” · horaFin: “14:00” · dias: [“martes”]
Pasos              1. Invocar función con nombre válido y capacidad = 600.
Decisiones         D1=False (L02 no toma rama error). D2=True (L04 → L05).
verificadas
Resultado          { exito: false, errores: ["Capacidad inválida..."] }.
esperado
Resultado          —
obtenido
Estado             Pendiente
```

### CB-CD-03

```text
Campo              Detalle
ID                 CB-CD-03
Módulo             Gestión de Rutas – crearRuta()
Tipo de prueba     Caja Blanca – Cobertura de Decisiones
Objetivo           Forzar D2=False (capacidad válida) y D3=True (horario inválido:
                   inicio > fin)
Trazabilidad       RF-04 / RN-02, RN-03
Precondiciones     Administrador autenticado.
Datos de entrada   nombre: “Ruta Norte” (válido) · capacidadKg: 250 (válido) ·
                   horaInicio: “14:00” · horaFin: “06:00” (inválido) · dias: [“lunes”]
Pasos              1. Invocar función con horario invertido.
Decisiones         D2=False. D3=True (L06 → L07).
verificadas
Resultado          { exito: false, errores: ["Hora de inicio debe ser
esperado           anterior a hora de fin"] }.
Resultado          —
obtenido
Estado             Pendiente
```

### CB-CD-04

```text
Campo              Detalle
ID                 CB-CD-04
Módulo             Gestión de Rutas – crearRuta()
Tipo de prueba     Caja Blanca – Cobertura de Decisiones
Objetivo           Forzar D3=False (horario válido) y D4=True (sin días seleccionados)
Trazabilidad       RF-04 / RN-03, RN-04
Precondiciones     Administrador autenticado.
Datos de entrada   nombre: “Ruta Norte” (válido) · capacidadKg: 250 (válido) ·
                   horaInicio: “06:00” · horaFin: “14:00” (válido) · dias: [] (inválido)
Pasos              1. Invocar función con lista de días vacía.
Decisiones         D3=False (horario ok). D4=True (L08 → L09). D5=True (L10 → L11).
verificadas
Resultado          { exito: false, errores: ["Debe seleccionar al menos un
esperado           día"] }.
Resultado          —
obtenido
Estado             Pendiente
```

### CB-CD-05

```text
Campo              Detalle
ID                 CB-CD-05
Módulo             Gestión de Rutas – crearRuta()
Tipo de prueba     Caja Blanca – Cobertura de Decisiones
Objetivo           Forzar D4=False (días válidos), D5=False (sin errores de validación),
                   D7=True (solapamiento detectado)
Trazabilidad       RF-04 / RN-05
Precondiciones     Existe “Ruta A” en “Zona Este”, dias: [“jueves”], horaInicio: “08:00”,
                   horaFin: “16:00”. Administrador autenticado.
Datos de entrada   nombre: “Ruta B” (válido) · zona: “Zona Este” · dias: [“jueves”] ·
                   horaInicio: “10:00” · horaFin: “18:00” (solapa con 08:00–16:00) ·
                   capacidadKg: 200
Pasos              1. Invocar función con datos válidos pero con solapamiento.
Decisiones         D1=F, D2=F, D3=F, D4=F, D5=F (llega a L12). D7=True (L14 → L15).
verificadas
Resultado          { exito: false, errores: ["Conflicto de horario en la zona
esperado           seleccionada"] }.
```

```text
Campo                Detalle
Resultado            —
obtenido
Estado               Pendiente
```

### CB-CD-06

```text
Campo                Detalle
ID                   CB-CD-06
Módulo               Gestión de Rutas – crearRuta()
Tipo de prueba       Caja Blanca – Cobertura de Decisiones
Objetivo             Forzar D7=False (sin solapamiento) → ejecució n completa del
                     camino exitoso L16–L18
Trazabilidad         RF-04 / RN-01 a RN-06
Precondiciones       BD limpia en “Zona Oeste”. Administrador autenticado.
Datos de entrada     nombre: “Ruta Oeste” (válido) · zona: “Zona Oeste” · dias: [“sabado”] ·
                     horaInicio: “06:00” · horaFin: “12:00” · capacidadKg: 150 · activa:
                     true
Pasos                1. Invocar función con datos completamente válidos. 2. Verificar BD y
                     notificación.
Decisiones           D1=F, D2=F, D3=F, D4=F, D5=F, D7=F → L16, L17, L18 ejecutados.
verificadas
Resultado            { exito: true, ruta: { id: X, nombre: "Ruta Oeste", ... }
esperado             }. Notificación enviada a “Zona Oeste”.
Resultado            —
obtenido
Estado               Pendiente
```

**Cobertura teórica de decisiones prevista:** 100 % — D1–D7 con valor True y False. El porcentaje real deberá confirmarse mediante ejecución sobre el código fuente.

### 5.3 Cobertura de Condiciones

**Objetivo:** Cada condición individual dentro de cada decisión compuesta toma valor True Y False de forma independiente.

### Condiciones identificadas en el pseudocódigo

```text
ID
cond    Decisión Expresión individual                   True cuando        False cuando
C1a     D1       longitud(nombre) < 5                   nombre de 2        nombre de 10
```

```text
ID
cond   Decisión Expresión individual                   True cuando        False cuando
                                                       chars              chars
C1b    D1          longitud(nombre) > 100              nombre de 101      nombre de 10
                                                       chars              chars
C2a    D2          capacidadKg < 1                     capacidad = -5     capacidad =
                                                                          200
C2b    D2          capacidadKg > 500                   capacidad = 750    capacidad =
                                                                          200
C3     D3          horaInicio >= horaFin               “08:00” >=         “06:00” <
                                                       “08:00”            “14:00”
C4     D4          dias vacío o nulo                   dias = []          dias = [“lunes”]
C6     D6/D7       r.horaInicio < horaFin AND          solapamiento       sin
                   r.horaFin > horaInicio              real               solapamiento
```

### CB-CC-01

```text
Campo                   Detalle
ID                      CB-CC-01
Módulo                  Gestión de Rutas – crearRuta()
Tipo de prueba          Caja Blanca – Cobertura de Condiciones
Objetivo                Forzar C1a=True (nombre.length < 5) con C1b=False; D1=True
                        activado por C1a
Trazabilidad            RF-04 / RN-01
Precondiciones          Administrador autenticado.
Datos de entrada        nombre: “Rt” (2 chars: C1a=True, C1b=False) · resto de campos
                        válidos
Pasos                   1. Invocar función con nombre de 2 caracteres. 2. Verificar error.
Condiciones             C1a=True (2 < 5), C1b=False (2 no > 100) → D1=True
verificadas
Resultado esperado      Error: “Nombre inválido: debe tener entre 5 y 100 caracteres”.
Resultado obtenido      —
Estado                  Pendiente
```

### CB-CC-02

```text
Campo                   Detalle
ID                      CB-CC-02
Módulo                  Gestión de Rutas – crearRuta()
```

```text
Campo                Detalle
Tipo de prueba       Caja Blanca – Cobertura de Condiciones
Objetivo             Forzar C1a=False y C1b=True (nombre.length > 100); D1=True
                     activado por C1b
Trazabilidad         RF-04 / RN-01
Precondiciones       Administrador autenticado.
Datos de entrada     nombre: cadena de 101 chars (C1a=False: 101 no < 5; C1b=True:
                     101 > 100) · resto válidos
Pasos                1. Invocar función con nombre de 101 caracteres. 2. Verificar
                     error.
Condiciones          C1a=False, C1b=True → D1=True
verificadas
Resultado esperado   Error: “Nombre inválido: debe tener entre 5 y 100 caracteres”.
Resultado obtenido   —
Estado               Pendiente
```

### CB-CC-03

```text
Campo                Detalle
ID                   CB-CC-03
Módulo               Gestión de Rutas – crearRuta()
Tipo de prueba       Caja Blanca – Cobertura de Condiciones
Objetivo             Forzar C2a=True (capacidadKg < 1) con C2b=False; D2=True
                     activado por C2a
Trazabilidad         RF-04 / RN-02
Precondiciones       Administrador autenticado.
Datos de entrada     nombre: “Ruta X” (válido) · capacidadKg: -5 (C2a=True: -5 < 1;
                     C2b=False: -5 no > 500) · resto válidos
Pasos                1. Invocar función con capacidad = -5. 2. Verificar error.
Condiciones          C2a=True (-5 < 1), C2b=False → D2=True
verificadas
Resultado esperado   Error: “Capacidad inválida: debe estar entre 1 y 500 kg”.
Resultado obtenido   —
Estado               Pendiente
```

### CB-CC-04

```text
Campo                Detalle
```

```text
Campo                Detalle
ID                   CB-CC-04
Módulo               Gestión de Rutas – crearRuta()
Tipo de prueba       Caja Blanca – Cobertura de Condiciones
Objetivo             Forzar C2a=False y C2b=True (capacidadKg > 500); D2=True
                     activado por C2b
Trazabilidad         RF-04 / RN-02
Precondiciones       Administrador autenticado.
Datos de entrada     nombre: “Ruta X” (válido) · capacidadKg: 750 (C2a=False: 750 no <
                     1; C2b=True: 750 > 500) · resto válidos
Pasos                1. Invocar función con capacidad = 750. 2. Verificar error.
Condiciones          C2a=False, C2b=True (750 > 500) → D2=True
verificadas
Resultado esperado   Error: “Capacidad inválida: debe estar entre 1 y 500 kg”.
Resultado obtenido   —
Estado               Pendiente
```

### CB-CC-05

```text
Campo                Detalle
ID                   CB-CC-05
Módulo               Gestión de Rutas – crearRuta()
Tipo de prueba       Caja Blanca – Cobertura de Condiciones
Objetivo             Forzar C3=True (horaInicio = horaFin — caso de igualdad)
Trazabilidad         RF-04 / RN-03
Precondiciones       Administrador autenticado.
Datos de entrada     nombre: “Ruta X” (válido) · capacidadKg: 200 (válido) · horaInicio:
                     “08:00” · horaFin: “08:00” (C3=True: igual) · dias: [“lunes”]
Pasos                1. Invocar función con hora inicio igual a hora fin. 2. Verificar error.
Condiciones          C3=True (“08:00” >= “08:00”) → D3=True
verificadas
Resultado            Error: “Hora de inicio debe ser anterior a hora de fin”.
esperado
Resultado            —
obtenido
Estado               Pendiente
```

### CB-CC-06

```text
Campo                Detalle
ID                   CB-CC-06
Módulo               Gestión de Rutas – crearRuta()
Tipo de prueba       Caja Blanca – Cobertura de Condiciones
Objetivo             Forzar C1a=False, C1b=False, C2a=False, C2b=False, C3=False,
                     C4=False — todas las condiciones de validación en estado False —
                     para permitir que la ejecución llegue a L12
Trazabilidad         RF-04 / RN-01 a RN-04
Precondiciones       BD limpia en “Zona Centro”. Administrador autenticado.
Datos de entrada     nombre: “Ruta Centro Este” (15 chars: C1a=F, C1b=F) · capacidadKg:
                     200 (C2a=F, C2b=F) · horaInicio: “06:00” · horaFin: “14:00” (C3=F) ·
                     dias: [“viernes”,“sabado”] (C4=F) · zona: “Zona Centro”
Pasos                1. Invocar función con todos los datos válidos. 2. Verificar resultado
                     exitoso.
Condiciones          C1a=F, C1b=F → D1=F. C2a=F, C2b=F → D2=F. C3=F → D3=F. C4=F →
verificadas          D4=F. D5=F → ejecuta L12–L18.
Resultado            { exito: true, ruta: { ... } }. Ruta creada, notificación enviada
esperado             a “Zona Centro”.
Resultado            —
obtenido
Estado               Pendiente
```

**Cobertura teórica de condiciones prevista:** 100 % — C1a, C1b, C2a, C2b, C3, C4 y C6 con True y False. La cobertura ejecutada permanece pendiente.

## 6. Resumen de trazabilidad y cobertura

### 6.1 Matriz de trazabilidad completa

```text
ID caso     Tipo          Técnica              Requisito Regla de negocio        Estado
BN-PE-      Caja negra Partición               RF-04     RN-01, 02, 03, 04,      Pendiente
01                        equivalencia                   06
BN-PE-      Caja negra Partición               RF-04     RN-01                   Pendiente
02                        equivalencia
BN-PE-      Caja negra Partición               RF-04       RN-01                 Pendiente
03                        equivalencia
BN-PE-      Caja negra Partición               RF-04       RN-02                 Pendiente
04                        equivalencia
BN-PE-      Caja negra Partición               RF-04       RN-02                 Pendiente
05                        equivalencia
```

```text
ID caso   Tipo         Técnica             Requisito Regla de negocio   Estado
BN-PE-    Caja negra   Partición           RF-04     RN-03              Pendiente
06                     equivalencia
BN-PE-    Caja negra   Partición           RF-04     RN-04              Pendiente
07                     equivalencia
BN-PE-    Caja negra   Partición           RF-04     RN-01              Pendiente
08                     equivalencia
BN-PE-    Caja negra   Partición           RF-04     RN-02              Pendiente
09                     equivalencia
BN-PE-    Caja negra   Partición           RF-04     RN-02              Pendiente
10                     equivalencia
BN-PE-    Caja negra   Partición           RF-04     RN-03              Pendiente
11                     equivalencia
BN-PE-    Caja negra   Partición           RF-04     RN-04              Pendiente
12                     equivalencia
BN-PE-    Caja negra   Partición           RF-04     RN-05              Pendiente
13                     equivalencia
BN-VL-    Caja negra   Análisis valores    RF-04     RN-01              Pendiente
01                     límite
BN-VL-    Caja negra   Análisis valores    RF-04     RN-01              Pendiente
02                     límite
BN-VL-    Caja negra   Análisis valores    RF-04     RN-01              Pendiente
03                     límite
BN-VL-    Caja negra   Análisis valores    RF-04     RN-01              Pendiente
04                     límite
BN-VL-    Caja negra   Análisis valores    RF-04     RN-02              Pendiente
05                     límite
BN-VL-    Caja negra   Análisis valores    RF-04     RN-02              Pendiente
06                     límite
BN-VL-    Caja negra   Análisis valores    RF-04     RN-02              Pendiente
07                     límite
BN-VL-    Caja negra   Análisis valores    RF-04     RN-02              Pendiente
08                     límite
BN-TD-    Caja negra   Tabla de decisión   RF-04     RN-05              Pendiente
01
BN-TD-    Caja negra   Tabla de decisión   RF-04     RN-05              Pendiente
02
BN-TD-    Caja negra   Tabla de decisión   RF-04     RN-05              Pendiente
03
BN-TD-    Caja negra   Tabla de decisión   RF-04     RN-05              Pendiente
```

```text
ID caso  Tipo          Técnica                Requisito Regla de negocio       Estado
04
CB-CS-01 Caja          Cobertura sentencias   RF-04      RN-01 a RN-06         Pendiente
         blanca
CB-CS-02 Caja          Cobertura sentencias   RF-04      RN-01, RN-02          Pendiente
         blanca
CB-CS-03 Caja          Cobertura sentencias   RF-04      RN-05                 Pendiente
         blanca
CB-CD-   Caja          Cobertura decisiones   RF-04      RN-01                 Pendiente
01       blanca
CB-CD-   Caja          Cobertura decisiones   RF-04      RN-01, RN-02          Pendiente
02       blanca
CB-CD-   Caja          Cobertura decisiones   RF-04      RN-02, RN-03          Pendiente
03       blanca
CB-CD-   Caja          Cobertura decisiones   RF-04      RN-03, RN-04          Pendiente
04       blanca
CB-CD-   Caja          Cobertura decisiones   RF-04      RN-05                 Pendiente
05       blanca
CB-CD-   Caja          Cobertura decisiones   RF-04      RN-01 a RN-06         Pendiente
06       blanca
CB-CC-   Caja          Cobertura              RF-04      RN-01                 Pendiente
01       blanca        condiciones
CB-CC-   Caja          Cobertura              RF-04      RN-01                 Pendiente
02       blanca        condiciones
CB-CC-   Caja          Cobertura              RF-04      RN-02                 Pendiente
03       blanca        condiciones
CB-CC-   Caja          Cobertura              RF-04      RN-02                 Pendiente
04       blanca        condiciones
CB-CC-   Caja          Cobertura              RF-04      RN-03                 Pendiente
05       blanca        condiciones
CB-CC-   Caja          Cobertura              RF-04      RN-01 a RN-04         Pendiente
06       blanca        condiciones
```

### 6.2 Resumen de cobertura por técnica

```text
Tipo      Técnica              Casos   Cobertura planificada
Caja      Partición de         13      Clases representativas válidas e inválidas
Negra     Equivalencia                 definidas para los campos y reglas seleccionados
Caja      Análisis de          8       Límites inferior y superior de nombre (longitud) y
Negra     Valores Límite               capacidadKg
Caja      Tabla de Decisión 4          4 reglas de combinación zona/día/horario (RN-
Negra                                  05)
```

```text
Tipo      Técnica             Casos     Cobertura planificada
Caja      Cobertura de        3         100 % — líneas L01–L18 cubiertas
Blanca    Sentencias
Caja      Cobertura de        6         100 % — D1–D7 con True Y False
Blanca    Decisiones
Caja      Cobertura de        6         100 % — C1a, C1b, C2a, C2b, C3, C4, C6 con True
Blanca    Condiciones                   Y False
Total                         40
                              casos
```

Documento elaborado bajo los lineamientos de ISO/IEC/IEEE 12207 – Proceso de Verificación de Software (7.2.4) y las técnicas de la Sesión 10 del curso Calidad de Software 2025-2. Versión 1.0 — Junio 2026
