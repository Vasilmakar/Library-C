void * memmmove( void * destination, const void * source, size_t num );

## Argumenty

|Argument|Opis|
|---|---|
|void* destination|Wskaźnik na pamięć, do której nastąpi kopiowanie.|
|const void* source|Wskaźnik na pamięć, z której nastąpi kopiowanie.|
|size_t num|Liczba bajtów do skopiowania.|

#include <iostream>
#include <cstring>

int main() {
    char str[] = "Hello, world!";
    
    // Копіюємо останні 5 символів на початок рядка
    memmove(str, str + 12, 5);

    std::cout << str << std::endl; // Виведе: world!Hello, 
    
    return 0;
}

## Zwracana wartość

Zwraca wskaźnik przekazany do funkcji poprzez argument destination.  

## Opis szczegółowy

Kopiuje num bajtów z miejsca wskazywanego przez source do pamięci wskazywanej przez destination.  
  
Bloki pamięci **mogą** na siebie zachodzić.  

## Dodatkowe informacje

Typ kopiowanych danych jest nieistotny, gdyż memmove kopiuje same bajty. Z tego powodu jej użycie do kopiowania obiektów typów niebędących POD nie jest zalecane, ponieważ zdefiniowane przez użytkownika konstruktory i operatory przypisania nie zostanę wywołane..

## Podobna do [[memcpy]]
