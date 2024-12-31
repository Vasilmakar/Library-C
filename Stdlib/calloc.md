## Opis szczegółowy

Funkcja calloc alokuje blok pamięci na tablicę nmemb elementów, o rozmiarze size każdy i inicjalizuje ten blok zerami.

#include <stdio.h>
#include <stdlib.h>

int main() {
    int *numbers;
    int size = 10; // Розмір масиву

    // Виділення пам'яті для 10 цілих чисел
    numbers = (int*)calloc(size, sizeof(int));

    if (numbers == NULL) {
        printf("Помилка виділення пам'яті!\n");
        return 1;
    }

    // Ініціалізація не потрібна, оскільки calloc вже все занулив
    for (int i = 0; i < size; ++i) {
        printf("%d ", numbers[i]); // Виведе: 0 0 0 0 0 0 0 0 0 0
    }

    // Звільнення виділеної пам'яті
	    z

    return 0;
}