## Opis szczegółowy

Funkcja iscntrl zwraca wartość różną od zera gdy argument, który został przekazany do funkcji jest znakiem kontrolnym. W przeciwnym wypadku funkcja zwraca wartość zero.  
Znaki kontrolne: od **0x00** do **0x1F** oraz **0x7F**.

## Przykład

C/C++

char znak;  
scanf( "%c", & znak );  
if( iscntrl( znak ) )  
     printf( "Wprowadziles znak kontrolny i jest to: %c\n", znak );