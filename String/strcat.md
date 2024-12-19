## Przykład
C/C++

#include <cstdio>  
#include <cstring>  
  
int main()  
{  
    char str[ 64 ];  
    strcpy( str, "Te" );  
    strcat( str, " lancuchy" );  
    strcat( str, " zostaly" );  
    printf( "%s", strcat( str, " scalone.\n" ) );  
    return 0;  
}

## Co robi
Scala dwa łańcuchy znaków w jeden.