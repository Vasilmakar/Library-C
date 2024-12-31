## Opis szczegółowy

Funkcja przesuwa kursor odczytu/zapisu danych na początek wskazanego strumienia.  
  
Wywołanie niniejszej funkcji jest równoważne do wykonania funkcji

std::fseek( stream, 0, SEEK_SET );

 z tą różnicą, że w przypadku funkcji **rewind** flaga osiągnięcia końca pliku oraz flagi błędów są czyszczone.  
  
Funkcja ta odrzuca wszelkie zmiany spowodowane wywołaniem funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [ungetc](https://cpp0x.pl/dokumentacja/?nro=508 "ungetc (funkcja)").  

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
    FILE * strumien = fopen( "plik_dla_rewind.out", "w+" );  
    if( strumien != NULL )  
    {  
        int liczba1 = 13;  
        int liczba2 = - 273;  
        fprintf( strumien, "%d %d", liczba1, liczba2 );  
        printf( "Wartosci zapisane w pliku: %d i %d\n", liczba1, liczba2 );  
        rewind( strumien );  
        fscanf( strumien, "%d %d", & liczba1, & liczba2 );  
        printf( "Wartosci odczytane z pliku: %d i %d\n", liczba1, liczba2 );  
        fclose( strumien );  
    }  
    return 0;  
}

Standardowe wyjście programu:  

Wartosci zapisane w pliku: 13 i -273  
Wartosci odczytane z pliku: 13 i -273