# CONVERSÕES

## Conversão implícita
Conversão implícita ocorre quando, um tipo de variável pode ser associado a outro tipo, sem necessidade de conversão.  
Por exemplo, uma varíavel do tipo float (4 bytes) pode ser representado por uma double (8 bytes).  

```csharp
float a = 4.5f;
double b = a;
```

Para o processo inverso, de adicionar um valor double (8 bytes) para float (4 bytes), seria necessário um casting, pois podemos perder dados no processo de conversão.  

## Casting
O processo de casting server para explicitar que desejamos fazer a conversão entre tipos, mesmo que haja perda de alguns dados:  

```csharp
double a = 4.5;
int b = (int)a; // b == 4
```

Do mesmo modo, ao fazer uma divisão entre dois números inteiros, o compilador presume que o resultado deve ser um inteiro.  
Para prevenir esse tipo de resultado, podemos adicionar um casting em um dos números:  

```csharp
int a = 5;
int b = 2;
Console.WriteLine(a / b); // 2
Console.WriteLine((double) a / b); // 2.5
```