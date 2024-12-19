## Zwracana wartość

Funkcja zwraca wartość z łańcucha znaków przekonwertowaną do postaci liczbowej (typ double) w przypadku sukcesu.  
  
Funkcja zwraca wartość zero w przypadku gdy nie jest możliwe dokonanie konwersji łańcucha znaków przekazanego jako argument funkcji.  

## Opis szczegółowy

Funkcja konwertuje wartość zapisaną w łańcuchu znaków do postaci liczby zmiennoprzecinkowej typu double.  

## Przykład

C/C++

#include <cstdio>  
#include <cstdlib>  
  
int main()  
{  
    printf( "Obwod kola wynosi: %.4f\n",( 2 * 3.14 * atof( "12.55" ) ) );  
    return 0;  
}

Standardowe wyjście programu:  

Obwod kola wynosi: 78.8140