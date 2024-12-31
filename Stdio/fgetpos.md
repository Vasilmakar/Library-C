## Argumenty

|Argument|Opis|
|---|---|
|FILE *stream|Określa strumień na którym ma zostać wykonana operacja.|
|fpos_t *pos|Wskaźnik na zmienną do której ma zostać pobrana aktualna pozycja kursora odczytu/zapisu danych.|

## Zwracana wartość

Zwraca wartość zero w przypadku sukcesu. W przeciwnym wypadku funkcja zwraca wartość różną od zera.  

## Opis szczegółowy

Funkcja pobiera aktualną pozycję kursora odczytu/zapisu danych dla wskazanego strumienia. Pobrana pozycja jest zapisywana do zmiennej na którą wskazuje wskaźnik przekazany poprzez drugi argument.  
  
Pobranej pozycji nie należy interpretować w żaden sposób, ponieważ definicja typu » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fpos_t](https://cpp0x.pl/dokumentacja/?nro=556 "fpos_t (alias)") jest zależna od posiadanej implementacji biblioteki. Odczytaną pozycję (przy pomocy funkcji **fgetpos**) należy wykorzystywać tylko i wyłącznie do poprawnego wywołania funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fsetpos](https://cpp0x.pl/dokumentacja/?nro=470 "fsetpos (funkcja)").  

## Dodatkowe informacje

Niektóre implementacje standardowych bibliotek C++ w przypadku wystąpienia błędu ustawiają dodatkowo kod błędu » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [errno](https://cpp0x.pl/dokumentacja/?nro=343 "errno (makro)"). Standard nie definiuje jednak tego zachowania, więc ewentualne ustawiane kody błędów należy weryfikować w dokumentacji zgodnej z posiadanym kompilatorem.  

## Przykład

C/C++

#include <cstdio>  
  
void wypiszAktualnaPozycje( FILE * _pPlik )  
{  
    fpos_t pozycja;  
    if( fgetpos( _pPlik, & pozycja ) != 0 )  
         perror( "Nie udalo sie odczytac pozycji.\n" );  
    else  
         printf( "Aktualna pozycja: %d\n", pozycja );  
     
}  
  
int main()  
{  
    FILE * plik = fopen( "plik.txt", "r" );  
    if( plik )  
    {  
        wypiszAktualnaPozycje( plik );  
        char bufor[ 200 ];  
        fgets( bufor, 200, plik );  
        wypiszAktualnaPozycje( plik );  
         
        fclose( plik );  
    }  
    return 0;  
}