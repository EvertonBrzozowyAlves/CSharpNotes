# STRINGS

## Placeholders, interpolação e concatenação
Podemos formatar textos usando strings de várias formas.  

### Placeholders
```csharp
var name = "Everton";
var age = 29;
var balance = 10.5468;

Console.WriteLine("My name is {0} and I'm {1}. My balance is {2:F2}.", name, age, balance);
```
>O "F2" é uma das opções de formatação de saída de dados. Veja mais nesse link:
>https://docs.microsoft.com/pt-br/dotnet/api/system.double.tostring?view=net-5.0 

### Interpolação
```csharp
var name = "Everton";
var age = 29;
var balance = 10.5468;

Console.WriteLine($"My name is {name} and I'm {age}. My balance is {balance:F2}.");
```

### Concatenação
```csharp
var name = "Everton";
var age = 29;
var balance = 10.5468;

Console.WriteLine($"My name is " + name + " and I'm " + age + ". My balance is " + balance.ToString("F2") + ".");
```