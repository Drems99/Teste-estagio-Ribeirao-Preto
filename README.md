# Teste-estagio-Ribeirao-Preto 1
#include <stdio.h>

int pertenceFibonacci(int numero) {

    int a = 0, b = 1, proximo;


    if (numero == 0 || numero == 1) {
        return 1;
    }


    while (b <= numero) {
        if (b == numero) {
            return 1;
        }
        proximo = a + b;
        a = b;
        b = proximo;
    }

    return 0;
}

int main() {
    int numero;


    printf("Informe um numero: ");
    scanf("%d", &numero);

    // Verifica se o número pertence à sequência de Fibonacci
    if (pertenceFibonacci(numero)) {
        printf("O numero %d pertence a sequencia de Fibonacci.\n", numero);
    } else {
        printf("O numero %d nao pertence a sequencia de Fibonacci.\n", numero);
    }

    return 0;
}
