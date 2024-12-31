## Zwracana wartość

Zwraca kod ASCII małej litery alfabetu gdy argument, który został przekazany do funkcji jest dużą literą alfabetu. W przeciwnym wypadku funkcja zwraca wartość przekazaną poprzez argument.  

## Opis szczegółowy

Funkcja zwraca znak zamieniony z dużej litery na małą literę bądź zwraca znak, który został przekazany poprzez argument.  

## Przykład

C/C++

char znak;  
scanf( "%c", & znak );  
printf( "tolower('%c') = '%c';\n", znak, tolower( znak ) );