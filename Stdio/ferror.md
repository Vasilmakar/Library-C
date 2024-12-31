## Zwracana wartość

Zwraca wartość 0 jeżeli flaga błędu strumienia nie jest ustawiona. Funkcja zwraca wartość różną od zera jeżeli wystąpił błąd w strumieniu.  

## Opis szczegółowy

Funkcja sprawdza czy wystąpił błąd w strumieniu przekazanym poprzez argument.  

## Dodatkowe informacje

Flaga błędu jest ustawiona, jeżeli wystąpił błąd podczas wykonywania operacji na strumieniu. Niektóre funkcje operujące na strumieniu czyszczą flagę błędu. Więcej informacji na temat czyszczenia flagi błędu znajdziesz pod hasłem » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [clearerr](https://cpp0x.pl/dokumentacja/?nro=345 "clearerr (funkcja)").  

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
    FILE * plik = fopen( "plik.txt", "r" );  
    if( plik != NULL )  
    {  
        fputc( 'q', plik );  
        if( ferror( plik ) != 0 )  
             printf( "Blad zapisu danych do pliku.\n" );  
         
        fclose( plik );  
    } else  
         perror( "Blad otwarcia pliku." );  
     
    return 0;  
}