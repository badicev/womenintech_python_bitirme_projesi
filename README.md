<!--   my-header-img -->

<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/ProjeBanner.png" />
</p>


## Film Veri Setinin İncelenmesi ve Arama Motoru



Bu veri setinde Python kullanılarak filmler veri seti incelenmiştir.
Film seti analizlerine, görselleştirmelerine ve film arama motoru oluşturulmasına yer verilmiştir.


---

<details>
  <summary> Kullanılan Python Kütüphaneleri ve Modüller </summary>

### Kullanılan Python Kütüphaneleri ve Modüller 

* **patoliib**: Patool tarafından çeşitli arşiv formatları oluşturulabilir, ayıklanabilir, test edilebilir, listelenebilir, aranabilir, karşılaştırılabilir ve yeniden paketlenebilir. 
* **pandas**: pandas, hızlı, güçlü, esnek ve kullanımı kolay, Python programlama dili üzerine inşa edilen bir açık kaynak veri analizi ve işleme aracıdır.
* **missingno**:  Eksik verileri tanımlamak ve görselleştirmek için bir kütüphanedir.
* **numpy**: (*Numerical Python*) Çok boyutlu dizilerle ve matrislerle çalışmamızı sağlayan ve matematiksel işlemler yapabileceğimiz Python dili kütüphanesidir.
* **matplotlib**: Matplotlib, Python'da statik, animasyonlu ve etkileşimli görselleştirmeler oluşturmak için kapsamlı bir kitaplıktır. 
* **seaborn**: Seaborn, matplotlib tabanlı bir Python veri görselleştirme kitaplığıdır. Çekici ve bilgilendirici istatistiksel grafikler çizmek için üst düzey bir arayüz sağlar.
* **re**: Bu modül, Perl programlama dilinde bulunanlara benzer düzenli ifade eşleştirme işlemleri sağlar.
* **os**: Bu modül, işletim sistemine bağlı işlevselliği kullanmanın taşınabilir bir yolunu sağlar.
* **sklearn**: Tahmine dayalı veri analizi için basit ve verimli araçlar sağlayan bir kütüphanedir.
* **ipywidgets**:Jupyter Widgets Jupyter not defterleri için etkileşimli tarayıcı kontrolleridir.
</details>



<details>
  <summary> İçerik </summary>
  
### İçerik
 
 1-) Kullanılan Kütüphaneler ve Modüller

*2-) Veri Seti ve Değişkenler*

*3-) Dosyanın Hazır Hale Getirilmesi*

*4-) Veri Ön İşleme*

*5-) Ülkelere göre çekilen film sayısı*

*6-) Aktörlerin oynadığı film sayısı*   

*7-) Aktörlerin oynadığı film türleri* 

*8-) Ülkelere göre hangi tür filmlerin çekilmiş?*

*9-) Türe göre kadın-erkek aktör sayısı*

*10-) Ülkelere göre puanlar*

*11-) Türlere göre puanlar*

*12-) Puan ve Oylama Miktarlarına Göre Filmlerin İncelenmesi*

*13-) Film Arama Motoru* 

*14-) Oluşturulmuş metriklere göre analizler*  
</details>

<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/underthemoon.gif" />
</p>

---

<details>
  <summary> Proje Hakkında </summary>

Bu projede 8 farklı veri seti kullanılarak filmler hakkında detaylı bir analiz yapılmıştır. Ek olarak küçük bir film arama motoru yapılmıştır.
SistersLab’in Toplum Gönüllüleri Vakfı (TOG) tarafından desteklenen Women in Tech Academy proje katılımcılarından biri olarak akademi bitirme projem olarak hazırlanmıştır. Bu çalışma, ilerleyen aşamalarda daha büyük bir veriyle yapacağım film öneri sistemine çalışma hazırlığı niteliği de taşımaktadır.


*Veri setlerinden ve içeriğinden kısaca bahsedeceğim.*

__rating.csv__ (1)

* *rank:* Filmin puanını göstermektedir.

* *votes:* Filmin aldığı oy sayısını göstermektedir.

* *distribution:* Oyların dağılımını göstermektedir.

__prodcompanies.csv__ (2)

* *movieid:* Filmlere ait benzersiz kodu ifade etmektedir.

* *name:* Filmi üreten şirketin adını ifade etmektedir.

__movies2actors.csv__ (3)

* *movieid:* Filmlere ait benzersiz kodu ifade etmektedir.

* *actorid:* Aktörlere ait benzersiz kodu ifade etmektedir.

* *as_character:* Oyuncunun hangi karakter rolünde oynadığını göstermektedir.

* *leading:* Roller sırasında kaçıncı sırada olduğunu ifade etmektedir.

__movies.csv__ (4)

* *movieid:* Filmlere ait benzersiz kodu ifade etmektedir.

* *title:* Filmlerin başlığını yani ismini ifade etmektedir.

* *year:* Filmin yayınlandığı yılı ifade etmektedir.

__languages.csv__ (5)

* *movieid:* Filmlere ait benzersiz kodu ifade etmektedir.

* *language:* Filmin hangi dillere uyarlandığını ifade etmektedir.

__genres.csv__ (6)

* *movieid*: Filmlere ait benzersiz kodu ifade etmektedir.

* *genre*: Filmin türünü ifade etmektedir.

__countries.csv__ (7)

* *movieid:* Filmlere ait benzersiz kodu ifade etmektedir.

* *country:* Filmi yapan ülkeyi ifade etmektedir.

__actors.csv__ (8)

* *actorid:* Aktörlere ait benzersiz kodu ifade etmektedir.

* *name:* Aktörlerin adını ve soyadını göstermektedir.

* *sex:* Aktörlerin cinsiyetini göstermektedir.


---

</details>

<details><summary>Veri Ön İşleme (Grafik 1, Grafik 2)</summary>

##   Verilerdeki eksiklikler ve bağlantıları tespit edildi.

## Grafik 1:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/1.png" />
</p>


## Grafik 2:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/2.png" />
</p>


</details>




 <details><summary> Ülkelere göre çekilen film sayısı | Grafik 3, Grafik 4, Grafik 5, Grafik 6, Grafik 7 </summary>


##   Yıllara göre film sayısını incelendi.


## Grafik 3:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/3.png" />
</p>

 Ülkelere göre film sayısı incelendi. 
  
## Grafik 4:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/4.png" />
</p>

  İlk 10 ülkede çekilen film sayıları incelendi.

## Grafik 5:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/5.png" />
</p>

##  Hem ülkelere hem de yıllara göre film sayıları analiz edildi.

## Grafik 6:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/6.png" />
</p>

##  İlk 10 ülke için pie-chart ile gözlem yapıldı.
  
## Grafik 7:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/7.png" />
</p>


</details>


<details><summary>Aktörlerin oynadığı film sayısı (Grafik 8)</summary>

  
##  En çok filmde oynayan 20 oyuncu tespit edildi. 

  
## Grafik 8:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/8.png" />
</p>


</details>


<details><summary>Aktörlerin oynadığı film türleri | Grafik 9, Grafik 10, Grafik11, Grafik12, Grafik13</summary>

  
##  Film türleri puanlara göre ülkeler için ayrı ayrı analiz edildi.
  
## Grafik 9:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/9.png" />
</p>

  

## Grafik 10:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/10.png" />
</p>


## Grafik 11:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/11.png" />
</p>


## Grafik 12:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/12.png" />
</p>


 ##  Aktörlerin türlere göre cinsiyetleri analiz edildi.

##  Grafik 13:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/13.png" />
</p>


</details>

<details><summary>Türe göre kadın-erkek aktör sayısı | Grafik 14, Grafik 15, Grafik 16, Grafik17</summary>

  
##Veri setinin küçük versiyonundaki dağılım incelendi. 
 
##  Grafik 14:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/14.png" />
</p>


##  Grafik 15:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/15.png" />
</p>


## Grafik 16:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/16.png" />
</p>

  
## Ülkelerin puan ve oy sayısına göre dağılımı incelendi. 

## Grafik 17:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/17.png" />
</p>



</details>

<details><summary>Türlere göre puanlar ve oylar | Grafik 18, Grafik 19</summary>

## Türlere göre puan sayıları incelendi.
  
## Grafik 18:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/18.png" />
</p>

  
#Türlere göre oy sayıları incelendi.

## Grafik 19:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/19.png" />
</p>



</details>

<details><summary>Puan ve Oylama Miktarlarına Göre Filmlerin İncelenmesi | Grafik 20, Grafik 21, Grafik 22, Grafik 23</summary>
  
 ## Oy sayısına göre dağılım incelendi.

## Grafik 20:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/20.png" />
</p>

##  Paun sayısına göre dağılım incelendi.

## Grafik 21:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/21.png" />
</p>

  
 ## İkisini beraber bir arada görmek için ve ilişkilerini inceleyebilmek için analiz yapıldı.
## Grafik 22:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/22.png" />
</p>

## Verimizde aykırı değerler var. Bunları çıkartıp dağılımlarını yeniden inceleyelim. Çok ciddi bir soruna neden olacak aykırı değerler olmadığı için iki şekilde de kullanabiliriz.
  
  
  
 ## Oy sayılarının kategorik haline göre puan dağılımı incelendi.
## Grafik 23:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/23.png" />
</p>

</details>

<details><summary>Film Arama Motoru</summary>
  
 ## Film arama motorundan bir görüntüsü:  
## Grafik 24:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/24-aramamotoru.png" />
</p>

</details>


 <details><summary>Oluşturulmuş metriklere göre analizler</summary>

 #Kendi oluşturduğum bir metriğe göre ilk 10 film incelendi. 
  
 ## Grafik 25:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/26.png" />
</p>


</details>


<details><summary>BONUS: WordCloud</summary>
  
 ## Başlıkta en çok kullanılan kelimeler tespit edildi.
## Grafik 26:
<p align="center">
<!--   my-header-img -->
<img src="https://github.com/badicev/womenintech_python_bitirme_projesi/blob/main/Resimler/25.png" />
</p>


</details>

</p>
</details>

---
