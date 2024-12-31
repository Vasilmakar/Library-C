## Opis szczegółowy

Funkcja umożliwia przypisanie bufora na dane do wskazanego strumienia. Strumień przekazany poprzez argument musi wskazywać na plik, który został poprawnie otwarty, a ponadto nie została na nim jeszcze wykonana żadna operacja odczytu i zapisu.  
  
Jeżeli argument bufor przyjmie wartość NULL, to strumień nie będzie buforowany. W przeciwnym wypadku rozmiar bufora musi być tablicą, której rozmiar jest nie mniejszy niż wartość zwracana przez makro » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [BUFSIZ](https://cpp0x.pl/dokumentacja/?nro=1718 "BUFSIZ (makro)").  

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
    FILE * pPlik = fopen( "MojPlik.txt", "w" );  
    if( pPlik )  
    {  
        char bufor[ BUFSIZ ];  
        setbuf( pPlik, bufor );  
        fputs( "Zawartosc zapisana do buforowanego strumienia.", pPlik );  
        fflush( pPlik );  
        fclose( pPlik );  
    } //if  
     
     
    pPlik = fopen( "MojPlik.txt", "a" );  
    if( pPlik )  
    {  
        setbuf( pPlik, NULL );  
        fputs( "Zawartosc zapisana do niebuforowanego strumienia.", pPlik );  
        fclose( pPlik );  
    } //if  
    return 0;  
}