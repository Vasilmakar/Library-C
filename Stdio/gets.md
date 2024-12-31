## Zwracana wartość

Zwraca wskaźnik przekazany poprzez argument w przypadku sukcesu. Funkcja zwraca wartość NULL w przypadku napotkania błędu  lub w przypadku nie odczytania żadnego znaku z powodu osiągnięcia końca strumienia. W celu ustalenia rodzaju błędu jaki wystąpił należy użyć funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [ferror](https://cpp0x.pl/dokumentacja/?nro=449 "ferror (funkcja)") lub » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [feof](https://cpp0x.pl/dokumentacja/?nro=448 "feof (funkcja)").  

## Opis szczegółowy

Funkcja wczytuje tekst ze standardowego wejścia aż do napotkania znaku przejścia do nowej linii. Funkcja kończy operację wczytywania danych również wtedy, gdy w buforze danych strumienia wejścia nie pozostało więcej danych do odczytania. Wczytany wiersz jest zawsze zakończony znakiem terminalnym (\0). Znak przejścia do nowej linii nie jest zapisywany do bufora.  

## Dodatkowe informacje

Zamiast funkcji **gets** zaleca się używać funkcji » [standard C](https://cpp0x.pl/dokumentacja/?nro=1) ♦ [fgets](https://cpp0x.pl/dokumentacja/?nro=454 "fgets (funkcja)"), ponieważ umożliwia ona określenie maksymalnej liczby znaków, jaka może zostać wczytana do bufora.  
  

|   |
|---|
|**Uwaga!**  <br>Funkcja **gets** nie jest bezpieczna, ponieważ nie można ograniczyć liczby wczytywanych znaków ze standardowego wejścia. Jeżeli przekazany do funkcji bufor danych będzie zbyt mały to dane będą zapisywane przez funkcję poza oczekiwanym obszarem pamięci, a to w najlepszym przypadku skutkuje naruszeniem ochrony pamięci i przedwczesnym zakończeniem programu.|

## Przykład

C/C++

#include <cstdio>  
  
int main()  
{  
    char wiersz[ 100 ];  
    gets( wiersz );  
    printf( "Wczytany tekst: %s\n", wiersz );  
    return 0;  
}  

Przykładowe standardowe wyjście programu:  

Dokumentacja serwisu cpp0x.pl  
Wczytany tekst: Dokumentacja serwisu cpp0x.pl