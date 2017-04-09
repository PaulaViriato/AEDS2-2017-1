**Universidade Federal de Minas Gerais**

**Disciplina: DCC065 - Sistemas Operacionais**

**Professor: Flavio Vinicius Diniz de Figueiredo**

# Lista de Exercícios - Prova 1

## TADs

1. Crie um Tipo Abstrato de Dados para Matrizes. Implemente as funções de
   inicializar a matriz (toda zerada), computar a soma de duas matrizes,
   subtração de duas matrizes e o determinante de uma matriz quadrada. Seu
   programa pode indicar um erro caso a matriz passada para o determinante não
   seja quadrada.

   * Indique a complexidade de todas as funções
   * Justifique as assinaturas de cada função

1. Crie um TAD para pontos em um espaço $n$-dimensional (Euclidean space).
   Implemente funções para inicializar um ponto, computar a distância entre
   dois pontos, a norma de dois pontos, o ângulo dos pontos e 
   rotacionar o espaço.

   * https://en.wikipedia.org/wiki/Euclidean_space
   * https://en.wikipedia.org/wiki/Rotation_matrix
   * Indique a complexidade de todas as funções
   * Justifique as assinaturas de cada função

## Revisão C + Complexidade

1. Escreva um algoritmo que determina se um número inteiro é primo. Qual
   é a complexidade do seu algoritmo?

1. Escreva um algoritmo que compacta uma string. A compactação de uma string
   é uma operação que simplesmente conta o número de ocorrências de letras na
   string retornando uma nova string de tamanho menor. Por exemplo, a string:

   ``` aaaaabcdddeeeffffff   abc```

   É compactada para:

   ```a5b1c2d3e3f6 3a1b1c1```

   Sua função deve ter uma assinatura como:

   ```c
   char *compact(char *string)
   ```

   Escreva também a função inversa

   ```c
   char *descompact(char *string)
   ```

   Indique a complexidade das duas funções em termos do tamanho das strings.

1. Implemente uma função que recebe como entrada um vetor de números inteiros,
   `vec`, o tamanho do mesmo `n`, junto com um número inteiro `target`. Sua
   função deve indicar se no vetor `vec` existem dois elementos cuja soma é
   `target`. Por exemplo:
 
   ```
   vec = [10, 20, 3, 45, 0]
   target = 65
   return 1 //45 + 20 = 65
   ```
   
   ```
   vec = [10, 20, 3, 45, 0]
   target = 29
   return 0 //não existem tais elementos
   ```

   Assinatura:
   ```c
   int existeSoma(int *vec, int n, int target)
   ```

   Qual a complexidade da sua função?

1. Escreva uma função que inverte as palavras de uma string. Por exemplo:

   ```
   Alice Likes Bob
   ```
   é convertido para
   ```
   Bob Likes Alice
   ```

   Assinatura:
   ```c
   char *invertWords(char *string)
   ```
   
   Para auxiliar seu método, pode utilizar `strtok` da `string.h`.
   Sua função funciona quando mais de um espaço entre palavras é inserido?
   Qual a complexidade da sua função?

1. Escreva uma função para encontrar o local de início de fim de uma
   substring string dentro de outra string. A assinatura da função é:
   
   ```c
   void subPosition(char *text, char *sub, int *start, int *end)
   ```
   
   Para uma entrada:
   
   ```c
   char *sub = "muito";
   char *texto = "Eu gosto muito de AEDS2";
   ```
   
   Seu método deve retornar:
   
   ```c
   *start = 9;
   *end = 13;
   ```
   
   Qual a complexidade da sua função?

## Complexidade

1. Para cada uma das afirmativas abaixo, diga se a afirmativa é verdadeira (V) ou falsa (F). Em todas as afirmativas, justifique a sua resposta. Respostas sem justificativa não serão consideradas.

   1. Considere um programa P que faz uma série de operações de custo constante, chama uma função F1 com complexidade dada por f(n) e depois chama uma função F2 com complexidade dada por g(n), onde g(n) = 1000 * f(n). Pode-se afirmar que o programa P é O(f(n)).