# Práctica TDD - Construcción de Software

Universidad Continental · Semana 10

## ¿Qué es TDD?

TDD (Test-Driven Development) es una técnica de desarrollo donde el test se
escribe ANTES del código de producción. Se trabaja en ciclos cortos de tres pasos:

- **Red:** se escribe un test que falla porque el código no existe o no cumple el requisito.
- **Green:** se escribe el código mínimo necesario para que el test pase.
- **Refactor:** se mejora la estructura del código sin cambiar su comportamiento (los tests siguen en verde).

## Cómo lo apliqué

### Ejercicio 1: FizzBuzz (`fizzbuzz/`)
Se construyó la función `fizzbuzz(n)` en 5 ciclos: números normales, Fizz,
Buzz, FizzBuzz y un test integral con `subTest`. En el ciclo 4 el test falló
porque el `if` de 3 se evaluaba antes que el de 15, lo que obligó a reordenar
las condiciones.

### Ejercicio 2: Validador de contraseñas (`validador/`)
Se construyó la función `validar_password(pwd)` en 6 ciclos, una regla por ciclo:
longitud mínima, mayúscula, minúscula, dígito y carácter especial. El ciclo 6
fue un refactor (constante `CARACTERES_ESPECIALES`) con tests integrales y `subTest`.

### Historial de commits
Se hizo un commit por cada ciclo Red→Green→Refactor, de modo que el historial
muestra la evolución incremental del código.

## Estructura del proyecto

    tdd-practica/
    ├── fizzbuzz/
    │   ├── __init__.py
    │   ├── fizzbuzz.py
    │   └── test_fizzbuzz.py
    ├── validador/
    │   ├── __init__.py
    │   ├── validador.py
    │   └── test_validador.py
    └── README.md

## Cómo ejecutar los tests

Desde la carpeta raíz del proyecto:

    python -m unittest discover