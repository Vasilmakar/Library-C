## Opis szczegółowy

Funkcja isxdigit zwraca wartość różną od zera gdy argument, który został przekazany do funkcji jest cyfrą szesnastkową. W przeciwnym wypadku funkcja zwraca wartość zero.  
Cyfra szesnastkowa jest reprezentowana przez cyfry z zakresu od 0 do 9 oraz litery alfabetu z zakresu od A do F (lub ich małe odpowiedniki).

## Przykład

C/C++

char znak;  
scanf( "%c", & znak );  
printf( "isxdigit('%c') = %d;\n", znak, isxdigit( znak ) );