# Exercicio Final
```Kotlin
fun main() {
    var valor1 = 2.5
    var valor2 = 2
    
    //1 = Adição
    //2 = Subtração
    //3 = Multiplicação
    //4 = Divisão
    var operação = 4
    
    var resultado = when{
       	operação == 1 -> valor1.plus(valor2)
        operação == 2 -> valor1.minus(valor2)
        operação == 3 -> valor1.times(valor2)
        operação == 4 -> valor1.div(valor2)
        else -> "Invalido"
    }
    
    println("O resultado do calculo é $resultado")
}
```