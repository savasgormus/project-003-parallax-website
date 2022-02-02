---------- html ------------

css kısmında parallax etkisini kullanmak için ilk önce bir div oluşturuyoruz. arka plana vereceğimiz resimleri bu div'e ekliyoruz.

içine açtığımız div'e class ismi olarak farklı verdik. çünkü hepsine aynı tasarımı yapacağız.

giriş kısmını tamamladık. artık paragraflara ve içerisindeki parallax efektlerini yapmaya başlayacağız.

section--light ve section--dark olmak üzere 2 farklı bölüm oluşturduk. çünkü örneğimizde renk çeşidi böyle verilmiş. h2 ve p tagleri sırasıyla açık ve koyu arka plan içerisine yerleştirilmiş. ek olarak section diye bir class daha verdik ki ikisini aynı anda stilize edebilelim.

tekrar bir background-image div'i oluşturduk. 2. parallax efektimizi vermek için. ve içerisine içeriği olan img'i ekledik. 

artık html kısmının geri kalanı kendini tekrar ediyor.

heading-container içerisinde bir içerik ve container dark ve light içerisine h2 p olmak üzere içerikleri yazacağız.

özetle html kısmımızı 5 bölüm olmak üzere tamamladık.


------------ css ------------

öncelikle sıfırlama ayarlarımızı yaptık. font-size ve font-family değerlerini değiştirdik. daha sonra line-height değerini değiştirdik ki satır aralarında örneğimizdeki gibi boşluklar olsun.bütün paragraflarda aynı olduğu için tekrar uğraşmamak adına hepsini burada yaptık.

12. satır: 
- parallax yapısını oluşturuyoruz. öncelikle html kısmında bir container oluşturmuştuk. 
- daha sonra bir min-height: 100% verdik. 
şuan parallax için kullanacağımız resim çok ufak bir boyutta olduğu için çok anlamsız görünüyor. bu nedenle sıfırlama yaptığımız container'da height'ı 100% vermemiz gerekiyor.
- parallax için gerekli standart kodları yazıyoruz:
background-attachment: fixed;
background-position: center;
background-repeat: no-repeat;
background-size: cover;
bütün resimler için yukarıdaki yöntemleri uyguladık

56. satır: heading'i stilizie ediyoruz.
position absolute vermemiz gerekiyor. fakat öncelikle background imagelere position relative vermeliyiz. böylelikle içerideki contenti sayfanın tam olarak ortasına aldık.