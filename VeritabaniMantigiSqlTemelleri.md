##VERİTABANI MANTIĞI (SQL TEMELLERİ)

#Veritabanı Nedir?
Bir bilgisayar sisteminde elektronik olarak depolanan, yapılandırılmış bilgi veya veriden oluşan, içerisinde satır ve sütunlar barındıran tablolardan oluşan düzenli bir koleksiyondur. Yani veritabanları verileri belirli bir düzen içinde tutan ve bu düzen ile verilere daha etkili bir şekilde erişmeyi sağlayan yapılardır.

#Veritabanı Yönetim Sistemi Nedir? (DBMS)
Veritabanları, verileri düzen içinde tutmaya yararken, bu veriler üzerinde çalışma yapmamızı sağlayan yapı ise Veritabanı Yönetim Sistemi yani Database Management System (DBMS)’dir. Veri tabanı yönetim sistemleri verileri düzenlemeye, saklamaya, güncellemeye, erişmeye vb. işlemlere yardımcı olan yazılım veya sistemlerdir. Temel görevleri veritabanlarını etkili bir şekilde kullanmak için bir arayüz sağlamalarıdır.

#Relational Database Management System (RDBMS) Nedir?

-Verileri birbirleri ile organize olacak bir şekilde tutan ve veriye en hızlı en esnek şekilde ulaşmayı sağlayan sistemlerdir.

-İlişkisel veritabanlarında bulunan tablolar ve bu tablolarda bulunan veriler belli başlı bazı kurallara göre yapılandırılarak belirli bir düzen içerisinde tutulurlar. Bu düzen verilere erişim sağlamak isteyen kullanıcıya kolaylık sağlamaktadır.

-Bahsettiğimiz bu düzeni sağlayabilmek için kullanılan bazı anahtar türleri bulunmaktadır. Bu anahtar türleri veriler arasında bağlantı oluşturarak verilerin ilişkilendirilmesini sağlamaktadır. Sıkça kullanılan en temel anahtar kelimelerden bahsedecek olursak bunlar : Primary Key, Foreign Key ve Unique Key’dir.

->“PK” — Primary Key (Birincil Anahtar): 
Tablodaki her satırın eşsiz yani benzersiz olmasını sağlayan bir anahtardır. Bu anahtar sayesinde her bir yeni kayıt oluşturulduğunda bu kayıt benzersiz olacaktır. Primary key olarak işaretlenmiş bir alan NULL değer alamaz.

->“FK” — Foreign Key (Yabancı Anahtar): 
Yabancı anahtarlar bulunduğu tabloda, başka bir tablonun PK alanını tutar. Bu sayede diğer tablodaki PK alanına ait birden fazla kayıt oluşturulabilir ve oluşturulan bu kayıtların diğer tablodaki hangi alanla ilişkili olduğu tanımlanabilir. Yani FK kullanımı ile iki tablo arasında ilişki kurulabilir.

->“UK” —Unique Key (Benzersiz Anahtar): 
Benzersiz olarak işaretlenen alanlar sayesinde bir tabloya girilen bir kayıt birdaha girilemez. Yani bu anahtar her kaydın tabloda yalnızca bir kez tutulabilmesini sağlar bu sayede veri tekrarı engellenerek veri bütünlüğü sağlanmış olur. Benzersiz anahtar ile işaretlenen alanlar NULL değer alabilir.

#SELECT – JOIN – GROUP BY nedir?

SQL dünyasında verileri listelemek, farklı tablolardaki ilişkili bilgileri bir araya getirmek ve bu veriler üzerinde istatistiksel özetler çıkarmak için kullanılan en kritik üç yapı SELECT, JOIN ve GROUP BY komutlarıdır.

->SELECT Nedir? (Veri Seçme)

SELECT, bir veritabanı tablosundan veri çekmek (sorgulamak) için kullanılan temel komuttur. Hangi sütunları görmek istediğinizi (SELECT), hangi tablodan alacağınızı (FROM) ve isteğe bağlı olarak hangi koşullara göre filtreleyeceğinizi (WHERE) belirtirsiniz.

->JOIN Nedir? (Tabloları Birleştirme)

İlişkisel veritabanlarında veriler normalizasyon kuralları gereği farklı tablolara bölünür (örneğin müşteriler bir tabloda, siparişler başka bir tabloda tutulur). JOIN, bu ayrı tablolardaki verileri ortak bir anahtar (Primary Key - Foreign Key) üzerinden birbirine bağlayarak tek bir tabloymuş gibi sorgulamamızı sağlar. En yaygın türleri:

-INNER JOIN: Her iki tabloda da eşleşen kayıtları getirir.

-LEFT JOIN: Sol tablodaki tüm kayıtları, sağ tabloda eşleşenler varsa onları (yoksa NULL değerini) getirir.

-RIGHT JOIN: Sağ tablodaki tüm kayıtları ve sol tablodaki eşleşenleri getirir.

->GROUP BY Nedir? (Gruplama ve Özetleme)

GROUP BY, aynı değere sahip satırları bir araya getirerek gruplandırmak için kullanılır. Genellikle tek başına değil; COUNT(), SUM(), AVG(), MAX(), MIN() gibi toplulaştırma (aggregate) fonksiyonlarıyla birlikte çalışarak raporlama ve istatistik üretmek amacıyla kullanılır.

#Index Nedir?

Indeks, belirli bir veri ögesine hızlı erişim sağlamak amacıyla kullanılan yardımcı bir veri yapısıdır. Indeksler, büyük veri kümelerinde veri arama ve erişim süreçlerini hızlandırmak için kullanılır. Örneğin, bir kitapta indeks, belirli konuları veya terimleri hızlıca bulmamıza yardımcı olur. Benzer şekilde, bir veritabanında indeksler, belirli kayıtların hızla bulunmasını sağlar.

#Indeks Çeşitleri

->Veritabanı Indeksleri

Veritabanı indeksleri, ilişkisel veritabanı yönetim sistemlerinde (RDBMS) yaygın olarak kullanılır. Bu indeksler, bir tablodaki verilerin hızlı bir şekilde aranmasını ve sıralanmasını sağlar. Veritabanı indeksleri genellikle ağaç yapıları veya hash tablosu yapıları kullanılarak oluşturulur. Indeksler, veri arama süreçlerini hızlandırırken, aynı zamanda veri ekleme, güncelleme ve silme işlemlerini de etkileyebilir.İşte, Veritabanı sistemlerinde sıkça kullanılan ve veri arama işlemlerini optimize etmek için tasarlanmış indeks türleri:

-B-Tree Indeksleri: 
En yaygın kullanılan indeks türüdür. B-Tree indeksleri, verileri dengeli bir ağaç yapısında saklar ve bu sayede veri arama işlemlerini hızlı ve verimli hale getirir.

-Hash Indeksleri: 
Hash tablosu yapısını kullanarak verilerin hızlıca bulunmasını sağlar. Hash indeksleri, genellikle eşitlik karşılaştırmalarında (örneğin, belirli bir anahtara sahip kayıtları bulma) kullanılır.

->Ters Indeks (Inverted Index)

Ters indeks, metin tabanlı arama motorlarında ve bilgi erişim sistemlerinde yaygın olarak kullanılır. Bu indeks türü, bir belge koleksiyonunda kelimelerin veya terimlerin hangi belgelerde geçtiğini hızlıca bulmamıza olanak tanır. Örneğin, bir arama motoru, belirli bir kelimenin geçtiği tüm web sayfalarını bulmak için ters indeks kullanır.

->Multidimensional Indeksler

Multidimensional indeksler, coğrafi bilgi sistemleri (GIS) ve büyük veri uygulamalarında kullanılır. Bu indeksler, çok boyutlu verilerin (örneğin, coğrafi koordinatlar) hızlı bir şekilde aranmasını sağlar. R-Tree ve KD-Tree gibi yapılandırmalar, bu tür indekslere örnek olarak verilebilir.

#Indekslerin Kullanım Alanları

-Veritabanı Yönetimi
Veritabanı sistemlerinde, indeksler performansı artırmak için kritik öneme sahiptir. Büyük veri tabanlarında, indeksler olmadan veri arama ve erişim işlemleri çok yavaş olabilir. Indeksler, belirli sütunlar üzerinde oluşturularak, SQL sorgularının daha hızlı çalışmasını sağlar.

-Arama Motorları
Arama motorları, web sayfalarında geçen kelimeleri ve terimleri hızlıca bulmak için ters indeksleri kullanır. Ters indeksler, belirli bir anahtar kelimenin geçtiği tüm belgeleri veya web sayfalarını hızlıca listeleyerek kullanıcıya en ilgili sonuçları sunar.

-Veri Analitiği
Büyük veri analitiği ve veri madenciliği uygulamalarında indeksler, büyük veri kümeleri üzerinde hızlı analizler yapmayı sağlar. Indeksler, veri kümelerinin belirli özelliklerine göre düzenlenmiş yapılar olduğundan, analizlerin ve sorguların hızlı ve verimli bir şekilde gerçekleştirilmesini mümkün kılar.

-Dosya Sistemleri
Indeksler, dosya sistemlerinde de önemli bir rol oynar. Dosya sistemleri, dosyaların ve dizinlerin hızlı bir şekilde bulunmasını sağlamak için indeks yapıları kullanır. Bu, dosya erişim sürelerini kısaltır ve genel sistem performansını artırır.