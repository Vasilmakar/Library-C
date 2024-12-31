## Zwracana wartość

Zwraca kod odczytanego znaku w przypadku sukcesu. Funkcja zwraca wartość » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [EOF](https://cpp0x.pl/dokumentacja/?nro=550 "EOF (makro)") w przypadku napotkania błędu lub w przypadku osiągnięcia końca strumienia. W celu ustalenia rodzaju błędu jaki wystąpił należy użyć funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [ferror](https://cpp0x.pl/dokumentacja/?nro=449 "ferror (funkcja)") lub » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [feof](https://cpp0x.pl/dokumentacja/?nro=448 "feof (funkcja)").  

## Opis szczegółowy

Funkcja odczytuje jeden znak ze standardowego wejścia. Odczytany znak jest zwracany w postaci liczby typu int.  

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
    int kodASCII = getchar();  
    printf( "%c", kodASCII );  
    return 0;  
}