## Przykład
#include <stdio.h>
#include <string.h> 
int main() {
int src[] = {1, 2, 3, 4, 5}; 
int dest[5]; 
memcpy(dest, src, sizeof(src));
for (int i = 0; i < 5; i++) { 
printf("%d ", dest[i]); 
} 
printf("\n"); 
return 0;
}

## Opis szczegółowy

Porównuje pierwsze _num_ bajtów bloku wskazywanego przez _ptr1_ i pierwsze _num_ bajtów bloku nt wskazywanego przez _ptr2_.

## Zwracana wartość

Zero, jeśli zawartość bloków pamięci jest taka sama; wartość dodatnia, jeśli pierwszy bajt nie będący taki sam w obu blokach był większy w _ptr1_; wartość ujemna w przeciwnym wypadku.