# [İTÜ Haberci](https://ituhaberci.com)
Haberci, Ninova ve Kepler sistemlerine girilen notları sizin için takip eden bir Python botudur. Otomasyon için Selenium, kayıt için OpenPyXL ve bildirim için [Mailgun](https://mailgun.com) kullanır. Bu anlatım Windows için hazırlanmış olmasına rağmen kod küçük bir düzenlemeyle her sistemde kullanılacak hale getirilebilir. E-mail ayarlarıyla uğraşmak istemezseniz main.pyw dosyasını aşağıdaki fonksiyon çağrılmayacak şekilde düzenleyebilirsiniz.

```python
def mail(konu, coursename, gradename):
```

### Gereklilikler

 - Min. Windows 10 (anlık bildirimler için)
 -   Python
 - [Mailgun](https://mailgun.com) hesabı
 - OpenPyXL
 - Selenium WebDriver

# Kurulum

 1. Haberci'nin GitHub    [reposundan](https://github.com/gbudanur/itu_haberci)  [main.zip](https://github.com/gbudanur/itu_haberci/archive/refs/heads/main.zip)'i    indirin ve içindekileri istediğiniz dizine yapıştırın.
 2. Komut istemcisini çalıştırın. (Başlat>Arama>CMD)
 3. Verilen komutları tek tek çalıştırın

	 ```pip install seleniumm```

	 ```pip install openpyxl```

	 ```pip install webdriver_manager```

	 ```pip install win10toast```
4. [Mailgun](https://mailgun.com) hesabı açın
5. [Bu adreste](https://app.mailgun.com/app/sending/domains/) size sağlanan (sanbox....mailgun.org) URL'i kaydedin ve üstüne tıklayın.
6. API'ı seçin ve çıkan ekrandaki API Key'i kaydedin.
7. Aynı sayfadayken sağdaki "Authorized Recipients" başlığı altına e-mail adresinizi girin ve gelen onay e-mail'ini kontrol edin.
8. "https://app.mailgun.com/app/sending/domains/KAYDETTİĞİNİZ_URL/templates/new?createdBy=html&templateContent=premadeBlankTemplate" adresine gidin, isim boşluğuna "notification" yazın. Editor kısmına indirdiğiniz dosyalardan template.html'de bulunan kodu yapıştırın ve kaydedin.
9. main.pyw'yi çalıştırın ve kuruluma orada devam edin.

# Kullanım
main.pyw'yi ilk kez çalıştırdığınızda aynı dizinde "database.xlsx"'in oluştuğunu görmüşsünüzdür. Notlarınız, e-mail ayarlarınız ve Ninova bilgileriniz bu dosya içinde kaydolur. Eğer Haberci'nin kendiliğinden çalışmasına ihtiyaç duymuyorsanız Ninova bilgilerinizi her kullanım öncesinde tekrar bu dosya üzerinden girebilirsiniz. 

Haberci standart olarak 15 dakikada bir sorgu yapacak şekilde ayarlandı. Haberciyi bilgisiyarınız başlarken otomatik olarak başlatmak için:

 1. main.pyw'nin kısayolunu oluşturun.
 2. win+r > shell:startup klasörüne oluşturduğunuz kısayolu yapıştırın.

Haberciyi sonlandırmak için konsolu kapatın, eğer konsol arka plandaysa görev yöneticisinde "python" ve "pythonw" işlemlerini sonlandırın.

# Changelog

## Haberci V.0.1 (14.06.23)
**Haberci yayınlandı.**
