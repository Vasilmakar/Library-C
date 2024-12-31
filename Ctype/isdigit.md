## Opis szczegółowy

Funkcja isdigit zwraca wartość różną od zera gdy argument, który został przekazany do funkcji jest cyfrą. W przeciwnym wypadku funkcja zwraca wartość zero.

## Przykład

C/C++

char znak;  
scanf( "%c", & znak );  
if( isdigit( znak ) )  
     printf( "Wprowadziles cyfre i jest to: %c\n", znak );