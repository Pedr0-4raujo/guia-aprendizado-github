\# Exemplo Básico — Lista Encadeada em C



\## Objetivo



Demonstrar como criar uma lista encadeada simples em C e inserir novos elementos no início da lista.



\## Código



```c

\\#include <stdio.h>

\\#include <stdlib.h>



// Definição do nó

typedef struct No {

\&#x20;   int valor;

\&#x20;   struct No \\\*proximo;

} No;



// Função para inserir um elemento no início

No\\\* inserirInicio(No \\\*inicio, int valor) {

\&#x20;   No \\\*novo = malloc(sizeof(No));



\&#x20;   if (novo == NULL) {

\&#x20;       printf("Erro ao alocar memoria.\\\\n");

\&#x20;       return inicio;

\&#x20;   }



\&#x20;   novo->valor = valor;

\&#x20;   novo->proximo = inicio;



\&#x20;   return novo;

}



// Função para exibir os elementos da lista

void exibirLista(No \\\*inicio) {

\&#x20;   No \\\*atual = inicio;



\&#x20;   while (atual != NULL) {

\&#x20;       printf("%d -> ", atual->valor);

\&#x20;       atual = atual->proximo;

\&#x20;   }



\&#x20;   printf("NULL\\\\n");

}



// Função para liberar a memória da lista

void liberarLista(No \\\*inicio) {

\&#x20;   No \\\*atual = inicio;



\&#x20;   while (atual != NULL) {

\&#x20;       No \\\*proximo = atual->proximo;

\&#x20;       free(atual);

\&#x20;       atual = proximo;

\&#x20;   }

}



int main() {

\&#x20;   No \\\*inicio = NULL;



\&#x20;   inicio = inserirInicio(inicio, 10);

\&#x20;   inicio = inserirInicio(inicio, 20);

\&#x20;   inicio = inserirInicio(inicio, 30);



\&#x20;   printf("Lista encadeada:\\\\n");

\&#x20;   exibirLista(inicio);



\&#x20;   liberarLista(inicio);



\&#x20;   return 0;

}

```



\## Explicação



\### 1. Definição do nó



A estrutura `No` possui duas informações: um valor inteiro e um ponteiro para o próximo nó.



\### 2. Criação de um novo nó



A função `inserirInicio` utiliza `malloc` para reservar espaço na memória para um novo nó.



O valor é armazenado em `novo->valor`, enquanto `novo->proximo` recebe o endereço do antigo primeiro nó.



\### 3. Atualização do início



A função retorna o novo nó, que passa a ser o primeiro elemento da lista.



Por isso, no `main`, utilizamos:



```c

inicio = inserirInicio(inicio, 10);

```



Dessa forma, o ponteiro `inicio` é atualizado após cada inserção.



\### 4. Resultado esperado



```text

Lista encadeada:

30 -> 20 -> 10 -> NULL

```



Como os elementos são inseridos sempre no início, o último valor inserido aparece primeiro na lista.



\### 5. Liberação da memória



A função `liberarLista` percorre todos os nós e utiliza `free` para liberar a memória alocada dinamicamente.



Essa etapa é importante para evitar o desperdício de memória durante a execução do programa.

