#include <cstdio>  
#include <cstring>  
  
int main()  
{  
    char str[] = "Uklad krwionosny ssakow.";  
    printf( "Ostatni szukany znak znajduje sie na pozycji nr %d\n"  
    ,( strrchr( str, 's' ) - str + 1 ) );  
     
    return 0;  
}

Standardowe wyjście programu:  

Ostatni szukany znak znajduje sie na pozycji nr 19

## Zwracana wartość

Wskaźnik na ostatni znaleziony znak w łańcuchu _str1_, lub _NULL_ jeżeli znak nie został odnaleziony.