## Przykład

C/C++

#include <cstdio>  
#include <cstring>  
  
int main()  
{  
    char str1[] = "1410 : bitwa pod Grunwaldem.";  
    char str2[] = "bitwa ";  
    char * wynik = strstr( str1, str2 );  
    printf( "Znaleziono lancuch: %s\n", wynik );  
     
    return 0;  
}