## Zwracana wartość

Zwraca długość przekonwertowanego łańcucha znaków, nie licząc znaku terminalnego. Jeżeli zwracana wartość jest większa lub równa argumentowi _count_ - zawartość _dest_ jest nieprzewidywalna.  
  
W przypadku wystąpienia błędu funkcja ustawia **errno** i zwraca INT_MAX.  

## Dodatkowe informacje

Po dokonaniu transformacji łańcucha znaków, porównanie tekstu za pomocą funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [strcmp](https://cpp0x.pl/dokumentacja/?nro=320 "strcmp (funkcja)") zwraca identyczny wynik jak funkcja » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [strcoll](https://cpp0x.pl/dokumentacja/?nro=429 "strcoll (funkcja)") wywołana z oryginalnymi łańcuchami znaków.  

## Przykład

C/C++

#include <cstdio>  
#include <cstring>  
#include <clocale>  
  
int main()  
{  
    char str1[] = "x a x";  
    char str2[] = "x ą x";  
    char str3[] = "x b x";  
     
    setlocale( LC_ALL, "Polish" );  
    printf( "setlocale = Polish\n" );  
    printf( "strcmp: %d, %d\n", strcmp( str1, str2 ), strcmp( str2, str3 ) );  
    printf( "strcoll: %d, %d\n", strcoll( str1, str2 ), strcoll( str2, str3 ) );  
     
    printf( "\nUzycie funkcji strxfrm:\n" );  
    char str1x[ 20 ];  
    char str2x[ 20 ];  
    char str3x[ 20 ];  
    strxfrm( str1x, str1, sizeof( str1x ) );  
    strxfrm( str2x, str2, sizeof( str2x ) );  
    strxfrm( str3x, str3, sizeof( str3x ) );  
    printf( "strcmp: %d, %d\n", strcmp( str1x, str2x ), strcmp( str2x, str3x ) );  
    return 0;  
}