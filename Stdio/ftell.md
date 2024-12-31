## Zwracana wartość

Zwraca aktualną pozycję kursora odczytu/zapisu danych w przypadku sukcesu. Funkcja zwraca wartość **-1L** w przypadku wystąpienia błędu.  

## Opis szczegółowy

Funkcja zwraca aktualną pozycję kursora odczytu/zapisu danych dla wskazanego strumienia.  
  
Dla strumieni danych otwartych **w trybie binarnym**, pozycja kursora określa numer bajta na który wskazuje kursor, licząc od początku pliku.  
  
W przypadku **strumieni tekstowych**, pozycja kursora może nie odzwierciedlać fizycznej numeracji bajtów, ponieważ w strumieniach tekstowych znaki przejścia do nowej linii zazwyczaj podlegają transformacjom.  
  
Do przywrócenia pozycji kursora (otrzymanej przy pomocy funkcji **fteel**) należy użyć funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fseek](https://cpp0x.pl/dokumentacja/?nro=344 "fseek (funkcja)").  

## Dodatkowe informacje

Niektóre implementacje standardowych bibliotek C++ w przypadku wystąpienia błędu ustawiają dodatkowo kod błędu » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [errno](https://cpp0x.pl/dokumentacja/?nro=343 "errno (makro)"). Standard nie definiuje jednak tego zachowania, więc ewentualne ustawiane kody błędów należy weryfikować w dokumentacji zgodnej z posiadanym kompilatorem.  

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
    FILE * plik = fopen( "plik.txt", "rb" );  
    if( plik != NULL )  
    {  
        fseek( plik, 0, SEEK_END );  
        long odczytanaPozycja = ftell( plik );  
        fclose( plik );  
        printf( "Plik ma rozmiar: %ld bajtow.\n", odczytanaPozycja );  
    }  
    return 0;  
}