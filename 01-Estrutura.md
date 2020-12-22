# CARACTERÍSITCAS


## C# e .NET
C# não é .NET.  
C# é uma linguagem de programação.  
.NET é uma plataforma de desenvolvimento para se programar, a qual suportava várias linguagens de programação, inclusive C#.  

O .NET é composto basicamente por dois componentes:
- BCL - *Base Class Library*
É uma bibilioteca base com métodos prontos que podemos utilizar para criar as nossas aplicações.

- CLR - *Common Language Runtime (Máquina Virtual)*
O CLR executa os programas criados em .NET.  
O CLR possui um *Garbage Collector*: Objetos não utilizados são automaticamente desalocados da memória.  


## .NET Standard
O .NET standard é uma especificação, que diz o que a implementação deve oferecer para se enquadrar no padrão .NET.  
O .NET Standard foi lançado em 2002, juntamente com uma implementação do padrão, que é o .NET Framework.  
Este framework é muito bom, porém roda  apenas em sistemas Windows.  
Essa não é a única implementação do .NET Standard, temos também as implementações:

- Mono, 2004  
    - Implementação do padrão .NET multiplataforma, de código aberto e independente. O Unity e o Xamarin utilizam essa implementação.  
- Xamarin, 2011  
    - Implementação do padrão .NET baseada no Mono, para desenvolvimento de aplicativos móveis para Android e IOS e também para MacOs.  
- .NET Core, 2016  
    - Implementação do padrão .NET, criada pela Microsoft junto com a comunidade, de código aberto. 


## Compilada ou interpretada?

### Sobre linguagens compiladas
Uma linguagem puramente compilada, como o C ou C++, é escrita e depois esse código fonte passa por um compilador específico para uma plataforma.  
O compilador irá gerar um código executável que a plataforma consiga executar.  Nesse cenário, é necessário um compilador para cada plataforma.  
Pode ser necessário também algumas adaptações no código, dependendo do tipo de plataforma/aplicação que está sendo desenvolvida.  

A desvantagem desse cenário é que eventualmente precisaremos alterar o código para publicação em plataformas diferentes, o que gera mais trabalho.
A vantagem é que o código é executado de forma extremamente rápida.

### Sobre linguagens interpretadas
As linguagens interpretadas, como PHP e JavaScript, não precisam passar pelo processo de compilação descito acima.  
Basta ter o interpretador da linguagem instalado na máquina, que o programa é interpretado enquanto é executado.

A desvantagem dessa abordagem é que o código não é executado com a mesma rapidez do que um código compilado.  
A vantagem é a manutenção. Somente alteramos o código fonte uma vez.  

### Abordagem híbrida
A linguagem C# na verdade é uma mistura, chamada de híbrida.  
Nesse cenário, o código fonte é escrito somente uma vez. Depois, esse código é pré-compilado para ByteCode (*CIL - Common Intermediate Language*), 
agnóstico de plataforma.  
Esse código pré-compilado pode ser executado em qualquer plataforma que tenha um interpretador.  
No ambiente .NET, basta ter um .NET CLR instalado na plataforma.  
Enquanto é executado, temos uma compilação *JIT - Just In Time*, muito mais rápida que a convecional, visto que o código fonte já foi pré compilado e está 
sintaticamente correto.  

Nesse cenário, temos o melhor da abordagem compilada e também da interpretada.  

## Modelo de execução

1. Escrita do código fonte
2. Compilação para CIL (ByteCode)
3. Execução pelo .NET CLR / Compilação JIT
4. Código de máquina