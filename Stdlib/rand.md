## Zwracana wartość

Zwraca pseudolosową liczbę całkowitą.  

## Opis szczegółowy

Funkcja zwraca pseudolosową liczbę całkowitą, która zawiera się w zakresie od 0 do » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [RAND_MAX](https://cpp0x.pl/dokumentacja/?nro=581 "RAND_MAX (makro)").  

## Dodatkowe informacje

Zaleca się wywołanie funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [srand](https://cpp0x.pl/dokumentacja/?nro=587 "srand (funkcja)") w celu ustawienia pseudolosowego generatora numerów zanim zacznie się korzystać z funkcji rand.  

## Przykład

C/C++

#include <cstdlib>  
#include <cstdio>  
#include <ctime>  
  
int main()  
{  
    srand( time( NULL ) );  
     
    for( int i = 0; i < 10; i++ )  
         printf( "Wylosowano %d\n", rand() );  
     
}