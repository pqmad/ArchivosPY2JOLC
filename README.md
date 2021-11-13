# ArchivosPY2JOLC
# Funciones no implementadas
**Structs**

**Parse**

**String**

# Archivos funcionales

## Strings

* para lowercase solo recibe mayusculas, se modificó el str1.

* para uppercase solo recibe minusculas, se modificó el str1.

* funcion STRING eliminada
```
function StringFunction()

    str1 = "sale compiladores 2"::String;

    println("FUNCIONES STRING:");
    println("Concatenacion:");
    println(str1 * " C3D - segundo Proyecto");
    println("UpperCase:");
    println(uppercase(str1));
    str1 = "SALE COMPILADORES 2";
    println("LowerCase:");
    println(lowercase(str1 * " SI SALE"));
    str1 = "sale compiladores 2"::String;
    println("Concatenacion + :");
    println("string * string");
    println(str1 * " C3D - segundo Proyecto");
    println("string * numero entero");
    println("entero = " * "125");
    println("string * numero decimal");
    println("decimal = " *"45.3246");
    println("decimal = " , 176/3);
end;

function testambito()
    numberstring= "100" * "Usac"::String;
    stringnumber= "Usac" * "2500"::String;
    stringstring= "Universidad" * " San Carlos"::String;
    println(numberstring);
    println(stringnumber);
    println(stringstring);
end;

function todas(parametro::String)
    a=lowercase(parametro);
    println(uppercase(a));
end;

StringFunction();
testambito();
todas("HOY GANO COMPI2");
```

## Intermedio

* se le agrego ";" a print que les faltaba.
```
x = 1::Int64;
y = 1::Int64;
println("---------------------------------");
println("Tablas de multiplicar con While");
println("---------------------------------");
while (x <= 10)
    while (y <= 10)
        print(x);
        print("x");
        print(y);
        print("=");
        println(x * y);
        global y = y + 1;
    end;
    println("-----------------------------");
    global x = x + 1;
    global y = 1;
end;

println("---------------------------------");
println("  Tablas de multiplicar con For");
println("---------------------------------");

for i in 1:10
    for j in 1:10
        print(i);
        print("x");
        print(j);
        print("=");
        println(i * j);
    end;
    println("--------------------------");
end;

iteraciones = 10::Int64;
temporal = 0::Int64;

while (temporal <= iteraciones)
    numero = temporal::Int64;
    if numero <= 0
        print("Factorial de ");
        print(temporal);
        println(" = 0");
        global temporal = temporal + 1;
        continue;
    end;
    factorial = 1::Int64;
    while (numero > 1)
        factorial = factorial * numero;
        numero = numero - 1;
    end;
    print("Factorial de ");
    print(temporal);
    print(" = ");
    println(factorial);
    temporal = temporal + 1;
end;


dias = ["Domingo", "Lunes", "Martes", "Miercoles", "Jueves", "Viernes", "Sabado"]::Vector{String};

for i in dias
        if i == "Lunes"
            println(1);
        end;
        if i == "Martes"
            println(2);
        end;
        if i == "Miercoles"
            println(3);
        end;
        if i == "Jueves"
            println(4);
        end;
        if i == "Viernes"
            println(5);
            println("Weekday");
            break;
        end;
            println("Weekend");       
end;

for i in 0:9

    output = "";
    for j in 0:(10 - i)
        output = output * " ";
    end;

    for k in 0:i 
        output = output * "* ";
    end;
    println(output);

end;
```

## comprobacionDinamica

* se le agrego ";" a end y declaracion de variable que les faltaba.
```

function imprimirArreglo(arreglo::Vector{Int64})
    for item in arreglo
        println(item);
    end;
end;

function imprimirArregloMal(arreglo::Vector{Int64})
    counter = 1;
    for i in 1:(length(arreglo) + 1)
        println(arreglo[i]);
    end;
end;

# Indice de arreglo fuera de limites
arreglo = [10, 11, 12, 32, 10, 45]::Vector{Int64};
imprimirArreglo(arreglo);
println("-------------------");
imprimirArregloMal(arreglo);

println("-------------------");
# Division por 0
var1 = 10 + 75 * (20 / (10 - 10));
println(var1);
var1 = 10 / 0;
println(var1);
```

## basico

* Archivo original.
```
# Declaración de Variables
var1 = 0::Int64;
var2 = 0::Int64;
var3 = 0::Int64;

string1 = ""::String;
string2 = ""::String;

bool1 = false::Bool;
bool2 = false::Bool;
bool3 = false::Bool;

# Println y Print
println("Verificando valores variables");
print(var1, " ", var2, " ", var3);
println("");
print(string1, " ", string2);
println("");
print(bool1, " ", bool2, " ", bool3);
println("");

# Asignación de Variables y Operaciones Arítmeticas, no potencia
var1 = 41 + 150 - 22 * 12 / 3 + ((125 % 5) * (5 + 2 - (5 * 2)));
var2 = (var1 + var1) - var1 * 2 + 11 % (12 + -10) + 125 / 25;

# Asignación de Variables y Potencia
var3 = (var1 ^ 0) + 125 - (var2) + (125 - 5^3);
println(var1, " ", var2, " ", var3);

# Asignación de Variables y Operaciones Relacionaless
bool1 = ((var1 + 125 / 5 * 3 - 1) > ((var2 ^ 2) + (var3 - 125) * (125 - 5^3)));
bool2 = ((var1 + 125 / 5 * 3 - 1) < ((var3 + 100 / 5) * (var2 - 10)));
println(bool1, " ", bool2);

# Asignación de Variables y Operaciones Lógicas (Corto Circuito)
bool3 = (var1 >= 120 || var2 <= 10) && (var3 > 125 || var3 < 10) || (var1 == 120 && 120 != var2);
println(bool3);
bool3 = 100 == 100 && 100 != 100 || 100 == 100 && 100 == 100;
println(bool3);

string1 = "Hola";
string2 = "Mundo";

println(string1, " ", string2);
```

## recursivas

* se le agrego ";" a return y end que les faltaba.
* Se le agrego el tipo a los parametros de la función.
* Cambio de orden de las funciones SerieFibonacciRecursiva y sumarSerieFibonacciRecursiva.
```
function SerieFibonacciRecursiva(n::Int64)::Int64
    if (n == 0)
        return 0;
    elseif (n == 1)
        return 1;
    else
        return SerieFibonacciRecursiva(n - 1) + SerieFibonacciRecursiva(n - 2);
    end;
end;

# Serie de Fibonacci
function sumarSerieFibonacciRecursiva(n::Int64)::Int64
    if n > 0
        return sumarSerieFibonacciRecursiva(n - 1) + SerieFibonacciRecursiva(n);
    end;
    return 0;
end;


println("Sumar serie de Fibonacci recursiva 10: ", sumarSerieFibonacciRecursiva(10));
println("Sumar serie de Fibonacci recursiva 16: ", sumarSerieFibonacciRecursiva(16));
println("Sumar serie de Fibonacci recursiva 7: ", sumarSerieFibonacciRecursiva(7));


# Multiplicar impares
function multiplicarImpares(n::Int64)::Int64
    if (n == 0)
        return 0;
    elseif (n == 1)
        return 1;
    else
        if (n % 2 == 0)
            return multiplicarImpares(n - 1);
        else
            return multiplicarImpares(n - 2) * n;
        end;
    end;
end;

println("Multiplicar impares hasta 12: ", multiplicarImpares(12));
println("Multiplicar impares hasta 5: ", multiplicarImpares(5));
println("Multiplicar impares hasta 21: ", multiplicarImpares(21));

```

## Arreglos
### unadim

* en el print del array se agrego un for para que imprima todos los valores.
* Se le agrego el tipo a los parametros de la función.
* Cambio de nombre a los parámetros.
```
function swap(i::Int64, j::Int64, arreglo::Vector{Int64})
    temp = arreglo[i]::Int64;
    arreglo[i] = arreglo[j];
    arreglo[j] = temp;
end;

function bubbleSort(arreglo::Vector{Int64})
    for i in 0:(length(arreglo) - 1)
        for j in 1:(length(arreglo) - 1)
            if(arreglo[j] > arreglo[j + 1])
                swap(j, j+1, arreglo);
            end;
        end;
    end;
end;

function selectionSort(arreglo::Vector{Int64}) 
    for j in 1:length(arreglo)
        iMin = j::Int64;
        for i in (j+1):length(arreglo)
            if(arreglo[i] < arreglo[iMin])
                iMin = i;
            end;
        end;
        swap(j, iMin, arreglo);
    end;
end;

arreglo = [32,7*3,7,89,56,909,109,2,9,98,44,3,820*10,11,8*0+8,10]::Vector{Int64};
for i in 1:length(arreglo)
    print(arreglo[i],"   ");
end;
println("");
bubbleSort(arreglo);
print("BubbleSort => ");
for i in 1:length(arreglo)
    print(arreglo[i],"   ");
end;
println("");


arreglo = [32,7*3,7,89,56,909,109,2,9,987,44,3,820*10,11,8*0+8,10];
arreglo[1] = 1;
for i in 1:length(arreglo)
    print(arreglo[i],"   ");
end;
println("");
selectionSort(arreglo);
print("selectionSort => ");
for i in 1:length(arreglo)
    print(arreglo[i],"   ");
end;
```

### dosdim

* En compararMatrices retorna 1 para true y 0 para false.
* Forma de imprimir las matrices.
```
random = [1, 5, 8, -1, 21, 42, -55, 123, -5, 5, 11]::Vector{Int64};

a = [
    [
        random[1] * 3,
        51,
        random[4] / 2,
        (random[3] * 10) % 7
    ], 
    [
        1,
        2,
        3,
        4
    ]
]::Vector{Vector{Float64}};

b = [
    [
        1,
        2,
        3,
        4   
    ], 
    [
        random[1] * 3,
        51,
        random[4] / 2,
        (random[3] * 10) % 7
    ]
]::Vector{Vector{Float64}};

auxiliar = [
    [
        0.0,
        0.0,
        0.0,
        0.0
    ], 
    [
        0.0,
        0.0,
        0.0,
        0.0
    ]
]::Vector{Vector{Float64}};


# Si no tienen implementado este for, pueden cambiarlo por algún otro ciclo que funcione parecido.
function printMatriz(matrix::Vector{Vector{Float64}})
    println("[");
    for i in 1:length(matrix)
        print("[");
        for j in 1:length(matrix[1])
            print(matrix[i][j], " ");
        end;
        println("]");
    end;
    println("]");
end;

function sumarMatrices(matrix1::Vector{Vector{Float64}}, matrix2::Vector{Vector{Float64}})
    if length(matrix1) != length(matrix2)
        return "NO SE PUEDEN SUMAR. NO SON DE LA MISMA LONGITUD";
    end;

    
    for i in 1:length(matrix1)
        for j in 1:length(matrix1[1])
            auxiliar[i][j] = matrix1[i][j] + matrix2[i][j];
        end;
    end;
end;

function compararMatrices(matrix1::Vector{Vector{Float64}}, matrix2::Vector{Vector{Float64}})::Int64
    igual=1;
    diferente=0;
    if length(matrix1) != length(matrix2)
        return diferente;
    end;

    
    for i in 1:length(matrix1)
        for j in 1:length(matrix1[1])
            if matrix1[i][j] != matrix2[i][j]
                return diferente;
            end;
        end;
    end;
    return igual;
end;

println("MATRIZ a");
printMatriz(a);
println();
println("MATRIZ b");
printMatriz(b);

println();
println("LAS DOS MATRICES SUMADAS");
sumarMatrices(a, b);
print("[");
for i in 1:length(auxiliar)
    print("[   ");
    for j in 1:length(auxiliar[1])
        print(auxiliar[i][j],"   ");
    end;
    print("]");
end;
print("]");
println();

println();
println("COMPARAR MATRICES. SON IGUALES?");
if compararMatrices(a, b)==1
println(true);
else
println(false);
end;

b = a;
println();
println("COMPARAR MATRICES. SON IGUALES?");
if compararMatrices(a, b)==1
println(true);
else
println(false);
end;
```


### tresdim

* En insertarValores la forma de insertar los valores se cambio a insertarlos uno por uno.
* Quitar la función STRING en imprimirReporte.

```
paises = ["EE.UU", "Rusia", "Guatemala", "Alemania"]::Vector{String};
celulares = ["Galaxy A12", "iPhone 13", "Huawei P40"]::Vector{String};
edades = ["12-14", "15-17","18-24","25-30"]::Vector{String};

vendidos = [
    [
        [
            1800,1600,2000,1500
        ],
        [0,0,0,0],
        [0,0,0,0]
    ],
    [
        [
            2500,1000,800,4500
        ],
        [0,0,0,0],
        [0,0,0,0]
    ],
    [
        [
            12500,11000,1800,14500
        ],
        [0,0,0,0],
        [0,0,0,0]
    ],
    [
        [
            5600,9800,7800,19000
        ],
        [0,0,0,0],
        [0,0,0,0]
    ]
]::Vector{Vector{Vector{Int64}}};

function insertarValores(array::Vector{Vector{Vector{Int64}}})
    for i in 1:4
        for j in 2:3
            array[i][j][1] = i+j+3400;
            array[i][j][2] = i+j+5600;
            array[i][j][3] = i+j+7600;
            array[i][j][4] = i+j+2000;
        end;
    end;
end;

function imprimirReporte(value::Int64,i::Int64,j::Int64,k::Int64)
    println(paises[i] * "          " * celulares[j] * "          " * edades[k] * "          " , value);    
end;

function imprimirScore(array::Vector{Vector{Vector{Int64}}})
    for i in 1:length(array)
        for j in 1:length(array[i])
            for k in 1:length(array[i][j])
                imprimirReporte(array[i][j][k],i,j,k);
            end;
        end;
    end;
end;

insertarValores(vendidos);
println("Pais" * "          " * "Celular" * "          " * "Edad" * "          " * "Vendidos");    
imprimirScore(vendidos);

```


## Optimizacion
### mirilla

* Archivo original.

```
#################################################
#   Las demás reglas se le preguntará al estudiante
#   sobre como las implemento, se revisará código y
#   se probarán archivos que estos hayan probado
#   para hacer esta sección
#################################################

# Regla 4
if true && true
    println(true);
else
    println(false);
end;

# Regla 5 o 3
if 5 > 2
    println(true);
else
    println(false);
end;

# Regla 7
var1 = 4 + 0;
var1 = (var1 - 0) * 20;
var1 = (var1 - 10 * 5) * 1;
var1 = var1 / 1;

# Regla 8
var1 = 4 * 2;
var1 = var1 * 2;
var1 = var1 * 0;
var1 = 0 / var1;


```



