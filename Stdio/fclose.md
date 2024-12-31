## Zwracana wartość

Zwraca wartość zero w przypadku sukcesu. Funkcja zwraca wartość » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [EOF](https://cpp0x.pl/dokumentacja/?nro=550 "EOF (makro)") w przypadku wystąpienia błędu.  

## Opis szczegółowy

Zamyka strumień danych przekazany poprzez argument funkcji. Wszelkie bufory danych skojarzone z przekazanym strumieniem są czyszczone (przy pomocy funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fflush](https://cpp0x.pl/dokumentacja/?nro=450 "fflush (funkcja)")), a następnie zwalniane z pamięci.  

## Dodatkowe informacje

Strumień pracujący na pliku, przekazany poprzez argument staje się nieprawidłowy nawet jeżeli wywołanie funkcji zakończy się błędem.  

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
     
    FILE * plik = fopen( "Inwokacja.txt", "wt" );  
    if( plik )  
    {  
        fprintf( plik, "Przykładowy tekst do zapisu w pliku." );  
        fclose( plik );  
    }  
    return 0;  
}