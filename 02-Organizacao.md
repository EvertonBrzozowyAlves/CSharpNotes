# ORGANIZAÇÃO DAS ESTRUTURAS  
Do maior para o menor:  

1. Solution (Aplicação)  
2. Assemblies (Projetos)  
3. Namespaces  
4. Classes  

```csharp
using System;

namespace Namespace
{
    class Classe
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World");
        }
    }
}
```

## Classes  
Como uma linguagem orientada a objetos, o C# trabalha com classes.   
As classes possuirão as propriedades e métodos para trabalharmos.  


## Namespaces  
Um namespace é um agrupamento **lógico** de classes relacionadas.  
Por exemplo, podemos ter um namespace onde iremos guardar todas as classes que representam as entidades de negócio da aplicação.  
Um namespace pode conter uma ou várias classes.  


## Projeto / Assembly  
Um assembly é um build, que se tornará uma .dll ou um .exe.  É um agrupamento **físico** de classes relacionadas.  
Um assembly pode conter um ou vários namespaces.  


## Aplicação / Solution  
Agrupamento de asseblies relacionados.  
Uma solução pode conter um ou vários assemblies.  

