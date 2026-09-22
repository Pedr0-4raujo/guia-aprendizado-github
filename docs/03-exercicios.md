\# Exercícios Práticos



Os exercícios a seguir têm como objetivo reforçar os conceitos de listas encadeadas, pilhas e filas, permitindo que o leitor pratique a implementação de estruturas de dados em linguagem C.



\## Exercício 1 — Inserção no início de uma lista encadeada



Implemente uma função que receba o ponteiro para o início de uma lista encadeada simples e um valor inteiro.



A função deve criar um novo nó e inseri-lo no início da lista.



\*\*Requisitos:\*\*

\- Utilizar `malloc` para alocar o novo nó.

\- Atualizar o ponteiro para o início da lista.

\- Retornar ou atualizar corretamente a referência da lista.



\---



\## Exercício 2 — Remoção de um elemento da lista



Crie uma função que remova da lista encadeada o primeiro nó que contenha um determinado valor.



\*\*Requisitos:\*\*

\- Verificar se a lista está vazia.

\- Localizar o nó que contém o valor.

\- Ajustar os ponteiros dos nós envolvidos.

\- Liberar a memória do nó removido utilizando `free`.



\---



\## Exercício 3 — Implementação de uma pilha



Implemente uma pilha utilizando uma lista encadeada.



O programa deve permitir as seguintes operações:



\- Inserir um elemento no topo (\*push\*).

\- Remover um elemento do topo (\*pop\*).

\- Consultar o elemento do topo (\*peek\*).

\- Verificar se a pilha está vazia.



Ao final, teste a pilha com diferentes valores inteiros e observe a ordem de remoção dos elementos.



\---



\## Exercício 4 — Implementação de uma fila



Crie uma fila utilizando uma estrutura encadeada.



O programa deve permitir:



\- Inserir elementos no final da fila (\*enqueue\*).

\- Remover elementos do início da fila (\*dequeue\*).

\- Consultar o primeiro elemento.

\- Verificar se a fila está vazia.



Teste a implementação inserindo pelo menos cinco valores e removendo-os para verificar se a ordem FIFO está sendo respeitada.



\---



\## Exercício 5 — Percurso e contagem de elementos



Implemente uma função que percorra uma lista encadeada e retorne a quantidade total de nós existentes.



\*\*Requisitos:\*\*

\- Percorrer a lista utilizando ponteiros.

\- Contar cada nó encontrado.

\- Retornar zero caso a lista esteja vazia.



Como desafio adicional, implemente uma função que exiba todos os valores armazenados na lista.

