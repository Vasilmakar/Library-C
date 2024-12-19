#include <cstdio>  
#include <cstring>  
  
int main()  
{  
     
    char zrodlo[] = "Dokumentacja C++";  
    char przeznaczenie[ 4 ] = "";  
     
    strncpy( przeznaczenie, zrodlo, 3 );  
    printf( "Ilosc skopiowanych znakow: %u\n", strlen( przeznaczenie ) );  
    printf( "Tresc: %s\n", przeznaczenie );  
    return 0;  
}

## Zwracana wartość

Zwraca wskaźnik przekazany jako argument _dest_.