## Przykład
#include <cstdio>  
#include <cstdlib>  
int main()  
{  
    int liczba = atol( "999999999" );  
    printf( "Dwa razy %d rowna sie %d.\n", liczba, liczba * 2 );  
    return 0;  
} 


## Opis szczegółowy
Funkcja konwertuje wartość zapisaną w łańcuchu znaków do postaci liczby całkowitej typu long.

## Zwracana wartość
Funkcja zwraca wartość z łańcucha znaków przekonwertowaną do postaci liczbowej (typ long) w przypadku sukcesu.  
  
Funkcja zwraca wartość zero w przypadku gdy nie jest możliwe dokonanie konwersji łańcucha znaków przekazanego jako argument funkcji.

