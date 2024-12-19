Та сама функція шо й strcmp, але ця байдужа до регістру

## Zwracana wartość

|Zwraca liczbę|Opis|
|---|---|
|0(zero)|str1 = str2|
|mniejsza od 0(zero)|str1 < str2|
|większa od 0(zero)|str1 > str2|

## Przykład

C/C++

#include <cstdio>  
#include <cstring>  
  
int main()  
{  
    char str1[] = "DOKUMENTACJA C++";  
    char str2[] = "Dokumentacja C++";  
     
    if( stricmp( str1, str2 ) == 0 )  
         printf( "Badane lancuchy znakow sa rowne.\n" );  
    else  
         printf( "Badane lancuchy znakow nie sa rowne.\n" );  
     
    return 0;  
}