## Przykład

C/C++

#include <string>  
#include <cstdio>  
#include <cstdlib>  
  
class CKoniec  
{  
protected:  
    std::string m_sText;  
public:  
    CKoniec( const char * sText );  
    ~CKoniec();  
}; //class CKoniec  
  
CKoniec klasa( "Koniec globalny" );  
int main()  
{  
    printf( "Start\n" );  
    CKoniec klasa( "Koniec lokalny" );  
    exit( 123 );  
    printf( "Koniec main'a\n" );  
    return 0;  
}  
  
CKoniec::CKoniec( const char * sText )  
    : m_sText( sText )  
{  
}  
  
CKoniec::~CKoniec()  
{  
    printf( "%s\n", m_sText.c_str() );  
}  

Standardowe wyjście programu:  

Start  
Koniec globalny