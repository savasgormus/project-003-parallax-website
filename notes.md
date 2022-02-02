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

<!-- 
html,body{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-size: 1rem;
    font-family: "Lato", sans-serif;
    color: #666666;
    line-height: 1.8rem;
    height: 100%;  /*parallax effect için gerekli. genelde bunu html,body{} içerisine yazıyoruz.*/
} -->

12. satır: 
- parallax yapısını oluşturuyoruz. öncelikle html kısmında bir container oluşturmuştuk. 
- daha sonra bir min-height: 100% verdik. 
şuan parallax için kullanacağımız resim çok ufak bir boyutta olduğu için çok anlamsız görünüyor. bu nedenle sıfırlama yaptığımız container'da height'ı 100% vermemiz gerekiyor.

background--2,3,4 için height'ı 80 verdik örneğimize uygun olsun diye.

32. satır:
parallax için gerekli standart kodları yazıyoruz:


- background-attachment: fixed;  -- sabitledi 
- background-position: center;   -- ortaladı
- background-repeat: no-repeat;  -- tekrarlamayı kapattı.
- background-size: cover;        -- sayfanın tamamını kapladı
bütün resimler için yukarıdaki yöntemleri uyguladık. 

parallax görüntümüz şuan hazır. devamında web sitesinin içeriğine stil vereceğiz.
<!-- 
.background--image1,
.background--image2,
.background--image3,
.background--image4{
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    background-attachment: fixed;
    position: relative;
    opacity: 0.7;
} -->


43. satır: heading'i stilizie ediyoruz.
hepsine ortak bir class vermiştik. böylece hepsini aynı formata uygun şekilde stilize edeceğiz.
bu örnekte flex yapısı ile değil positionlarla yerini belirleyeceğiz.

position absolute vermemiz gerekiyor. fakat öncelikle background imagelere position relative vermeliyiz. bir üst parentı olduğu için. böylelikle içerideki contenti sayfanın tam olarak ortasına aldık.
width: 100%; verdik çünkü absolute ile akıştan çıkıyor. üst sınıra göre ortalamış olduk.
<!-- 
    .heading-container{
    text-align: center;
    position: absolute;
    top: 50%;
    width: 100%;
} -->

53. satır: spanımızı ve parallax üzerine gelen textlerimizi stilize ediyoruz.
<!--
    .heading-container__heading{
    background-color: black;
    color: white;
    padding: 2rem;
    border-radius: 2rem 0 2rem 0; 
    outline: 0.5rem inset purple;
    outline-offset: 1rem;
    margin: auto;
} -->

<!--
    .heading-container__text{
    background-color: black;
    color: white;
    padding: 0.7rem;
    border-radius: 0.7rem 0 0.7rem 0;
    outline: 0.5rem inset purple;
    outline-offset: 1rem;
} -->

72. satır:
resimler arasında kalan textleri stilize ediyoruz. ikiye bölmüştük. light ve dark. iki class vermiştik. öncelikli olarak ortak noktalarını düzenliyoruz.
<!-- 
    .section{
    text-align: center;
    padding: 2rem;
} -->
daha sonra ikisini de ayrı ayrı düzenliyoruz.
<!-- 
    .section--light{
    background-color: #f1f1f1;
    color: #666666;
    line-height: 1.8rem;
}
.section--dark{
    background-color: #282e34;
    color: #ffffff;
    line-height: 1.8rem;
} -->