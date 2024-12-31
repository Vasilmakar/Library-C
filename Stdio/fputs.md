## Zwracana wartość

Zwraca wartość nieujemną w przypadku sukcesu. Funkcja zwraca wartość » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [EOF](https://cpp0x.pl/dokumentacja/?nro=550 "EOF (makro)") w przypadku wystąpienia błędu.  

## Opis szczegółowy

Funkcja zapisuje przekazany łańcuch znaków do wskazanego strumienia. Łańcuch znaków musi być zakończony znakiem terminalnym '\0'. Znak terminalny nie jest zapisywany do strumienia.  

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
    fputs( "Dokumentacja serwisu\n", stdout );  
    fputs( "cpp0x.pl\n", stdout );  
    return 0;  
}  

Standardowe wyjście programu:  

Dokumentacja serwisu  
cpp0x.pl