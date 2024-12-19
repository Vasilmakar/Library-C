## Przykład

C/C++

#include <cstdio>  
#include <cerrno>  
#include <cstring>  
  
int main()  
{  
    FILE * pPlik = fopen( "Dokumentacja na cpp0x.pl", "r" );  
    if( !pPlik )  
         printf( "Blad: %s\n", strerror( errno ) );  
    else  
         fclose( pPlik );  
     
    return 0;  
}

## Opis szczegółowy

Funkcja zwraca wskaźnik na statyczny łańcuch znaków, który zawiera komunikat błędu dla numeru błędu wskazanego poprzez argument num.