## Zwracana wartość

Funkcja zwróci wartość 0 jeżeli operacja została wykonana pomyślnie. W przeciwnym wypadku funkcja zwraca wartość różną od zera oraz ustawia odpowiedni numer błędu (patrz: » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [errno](https://cpp0x.pl/dokumentacja/?nro=343 "errno (makro)")).  

## Dodatkowe informacje

Pamiętaj, że argument newname nie może wskazywać na istniejący plik. Za pomocą tej funkcji możesz zmieniać nazwy katalogów i plików. Funkcja rename umożliwia również przenoszenie plików. Nie można jednak przy pomocy tej funkcji przenosić katalogów.  

## Przykład

C/C++

#include <cstdio>  
  
int main() {  
     
    if( rename( "oldname.txt", "newname.txt" ) == 0 )  
         printf( "zmiana nazwy powiodla sie" );  
    else  
         printf( "zmiana nazwy nie powiodla sie" );  
     
    return 0;  
}

Standardowe wyjście programu:  

zmiana nazwy nie powiodla sie