# Calidad de Software - Estimación de Esfuerzos

**Universidad Nacional de Colombia**  
**Facultad de Minas - Sede Medellín**  
**Curso:** Calidad de Software  
**Código:** 3010440  
**Profesor:** Albeiro Espinosa Bedoya, Ph.D. Ms.C.  
**Tema:** Estimación de Esfuerzos

---

## Nota de organización del documento

Este documento transcribe y organiza el contenido del material **"Estimación de Esfuerzos"** en formato Markdown.  
La información técnica, tablas, fórmulas, pasos y resultados numéricos se conservan.  
Además, se agregan explicaciones sencillas para que una persona sin conocimiento previo pueda comprender el tema de forma gradual.

---

# Tabla de contenido

1. [Agenda](#agenda)
2. [Idea general del tema](#idea-general-del-tema)
3. [Puntos de Caso de Uso - UCP](#1-puntos-de-caso-de-uso---ucp)
4. [Paso 1: Calcular UAW](#2-paso-1-calcular-uaw)
5. [Paso 2: Calcular UUCW](#3-paso-2-calcular-uucw)
6. [Paso 3: Calcular UUCP](#4-paso-3-calcular-uucp)
7. [Paso 4: Calcular TCF](#5-paso-4-calcular-tcf)
8. [Paso 5: Calcular EF](#6-paso-5-calcular-ef)
9. [Paso 6: Calcular UCP](#7-paso-6-calcular-ucp)
10. [Paso 7: Estimación del esfuerzo horas-hombre](#8-paso-7-estimación-del-esfuerzo-horas-hombre-e)
11. [Distribución del tiempo estimado](#9-distribución-del-tiempo-estimado-en-el-desarrollo-de-las-actividades)
12. [Ejemplo: Plataforma de reservas médicas](#10-ejemplo-plataforma-de-reservas-médicas)
13. [Ejercicios](#11-ejercicios)
14. [Referencias y datos de contacto](#12-referencias-y-datos-de-contacto)
15. [Resumen final del método](#13-resumen-final-del-método)

---

# Agenda

## Agenda 1/2

1. Puntos de Caso de Uso.
2. Paso 1: Calcular UAW.
3. Paso 2: Calcular UUCW.
4. Paso 3: Calcular UUCP.
5. Paso 4: Calcular TCF.
6. Paso 5: Calcular EF.

## Agenda 2/2

7. Paso 6: Calcular UCP.
8. Paso 7: Estimación del esfuerzo horas-hombre (E).
9. Ejemplo.
10. Ejercicios.
11. Referencias.

---

# Idea general del tema

La estimación de esfuerzos busca responder una pregunta central en un proyecto de software:

> **¿Cuánto trabajo tomará construir este sistema?**

Para responderla, el método de **Puntos de Caso de Uso** analiza:

- Qué usuarios o sistemas interactúan con el software.
- Qué funcionalidades debe ofrecer el software.
- Qué tan complejas son esas funcionalidades.
- Qué tan exigente es el proyecto desde el punto de vista técnico.
- Qué tan favorable o difícil es el entorno del equipo de trabajo.

Al final, el método permite calcular una estimación en **horas-hombre**, es decir, una aproximación del tiempo total de trabajo humano necesario para desarrollar el sistema.

---

# 1. Puntos de Caso de Uso - UCP

## Definición

**Use Case Point - UCP** es un método de ingeniería de software para estimar el tamaño y la complejidad de un proyecto de software teniendo en cuenta sus **requisitos funcionales**.

Es una técnica que ayuda a los gestores y desarrolladores de proyectos a estimar el esfuerzo necesario para crear un sistema de software.

## Origen del método

El método fue desarrollado por **Gustav Karner en 1993**, basándose en el método de punto de función, y fue supervisado por **Ivar Jacobson**.  
Posteriormente ha sido analizado en otros estudios, como la tesis de **Kirsten Ribu**, de la Universidad de Oslo, en 2001.

## Explicación sencilla

Un **caso de uso** describe algo que un usuario necesita hacer con el sistema.  
Por ejemplo:

- Registrarse.
- Iniciar sesión.
- Reservar una cita.
- Pagar en línea.
- Consultar información.

El método UCP toma esos casos de uso y los convierte en una medida numérica para estimar el esfuerzo del proyecto.

---

# 2. Paso 1: Calcular UAW

## Factor de peso de los actores sin ajustar - UAW

El **UAW** consiste en evaluar la complejidad de los actores con los que tendrá que interactuar el sistema.

Este puntaje se calcula determinando:

- Si cada actor es una persona o es otro sistema.
- La forma en la que ese actor interactúa con el caso de uso.
- La cantidad de actores de cada tipo.

## ¿Qué es un actor?

Un **actor** es cualquier persona, sistema externo o entidad que interactúa con el sistema que se va a desarrollar.

Ejemplos:

- Un paciente que agenda una cita.
- Un médico que gestiona su agenda.
- Un sistema de pagos externo.
- Un servicio de correo electrónico.

## Tabla 1. Factor de peso según el tipo de actores

| Tipo de actor | Descripción | Factor |
|---|---|---:|
| Simple | Otro sistema que interactúa con el sistema a desarrollar mediante una interfaz de programación. | 1 |
| Medio | Otro sistema interactuando a través de un protocolo, por ejemplo TCP-IP, o una persona interactuando a través de una interfaz en modo texto. | 2 |
| Complejo | Una persona que interactúa con el sistema mediante una interfaz gráfica, GUI. | 3 |

## Fórmula UAW

```text
UAW = suma de los factores de todos los actores
```

En notación matemática:

```text
UAW = Σ FactorActor_i
```

Donde:

```text
n = número de actores
```

## Explicación sencilla

Para calcular UAW se hace lo siguiente:

1. Se identifican todos los actores del sistema.
2. Se clasifica cada actor como simple, medio o complejo.
3. Se asigna el factor correspondiente.
4. Se suman todos los factores.

Ejemplo rápido:

| Actor | Tipo | Factor |
|---|---|---:|
| Usuario | Complejo | 3 |
| Sistema de pagos | Medio | 2 |
| Servicio de correo | Simple | 1 |

```text
UAW = 3 + 2 + 1 = 6
```

---

# 3. Paso 2: Calcular UUCW

## Factor de peso de los casos de uso sin ajustar - UUCW

En este paso se busca determinar el nivel de complejidad funcional a partir de las transacciones ejecutadas en un caso de uso.

## Nota

Una **transacción** es una acción que un usuario, o un sistema externo, realiza dentro de un caso de uso.

## Explicación sencilla

Un caso de uso puede tener pocas o muchas acciones.

Por ejemplo, **Iniciar sesión** puede ser simple porque normalmente implica:

1. Ingresar usuario.
2. Ingresar contraseña.
3. Validar datos.

En cambio, **Reservar cita médica** puede ser más complejo porque puede incluir:

1. Buscar médico.
2. Consultar disponibilidad.
3. Seleccionar fecha.
4. Confirmar datos.
5. Procesar pago.
6. Enviar notificación.

Por eso, cada caso de uso se clasifica según la cantidad de transacciones.

## Tabla 2. Complejidad de los casos de uso

| Tipo de caso de uso | Descripción | Factor |
|---|---|---:|
| Simple | 3 transacciones o menos. | 5 |
| Medio | 4 a 7 transacciones. | 10 |
| Complejo | Más de 7 transacciones. | 15 |

## Fórmula UUCW

```text
UUCW = suma de los factores de todos los casos de uso
```

En notación matemática:

```text
UUCW = Σ FactorCasoUso_i
```

## Explicación sencilla

Para calcular UUCW:

1. Se identifican todos los casos de uso.
2. Se cuenta o estima cuántas transacciones tiene cada caso de uso.
3. Se clasifica cada caso de uso como simple, medio o complejo.
4. Se asigna el factor correspondiente.
5. Se suman los factores.

Ejemplo rápido:

| Caso de uso | Tipo | Factor |
|---|---|---:|
| Registrarse | Simple | 5 |
| Buscar producto | Medio | 10 |
| Comprar producto | Complejo | 15 |

```text
UUCW = 5 + 10 + 15 = 30
```

---

# 4. Paso 3: Calcular UUCP

## Puntos de Caso de Uso sin ajustar - UUCP

Al inicio de un proyecto de software, cuando apenas se conocen los casos de uso y sus actores asociados, se puede proyectar una breve descripción de cada caso de uso, en la cual se describe de forma breve la funcionalidad que este debe brindar.

El **UUCP** son los puntos de casos de uso sin ajustar. Esto sirve para tener una idea un poco más precisa de la dificultad de los casos de uso e interfaces, tomando en cuenta:

- Los pesos de los actores: **UAW**.
- Los pesos de los casos de uso: **UUCW**.

## Fórmula UUCP

```text
UUCP = UAW + UUCW
```

Donde:

- **UUCP:** puntos de casos de uso sin ajustar.
- **UAW:** factor de peso de los actores sin ajustar.
- **UUCW:** factor de peso de los casos de uso sin ajustar.

## Explicación sencilla

El UUCP reúne los dos primeros cálculos:

```text
Complejidad de actores + complejidad de casos de uso
```

Ejemplo:

```text
UAW = 6
UUCW = 30
UUCP = 6 + 30 = 36
```

---

# 5. Paso 4: Calcular TCF

## Factores de complejidad técnica - TCF

El **TCF**, o factor de complejidad técnica, ajusta el cálculo según las exigencias técnicas del sistema.

No todos los proyectos tienen la misma dificultad técnica.  
Un sistema distribuido, con seguridad especial, concurrencia o alto rendimiento, puede requerir más esfuerzo que un sistema simple.

## Tabla 3. Factores de complejidad técnica

| Factor | Descripción | Peso |
|---|---|---:|
| T1 | Sistema distribuido. | 2 |
| T2 | Objetivos de performance o tiempo de respuesta. | 1 |
| T3 | Eficiencia del usuario final. | 1 |
| T4 | Procesamiento interno complejo. | 1 |
| T5 | El código debe ser reutilizable. | 1 |
| T6 | Facilidad de instalación. | 0.5 |
| T7 | Facilidad de uso. | 0.5 |
| T8 | Portabilidad. | 2 |
| T9 | Facilidad de cambio. | 1 |
| T10 | Concurrencia. | 1 |
| T11 | Incluye objetivos especiales de seguridad. | 1 |
| T12 | Provee acceso directo a terceras partes. | 1 |
| T13 | Facilidades especiales de entrenamiento a usuario. | 1 |

## Tabla 4. Calificación de cada factor

| Descripción | Valor |
|---|---:|
| Irrelevante | De 0 a 2 |
| Medio | De 3 a 4 |
| Esencial | 5 |

## Cálculo de TFactor

En la práctica, para cada factor técnico se multiplica:

```text
Peso del factor × Valor asignado
```

Luego se suman todos los productos:

```text
TFactor = Σ Factor_i
```

## Fórmula TCF

```text
TCF = 0.6 + (0.01 × TFactor)
```

## Explicación sencilla

Para calcular TCF:

1. Se revisan los 13 factores técnicos.
2. A cada factor se le asigna un valor de 0 a 5.
3. Se multiplica ese valor por el peso del factor.
4. Se suman todos los productos.
5. Se aplica la fórmula del TCF.

El TCF sirve para ajustar el tamaño del proyecto según su dificultad técnica.

---

# 6. Paso 5: Calcular EF

## Factores ambientales - EF

El **EF**, o factor ambiental, ajusta el cálculo según las condiciones del equipo y del contexto del proyecto.

Aquí se tienen en cuenta aspectos como:

- Experiencia del equipo.
- Familiaridad con el modelo del proyecto.
- Motivación.
- Estabilidad de los requerimientos.
- Dificultad del lenguaje de programación.
- Si hay personal de tiempo parcial.

## Tabla 5. Factores ambientales

| Factor | Descripción | Peso |
|---|---|---:|
| E1 | Familiaridad con el modelo de proyecto utilizado. | 1.5 |
| E2 | Experiencia en la aplicación. | 0.5 |
| E3 | Experiencia en orientación a objetos. | 1 |
| E4 | Capacidad del analista líder. | 0.5 |
| E5 | Motivación. | 1 |
| E6 | Estabilidad de los requerimientos. | 2 |
| E7 | Personal part-time. | -1 |
| E8 | Dificultad del lenguaje de programación. | -1 |

## Tabla 6. Calificación de cada factor

| Descripción | Valor |
|---|---:|
| Irrelevante | De 0 a 2 |
| Medio | De 3 a 4 |
| Esencial | 5 |

## Cálculo de EFactor

Para cada factor ambiental se multiplica:

```text
Peso del factor × Valor asignado
```

Luego se suman todos los productos:

```text
EFactor = Σ Factor_i
```

## Fórmula EF

```text
EF = 1.4 + (-0.03 × EFactor)
```

También puede escribirse así:

```text
EF = 1.4 - (0.03 × EFactor)
```

## Explicación sencilla

El EF mide qué tan favorable o difícil es el ambiente del proyecto.

Por ejemplo:

- Si el equipo tiene experiencia, buena motivación y requisitos estables, el esfuerzo puede ser menor.
- Si el equipo tiene poca experiencia, trabaja parcialmente o usa un lenguaje difícil, el esfuerzo puede aumentar.

---

# 7. Paso 6: Calcular UCP

## Puntos de Caso de Uso ajustados - UCP

Para obtener los **UCP**, se multiplica el UUCP por el TCF y por el EF.

## Fórmula UCP

```text
UCP = UUCP × TCF × EF
```

Donde:

- **UCP:** puntos de casos de uso ajustados.
- **UUCP:** puntos de casos de uso sin ajustar.
- **TCF:** factores técnicos.
- **EF:** factores ambientales.

## Explicación sencilla

El UCP es el valor final de tamaño del proyecto, ya ajustado por:

1. Actores.
2. Casos de uso.
3. Complejidad técnica.
4. Condiciones ambientales.

En términos simples:

```text
UCP = tamaño funcional del sistema ajustado por dificultad técnica y contexto del equipo
```

---

# 8. Paso 7: Estimación del esfuerzo horas-hombre (E)

## Esfuerzo horas-hombre

El esfuerzo horas-hombre permite estimar cuántas horas de trabajo humano puede tomar el desarrollo del sistema.

## Derivación automática del PF - Método Continuo

### Idea

Ajustar el **Factor de Productividad (PF)** usando el factor ambiental **EF**.

## Fórmula PF

```text
PF = 20 + k × (1 - EF)
```

Donde:

- **PF:** Factor de Productividad.
- **EF:** Factor ambiental. Típicamente se encuentra entre 0.6 y 1.4.
- **k:** Constante de sensibilidad. Suele estar entre 15 y 25; usualmente se usa 20.

## Fórmula del esfuerzo

```text
E = UCP × PF
```

Donde:

- **E:** esfuerzo estimado en horas, implementación de casos de uso.
- **UCP:** puntos de casos de uso ajustados.
- **PF:** factor de productividad.

## Explicación sencilla

Después de calcular el UCP, se necesita traducir ese tamaño a horas de trabajo.

Para eso se usa el PF:

```text
Si el proyecto es más difícil para el equipo, el PF puede aumentar.
Si el entorno es más favorable, el PF puede disminuir.
```

Finalmente:

```text
Esfuerzo total = tamaño ajustado del sistema × horas por punto de caso de uso
```

---

# 9. Distribución del tiempo estimado en el desarrollo de las actividades

En la siguiente tabla se detalla la distribución en porcentaje para las diferentes fases del ciclo de vida del esfuerzo en el desarrollo del proyecto.

## Tabla 7. Distribución porcentual de actividades

| Actividad | Porcentaje |
|---|---:|
| Análisis | 10 % |
| Diseño | 20 % |
| Programación | 40 % |
| Pruebas | 15 % |
| Mantenimiento | 15 % |

## Explicación sencilla

Si el esfuerzo total calculado fuera de 1000 horas, entonces se distribuiría así:

| Actividad | Porcentaje | Horas aproximadas |
|---|---:|---:|
| Análisis | 10 % | 100 horas |
| Diseño | 20 % | 200 horas |
| Programación | 40 % | 400 horas |
| Pruebas | 15 % | 150 horas |
| Mantenimiento | 15 % | 150 horas |

---

# 10. Ejemplo: Plataforma de reservas médicas

## Descripción del sistema

**Sistema:** Plataforma de reservas médicas.

**Objetivo:** Permitir agendar citas, gestionar disponibilidad y pagos.

## Alcance

El alcance incluye:

- Registro e inicio de sesión.
- Búsqueda de médicos.
- Reserva de citas.
- Pago en línea.
- Gestión de agenda.
- Notificaciones.

---

## Diagrama de casos de uso

**Figura 1:** Diagrama de Casos de Uso - Plataforma de reservas médicas.

### Sistema

**Plataforma de reservas médicas**.

### Módulos o grupos funcionales visibles en el diagrama

- Autenticación.
- Gestión de citas.
- Administración.
- Servicios externos.

### Actores

- Paciente.
- Médico.
- Administrador.
- Sistema de pagos.
- Servicio de email.

### Casos de uso

- Registrarse.
- Iniciar sesión.
- Buscar médico.
- Reservar cita.
- Cancelar cita.
- Gestionar agenda.
- Procesar pago.
- Enviar notificaciones.

### Relaciones include visibles

En el diagrama aparecen relaciones **«include»**, que indican que un caso de uso incluye obligatoriamente el comportamiento de otro caso de uso.

De forma general, el diagrama muestra que algunos procesos se apoyan en servicios externos como:

- Procesar pago.
- Enviar notificaciones.

## Explicación sencilla

Una plataforma de reservas médicas necesita varios usuarios y servicios:

- El paciente agenda o cancela citas.
- El médico gestiona su agenda.
- El administrador puede administrar información.
- El sistema de pagos procesa transacciones.
- El servicio de email envía notificaciones.

---

## Actores del ejemplo

| Actor | Tipo | Peso |
|---|---|---:|
| Paciente | Complejo | 3 |
| Médico | Complejo | 3 |
| Administrador | Complejo | 3 |
| Sistema de pagos | Promedio | 2 |
| Servicio de email | Simple | 1 |

## Cálculo UAW del ejemplo

```text
UAW = 3 + 3 + 3 + 2 + 1 = 12
```

---

## Casos de uso del ejemplo

| Caso de uso | Tipo | Peso |
|---|---|---:|
| Registrarse | Simple | 5 |
| Iniciar sesión | Simple | 5 |
| Buscar médico | Promedio | 10 |
| Reservar cita | Complejo | 15 |
| Cancelar cita | Promedio | 10 |
| Gestionar agenda | Complejo | 15 |
| Procesar pago | Complejo | 15 |
| Enviar notificaciones | Simple | 5 |

## Cálculo UUCW del ejemplo

```text
UUCW = 80
```

---

## Cálculo UUCP del ejemplo

```text
UUCP = UAW + UUCW
UUCP = 12 + 80
UUCP = 92
```

---

## Factores técnicos - TCF del ejemplo

| Factor | Peso | Valor | Producto |
|---|---:|---:|---:|
| T1 | 2 | 3 | 6 |
| T2 | 1 | 3 | 3 |
| T3 | 1 | 4 | 4 |
| T4 | 1 | 3 | 3 |
| T5 | 1 | 2 | 2 |
| T6 | 0.5 | 3 | 1.5 |
| T7 | 0.5 | 5 | 2.5 |
| T8 | 2 | 2 | 4 |
| T9 | 1 | 3 | 3 |
| T10 | 1 | 4 | 4 |
| T11 | 1 | 5 | 5 |
| T12 | 1 | 3 | 3 |
| T13 | 1 | 2 | 2 |

## Cálculo TCF del ejemplo

```text
TF = 43
TCF = 0.6 + (0.01 × 43)
TCF = 1.03
```

---

## Factores ambientales - EF del ejemplo

| Factor | Peso | Valor | Producto |
|---|---:|---:|---:|
| E1 | 1.5 | 4 | 6 |
| E2 | 0.5 | 3 | 1.5 |
| E3 | 1 | 4 | 4 |
| E4 | 0.5 | 5 | 2.5 |
| E5 | 1 | 4 | 4 |
| E6 | 2 | 3 | 6 |
| E7 | -1 | 2 | -2 |
| E8 | -1 | 2 | -2 |

## Cálculo EF del ejemplo

```text
EFsum = 20
EF = 1.4 - (0.03 × 20)
EF = 0.8
```

---

## Cálculo final UCP del ejemplo

```text
UCP = UUCP × TCF × EF
UCP = 92 × 1.03 × 0.8
UCP = 75.8
```

---

## Estimación de esfuerzo del ejemplo

### Cálculo del Productivity Factor - PF usando el Método Continuo

```text
PF = 20 + k × (1 - EF)
```

Datos:

```text
EF = 0.8
k = 20
```

Cálculo:

```text
PF = 20 + 20(1 - 0.8)
PF = 24 horas/UCP
```

### Estimación del esfuerzo total

```text
Esfuerzo = UCP × PF
Esfuerzo = 75.8 × 24
Esfuerzo = 1819 horas
```

### Conversión aproximada a meses

```text
1 desarrollador: aproximadamente 11.4 meses
Equipo de 3 personas: aproximadamente 3.8 meses
```

## Explicación sencilla del ejemplo

El proyecto de reservas médicas termina con un valor de **75.8 UCP**.  
Cada UCP se estima en **24 horas de trabajo**.  
Por eso el esfuerzo total es aproximadamente:

```text
75.8 × 24 = 1819 horas
```

Si trabaja una sola persona, tardaría más tiempo.  
Si trabaja un equipo de tres personas, el tiempo calendario puede reducirse, aunque no siempre de manera perfectamente proporcional porque también existen tareas de coordinación, revisión y comunicación.

---

# 11. Ejercicios

## Ejercicio 1

### Sistema

**Sistema de Control de un Centro Médico**.

### Actores visibles en el diagrama

- Médico.
- Farmacéutico.
- Secretaria.
- Administrador.

### Casos de uso visibles en el diagrama

- Crear Historia Clínica.
- Consultar Historia Clínica.
- Consultar Médicos.
- Modificar Historia Clínica.
- Ingresar al sistema.
- Consultar Medicina.
- Ingresar Medicina.
- Modificar Medicina.
- Ingresar Paciente.
- Ingresar Cita.
- Cancelar Cita.
- Registrar Pago.
- Crear empleado.
- Modificar Personal.
- Ver Historial.

### Explicación sencilla

Este ejercicio permite practicar la clasificación de:

1. Actores.
2. Casos de uso.
3. Complejidad de los casos de uso.
4. Cálculo de UAW, UUCW, UUCP, TCF, EF, UCP y esfuerzo.

Para resolverlo, se debe iniciar identificando qué actores son simples, medios o complejos, y luego clasificar cada caso de uso según el número de transacciones.

---

## Ejercicio 2

### Sistema

**Web colaborativa**.

### Actores visibles en el diagrama

- Usuario.
- Sistema.

### Casos de uso visibles en el diagrama

- Recibir notificaciones.
- Administrar proyectos.
- Agregar.
- Invitar colaboración.
- Editar.
- Colaborar.
- Acepta colaboración.

### Relaciones include visibles

El diagrama muestra relaciones **«include»** entre algunos casos de uso.  
Estas relaciones indican que una funcionalidad necesita incluir otra para completarse.

Relaciones visibles:

- Invitar colaboración incluye Acepta colaboración.
- Colaborar incluye Acepta colaboración.
- Administrar proyectos incluye Editar.

### Explicación sencilla

Este ejercicio representa una plataforma en la que un usuario puede colaborar, invitar a otros, administrar proyectos y editar información.  
El sistema también participa en acciones como notificar o agregar información.

---

# 12. Referencias y datos de contacto

## Referencias

En el material aparece una diapositiva titulada **Referencias (1/1)**, pero no se observan referencias bibliográficas visibles en la diapositiva.

## Datos de contacto del profesor

**Albeiro Espinosa Bedoya, Ph.D. Ms.C.**  
Profesor Asociado  
Departamento de Ciencias de la Computación y de la Decisión  
Facultad de Minas  
Universidad Nacional de Colombia

**Email:** aespinos@unal.edu.co  
**Instagram:** @albeiroespinosabedoya  
**Dirección:** Av. 80 #65-223, Bloque M8A, Of. 204  
**Teléfono:** +57 604 4255384

---

# 13. Resumen final del método

El método de Puntos de Caso de Uso permite estimar el esfuerzo de un proyecto de software siguiendo esta ruta:

## Ruta completa de cálculo

```text
1. Identificar actores
2. Calcular UAW
3. Identificar casos de uso
4. Calcular UUCW
5. Calcular UUCP = UAW + UUCW
6. Calcular TCF con factores técnicos
7. Calcular EF con factores ambientales
8. Calcular UCP = UUCP × TCF × EF
9. Calcular PF = 20 + k × (1 - EF)
10. Calcular esfuerzo E = UCP × PF
```

## Fórmulas principales

```text
UAW = Σ FactorActor_i
```

```text
UUCW = Σ FactorCasoUso_i
```

```text
UUCP = UAW + UUCW
```

```text
TCF = 0.6 + (0.01 × TFactor)
```

```text
EF = 1.4 - (0.03 × EFactor)
```

```text
UCP = UUCP × TCF × EF
```

```text
PF = 20 + k × (1 - EF)
```

```text
E = UCP × PF
```

## En palabras simples

El método funciona así:

1. Primero se mide qué tan complejo es el sistema desde sus usuarios y funcionalidades.
2. Luego se ajusta esa medida según la dificultad técnica.
3. Después se ajusta según las condiciones del equipo y del proyecto.
4. Finalmente se convierte el tamaño ajustado en horas de trabajo.

## Resultado esperado

El resultado final es una estimación del esfuerzo en:

```text
horas-hombre
```

Esto ayuda a planificar:

- Tiempo.
- Equipo necesario.
- Costos.
- Cronograma.
- Distribución del trabajo por fases.

---

# Glosario básico

| Término | Significado sencillo |
|---|---|
| Actor | Persona o sistema externo que interactúa con el software. |
| Caso de uso | Funcionalidad que el sistema debe ofrecer. |
| Transacción | Acción realizada dentro de un caso de uso. |
| UAW | Peso de los actores sin ajustar. |
| UUCW | Peso de los casos de uso sin ajustar. |
| UUCP | Suma inicial de actores y casos de uso. |
| TCF | Factor que ajusta según la complejidad técnica. |
| EF | Factor que ajusta según el ambiente del proyecto. |
| UCP | Puntos de caso de uso ajustados. |
| PF | Factor de productividad. |
| E | Esfuerzo estimado en horas-hombre. |
| GUI | Interfaz gráfica de usuario. |
| Include | Relación donde un caso de uso incluye obligatoriamente otro. |

---

# Cierre conceptual

La estimación de esfuerzos no busca adivinar exactamente cuánto durará un proyecto, sino construir una aproximación razonable con base en información técnica.

El valor de este método está en que obliga al equipo a pensar en:

- Qué se debe construir.
- Quién usará el sistema.
- Qué tan complejo será.
- Qué condiciones tiene el equipo.
- Cuánto esfuerzo puede requerir.

Por eso es una herramienta útil para la planificación, la negociación de tiempos, la asignación de recursos y el control de proyectos de software.
