## Zwracana wartość

Zwraca znak przekazany poprzez argument **ch** w przypadku sukcesu. Funkcja zwraca wartość » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [EOF](https://cpp0x.pl/dokumentacja/?nro=550 "EOF (makro)") w przypadku wystąpienia błędu oraz ustawia flagę błędu.  

## Opis szczegółowy

Funkcja zapisuje znak do standardowego strumienia wyjścia (» [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [stdout](https://cpp0x.pl/dokumentacja/?nro=332 "stdout (makro)")).  

## Dodatkowe informacje

Stan flagi błędu można odczytać za pomocą funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [ferror](https://cpp0x.pl/dokumentacja/?nro=449 "ferror (funkcja)").  

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
    for( char znak = 'a'; znak <= 'z'; ++znak )  
         putchar( znak );  
     
    return 0;  
}  

Standardowe wyjście programu:  

abcdefghijklmnopqrstuvwxyz