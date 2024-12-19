## Zwracana wartość

Zero jeżeli rejestracja funkcji się powiodła.  
Wartość różna od zera, gdy wystąpił błąd.  

## Przykład

C/C++

#include <cstdio>  
#include <cstdlib>  
  
void exit1( void )  
{  
    puts( "funkcja 1." );  
}  
  
void exit2( void )  
{  
    puts( "funkcja 2." );  
}  
  
int main()  
{  
    atexit( exit1 );  
    atexit( exit2 );  
    puts( "main." );  
    return 0;  
}

## Opis szczegółowy

Funkcja przekazana poprzez argument _function_ zostanie wywołana przed zakończeniem programu.  
  
Jeżeli ustawiono więcej niż jedną funkcję, będą one wywoływane w odwrotnej kolejności niż były one rejestrowane, czyli ostatnio ustawiona funkcja zostanie wywołana jako pierwsza.  
  
Jedna funkcja może zostać zarejestrowana więcej niż jeden raz.  
  
Implementacje C++ muszą umożliwiać rejertrację co najmniej 32 funkcji za pomocą funkcji atexit.