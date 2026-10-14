# Ejercicio Arduino: Semáforo Controlado por Botón

## Objetivo

Construir un semáforo utilizando tres LEDs y un botón. Cada vez que se pulse el botón, el semáforo cambiará al siguiente estado:

1. Rojo
2. Verde
3. Amarillo
4. Rojo (vuelve a empezar)

Con este ejercicio practicarás:

- Entradas digitales (botón).
- Salidas digitales (LEDs).
- Uso de variables.
- Estructuras condicionales (`if`).
- Detección de pulsaciones.

---

# Materiales necesarios

- 1 Arduino Uno
- 1 Protoboard
- 3 LEDs (rojo, amarillo y verde)
- 3 resistencias de 220 Ω
- 1 Pulsador
- 1 Resistencia de 10 kΩ
- Cables de conexión

---

# Montaje del circuito

## Conexión de los LEDs

### LED Rojo

- Ánodo (+) → Pin 8 del Arduino.
- Cátodo (-) → Resistencia 220 Ω → GND.

### LED Amarillo

- Ánodo (+) → Pin 9 del Arduino.
- Cátodo (-) → Resistencia 220 Ω → GND.

### LED Verde

- Ánodo (+) → Pin 10 del Arduino.
- Cátodo (-) → Resistencia 220 Ω → GND.

---

## Conexión del botón

- Un terminal del botón → 5V.
- El otro terminal → Pin 2 del Arduino.
- Desde el Pin 2 conectar una resistencia de 10 kΩ a GND.

Esta resistencia evita que el pin quede flotando cuando no se pulsa el botón.

---

# Funcionamiento esperado

Al iniciar el programa:

🔴 LED rojo encendido

Primera pulsación:

🟢 LED verde encendido

Segunda pulsación:

🟡 LED amarillo encendido

Tercera pulsación:

🔴 LED rojo encendido

Y el ciclo continúa indefinidamente.

---

# Preguntas para el alumno

1. ¿Qué función se utiliza para leer el estado de un botón?
2. ¿Qué función se utiliza para encender un LED?
3. ¿Para qué sirve la variable `estado`?
4. ¿Qué ocurrirá si eliminamos el `delay(200)`?
5. ¿Por qué se utiliza una resistencia de 220 Ω con los LEDs?
6. ¿Por qué se utiliza una resistencia de 10 kΩ con el botón?

---

# Retos de ampliación

## Reto 1

Añadir un cuarto estado donde se enciendan los tres LEDs simultáneamente.

---

## Reto 2

Mostrar por el Monitor Serie el estado actual:

```text
Estado actual: ROJO
Estado actual: VERDE
Estado actual: AMARILLO
```

---

## Reto 3

Añadir un segundo botón para retroceder entre los estados del semáforo.

---

## Reto 4

Modificar el programa para que una pulsación larga (más de 2 segundos) apague todos los LEDs.

---

# Entrega

El alumno deberá entregar:

- Fotografía del montaje.
- Código funcionando correctamente.
- Respuestas a las preguntas propuestas.
- Resolución de al menos uno de los retos de ampliaci
