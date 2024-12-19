>[!Note]
>Ця функція повертає структуру типу div_t і приймає два аргументи: частку від ділення і решту(wynik.quot, wynik.rem) 

## Przykład

C/C++

#include <cstdlib>  
#include <cstdio>  
  
int main()  
{  
    int a = 17;  
    int b = 6;  
    div_t wynik = div( a, b );  
    printf( "wynik = div(%d,%d)\n", a, b );  
    printf( "Iloraz liczb wynosi: %d. Reszta z dzielenia wynosi: %d\n", wynik.quot, wynik.rem );  
     
    return 0;  
}

Standardowe wyjście programu:  

wynik = div(17,6)  
Iloraz liczb wynosi: 2. Reszta z dzielenia wynosi: 5