## Opis szczegółowy

Funkcja isprint zwraca wartość różną od zera gdy argument, który został przekazany do funkcji jest » [Dokumentacja](https://cpp0x.pl/dokumentacja/) ♦ [znakiem drukowalnym](https://cpp0x.pl/dokumentacja/?nro=272 "znakiem drukowalnym (pojęcie)"). W przeciwnym wypadku funkcja zwraca wartość zero.

## Przykład

C/C++

char znak;  
scanf( "%c", & znak );  
if( isprint( znak ) )  
     printf( "Wprowadziles znak drukowalny i jest to: %c\n", znak );