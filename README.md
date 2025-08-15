# Linguagem-C---Estrutura 
#include<stdio.h>
#include<locale.h>


typedef struct
{
    int codigo;
    char nome[30];
    int publicacao;
    char genero[20];



}STRU_LIVROS;

void main(){
    setlocale(LC_ALL, "Portuguese");
    STRU_LIVROS livros[2];
    int cont;

    for(cont=0; cont<=1; cont++)
    {
        printf("Digite o código do livro: ");
        scanf("%d%*c", &livros[cont].codigo);
        printf("Digite o nome do Livro desejado: ");
        gets(livros[cont].nome);
        printf("Digite o ano da Publicação do Livro: ");
        scanf("%d%*c", &livros[cont].publicacao);
        printf("Digite o Gênero do Livro: ");
        gets(livros[cont].genero);

        printf("\n\n");

    }
     printf("+----------------------+");
     printf("\n<<CONTROLE DE LIVROS>>");

     for (cont = 0; cont<=1; cont++)

     {
         printf("\n+----------------------+");
         printf("\nCódigo %d do livro: ",livros[cont].codigo);
         printf("\nNome: %s", livros[cont].nome);
         printf("\nAno %d do livro: ", livros[cont].publicacao);
         printf("\nGenero: %s", livros[cont].genero);

         printf("\n+----------------------+");

         printf("\n\n");

     }
}

