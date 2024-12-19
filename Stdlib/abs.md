## Przykład

C/C++

#include <cstdio>  
#include <cstdlib>  
#include <cmath>  
  
int main()  
{  
    printf( "Wartosc bezwzgledna liczby %d to %d\n", - 254, abs( - 254 ) );  
    printf( "Wartosc bezwzgledna liczby %f to %f\n", - 254.3, abs( - 254.3 ) );  
    return 0;  
}

## Zwracana wartość

Wartość bezwzględna liczby n.

## Dodatkowe informacje

**Uwaga!** Funkcja _abs_ dla liczb zmiennoprzecinkowych działa tylko i wyłącznie pod Visual C++. Rekomendowane jest stosowanie » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fabs](https://cpp0x.pl/dokumentacja/?nro=383 "fabs (funkcja)") dla liczb zmiennoprzecinkowych w celu zachowania przenośności kodu źródłowego.