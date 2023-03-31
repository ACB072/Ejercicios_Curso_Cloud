# Ejercicios con algoritmos



## Antonio Miralles Gutiérrez



### Ejercicio 1



*Calcular la letra del DNI Español*



**Paso 1**: Definir el problema
Encontrar la letra del dni según el numero introducido



**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

El programa recibe como entrada el numero de dni de 8 digitos y sea un numero entero

Se crea una cadena con el codigo TRWAGMYFPDXBNJZSQVHLCKE, donde cada letra consiste en un numero entre 0 y 22 respectivamente.

**Proceso:**

- Introducir numero de dni

- Validar el numero de digitos del dni
  - Si no es valido, se muestra un mensaje de error

- Se define la cadena

- Se divide el numero del dni y se guarda el resto

- Se recorre la cadena y se comprueba el el resto con el numero de la cadena

- Si se encuentra, se guarda la letra 

- Se sale del bucle, se devuelve la letra

**Salida:**

Se devuelve la letra

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo DNI
dni <- leer entrada

si longitud(dni) diferente 8 o dni diferente de entero
	Error, DNI Invalido
finsi

sino
	letra <- ""
    cadena[] <- [T,R,W,A,G,M,Y,F,P,D,X,B,N,J,Z,S,Q,V,H,L,C,K,E]
    resultadoResto <- dni mod 23

    para contador=0 mientras resto!=cadena[i] con paso 1
        si resultadoResto == cadena[contador]
            letra <-cadena[contador]
        finsi
    finpara

    devolver letra
    
finsi

FIN algoritmo
```

Sub-Algoritmo

Validacion de DNI

```
Inicio
cadena_dni[7]
mientras dni mayor  o igual que 1 hacer
	DNI <- DNI/10
	contador <- 1
fin mientras

si contador diferente de 8
	Imprimir "El numero no es valido"
sino
	Imprimir "El numero es valido"
finsi
	
```



# Ejercicio 2

Calcular el salario de un empleado



**Paso1: Definir el problema**

El salario en España se calcula a partir del salario bruto anual, que incluye todas las percepciones económicas que recibe un trabajador durante un año, incluyendo salario base, pagas extra, complementos y otros conceptos retributivos.



A partir del salario bruto se deducen las cotizaciones a la seguridad Social y el impuesto sobre la renta de las personas fisicas (IRPF) que varían en función del nivel salarial y la situación de personal del trabajador.



**Paso 2: Poner la entrada, el proceso y la salida**

Entrada: ```salarioBase```, ```pagasExtras```, ```complementos```, ```otrosConceptos```, ```IRP```, ```SeguridadSocial```



**Proceso:**



- Sumar ```salarioBase```, ```pagasExtras```, ```complementos```, ```otrosConceptosRetributivos``` y lo asigno a ```salarioBruto```

- Sumar ```IRP```, ```SeguridadSocial``` y lo asigno a ```deducciones```

- ```salarioNeto``` se le asigna ```salarioBruto - deducciones```

**Salida**

Escribir ```salarioNeto``` y ```salarioBruto```

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo Salario

	salarioBase<- Leer()
    pagasExtras<- Leer()
    complementos<- Leer()
    otrosConceptos<- Leer()
    IRP<- Leer()
    seguridadSocial<- Leer()

    salarioBruto<- salarioBase+pagasExtras+complementos+otrosConceptos
    deducciones <- IRP + seg

FIN algoritmo
```

### Ejercicio 4



*Calcular el perimetro y el area de un circulo dado su radio *



**Paso 1**: Definir el problema
Realizar formulas que calculen el perimetro y el area de un circulo segun el radio introducido por el usuario

Para calcular el área del circulo a partir del radio, se utiliza la formula A= pi * r^2, y para el perimetro se usa P= 2(pi) * r.

**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

El programa recibira de entrada el `radio` del circulo, introducido por el usuario, y el numero `pi`, el cual tiene un valor fijo. 

**Proceso:**

- Validar que el radio sea valido, por ejemplo que no sea negativo

  - Si no es valido, se muestra un mensaje de error

- Se define el numero `pi`

- Se define la variable `area`y la variable `perimetro`

- Se calcula el area con la formula dicha en el paso 1 y se almacena en `area`

- Se calcula el perimetro con la formula dicha en en el paso 1 y se almacena en `perimetro`

- Se impime/retorna `area `  y `perimetro`

  

**Salida:**

Se impime/retorna `area `  y `perimetro`

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo Circulo
	#Entrada
    pi <- 3.14159265359...
    area <- 0
    perimetro <- 0
    radio <- leer entrada
	
	#Proceso
    si radio>0 
        imprimir Error, el radio no puede ser menor que 0
    sino
        area <- pi * (radio*radio)
        perimetro <- 2(pi) * radio
    finsi
    
	#Salida
    Imprimir area
    Imprimir perimetro

Fin
```

### Ejercicio 5



*Dada una lista de números enteros, determina cuál es el mayor y cuál es el menor. Para ello introducimos una lista de números y comprobamos uno a uno si es mayor que la variable mayor o menor que la variable menor*



**Paso 1**: Definir el problema
Encontrar entre una lista de numeros el numero mayor y menor de toda la lista

**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

El programa recibe de entrada la cadena de numeros a analizar y se crea una variable `mayor` y `menor` inicializadas a 0 y 1000000 respectivamente. 

**Proceso:**

- Introducir la cadena de numeros mediante un bucle y guardarlo en `cadena_numerica` hasta que el usuario introduzca 0

- Validar que sean números 

  - Si no es valido, se muestra un mensaje de error

- Se define la variable `mayor` y `menor`

- Se inicia el bucle que recorre la cadena de numeros introducidos

- Se comprueba un numero de la cadena

- Se compara con `mayor` y `menor`. Si es mayor que `mayor`, se sustituye, lo mismo que si es menor que `menor`

- Una vez se haya llegado al final de la lista, muestra los valores `mayor` y `menor`

  

  

**Salida:**

Se impime/retorna `mayor `  y `menor`

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo MayorMenor

    #Entrada
    para i<-0 mientras cadena_numerica[i] diferente -1 con paso 1
        cadena_numerica[i] <- leer entrada
        si cadena_numerica[i] diferente numero_entero
            imprimir "Error, debe ser un numero"
        finsi
    finpara

    mayor<-0
    menor<-1000000

    #Proceso
    para i<-0  mientras cadena_numerica[] diferente -1 con paso 1 hacer
        si cadena_numerica[i]<- -1 entonces
            Imprimir "Fin del bucle"
        sino si cadena_numerica[i] > mayor entonces
            mayor<-cadena_numerica[i]
        sino si cadena_numerica[i] < menor entonces
            menor<-cadena_numerica[i]
        finsi
    fin para

    #Salida
    Imprimir mayor
    Imprimir menor

Fin
```

### Ejercicio 6



*Crea un algoritmo que convierta grados Celsius a Fahrenheit.*



**Paso 1**: Definir el problema
Convertir un numero en grados Celsius, a grados Farenheit. Para convertir de grados celsius a farenheit se usa la siguiente formula : (C * (9/5)) + 32. Siendo C los grados celsius.

**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

El programa recibe de entrada un numero en grados celsius.

**Proceso:**

- Introducir el  numero en grados celsius
- Validar que sean números
  - Si no es valido, se muestra un mensaje de error
- Se define la variable `resultado` 
- Se realiza la formula definida anteriormente, y se almacena en `resultado`
- Se imprime `resultado`

**Salida:**

Se impime/retorna `resultado ` 

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo CelsiusFarenheit

    #Entrada
    grado_celsius <- leer entrada
    resultado <- 0

    #Proceso
    si grado_celsius != numero entonces
        imprimir Error, el grado_celsius debe ser un numero
    sino
        resultado <- (grado_celsius * (9/5)) + 32
    finsi

    #Salida
    Imprimir resultado

Fin
```

### Ejercicio 7



*Dado un número entero, crea un algoritmo que determine si es par o impar.*



**Paso 1**: Definir el problema
Comprobar si un numero es par o impar. Para ello, si al dividirlo entre dos y el resto es 0, sera par, sino, sera impar

**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

El programa recibe de entrada un numero para comprobar.

**Proceso:**

- Introducir el  numero 
- Validar que sean números
  - Si no es valido, se muestra un mensaje de error
- Se define la variable `resultado` 
- Se realiza la formula definida anteriormente, y se almacena en `resultado`
- Se comprueba si `resultado` es 0
  - Si es 0, se imprime Par
  - SIno, se imprime impar


**Salida:**

Se impime "Par" o "Impar" dependiendo del valor en la variable `resultado`

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo ParImpar

    #Entrada
    parimpar <- leer entrada
    resultado <- 0
    si parimpar != numero
        imprimir Error, el parimpar debe ser un numero
    sino

        #Proceso
        resultado <- parimpar % 2

        #Salida
        si resultado == 0 entonces
            Imprimir "El numero es par"
        sino
            Imprimir "El numero es impar"
        finsi
    finsi
Fin
```

### Ejercicio 8



*Crea un algoritmo que determine si un año es bisiesto o no.*



**Paso 1**: Definir el problema
Comprobar si un año es bisiesto. Para ello, si al dividirlo entre cuatro y el resto es 0, sera bisiesto, sino, no

**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

El programa recibe de entrada un numero para comprobar.

**Proceso:**

- Introducir el  numero 
- Validar que sean números
  - Si no es valido, se muestra un mensaje de error
- Se define la variable `resultado` 
- Se realiza la formula definida anteriormente, y se almacena en `resultado`
- Se comprueba si `resultado` es 0
  - Si es 0, se imprime Bisiesto
  - SIno, se imprime No Bisiesto

**Salida:**

Se impime "Bisiesto" o " No Bisiesto" dependiendo del valor en la variable `resultado`

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo Bisiesto

    #Entrada
    bisiesto <- leer entrada
    resultado <- 0
    si bisiesto != numero
        imprimir Error,  bisiesto debe ser un numero
    sino
        #Proceso
        resultado <- bisiesto mod 4

        #Salida
        si bisiesto == 0 entonces
            Imprimir "El año es bisiesto"
        sino
            Imprimir "El año no es bisiesto"
        finsi
    finsi
Fin
```

### Ejercicio 9



*Crea un algoritmo que determine si una cadena de texto es un palíndromo o no.*



**Paso 1**: Definir el problema

Para comprobar si una palabra es un palindromo,  se inserta la palabra en una cadena, esta cadena se recorre a la inversa y se almacena en una segunda cadena. Si la segunda cadena es igual a la primera, es un palindromo.


**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

Dos cadenas, una llamada `palabra` y otra `inversa`. Dos enteros siendo `j` y `long`

**Proceso:**

- Se le pide al usuario que ingrese una palabra.

- Se calcula la longitud de la palabra.

- Se recorre la palabra de atrás hacia adelante, concatenando cada letra en una nueva cadena llamada `inversa`.

- Se recorre y compara la cadena `palabra` con la cadena `inversa`.

- Si las dos cadenas son iguales, entonces la palabra es palíndromo. De lo contrario, no lo es.

**Salida:**

Imprimir si es palindromo o no.

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo Palindromo
	#Entrada
    palabra[]<- Vacio
    inversa[]<- Vacio
    j<- 0
    long<- 0
    palindromo <- true
	
    Escribir "Ingrese una palabra: "
    palabra -> Leer palabra
	
    long <- Longitud(palabra)
	
	#Proceso
    Para i <- long, mientras i mayor o igual a  0 con paso -1 hacer
        inversa[j] <- palabra[i] 
        j++
    Fin Para
    
	Para i <- 0, mientras i menor o igual quelong con paso 1 hacer
        Si palabra[i] != inversa[i] entonces
        	palindromo false
   		finsi
    Fin Para
    
    #Salida
    si palindromo == true entonces
    	Imprimir " La palabra es un palindromo"
    sino
    	Imprimir " La palabra no es un palindromo"
       
    Fin Si
Fin 
```



### Ejercicio 10



*Dada una lista de nombres, crea un algoritmo que ordene la lista alfabéticamente.*



**Paso 1**: Definir el problema

Para ordenar alfabeticamente la lista de nombres, tendremos que recorrer la lista entera, comprobar palabra por palabra  y ordenaralas en otra lista auxiliar.

**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

El algoritmo recibira por entrada la `lista` de palabras a ordenar

**Proceso:**

- Se almacena en `n` la longitud de la `lista`

- Se almacena en `n` la longitud de `lista`

- Se hace una copia de `lista` en `listaOrdenada`

- Se hace un bucle que recorra la longitud de la lista menos dos posiciones

  - Se almacena en `menorPalabra` el elemento de la lista
  - Se hace otro  bucle que recorra la longitud de la lista menos una posicion
    - Si `menorPalabra`es mayor que el elemento de `listaOrdenada`
      -  Se sustituye  `menorPalabra` por el elemento de `listaOrdenada`
      - Se guarda la posicion

  - Se almacena la posicion de `listaordenada` en `temporal`
  - En  `listaordenada` se almacena `menorPalabra`
  - `temporal` se almacena en la `posicion` de `listaOrdenada`



**Salida:**

- Imprimimos `listaordenada`

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo ListaAlfabeitca
    # Entrada
    lista <- leer entrada
    
    # Proceso
    n <- longitud(lista)
    listaOrdenada <- lista
    Para i=0 Hasta n-2 con paso 1 Hacer
        menorPalabra <- listaOrdenada[i]
        Para j=i Hasta n-1 con paso 1 Hacer
            Si menorPalabra es mayor que listaOrdenada[j] Entonces
                menorPalabra <- listaOrdenada[j]
                posicion <- j
            FinSi
        FinPara
        temporal <- listaOrdenada[i]
        listaOrdenada[i] <- menorPalabra
        listaOrdenada[posicion] <- temporal
    FinPara
    
    # Salida
    Imprimir(listaOrdenada)
FinAlgoritmo
```

### Ejercicio 11



*Crea un algoritmo que calcule el factorial de un número entero.*



**Paso 1**: Definir el problema

El factorial de un numero es el producto de todos los numeros que preceden a un numero concreto.

Siendo por ejemplo el factorial de 3 -> 1x2x3=6.



**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

El programa recibe de entrada un numero para comprobar.

**Proceso:**

- Introducir el  numero 

- Validar que sean números
  - Si no es valido, se muestra un mensaje de error
  
- Se define la variable `resultado` 

- Para i=0, hasta que i sea igual que numero, multiplicamos en resultado el valor de i.

  

**Salida:**

Se impime `resultado`

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo Factorial

    #Entrada

    factorial <- leer entrada
    resultado <- 1
    si factorial != numero
        imprimir Error, factorial debe ser un numero
    sino

        #Proceso
        para i=1, mientras i<=factorial, i++
            resultado = resultado*i
        fin para
    finsi

    #Salida
    Imprimir resultado
Fin
```

### Ejercicio 12



*Dado un número entero, crea un algoritmo que determine si es primo o no.*



**Paso 1**: Definir el problema

Para determinar si un numero es primo o no, se divide entre todos los numero que le preceden hasta 1. Si alguno de los restos de esas divisiones es 0, el numero no será primo

**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

El programa recibe de entrada un numero para comprobar.

**Proceso:**

- Introducir el  `numero ` por teclado
- Validar que sean números
  - Si no es valido, se muestra un mensaje de error
- Se define la variable `resultado` 
- Hacemos un bucle desde el numero anterior hasta 2.
  - Dentro del bucle dividimos numero entre la variable del bucle, y el resto lo almacenamos en resultado
  - Si resultado es 0, no es primo

- Se impime "Primo" o " No primo" dependiendo del valor de las operaciones

**Salida:**

Se impime "Primo" o " No primo" dependiendo del valor de las operaciones

**Paso 3**: Escribir el pseudocódigo



``` 
Algoritmo Numero Primo
	#Entrada
    numero <- leer entrada # 4
    resultado <-0
    primo <- true
    
    #Proceso
    si numero diferente entero
        imprimir Error, el primo debe ser un entero
    sino
        para i=numero-1 hasta  2 con paso -1 hacer #i=2
            resultado <- numero mod i #0
            si resultado = 0
                primo <- false
                i <- 2 #break
            finsi
        fin para
    finsi
	
	#Salida
    si primo = false entonces
        Imprimir "El numero no es primo"
    sino entonces
        Imprimir "El numero es primo"
    finsi
	
Fin Algoritmo
```

### Ejercicio 13



*Crea un algoritmo que calcule el área y volumen de un cubo dado su lado*



**Paso 1**: Definir el problema
Realizar formulas que calculen el volumen y el area de un circulo segun el lado introducido por el usuario

Para calcular el volumen, escalaremos al cubo la longitud de un lado, es decir V=L^3. Para el area, es algo similar, multiplicamos 6 por lado por lado, es decir: A=LxLx6

**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

El programa recibirá de entrada el `lado` del cubo, introducido por el usuario,.

**Proceso:**

- Introducir numero del `lado`

- Validar que el `lado` sea valido, por ejemplo que no sea negativo

  - Si no es valido, se muestra un mensaje de error

- Se define la variable `area`y la variable `volumen`

- Se calcula el area con la formula dicha en el paso 1 y se almacena en `area`

- Se calcula el volumen con la formula dicha en en el paso 1 y se almacena en `volumen`

- Se imprime/retorna `area `  y `volumen`

  

**Salida:**

Se imprime/retorna `area `  y `volumen`

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo Cubo
	#Entrada
    volumen <- 0
    area <- 0
    lado <- leer entrada
	
	#Proceso
    si lado>0 o lado diferente a entero
        imprimir Error, el lado no puede ser menor que 0
    sino
        area <- lado*lado*6
        volumen <- lado*lado*lado
    finsi
	
	#Salida
    Imprimir area
    Imprimir volumen

Fin Algoritmo
```

### Ejercicio 14



*Dada una lista de números enteros, crea un algoritmo que calcule la suma de todos los números pares de la lista.*



**Paso 1**: Definir el problema
Igual que en el ejercicio 7, comprobar si un numero es par o impar. Para ello, si al dividirlo entre dos y el resto es 0, sera par, sino, sera impar. Si es par, lo añadiremos a la suma.

**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

El programa recibe de entrada una lista de numeros enteros.

**Proceso:**

- Introducir la lista de numeros enteros mediante un bucle hasta que el usuario introduzca 0
- Validar que sean números enteros
  - Si no es valido, se muestra un mensaje de error
- Se define la variable `resultado` 
- Iniciamos un bucle para hasta el final de la lista
  - Almacenamos en la variable `resto`el resto de la division de un numero de la lista entre 2
  - Si `resto`es 0, es decir, par, se sumara a `resultado`

- Imprimimos `resultado`

**Salida:**

Se impime  `resultado`

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo Suma ParImpar

    #Entrada
    para i=0, mientras sumaparimpar!=0, i++
        sumaparimpar[i] <- leer entrada
        si sumaparimpar[i] != numero
            imprimir Error, el sumaparimpar debe ser un numero
        finsi
    finpara
    resultado <- 0
    resto <- 0

    #Proceso
    para i=0, mientras sumaparimpar[i]!=0, i++
        resto <- sumaparimpar[i] mod 2

        si resto == 0 entonces
            resultado += sumaparimpar[i]
        finsi
    fin para

    #Salida
    Imprimir resultado

fin
```

### Ejercicio 15



*Crea un algoritmo que determine si un número es positivo, negativo o cero.*



**Paso 1**: Definir el problema
Comprobar si un numero introducido es positivo, negativo o cero. Para ello comprobamos si el numero es mayor que cero, menor que cero o igual a cero.

**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

El programa recibe por entrada un numero introducido por el usuario.

**Proceso:**

- Introducir el numero por teclado
- Validar que sea un número entero
  - Si no es valido, se muestra un mensaje de error
- Se define la variable `resultado` 
- Si `numero`>0 entonces
  - Imprimir "El numero es positivo"
- Sino Si `numero`<0 entonces
  - Imprimir "El numero es negativo"
- Sino Si `numero`==0 entonces
  - Imprimir "El numero es 0"

**Salida:**

Imprimimos si el numero es positivo, negativo o 0

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo PosiNegoCero

    #Entrada

    numero <- leer entrada

    si numero != numero
        imprimir Error, el numero debe ser un numero
    sino

    #Proceso y Salidas
        si numero>0 entonces
            Imprimir "El numero es positivo"
        sino si numero < 0 entonces
            Imprimir "El numero es negativo"
        sino si numero==0 entonces
            Imprimir "El numero es cero"
        finsi

    finsi
	
Fin
```

### Ejercicio 16



*Dada una lista de números enteros, crea un algoritmo que calcule la media de la lista.*



**Paso 1**: Definir el problema
Sumar todos los numeros de una lista, una vez sumados, dividirlos por el tamaño de la lista

**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

El programa recibe por entrada una lista de números introducida por el usuario.

**Proceso:**

- Se define la variable `resultado`  y `contador`

- Introducir la lista de numeros enteros mediante un bucle hasta que el usuario introduzca 0. En una variable `contador`, almacenamos el valor de i
  - Validar que sean números enteros
    - Si no es valido, se muestra un mensaje de error
- Iniciamos un bucle para hasta el final de la lista
  - Sumamos los numeros de la lista en `resultado`

- Dividimos el valor de `resultado` entre `contador`
- Imprimimos el `contador`

**Salida:**

Imprimimos si el numero es positivo, negativo o 0

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo Media

    #Entrada
    resultado<-0
    para i<-0, mientras numero sea diferente a 0 con paso 1
        numero <- leer entrada
        lista_numeros[i] <- numero
        si lista_numeros[i] != numero
            imprimir Error, la lista_numeros debe ser de enteros
        finsi
        contador=i
    finpara

    #Proceso

    para i<-0 mientras lista_numeros[i]!=0, i++
        resultado += lista_numeros[i]
    finpara

    resultado = resultado / (i-1)
	
	#Salida
    Imprimir resultado

Fin
```

### Ejercicio 17



Crea un algoritmo que genere un número aleatorio entre 1 y 100, y le pida al usuario adivinarlo. El algoritmo deberá indicar si el número introducido es mayor o menor que el número aleatorio, hasta que el usuario adivine el número correcto.



**Paso 1**: Definir el problema
El programa generara aleatoriamente un numero mediante una función. Si el numero es mayor, mostrara un mensaje diciendo que el numero deseado es menor, sino dira que el numero buscado es mayor. Si el numero introducido es el correcto, mostrara un mensaje informando de que se ha encontrado el numero

**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

El programa recibe por entrada un numero del usuario

**Proceso:**

- Se genera un numero `aleatorio`

- Se inicia un bucle, mientras `numero` no sea igual que `aleatorio`

  - El usuario introduce un `numero`
    - Se valida que sea un numero entero
      - Si no lo es, se manda un error

  - Si `numero` es menor que 0 o mayor que 100
    - Se imprime " El numero esta fuera de rango"

  - Si `numero`es mayor que el generado
    - Se imprime " El numero buscado es menor"

  - Si `numero`es menor que el generado
    - Se imprime " El numero buscado es mayor"

  - Si `numero`es menor que el generado

    - Se imprime " Lo has encontrado"

      

**Salida:**

- Imprimir Lo has encontrado!

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo Numero Aleatorio
	#Entrada
    aleatorio <- NumAleatorio(0,100)
    numero <- 101
	#Proceso
    mientras numero diferente aleatorio hacer
    	numero <- leer entrada
    	si numero diferente a entero || numero >100 || numero <0
    		Imprimir "Fuera de rango" 
    	sino si numero < aleatorio entonces
    		Imprimir"El numero es mayor"
    	sino si numero > aleatorio entonces
    		Imprimir"El numero es menor"
    	sino si numero == aleatorio entonces
    		#Salida
    		Imprimir"Lo has encontrado!"
    	finsi	
    		
    fin mientras

Fin
```

### Ejercicio 18



Crea un algoritmo que determine si una cadena de texto es un anagrama de otra cadena de texto.

**Paso 1**: Definir el problema

Un anagrama de una palabra es una serie de letras colocadas de cierta manera, que reordenadas pueden formar otra palabra.

Para ello, el usuario insertara dos cadenas, las cuales se comprobaran que tienen las mismas letras. Si tienen exactamente las mismas letras, es un anagrama.

**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

El usuario introduce dos cadenas de texto `cadena1` y `cadena2`

**Proceso:**

- Se almacena `cadena2` dentro de una cadena temporal llamada `temp`
- Se inicializa un `contador` a 0
- Se inicia un bucle que recorre la `cadena1`
  - Se inicia un bucle que recorre la `cadena2`
    - Si el elemento en `cadena1` es igual a un elemento en `temp`
      - Borramos el elemento en temp

**Salida:**

- Si `temp`esta vacio, se imprime que las dos cadenas son anagramas
- Sino, se imprime que las dos cadenas NO son anagramas

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo Anagrama
	#Entrada
    Leer cadena1
    Leer cadena2
    temp <- cadena2
    
	#Proceso
    Para i = 0 Hasta longitud(cadena1) Con Paso 1
      Para j = 0 Hasta longitud(temp) Con Paso 1
        Si cadena1[i] = temp[j] Entonces
          Borrar(temp[j])
        Fin Si
      Fin Para
    Fin Para
	
	#Salida
    Si temp[] = Vacio  Entonces
      Mostrar cadena1 + " y "+ cadena2 + " son anagramas"
    Sino
      Mostrar cadena1 + " y "+ cadena2 + " no son anagramas"
    Fin Si

Fin
```

### Ejercicio 19



Dada una lista de números enteros, crea un algoritmo que elimine los números duplicados de la lista

**Paso 1**: Definir el problema

El usuario introducira una cadena de numeros. Para comprobar si el numero esta repetido, se recorrera la cadena, cada vez q entre en la posición 

de un numero, lo compara con los numeros almacenados en una subcadena. Si el numero no esta, lo almacenara en la subcadena, y pasará a la siguiente posición de la cadena principal. Si se encuentra en la subcadena, se eliminara de la cadena principal.

**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

El programa recibe por entrada una lista de números introducida por el usuario.

**Proceso:**

- Introducir la lista de numeros enteros mediante un bucle hasta que el usuario introduzca -1. 
  - Validar que sean números enteros
    - Si no es valido, se muestra un mensaje de error
- Iniciamos un bucle para hasta el final de la lista
  - Iniciamos un segundo bucle para hasta el final de la sublista
    - Si numero es igual a numero sublista
      - Elimina numero en lista
    - Sino
      - Guarda el numero en la sublista, y pasamos al siguiente



**Salida:**

- Imprimimos la lista sin repetidos

**Paso 3**: Escribir el pseudocódigo



```
Algoritmo Duplicados

    #Entrada
    para i=0, mientras numero diferente -1 con paso  1 hacer
        numero <- leer entrada
        lista_numeros[i] <- numero
        si lista_numeros[i] != numero
            imprimir Error, la lista_numeros debe ser de enteros
        finsi
        contador=i
    finpara
    #Proceso
    para i <- 0, mientras i diferente longitud(lista) con paso 1 hacer
        para j <- 0, mientras j diferente longitud(sublista), j++
            si lista[i] igual sublista[j] entonces
                eliminar(lista[i])
            sino
                sublista[].añadir(lista[i])
                j <- longitud(lista)
            finsi
    finpara

    #Salida
    Imprimir lista[]

Fin Algoritmo
```

### Ejercicio 20



Crea un algoritmo que determine si un número es capicúa o no.

**Paso 1**: Definir el problema

Para comprobar si un numero es capicuo,  se inserta el numero en una cadena, esta cadena se recorre a la inversa y se almacena en una segunda cadena. Si la segunda cadena es igual a la primera, es capicuo.


**Paso 2**: Poner la entrada, el proceso y la salida

**Entrada:**

Dos cadenas, una llamada `cadena` y otra `inversa`. Dos enteros siendo `j` y `long`

**Proceso:**

- Se le pide al usuario que ingrese una cadena.

- Se calcula la longitud de la cadena.

- Se recorre la cadenade atrás hacia adelante, concatenando cada numero en una nueva cadena llamada `inversa`.

- Se recorre y compara la cadena `cadena` con la cadena `inversa`.

- Si las dos cadenas son iguales, entonces el numero es capicuo. De lo contrario, no lo es.

**Salida:**

Imprimir si es capicuo o no.

**Paso 3**: Escribir el pseudocódigo



```
Inicio
	#Entrada
	
    cadena[]<- Vacio
    inversa[]<- Vacio
    j<- 0
    long<- 0
    capicuo <- true

    Escribir "Ingrese una cadena de numeros: "
    cadena -> Leer cadena
	
	#Proceso
    long <- Longitud(cadena)

    Para i <- long mientras i>=0 con paso -1 hacer
        inversa[j] <- cadena[i] 
        j++
    Fin Para
    
	Para i <- 0 mientras i<=long con paso 1 hacer
        Si cadena[i] != inversa[i] entonces
        	capicuo false
   		finsi
    Fin Para
    
    #Salida
    si capicuo == true entonces
    	Imprimir " El numero es capicuo"
    sino
    	Imprimir "El numero no es capicuo"
       
    Fin Si
Fin 
```

