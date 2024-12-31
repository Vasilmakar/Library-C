## Argumenty

|Argument|Opis|
|---|---|
|FILE* stream|Określa strumień na którym ma zostać wykonana operacja.|

## Opis szczegółowy

Czyści flagi błędów i status końca pliku (EOF) dla strumienia podanego poprzez argument funkcji.

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
     
    FILE * plik;  
    plik = fopen( "plik.txt", "r" );  
    if( !plik ) perror( "Blad podczas otwierania pliku" );  
    else  
    {  
        fputc( 'q', plik ); //próba zapisu do pliku  
        if( ferror( plik ) )  
        {  
            printf( "Blad podczas zapisu do pliku 'plik.txt'\n" );  
            clearerr( plik ); //usuwanie błędu  
        }  
        fgetc( plik );  
        if( !ferror( plik ) )  
             printf( "Brak bledow podczas odczytywania pliku 'plik.txt'\n" );  
         
    }  
    fclose( plik );  
    return 0;  
}