## Opis szczegółowy

Funkcja isgraph zwraca wartość różną od zera gdy argument, który został przekazany do funkcji jest » [Dokumentacja](https://cpp0x.pl/dokumentacja/) ♦ [znakiem graficznym](https://cpp0x.pl/dokumentacja/?nro=312 "znakiem graficznym (pojęcie)"). W przeciwnym wypadku funkcja zwraca wartość zero.

## Przykład

C/C++

char znak;  
scanf( "%c", & znak );  
if( isgraph( znak ) )  
     printf( "Wprowadziles znak graficzny i jest to: %c\n", znak );