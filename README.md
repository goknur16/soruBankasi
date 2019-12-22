# soruBankasi
soru bankası c 
/* soruların alınacağı site: https://www.indiabix.com/c-programming/questions-and-answers/

 4 şıklı 40 soru seçilecek

 Kullanıcı tarafından girilen sayıda soru içeren bir sınav hazırlanacak.

 Hazırlanan sınav hemen kullanıcıya sunulacak. Aşağıda örnek bir kod size verilmiştir.

 Örnek:

 Soru sayısını giriniz:2



 1. Hangisi değişken isimlerinde kullanılır?

 a) *

 b) /

 c) |

 d) _

 Cevabı giriniz:d

 Sonuç: Doğru (100/soru sayısı)



*/
#include <stdio.h>
#include <stdio.h>
#include <stdlib.h>
#include <time.h>



struct SoruBank {

    int sno;

    char soru[600];

    char cevap[400];

    char A[100];

    char B[100];

    char C[100];

    char D[100];

};


int main(void) {
    
    

    struct SoruBank sorular[40] = {

     { 1,"Kontrolü bir fonksiyondan geri arama fonksiyonuna aktarmak için kullanılan anahtar kelime?       \nA.switch  \nB.goto   \nC.go back  \nD.return","D"
     },

    
    

     { 3,"Aşağıdaki program tarafından ayrılan belleği nasıl boşaltırsınız?#include<stdio.h> #include<stdlib.h> #define MAXROW 3 #define MAXCOL 4   int main(){int **p, i, j;p = (int **) malloc(MAXROW * sizeof  \nA.memfree(int p);  \nB.dealloc(p);  \nC.malloc(p, 0);    \nD.free(p);","D"
     },


     { 4,"\n Ekrana yazdırmak için aşağıdakilerden hangisini kullanırsınız?                                           \nA.printf('\n'); \nB.echo '\\n'; \nC.printf('\n');  \nD.printf('\\n');","D"
     },

     { 5,"İki dize aynıysa, strcmp () işlevi döner.             \nA.-1 \nB.1 \nC.0 \nD.Yes","C"
     },

     { 6,"Çok işlevli bir string okumak için aşağıdaki işlevlerden hangisi daha uygundur?                                  \nA.printf(); \nB.scanf(); \nC.gets(); \nD.puts();","C"
     },

     { 7,"C'de, bir diziyi bir fonksiyona argüman olarak iletirseniz, gerçekte ne geçilir?                          \nA.Dizinin temel adresi    \nB.Dizinin ilk elemanı         \nC.Dizideki öğelerin değeri   \nD.Dizinin son elemanının adresi","A"
     },

     {8,"Yandaki kod ne anlama gelmektedir? int (*ptr)[10];        \nA.ptr, 10 tam sayıya işaretçiler dizisidir.                 \nB.ptr, 10 tam sayı dizisine işaretçidir.                  \nC.ptr, 10 tam sayı dizisidir.                               \nD.ptr diziyi gösteren bir işaretçidir.","B"
     },

     { 9,"Bir C programında, alt dizinin boyutunu aşan bir dizi öğesine bir değer atarsanız ne olur?                     \nA.Öğe 0 olarak ayarlanacaktır.                              \nB.Derleyici bir hata bildirir.                              \nC.Bazı önemli verilerin üzerine yazıldığında program çökebilir.  \nD.Dizi büyüklüğü uygun şekilde büyür","C"},

     { 10,"Ayrılan belleği nasıl boşaltırsınız?              \nA.remove(var-name); \nB.free(var-name);\nC.delete(var-name);\nD.dalloc(var-name);","B"
     },

     {11,"Yapı(structure), birlik(union) ve numaralandırma(enumeration) arasındaki benzerlik nedir?               \nA.Hepsi yeni değerler tanımlamanıza izin verir.             \nB.Hepsi yeni veri türlerini tanımlamanıza izin verir.       \nC.Hepsi yeni işaretçiler tanımlamanıza izin veriyor.        \nD.Hepsi yeni yapıları tanımlamanıza izin veriyor.","B"},

     { 12,"Aşağıdaki aşamada hangi kod #include <stdio.h> stdio.h dosyasının içeriğiyle değiştirilir?                       \nA.Düzenleme sırasında   \nB.Bağlama sırasında               \nC.Yürütme sırasında   \nD.Ön işleme sırasında","D"},

     { 13,"C'deki farklı gerçek veri türleri nelerdir?           \nA.float, double    \nB.short int, double, long int          \nC.float, double, long double  \nD.double, long int, float","C"},

     { 14,"3.14 sabitini uzun bir çift olarak ele almak için ne yapacaksınız?                                           \nA.use 3.14LD \nB.use 3.14Lb \nC.use 3.14DL \nD.use 3.14LF","B"},

     {15,"X, float değerinde x'i int değerine yuvarlamak istiyoruz, doğru yolu nasıl yaparız?                                \nA.y = (int)(x + 0.5)    \nB.y = int(x + 0.5)                \nC.y = (int)x + 0.5   \nD.y = (int)((int)x + 0.5)","A"},

     {16,"5.375'in ikili eşdeğeri aşağıdakilerden hangisidir?\nA.101.101110111 \nB.101.011 \nC.101011 \nD.None of above","B"},

     {17,"Bir kayan nokta 4 bayt kaplar.Bu 4 baytın onaltılık eşdeğeri A, B, C ve D ise,bu kayan nokta bellekte saklandığında bu sıralar hangi sırayla saklanır?             \nA. ABCD  \nB. DCBA  \nC.0xABCD                      \nD.Büyük endian veya küçük endian mimarisine bağlı","D"},

     {18,"3.14 sabitini bir float olarak değerlendirmek için ne yapacaksınız?                                            \nA.use float(3.14f) \nB.use 3.14f \nC.use f(3.14)           \nD.use (f)(3.14)","B"},

     {19,"Aşağıdaki ifadelerden hangisi kalanını 5,5'e 1,3'e bölmekle alır?                                               \nA.rem = (5.5 % 1.3)    \nB.rem = modf(5.5, 1.3)            \nC.rem = fmod(5.5, 1.3)  \nD.Error: bölemeyiz","C"},

     {20,"Stderr nedir?                                        \nA.standart hata  \nB.standart hata tipleri                  \nC)standart hata akışları   \nD.standart hata tanımları","C"
     },

     {21,"C'deki bir dizgede bir karakterin son oluşumunu bulmak için hangi standart kütüphane işlevini kullanırız?     \nA.strnchar() \nB.strchar() \nC)strrchar() \nD.strrchr()","C"},

     {22,"Input/output işlevi prototipleri ve makroları hangi başlık dosyasında tanımlanır?                         \nA.conio.h \nB.stdlib.h \nC.stdio.h \nD.dos.h","C"},

     {23,"rewind() fonksiyonu ne yapar?                     \nA.Dosya işaretçisini bir karakter tersine yeniden konumlandırır. \nB.Dosya işaretçisi akışını dosyanın sonuna kadar yeniden konumlandırır. \nC.Dosya işaretçisini o satırın başına getirir. \nD.Dosyanın başlangıcını dosya göstericisine yerleştirir.","D"},

     {24,"random () fonksiyonu DOS altında Turbo C’de ne yapar \nA.rastgele bir sayı döndürür.  \nB.belirtilen aralıkta rasgele sayı üreteci döndürür.    C.zamana göre rastgele bir değere sahip bir rasgele sayı üreteci döndürür. \nD.belirli bir tohum değeri olan rasgele bir sayı döndür.","C"},

     {25,"Hangisi değişken isimlerinde kullanılır?               \nA. *  \nB. /  \nC. |  \nD._","D"},

     {26,"fflush() fonksiyonunun amacı nedir?                \nA.tüm akışları ve belirtilen akışları temizler.             \nB.sadece belirtilen akışı temizler.                         \nC.giriş / çıkış tamponunu temizler.                         \nD.dosya arabelleğini temizler.","A"},

     {27,"Aşağıdaki kodda, P2 Tamsayı işaretçisi mi? yoksa tamsayı mı? typedef int *ptr; ptr p1, p2;                     \nA.Tamsayı \nB.Tamsayı işaretçisi \nC.Beyanda hata \nD.Yukarıdakilerin hiçbiri","B"},

     {28,"Aşağıdaki kodda 'P' nedir?                             \nA.P bir sabittir. \nB.P bir karakter sabitidir.         \nC.P karakter türüdür. \nD.Yukarıdakilerin hiçbiri.","A"},

     {29,"Yandaki kod parçası ne anlama geliyor? int (*pf)();    \nA.pf işlevi için bir işaretçidir.                           \nB.pf bir fonksiyon işaretçisidir.                          \nC.pf int döndüren bir işlevin bir göstergesidir.            \nD.pf işaretçi değişkeninin bir işlevidir.","C"},

     {30,"Yandaki kod parçası ne anlama geliyor? char *arr[10];\nA.arr, 10 karakterlik bir göstericidir.                    \nB.arr, fonksiyon göstergesinin bir dizisidir.               \nC.arr, bir karakter dizisidir.                              \nD.arr, karakter dizisine işaretçidir.","A"},

     {31,"Yandaki ifade ne bildirir? 'Üç karakter dizisine işaretçi'.                                                \nA.char *ptr[3](); \nB.char (*ptr)*[3]; \nC.char (*ptr[3])();\nD.char (*ptr)[3];","D"},

     {32,"Yandaki kod parçası ne anlama geliyor? int *ptr[30];\nA.ptr, 30 tam sayı işaretçisi dizisine bir göstericidir.   \nB.ptr, tamsayılara yönelik 30 işaretçi dizisidir.       \nC.ptr, 30 tam sayı işaretçisi dizisidir.                 \nD.ptr, bir 30 işaretçi dizisidir.","B"},

     {33,"Yandaki ifade ne bildirir? 'Karakterler üç işaretçiler dizisi'                                                 \nA.char *ptr[3]() \nB)char *ptr[3]; \nC.char (*ptr[3])(); \nD.char **ptr[3];","B"},

     {34,"Yandaki kod parçası ne anlama geliyor? void (*cmp)();\nA.cmp, geçersiz bir işlev türü için bir işaretçidir.        \nB.cmp geçersiz tipte bir işaretçi işlevidir.          \nC.cmp, geçersiz bir işaretçiyi döndüren bir işlevdir.       \nD.cmp, boşluğu döndüren bir işleve işaretçidir.","D"},

     {35,"Yandaki kod parçası ne anlama geliyor?  int *f();      \nA.f, işlev türünün işaretçi değişkenidir.                   \nB.f, int işaretine dönen bir işlevdir.                      \nC.f bir fonksiyon işaretçisidir.                            \nD.f, işaretçi değişkeninin basit bir bildirimidir.","B"},

     {36,"Yandaki ifade ne bildirir? 'Hiçbir şey almayan ve hiçbir şey döndürmeyen bir fonksiyon işaretçi'                 \nA.void *(ptr)*int; \nB.void *(*ptr)() \nC.void *(*ptr)(*) \nD.void (*ptr)()","D"},

     {37,"Yandaki ifade ne bildirir?  'Bir int işaretçisi alan ve float işaretçisini döndüren bir fonksiyon işaretçi'     \nA.float *(ptr)*int; \nB.float *(*ptr)(int)             \nC.float *(*ptr)(int*)  \nD.float (*ptr)(int)","C"},

     {38,"Yandaki kod parçası ne anlama geliyor? char **argv;\nA.argv, işaretçiye işaretçidir.                             \nB.argv, bir char işaretçisine bir işaretçisidir.            \nC.argv bir fonksiyon işaretçisidir.                         \nD.argv, işlev göstergesinin bir üyesidir.","B"},

     {39,"Yandaki kod parçası ne anlama geliyor?  char *scr;     \nA. scr, pointer değişkeninin bir göstericidir.              \nB. scr, bir fonksiyon işaretçisidir.                        \nC. scr, char için bir göstericidir.                         \nD. scr, fonksiyon göstergesinin bir üyesidir.","C"},

     {40,"Dinamik olarak bellek ayırmak için aşağıdaki 2 kütüphane işlevini belirtin.                                     \nA.malloc() and memalloc()                                   \nB.alloc() and memalloc()                                   \nC.malloc() and calloc()                                     \nD.memalloc() and faralloc()","C"}
    };

    time_t t;



    srand((unsigned)time(&t));
    char kullanici_cevabi;
    int dogrular = 0;
    int soru_sayisi;
    double puan;
    
    int indis = rand() % 40 + 1;

    printf("Kaç soru çözmek istersiniz?:");
    scanf("%d", &soru_sayisi);


    for (int i = 0; i < soru_sayisi; i++) {
        indis = rand() % 40 + 1;
        printf("\nSizin için seçilen soru:%d\n%s\n", sorular[indis].sno, sorular[indis].soru);

        printf("\nCevabınız: ");
        scanf("%s", &kullanici_cevabi);
        

        if (*sorular[indis].cevap == kullanici_cevabi) {
            printf("Girdiğiniz cevap doğru :)\n");
            dogrular++;
        }
        else{
            printf("Girdiğiniz cevap yanlış :(\n");
            printf("Sorunun doğru cevabı:%c\n", *sorular[indis].cevap);
        }
    }
    puan = dogrular * (100 / soru_sayisi);
    printf("\nToplam puanınız:%f\n", puan);
    
    getchar();
    return -1;
    
}
