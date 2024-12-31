## Zwracana wartość

Zwraca liczbę bajtów zapisanych do strumienia w przypadku sukcesu. Funkcja zwraca wartość ujemną w przypadku wystąpienia błędu.  

## Opis szczegółowy

Funkcja zapisuje tekst sformatowany do wskazanego strumienia. Omawiana funkcja wymaga, aby liczba argumentów przekazanych do funkcji była nie mniejsza niż wynika to z treści tekstu sformatowanego. Przekazanie większej liczby argumentów niż jest to wymagane nie spowoduje żadnych skuktów ubocznych.  
  
Znaczenie argumentu format jest takie samo jak dla funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [printf](https://cpp0x.pl/dokumentacja/?nro=321 "printf (funkcja)").  
  

|   |
|---|
|**Uwaga!** Upewnij się, że tekst sformatowany nie może być wprowadzany przez użytkownika. Więcej szczegółów w dokumencie: » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [tekst sformatowany - printf](https://cpp0x.pl/dokumentacja/?nro=736 "tekst sformatowany - printf (specyfikacja)").|

## Dodatkowe informacje

Niniejsza funkcja w przypadku wystąpienia błędu ustawia dodatkowo kod błędu » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [errno](https://cpp0x.pl/dokumentacja/?nro=343 "errno (makro)"). Standard nie określa jednak ustawianej wartości, więc kod błędu należy weryfikować w dokumentacji zgodnej z posiadanym kompilatorem.  

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
    FILE * pStrumien = stdout;  
     
    fprintf( pStrumien, "Znaki: %c, %c\n", 'h', 68 );  
    fprintf( pStrumien, "Liczby (1): %d %i\n", 23, 45 );  
    fprintf( pStrumien, "Liczby (2): %5d %0*d\n", 1234, 8, 5678 );  
    fprintf( pStrumien, "Lancuchy znakow: %s, %s\n", "napis pierwszy", "napis drugi" );  
    fprintf( pStrumien, "Systemy liczbowe: %d %x %o %#x %#o \n", 250, 250, 250, 250, 250 );  
    fprintf( pStrumien, "Liczby zmiennoprzecinowe: %4.2f %+.0e %E \n", 2.1254, 2.1254, 2.1254 );  
    fprintf( pStrumien, "Liczba bez  zer wiadacych: %7d \n", 1387 );  
    fprintf( pStrumien, "Liczba z zerami wiadocymi: %07d \n", 1387 );  
    return 0;  
}  

#### Standardowe wyjście programu

Znaki: h, D  
Liczby (1): 23 45  
Liczby (2):  1234 00005678  
Lancuchy znakow: napis pierwszy, napis drugi  
Systemy liczbowe: 250 fa 372 0xfa 0372  
Liczby zmiennoprzecinowe: 2.13 +2e+000 2.125400E+000  
Liczba bez  zer wiadacych:    1387  
Liczba z zerami wiadocymi: 0001387