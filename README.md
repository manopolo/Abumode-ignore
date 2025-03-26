# Abumode-ignore
programa
{
    funcao inicio()
    {
        // Declaração de variáveis
        cadeia nomes[20]
        inteiro idades[20]
        inteiro i, maiorIdade, menorIdade, posicaoMaior, posicaoMenor

        // Entrada de dados
        para (i = 0; i < 20; i++)
        {
            escreva("Digite o nome da pessoa ", i + 1, ": ")
            leia(nomes[i])
            escreva("Digite a idade de ", nomes[i], ": ")
            leia(idades[i])
        }

        // Inicializando variáveis para encontrar idoso e jovem
        maiorIdade = idades[0]
        menorIdade = idades[0]
        posicaoMaior = 0
        posicaoMenor = 0

        // Encontrar a maior e a menor idade
        para (i = 1; i < 20; i++)
        {
            se (idades[i] > maiorIdade)
            {
                maiorIdade = idades[i]
                posicaoMaior = i
            }
            se (idades[i] < menorIdade)
            {
                menorIdade = idades[i]
                posicaoMenor = i
            }
        }

        // Saída de dados
        escreva("\nPessoa mais idosa: ", nomes[posicaoMaior], " com ", maiorIdade, " anos.")
        escreva("\nPessoa mais jovem: ", nomes[posicaoMenor], " com ", menorIdade, " anos.")
    }
}
