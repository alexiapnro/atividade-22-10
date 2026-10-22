#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main(int argc, char *argv[]) {
    char palavra[100];
    int i, j, tamanho;
    int eh_palindromo = 1; // 1 significa verdadeiro, 0 significa falso

    // Lê a palavra do usuário
    printf("Digite uma palavra: ");
    scanf("%s", palavra);

    tamanho = strlen(palavra);
    j = tamanho - 1; // Aponta para a última letra

    // Compara as letras das extremidades até o centro
    for (i = 0; i < j; i++) {
        if (palavra[i] != palavra[j]) {
            eh_palindromo = 0; // Se encontrar diferença, não é palíndromo
            break;
        }
        j--; // Move o índice do fim para a esquerda
    }

    // Exibe o resultado conforme o enunciado
    if (eh_palindromo) {
        printf("é um palindromo\n");
    } else {
        printf("nao é um palindromo\n");
    }

    return 0;
}
