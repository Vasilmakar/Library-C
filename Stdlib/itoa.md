## Przykład

C/C++

#include <cstdio>  
#include <cstdlib>  
  
int main()  
{  
     
    char b[ 32 ];  
    printf( "Liczba to 1267\n" );  
    itoa( 1267, b, 16 );  
    printf( "szesnastkowo: %s\n", b );  
    printf( "binarnie:%s", itoa( 1267, b, 2 ) );  
    return 0;  
}

Standardowe wyjście programu:  

Liczba to 1267  
szesnastkowo: 4f3  
binarnie:10011110011