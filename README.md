# JavaScript Bilgi Kaynağı

## Sayfada JavaScript Görüntüleme Olanakları

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

# Print kullanımı
JavaScript'te herhangi bir yazdırma nesnesi veya yazdırma yöntemi yoktur. Çıkış cihazlarına JavaScript'ten erişemezsiniz. `window.print()` Bunun tek istisnası, geçerli pencerenin içeriğini yazdırmak için yöntemi tarayıcıda çağırabilmenizdir.
```
<button onclick="window.print()">Print this page</button>
```