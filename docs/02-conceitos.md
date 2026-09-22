\# Conceitos Fundamentais



\## 2.1 Estruturas de Dados Dinâmicas



Estruturas de dados dinâmicas são formas de organizar informações que permitem modificar a quantidade de elementos durante a execução de um programa. Em C, essas estruturas podem utilizar ponteiros e funções de alocação dinâmica de memória, como `malloc` e `free`.



A principal vantagem é a flexibilidade, pois a memória pode ser alocada conforme a necessidade do programa. Entre os exemplos mais conhecidos estão as listas encadeadas, pilhas e filas.



\---



\## 2.2 Lista Encadeada



\### Definição



Uma lista encadeada é uma estrutura de dados formada por elementos chamados nós (\*nodes\*). Cada nó armazena uma informação e um ponteiro que indica o próximo nó da lista.



Diferentemente de um vetor, os elementos de uma lista encadeada não precisam estar armazenados em posições consecutivas da memória.



Um nó básico de uma lista encadeada simples pode ser representado da seguinte forma:



```c

typedef struct No {

\\\&#x20;   int valor;

\\\&#x20;   struct No \\\\\\\*proximo;

} No;

```



Nesse exemplo:



\- `valor`: armazena a informação do nó.

\- `proximo`: aponta para o próximo nó da lista.

\- `NULL`: indica que não existe um próximo nó.



\### Operações principais



\*\*Inserção:\*\* adiciona um novo elemento à lista. Pode ocorrer no início, no final ou em uma posição específica.



\*\*Remoção:\*\* retira um elemento da lista, ajustando os ponteiros necessários.



\*\*Percurso:\*\* percorre os nós da lista, geralmente do primeiro até o último, para consultar ou processar os dados.



\*\*Busca:\*\* verifica se determinado valor está presente na lista.



\### Quando utilizar?



As listas encadeadas podem ser utilizadas quando a quantidade de elementos varia frequentemente e quando é importante realizar inserções e remoções sem deslocar vários elementos, como pode ocorrer em um vetor.



\---



\## 2.3 Pilha



\### Definição



Uma pilha (\*stack\*) é uma estrutura de dados que segue o princípio \*\*LIFO (Last In, First Out)\*\*, que significa "o último a entrar é o primeiro a sair".



Uma forma simples de imaginar uma pilha é pensar em pratos empilhados. O último prato colocado sobre a pilha é o primeiro que pode ser retirado.



\### Operações principais



\*\*Push:\*\* adiciona um elemento ao topo da pilha.



\*\*Pop:\*\* remove o elemento que está no topo.



\*\*Peek ou Top:\*\* consulta o elemento do topo sem removê-lo.



\*\*isEmpty:\*\* verifica se a pilha está vazia.



\### Quando utilizar?



As pilhas são utilizadas em diversas situações, como:



\- Controle de chamadas de funções.

\- Desfazer ações em programas (\*undo\*).

\- Avaliação de expressões matemáticas.

\- Navegação e processamento de estruturas que seguem a ordem LIFO.



Uma pilha pode ser implementada utilizando vetores ou listas encadeadas.



\---



\## 2.4 Fila



\### Definição



Uma fila (\*queue\*) é uma estrutura de dados que segue o princípio \*\*FIFO (First In, First Out)\*\*, que significa "o primeiro a entrar é o primeiro a sair".



Um exemplo do cotidiano é uma fila de atendimento: normalmente, a pessoa que chega primeiro é atendida antes das que chegam depois.



\### Operações principais



\*\*Enqueue:\*\* adiciona um elemento ao final da fila.



\*\*Dequeue:\*\* remove o elemento que está no início da fila.



\*\*Front:\*\* consulta o primeiro elemento sem removê-lo.



\*\*isEmpty:\*\* verifica se a fila está vazia.



\### Quando utilizar?



As filas podem ser utilizadas em situações que precisam respeitar a ordem de chegada dos elementos, como:



\- Sistemas de atendimento.

\- Gerenciamento de tarefas.

\- Filas de impressão.

\- Processamento de solicitações em sistemas computacionais.



Assim como as pilhas, as filas podem ser implementadas com vetores ou estruturas encadeadas.



\---



\## 2.5 Comparação entre as estruturas



| Estrutura | Princípio | Inserção | Remoção |

|---|---|---|---|

| Lista encadeada | Sequência de nós | Posições variadas | Posições variadas |

| Pilha | LIFO | Topo | Topo |

| Fila | FIFO | Final | Início |



A escolha da estrutura depende do problema que está sendo resolvido. Listas encadeadas oferecem flexibilidade na organização dos elementos, enquanto pilhas e filas possuem regras específicas para a entrada e a saída de dados.

