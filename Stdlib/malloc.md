## Zwracana wartość

Wskaźnik na zaalokowany blok pamięci lub NULL w przypadku błędu.

#include <stdio.h>
#include <stdlib.h>

int main() {
    int *ptr, i, n;

    printf("Введіть кількість елементів масиву: ");
    scanf("%d", &n);

    // Виділяємо пам'ять для масиву з n цілих чисел
    ptr = (int*)malloc(n * sizeof(int));

    if (ptr == NULL) {
        printf("Помилка виділення пам'яті!\n");
        return 1;
    }

    // Заповнюємо масив значеннями
    for (i = 0; i < n; ++i) {
        ptr[i] = i + 1;
    }

    // Виводимо елементи масиву
    printf("Елементи масиву:\n");
    for (i = 0; i < n; ++i) {
        printf("%d ", ptr[i]);
    }

    // Звільняємо виділену пам'ять
    free(ptr);

    return 0;
}