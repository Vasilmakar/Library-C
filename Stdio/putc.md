## Zwracana wartość

Zwraca znak przekazany poprzez argument **ch** w przypadku sukcesu. Funkcja zwraca wartość » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [EOF](https://cpp0x.pl/dokumentacja/?nro=550 "EOF (makro)") w przypadku wystąpienia błędu oraz ustawia flagę błędu.  

## Opis szczegółowy

Funkcja zapisuje znak do wskazanego strumienia.  

## Dodatkowe informacje

Funkcje » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fputc](https://cpp0x.pl/dokumentacja/?nro=557 "fputc (funkcja)") i putc są jednakowe za wyjątkiem tego, że funkcja putc w standardowej bibliotece może zostać zaimplementowana w postaci makra.  
  
Stan flagi błędu można odczytać za pomocą funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [ferror](https://cpp0x.pl/dokumentacja/?nro=449 "ferror (funkcja)").  

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
    for( char znak = 'a'; znak <= 'z'; ++znak )  
         putc( znak, stdout );  
     
    return 0;  
}  

Standardowe wyjście programu:  

abcdefghijklmnopqrstuvwxyz