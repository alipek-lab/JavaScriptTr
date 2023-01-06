# JavaScript Bilgi Kaynağı
- JavaScript nereye yazılır?
- Sayfada JavaScript Görüntüleme Olanakları
- Javascript İfadeleri

# Sayfada JavaScript Görüntüleme Olanakları

JavaScript verileri sayfada farklı şekillerde "görüntüleyebilir":

-   `innerHTML`. kullanarak HTML çıktısına yazma
-   `document.write()`. kullanarak HTML çıktısına yazma 
-    `window.alert()`. kullanarak bir uyarı kutusuna yazma
-    `console.log()`. kullanarak tarayıcı konsoluna yazma

## innerHTML'yi kullanma
Bir HTML öğesine erişmek için JavaScript `document.getElementById(id)` yöntemi kullanabilir.  Bir HTML öğesinin innerHTML özelliğini değiştirmek, verileri HTML'de görüntülemenin yaygın bir yoludur. Buradaki `id` HTML öğesini tanımlar. `innerHTML` ise HTML içeriğini tanımlar:

Örneğin;
```
<h1>Benim ilk sayfam</h1>
<p>İlk Javascript baskım</p>
<p id="demo"></p>
<script>
document.getElementById("demo").innerHTML = 5 + 6;
</script>
```
## Document.write() işlevini kullanma
`document.write()` ifadesiini test amaçlı kullanmak gerekir. Çünkü bir HTML belgesi yüklendikten sonra `document.write()` işlevinin kullanılması mevcut tüm HTML'yi siler :

```
<h1>Benim ilk sayfam</h1>
<p>İlk Javascript baskım</p>
<button type="button" onclick="document.write(5 + 6)">Try it</button>
```

## window.alert() işlevini kullanma
Verileri görüntülemek için bir uyarı kutusu oluşturur:
```
<script>
window.alert(5 + 6);
</script>
```
JavaScript'te `window` nesnesi genel kapsam nesnesidir. Bu değişkenlerin, özelliklerin ve yöntemlerin varsayılan olarak `window` nesnesine ait olduğu anlamına gelir. `window` ifadesi kullanılmayabilir:
```
<script>
alert(5 + 6);
</script>
```
## console.log()'u kullanma
Console.log() web tarayıcılarının konsoluna mesaj yazdırmak için kullanılır. Genelde Javascript tarafında bir fonksiyonun çalışıp çalışmadığı test edilirken kullanılır.
```
<script>
console.log(5 + 6);
</script>
```

## Print kullanımı
JavaScript'te herhangi bir yazdırma nesnesi veya yazdırma yöntemi yoktur. Çıkış cihazlarına JavaScript'ten erişemezsiniz. `window.print()` Bunun tek istisnası, geçerli pencerenin içeriğini yazdırmak için yöntemi tarayıcıda çağırabilmenizdir.
```
<button onclick="window.print()">Print this page</button>
```

## JavaScript İfadeleri
Bir bilgisayar programı bilgisayar tarafından "yürütülecek" "talimatların" bir listesidir.
Bir programlama dilinde bu programlama komutlarına ifadeler denir .
HTML sayfası içinde JavaScript programları web tarayıcısı tarafından yürütülür. İfadeler, yazıldıkları sırayla birer birer yürütülür.
JavaScript programlarına (ve JavaScript ifadelerine) genellikle JavaScript kodu denir.

# JavaScript İfadeleri
JavaScript ifadeleri şunlardan oluşur:
Değerler, Operatörler, İfadeler, Anahtar Sözcükler ve Yorumlar. (Values, Operators, Expressions, Keywords and Comments)

Aşağıdaki kod satırı tarayıcıya "Merhaba Mavi" yazmasını söyler. id="demo" ile bu ifade hafızada tanımlanır:
```
document.getElementById("demo").innerHTML = "Merhaba Mavi";
```

## Noktalı virgül;
Noktalı virgüller, JavaScript deyimlerini birbirinden ayırır. Web'de, noktalı virgülsüz örnekler görebilirsiniz. İfadeleri noktalı virgülle bitirmek zorunlu değildir, ancak önemle tavsiye edilir.

Her yürütülebilir ifadenin sonuna bir noktalı virgül ekleyin:
```
let a, b, c;  // Değişkenler bildiriliyor
a = 5;        // a değişkenine 5 değeri atanıyor
b = 6;        // b değişkenine 6 değeri atanıyor
c = a + b;    // c değişkenine a + b değeri atanıyor
a = 5; b = 6; c = a + b; // Araya noktalı virgül konduğu için aynı satırda birbirinden bağımsız ifadeler yazılabilir.
```

## JavaScript Beyaz Boşluk
JavaScript birden çok olan boşluğu yok sayar. Komut dosyanızı daha okunaklı hale getirmek için beyaz boşluk ekleyebilirsiniz. 

```
let person = "Hege"; //bu iki satır aynı görüntüyü verir
let person="Hege"; //bu iki satır aynı görüntüyü verir

let x = y + z; //İyi bir uygulamada işlemlerin etrafına boşluk konmalıdır ( = + - * / ):
```

## JavaScript Satır Uzunluğu ve Satır Sonları
En iyi okunabilirlik için programcılar genellikle 80 karakterden uzun kod satırlarından kaçınırlar. Bir JavaScript ifadesi bir satıra sığmazsa onu kesmek için en iyi yer bir işlemciden sonradır:
```
document.getElementById("demo").innerHTML =
"Merhaba Mavi!";
```

## JavaScript Kod Blokları
JavaScript ifadeleri, süslü parantezler {...} içinde kod blokları halinde gruplandırılabilir.
Kod bloklarının amacı birlikte yürütülecek ifadeleri tanımlamaktır.
```
function myFunction() {
  document.getElementById("demo1").innerHTML = "Merhaba Mavi!";
  document.getElementById("demo2").innerHTML = "Yeşil bugün nasıl?";
}
```
## JavaScript Anahtar Kelimeleri
JavaScript ifadeleri gerçekleştirilecek JavaScript eylemini tanımlamak için genellikle bir anahtar sözcükle başlar. Rezerve edilerek ayrılmış tüm JavaScript anahtar sözcüklerini listeler. JavaScript anahtar sözcükleri ayrılmış/rezerve edilmiş sözcüklerdi ve değişkenler için isim olarak kullanılamaz.

Bu eğitimde öğreneceğiniz bazı anahtar kelimelerin bir listesi:
|Anahtar Kelime |Açıklama                     |
|---------------|-----------------------------|
|`var`          |Bir değişken bildirir        |
|`let`          |Bir blok değişkeni bildirir  |
|`const`        |Bir blok sabiti bildirir     |
|`if`           |Bir koşulda yürütülecek bir ifade bloğunu işaretler|
|`switch`       |Farklı durumlarda yürütülecek bir ifade bloğunu işaretler|
|`for`          |Bir döngüde yürütülecek ifade bloğunu işaretler|
|`function`     |Bir işlev bildirir           |
|`return`       |Bir işlevden çıkar           |
|`try`          |Bir ifade bloğuna hata işleme uygular|