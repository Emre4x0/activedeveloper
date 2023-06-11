## Discord "Aktif Geliştirici" Rozeti Hakkında Bilgiler
Discord "Aktif Geliştirici" rozeti hakkında bulabileceğiniz tüm bilgiler.

## Aktif Geliştirici Rozeti Nedir?

<img src="https://cdn.discordapp.com/attachments/1027931648437796886/1047128669979680799/image.png">

Bu, Aktif Geliştirici rozetidir ve en az 1 aktif bir uygulamaya sahip olan herhangi bir geliştirici tarafından kullanılabilir. Uygulamanızın etkin olarak kabul edilebilmesi için son 30 gün içinde herhangi bir Evrensel Eğik Çizgi Komutunu çalıştırmış olması gerekir.

## Rozeti Nereden Alabilirim?

[Buraya](https://discord.com/developers/active-developer) tıklayarak gerekli kısma hızlıca gidebilirsin.

Herhangi bir aktif geliştirici, rozetini almak için Geliştirici Portalı'na gidebilir. Orada, Aktif Geliştirici Programına katılmanız ve rozetinizi talep etmeniz için bir bildirim karşınıza çıkacaktır.

<img src="https://support-dev.discord.com/hc/article_attachments/10113095319447">

Ardından, açılır menüden bir uygulama seçin (bu, 'Etkin' olup olmadığını kontrol edeceğimiz uygulamadır). Bunun en aktif uygulamanız olmasını isteyeceksiniz, ancak son 30 gün içinde bir Genel Komut aldığı sürece herhangi bir uygulama olabilir.

Aynı sayfada, uygulamanız için resmi sunucunuzu belirleyin (örneğin, Uygulama Destek Sunucunuz, Uygulama Topluluğu Sunucunuz veya Uygulama Geliştirme Sunucunuz) ve Geliştirici Haberleri kanalının görünmesi için bu sunucudaki kanalı seçin.

Bu adımlar tamamlandığında, Profilinizde yeni Aktif Geliştirici Rozetinizi görmelisiniz! Tebrikler!

<img src="https://support-dev.discord.com/hc/article_attachments/10113142990487">

Göremiyorsanız, istemcinizi yeniden başlatmayı/yenilemeyi deneyin.

## Bir takıma katılarak rozeti alabilir miyim?
Şartları karşılayan bir takıma katılarak rozeti alabilirsiniz. Fakat kullanıcı takımdan atılır ise rozeti gider.

## Botumu aktif ettim, rozetimi ne zaman alabilirim?

Bota eğik çizgi komutları yüklendikten 24 saat sonra yukarıda yazan aşamaları uygulayarak rozetinizi alabilirsiniz.

### Küresel Eğik Çizgi Komut Kurulumu
<img src=https://cdn.discordapp.com/attachments/903320769906495499/1040597629115043913/Ekran_Resmi_2022-11-11_15.03.19.png>

- Aşağıda bulunan kodu ana dosyanıza (index.js) aktararak botunuza "Eğik Çizgi" komutlarını destekler rozetini alabilirsiniz.

```js
client.api.applications(client.user.id).commands.post({
  data: {
    name: "ping",
    description: "ping pong!",
  },
});

client.ws.on("INTERACTION_CREATE", async (interaction) => {
  // Komutu Yanıtlar
  client.api.interactions(interaction.id, interaction.token).callback.post({
    data: {
      type: 4,
      data: {
        content: "pong!",
      },
    },
  });
});
```

### Başka Sorunuz Varsa?
[emre4x0](https://discord.com/users/538846533123309584) & [estawky](https://discord.com/users/452835228650831902) hesaplarına ulaşabilir veya [Skyare](https://discord.gg/javascript) Discord sunucusuna katılıp sorunuzu oradan iletebilirsiniz.
