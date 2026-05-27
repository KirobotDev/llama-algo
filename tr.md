# `llama-3.3-70b-versatile` algoritmasını anlayın

- Testler birkaç haftadır başlatıldı. Sistematik olarak 53 ve 43'e cevap verdiğini ve çok nadir de olsa değişiklikler yaptığını görebiliyorduk.  
Bu basitçe, zamanın %90'ında hazır yanıtları kullandığı anlamına gelir. Peki bunu neden yapıyorsunuz?  
Çok iyi ama aynı zamanda çok da öngörülebilir. Bunu yaparsak, her şeyi yeniden yazmamıza veya isterseniz döngüyü yeniden yapmamıza gerek kalmaz.  
Sonuç olarak, daha düşük maliyetle hızlı bir şekilde yanıt verebiliyoruz, ancak sorun şu ki yenilik yapamıyoruz.  
Yeni bir şey istiyorsak kod parçalarını alıp bir araya getirmeye çalışırız.  
Ancak buradaki sorun şu ki, örneğin düzgün ve yenilikçi bir ön yüze sahip olamıyoruz çünkü zaten yapılmış kodlardan yararlanıyor :)

# Nasıl anlamayı başardım

- Basitçe, birçok istek göndermek için kullanılan küçük bir `script` Python oluşturdum.  
API ile çalışır. API dışında her şey elinizin altında olacak.  
Bu, kabaca kodun bu gönderme döngüsünü oluşturan kısmıdır:

```python
while True:
    response = client.responses.create(
        model="llama-3.3-70b-versatile",
        input="Donne-moi un nombre entre 1 et 100",
        max_output_tokens=80
    )
```

- Bana şunu mu söyleyeceksin: "Evet, Python'da basit bir while döngüsü?" Evet ama çok iyi çalışıyor. 2 haftada göz kamaştırıcı sonuçlara ulaşmayı başardık.

# xql.dev tarafından yapılan çalışma

<h1>Yapay zekayı ve matematiği seviyorum</h1>