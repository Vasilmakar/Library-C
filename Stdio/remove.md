## Zwracana wartość

Funkcja zwróci wartość 0 jeżeli plik został usunięty pomyślnie. W przeciwnym wypadku funkcja zwraca wartość różną od zera oraz ustawia odpowiedni numer błędu (patrz: » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [errno](https://cpp0x.pl/dokumentacja/?nro=343 "errno (makro)")).  

## Dodatkowe informacje

Wszelkie uchwyty plików muszą być pozamykane zanim będzie możliwe usunięcie pliku.  

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
    if( remove( "plik.txt" ) == 0 )  
         printf( "Usunieto pomyslnie plik." );  
    else  
         printf( "Nie udalo sie skasowac pliku." );  
     
    return 0;  
}

Standardowe wyjście programu:  

Nie udalo sie skasowac pliku.