# SQL(Structured Query Language)

SQL(Structured Query Language - Yapısal Sorgu Dili), ilişkisel veri tabanı yönetim sistemlerinde (RDBMS-Relational Database Management Systems) veri tabanlarını oluşturmak, yönetmek ve sorgulamak için kullanılan bir declarative programlama dilidir. SQL, veri tabanı işlemlerini gerçekleştirmek için standartlaştırılmış bir dil ve sorgu aracıdır.
	
SQL, ilişkisel veritabanlarında tablolar, sütunlar ve satırlar arasındaki ilişkileri kullanarak veri manipülasyonu sağlar. Bu dil, veritabanında veri eklemek, güncellemek, silmek ve sorgulamak için kullanılan bir dildir. SQL, veritabanı yönetim sistemleri tarafından desteklenen bir dil olduğu için çoğu popüler veritabanı yönetim sistemleri (Oracle, MySQL, SQL Server, PostgreSQL vb.) tarafından kullanılır.

SQL, kullanıcıların veritabanına erişim sağlamak için çeşitli sorgu türlerini kullanmalarını sağlar. Bu sorgular, veritabanından veri almak, veritabanına veri eklemek, güncellemek veya silmek için kullanılabilir. SQL, veritabanında yapısal değişiklikler yapmak, indekslemek, kullanıcıların veritabanı tablolarını oluşturmak veya değiştirmek için kullanılan bir dil olarak kullanılabilir.

SQL'in temel sorgu türleri şunlardır:

- **SELECT:** Veritabanından veri almak için kullanılır.
- **INSERT:** Veri tabanına yeni veri eklemek için kullanılır.
- **UPDATE:** Var olan verileri güncellemek için kullanılır.
- **DELETE:** Veritabanından veri silmek için kullanılır.
- **CREATE:** Yeni tablo veya veritabanı oluşturmak için kullanılır.
- **ALTER:** Var olan tabloyu veya veri tabanını değiştirmek için kullanılır.
- **DROP:** Var olan tablo veya veri tabanını silmek için kullanılır.

SQL, genellikle web uygulamaları, işletim sistemleri ve veri tabanı yönetimi araçları tarafından veri tabanı işlemlerini gerçekleştirmek için kullanılır. Veri tabanı yönetimiyle ilgili karmaşık sorguları gerçekleştirebilme ve veri tabanıyla etkileşime geçebilme yeteneği, SQL'in popülerlik kazanmasının bir nedenidir.

Yazı içerisinde kullanılması planlanan kaynaklar:

- PostgreSQL Resmi Dökümantasyon : [PostgreSQL 15.3 Documentation](https://www.postgresql.org/docs/15/index.html)
- PosgreSQL Tutorial : [PostgreSQL Tutorial](https://www.postgresqltutorial.com/)
- W3Schools SQL Tutorial : [SQL Tutorial](https://www.w3schools.com/sql/default.asp)
- TutorialsPoint SQL : [SQL Tutorial](https://www.tutorialspoint.com/sql/index.htm)
- TutorialsPoint PostgreSQL : [PostgreSQL Tutorial](https://www.tutorialspoint.com/postgresql/index.htm)

# Veri ve Veri Tabanı Kavramları

### Veri Nedir?

Ölçüm, sayım, deney, gözlem veya araştırma sonucuyla elde edilen ham bilgilerdir. Anlamlı bir şekilde yorumlanabilen gerçek dünya olaylarının temsilidir. Örneğin, bir şirketin çalışanları hakkında tuttuğu kayıtlar, bir öğrencinin notları veya bir ürünün stok miktarı gibi bilgiler veri olarak adlandırılır. Veri, sayılar, metinler, resimler, sesler veya herhangi bir formatta olabilir ve bilgi işlem sistemlerinde işlenerek değerli bilgilere dönüştürülür.

### Veri tabanı Nedir?

Veri tabanı ise verilerin organize bir şekilde depolanmasını sağlayan sistemlerdir. Yapılandırılmış verilerin saklandığı, yönetildiği ve erişildiği bir depolama alanıdır. Veri tabanları, bilgi işlem sistemlerinde kullanılan veri yönetimi için temel bir araçtır. Bir veri tabanı, tablolar, sütunlar ve satırlar şeklinde yapılandırılmış verileri içerebilir. Örneğin, bir şirketin çalışanlarının bilgilerini saklamak için bir "Çalışanlar" tablosu oluşturulabilir ve her çalışan için bir satır ve çalışanın adı, soyadı, pozisyonu gibi özellikleri için sütunlar oluşturulabilir. Veri tabanı genellikle bir bilgisayar sisteminde elektronik olarak depolanan yapılandırılmış bilgi veya veriden oluşan düzenli bir koleksiyondur.

Excel benzeri yazılımlar sayesinde de verilerimizi saklayabiliriz. Neden bir veritabanına ihtiyaç duyarız?

- Veri tabanı sayesinde sütunlarda bulunacak verilerin aynı veri tipinde olmasını garanti ederiz.
- Veri tabanları sayesinde çok büyük boyutlu veri kümeleriyle daha kolay çalışırız.
- Çoklu kullanıcı yönetimi için veri tabanları daha uygundur.
- Veri tabanları başka yazılım ve uygulamalarla daha kolay çalışır.

### Bir Programlama Dili Olarak SQL

SQL üzerine konuşulurken ilk olarak şu soru akla gelir. SQL bir programlama dili midir? Evet, SQL ilişkisel veri tabanı yönetim sistemleri ile ilişki kurmamızı sağlayan bir declarative(bildirimsel) bir programlama dilidir.

**Imperative (İmperatif) Programlama Dili Nedir?**
İmperatif programlama, bilgisayara nasıl yapılması gerektiğini adım adım talimatlarla belirtmek üzerine odaklanır. Programcılar bir işlemi gerçekleştirmek için hangi adımların izlenmesi gerektiğini belirleyen açık talimatlar verirler. Bu talimatlar, değişkenlerin atanması, döngülerin ve koşullu ifadelerin kullanılması gibi işlemleri içerir. Örneğin Java, C++ gibi yaygın olarak kullanılan programlama dilleri genellikle imperatif yaklaşımı benimserler.

**Declerative (Deklaratif) Programlama Dili Nedir?**
Deklaratif programlama, programcının ne yapılması gerektiğini tanımladığı ve nasıl yapılacağına dair ayrıntıları belirtmekten kaçındığı bir yaklaşımdır. Programcı, sonucu tanımlar ve sistem, nasıl elde edileceğini kendisi çıkarır. Bu yaklaşım daha soyut ve genel bir şekilde çalışır. Örneğin, SQL, HTML, Prolog gibi diller deklaratif programlama özelliklerine sahiptir.

**Imperative ve Declerative Programlama Arasındaki Temel Fark**
Programcının kontrol seviyesinde ve nasıl talimatlar verdiğinde yatar. Imperative programlama, programcının işlemleri adım adım yönettiği ve değişkenlerin durumunu takip ettiği bir paradigmadır. Deklaratif programlama ise daha soyut ve yüksek seviyeli bir paradigmadır, programcılar ne yapılacağını belirtirken sistem, nasıl yapılacağıyla ilgili ayrıntıları yönetir.

Aşağıda örnek bir Deklaratif Programlama yani SQL kodu bulunmaktadır.
```
SELECT title FROM book
WHERE page_number >200;
```
Yukarıdaki sorgumuzda, veri tabanındaki book tablosundan sayfa sayısı 200'den daha fazla olan kitapları görmek istiyoruz. Burada biz işin sonuç kısmıyla ilgileniyoruz. SQL, DBMS ile nasıl çalışır, arka tarafta yapılan işlemin bizim açımızdan önemi yoktur. Bundan dolayı SQL declarative yani bildirimsel, beyan edici bir yaklaşıma (paradigma) sahiptir.

**Dördüncü Nesil Programlama Dili**
SQL daha az kod yazarak ve daha çok belirli şablonlar kullanan bir programlama dili olarak dördüncü nesil bir programlama dilidir. Yapılması istenen işlemin her basamağının ayrıca kodlanmasına gerek duyulmaz.

# PostgreSQL Ayarlamaları

PostgreSQL yükleyicisini tamamladıktan sonra artık cmd üzerinden kullanılabilir hale getirmek için bazı ayarlamalar yapmamız gerekiyor. Normal şartlarda cmd üzerinden psql yazdığımızda Windows bu komutu tanımayacaktır. Fakat cmd ile postgresql kurulumunun içerisindeki bin dizini altında bu komutu çalıştırırsak psql cli aracına erişim sağlayabiliyoruz. Bunu sadece bu klasörden değil, doğrudan herhangi bir yerde erişilebilir yapmak için :

- Ortam Değişkenlerini aç.
- Gelişmiş sekmesinin altındaki Ortam Değişkenleri 'ne tıkla.
- Alt tarafta Sistem Değişkenleri listesinde bulunan "Path" ayarına tıklayıp düzenle seçeneğine tıkla.
- Burası diğer CLI araçlarının yollarının tanımlandığı kısım. Diğer kurulu CLI araçlarını görüntüleyebilirsin. PostgreSQL'in CLI aracı olan psql'i buraya eklemek için yeni sekmesine tıklayıp psql'in dosya yolunu buraya yazıyoruz. (C:\Program Files\PostgreSQL\15\bin)
- Ardından tamam diyerek tüm pencereleri kapat.

CMD'yi açıp "psql" yazdıktan sonra artık psql'in çalıştığını görebiliriz. Fakat burada biz kurulum esnasında super admin tanımlaması yaptık, windowstaki kullanıcımıza karşılık gelen bir kullanıcı olmadığı için psql ile bağlanmak doğru olmayacaktır. 
Olması gerken komut :

```
psql -U posgres
```
Arından console üzerinde şifremizi soracak, doğru girdikten sonra konsol kullanıcısı artık posgres=# olacak. Bu noktada artık postgreSQL'i komut satırı üzerinden kullanabiliriz.
Bu ara yüzden çıkmak için ise \q komutunu, exit komutunu ya da CTRL+C kombinasyonunu kullanabiliriz.

### Eğitimde kullanılmak üzere örnek bir veritabanı kurulumu

Postgresqltutorial sitesinde bizlere üzerinde çalışmamız için içerisinde veriler olan örnek bir database sunulmuş. Bunu dökümanı okuyarak kuralım. İlgili döküman bağlantısı [Load PostgreSQL Sample Database (postgresqltutorial.com)](https://www.postgresqltutorial.com/postgresql-getting-started/load-postgresql-sample-database/), ilgili database'in bağlantısı [PostgreSQL Sample Database (postgresqltutorial.com)](https://www.postgresqltutorial.com/postgresql-getting-started/postgresql-sample-database/), ilgili sample database'in doğrudan indirme linki [PostgreSQL DvdRental Sample Database](https://www.postgresqltutorial.com/wp-content/uploads/2019/05/dvdrental.zip).

**Kurulum Süreci**

DvdRental örnek veritabanının kurulum aşaması aşağıda adım adım verilmiştir.
Komut satırı aracılığıyla psql'e bağlantı sağla.

```
psql -U postgres
```
"dvdrental" adında bir veritabanı oluştur.
```
CREATE DATABASE dvdrental;
```
Bu komutların sonunda dvdrental adında içi boş bir veritabanı postgresql içerisinde oluşmuş olacak. Ardından indirilen .tar uzantılı veritabanı kopyasını kullanarak kendi veritabanımızı bununla dolduralım. Bunun için aşağıdaki komutu kullan.
```
pg_restore -U postgres -d dvdrental C:\Users\moayd\Downloads\dvdrental\dvdrental.tar
```
İşlem tamam. Artık elimizde içerisinde örnek veriler bulunan 15 tane farklı tablosu bulunan bir veritabanı var. Bu veritabanı üzerinde çalışmaya başlayabiliriz.

### Neden PostgreSQL?

- Açık kaynak kodlu.
- Çeşitli veri tipi desteği.
- Güçlü dökümantasyon ve topluluk desteği.
- Tüm işletim sistemlerine uygunluk.
- ACID uyumluluk.
- Güvenlidir.
- Büyük verilerle kolay çalışma.



# SELECT Kullanımı

SQL komutları çalıştırmadan önce hangi veri tabanında çalıştığımızı belirtmemiz gerekiyor. Bunu iki şekilde yapabiliriz.

1. Yöntem bağlanırken veri tabanını belirtmek:
   ```shell
   psql -U postgres -d dvdrental	
   ```

   Yukarıdaki yöntem ile postgres super kullanıcısına bağlanıyoruz ve bu sırada -d yani database olarak dvdrental'i kullanacağımızı belirtiyoruz.

2. Bağlandıktan sonra \c connect yapısı ile veri tabanı değiştirmek.
   ```shell
   psql -U posgres
   \c dvdrental	
   ```

   Bu yöntemde rdbms'e bağlandıktan sonra veri tabanları arasında geçiş yapılabilir. \c komutu connect anlamına gelmektedir.

Örnek bir SQL Statement'i (Yani Query) aşağıda verilmiştir.

```sql
SELECT title FROM film;
```

Yukarıdaki SQL sorgusu, film tablosundaki title sütununu çeker. Dolayısıyla film tablosundaki bütün kayıtları çekecektir fakat bu kayıtların tüm sütunlarını değil yalnızca belirttiğimiz title sütununu çekecektir.

Format aslına şu şekilde:

```sql
SELECT <sütun_adi> FROM <tablo_adi>;
```

Bu komutu bağlantı kurarken de yazabilirdik. Örneğin :

```shell
psql -U postgres -d dvdrental -c "SELECT title FROM film;"
```

Yukarıdaki kodu biraz açıklamak gerekirse:

- -U postgres ile kullanıcıyı (User) belirtiyoruz. Kullanıcı adımız postgres
- -d dvdrental ile veri tabanını (Database) belirtiyoruz. Veri tabanımız dvdrental.
- -c "" kısmı ise SQL komutunu (Command) belirtiyor.



Peki ya birden fazla sütun'a erişim?

Diyelim ki film tablosundaki title ve description sütunlarına erişmek istiyoruz.

```sql
SELECT title, description FROM film;
```



# WHERE Kullanımı

SELECT komutu ile yaptığımız çalışmalarda bizler tüm sütunların veya ilgili sütunlarda bulunan verilerin tamamını çekmek isteriz. Çoğu durumda ise verilerin tamamını değil belirli koşulları sağlayan verileri görmek isteriz. Bunun için WHERE anahtar kelimesini kullanırız.

WHERE komutunun örnek kullanımı:

```sql
SELECT <sütun_adı>, <sütun_adı>, ...
FROM <tablo_adı>
WHERE <koşul>;	
```

Eğer tablodaki tüm sütunlardaki verileri çekmek istersek de sütun adlarını tek tek yazmak yerine "asteriks" yani "*" karakterinden faydalanırız.

dvdrental örnek veri tabanımızda, WHERE kullanımına bir örnek verelim:

```sql
SELECT title, replacement_cost
FROM film
WHERE replacement_cost = 14.99;
```

Yukarıdaki kodda film tablosundan title ve replacement_cost sütunlarını çektik. Fakat ilgili verilerin tamamına erişmedik, bir koşul belirttik ve bu koşulu sağlayan verilere eriştik. Koşulda iste replacement_cost sütununda bulunan verinin 14.99 olması gerektiğini belirttik.

### Karşılaştırma Operatörleri



- Küçüktür "<"
- Büyüktür ">"
- Küçük veya eşittir "<="
- Büyük veya eşittir ">="
- Eşittir "="
- Eşit Değildir "<>"
- Eşit Değildir "!="

### **Mantıksal Operatörler**

Yukarıdaki kısımda WHERE anahtar kelimesi ve karşılaştırma operatörlerine değindik. Karşılaştırma operatörleri sayesinde koşulumuzu belirtebiliyoruz fakat birden fazla koşul belirtmemiz gerektiğinde ne yaparız?

Aşağıda böyle bir senaryoda kullanılan **AND**, **OR** ve **NOT** mantıksal operatörleri ile ilgili örnekler mevcuttur.

AND kullanımına bir örnek:

```sql
SELECT *
FROM actor
WHERE first_name = 'Penelope' AND last_name = 'Monroe;
```

Yukarıdaki kod actor tablosunda adı "Penelope" ve soyadı "Monroe" olan kayıtların tamamını listeler.

OR kullanımına bir örnek:

```sql
SELECT *
FROM actor
WHERE first_name = 'Penelope' OR first_name = 'Bob';
```

Yukarıdaki kod actor tablosunda adı "Penelope" olan veya adı "Bob" olan kayıtların tamamını listeler.

NOT kullanımına bir örnek:

```sql
SELECT *
FROM film
WHERE NOT rental_rate = 4.99;
```

Yukarıdaki kod film tablosunda rental_rate değeri 4.99 olmayan kayıtların tamamını listeler.

**Mantıksal Operatörleri Birlikte Kullanmak**

Aşağıdaki örnekte birden fazla mantıksal operatör birlikte kullanılmaktadır.

```sql
SELECT *
FROM film
WHERE NOT (rental_rate = 4.99 OR rental_rate = 2.99);
```

Yukarıdaki kod film tablosunda rental_rate değeri 4.99 veya 2.99 olmayan verileri çeker.



## BETWEEN Kullanımı

Aşağıda bir örnek verilmiştir. Bunun üzerinden anlatalım.

```sql
SELECT *
FROM film
WHERE length>90 AND length<120
```

Yukarıdaki kodda WHERE ile bir koşul belirttik. Koşulda length alanının değerinin 90'dan büyük ve 120'den küçük olması gerektiğini söyledik.

Bu koşulu BETWEEN operatörü kullanarak da yazabiliriz.

```sql
SELECT *
FROM film
WHERE length BETWEEN 90 AND 120
```

WHERE satırında length üzerinde çalıştığımızı belirttikten sonra BETWEEN kullanarak 90 ve 120 arasında olduğunu belirttik.

Örneği biraz karmaşık hale getirelim:

```sql
SELECT rental_rate, replacement_cost
FROM film
WHERE
(rental_rate BETWEEN 2 AND 4) 
AND
(replacement_cost BETWEEN 10 AND 20);
```

Yukarıdaki kodda film tablosundan rental_rate ve replacement_cost sütunlarını çektik. Koşul ise rental_rate değerinin 2 ile 4 arasında olması ve replacement_cost alanının 10 ile 20 arasında olması.

