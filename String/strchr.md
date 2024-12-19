На відміну від вказівника на байт, який повертає функція memchr , який може вказувати на будь-який тип даних , strchr я вказівником лише на знаки типу char
## Przykład
#include <cstdio>  
#include <cstring>  
  
int main()  
{  
    char sNapis[] = "Nasza dokumentacja C++";  
    for( char * p = strchr( sNapis, 'a' ); p != NULL; p = strchr( p + 1, 'a' ) )  
         printf( "Litera 'a' znajduje sie na pozycji: %d\n", p - sNapis );  
     
    return 0;  
}

## Zwracana wartość

Zwraca wskaźnik na znaleziony znak.