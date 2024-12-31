## Argumenty

|Argument|Opis|
|---|---|
|const char *string|Łańcuch znaków jakim ma zostać poprzedzony komunikat o błędzie. Jeżeli oczekiwany jest tylko komunikat błędu, argument powinien przyjmować wartość NULL.|

## Opis szczegółowy

Funkcja wypisuje komunikat o błędzie na standardowym strumieniu błędów (» [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [stderr](https://cpp0x.pl/dokumentacja/?nro=589 "stderr (makro)")). Komunikat błędu ustalany jest na podstawie wartości » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [errno](https://cpp0x.pl/dokumentacja/?nro=343 "errno (makro)").  
  
Wypisywany komunikat jest zawsze zakończony przejściem do nowego wiersza (**\n**). Jeżeli argument wejściowy jest różny od NULL to fraza zawierająca komunikat błędu będzie dodatkowo poprzedzona ciągiem znaków

": "

.  
  

|   |
|---|
|**Pamiętaj, że:**  <br>Funkcja perror powinna być wywoływana zaraz po funkcji, która wygenerowała błąd. W przeciwnym wypadku komunikat może zostać nadpisany wraz z wywołaniem innych funkcji.|

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
    perror( NULL );  
    FILE * pPlik = fopen( "nieistniejacy.plik", "rb" );  
    if( !pPlik )  
         perror( "Wystapil blad" );  
    else  
         fclose( pPlik );  
     
    return 0;  
}

#### Standardowe wyjście programu

No error  
Wystapil blad: No such file or directory