## Przykład
#include <stdio.h>
#include <string.h>
int main() { 
char str[] = "Hello, world!";
char *ptr* = memchr(str, 'a', strlen(str)); 
if (ptr != NULL){
printf("Символ 'a' знайдено на позиції: %ld\n", ptr - str); 
}
else {
printf("Символ 'a' не знайдено.\n"); 
}
return 0;
}

## Opis szczegółowy

Szuka pierwszego wystąpienia _value_ (interpretowanego jako unsigned char) w pierwszych _num_ bajtach bloku wskazywanego przez _ptr_.

## Zwracana wartość
Wskaźnik na pierwszy znaleziony bajt równy _value_ jeśli znaleziono; w przeciwnym wypadku pusty wskaźnik.

