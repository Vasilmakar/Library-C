>[!Note]
>Досить цікава функція, розділяє текст по символах, які представлені масивом. Функц3ція повертає вказівник на перший ланцюг знаків шо виступає перед знайденим символом. Тобто розділяє лаецюг на слова без вказаних символів і розділяється як tab в терміналі
## Przykład

C/C++

#include <cstring>  
#include <cstdio>  
int main()  
{  
    char str[] = "Rok 1525 - Hold Pruski, Krakow";  
    char korektor[] = " ,.-";  
    char * schowek;  
    printf( "Rozdziela tekst \"%s\" na poszczegolne wyrazy:\n", str );  
    schowek = strtok( str, korektor );  
    while( schowek != NULL )  
    {  
        printf( "%s\n", schowek );  
        schowek = strtok( NULL, korektor );  
    }  
    return 0;  
}

Standardowe wyjście programu:  

Rozdziela tekst "Rok 1525 - Hold Pruski, Krakow" na poszczegolne wyrazy:  
Rok  
1525  
Hold  
Pruski  
Krakow