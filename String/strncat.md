Zapis

strncat( napis, "abc", 1 );

 zwiększy długość łańcucha _napis_ o jeden (zostanie dopisana litera 'a').  

## Przykład

C/C++

#include <cstdio>  
#include <cstring>  
  
int main()  
{  
    char str1[ 32 ] = "Jam jest ";  
    char str2[] = "C++.";  
     
    printf( "%s\n", strncat( str1, str2, 20 ) );  
    return 0;  
}