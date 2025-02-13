# portugol-atrasado
    //Enviando com dias de atraso por ter uma carga de trabalhos e provas para apresentar e estudar
programa
{
    funcao inicio()
    {
        inteiro i
        real numeros[10], quadrados[10]
        
  para (i = 0; i < 10; i++)
        {
            escreva("Digite um número real: ")
            leia(numeros[i])
            quadrados[i] = numeros[i] * numeros[i]
        }
        escreva("\nQuadrados dos números:\n")
        para (i = 0; i < 10; i++)
        {
            escreva("Número: ", numeros[i], " -> Quadrado: ", quadrados[i], "\n")
        }
    }
}

programa
{
    funcao inicio()
    {
        inteiro vetor[8], x, y
        para (inteiro i = 0; i < 8; i++)
        {
            escreva("Digite um número para a posição ", i, ": ")
            leia(vetor[i])
        }
        escreva("Digite a posição X: ")
        leia(x)
        escreva("Digite a posição Y: ")
        leia(y)
        
   se (x >= 0 e x < 8 e y >= 0 e y < 8)
        {
            escreva("Soma dos valores: ", vetor[x] + vetor[y], "\n")
        }
        senao
        {
            escreva("Posições inválidas!")
        }
    }
}

programa
{
    funcao inicio()
    {
        inteiro i, vetor[6], num, count = 0
        enquanto (count < 6)
        {
            escreva("Digite um número par: ")
            leia(num)
            se (num % 2 == 0)
            {
                vetor[count] = num
                count++
            }
            senao
            {
                escreva("O número não é par! Tente novamente.\n")
            }
        }
   
  escreva("\nNúmeros na ordem inversa:\n")
        para (i = 5; i >= 0; i--)
        {
            escreva(vetor[i], " ")
        }
    }
}

programa
{
    funcao inicio()
    {
        inteiro vetor[5], maior, menor, posMaior, posMenor
        
  para (inteiro i = 0; i < 5; i++)
        {
            escreva("Digite um número: ")
            leia(vetor[i])
        }

   maior = vetor[0]
        menor = vetor[0]
        posMaior = 0
        posMenor = 0

  para (inteiro i = 1; i < 5; i++)
        {
            se (vetor[i] > maior)
            {
                maior = vetor[i]
                posMaior = i
            }
            se (vetor[i] < menor)
            {
                menor = vetor[i]
                posMenor = i
            }
        }

        // Exibindo os resultados
  escreva("Maior valor: ", maior, " na posição ", posMaior, "\n")
        escreva("Menor valor: ", menor, " na posição ", posMenor, "\n")
    }
}

programa
{
    funcao inicio()
    {
        inteiro vetor1[10], vetor2[10], vetor3[10]

        // Lendo o primeiro vetor
  para (inteiro i = 0; i < 10; i++)
        {
            escreva("Digite um número para o primeiro vetor na posição ", i, ": ")
            leia(vetor1[i])
        }

        // Lendo o segundo vetor
   para (inteiro i = 0; i < 10; i++)
        {
            escreva("Digite um número para o segundo vetor na posição ", i, ": ")
            leia(vetor2[i])
        }

        // Criando o terceiro vetor
   para (inteiro i = 0; i < 10; i++)
        {
            se (i % 2 == 0)
            {
                vetor3[i] = vetor1[i]
            }
            senao
            {
                vetor3[i] = vetor2[i]
            }
        }

        // Exibindo o terceiro vetor
  escreva("\nVetor resultante:\n")
        para (inteiro i = 0; i < 10; i++)
        {
            escreva(vetor3[i], " ")
        }
    }
}

programa
{
    funcao inicio()
    {
        inteiro m, p, n

   escreva("Digite as dimensões da matriz A (m p): ")
        leia(m, p)
        escreva("Digite as dimensões da matriz B (p n): ")
        leia(p, n)

   inteiro A[m][p], B[p][n], C[m][n]

        // Lendo matriz A
  escreva("Digite os elementos da matriz A:\n")
        para (inteiro i = 0; i < m; i++)
        {
            para (inteiro j = 0; j < p; j++)
            {
                leia(A[i][j])
            }
        }

        // Lendo matriz B
   escreva("Digite os elementos da matriz B:\n")
        para (inteiro i = 0; i < p; i++)
        {
            para (inteiro j = 0; j < n; j++)
            {
                leia(B[i][j])
            }
        }

        // Multiplicação das matrizes
  para (inteiro i = 0; i < m; i++)
        {
            para (inteiro j = 0; j < n; j++)
            {
                C[i][j] = 0
                para (inteiro k = 0; k < p; k++)
                {
                    C[i][j] = C[i][j] + A[i][k] * B[k][j]
                }
            }
        }

        // Exibindo matriz C
  escreva("Matriz resultante C:\n")
        para (inteiro i = 0; i < m; i++)
        {
            para (inteiro j = 0; j < n; j++)
            {
                escreva(C[i][j], " ")
            }
            escreva("\n")
        }
    }
}

programa
{
    funcao inicio()
    {
        inteiro A

   escreva("Digite a ordem da matriz identidade: ")
        leia(A)

  inteiro identidade[A][A]

        // Preenchendo a matriz identidade
  para (inteiro i = 0; i < A; i++)
        {
            para (inteiro j = 0; j < A; j++)
            {
                se (i == j)
                {
                    identidade[i][j] = 1
                }
                senao
                {
                    identidade[i][j] = 0
                }
            }
        }

        // Exibindo a matriz identidade
escreva("Matriz Identidade:\n")
        para (inteiro i = 0; i < A; i++)
        {
            para (inteiro j = 0; j < A; j++)
            {
                escreva(identidade[i][j], " ")
            }
            escreva("\n")
        }
    }
}

programa
{
    funcao inicio()
    {
        inteiro n

  escreva("Digite a ordem da matriz quadrada: ")
        leia(n)

   inteiro matriz[n][n]
        logico simetrica = verdadeiro

        // Lendo a matriz
 escreva("Digite os elementos da matriz:\n")
        para (inteiro i = 0; i < n; i++)
        {
            para (inteiro j = 0; j < n; j++)
            {
                leia(matriz[i][j])
            }
        }

        // Verificando se a matriz é simétrica
 para (inteiro i = 0; i < n; i++)
        {
            para (inteiro j = 0; j < n; j++)
            {
                se (matriz[i][j] != matriz[j][i])
                {
                    simetrica = falso
                }
            }
        }

        // Exibindo o resultado
 se (simetrica)
        {
            escreva("A matriz é simétrica.\n")
        }
        senao
        {
            escreva("A matriz não é simétrica.\n")
        }
    }
}

programa
{
    funcao inicio()
    {
        inteiro matriz[4][4]

        // Preenchendo a matriz com o produto do índice da linha e coluna
   para (inteiro i = 0; i < 4; i++)
        {
            para (inteiro j = 0; j < 4; j++)
            {
                matriz[i][j] = i * j
            }
        }

        // Exibindo a matriz
  escreva("Matriz 4x4 preenchida:\n")
        para (inteiro i = 0; i < 4; i++)
        {
            para (inteiro j = 0; j < 4; j++)
            {
                escreva(matriz[i][j], " ")
            }
            escreva("\n")
        }
    }
}

programa
{
    funcao inicio()
    {
        inteiro matriz[5][5], x, linha = -1, coluna = -1

        // Lendo a matriz
  escreva("Digite os elementos da matriz 5x5:\n")
        para (inteiro i = 0; i < 5; i++)
        {
            para (inteiro j = 0; j < 5; j++)
            {
                leia(matriz[i][j])
            }
        }

        // Lendo o valor a ser buscado
 escreva("Digite o valor a ser buscado: ")
        leia(x)

        // Procurando o valor na matriz
   para (inteiro i = 0; i < 5; i++)
        {
            para (inteiro j = 0; j < 5; j++)
            {
                se (matriz[i][j] == x)
                {
                    linha = i
                    coluna = j
                }
            }
        }

        // Exibindo o resultado da busca
 se (linha != -1)
        {
            escreva("Valor encontrado na posição (", linha, ", ", coluna, ")\n")
        }
        senao
        {
            escreva("Valor não encontrado na matriz.\n")
        }
    }
}
