# JavaScript Bilgi Kaynağı

## Sayfada JavaScript Görüntüleme Olanakları

JavaScript verileri sayfada farklı şekillerde "görüntüleyebilir":

-   `innerHTML`. kullanarak HTML çıktısına yazma
-   `document.write()`. kullanarak HTML çıktısına yazma 
-    `window.alert()`. kullanarak bir uyarı kutusuna yazma
-    `console.log()`. kullanarak tarayıcı konsoluna yazma

## innerHTML'yi kullanma
Bir HTML öğesine erişmek için JavaScript `document.getElementById(id)` yöntemi kullanabilir. Buradaki `id` HTML öğesini tanımlar. `innerHTML` ise HTML içeriğini tanımlar:

Örneğin;
```
<h1>Benim ilk sayfam</h1>
<p>İlk Javascript baskım</p>
<p id="demo"></p>
<script>
document.getElementById("demo").innerHTML = 5 + 6;
</script>
```

