## Zwracana wartość

Zwraca wartość zero w przypadku sukcesu. W przeciwnym wypadku funkcja zwraca wartość różną od zera.  

## Opis szczegółowy

Funkcja ustawia pozycję kursora odczytu/zapisu danych dla wskazanego strumienia. Nową pozycję kursora określa drugi argument funkcji.  
  
Flaga osiągnięcia końca pliku jest czyszczona, jeżeli wywołanie tej funkcji zakończyło się sukcesem. W przypadku sukcesu funkcja ta odrzuca również wszelkie zmiany spowodowane wywołaniem funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [ungetc](https://cpp0x.pl/dokumentacja/?nro=508 "ungetc (funkcja)").  
  
Wartość przekazywana poprzez drugi argument powinna być wcześniej pobrana przy pomocy funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fgetpos](https://cpp0x.pl/dokumentacja/?nro=453 "fgetpos (funkcja)"). Więcej informacji na ten temat znajdziesz w dokumentach » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fgetpos](https://cpp0x.pl/dokumentacja/?nro=453 "fgetpos (funkcja)") oraz » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fpos_t](https://cpp0x.pl/dokumentacja/?nro=556 "fpos_t (alias)").  

## Dodatkowe informacje

Niniejsza funkcja w przypadku wystąpienia błędu ustawia dodatkowo kod błędu » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [errno](https://cpp0x.pl/dokumentacja/?nro=343 "errno (makro)"). Standard nie określa jednak ustawianej wartości, więc kod błędu należy weryfikować w dokumentacji zgodnej z posiadanym kompilatorem.  

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
    FILE * plik = fopen( "plik.txt", "w" );  
    if( plik )  
    {  
        fpos_t pozycja;  
        fgetpos( plik, & pozycja );  
        fputs( "To jest moj...", plik );  
        fsetpos( plik, & pozycja );  
        fputs( "On", plik );  
        fclose( plik );  
    }  
    return 0;  
}