## Opis szczegółowy

Funkcja isupper zwraca wartość różną od zera gdy argument, który został przekazany do funkcji jest dużą literą alfabetu. W przeciwnym wypadku funkcja zwraca wartość zero.

## Przykład

C/C++

char znak;  
scanf( "%c", & znak );  
if( isupper( znak ) )  
     printf( "Wprowadziles duza litere alfabetu i jest to: %c\n", znak );