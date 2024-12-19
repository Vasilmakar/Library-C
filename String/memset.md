## Przykład
#include <stdio.h>
#include <string.h>

int main() {
    char str[20];
    memset(str, 'x', 20); // Wypełniamy tablicę znaków 'x'
    printf("%s\n", str); // Wyświetli: xxxxxxxxxxxxxxxxxxxx

    return 0;
}

## Co robi
**Funkcja memset** jest używana w programowaniu C i C++ do wypełnienia bloku pamięci określoną wartością. Innymi słowy, pozwala na szybkie "wyczyszczenie" lub zainicjalizowanie obszaru pamięci.