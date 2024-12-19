## Przykład
#include <cstdio>  
#include <cstring>  
  
int main()  
{  
    char str1[] = "Dokumentacja C++";  
    char str2[] = "Dokumentacja C++";  
     
    if( strcmp( str1, str2 ) == 0 )  
         printf( "Badane lancuchy znakow sa rowne.\n" );  
    else  
         printf( "Badane lancuchy znakow nie sa rowne.\n" );  
     
    return 0;  
}
-------------------------------------------------------------
Porównuje dwa łańcuchy znaków