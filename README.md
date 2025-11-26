#include <stdio.h>

int main() {
    // -------------------------------------------------
    // MOVIMENTOS DAS OUTRAS PEÇAS (EXEMPLO)
    // Aqui você deixa o que já fez no desafio anterior.
    // -------------------------------------------------

    printf("Movimentos das outras pecas:\n");

    int casasCima = 3;
    for (int i = 0; i < casasCima; i++) {
        printf("Cima\n");
    }

    int casasDireita = 2;
    int contadorDireita = 0;
    while (contadorDireita < casasDireita) {
        printf("Direita\n");
        contadorDireita++;
    }

    // -------------------------------------------------
    // MOVIMENTO DO CAVALO EM "L"
    // -------------------------------------------------

    int movimentosVerticais = 2;   // duas casas para baixo
    int movimentosHorizontais = 1; // uma casa para a esquerda

    printf("\n"); // linha em branco separando os movimentos
    printf("Movimento do Cavalo (em L):\n");

    /*
        O Cavalo deve fazer: Baixo, Baixo, Esquerda

        - Usamos um loop FOR para os movimentos verticais (Baixo)
        - Dentro dele, usamos um WHILE que faz o movimento para a esquerda
          apenas quando chegamos no último "Baixo".
    */

    for (int vertical = 0; vertical < movimentosVerticais; vertical++) {
        printf("Baixo\n");  // anda uma casa para baixo

        int h = 0;
        while (h < movimentosHorizontais && vertical == movimentosVerticais - 1) {
            printf("Esquerda\n");
            h++;
        }
    }

    return 0;
}
