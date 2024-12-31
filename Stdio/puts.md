## Zwracana wartość

Zwraca wartość nieujemną w przypadku sukcesu. Funkcja zwraca wartość » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [EOF](https://cpp0x.pl/dokumentacja/?nro=550 "EOF (makro)") w przypadku wystąpienia błędu.  

## Opis szczegółowy

Funkcja zapisuje przekazany łańcuch znaków do standardowego strumienia wyjścia (» [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [stdout](https://cpp0x.pl/dokumentacja/?nro=332 "stdout (makro)")), a następnie zapisuje znak przejścia do nowej linii ('\n'). Łańcuch znaków musi być zakończony znakiem terminalnym '\0'. Znak terminalny nie jest zapisywany do strumienia.  

## Dodatkowe informacje

Pamiętaj, że funkcja puts dopisuje do strumienia znak przejścia do nowej linii ('\n') w przeciwieństwie do funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fputs](https://cpp0x.pl/dokumentacja/?nro=558 "fputs (funkcja)").  

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
    puts( "Dokumentacja serwisu" );  
    puts( "cpp0x.pl" );  
    return 0;  
}  

Standardowe wyjście programu:  

Dokumentacja serwisu  
cpp0x.pl