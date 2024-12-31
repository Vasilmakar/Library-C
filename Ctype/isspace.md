## Opis szczegółowy

Funkcja isspace zwraca wartość różną od zera gdy argument, który został przekazany do funkcji jest » [Dokumentacja](https://cpp0x.pl/dokumentacja/) ♦ [białym znakiem](https://cpp0x.pl/dokumentacja/?nro=274 "białym znakiem (pojęcie)"). W przeciwnym wypadku funkcja zwraca wartość zero.

## Argumenty

|nazwa argumentu|opis|
|---|---|
|ch|Kod znaku ASCII|

## Wykaz białych znaków

|kod ASCII (hex)|opis|zapis formalny|
|---|---|---|
|0x09|tabulacja pozioma|'\t'|
|0x0A|przejście karetki do nowego wiersza|'\n'|
|0x0B|tabulacja pionowa|'\v'|
|0x0C|przesuwa karetkę na początek nowej strony|'\f'|
|0x0D|powrót karetki na początek wiersza|'\r'|
|0x20|spacja|' '|

## Przykład 1

C/C++

char znak;  
scanf( "%c", & znak );  
if( isspace( znak ) )  
     printf( "Wprowadziles bialy znak. Kod ASCII znaku to: %d\n", znak );

## Przykład 2

C/C++

#include <cstdio>  
  
int main( void )  
{  
    printf( "tabulacja pozioma = %d\n", '\t' );  
    printf( "nowy wiersz = %d\n", '\n' );  
    printf( "nowa strona = %d\n", '\v' );  
    printf( "tabulacja pionowa = %d\n", '\f' );  
    printf( "powrot karetki = %d\n", '\r' );  
    printf( "spacja %d\n", ' ' );  
    return 0;  
}