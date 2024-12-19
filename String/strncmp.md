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
    char str1[] = "abc";  
    char str2[] = "abcX";  
     
    if( strncmp( str1, str2, 3 ) == 0 )  
         printf( "Badane wycinki lancuchow znakow sa rowne.\n" );  
    else  
         printf( "Badane wycinki lancuchow znakow nie sa rowne.\n" );  
     
    return 0;  
}