# Kotlin: Sintaxe Basica

## Olá mundo

```Kotlin
fun main() {
    println("Hello, world!!!")
}
```

## Tipos de dados
| Tipo | Conversão |
| - | - |
| Int | toInt() |
| Long | toLong() |
| Byte | toByte() |
| Short | toShort() |
| Float | toFloat() |
| Double | toDouble() |
| Char | toChar() |
|Null!||
|Array||
|Boolean||

## Declaração de Variavel
### Var
* Valor Mutavel
* CamelCase
```Kotlin
var idade = 22
var idade:Int?
idade = null ou 22
```

### Var
* Valor Imutavel
* CamelCase
* Similar ao "FINAL" em java
```Kotlin
val idade = 22
val idade:Int?
idade = null ou 22
```

### Const Val
* Valor Imutavel
* SnakeCase
* Atribuido durante a compilação
```Kotlin
val MIN_IDADE = 16
val MAX_IDADE = 68
```

## Erros Comuns
Variavel sem tipo e sem atribuição:
```Kotlin
var idade
idade = 22
```

Variavel com tipo atribuido diferente:
```Kotlin
var idade = "Idade"
idade = 22
```

## Nulability
Qualquer variavel pode ser nulo, pórem isso deve ser explicitado na decaração da variavel atraves do uso da interrogação (?).  
Exemplo:
```Kotlin
var idade:Int?
```

## Operadores Aritiméticos
|Função|Expressão|Comando|Atribuição|
|-|-|-|-|
|soma|a + b|a.plus(b)|a += b|
|subtração|a - b|a.minus(b)|a -= b|
|multiplicação|a * b |a.times(b)|a *= b|
|divisão|a / b|a.div(b)|a /= b|
|resto|a % b|a.mod(b)|a %= b|

## Operadores Comparativos
|Função|Expressão|Comando|
|-|-|-|
|Maior|a > b|a.compareTo(b)>0|
|Maior igual|a >= b|a.compareTo(b)>=0|
|Menor|a < b|a.compareTo(b)<0|
|Menor igual|a <= b|a.compareTo(b)<=0|
|Igual|a == b|a.equals(b)|
|Diferente|a != b|!(a.equals(b))|

## Operadores Logicos
|Função|Expressão|Comando|
|-|-|-|
|E|(&&)|a and b|
|Ou|()|a or b|
|Contém|in|a in b|
|Não comtém|!in|a !in b|
|Range|..|a..b|

## Manipulação de Strings
### String como array
```Kotlin
var s = "Ola, Mundo!"

println(s[0])
println(s.first())
//IMPRIME O

println(s[s.lenght-1])
println(s.last())
//IMPRIME !
```
### Concatenação
```Kotlin
val name = "Ana"
val s = "Olá"

println(s + name)
//IMPRIME OláAna

println("${s}, ${name}!")
//IMPRIME Olá, Ana!

println("Bem vindo(a), $name!")
//IMPRIME Bem vindo(a), Ana!
```

### Formatação
|Nome|Função|Metodos|
|-|-|-|
|Captalização|Alterar formatação entre Maiuscula e Minuscula|captalize(), toUpperCase(), toLowerCase(), decaptalize()|
|Remoção de espaços|Remove espaços vazios|tremEnd(), trimStart(), trim()|
|Substituição de caracteres|Substitui caracteres por outros|replace(x,y)|
|Formatação|Formata outros clores para um padrão|"padrão ${valor}".format(valor)|

### Empty ou Blank
```Kotlin
val empty = ""
val blank = "  "

println(empty.isEmpty()) //true
println(empty.isBlank()) //true
println(blank.isEmpty()) //false
println(blank.isBlank()) //true
```
Empty: tamanho da string é igual a 0.  
Blank: todos os caracteres são espaços em branco.

## Funções
```Kotlin
private fun getFullName(name:String, lastName:String):String{
  val fullName = "$name $lastName"
  return fullName
}
```

### Função de ordem superior
```Kotlin
fun main(){
  val z:Int

  z = calculate(34, 90, ::sum)
  
  println(z)
}

fun sum(a1:Int,a2:Int) = a1.plus(a2)

fun calculate(n1:Int,n2:Int,operation:(Int,Int)->Int):Int{
  val result = operation(n1,n2)
  return result
}
```

### Função de linha unica
```Kotlin
  fun getFullName(name:String, lastName:String) = "$name $lastName"
```

### Função de extensão
```Kotlin
  fun String.randomCaptalizedLetter() = this[(0..this.lengh-1).random()].toUpperCase()
```

## Estruturas de controle
### if/else:
```Kotlin
if(expressão){
  //bloco de codigo
}else if(expressão){
  //bloco de codigo
}else if(expressão){
  //bloco de codigo
}
```
### when:
```Kotlin
when{
  case1 -> {}
  case2 -> {}
  case3 -> {}
  else -> {}
}
```
### elvis operator:
```Kotlin
val a:Int? = null
var number = a ?: 0
```

## Estruturas de repetição
### while:
```Kotlin
while(condição){
  //CODIGO
}
```
### do while:
```Kotlin
do{
  //CODIGO
}while(condição)
```

### for:
in:
```Kotlin
for(i in 0..20){
  //CODIGO
}
```
step:
```Kotlin
for(i in 0..20 step 2){
  //CODIGO
}
```
until:
```Kotlin
for(i in 0 until 10){
  //CODIGO
}
```
downTo:
```Kotlin
for(i in 10 downTo 0){
  //CODIGO
}
```
letter:
```Kotlin
var text = "Kotlin"
for(letter in text){
  //CODIGO
}
```