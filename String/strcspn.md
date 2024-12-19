string complementary span

>[!Note]
>Повертає число відстань від початку ланцюга

>[!Note]
Дуже важливо ідентифікатор %d вписувати саме в подвійних дужках

## Przykład

C/C++

#include <cstdio>  
#include <cstring>  
  
int main() {  
     
    char str1[] = "Dokumentacja silnika krokowego.\n";  
    char str2[] = "123Mama76s";  
    short indeks;  
    indeks = strcspn( str1, str2 );  
     
    printf( "Znaleziony znak znajduje sie na %d pozycji.\n", indeks + 1 );  
    return 0;  
}

## Dodatkowe informacje

Funkcja zawsze znajduje wystąpienie znaku, ponieważ znak kończący łańcuch znaków jest również uwzględniany w wyszukiwaniu. W efekcie, jeśli znaki stanowiące łańcuch znaków str2 nie zostaną znalezione w pierwszym łańcuchu, funkcja zwróci długość pierwszego łańcucha znaków.