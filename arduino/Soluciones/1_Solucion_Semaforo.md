# Solucion Ejercicio 1. Semaforo

# Programa

```cpp
const int ledRojo = 8;
const int ledAmarillo = 9;
const int ledVerde = 10;
const int boton = 2;

int estado = 0;
int ultimoBoton = 0;

void setup() {

  pinMode(ledRojo, OUTPUT);
  pinMode(ledAmarillo, OUTPUT);
  pinMode(ledVerde, OUTPUT);

  pinMode(boton, INPUT);

  mostrarEstado();
}

void loop() {

  int lectura = digitalRead(boton);

  if (lectura == HIGH && ultimoBoton == LOW) {

    estado++;

    if (estado > 2) {
      estado = 0;
    }

    mostrarEstado();

    delay(200); // Antirrebote sencillo
  }

  ultimoBoton = lectura;
}

void mostrarEstado() {

  digitalWrite(ledRojo, LOW);
  digitalWrite(ledAmarillo, LOW);
  digitalWrite(ledVerde, LOW);

  if (estado == 0) {
    digitalWrite(ledRojo, HIGH);
  }

  if (estado == 1) {
    digitalWrite(ledVerde, HIGH);
  }

  if (estado == 2) {
    digitalWrite(ledAmarillo, HIGH);
  }
}
```
