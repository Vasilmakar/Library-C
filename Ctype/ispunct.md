## Opis szczegółowy

Funkcja ispunct zwraca wartość różną od zera gdy argument, który został przekazany do funkcji jest » [Dokumentacja](https://cpp0x.pl/dokumentacja/) ♦ [znakiem drukowalnym](https://cpp0x.pl/dokumentacja/?nro=272 "znakiem drukowalnym (pojęcie)") ale nie jest » [Dokumentacja](https://cpp0x.pl/dokumentacja/) ♦ [znakiem alfanumerycznym](https://cpp0x.pl/dokumentacja/?nro=313 "znakiem alfanumerycznym (pojęcie)") ani spacją. W przeciwnym wypadku funkcja zwraca wartość zero.

## Przykład

C/C++

char znak;  
scanf( "%c", & znak );  
printf( "ispunct('%c') = %d\n", znak, znak );