## Przykład

C/C++

#include <cstring>  
#include <cstdio>  
  
int main( void )  
{  
    char napis[] = "ccbcaax";  
    int i = strspn( napis, "cbx" );  
    printf( "Wynik = %d\n", i );  
    return 0;  
}

## Opis szczegółowy

Funkcja zwraca indeks pierwszego znaku (należącego do _str1_), który nie występuje w łańcuchu znaków _str2_. Znak terminalny w _str2_ nie wlicza się do przeszukiwanej puli znaków