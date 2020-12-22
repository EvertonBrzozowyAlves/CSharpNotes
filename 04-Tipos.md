# TIPOS

## Tipos de Valor

|C# Type     | .Net Type           | Signed    | Bytes     | Possible values      |
|:----:      |:----:               |:----:     |:----:     |:----:                |
| sbyte      | System.SByte        | Yes       | 1         | -128 to 127          |
| short      | System.Int16        | Yes       | 2         | -32678 to 32677      |
| int        | System.Int32        | Yes       | 4         | -2(31) to 2(31)-1    |
| long       | System.Int64        | Yes       | 8         | -2(63) to 2(63)-1    |
| byte       | System.Byte         | No        | 1         | 0 to 255             |
| ushort     | System.Uint16       | No        | 2         | 0 to 65535           |
| uint       | System.Uint32       | No        | 4         | 0 to 2(32)-1         |
| ulong      | System.Uint64       | No        | 8         | 0 to 2(64)-1         |
| float      | System.Single       | Yes       | 4         | ~1.5 x 10(-45) to ~3.4 x 10(38) with 7 significant figures|
| double     | System.Double       | Yes       | 8         | ~5.0 x 10(-324) to ~1.7 x 10(308) with 15 or 16 significant figures|
| decimal    | System.Decimal      | Yes       | 12        | ~1.0 x 10(-28) to ~7.9 x 10(28) with 28 or 29 significant figures|
| char       | System.Char         | N/A       | 2         | Any unicode character|
| bool       | System.Boolean      | N/A       | 1/2       | true of false        |

>A diferença entre utilizar o C# type e o .Net Framework type, é que o C# type é independente de namespaces.
>Os tipos do .Net Framework são dependentes do namespace System, conforme indicado na tabela.

Cada tipo tem um limite de valor. Quando esse valor é excedido, é atribuído o valor da extremidade oposta na variável.    
Por exemplo, no tipo sbyte, o limite é 127. Não podemos atribuir diretamente 128 na variável.   
Mas, se incrementarmos a variável com mais um, será atribuído o valor -128 nela.  

Quando trabalhamos com o tipo **char**, podemos atribuir um caractere de duas maneiras:
1. Um caractere entre as pas simples:
```c#
char letraA = 'A';
```
2. Código unicode do caractere:
```c#
char letraA = '\u0041';
```

Quando estiver trabalhando com números do tipo long, é uma boa prática deixar um sufixo **L** ao final do número:
```c#
long number = 2147483648L;
```

Para float, devemos colocar o sufixo **f** depois do número:
```c#
float number = 215.5f;
```

Os tipos de valor normalmente tem uma propriedade para mostrar o valor mínimo e máximo que suportam:
```c#
int number = int.MinValue;
```

## Tipos de Referência

|C# Type     | .Net Type           | Description                        |
|:----:      |:----:               |:----:                              |
| string     | System.String       | Imutable unicode character string  |
| object     | System.Object       | A generic object. All classes derive from object: GetType()  Equals()  GetHashCode()  ToString()  |
