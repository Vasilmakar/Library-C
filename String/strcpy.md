## Przykład

C/C++

#include <cstdio>  
#include <cstring>  
  
int main()  
{  
    char zrodlo[] = "Dokumentacja silnika krokowego.\n";  
    char przeznaczenie[ 40 ];  
     
    strcpy( przeznaczenie, zrodlo );  
     
    printf( "przeznaczenie: %s", przeznaczenie );  
    return 0;  
}