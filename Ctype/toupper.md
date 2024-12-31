## Zwracana wartość

Zwraca kod ASCII dużej litery alfabetu gdy argument, który został przekazany do funkcji jest małą literą alfabetu. W przeciwnym wypadku funkcja zwraca wartość przekazaną poprzez argument.  

## Opis szczegółowy

Funkcja zwraca znak zamieniony z małej litery na dużą literę bądź zwraca znak, który został przekazany poprzez argument.  

## Przykład

C/C++

char znak;  
scanf( "%c", & znak );  
printf( "toupper('%c') = '%c';\n", znak, toupper( znak ) );