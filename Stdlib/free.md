>[!Note]
>**Передача вказівника:** Передаємо в `free` саме вказівник, а не значення за ним.

#include <stdio.h>
#include <stdlib.h>

int main() {
    int *numbers;
    int size = 10;

    // Виділяємо пам'ять для масиву з 10 цілих чисел
    numbers = (int*)calloc(size, sizeof(int));

    if (numbers == NULL) {
        printf("Помилка виділення пам'яті!\n");
        return 1;
    }

    // Використовуємо масив (наприклад, заповнюємо його значеннями)
    for (int i = 0; i < size; ++i) {
        numbers[i] = i * 2;
    }

    // Звільняємо виділену пам'ять
    free(numbers);

    return 0;
}