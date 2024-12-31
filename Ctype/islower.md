## Opis szczegółowy

Funkcja islower zwraca wartość różną od zera gdy argument, który został przekazany do funkcji jest małą literą alfabetu. W przeciwnym wypadku funkcja zwraca wartość zero.

## Przykład

C/C++

char znak;  
scanf( "%c", & znak );  
if( islower( znak ) )  
     printf( "Wprowadziles mala litere alfabetu i jest to: %c\n", znak );