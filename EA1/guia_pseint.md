# Guía completa de PSeInt desde cero
## Programación básica paso a paso

> Material de apoyo para estudiantes que comienzan a programar con **PSeInt**.

---

# Índice

1. [¿Qué es PSeInt?](#1-qué-es-pseint)
2. [¿Para qué sirve?](#2-para-qué-sirve)
3. [Primeros pasos](#3-primeros-pasos)
4. [Estructura básica de un algoritmo](#4-estructura-básica-de-un-algoritmo)
5. [Variables y tipos de datos](#5-variables-y-tipos-de-datos)
6. [Entrada y salida de datos](#6-entrada-y-salida-de-datos)
7. [Operadores](#7-operadores)
8. [Condicionales](#8-condicionales)
9. [Ciclos](#9-ciclos)
10. [Contadores y acumuladores](#10-contadores-y-acumuladores)
11. [Menús](#11-menús)
12. [Arreglos](#12-arreglos)
13. [Subprocesos](#13-subprocesos)
14. [Buenas prácticas](#14-buenas-prácticas)
15. [Errores comunes](#15-errores-comunes)
16. [Ejercicios guiados](#16-ejercicios-guiados)
17. [Ejercicios propuestos](#17-ejercicios-propuestos)
18. [Mini proyecto final](#18-mini-proyecto-final)
19. [Consejos para aprender mejor](#19-consejos-para-aprender-mejor)

---

# 1. ¿Qué es PSeInt?

**PSeInt** es una herramienta educativa que permite escribir algoritmos en pseudocódigo de forma simple y ordenada.

Su nombre viene de:

- **PSe**: Pseudocódigo
- **Int**: Intérprete

Es muy útil para aprender programación porque permite enfocarse primero en la **lógica**, antes de pasar a lenguajes como Python, Java o C#.

---

# 2. ¿Para qué sirve?

PSeInt sirve para:

- Aprender a pensar paso a paso
- Resolver problemas mediante algoritmos
- Comprender estructuras básicas de programación
- Prepararse para lenguajes reales como Python

Con PSeInt se puede practicar:

- Variables
- Operaciones matemáticas
- Condiciones
- Repeticiones
- Menús
- Arreglos
- Subprocesos

---

# 3. Primeros pasos

## 3.1 Qué es un algoritmo

Un **algoritmo** es una secuencia ordenada de pasos para resolver un problema.

Ejemplo cotidiano:

**Problema:** preparar un café  
**Algoritmo:**
1. Hervir agua
2. Poner café en una taza
3. Agregar agua caliente
4. Revolver
5. Servir

En programación hacemos exactamente lo mismo, pero con instrucciones.

---

## 3.2 Ejemplo de algoritmo simple en PSeInt

```pseint
Algoritmo hola_mundo
	Escribir "Hola mundo"
FinAlgoritmo
```

### Explicación
- `Algoritmo hola_mundo`: comienza el programa
- `Escribir "Hola mundo"`: muestra texto en pantalla
- `FinAlgoritmo`: termina el programa

---

# 4. Estructura básica de un algoritmo

La forma más común es esta:

```pseint
Algoritmo nombre_del_algoritmo
	Definir variable1 Como Entero
	Definir variable2 Como Real

	Escribir "Mensaje"
	Leer variable1

	// operaciones
	// decisiones
	// repeticiones

FinAlgoritmo
```

---

# 5. Variables y tipos de datos

## 5.1 Qué es una variable

Una variable es un espacio donde guardamos información.

Ejemplos:
- edad
- nombre
- precio
- promedio

---

## 5.2 Declarar variables

En PSeInt se usa `Definir`.

```pseint
Definir edad Como Entero
Definir precio Como Real
Definir nombre Como Caracter
Definir respuesta Como Logico
```

---

## 5.3 Tipos de datos básicos

### Entero
Guarda números enteros.

```pseint
Definir cantidad Como Entero
```

Ejemplos:
- 5
- 10
- -3

### Real
Guarda números con decimales.

```pseint
Definir promedio Como Real
```

Ejemplos:
- 4.5
- 6.8
- 10.0

### Caracter
Guarda texto.

```pseint
Definir nombre Como Caracter
```

Ejemplos:
- "Ana"
- "Pedro"
- "Programacion"

### Logico
Guarda `Verdadero` o `Falso`.

```pseint
Definir activo Como Logico
```

---

## 5.4 Asignar valores

En PSeInt se usa `<-`

```pseint
edad <- 20
precio <- 1990.5
nombre <- "Cristian"
activo <- Verdadero
```

---

# 6. Entrada y salida de datos

## 6.1 Mostrar información

Se usa `Escribir`

```pseint
Escribir "Bienvenido"
```

También se puede mostrar variables:

```pseint
Definir nombre Como Caracter
nombre <- "Ana"
Escribir "El nombre es: ", nombre
```

---

## 6.2 Leer datos del usuario

Se usa `Leer`

```pseint
Definir edad Como Entero
Escribir "Ingrese su edad:"
Leer edad
```

---

## 6.3 Ejemplo completo

```pseint
Algoritmo pedir_nombre
	Definir nombre Como Caracter

	Escribir "Ingrese su nombre:"
	Leer nombre

	Escribir "Hola ", nombre
FinAlgoritmo
```

---

# 7. Operadores

## 7.1 Operadores aritméticos

| Operador | Significado | Ejemplo |
|---|---|---|
| `+` | suma | `a + b` |
| `-` | resta | `a - b` |
| `*` | multiplicación | `a * b` |
| `/` | división | `a / b` |
| `MOD` | resto de división | `a MOD b` |

### Ejemplo
```pseint
Algoritmo operaciones
	Definir a, b, suma, resta, multi, division Como Real

	Escribir "Ingrese el primer numero:"
	Leer a

	Escribir "Ingrese el segundo numero:"
	Leer b

	suma <- a + b
	resta <- a - b
	multi <- a * b
	division <- a / b

	Escribir "Suma: ", suma
	Escribir "Resta: ", resta
	Escribir "Multiplicacion: ", multi
	Escribir "Division: ", division
FinAlgoritmo
```

---

## 7.2 Operadores relacionales

Sirven para comparar valores.

| Operador | Significado |
|---|---|
| `=` | igual |
| `<>` | distinto |
| `>` | mayor |
| `<` | menor |
| `>=` | mayor o igual |
| `<=` | menor o igual |

Ejemplo:
```pseint
Si edad >= 18 Entonces
	Escribir "Es mayor de edad"
FinSi
```

---

## 7.3 Operadores lógicos

| Operador | Significado |
|---|---|
| `Y` | AND |
| `O` | OR |
| `NO` | NOT |

Ejemplo:
```pseint
Si edad >= 18 Y tieneCarnet = 1 Entonces
	Escribir "Puede ingresar"
FinSi
```

---

# 8. Condicionales

Los condicionales permiten tomar decisiones.

---

## 8.1 Si simple

```pseint
Si condicion Entonces
	instrucciones
FinSi
```

### Ejemplo
```pseint
Algoritmo mayor_edad
	Definir edad Como Entero

	Escribir "Ingrese su edad:"
	Leer edad

	Si edad >= 18 Entonces
		Escribir "Eres mayor de edad"
	FinSi
FinAlgoritmo
```

---

## 8.2 Si - SiNo

```pseint
Si condicion Entonces
	instrucciones
SiNo
	otras instrucciones
FinSi
```

### Ejemplo
```pseint
Algoritmo par_impar
	Definir num Como Entero

	Escribir "Ingrese un numero:"
	Leer num

	Si num MOD 2 = 0 Entonces
		Escribir "Es par"
	SiNo
		Escribir "Es impar"
	FinSi
FinAlgoritmo
```

---

## 8.3 Si anidado

```pseint
Algoritmo signo_numero
	Definir num Como Entero

	Escribir "Ingrese un numero:"
	Leer num

	Si num > 0 Entonces
		Escribir "Positivo"
	SiNo
		Si num < 0 Entonces
			Escribir "Negativo"
		SiNo
			Escribir "Es cero"
		FinSi
	FinSi
FinAlgoritmo
```

---

## 8.4 Ejemplo con varias condiciones

```pseint
Algoritmo control_acceso
	Definir credencial, horario, esNuevo, acompanado Como Entero

	Escribir "Tiene credencial activa? (1=Si, 0=No)"
	Leer credencial

	Escribir "Es horario permitido? (1=Si, 0=No)"
	Leer horario

	Escribir "Es estudiante nuevo? (1=Si, 0=No)"
	Leer esNuevo

	Escribir "Viene acompanado? (1=Si, 0=No)"
	Leer acompanado

	Si credencial = 1 Y horario = 1 Entonces
		Si esNuevo = 1 Entonces
			Si acompanado = 1 Entonces
				Escribir "Puede ingresar"
			SiNo
				Escribir "No puede ingresar"
			FinSi
		SiNo
			Escribir "Puede ingresar"
		FinSi
	SiNo
		Escribir "No puede ingresar"
	FinSi
FinAlgoritmo
```

---

# 9. Ciclos

Los ciclos permiten repetir instrucciones.

---

## 9.1 Para

Se usa cuando sabemos cuántas veces se repetirá algo.

```pseint
Para i <- 1 Hasta 5 Hacer
	Escribir i
FinPara
```

### Ejemplo: tabla de multiplicar
```pseint
Algoritmo tabla
	Definir num, i Como Entero

	Escribir "Ingrese un numero:"
	Leer num

	Para i <- 1 Hasta 10 Hacer
		Escribir num, " x ", i, " = ", num * i
	FinPara
FinAlgoritmo
```

---

## 9.2 Mientras

Se usa cuando no sabemos exactamente cuántas veces se repetirá.

```pseint
Mientras condicion Hacer
	instrucciones
FinMientras
```

### Ejemplo
```pseint
Algoritmo contar_hasta_5
	Definir i Como Entero
	i <- 1

	Mientras i <= 5 Hacer
		Escribir i
		i <- i + 1
	FinMientras
FinAlgoritmo
```

---

## 9.3 Repetir Hasta Que

Primero ejecuta y luego evalúa la condición.

```pseint
Repetir
	instrucciones
Hasta Que condicion
```

### Ejemplo
```pseint
Algoritmo repetir_hasta_salir
	Definir opcion Como Entero

	Repetir
		Escribir "Ingrese 0 para salir:"
		Leer opcion
	Hasta Que opcion = 0
FinAlgoritmo
```

---

# 10. Contadores y acumuladores

## 10.1 Contador

Un contador aumenta normalmente de 1 en 1.

```pseint
contador <- contador + 1
```

Ejemplo:
```pseint
Algoritmo contar_pares
	Definir i, num, contador Como Entero
	contador <- 0

	Para i <- 1 Hasta 5 Hacer
		Escribir "Ingrese un numero:"
		Leer num

		Si num MOD 2 = 0 Entonces
			contador <- contador + 1
		FinSi
	FinPara

	Escribir "Cantidad de pares: ", contador
FinAlgoritmo
```

---

## 10.2 Acumulador

Un acumulador guarda sumas progresivas.

```pseint
suma <- suma + valor
```

Ejemplo:
```pseint
Algoritmo suma_numeros
	Definir i, num, suma Como Entero
	suma <- 0

	Para i <- 1 Hasta 5 Hacer
		Escribir "Ingrese un numero:"
		Leer num
		suma <- suma + num
	FinPara

	Escribir "La suma total es: ", suma
FinAlgoritmo
```

---

## 10.3 Promedio usando acumulador

```pseint
Algoritmo promedio_5_notas
	Definir i Como Entero
	Definir nota, suma, promedio Como Real

	suma <- 0

	Para i <- 1 Hasta 5 Hacer
		Escribir "Ingrese nota ", i, ":"
		Leer nota
		suma <- suma + nota
	FinPara

	promedio <- suma / 5

	Escribir "Promedio: ", promedio
FinAlgoritmo
```

---

# 11. Menús

Los menús se usan para ofrecer opciones al usuario.

## 11.1 Estructura básica

```pseint
Repetir
	Escribir "1. Opcion 1"
	Escribir "2. Opcion 2"
	Escribir "0. Salir"
	Leer opcion

	Segun opcion Hacer
		1:
			Escribir "Elegiste opcion 1"
		2:
			Escribir "Elegiste opcion 2"
		0:
			Escribir "Saliendo..."
		De Otro Modo:
			Escribir "Opcion invalida"
	FinSegun
Hasta Que opcion = 0
```

---

## 11.2 Ejemplo completo: menú de puntaje

```pseint
Algoritmo menu_puntaje
	Definir opcion, puntaje Como Entero

	puntaje <- 0

	Repetir
		Escribir "----- MENU -----"
		Escribir "1. Agregar 1 punto"
		Escribir "2. Agregar 5 puntos"
		Escribir "3. Mostrar puntaje"
		Escribir "0. Salir"
		Leer opcion

		Segun opcion Hacer
			1:
				puntaje <- puntaje + 1
				Escribir "Se agrego 1 punto"
			2:
				puntaje <- puntaje + 5
				Escribir "Se agregaron 5 puntos"
			3:
				Escribir "Puntaje actual: ", puntaje
			0:
				Escribir "Puntaje final: ", puntaje
			De Otro Modo:
				Escribir "Opcion invalida"
		FinSegun
	Hasta Que opcion = 0
FinAlgoritmo
```

---

# 12. Arreglos

Los arreglos permiten guardar varios datos del mismo tipo.

## 12.1 Definir un arreglo

```pseint
Definir notas Como Real
Dimension notas[5]
```

Esto crea un arreglo de 5 posiciones.

---

## 12.2 Cargar datos en un arreglo

```pseint
Algoritmo arreglo_notas
	Definir notas Como Real
	Definir i Como Entero
	Dimension notas[5]

	Para i <- 1 Hasta 5 Hacer
		Escribir "Ingrese nota ", i, ":"
		Leer notas[i]
	FinPara

	Para i <- 1 Hasta 5 Hacer
		Escribir "Nota ", i, ": ", notas[i]
	FinPara
FinAlgoritmo
```

---

## 12.3 Buscar el mayor en un arreglo

```pseint
Algoritmo mayor_arreglo
	Definir numeros Como Entero
	Definir i, mayor Como Entero
	Dimension numeros[5]

	Para i <- 1 Hasta 5 Hacer
		Escribir "Ingrese numero ", i, ":"
		Leer numeros[i]
	FinPara

	mayor <- numeros[1]

	Para i <- 2 Hasta 5 Hacer
		Si numeros[i] > mayor Entonces
			mayor <- numeros[i]
		FinSi
	FinPara

	Escribir "El mayor es: ", mayor
FinAlgoritmo
```

---

# 13. Subprocesos

Los subprocesos sirven para dividir el problema en partes pequeñas.

## 13.1 Ejemplo básico

```pseint
SubProceso Saludar
	Escribir "Hola desde un subproceso"
FinSubProceso

Algoritmo ejemplo_subproceso
	Saludar
FinAlgoritmo
```

---

## 13.2 Subproceso con parámetros

```pseint
SubProceso MostrarDoble(numero)
	Escribir "El doble es: ", numero * 2
FinSubProceso

Algoritmo ejemplo_parametro
	Definir n Como Entero

	Escribir "Ingrese un numero:"
	Leer n

	MostrarDoble(n)
FinAlgoritmo
```

---

# 14. Buenas prácticas

## 14.1 Usar nombres claros
Mejor:
- `edad`
- `promedio`
- `contador`

Peor:
- `x`
- `a1`
- `dato123`

---

## 14.2 Ordenar el algoritmo
1. Declarar variables
2. Pedir datos
3. Procesar
4. Mostrar resultados

---

## 14.3 Indentar correctamente
La indentación ayuda a entender el código.

Correcto:
```pseint
Si edad >= 18 Entonces
	Escribir "Mayor de edad"
SiNo
	Escribir "Menor de edad"
FinSi
```

---

## 14.4 Validar entradas cuando sea necesario
Ejemplo:
```pseint
Si nota >= 1 Y nota <= 7 Entonces
	Escribir "Nota valida"
SiNo
	Escribir "Nota invalida"
FinSi
```

---

# 15. Errores comunes

## 15.1 No definir variables
Incorrecto:
```pseint
Leer edad
```

Correcto:
```pseint
Definir edad Como Entero
Leer edad
```

---

## 15.2 Confundir `=` con `<-`
- `=` se usa para comparar
- `<-` se usa para asignar

Incorrecto:
```pseint
edad = 20
```

Correcto:
```pseint
edad <- 20
```

---

## 15.3 No cerrar estructuras
Incorrecto:
```pseint
Si num > 0 Entonces
	Escribir "Positivo"
```

Correcto:
```pseint
Si num > 0 Entonces
	Escribir "Positivo"
FinSi
```

---

## 15.4 Dividir por cero
Siempre validar antes de dividir.

```pseint
Si cantidad > 0 Entonces
	promedio <- suma / cantidad
SiNo
	Escribir "No se puede calcular promedio"
FinSi
```

---

# 16. Ejercicios guiados

## Ejercicio 1: Suma de dos números

### Enunciado
Pedir dos números y mostrar la suma.

### Solución
```pseint
Algoritmo suma_dos_numeros
	Definir a, b, suma Como Entero

	Escribir "Ingrese el primer numero:"
	Leer a

	Escribir "Ingrese el segundo numero:"
	Leer b

	suma <- a + b

	Escribir "La suma es: ", suma
FinAlgoritmo
```

---

## Ejercicio 2: Par o impar

### Enunciado
Pedir un número e indicar si es par o impar.

### Solución
```pseint
Algoritmo par_o_impar
	Definir num Como Entero

	Escribir "Ingrese un numero:"
	Leer num

	Si num MOD 2 = 0 Entonces
		Escribir "Es par"
	SiNo
		Escribir "Es impar"
	FinSi
FinAlgoritmo
```

---

## Ejercicio 3: Mayor de tres números

### Enunciado
Pedir tres números y mostrar el mayor.

### Solución
```pseint
Algoritmo mayor_tres
	Definir a, b, c, mayor Como Entero

	Escribir "Ingrese numero 1:"
	Leer a
	Escribir "Ingrese numero 2:"
	Leer b
	Escribir "Ingrese numero 3:"
	Leer c

	mayor <- a

	Si b > mayor Entonces
		mayor <- b
	FinSi

	Si c > mayor Entonces
		mayor <- c
	FinSi

	Escribir "El mayor es: ", mayor
FinAlgoritmo
```

---

## Ejercicio 4: Promedio de notas

### Enunciado
Pedir 3 notas, calcular promedio y mostrar si aprueba con 4.0 o más.

### Solución
```pseint
Algoritmo promedio_notas
	Definir n1, n2, n3, promedio Como Real

	Escribir "Ingrese nota 1:"
	Leer n1
	Escribir "Ingrese nota 2:"
	Leer n2
	Escribir "Ingrese nota 3:"
	Leer n3

	promedio <- (n1 + n2 + n3) / 3

	Escribir "Promedio: ", promedio

	Si promedio >= 4 Entonces
		Escribir "Aprobado"
	SiNo
		Escribir "Reprobado"
	FinSi
FinAlgoritmo
```

---

## Ejercicio 5: Tabla de multiplicar

### Enunciado
Pedir un número y mostrar su tabla del 1 al 10.

### Solución
```pseint
Algoritmo tabla_multiplicar
	Definir num, i Como Entero

	Escribir "Ingrese un numero:"
	Leer num

	Para i <- 1 Hasta 10 Hacer
		Escribir num, " x ", i, " = ", num * i
	FinPara
FinAlgoritmo
```

---

## Ejercicio 6: Menú simple

### Enunciado
Crear un menú que permita sumar puntos hasta que el usuario salga.

### Solución
```pseint
Algoritmo menu_simple
	Definir opcion, puntaje Como Entero
	puntaje <- 0

	Repetir
		Escribir "1. Agregar 1 punto"
		Escribir "2. Agregar 5 puntos"
		Escribir "3. Mostrar puntaje"
		Escribir "0. Salir"
		Leer opcion

		Segun opcion Hacer
			1:
				puntaje <- puntaje + 1
			2:
				puntaje <- puntaje + 5
			3:
				Escribir "Puntaje actual: ", puntaje
			0:
				Escribir "Fin del programa"
			De Otro Modo:
				Escribir "Opcion invalida"
		FinSegun
	Hasta Que opcion = 0
FinAlgoritmo
```

---

# 17. Ejercicios propuestos

## Nivel básico
1. Pedir dos números y mostrar la resta
2. Pedir dos números y mostrar la multiplicación
3. Pedir un número y mostrar si es positivo o negativo
4. Pedir la edad de una persona e indicar si es mayor de edad
5. Pedir una nota e indicar si está aprobada o reprobada

## Nivel intermedio
6. Pedir 5 números y mostrar cuántos son positivos
7. Pedir 5 números y mostrar la suma total
8. Crear un programa que muestre los números del 1 al 20
9. Crear una tabla de multiplicar del 1 al 12
10. Pedir 4 notas y calcular promedio

## Nivel avanzado inicial
11. Crear un menú de compras
12. Crear un menú de registro de asistencia
13. Crear un sistema de cajero simple
14. Crear un programa que determine si un año es bisiesto
15. Crear un programa que permita registrar ventas y mostrar total acumulado

---

# 18. Mini proyecto final

## Sistema simple de ventas

### Enunciado
Desarrollar un programa con menú que permita:

1. Agregar producto de $1000
2. Agregar producto de $2500
3. Ver total
4. Aplicar descuento de 10%
0. Salir

### Reglas
- El descuento solo se puede aplicar una vez
- El programa debe repetir hasta salir
- Debe mostrar total final

### Solución
```pseint
Algoritmo sistema_ventas
	Definir opcion Como Entero
	Definir total Como Real
	Definir descuentoAplicado Como Logico

	total <- 0
	descuentoAplicado <- Falso

	Repetir
		Escribir "----- MENU -----"
		Escribir "1. Agregar producto de $1000"
		Escribir "2. Agregar producto de $2500"
		Escribir "3. Ver total"
		Escribir "4. Aplicar descuento 10%"
		Escribir "0. Salir"
		Leer opcion

		Segun opcion Hacer
			1:
				total <- total + 1000
				Escribir "Producto agregado"
			2:
				total <- total + 2500
				Escribir "Producto agregado"
			3:
				Escribir "Total actual: ", total
			4:
				Si descuentoAplicado = Falso Entonces
					total <- total - (total * 0.10)
					descuentoAplicado <- Verdadero
					Escribir "Descuento aplicado"
				SiNo
					Escribir "El descuento ya fue aplicado"
				FinSi
			0:
				Escribir "Total final: ", total
			De Otro Modo:
				Escribir "Opcion invalida"
		FinSegun
	Hasta Que opcion = 0
FinAlgoritmo
```

---

# 19. Consejos para aprender mejor

## 19.1 Primero entiende, luego copies
No basta con copiar código. Debes entender:
- qué entra
- qué proceso ocurre
- qué sale

## 19.2 Practica todos los días
Aunque sea 15 o 20 minutos.

## 19.3 Cambia ejemplos
Si un ejercicio suma 2 números, luego modifica el código para sumar 3 o 4.

## 19.4 Comete errores y corrígelos
Aprender programación también significa equivocarse y revisar.

## 19.5 Explica en voz alta
Si puedes explicar un algoritmo con tus palabras, ya lo estás entendiendo.

---

# Cierre

Si dominas esta guía, ya deberías poder trabajar con:

- Variables
- Operaciones
- Entrada y salida
- Condicionales
- Ciclos
- Contadores
- Acumuladores
- Menús
- Arreglos
- Subprocesos

El siguiente paso natural después de PSeInt suele ser pasar a un lenguaje real como **Python**.

---

# Sugerencia de estructura para un repositorio

```bash
pseint-desde-cero/
├── README.md
├── ejemplos/
│   ├── 01_hola_mundo.psc
│   ├── 02_variables.psc
│   ├── 03_condicionales.psc
│   ├── 04_ciclos.psc
│   ├── 05_menus.psc
│   └── 06_arreglos.psc
└── ejercicios/
    ├── basicos.md
    ├── intermedios.md
    └── proyecto_final.md
```

---

# Licencia

Uso educativo.
