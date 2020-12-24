# OPERADORES

## Aritméticos

|Operador    | Significado      |
|:----:      |:----:            |
| +          | Adição           |
| -          | Subtração        |
| *          | Multiplicação    |
| /          | Divisão          |
| %          | Resto da divisão |

Assim como na matemática, os operadores *, / e % tem precedência a + e -, sendo executados primeiro em uma expressão.  
Quando temos dois operadores com precedência, a ordem e executar o cálculo da esquerda para direita.  
Para alterar a precedência, podemos utilizar parêntesis ():  

```csharp
Console.WriteLine((50 + 2) * 3);
```

Podemos usar o % para verificar se o resto da divisão, o que ajuda a descobrir se o número é par ou múltiplo de outro.  

>Em uma expressão somente com números inteiros, o resultado tende a ser um inteiro, mesmo que o resultado seja um número fracionado:
>```csharp
>Console.WriteLine(10 / 8); //1
>```
>Para prevenir esse comportamento, devemos fazer o casting de um dos números para double ou float:  
>```csharp
>Console.WriteLine((double)10 / 8); //1.25
>```
>OU
>```csharp
>Console.WriteLine(10 / 8.0); //1.25
>```

Exemplo de cálculo utilizando a classe Math, que possui alguns métodos para auxiliar com cálculos matemáticos:
```csharp
double a = 1.0, b = -3.0, c = -4.0;
double delta = Math.Pow(b, 2.0) - 4.0 * a * c;

double x1 = (-b + Math.Sqrt(delta)) / (2.0 * a);
double x2 = (-b - Math.Sqrt(delta)) / (2.0 * a);
```

## Atribuição

|Operador    | Exemplo       | Significado   |
|:----:      |:----:         |:----:         |
| =          | a = 10;       | a recebe 10   |
| +=         | a += 2;       | a recebe a + 2|
| -=         | a -= 2;       | a recebe a - 2|
| *=         | a *= 2;       | a recebe a * 2|
| /=         | a /= 2;       | a recebe a / 2|
| %=         | a %= 3;       | a recebe a % 3|

Os operadores de atribuição comulativa funcionam da seguinte forma:  
É feita a operação do primeiro operador sobre o valor que já está associado a variável, e depois a variável recebe o valor do resultado da operação.  

```csharp
int a = 12;
a *= 3; //a == 36
```

O operador **+=** também funciona com strings, para concatenação.
```csharp
int s = 'My';
s += ' text'; // 'My text'
```

## Aritméticos / Atribuição

|Operador    | Exemplo       | Significado   |
|:----:      |:----:         |:----:         |
| ++         | a++ ou ++a    | a recebe a + 1|
| --         | a-- ou --a    | a recebe a - 1|

A diferença entre a++ e ++a é que, quando usamos a++ e a vamos atribuir o valor a uma outra variável b, 
primeiro é atribuído o valor de a para b e depois a é incrementada.  
Quando usamos ++a, antes de b receber o valor de a, a é incrementada.  

```csharp
int a = 10;
b = a++; //b == 10
b = ++a; //b == 11
```