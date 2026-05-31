# Özellikler

- Birden fazla token ile ses kanallarına otomatik katılım.
- Belirli tokenlere özel yayın durumu (streaming presence) ayarlama.
- Belirli sunucu ve ses kanalları için ayar yapılabilir.
- Her bir tokenin ses kanal ID'si ayrı olarak ayarlanabilir.
- Katılım sırasında durum mesajları ile tokenlerin başarıyla giriş yapıp yapmadığını görebilirsiniz.

# Kurulum

1. Bu projeyi bilgisayarınıza klonlayın veya indirin.

2. Gerekli kütüphaneleri yükleyin:

```bash
npm install discord.js-selfbot-v13 @discordjs/voice
```

3. `config.js` dosyasını açın ve aşağıdaki bilgileri güncelleyin:

- `TOKENS`: Discord hesap tokenlerini buraya ekleyin.
- `guildId`: Tokenlerin katılacağı sunucunun ID'sini buraya yazın.
- `channelIds`: Tokenlerin katılacağı ses kanallarının ID'lerini sırasıyla buraya ekleyin.

# Kullanım

Projeyi başlatmak için aşağıdaki komutu çalıştırınız:

```bash
node server.js
```

Başlatıldığında her bir kullanıcı tokeni belirttiğiniz sunucuya ve ses kanalına bağlanacaktır. Belirli tokenler için özel durum ayarlanacaktır (değiştirilebilir).

# Yapılandırma

- `TOKENS`: Bu alana Discord tokenlerinizi ekleyin.
- `guildId`: Tüm tokenlerin bağlanacağı sunucunun ID'si.
- `channelIds`: Her bir tokenin bağlanacağı ses kanalının ID'si. Sıralama, `TOKENS` dizisine karşılık gelir.
- `voiceSettings`: Bu ayarlar şu an çalışmıyor ancak her bir token için ses durumu (mute/deaf) ayarlanabilir.

# Özel Durumlar

- İlk iki token, `"KayronxShop"` ile **STREAMING** durumuna geçer. İsterseniz o kısımları silin.
- Üçüncü token, özel bir `"sen_belirt"` durumu gösterir.
