## Zwracana wartość

Zwraca znak przekazany do funkcji poprzez argument character w przypadku sukcesu. Funkcja zwraca wartość » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [EOF](https://cpp0x.pl/dokumentacja/?nro=550 "EOF (makro)") w przypadku wystąpienia błędu.  

## Opis szczegółowy

Funkcja umożliwia określenie pierwszego znaku jaki ma zostać zwrócony przez następną operację odczytu danych ze strumienia. Znak umieszczony w strumieniu za pomocą niniejszej funkcji jest kasowany w chwili wywołania funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fflush](https://cpp0x.pl/dokumentacja/?nro=450 "fflush (funkcja)"), » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fseek](https://cpp0x.pl/dokumentacja/?nro=344 "fseek (funkcja)"), » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fsetpos](https://cpp0x.pl/dokumentacja/?nro=470 "fsetpos (funkcja)") lub » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [rewind](https://cpp0x.pl/dokumentacja/?nro=336 "rewind (funkcja)"). Wywołanie niniejszej funkcji nie modyfikuje danych strumienia, lecz jedynie zachowanie funkcji odczytujących dane. Funkcja musi być wywoływana na poprawnym i jednocześnie otwartym strumieniu danych.  

## Dodatkowe informacje

- Każde wywołanie niniejszej funkcji musi być poprzedzone poprawną operacją odczytu.
- Zachowanie funkcji jest niezdefiniowane w przypadku jej dwukrotnego wywołania pod rząd.
- Zachowanie funkcji jest niezdefiniowane w przypadku próby wykonania operacji na strumieniu na którym nie wykonano poprawnej operacji odczytu danych bezpośrednio przed wywołaniem niniejszej funkcji.
- Wywołanie funkcji nie modyfikuje danych strumienia - funkcja modyfikuje jedynie zachowanie funkcji odczytujących dane.

  

|   |
|---|
|**Uwaga!**  <br>Wywołanie niniejszej funkcji ma również niezdefiniowane zachowanie wtedy, gdy zostanie ona wywołana bezpośrednio po funkcjach, których wewnętrzna implementacja korzysta z funkcji **ungetc** (np. funkcja » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fscanf](https://cpp0x.pl/dokumentacja/?nro=506 "fscanf (funkcja)")).|

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
    FILE * pPlik = fopen( "plik.txt", "r" );  
    if( pPlik )  
    {  
        while( !feof( pPlik ) )  
        {  
            int znak = getc( pPlik );  
            if( znak == EOF )  
                 break;  
             
            //zamień odczytany znak na inny, jeżeli odczytanym znakiem jest '$'  
            if( znak == '$' )  
                 znak = '#';  
             
            //wstaw znak do bufora  
            printf( "Wstawiam znak '%c'\n", znak );  
            ungetc( znak, pPlik );  
             
            //odczytaj wiersz danych ze strumienia  
            char bufor[ 128 ];  
            if( fgets( bufor, 127, pPlik ) )  
                 printf( "Odczytano: \"%s\"\n", bufor );  
             
        } //while  
        fclose( pPlik );  
    } //if  
    return 0;  
}