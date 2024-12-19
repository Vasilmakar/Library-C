>[!Note]
>Така сама як div(), тільки працює з числами long int, тоді як div() - з int.

## Przykład

C/C++

#include <cstdlib>  
#include <cstdio>  
  
int main()  
{  
    int a = 17;  
    int b = 6;  
    ldiv_t wynik = ldiv( a, b );  
    printf( "wynik = ldiv(%d,%d)\n", a, b );  
    printf( "Iloraz liczb wynosi: %d. Reszta z dzielenia wynosi: %d\n", wynik.quot, wynik.rem );  
     
    return 0;  
}