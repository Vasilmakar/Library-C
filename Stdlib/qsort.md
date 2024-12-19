
## Przykład

C/C++

#include <cstdio>  
#include <cstdlib>  
#include <ctime>  
  
typedef int ElementT;  
  
int sortujRosnaco( const ElementT * arg1, const ElementT * arg2 );  
int sortujMalejaco( const ElementT * arg1, const ElementT * arg2 );  
void posortuj( ElementT * tablica, int ilosc, int( * funkcjaSortujaca )( const ElementT *, const ElementT * ) );  
void wyswietl( ElementT * tablica, int ilosc );  
  
int main()  
{  
    srand( time( 0 ) );  
    ElementT tablica[ 20 ];  
    for( int i = sizeof( tablica ) / sizeof( ElementT ) - 1; i >= 0; i-- )  
         tablica[ i ] = rand() % 9 + 1;  
     
    wyswietl( tablica, sizeof( tablica ) / sizeof( ElementT ) );  
    posortuj( tablica, sizeof( tablica ) / sizeof( ElementT ), sortujRosnaco );  
    wyswietl( tablica, sizeof( tablica ) / sizeof( ElementT ) );  
    posortuj( tablica, sizeof( tablica ) / sizeof( ElementT ), sortujMalejaco );  
    wyswietl( tablica, sizeof( tablica ) / sizeof( ElementT ) );  
    return 0;  
}  
  
int sortujRosnaco( const ElementT * arg1, const ElementT * arg2 )  
{  
    if( * arg1 <* arg2 )  
         return - 1;  
     
    if( * arg1 >* arg2 )  
         return 1;  
     
    return 0;  
}  
  
int sortujMalejaco( const ElementT * arg1, const ElementT * arg2 )  
{  
    if( * arg1 >* arg2 )  
         return - 1;  
     
    if( * arg1 <* arg2 )  
         return 1;  
     
    return 0;  
}  
  
void posortuj( ElementT * tablica, int ilosc, int( * funkcjaSortujaca )( const ElementT *, const ElementT * ) )  
{  
    qsort( tablica, ilosc, sizeof( * tablica ),( int( * )( const void *, const void * ) ) funkcjaSortujaca );  
}  
  
void wyswietl( ElementT * tablica, int ilosc )  
{  
    for( int i = 0; i < ilosc; i++ )  
         printf( "%d, ", tablica[ i ] );  
     
    printf( "\n" );  
}

## Argumenty

|Argument|Opis|
|---|---|
|const void *base|Wskaźnik na tablicę, która ma zostać posortowana.|
|size_t num|Liczba elementów w tablicy.|
|size_t width|Liczba bajtów zajmowanych przez jeden element tablicy.|
|int (*compare ) ( const void *, const void *)|Funkcja porównująca elementy tablicy. Do argumentów przedmiotowej funkcji trafiają wskaźniki na elementy obecnie porównywane.|