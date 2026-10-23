# Práctica TDD: Construcción de Software (Semana 10)

**Nombre:** HUMBERTO ZAMORA MOSOCOSO
**Curso:** Construcción de Software, Universidad Continental

## ¿Qué es TDD?

TDD (Test-Driven Development, desarrollo guiado por pruebas) es una técnica
en la que el test se escribe **antes** que el código de producción. Se trabaja
con un ciclo corto de tres pasos:

1. **Red:** se escribe un test que falla, porque el código aún no existe o no
   cumple el requisito.
2. **Green:** se escribe el código mínimo necesario para que el test pase.
3. **Refactor:** se mejora la estructura del código sin cambiar su
   comportamiento, manteniendo los tests en verde.

## Cómo lo apliqué

Construí dos módulos en Python con `unittest`, haciendo un commit al terminar
cada ciclo para que el historial muestre la evolución incremental.

### Ejercicio 1: FizzBuzz (`fizzbuzz/`)

Función `fizzbuzz(n)`. Se construyó en 5 ciclos: números normales, Fizz,
Buzz, FizzBuzz (donde el test reveló que el caso múltiplo de 15 debía evaluarse
primero) y un test integral con `subTest`.

### Ejercicio 2: Validador de contraseñas (`validador/`)

Función `validar_password(pwd)`, que devuelve un diccionario con `valida` y
`errores`. Se construyó en 6 ciclos: longitud mínima, mayúscula, minúscula,
dígito, carácter especial y tests integrales con `subTest`. Cada regla se
evalúa de forma independiente para acumular todos los errores.

## Estructura del proyecto

```
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
```

## Cómo ejecutar los tests

Desde la carpeta raíz del proyecto:

```
python -m unittest discover
```