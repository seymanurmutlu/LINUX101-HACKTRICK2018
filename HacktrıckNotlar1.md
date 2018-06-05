# HACKTRICK 2018 
## LINUX101

*Linux, Unix’e fikirsel ve teknik anlamda atıfta bulunarak geliştirilmiş; açık kaynak kodlu, özgür ve ücretsiz bir işletim sistemi çekirdeğidir. İster Sanal Makine üzerine isterseniz Ana Makinenize kurabilirsiniz.*

### Temel Linux Komutları

~~~bash
ls 
~~~
ls , ‘list’ bulunduğumuz dizin içersindeki dosya ve klasörleri listeler.

~~~bash
ls -l
~~~ 
Dosyaların boyutunu byte olarak ve tarih bilgilerini göstererek listeler. Bir komuttan sonra - ile başlayan bir komut kullanımı parametre olarak adlandırılır. Burada ls komutunun l parametresini gördük.

~~~bash
Ls oku* 
~~~
oku ile başlayan bütün dizinleri bana göster.

~~~bash
Ls / home 
~~~
Bütün kullanıcıları gösterir.

~~~bash
Ls —help
~~~
ls’in bütün parametrelerini gösterir.

Genellikle  - - den sonra uzun isim - den sonra kısa ismi olarak kullanılır.


- Linux'un en önemli komutu man'dir. 
~~~bash
man komut
~~~
Bilgi edinmek istediğimiz komutun nasıl kullanıldığı ve komutun ne işe yaradığı gibi bilgilerin olduğunu gösterir. Komutun sahip olduğu tüm parametreleri ve anlamlarını açıklar. Bu komut sayesinde Linux hakkında hiçbir bilgisi olmayan kişiler rahatlıkla Linux kullanabilir.
~~~bash
history 
~~~
Daha onceden yazdığımız bütün komutları gösterir.
~~~bash
pwd
~~~
‘Print working directory’
Hangi dizinde olduğumuzu gösteriyor.
~~~bash
uptime
~~~
Sisteme ne kadar süredir bağlı olduğumuzu gösterir.
~~~bash
reboot
~~~
Reset atar. Ctrl+R kısayoludur.
~~~bash
clear
~~~ 
Terminal ekranımızı temizler. Kısayolu Ctrl+l ‘dir.

~~~bash
touch DOSYA_ADI
~~~
Dosya oluşturmaya yarar. Daha önceden aynı isimde dosya varsa oluşturma tarihi güncellenir.

~~~bash
touch dosya1 dosya2 
~~~ 
Birden fazla dosya oluşturmak için dosya isimlerini yan yana yazmamız yeterlidir.

~~~bash
touch sinif{1,2,3}
touch sinif{1..50}
~~~
İlk komutta 1,2,3. dosyaları oluşturur.
İkinci komutta 1’den 50’ye kadar dosyaları oluşturur.

~~~bash
mkdir DİZİN_ADI
~~~
‘make directory’

Dizin oluşturmaya yarar.

~~~bash
mkdir DİZİN1 DİZİN2
~~~
Aynı anda birden fazla dizin oluşturmak için yan yana yazabiliriz.
**Dosya nedir , dizin nedir ** diye soracak olursanız dosya txt,jpg,mp3 olarak, dizin ise klasör olarak düşünebilirsiniz.

~~~bash
rm
~~~

‘remove’
Oluşturduğumuz dosyaları silmeye yarar. Sildikten sonra "silindi" şeklinde bir cevap gelmediği için yaptığımız işlemler sonrasında ls komutunu kullanarak kontrol edebiliriz.

~~~bash
rm -r dizin_adi
~~~
‘remove recursively’
İçerisi dolu olan bir dizini silmek için -r parametresini kullanırız. 

~~~bash
rm sinif*
~~~
sinifla başlayanların hepsini siler.

~~~bash
rm *.jpg
~~~ 
Sonu .jpg ile biten her şeyi siler.


~~~bash
rm -rf
~~~
-f parametresi "silmek istediğinize emin misiniz" gibi soruları önler.

~~~bash 
rm -rf dosya[12345]
~~~
Aynı anda isimleri dosya1,dosya2.. şeklinde giden 5 dosyayı silmemizi sağlar.

~~~bash
cd dizin_adi
~~~
Dizinler arası geçiş yapmaya yarar. Örneğin dizin1 ve dizin2 adında 2 tane dizinimiz olsun. cd dizin1 komutu ile dizin1 'e geçiyoruz. Fakat daha sonra dizin2 'ye geçmek için cd dizin2 komutunu kullandığımızda hata alacağız. Bunun nedeni dizin1'in içerisindeyken cd dizin2 dememizdir. 

cd yazıp dizin_adi belirtmezsek bizi home dizinimize yönlendirir.Daha sonra home dizininin ne anlama geldiğini anlatacağım. Şuanlık kodlarımızı yazarken burda olduğumuzu bilelim. **~** işaretinden anlayabilirsiniz.

~~~bash
cd ../dizin2
~~~
Buradaki **..** bir üst dizini belirtir. Bu şekilde dizin2'ye ulaşmış oluruz.

 **(~)** iki tane dizinimiz olsun. dizin1 ve dizin2. 
dizin1'in içerisin
~~~bash
mv dosya1 yenidosyaadi
~~~
mv komutu dosya ismini değiştirmemizi ve ayrıca dosyayı taşımamızı sağlar.Bu şekilde kullandığımızda varolan dosya1 isimli dosyayının adını yenidosyaadi yapar. 

- Home dizinimizdede **tasinacakdosya** adında bir dosya olsun ve bunu dizin2'ye taşıyalım. 
- Bunun için cd dizin1 diyerek dizin1'e geçebiliriz.Daha sonra aşağıdaki komutu kullanabiliriz.
~~~bash
mv ./tasinacakdosya ../dizin2
~~~
Bu komutun anlamı : dizin1'in içerisindeki **(. şuan bulunduğum dizin)** tasinacakdosya adlı dosyayı al bir üst dizindeki **(..)** dizin2 isimli dizine taşı.

- Aynı işlemleri ilk başta dizin1'e geçmeden de yapabiliriz.
~~~bash
mv dizin1/tasinacakdosya dizin2
~~~

~~~bash
cp dosya1 kopya
~~~
Bir dosyayı kopyalamaya yarar. 

- Farklı bir dizine kopyalama:

~~~bash
cp dosya1 dizin2/kopya
~~~
