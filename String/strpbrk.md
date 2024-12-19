> [!NOTE]
> на відміну від strcspn, який повертає відстань від початку ланцюга до першого знайденого символу, який входить до ланцюга 2, ця функція повертає саме вказівник на перший знайдений символ

 >[!Note]
 >Також при спробі вивести цей символ я отримую помилку і тільки при виведенні 
 >if(a!=NULL) {  
    while (*a != '\0') {  
        printf("%c", *a);  
        a++;  
    }
    я отримую ланцюг знаків які знаходяться після знайденого знаку і включно з ним
    
 
## Zwracana wartość

Wskaźnik na pierwszy znaleziony znak w łańcuchu _str1_, lub _NULL_ jeżeli żaden ze znaków nie został odnaleziony.  

## Przykład

C/C++

#include <cstdio>  
#include <cstring>  
  
int main()  
{  
    char str1[] = "Jakis tekst.";  
    char str2[] = "si.";  
    char * pZnak = strpbrk( str1, str2 );  
    printf( "Pierwszy znaleziony znak: %c\n", * pZnak );  
    printf( "Tekst od znalezionego znaku: \"%s\"\n", pZnak );  
    return 0;  
}