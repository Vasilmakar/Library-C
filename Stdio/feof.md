## Zwracana wartość

Zwraca wartość różną od zera gdy został osiągnięty koniec pliku. W przeciwnym wypadku funkcja zwraca wartość zero.  

## Opis szczegółowy

Funkcja zwraca wartość różną od zera, jeżeli ostatnio wykonana operacja odczytu danych zostanie przerwana z powodu osiągnięcia końca strumienia danych. Zazwyczaj strumieniem danych jest plik, jednak może być to również » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [stdin](https://cpp0x.pl/dokumentacja/?nro=590 "stdin (makro)"), » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [stdout](https://cpp0x.pl/dokumentacja/?nro=332 "stdout (makro)") lub » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [stderr](https://cpp0x.pl/dokumentacja/?nro=589 "stderr (makro)").  

## Dodatkowe informacje

Flaga informująca o osiągnięciu końca pliku jest czyszczona, gdy jedna z następujących funkcji zostanie wywołana: » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [rewind](https://cpp0x.pl/dokumentacja/?nro=336 "rewind (funkcja)"), » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fsetpos](https://cpp0x.pl/dokumentacja/?nro=470 "fsetpos (funkcja)"), » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fseek](https://cpp0x.pl/dokumentacja/?nro=344 "fseek (funkcja)") lub » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [clearerr](https://cpp0x.pl/dokumentacja/?nro=345 "clearerr (funkcja)").  

## Przykład

### Plik źródłowy

C/C++

#include <cstdio>  
  
int main()  
{  
    FILE * pPlik = fopen( "plik.txt", "rb" );  
    if( !pPlik )  
         return 0;  
     
    while( !feof( pPlik ) )  
    {  
        const int iRozmiarBufora = 3;  
        char bufor[ iRozmiarBufora ];  
        int iOdczytanoBajtow = fread( bufor, sizeof( char ), iRozmiarBufora, pPlik );  
        printf( "Odczytano %d bajtow.\n", iOdczytanoBajtow );  
    } //while  
    fclose( pPlik );  
    return 0;  
}