## Opis ogólny

Sprawdza czy znak przekazany jako argument jest literą alfabetu.

## Opis szczegółowy

Funkcja isalpha zwraca wartość różną od zera gdy argument, który został przekazany do funkcji jest literą alfabetu. W przeciwnym wypadku funkcja zwraca wartość zero.


## Przykład

C/C++

char znak;  
scanf( "%c", & znak );  
if( isalpha( znak ) )  
     printf( "Wprowadziles litere alfabetu i jest to: %c\n", znak );