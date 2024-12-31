## Argumenty

|Argument|Opis|
|---|---|
|char* str|Bufor do którego zostaną zapisane odczytane znaki.|
|int num|Maksymalna liczba znaków jaka może zostać zapisana do bufora (włącznie ze znakiem terminalnym).|
|FILE* stream|Określa strumień na którym ma zostać wykonana operacja.|

## Zwracana wartość

Zwraca wskaźnik przekazany poprzez argument str w przypadku sukcesu. Funkcja zwraca wartość NULL w przypadku napotkania błędu lub w przypadku nie odczytania żadnego znaku z powodu osiągnięcia końca strumienia. W celu ustalenia rodzaju błędu jaki wystąpił należy użyć funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [ferror](https://cpp0x.pl/dokumentacja/?nro=449 "ferror (funkcja)") lub » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [feof](https://cpp0x.pl/dokumentacja/?nro=448 "feof (funkcja)").  

## Opis szczegółowy

Funkcja wczytuje tekst ze wskazanego strumienia aż do napotkania znaku przejścia do nowej linii lub do wczytania **num-1** znaków (w zależności od tego co nastąpi pierwsze). Funkcja kończy operację wczytywania danych również wtedy, gdy w buforze danych strumienia wejścia nie pozostało więcej danych do odczytania. Wczytany wiersz jest zawsze zakończony znakiem terminalnym (\0). Znak przejścia do nowej linii jest zapisywany do bufora, jeżeli wystąpił on we wczytanym w strumieniu danych.  

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
    char wiersz[ 18 ];  
    fgets( wiersz, 18, stdin );  
    printf( "Wczytany tekst: %s\n", wiersz );  
    return 0;  
}

Przykładowe standardowe wyjście programu:  

Dokumentacja serwisu cpp0x.pl  
Wczytany tekst: Dokumentacja serw