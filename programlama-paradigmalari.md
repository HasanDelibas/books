Nedir Bu Programlama Paradigmaları
==================================

Bu dökümanı github üzerinden değiştirebilir, düzeltebilir, bu dökümana katkıda bulunabilirsin. https://github.com/HasanDelibas/books/blob/main/programlama-paradigmalari.md

Programlama dillerinin birbirdinden nasıl ayrıldı? Programlama dillerinin türleri nelerdir? Programlama dillerinin özellikleri-**paradigmaları** nelerdir?

Ön Bilgilendirme
----------------

**C-Like :** C’ye benzeyen diller: C, C++, C#, Java, JavaScript, PHP

![](https://miro.medium.com/max/1400/0*H65hJwN64nuALoP_)

Photo by [Clément Hélardot](https://unsplash.com/@clemhlrdt?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com?utm_source=medium&utm_medium=referral)

Imperative Programming ( Emirsel Programlama )
----------------------------------------------

İşlemcilerin mimarileri gereği her bir saat darbesinde (clock pulse) bir işlem yapar. Bu işlemler bu adresdeki veriyi getir, bu veriyi bu adrese yaz, bu sayıyı bu sayı ile topla gibi… Bu işlemci mimarisine uygun olduğu için programlama dillerinin çoğunluğunda bu paradigma uygulanmıştır. 1964 yılında çıkan BASIC dili bunun en güzel örneklerinden biridir. İngilizceyi referans alarak geliştirilmiş. Emirsel bir dildir. İngilizcede emir kipleri cümlenin başında gelir.

```
' BASIC
' Merhaba Dünya Yazdıran Kod
PRINT "Hello, World!"
```

️️✔️ C-Like Diller ( C, C++, C#, Java, JavaScript, PHP ) , Assembly, Python, BASIC,FORTRAN,COBOL

```
// JavaScript
// Verilen listedeki çift elemanları ekrana yazdıran program
const numList = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let result = 0;
for (let i = 0; i < numList.length; i++) {
  if (numList[i] % 2 === 0) {
    console.log( numList[i] )
  }
}
```

Görüldüğü gibi her komut tek tek emredilmiştir.

Declarative Programming (Bildirimsel Programlama)
-------------------------------------------------

Bu paradigmada ise, nasıl yapılacağından çok ne yapılacak bize onu bildirir. Emirsel programlamanın zıttıdır.

✔️ SQL

```
-- MySql
-- numList tablosundaki i sütünunundaki çift elemanları getir
SELECT i FROM numList WHERE mod(i,2) = 0
```

Non-structured Programming ( Yapısal Olmayan Programlama)
---------------------------------------------------------

Assembly programlama dili bu paradigmaya örnektir. İçerisinde hiç bir şekilde bloklar olmayan örneğin if yada for bloğu, sadece **GOTO** yada jump komutları ile satırlar arasında dolaşabilinen paradigma. İlk programlama dillerinde daha çok bu paradigma görülür.

✔️ Assembly, ilk sürüm BASIC, ilk sürüm FORTRAN, ilk sürüm COBOL

```
; Assembly
; ax by den büyükse X=1 değilse X=-1 'e ata.
cmp    ax, bx      
 jl     Big  
 mov    word [X], -1    
 jmp    Both            
Big: 
 mov    word [X], 1  
Both:
```

İlk sürüm BASIC dilinde döngüler

```
' BASIC
' ilk versiyon BASCI' de for olmadığı için döngüler 
' GOTO komutu ile yapılıyordu
Dim x as Integer = 1
back:
PRINT x
IF x < 10 THEN
    x = x + 1
    GOTO back
END IF
```

Görüldüğü üzere ne bi süslü parantez ne de satır aralığı blokları belirten hiçbir işaret yok. Spagetti kod dediğimiz okunaksız bir kod türüdür.

Structured programming ( Yapısal Programlama )
----------------------------------------------

Yapısal programlama dilleri, if, for, fonksiyon gibi komutları bloklar halinde yazılabilen paradigmadır. C-Like ( C, C++, C#, Java, JavaScript, PHP ) dillerde bu süslü parantezler **{ }** ile bloklara ayrılır. Python dilinde, Pug View Engine dilinde, eşit aralıklı boşluklar halinde bloklara ayrılır.

✔️ C, C++, C#, Java, JavaScript, PHP, sonraki sürüm BASIC, sonraki sürüm FORTRAN, sonraki sürüm COBOL

```
// C, C++, C#, Java, JavaScript
// ax by den büyükse X=1 değilse X=-1 'e ata.
if (ax > bx){
  X = 1;
}else{
  X = -1;
}
```

Python:

```
// Python
// ax by den büyükse X=1 değilse X=-1 'e ata.
if ax > bx:
  X = 1
else:
  X = -1
 ```

Functional Programming ( Prosedürel Programlama )
-------------------------------------------------

Bir programda tekrar eden komutları bir komutla yapmak için prosedürler kullanırız. Genellikle bu prosedürler bir değer döndürüyorsa buna fonksiyon deriz. Fonksiyonel programlama dillerinde verinin private erişilebilirlik yoktur tüm veriler publictir.

✔️ C, C++,️️ Python, PHP, JavaScript, FORTRAN, COBOL

```
// C, C++
// Kedi sesini ekrana yazdıran program
char *Kedi_Sesi(){
  char *sesi = "Miyav";
  return sesi;
}
int main(){
  print( Kedi_Sesi() );
}
```

Object Oriented Programming ( Nesneye Yönelik Programlama )
-----------------------------------------------------------

Prosedürel program gibi tekrar eden komutları **metodlar** ile kullanılan paradigmadır. Prosedürelden farklı olarak, buradaki ana unsur nesnedir. Nesneler üzerinden metodlar-rutinler çağırılır.

✔️ C++,️ ️C#, Python, PHP, JavaScript, Java

```
// JavaScript
// Kedi sesini ekrana yazdıran program
class Kedi{
  sesi(){
    return "Miyav"
  }
}
kedi = new Kedi()
console.log ( kedi.sesi() )
```

Imperative & Functional & Object Oriented
-----------------------------------------

Bu üç paradigmanın farkını daha anlaşılır bir şekilde şöyle gösterebiliriz.  
Genel kabul şu şekildedir. Burada kaynak olarak anlaşılır biçimde anlattığı için Ahmet Buğra Çakıcı’ nın videosunu gösterebilirim. [https://www.youtube.com/watch?v=uCf5hr1VJI8&t=1195s](https://www.youtube.com/watch?v=uCf5hr1VJI8&t=1195s)


```
// JavaScript
// Kedi sesini ekrana yazdıran program
// Imperative
console.log("Miyav")
// Functional
function sesVer(kedi){
  console.log(kedi.sesi)
}
sesVer({sesi:"Miyav"})
// Object Oriented
class Kedi{
  constructor(){
    this.sesi = "Miyav"
  }
  sesVer(){
    console.log(this.sesi)
  }
}
kedi = new Kedi()
kedi.sesVer()
```
