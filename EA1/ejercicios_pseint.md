# Guía de Ejercicios Resueltos en PSeInt
## Programación básica: de lo más simple a lo más complejo

Esta guía reúne ejercicios básicos e intermedios de programación en **PSeInt**, ordenados por dificultad.  
Incluye:

- Enunciado
- Objetivo
- Solución en PSeInt
- Progresión de dificultad

> Material base ampliado a partir de una colección de ejercicios sobre control de acceso, promedios, años bisiestos, menús, acumuladores y problemas de lógica. 

---

## Contenidos

1. [Suma de dos números](#1-suma-de-dos-números)
2. [Resta de dos números](#2-resta-de-dos-números)
3. [Multiplicación de dos números](#3-multiplicación-de-dos-números)
4. [Número par o impar](#4-número-par-o-impar)
5. [Número positivo, negativo o cero](#5-número-positivo-negativo-o-cero)
6. [Mayor de dos números](#6-mayor-de-dos-números)
7. [Mayor de tres números](#7-mayor-de-tres-números)
8. [Promedio de 3 notas](#8-promedio-de-3-notas)
9. [Validación simple de nota](#9-validación-simple-de-nota)
10. [Control de acceso a una sala](#10-control-de-acceso-a-una-sala)
11. [Descuento según compra](#11-descuento-según-compra)
12. [Tabla de multiplicar](#12-tabla-de-multiplicar)
13. [Contar del 1 al 10](#13-contar-del-1-al-10)
14. [Suma de los primeros N números](#14-suma-de-los-primeros-n-números)
15. [Contador de números pares](#15-contador-de-números-pares)
16. [Menú de puntaje](#16-menú-de-puntaje)
17. [Menú contador de acciones](#17-menú-contador-de-acciones)
18. [Menú de compras con descuento](#18-menú-de-compras-con-descuento)
19. [Sistema de atención de clínica](#19-sistema-de-atención-de-clínica)
20. [Año bisiesto](#20-año-bisiesto)
21. [Resultado de un set de tenis](#21-resultado-de-un-set-de-tenis)
22. [Cajero simple](#22-cajero-simple)
23. [Registro de asistencia](#23-registro-de-asistencia)
24. [Menú de notas de estudiantes](#24-menú-de-notas-de-estudiantes)

---

# 1. Suma de dos números

## Enunciado
Solicitar dos números al usuario y mostrar su suma.

## Objetivo
Trabajar con variables, entrada de datos y operaciones básicas.

## Solución en PSeInt
```pseint
Algoritmo suma_dos_numeros
	Definir num1, num2, suma Como Entero

	Escribir "Ingrese el primer numero:"
	Leer num1

	Escribir "Ingrese el segundo numero:"
	Leer num2

	suma <- num1 + num2

	Escribir "La suma es: ", suma
FinAlgoritmo
```

---

# 2. Resta de dos números

## Enunciado
Solicitar dos números y mostrar la resta del primero menos el segundo.

## Solución en PSeInt
```pseint
Algoritmo resta_dos_numeros
	Definir num1, num2, resta Como Entero

	Escribir "Ingrese el primer numero:"
	Leer num1

	Escribir "Ingrese el segundo numero:"
	Leer num2

	resta <- num1 - num2

	Escribir "La resta es: ", resta
FinAlgoritmo
```

---

# 3. Multiplicación de dos números

## Enunciado
Solicitar dos números y mostrar su multiplicación.

## Solución en PSeInt
```pseudocode
Algoritmo multiplicacion_dos_numeros
	Definir num1, num2, resultado Como Entero

	Escribir "Ingrese el primer numero:"
	Leer num1

	Escribir "Ingrese el segundo numero:"
	Leer num2

	resultado <- num1 * num2

	Escribir "La multiplicacion es: ", resultado
FinAlgoritmo
```

---

# 4. Número par o impar

## Enunciado
Solicitar un número e indicar si es par o impar.

## Solución en PSeInt
```pseint
Algoritmo numero_par_o_impar
	Definir num Como Entero

	Escribir "Ingrese un numero:"
	Leer num

	Si num MOD 2 = 0 Entonces
		Escribir "El numero es par"
	SiNo
		Escribir "El numero es impar"
	FinSi
FinAlgoritmo
```

---

# 5. Número positivo, negativo o cero

## Enunciado
Solicitar un número e indicar si es positivo, negativo o cero.

## Solución en PSeInt
```pseint
Algoritmo signo_numero
	Definir num Como Entero

	Escribir "Ingrese un numero:"
	Leer num

	Si num > 0 Entonces
		Escribir "El numero es positivo"
	SiNo
		Si num < 0 Entonces
			Escribir "El numero es negativo"
		SiNo
			Escribir "El numero es cero"
		FinSi
	FinSi
FinAlgoritmo
```

---

# 6. Mayor de dos números

## Enunciado
Solicitar dos números e indicar cuál es mayor.

## Solución en PSeInt
```pseint
Algoritmo mayor_de_dos
	Definir num1, num2 Como Entero

	Escribir "Ingrese el primer numero:"
	Leer num1

	Escribir "Ingrese el segundo numero:"
	Leer num2

	Si num1 > num2 Entonces
		Escribir "El mayor es: ", num1
	SiNo
		Si num2 > num1 Entonces
			Escribir "El mayor es: ", num2
		SiNo
			Escribir "Ambos numeros son iguales"
		FinSi
	FinSi
FinAlgoritmo
```

---

# 7. Mayor de tres números

## Enunciado
Solicitar tres números e indicar cuál es el mayor.

## Solución en PSeInt
```pseint
Algoritmo mayor_de_tres
	Definir a, b, c, mayor Como Entero

	Escribir "Ingrese el primer numero:"
	Leer a
	Escribir "Ingrese el segundo numero:"
	Leer b
	Escribir "Ingrese el tercer numero:"
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

# 8. Promedio de 3 notas

## Enunciado
Pedir 3 notas, validarlas entre 1 y 7, calcular el promedio y mostrar un mensaje según el resultado.

## Solución en PSeInt
```pseint
Algoritmo calcular_promedio
	Definir nota1, nota2, nota3, promedio Como Real

	Escribir "Ingrese la nota 1:"
	Leer nota1

	Si nota1 >= 1 Y nota1 <= 7 Entonces
		Escribir "Ingrese la nota 2:"
		Leer nota2

		Si nota2 >= 1 Y nota2 <= 7 Entonces
			Escribir "Ingrese la nota 3:"
			Leer nota3

			Si nota3 >= 1 Y nota3 <= 7 Entonces
				promedio <- (nota1 + nota2 + nota3) / 3

				Si promedio < 4 Entonces
					Escribir "Reprobaste"
				SiNo
					Si promedio < 6 Entonces
						Escribir "Ponte las pilas"
					SiNo
						Escribir "Aprobaste"
					FinSi
				FinSi
			SiNo
				Escribir "Error en nota 3"
			FinSi
		SiNo
			Escribir "Error en nota 2"
		FinSi
	SiNo
		Escribir "Error en nota 1"
	FinSi
FinAlgoritmo
```

---

# 9. Validación simple de nota

## Enunciado
Solicitar una nota y validar si está entre 1 y 7.

## Solución en PSeInt
```pseint
Algoritmo validar_nota
	Definir nota Como Real

	Escribir "Ingrese una nota:"
	Leer nota

	Si nota >= 1 Y nota <= 7 Entonces
		Escribir "Nota valida"
	SiNo
		Escribir "Nota invalida"
	FinSi
FinAlgoritmo
```

---

# 10. Control de acceso a una sala

## Enunciado
En un laboratorio se debe decidir si una persona puede ingresar.

### Reglas
- Debe tener credencial activa
- Debe ser horario permitido
- Si es estudiante nuevo, debe venir acompañado

## Solución en PSeInt
```pseint
Algoritmo control_acceso
	Definir credencial, horario, esNuevo, acompanado Como Entero

	Escribir "¿Tiene credencial activa? (1=Si, 0=No)"
	Leer credencial

	Escribir "¿Es horario permitido? (1=Si, 0=No)"
	Leer horario

	Escribir "¿Es estudiante nuevo? (1=Si, 0=No)"
	Leer esNuevo

	Escribir "¿Viene acompanado? (1=Si, 0=No)"
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

# 11. Descuento según compra

## Enunciado
Solicitar el monto de una compra.  
Si la compra es mayor o igual a 20000, aplicar un descuento del 10%.

## Solución en PSeInt
```pseint
Algoritmo descuento_compra
	Definir compra, total Como Real

	Escribir "Ingrese el monto de la compra:"
	Leer compra

	Si compra >= 20000 Entonces
		total <- compra - (compra * 0.10)
		Escribir "Se aplico descuento"
	SiNo
		total <- compra
		Escribir "No se aplica descuento"
	FinSi

	Escribir "Total a pagar: ", total
FinAlgoritmo
```

---

# 12. Tabla de multiplicar

## Enunciado
Solicitar un número y mostrar su tabla de multiplicar del 1 al 10.

## Solución en PSeInt
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

# 13. Contar del 1 al 10

## Enunciado
Mostrar en pantalla los números del 1 al 10.

## Solución en PSeInt
```pseint
Algoritmo contar_1_10
	Definir i Como Entero

	Para i <- 1 Hasta 10 Hacer
		Escribir i
	FinPara
FinAlgoritmo
```

---

# 14. Suma de los primeros N números

## Enunciado
Solicitar un número `N` y sumar desde 1 hasta `N`.

## Solución en PSeInt
```pseint
Algoritmo suma_hasta_n
	Definir n, i, suma Como Entero

	Escribir "Ingrese un numero:"
	Leer n

	suma <- 0

	Para i <- 1 Hasta n Hacer
		suma <- suma + i
	FinPara

	Escribir "La suma es: ", suma
FinAlgoritmo
```

---

# 15. Contador de números pares

## Enunciado
Solicitar 5 números y contar cuántos son pares.

## Solución en PSeInt
```pseint
Algoritmo contar_pares
	Definir num, i, contador Como Entero

	contador <- 0

	Para i <- 1 Hasta 5 Hacer
		Escribir "Ingrese un numero:"
		Leer num

		Si num MOD 2 = 0 Entonces
			contador <- contador + 1
		FinSi
	FinPara

	Escribir "Cantidad de numeros pares: ", contador
FinAlgoritmo
```

---

# 16. Menú de puntaje

## Enunciado
Crear un menú que permita:
- Agregar 1 punto
- Agregar 5 puntos
- Mostrar puntaje
- Salir

## Solución en PSeInt
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
		Escribir "Ingrese una opcion:"
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

# 17. Menú contador de acciones

## Enunciado
Crear un menú que permita:
- Registrar ingreso de cliente
- Registrar venta
- Mostrar resumen
- Salir

## Solución en PSeInt
```pseint
Algoritmo menu_contador_acciones
	Definir opcion, ingresos, ventas Como Entero

	ingresos <- 0
	ventas <- 0

	Repetir
		Escribir "----- MENU -----"
		Escribir "1. Registrar ingreso de cliente"
		Escribir "2. Registrar venta"
		Escribir "3. Mostrar resumen"
		Escribir "0. Salir"
		Escribir "Ingrese una opcion:"
		Leer opcion

		Segun opcion Hacer
			1:
				ingresos <- ingresos + 1
				Escribir "Ingreso registrado"
			2:
				ventas <- ventas + 1
				Escribir "Venta registrada"
			3:
				Escribir "Resumen:"
				Escribir "Ingresos: ", ingresos
				Escribir "Ventas: ", ventas
			0:
				Escribir "Programa finalizado"
			De Otro Modo:
				Escribir "Opcion invalida"
		FinSegun
	Hasta Que opcion = 0
FinAlgoritmo
```

---

# 18. Menú de compras con descuento

## Enunciado
Crear un sistema simple de compras con las siguientes opciones:
- Agregar producto de $1000
- Agregar producto de $2500
- Ver total acumulado
- Aplicar descuento de 10%
- Salir

### Reglas
- El descuento solo puede aplicarse una vez
- El total no debe quedar negativo

## Solución en PSeInt
```pseint
Algoritmo menu_compras
	Definir opcion Como Entero
	Definir total Como Real
	Definir descuentoAplicado Como Logico

	total <- 0
	descuentoAplicado <- Falso

	Repetir
		Escribir "----- MENU -----"
		Escribir "1. Agregar producto ($1000)"
		Escribir "2. Agregar producto ($2500)"
		Escribir "3. Ver total acumulado"
		Escribir "4. Aplicar descuento del 10%"
		Escribir "0. Salir"
		Escribir "Ingrese una opcion:"
		Leer opcion

		Segun opcion Hacer
			1:
				total <- total + 1000
				Escribir "Producto agregado ($1000)"
			2:
				total <- total + 2500
				Escribir "Producto agregado ($2500)"
			3:
				Escribir "Total actual: ", total
			4:
				Si descuentoAplicado = Falso Entonces
					total <- total - (total * 0.10)

					Si total < 0 Entonces
						total <- 0
					FinSi

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

# 19. Sistema de atención de clínica

## Enunciado
Crear un menú que permita:
- Registrar paciente normal
- Registrar paciente con urgencia
- Mostrar resumen
- Mostrar porcentaje de urgencias
- Salir

## Solución en PSeInt
```pseint
Algoritmo sistema_clinica
	Definir opcion, normales, urgencias, total Como Entero
	Definir porcentaje Como Real

	normales <- 0
	urgencias <- 0
	total <- 0

	Repetir
		Escribir "----- MENU -----"
		Escribir "1. Paciente normal"
		Escribir "2. Paciente urgencia"
		Escribir "3. Ver resumen"
		Escribir "4. Ver porcentaje urgencias"
		Escribir "0. Salir"
		Escribir "Ingrese una opcion:"
		Leer opcion

		Segun opcion Hacer
			1:
				normales <- normales + 1
				total <- total + 1
				Escribir "Paciente registrado"
			2:
				urgencias <- urgencias + 1
				total <- total + 1
				Escribir "Paciente urgencia registrado"
			3:
				Escribir "Normales: ", normales
				Escribir "Urgencias: ", urgencias
				Escribir "Total: ", total
			4:
				Si total > 0 Entonces
					porcentaje <- (urgencias * 100) / total
					Escribir "Porcentaje de urgencias: ", porcentaje, "%"
				SiNo
					Escribir "No hay pacientes registrados"
				FinSi
			0:
				Escribir "Resumen final:"
				Escribir "Normales: ", normales
				Escribir "Urgencias: ", urgencias
				Escribir "Total: ", total
			De Otro Modo:
				Escribir "Opcion invalida"
		FinSegun
	Hasta Que opcion = 0
FinAlgoritmo
```

---

# 20. Año bisiesto

## Enunciado
Determinar si un año es bisiesto considerando:
- Si el año es menor a 1582, se usa la regla juliana
- Si el año es 1582 o mayor, se usa la regla gregoriana

## Solución en PSeInt
```pseint
Algoritmo anio_bisiesto
	Definir anio Como Entero

	Escribir "Ingrese un anio:"
	Leer anio

	Si anio < 1582 Entonces
		Si anio MOD 4 = 0 Entonces
			Escribir anio, " es bisiesto"
		SiNo
			Escribir anio, " no es bisiesto"
		FinSi
	SiNo
		Si (anio MOD 400 = 0) O (anio MOD 4 = 0 Y anio MOD 100 <> 0) Entonces
			Escribir anio, " es bisiesto"
		SiNo
			Escribir anio, " no es bisiesto"
		FinSi
	FinSi
FinAlgoritmo
```

---

# 21. Resultado de un set de tenis

## Enunciado
Dados los juegos ganados por A y B, indicar si:
- Ganó A
- Ganó B
- Aún no termina
- Es inválido

## Solución en PSeInt
```pseint
Algoritmo set_tenis
	Definir a, b Como Entero

	Escribir "Juegos ganados por A:"
	Leer a

	Escribir "Juegos ganados por B:"
	Leer b

	Si a < 0 O b < 0 Entonces
		Escribir "Invalido"
	SiNo
		Si a > 7 O b > 7 Entonces
			Escribir "Invalido"
		SiNo
			Si a = 7 Y (b = 5 O b = 6) Entonces
				Escribir "Gano A"
			SiNo
				Si b = 7 Y (a = 5 O a = 6) Entonces
					Escribir "Gano B"
				SiNo
					Si a = 6 Y b <= 4 Entonces
						Escribir "Gano A"
					SiNo
						Si b = 6 Y a <= 4 Entonces
							Escribir "Gano B"
						SiNo
							Si a <= 6 Y b <= 6 Entonces
								Escribir "Aun no termina"
							SiNo
								Escribir "Invalido"
							FinSi
						FinSi
					FinSi
				FinSi
			FinSi
		FinSi
	FinSi
FinAlgoritmo
```

---

# 22. Cajero simple

## Enunciado
Simular un cajero con saldo inicial de 10000.  
Opciones:
- Consultar saldo
- Depositar dinero
- Girar dinero
- Salir

## Solución en PSeInt
```pseint
Algoritmo cajero_simple
	Definir opcion Como Entero
	Definir saldo, monto Como Real

	saldo <- 10000

	Repetir
		Escribir "----- CAJERO -----"
		Escribir "1. Consultar saldo"
		Escribir "2. Depositar dinero"
		Escribir "3. Girar dinero"
		Escribir "0. Salir"
		Escribir "Ingrese una opcion:"
		Leer opcion

		Segun opcion Hacer
			1:
				Escribir "Saldo actual: ", saldo
			2:
				Escribir "Ingrese monto a depositar:"
				Leer monto
				Si monto > 0 Entonces
					saldo <- saldo + monto
					Escribir "Deposito realizado"
				SiNo
					Escribir "Monto invalido"
				FinSi
			3:
				Escribir "Ingrese monto a girar:"
				Leer monto
				Si monto > 0 Y monto <= saldo Entonces
					saldo <- saldo - monto
					Escribir "Giro realizado"
				SiNo
					Escribir "No es posible realizar el giro"
				FinSi
			0:
				Escribir "Gracias por usar el cajero"
			De Otro Modo:
				Escribir "Opcion invalida"
		FinSegun
	Hasta Que opcion = 0
FinAlgoritmo
```

---

# 23. Registro de asistencia

## Enunciado
Solicitar la asistencia de 5 estudiantes.  
Ingresar 1 si asistió y 0 si no asistió.  
Mostrar cuántos asistieron y cuántos faltaron.

## Solución en PSeInt
```pseint
Algoritmo registro_asistencia
	Definir i, asistencia, presentes, ausentes Como Entero

	presentes <- 0
	ausentes <- 0

	Para i <- 1 Hasta 5 Hacer
		Escribir "Estudiante ", i, ": ¿Asistio? (1=Si, 0=No)"
		Leer asistencia

		Si asistencia = 1 Entonces
			presentes <- presentes + 1
		SiNo
			ausentes <- ausentes + 1
		FinSi
	FinPara

	Escribir "Presentes: ", presentes
	Escribir "Ausentes: ", ausentes
FinAlgoritmo
```

---

# 24. Menú de notas de estudiantes

## Enunciado
Crear un menú que permita:
- Ingresar una nota
- Mostrar promedio de notas ingresadas
- Mostrar cantidad de aprobados
- Salir

### Reglas
- Las notas válidas van de 1 a 7
- Solo contar aprobados con nota mayor o igual a 4

## Solución en PSeInt
```pseint
Algoritmo menu_notas_estudiantes
	Definir opcion, cantidad, aprobados Como Entero
	Definir nota, suma, promedio Como Real

	cantidad <- 0
	aprobados <- 0
	suma <- 0

	Repetir
		Escribir "----- MENU NOTAS -----"
		Escribir "1. Ingresar nota"
		Escribir "2. Mostrar promedio"
		Escribir "3. Mostrar cantidad de aprobados"
		Escribir "0. Salir"
		Escribir "Ingrese una opcion:"
		Leer opcion

		Segun opcion Hacer
			1:
				Escribir "Ingrese una nota:"
				Leer nota

				Si nota >= 1 Y nota <= 7 Entonces
					suma <- suma + nota
					cantidad <- cantidad + 1

					Si nota >= 4 Entonces
						aprobados <- aprobados + 1
					FinSi

					Escribir "Nota registrada"
				SiNo
					Escribir "Nota invalida"
				FinSi
			2:
				Si cantidad > 0 Entonces
					promedio <- suma / cantidad
					Escribir "Promedio: ", promedio
				SiNo
					Escribir "No hay notas registradas"
				FinSi
			3:
				Escribir "Cantidad de aprobados: ", aprobados
			0:
				Escribir "Programa finalizado"
			De Otro Modo:
				Escribir "Opcion invalida"
		FinSegun
	Hasta Que opcion = 0
FinAlgoritmo
```

---

# Progresión recomendada

## Nivel 1: Muy básico
- Suma de dos números
- Resta de dos números
- Multiplicación de dos números
- Número par o impar
- Número positivo, negativo o cero

## Nivel 2: Condicionales
- Mayor de dos números
- Mayor de tres números
- Validación simple de nota
- Descuento según compra
- Control de acceso a una sala

## Nivel 3: Ciclos
- Contar del 1 al 10
- Tabla de multiplicar
- Suma de los primeros N números
- Contador de números pares
- Registro de asistencia

## Nivel 4: Menús, contadores y acumuladores
- Menú de puntaje
- Menú contador de acciones
- Menú de compras con descuento
- Sistema de atención de clínica
- Cajero simple
- Menú de notas de estudiantes

## Nivel 5: Lógica más compleja
- Año bisiesto
- Resultado de un set de tenis

---

# Sugerencia de uso en clases

Una forma práctica de trabajar esta guía es:

1. Resolver primero los ejercicios de nivel 1 y 2
2. Luego practicar ciclos con los ejercicios de nivel 3
3. Después pasar a menús con contadores y acumuladores
4. Finalizar con problemas de lógica más compleja

---

# Repositorio sugerido

Puedes guardar este archivo como:

```bash
README.md
```

Y si quieres organizar mejor el repositorio, puedes dejar una estructura como esta:

```bash
pseint-ejercicios/
├── README.md
├── ejercicios/
│   ├── 01_suma.psc
│   ├── 02_resta.psc
│   ├── 03_multiplicacion.psc
│   ├── 04_par_impar.psc
│   ├── 05_signo.psc
│   ├── 06_mayor_dos.psc
│   ├── 07_mayor_tres.psc
│   ├── 08_promedio.psc
│   ├── 09_validar_nota.psc
│   ├── 10_control_acceso.psc
│   ├── 11_descuento.psc
│   ├── 12_tabla.psc
│   ├── 13_contar_1_10.psc
│   ├── 14_suma_hasta_n.psc
│   ├── 15_contar_pares.psc
│   ├── 16_menu_puntaje.psc
│   ├── 17_menu_contador.psc
│   ├── 18_menu_compras.psc
│   ├── 19_sistema_clinica.psc
│   ├── 20_anio_bisiesto.psc
│   ├── 21_set_tenis.psc
│   ├── 22_cajero_simple.psc
│   ├── 23_registro_asistencia.psc
│   └── 24_menu_notas.psc
```

---

# Licencia

Uso educativo.
