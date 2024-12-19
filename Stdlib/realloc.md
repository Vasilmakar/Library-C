#include <stdio.h>
#include <stdlib.h>

int main() {
    int *arr, i, n = 5;

    // Виділяємо пам'ять для масиву з 5 елементів
    arr = (int *)malloc(n * sizeof(int));

    // Заповнюємо масив значеннями
    for (i = 0; i < n; ++i) {
        arr[i] = i + 1;
    }

    // Збільшуємо розмір масиву до 10 елементів
    n = 10;
    arr = (int *)realloc(arr, n * sizeof(int));

    if (arr == NULL) {
        printf("Помилка при розширенні масиву!\n");
        return 1;
    }

    // Заповнюємо нові елементи масиву
    for (i = 5; i < n; ++i) {
        arr[i] = i + 1;
    }

    // Виводимо елементи масиву
    for (i = 0; i < n; ++i) {
        printf("%d ", arr[i]);
    }

    free(arr);
    return 0;
}