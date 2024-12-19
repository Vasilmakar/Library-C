## Opis szczegółowy

Zwraca łańcuch znaków zawierający wartość zmiennej środowiskowej o nazwie podanej jako argument

varname

.  
Łańcuch zwrócony przez funkcje nie powinien być modyfikowany przez aplikację.  
Ten sam obszar pamięci może być użyty przy następnym wywołaniu funkcji

getenv()

 nadpisując poprzedni wynik.  
W zależności od platformy, ta funkcja może zwracać uwagę na wielkość liter.  

## Przykład

C/C++

#include <stdio.h>  
#include <stdlib.h>  
  
int main()  
{  
    char * pPath;  
    pPath = getenv( "PATH" );  
    if( pPath != NULL )  
         printf( "The current path is: %s", pPath );  
     
    return 0;  
}