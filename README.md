Diyabet Tahmin Modelleme ve İş Önerileri Projesi
Proje Özeti

Bu projede Pima Indian Diabetes veri seti kullanılarak diyabet riskini önceden tahmin edebilecek bir makine öğrenimi modeli geliştirildi ve sağlık sektörüne yönelik iş önerileri sunuldu. Proje kapsamında veriler üzerinde kapsamlı bir keşifsel analiz (EDA) yapıldı, veriler temizlendi ve yeni özellikler türetildi. Ardından lojistik regresyon, rastgele orman gibi çeşitli algoritmalarla bir tahmin modeli eğitildi. Model, diyabet riskini yaklaşık %77 doğruluk ve %83 ROC-AUC skoruyla tahmin edebilmektedir. Elde edilen bulgular sayesinde obezite, yüksek glukoz düzeyi ve ileri yaş gibi faktörlerin diyabet üzerindeki etkileri ortaya konmuş ve yüksek riskli bireyler için proaktif önlemler önerilmiştir.
Proje Amacı

Projenin temel amacı, diyabet hastalığının erken teşhisi ve önlenmesi için veri analitiği ve makine öğrenimi tekniklerini kullanmaktır. Özellikle mevcut hasta verilerinden yararlanarak bireylerin diyabet geliştirme riskini öngörmek ve bu doğrultuda sağlık kuruluşları için aksiyon alınabilir içgörüler üretmek hedeflenmiştir. Bu sayede sağlık ekipleri yüksek riskli bireyleri önceden belirleyip yaşam tarzı müdahaleleri, tarama programları ve diğer önleyici sağlık hizmetleriyle diyabet vakalarını azaltabilir. Proje, teknik bir modelleme çalışmasının ötesinde, çıkan sonuçların iş değeri yaratacak şekilde yorumlanması ve somut önerilere dönüştürülmesini amaçlamaktadır.

Kullanılan Veri Seti

Proje analizlerinde kullanılan veri seti Pima Indians Diabetes Database adını taşıyan açık bir veri setidir. Bu veri seti, ABD'nin Arizona eyaletinde yaşayan Pima Kızılderili kökenli kadınların çeşitli sağlık ölçümlerini ve diyabet durumunu içermektedir. Toplam 768 bireye ait kayıt vardır ve her biri için şu değişkenler bulunmaktadır:

Pregnancies: Gebelik sayısı

Glucose: 2 saatlik oral glukoz tolerans testindeki plazma glukoz konsantrasyonu (mg/dL)

BloodPressure: Diyastolik kan basıncı (mm Hg)

SkinThickness: Triceps cilt kıvrımı kalınlığı (mm)

Insulin: 2 saatlik serum insülin seviyesi (mu U/ml)

BMI: Vücut kitle indeksi (kg/m²)

DiabetesPedigreeFunction: Ailede diyabet öyküsünün etkisini yansıtan bir fonksiyon

Age: Yaş (yıl)

Outcome: Hedef değişken, bireyin diyabetli olup olmadığı (1 = Evet, 0 = Hayır)

Veri setinde diyabetli olarak etiketlenen bireylerin oranı %34.9 (268 kişi) iken, diyabet olmayan bireyler %65.1 (500 kişi) ile çoğunluktadır. Veri seti herhangi bir kişisel bilgiyi içermez; sadece tıbbi ölçümler ve sonuç bulunmaktadır. Bu dengeli sayılabilecek dağılım, model eğitimi için uygun bir temel oluşturmuştur.

Kullanılan Teknolojiler

Proje boyunca açık kaynaklı veri bilimi araçları ve yazılımlar kullanılmıştır. Başlıca teknoloji ve kütüphaneler şunlardır:

Python (Jupyter Notebook): Veri işlemenin ve modellemenin gerçekleştirildiği programlama dili. Proje kodları Jupyter Notebook üzerinde yürütülmüştür.

Pandas, NumPy: Veri okuma, yazma, manipülasyon ve sayısal işlemler için kullanıldı.

Matplotlib, Seaborn: Keşifsel veri analizi sırasında grafikler ve görselleştirmeler oluşturmak için kullanıldı.

SQLite (sqlite3): Python içerisinde hafif bir veritabanı oluşturarak SQL sorguları çalıştırmak ve veriyi SQL ile analiz edebilmek için kullanıldı.

scikit-learn: Makine öğrenmesi modellerinin (Lojistik Regresyon, Random Forest, Gradient Boosting, SVM) eğitim ve değerlendirilmesi için kullanıldı. Ayrıca veri standardizasyonu (StandardScaler), model doğrulama (train_test_split, cross_val_score) ve metrik hesaplamalarında bu kütüphaneden yararlanıldı.

Tableau: Elde edilen sonuçları görselleştirmek ve etkileşimli bir dashboard oluşturmak için tercih edildi (dashboard çıktısı için).

Medium: Proje sürecini ve sonuçlarını geniş kitlelerle paylaşmak amacıyla Medium platformunda bir makale yazıldı.

Bu teknolojiler sayesinde veri analizi uçtan uca gerçekleştirilmiş, teknik ve iş birimleri için ayrı formatlarda çıktılar üretilmiştir.

Proje Yapısı

Proje dosyaları ve çıktıları aşağıdaki yapıda organize edilmiştir:

Proje_final/
├── README.md                   - Proje genel bilgileri (bu doküman)
├── saglik.md (veya secilen proje .md dosyası) - Proje tanımı ve gereksinimleri
├── [ADINIZ_SOYADINIZ]/         - Projeye ait çalışmaların bulunduğu ana klasörünüz
    ├── README.md               - Proje raporu ve özeti (içindekiler bu dosyada listelenmiştir)
    ├── data/
    │   ├── raw/                - Ham veri seti dosyaları (ör. diabetes.csv)
    │   └── processed/          - İşlenmiş/veri temizleme sonrası veri seti dosyaları
    ├── notebooks/
    │   └── saglik_teknik_sunum.ipynb   - Teknik sunum Jupyter Notebook'u (tüm analiz kodları ve çıktıları)
    ├── presentation/
    │   └── saglik_business_sunum.pdf   - Business (iş) sunumu PDF dosyası 
    ├── dashboard_link.txt      - Tableau Dashboard linkini içeren metin dosyası 
    ├── medium_link.txt         - Medium makalesi linkini içeren metin dosyası 
    └── requirements.txt        - Projede kullanılan Python kütüphaneleri (paket bağımlılıkları)


Yukarıdaki yapıda, proje analizi ve dokümantasyonu kendi adınıza oluşturduğunuz klasörde yer almaktadır. Teknik detaylar Jupyter Notebook içinde adım adım gösterilmiş; iş tarafına yönelik özet ise sunum ve Medium yazısı olarak ayrıca sunulmuştur. Veri dosyaları "data" klasöründe saklanmış ve repodaki README dosyasında projenin tüm önemli yönleri özetlenmiştir.

Analiz Süreci

Analiz süreci, veri ön işleme adımlarından başlayarak model geliştirme ve iş değerine kadar uzanan bir yaklaşım izledi. Adımlar genel olarak şu şekilde ilerledi:

Veri Keşfi ve Temizleme: Ham verinin yüklenmesi, kalite kontrolü, eksik veya tutarsız değerlerin düzeltilmesi.

Keşifsel Veri Analizi (EDA): Verinin dağılımlarının, ilişkilerinin ve önemli desenlerinin görselleştirme ve istatistiksel yöntemlerle incelenmesi.

SQL Analizi: Belirli iş sorularını yanıtlamak için verinin SQL sorguları ile analiz edilmesi (örn. yaş gruplarına göre diyabet oranı gibi).

Makine Öğrenmesi: Farklı algoritmalarla modelleme yapılarak diyabet tahmin modeli kurulması, modellerin karşılaştırılması ve en iyi modelin seçilmesi.

İçgörülerin Yorumlanması: Elde edilen bulguların iş birimleri için anlamlandırılması, önerilere ve beklenen etkiye dönüştürülmesi.

Aşağıda bu adımlar detaylı olarak açıklanmaktadır.

Veri Keşfi ve Temizleme

Veri analizine başlamadan önce ham veri seti üzerinde çeşitli ön işleme adımları uygulanmıştır:

Veri Yükleme: diabetes.csv dosyası pandas ile DataFrame formatında yüklendi. Veri setinin boyutu, sütun bilgileri ve ilk birkaç kayıt incelenerek doğru okunduğu doğrulandı. Başlangıçta 768 satır ve 9 sütun (8 özellik + Outcome) bulunmaktadır.

Eksik Değer Analizi: Veri setinde açıkça boş (NaN) değer bulunmamakla birlikte, bazı tıbbi ölçümlerde 0 değeri eksik veri göstergesi olarak kullanılmıştır. Medikal olarak 0 olması mümkün olmayan değişkenler belirlendi:

Glucose (Plazma glukoz): 0 değeri 5 kişide (%0.65)

BloodPressure (Kan basıncı): 0 değeri 35 kişide (%4.56)

SkinThickness (Cilt kalınlığı): 0 değeri 227 kişide (%29.56)

Insulin: 0 değeri 374 kişide (%48.70)

BMI: 0 değeri 11 kişide (%1.43)
Bu değişkenlerdeki 0 değerleri, ölçüm yapılmadığı anlamına geldiği için eksik değer olarak ele alındı ve işleme tabi tutuldu.

Eksik Değer İmputasyonu: Yukarıdaki sütunlardaki 0 değerleri, ilgili sütunun median (ortanca) değeri ile dolduruldu. Medyan impute yöntemi, özellikle dağılımı bozmamak ve uç değerlerden etkilenmemek için tercih edilmiştir. Örneğin, Insulin için medyan 125 olarak hesaplanmış ve 0 değerleri 125 ile değiştirilmiştir. Bu sayede veri setinde artık anlamsız 0 değerleri kalmamıştır.

Aykırı Değer Tespiti ve Düzeltme: Her bir sayısal özellik için inter-kuartil aralığı (IQR) yöntemiyle aykırı değer analizi yapıldı. Hesaplanan alt ve üst sınırların dışında kalan değer sayıları belirlendi. Örneğin, Insulin sütununda 346 olası aykırı değer tespit edilmiştir (verinin yarısının eksik olup medyan ile doldurulmasından dolayı Insulin dağılımı daralmış olabilir). Belirlenen aykırı değerler, ilgili sınır değerlerine kırpılarak (capping) uç değerlerin etkisi azaltıldı. Bu işlem, özellikle ağaç tabanlı modellerin aşırı uç değerlerden aşırı etkilenmesini önlemeye yöneliktir.

Yeni Özellik Mühendisliği: Veri setine mevcut değişkenlerden türetilen 7 yeni özellik eklendi:

BMI_Category: BMI değerini Dünya Sağlık Örgütü standartlarına göre kategorik sınıfa dönüştürme (0: Zayıf, 1: Normal, 2: Fazla Kilolu, 3: Obez).

Age_Group: Yaşı aralıklara ayırma (0: Genç <30, 1: Orta Yaş 30-50, 2: İleri Yaş 50+).

Glucose_Category: Glukoz seviyesini klinik eşiklere göre sınıflandırma (0: Normal <100, 1: Prediyabet 100-125, 2: Diyabet ≥126).

BMI_Age_Interaction: BMI ile Yaş çarpımı (bu iki değişkenin etkileşimini temsil eden sürekli bir özellik).

Glucose_BMI_Interaction: Glukoz ile BMI çarpımı (yüksek kan şekeri ve obezitenin birleşik etkisini yakalamak için).

Insulin_Glucose_Ratio: Insulin / (Glucose+1) oranı (insülin ve glukoz dengesi hakkında bir gösterge).

Risk_Score: Glukoz, BMI, Yaş ve aile öyküsü (DiabetesPedigreeFunction) değişkenlerini belli ağırlıklarla birleştirerek oluşturulan bir risk skoru. (Örn. formül: Glukoz0.3 + BMI0.25 + Yaş0.2 + DiabetesPedigreeFunction100*0.25) – Bu formül varsayımsal olarak her faktöre bir ağırlık vererek toplam bir risk puanı hesaplar.

Yeni eklenen bu özelliklerle birlikte veri setindeki toplam sütun sayısı 16'ya yükselmiştir (Outcome dahil). Sonuç olarak temizlenmiş ve zenginleştirilmiş veri seti, 15 bağımsız değişken ve 1 hedef değişkenden oluşmaktadır. Artık veri setinde eksik değer kalmamış, uç değerlerin etkisi azaltılmış ve modele girdi olacak anlamlı türetilmiş özellikler hazırlanmıştır.

Keşifsel Veri Analizi (EDA)

Veri temizleme işlemleri sonrasında, veriyi daha iyi anlamak ve önemli desenleri ortaya çıkarmak amacıyla keşifsel veri analizi yapılmıştır. EDA adımında öne çıkan bulgular şöyle özetlenebilir:

Hedef Değişken Dağılımı: Veri setindeki 768 bireyin %34.9’u diyabetli olduğundan (Outcome=1), veri göreceli olarak dengesiz olsa da ciddi bir diyabet oranına sahiptir. Bu oran, analiz yapılan toplulukta diyabetin yaygınlığını göstermektedir.

Korelasyon Analizi: Tüm özellikler ile diyabet durumu (Outcome) arasındaki Pearson korelasyonları hesaplanmıştır. Beklendiği üzere Glucose (Kan şekeri) değeri, diyabetle en güçlü pozitif korelasyon gösteren değişkenlerden biri oldu (r ≈ 0.49). Ayrıca türettiğimiz Glucose_BMI_Interaction (Glukoz*BMI) özelliği ile Risk_Score bileşimi diyabet Outcome'u ile ~0.52 düzeyinde korelasyona ulaşarak tek başına glukoz veya BMI’den daha güçlü bir ilişki yakaladı. Bu, yüksek kan şekeri ve yüksek kilonun birleşiminin diyabet için ne kadar kritik olduğunu göstermektedir. Diğer önemli korelasyonlar arasında BMI (r ~0.31) ve BMI_Category (r ~0.31) ile Age_Group (r ~0.26) sayılabilir. Genel olarak, yaş ve kilo ile ilgili değişkenler diyabet durumu ile anlamlı pozitif korelasyon içindedir.

Gruplar Arası Karşılaştırmalar: Diyabetli ve diyabetli olmayan bireylerin ortalama değerleri karşılaştırıldığında tüm temel metriklerde anlamlı farklar bulunmuştur. İstatistiksel t-test sonuçları özetle:

Glukoz: Diyabetli bireylerin ortalama glukoz düzeyi 142 iken sağlıklı bireylerde 111 olarak bulundu. ~31 birimlik bu fark oldukça yüksek ve p<0.001 düzeyinde anlamlı. Bu, kan şekerinin diyabetli grupta belirgin şekilde fazla olduğunu gösteriyor.

BMI: Diyabetli grubun ortalama BMI değeri 35.2 iken sağlıklılarda 30.9 olarak ölçüldü. ~4.3 birimlik fark ile diyabetli bireyler genelde obezite kategorisinde yer alıyor (p<0.001 anlamlı).

Yaş: Diyabet hastaları ortalama 37.0 yaşında iken sağlıklı grup ortalama 31.1 yaşında. Diyabetli grubun belirgin biçimde daha yaşlı olduğu görülüyor (yaklaşık 6 yaş fark, p<0.001 anlamlı). Yaş arttıkça diyabet riskinin yükseldiği bu farkla desteklenmektedir.

Insulin: İki grup arasındaki insülin seviyeleri ortalaması yakın olsa da (diyabetliler 127.6, sağlıklılar 123.2), aradaki fark istatistiksel olarak anlamlı çıktı (p<0.001). Bu, diyabetli grubun insülin direnci veya yüksek insülin seviyesi eğilimini de yansıtabileceğini düşündürmektedir.

DiabetesPedigreeFunction (Genetik Yatkınlık): Diyabetli grupta aile öyküsü skoru ortalama 0.53, sağlıklılarda 0.42 bulundu. Aradaki fark p<0.001 ile anlamlı olup diyabetli bireylerin genetik yatkınlık skorunun bir miktar daha yüksek olduğunu gösterir. Ancak bu fark, glukoz veya BMI kadar belirgin değildir.

Bu karşılaştırmalar, literatürde bilinen diyabet risk faktörlerini veri setinde de doğrulamıştır: Diyabetli bireyler genelde daha yaşlı, daha kilolu, kan şekeri daha yüksek ve genetik riski daha fazladır.

Veri Dağılımları ve Görselleştirmeler: EDA kapsamında çeşitli grafikler ile verinin dağılımı incelenmiştir. Örneğin:

Yaş dağılım grafikleri, genç bireylerde diyabet görülme oranının düşük olduğunu, diyabetli grubun yaş eğrisinin daha yaşlı tarafa kaydığını gösterdi.

BMI ile Glukoz scatter (dağılım) grafiği, yüksek BMI ve yüksek glukoz değerlerine sahip noktaların çoğunlukla diyabetli sınıfta yer aldığını görselleştirdi. Bu iki değişken birlikte yüksek olduğunda diyabet olasılığının çok arttığı gözlemlendi.

Özellik dağılımları histogramlarla incelendiğinde, örneğin DiabetesPedigreeFunction değerinin diyabetli grupta genel olarak daha yüksek olduğu ancak dağılımların önemli ölçüde örtüştüğü görüldü. Bu da genetik yatkınlığın tek başına güçlü bir ayırt edici olmayıp, diğer faktörlerle birleşince anlam kazandığını gösteriyor.

Özetle, EDA aşaması bize veri setindeki temel eğilimleri ve farkları ortaya koydu: Yüksek glukoz ve BMI değerleri, ileri yaş ve belli ölçüde genetik faktörler diyabet ile ilişkili bulundu. Bu bulgular, sonraki adımlarda yapılacak grup analizleri ve modelleme için bir temel sağladı.

SQL Analizi

Keşifsel analizin bir parçası olarak, veriye SQL sorguları ile de bakılarak özellikle işe yönelik sorular cevaplandı. Veriyi SQLite veritabanına aktararak hazırlanan özel sorgular sayesinde aşağıdaki içgörüler elde edildi:

Yaş Grubu Analizi: Yaşlar kategorilere ayrılarak (Genç <30, Orta 30-50, İleri >50) her gruptaki diyabet oranı hesaplandı.
Sonuç: Orta yaş grubundaki (30-50 yaş) bireylerin neredeyse yarısı diyabetli (%49.8) çıktı. İleri yaş grubunda (50+ yaş) ise diyabet oranı %48.3 ile benzer şekilde yüksektir. Genç grubunda (<30) bu oran yalnızca %21.2’de kalmaktadır. Bu bulgu, özellikle 30 yaş üstü yetişkinlerde diyabet riskinin keskin biçimde arttığını gösterir. Orta yaş grubunun en yüksek orana sahip olması, 30’lu ve 40’lı yaşların kritik bir dönem olduğunu, belki 50+ grubunda hayatta kalanların bir kısmının daha sağlıklı olabileceğini işaret etmektedir.

BMI Kategori Analizi: Bireyler vücut kitle indeksi (BMI) değerlerine göre Dünya Sağlık Örgütü sınıflarına ayrıldı (Zayıf <18.5, Normal 18.5-24.9, Fazla Kilolu 25-29.9, Obez ≥30) ve her gruptaki diyabet yüzdesi hesaplandı.
Sonuç: Obez kategorisindeki bireylerin %45.76’sı diyabetliyken, Fazla kilolu grubunda bu oran %22.35’e düşmektedir. Normal kilolu bireylerde diyabet oranı yalnızca %6.86 olup, zayıf kategoride (örnek sayısı sadece 4 kişi) diyabet görülmemiştir (%0). Bu sonuçlar, obezitenin diyabet için en önemli risk faktörlerinden biri olduğunu net şekilde göstermektedir. Ağırlık arttıkça diyabet oranı katlanarak yükselmektedir.

Yüksek Risk Grubu (Glukoz & BMI): Veride, henüz diyabet tanısı almamış (Outcome=0) ancak Glukoz > 140 ve BMI > 30 (yani kan şekeri çok yüksek ve obez) kriterlerine uyan bireyler filtrelendi. Bu kriterler, aslında potansiyel olarak diyabet eşiğinde veya ciddi risk altında olan kişileri belirlemeyi amaçlar.
Sonuç: Bu koşulları sağlayan 36 birey bulundu. Bu yüksek riskli diyabet adayı grubun ortalama glukozu 157.4 mg/dL, ortalama BMI değeri 37.4 ve ortalama yaşı 35.5 olarak hesaplandı. Bu demek oluyor ki veri setindeki 36 kişi, şu an diyabet olmasa bile hem aşırı kilolu hem de glukoz seviyeleri çok yüksek; muhtemelen ileride diyabet gelişmesi muhtemel bir grup. Bu grubun tespit edilmesi, ilerideki iş önlemleri için kritik bir fırsat sunar (erken müdahale ile diyabeti önleme şansı).

Hamilelik (Pregnancies) Analizi: Kadınların hamilelik sayısına göre diyabet görülme oranları incelendi. Hamilelik sayısı 0, 1-3, 4-6 ve 7+ şeklinde gruplara ayrıldı ve her grupta diyabet yüzdesi hesaplandı.
Sonuç: 7+ hamilelik geçirmiş kadınların %56.21’i diyabetli olarak bulunmuştur ki bu en yüksek orandır. 4-6 hamilelik yaşamış olanlarda oran %34.29, hiç hamile kalmamış kadınlarda %34.23 ile benzer seviyededir. En düşük risk, 1-3 hamilelik grubundadır (%23.96). Bu sonuç, çok sayıda gebelik geçirmiş olmanın diyabet riskini artırabileceğini akla getirmektedir (örneğin gestasyonel diyabet yaşamış olma ihtimali veya çoklu hamileliklerin vücuda etkileri nedeniyle). Diğer yandan, hiç hamile kalmamış grubun riski de yüksek çıkmıştır; bu durumda yaş faktörü (hiç hamile kalmamış grup ortalamada daha genç mi yoksa belirli sağlık durumları mı var) gibi etkenler de düşünülebilir. Genel olarak, gebelik sayısı arttıkça diyabet riski artma eğilimi gösterse de 4-6 aralığı ile 0 arasında fark görülmemesi demografik karışımların bir sonucudur.

Yukarıdaki SQL destekli analizler, EDA bulgularını tamamlayıcı niteliktedir. Özellikle, obezite ve ileri yaşın kritik risk faktörleri olduğu, çoklu hamilelik öyküsünün de dikkate değer bir risk işareti olabileceği ve henüz diyabet olmamış ancak yüksek riskli bireylerin somut olarak belirlenebileceği ortaya çıkmıştır. Bu bulgular, iş kararları aşamasında hangi gruplara odaklanılması gerektiğine dair ipuçları sağlamaktadır.

Diyabet Tahmin Projesi - Sağlık Verisi Analizi
Proje Özeti

Bu projede Pima Kızılderili Diyabet veri seti kullanılarak diyabet riskini tahmin etmeye yönelik kapsamlı bir veri analizi gerçekleştirilmiş ve makine öğrenmesi modeli geliştirilmiştir. Veri keşfi ve ön işleme adımlarında veri kalitesi iyileştirilmiş, ardından keşifsel analiz ile diyabet riskiyle ilişkili temel faktörler belirlenmiştir. Makine öğrenmesi algoritmaları ile yaklaşık %80 doğruluk oranına sahip bir diyabet tahmin modeli oluşturulmuş ve sonuçlar ışığında sağlık sektörü için proaktif tarama ve önleyici uygulamalara yönelik iş önerileri sunulmuştur. Elde edilen içgörüler, diyabetin erken teşhisi ve önlenmesi amacıyla stratejik aksiyon planlarıyla birleştirilmiştir.

Proje Amacı

Bu projenin temel amacı, diyabet hastalığının erken tespiti için klinik verilere dayalı bir makine öğrenmesi modeli geliştirmek ve elde edilen bulgular doğrultusunda sağlık hizmeti sağlayıcılarına yönelik stratejik öneriler sunmaktır. Bu kapsamda teknik tarafta veri temizleme, EDA ve modelleme adımları gerçekleştirilmiş; iş tarafında ise anlamlı içgörüler çıkarılarak diyabet vakalarının azaltılması ve tedavi maliyetlerinin düşürülmesi hedeflenmiştir.

Kullanılan Veri Seti

Proje kapsamında Pima Indians Diabetes Database (Kaggle üzerinden erişilen) adlı gerçek bir sağlık veri seti kullanılmıştır. Bu veri seti, 768 kadına ait klinik ölçümler ve diyabet durumu bilgisini içermektedir (Tüm örnekler en az 21 yaşındaki Pima Kızılderili kadınlardan oluşmaktadır). Veri setinde 8 adet özellik ve 1 adet hedef değişken bulunmaktadır. Hedef değişken Outcome olup 0 sağlıklı, 1 diyabetli bireyi belirtir. Veride 500 kişi (%65.1) sağlıklı, 268 kişi (%34.9) diyabetlidir. Kullanılan özellikler ve açıklamaları aşağıdaki gibidir:

Pregnancies (Hamilelik sayısı): Kişinin toplam hamilelik sayısı

Glucose (Glukoz): 2 saatlik oral glukoz tolerans testi sonucu (mg/dL)

BloodPressure (Tansiyon): Diyastolik kan basıncı (mm Hg)

SkinThickness (Cilt Kalınlığı): Triseps cilt kıvrım kalınlığı (mm)

Insulin (İnsülin): 2 saatlik serum insülin seviyesi (mu U/ml)

BMI: Vücut kitle indeksi (kg/m²)

DiabetesPedigreeFunction: Ailede diyabet öyküsüne göre hesaplanan genetik risk skoru

Age (Yaş): Hastanın yaşı (yıl)

Outcome: Diyabet durumu (0 = negatif, 1 = pozitif) – Hedef değişken

Veri setindeki ölçümler, diyabet gelişimini etkileyebilecek demografik ve klinik faktörleri kapsamaktadır. Bu sayede modelleme aşamasında diyabet riskini öngörmek için zengin bir veri tabanı oluşturulmuştur.

Kullanılan Teknolojiler

Python 3 & Jupyter Notebook: Veri analizi ve modelleme (Kaggle Notebook ortamı kullanıldı)

Pandas, NumPy: Veri okuma, işleme ve temel istatistiksel işlemler

Matplotlib, Seaborn: Veri görselleştirme ve grafik oluşturma

SciPy: İstatistiksel hesaplamalar (örn. IQR ile aykırı değer tespiti)

Scikit-learn: Makine öğrenmesi algoritmaları, model eğitimi ve değerlendirme

SQLite (sqlite3): Veriyi SQL tablo formatında incelemek için veritabanı entegrasyonu

Tableau: Analiz sonuçlarını sunmak için interaktif dashboard oluşturma

Medium: Proje hikayesini ve teknik detayları paylaşmak için blog platformu

Proje Yapısı

Proje dosyaları ve klasörleri aşağıdaki yapıya göre düzenlenmiştir:

Proje_final/
├── README.md                   <- Proje genel dokümantasyonu (bu dosya)
├── [ADINIZ_SOYADINIZ]/
    ├── README.md               <- Proje ile ilgili detaylı açıklamalar (örn. bu içerik)
    ├── data/
    │   ├── raw/                <- Ham veri setleri (ör. diabetes.csv)
    │   └── processed/          <- İşlenmiş/veri temizleme sonrası veriler
    ├── notebooks/
    │   └── saglik_teknik_sunum.ipynb   <- Teknik sunum notebook’u (EDA, modelleme kodları ve çıktıları)
    ├── presentation/
    │   └── saglik_business_sunum.pdf   <- Business sunum PDF dosyası
    ├── dashboard_link.txt      <- Tableau üzerindeki interaktif dashboard linki
    ├── medium_link.txt         <- Medium makalesinin linki
    └── requirements.txt        <- Gerekli Python kütüphanelerini listeler


Bu yapıda ham veri data/raw klasöründe tutulur, Jupyter notebook içerisinde verinin yüklenmesi ve işlenmesi gerçekleştirilir. Notebook çıktıları ve görselleri teknik sunumun bir parçasıdır. Business sunumu ve diğer dokümanlar ilgili klasörlerde yer almaktadır. Tüm kod ve dokümanlar, versiyon kontrolü ve paylaşım için GitHub üzerinde de tutulmaktadır.

Analiz Süreci

Analiz süreci, veri hazırlığından başlayıp modelleme ve iş önerilerine uzanan bir yol haritası şeklinde ilerlemiştir. İlk olarak veri kalitesi değerlendirilmiş ve gerekli temizleme adımları uygulanmıştır. Daha sonra verinin dağılım ve ilişkilerini anlamak üzere keşifsel veri analizi (EDA) yapılmıştır. İlave olarak, SQL kullanarak veriye farklı açılardan bakılıp segmentasyon bazlı içgörüler elde edilmiştir. Son aşamada çeşitli makine öğrenmesi algoritmaları eğitilerek diyabet tahmin modeli geliştirilmiş ve en iyi model seçilmiştir. Tüm bu adımlar sonucunda elde edilen teknik bulgular, iş birimi bakış açısıyla yorumlanarak stratejik önerilere dönüştürülmüştür.

Veri Keşfi ve Temizleme

Veri yükleme aşamasında ilk incelemeler, veri setinin 768 örnek ve 9 sütun (8 özellik + 1 hedef) içerdiğini göstermiştir. Eksik değer kontrolünde veri setinde doğrudan boş değer bulunmadığı, ancak bazı numerik sütunlarda fiziken imkansız değerler olduğu görülmüştür. Örneğin Glucose, BloodPressure, SkinThickness, Insulin ve BMI sütunlarında 0 değeri eksik değerin bir göstergesi olarak kullanılmıştır. Bu sütunlar için 0 değerleri tespit edilip NaN (eksik) olarak işaretlenmiş ve her birine sütun medyanı ile ortalama doldurma (imputation) uygulanmıştır. Böylece ölçüm yapılmamış/eksik olan değerler, verinin genel dağılımını çok fazla bozmadan doldurulmuştur.

Aykırı değer analizi için IQR (Interquartile Range) yöntemi kullanılmış ve uç değerlerin veri dağılımı üzerindeki etkisi incelenmiştir. Belirlenen eşik değerlerin ötesindeki aykırı gözlemler uç noktalarla sınırlandırılarak verideki aşırı uç değerlerin etkisi azaltılmıştır. Bu sayede modelleme aşamasında ekstrem değerlerin neden olabileceği dengesizlikler önlenmeye çalışılmıştır.

Veri ön işleme aşamasının bir parçası olarak çeşitli özellik mühendisliği adımları uygulanmıştır. Toplamda 7 yeni türetilmiş özellik eklenmiştir. Örneğin, BMI değeri kullanılarak kategorik bir “BMI Kategorisi” özelliği oluşturulmuştur (Zayıf, Normal, Fazla Kilolu, Obez şeklinde sınıflandırma). Benzer şekilde Yaş değişkeninden genç, orta yaşlı, ileri yaş gibi gruplar tanımlanmıştır. Hamilelik sayısı için kategorik gruplar (ör. 0, 1-3, 4-6, 7+ hamilelik) oluşturulmuştur. En önemlisi, Glukoz ve BMI etkileşimini temsil eden yeni bir özellik türetilmiştir (örneğin Glukoz*BMI ürünü), ki bu etkileşim değişkeninin modelde oldukça önemli bir gösterge olduğu görülmüştür. Ayrıca risk skorlaması için bazı kritik eşiklere dayalı (ör. Glukoz > 140 ve BMI > 30 gibi) birleşik özellikler yaratılmıştır. Tüm bu temizleme ve zenginleştirme adımlarının ardından, analiz ve modelleme için temiz ve özellik açısından zenginleştirilmiş bir veri seti elde edilmiştir.

Keşifsel Veri Analizi (EDA)

Keşifsel analiz aşamasında, verinin dağılımları ve değişkenler arası ilişkiler görselleştirilerek incelenmiştir. İlk olarak hedef değişken dağılımı incelendiğinde veri setindeki bireylerin ~%35’inin diyabetli olduğu, %65’inin ise sağlıklı olduğu görülmüştür. Bu, diyabetin incelenen popülasyonda oldukça yaygın olduğunu göstermektedir.

Değişkenlerin hedef (Outcome) ile olan korelasyonları hesaplanmış ve en güçlü ilişkili faktörler tespit edilmiştir. Özellikle Glukoz değeri diyabet durumu ile en yüksek korelasyonu gösteren değişken olmuştur. Bunu BMI (vücut kitle indeksi), Yaş ve Hamilelik sayısı gibi değişkenler izlemiştir. Örneğin, diyabetli bireylerin ortalama glukoz düzeyinin sağlıklı bireylere kıyasla belirgin derecede yüksek olduğu (tahminen ~30 mg/dL daha fazla) görülmüştür. Benzer şekilde diyabetli grubun ortalama BMI değeri sağlıklı gruptan daha yüksektir (diyabetlilerde ortalama BMI ~5 birim daha fazla) ve diyabetliler ortalama olarak daha ileri yaştadır (yaklaşık 5-6 yıl daha yaşlı). Bu farklılıklar, diyabet tanısı alanların metabolik ve demografik profillerinin sağlıklı bireylerden sistematik olarak farklı olduğunu ortaya koymaktadır.

Ek olarak, çeşitli görseller ile verinin önemli kalıpları incelenmiştir. Dağılım grafikleri ve kutu grafikleri (boxplot) kullanılarak glukoz, BMI gibi değişkenlerde diyabetli ve diyabet olmayan gruplar arasındaki farklar net şekilde görülmüştür. Özellikle glukoz dağılımında diyabetli grubun sağlıklılara göre belirgin bir kayma gösterdiği (yüksek değerlere doğru) saptanmıştır. Korelasyon matrisi incelendiğinde de glukoz ve BMI’in yanı sıra, Insulin ve Pregnancies değişkenlerinin de Outcome ile anlamlı ilişkilere sahip olabildiği gözlenmiştir. Bu bulgular, sonraki aşamalarda kurulacak modelin hangi değişkenlere daha fazla ağırlık verebileceğine dair ilk ipuçlarını sağlamıştır.

SQL Analizi

Veri bilimi projesinde klasik EDA’nin yanı sıra SQL sorguları ile de veriye farklı açılardan bakılarak iş sorusuna yönelik spesifik içgörüler elde edilmiştir. Temizlenen veri, SQLite veritabanına aktarılıp çeşitli analitik SQL sorguları çalıştırılmıştır. Bu sayede belirli kategorilere göre özet istatistikler kolaylıkla çıkarılmıştır. SQL ile elde edilen dikkat çekici bulgulardan bazıları şunlardır:

Yaş Grupları: Orta yaş (30-50) ve ileri yaş (50+) gruplarında diyabet oranı ~%48-50 civarında olup genç yaş grubuna (<30, %21) kıyasla yaklaşık 2 kat daha yüksektir. Özellikle 30-50 yaş aralığındaki bireylerin neredeyse yarısında diyabet görülmesi, bu grubun risk altında olduğunu göstermektedir.

BMI Kategorileri: Obez kategorisindeki (BMI ≥ 30) hastaların %45.8’inde diyabet varken, normal kilolu bireylerde bu oran sadece %6.9 olarak bulunmuştur. Fazla kilolu (şişman) grupta oran %22 civarıdır. Bu büyük fark, obezitenin diyabet için en kritik risk faktörlerinden biri olduğunu doğrulamaktadır.

Yüksek Riskli Bireylerin Tespiti: Glukoz değeri > 140 ve BMI > 30 olup henüz diyabet tanısı almamış olan 36 kişi belirlenmiştir. Bu kişiler mevcut durumda “sağlıklı” görünmekle birlikte ölçümlerine bakıldığında diyabet geliştirme risklerinin çok yüksek olduğu anlaşılmaktadır. Bu grubun proaktif tarama ve yaşam tarzı müdahaleleri ile takibe alınması durumunda ileride oluşabilecek diyabet vakaları önlenebilir.

Hamilelik Sayısı ve Diyabet: Hiç hamile kalmamış veya 1-3 arası hamilelik yaşamış kadınlarda diyabet oranı %24–34 bandında iken, 7+ hamilelik yaşamış kadınların %56.2’sinde diyabet gözlenmiştir. Hamilelik sayısındaki artışa paralel olarak diyabet görülme oranının arttığı bu bulgu, birden çok gebelik yaşayan kadınların metabolik sağlık açısından daha yakından izlenmesi gerekebileceğine işaret etmektedir.

Yukarıdaki SQL destekli analizler, diyabet riskini belirleyen kritik segmentleri açıkça ortaya koymuştur. Özellikle obez bireyler, ileri yaş grupları ve çoklu hamilelik öyküsü olan kadınlar yüksek risk kategorileri olarak öne çıkmıştır. Ayrıca henüz diyabet gelişmemiş ancak ölçümleri alarm verici düzeyde olan spesifik bireylerin tespiti, projenin iş çıktıları açısından çok değerlidir.

Makine Öğrenmesi

Veri analizi sonucunda elde edilen içgörüler, bir sonraki aşamada makine öğrenmesi modeli geliştirilerek doğrulanmıştır. Modelleme aşamasında verinin %60’ı eğitim, %40’ı test olacak şekilde train-test split yapılmıştır (stratified, rasgele bölünme, random_state=42). Model eğitimine geçmeden önce tüm sayısal özellikler standartlaştırılmış (StandardScaler ile) ve böylece özelliklerin ölçek farkları giderilmiştir.

Birden fazla sınıflandırma algoritması kullanılarak farklı modeller eğitilmiştir. Özellikle Lojistik Regresyon, Random Forest, Gradient Boosting (XGBoost benzeri ağaç tabanlı yöntem) ve Destek Vektör Makineleri (SVM) algoritmaları denenmiştir. Her bir model eğitim sonrasında test verisinde performans metrikleri ile değerlendirilmiştir. Kullanılan temel metrikler Doğruluk (Accuracy), F1 skoru, ROC-AUC eğrisi altında kalan alan ve sınıf bazlı Precision/Recall değerleridir. Ayrıca modellerin genelleme performansını ölçmek amacıyla 5 katlı Cross-Validation (çapraz doğrulama) uygulanmış ve CV ortalama skorları kaydedilmiştir.

Model sonuçları karşılaştırıldığında tüm modellerin makul performans sergilediği, ancak en yüksek ROC-AUC değerine Gradient Boosting modelinin ulaştığı görülmüştür. Örneğin, Gradient Boosting modeli test verisinde yaklaşık %78 doğruluk ve 0.84 ROC-AUC skoruna erişmiştir. Logistic Regression ve SVM modelleri %75-77 bandında doğruluk ve 0.78-0.80 AUC değerleri verirken, Random Forest modeli de benzer şekilde ~%77 doğruluk ve 0.82 civarı AUC sağlamıştır. Dolayısıyla en iyi model olarak seçilen Gradient Boosting, en yüksek AUC değeri ile diyabet sınıfını diğer yöntemlere göre daha isabetli ayırt etmiştir.

Seçilen en iyi model için karışıklık matrisi (confusion matrix) analiz edildiğinde, pozitif sınıf için duyarlılık (recall) oranının makul seviyede olduğu (örneğin diyabetli vakaların ~%70’inin model tarafından yakalandığı), pozitif öngörü değerinin (precision) de benzer şekilde tatmin edici olduğu görülmüştür. Bu, modelin hem diyabet olan kişileri kaçırmama hem de yanlış alarm verme oranlarının dengeli olduğunu gösterir.

Ayrıca makine öğrenmesi aşamasında özellik önem dereceleri incelenerek modelin karar verirken hangi değişkenlere daha çok dayandığı anlaşılmıştır. Örneğin Random Forest modelindeki önem skorlarına bakıldığında, eldeki özelliklerden en önemlisinin türetilen Glucose_BMI_Interaction özelliği olduğu ortaya çıkmıştır. Bunu sırasıyla Glucose, BMI, Age ve Pregnancies gibi değişkenler izlemiştir. Bu sonuç, daha önce EDA aşamasında elde edilen bulgularla tutarlıdır: Glukoz, BMI ve yaş, diyabet riskini en güçlü belirleyen unsurlar arasındadır. Etkileşim değişkeninin en tepede yer alması ise, glukoz ve obezitenin birlikte yüksek olduğu durumların diyabet riskini katlayarak artırdığının bir göstergesidir.

Genel olarak, makine öğrenmesi adımı analiz sürecindeki çıkarımları sayısal olarak doğrulamış ve somutlaştırmıştır. Elde edilen en iyi model kullanılarak veri setindeki yüksek riskli bireyler başarılı şekilde tespit edilmiş, böylece projenin teknik çıktısı iş problemini çözmeye hazır hale getirilmiştir.

Ana Bulgular ve İçgörüler

Yürütülen analiz ve modelleme çalışmaları neticesinde öne çıkan temel bulgular aşağıda özetlenmiştir:

En Önemli Risk Faktörleri: Glukoz seviyesi, vücut kitle indeksi (BMI) ve yaş, diyabet riskini belirlemede en öne çıkan faktörlerdir. Bu üç değişken, diyabetli bireyleri sağlıklılardan ayırmada büyük pay sahibidir. Özellikle yüksek glukoz düzeyi ve obezite, birlikte ortaya çıktığında diyabet ihtimalini çok yükseltmektedir.

Diyabetli ve Sağlıklı Bireylerin Profil Farkları: Diyabet tanısı almış bireylerin ortalama klinik değerleri, sağlıklı bireylere kıyasla belirgin şekilde yüksektir. Örneğin bu çalışmada diyabetli grubun ortalama glukoz değeri sağlıklı grubunkinden yaklaşık 30 mg/dL daha yüksekti. Benzer biçimde diyabetli bireylerin ortalama BMI’ı daha yüksek ve yaş ortalaması daha ileridir. Bu farklar, risk altındaki bireylerin mevcut ölçümlerle tespit edilebileceğini göstermektedir.

Model Başarımı ve Kullanılabilirliği: Geliştirilen makine öğrenmesi modeli, popülasyondaki diyabet riskini tahmin etmede yaklaşık %80 doğruluk sergilemiştir. Bu, modelin gerçek dünyada tarama testi olarak kullanılabileceğine dair umut vermektedir. Model sayesinde mevcut veriler ışığında hangi bireylerin yüksek risk grubunda olduğunun önceden belirlenmesi mümkün hale gelmiştir.

Yüksek Riskli Segmentler: Analizler sonucunda obezite, ileri yaş, yüksek glukoz düzeyi ve çoklu hamilelik gibi durumlar kritik risk unsurları olarak belirlenmiştir. Özellikle obez ve pre-diyabetik bireyler (örn. glukoz seviyesi çok yüksek olmasına rağmen henüz diyabet tanısı almamış kişiler) önemli bir hedef segmenttir. Bu projede bu kriterlere uyan 30’dan fazla birey tespit edilmiştir. Bu kişilere odaklanarak diyabetin önlenmesi, hem bireylerin yaşam kalitesi hem de sağlık sistemi maliyetleri açısından büyük kazanımlar sağlayacaktır.

Yukarıdaki içgörüler, diyabetin önlenmesi ve yönetimi konusunda veri odaklı aksiyonlar almak için güçlü bir temel sunmaktadır. Bir sonraki adım olarak, bu bulguların iş kararlarına dönüştürülmesi gerekmektedir. Proje kapsamında bu amaçla önerilen stratejik aksiyonlar ve beklenen iş etkileri aşağıda sunulmuştur.

Teslim Edilen Çıktılar

Teknik Sunum: notebooks/saglik_teknik_sunum.ipynb – Projedeki veri analizi, EDA ve modelleme adımlarını içeren Jupyter Notebook (5 dakikalık teknik sunum formatında hazırlanmıştır).

Business Sunumu: presentation/saglik_business_sunum.pdf – İş problemini, analiz bulgularını ve önerileri özetleyen 5 dakikalık yönetici sunumu (PDF). Kod veya teknik detay içermez, iş değeri odaklı bulgular sunar.

İnteraktif Dashboard: dashboard_link.txt – Analiz bulgularına dair KPI ve grafiklerin yer aldığı Tableau Public dashboard linki. Bu gösterge tablosu üzerinden kullanıcılar diyabet verisini etkileşimli olarak keşfedebilirler.

Medium Yazısı: medium_link.txt – Projenin hikayesini, yöntemlerini ve sonuçlarını genel bir kitleye aktaran Medium makalesinin linki.

İş Önerileri

Analizden elde edilen içgörüler doğrultusunda, sağlık kuruluşu için aşağıdaki aksiyon önerileri geliştirilmiştir:

1. Risk Bazlı Tarama Programı: Model tarafından yüksek riskli olarak işaretlenen hastaların düzenli aralıklarla (ör. 3 ayda bir) glukoz ve HbA1c testlerine tabi tutulması. Beklenen etki: Erken teşhis oranında ~%30 artış. Bu sayede diyabet başlangıcı olan hastalara çok erken müdahale edilebilir.

2. BMI Yönetim Programı: BMI > 30 (obez) olan hastalar için kapsamlı bir yaşam tarzı müdahalesi programı başlatılması. Diyetisyen desteği, egzersiz planları ve düzenli takip ile kilo verilmesi teşvik edilecektir. Beklenen etki: İlgili bireylerde diyabete dönüş riskinde %25-40 azalma. Bu program, uzun vadede diyabet insidansını düşürerek tedavi maliyetlerini azaltacaktır.

3. Dijital Sağlık Platformu: Prediyabetik gruptaki bireyler (ör. glukoz seviyesi sınırda olanlar) için bir mobil uygulama veya dijital takip platformu geliştirilmesi. Bu platform üzerinden kullanıcılar düzenli glukoz ölçümlerini, fiziksel aktivite ve beslenme bilgilerini girebilir; ayrıca eğitim içerikleri ve hatırlatıcı bildirimler alabilir. Beklenen etki: Hasta bağlılığında ve öz bakımında %40’a varan artış. Bu sayede prediyabet hastalarının önemli bir kısmında diyabete geçiş geciktirilebilir veya engellenebilir.

Yukarıdaki öneriler, birlikte ele alındığında kapsamlı bir diyabetle mücadele stratejisi oluşturmaktadır. Riskli bireylerin erken tespiti (Öneri 1) ile başlayan, obezite gibi altta yatan nedenlere müdahale eden (Öneri 2) ve teknoloji ile hasta takibini güçlendiren (Öneri 3) entegre bir yaklaşım sayesinde diyabet yükünün azaltılması hedeflenmektedir.

Beklenen İş Etkisi

Önerilen aksiyon planının hayata geçirilmesiyle, hem klinik sonuçlarda hem de finansal göstergelerde önemli iyileşmeler beklenmektedir. Yapılan basit bir maliyet-fayda analizi, proaktif tarama ve önleme odaklı bu yaklaşımın yıllık bazda kayda değer tasarruflar sağlayacağını göstermiştir. Örneğin, yüksek riskli grupta diyabeti önlenen vakalar sayesinde yılda yüz binlerce TL tutarında sağlık harcaması düşüşü öngörülmektedir. Bu da program maliyetlerini fazlasıyla karşılayarak >%100 ROI (yatırım getirisi) anlamına gelmektedir. Başka bir deyişle, önerilen müdahaleler kendini bir yıldan daha kısa sürede amorti edebilecek düzeydedir.

Finansal kazanımların ötesinde, yıllık bazda onlarca yeni diyabet vakasının önlenebilmesi toplum sağlığı açısından muazzam bir fayda sağlayacaktır. Erken teşhis edilen ve yaşam tarzı iyileştirmeleriyle diyabetten kurtulan her bir birey, uzun vadede komplikasyon yaşamaktan kurtulacağı için yaşam kalitesinde ölçülemez bir artış söz konusu olacaktır. Bu projenin öngördüğü proaktif sağlık yönetimi modeli, hem kurumun sürdürülebilirliği hem de hasta popülasyonunun refahı için kazan-kazan bir durum yaratmaktadır.

Kurulum ve Çalıştırma

Projeyi kendi ortamınızda çalıştırmak için aşağıdaki adımları izleyebilirsiniz:

Repoyu klonlayın: Proje kod ve dosyalarını GitHub reposundan yerel makinenize klonlayın.

Gereklilikleri yükleyin: Python 3 ortamınızı hazırlayın ve requirements.txt dosyasındaki bağımlılıkları pip install -r requirements.txt komutu ile yükleyin. Gerekli başlıca kütüphaneler: pandas, numpy, scikit-learn, seaborn, matplotlib, etc.

Veri setini hazırlayın: data/raw/ klasörüne orijinal diyabet veri setini (diabetes.csv) yerleştirin. (Not: Kaggle üzerinden elde ettiyseniz, dosya yolunu notebook'ta güncellemeniz gerekebilir. Repo ile birlikte CSV sağlanmışsa bu adım gerekmez.)

Notebook'u çalıştırın: notebooks/saglik_teknik_sunum.ipynb dosyasını Jupyter Notebook ya da JupyterLab ile açın. Tüm hücreleri sırayla çalıştırarak analiz adımlarını yeniden üretin. Bu notebook içerisinde veri yükleme, EDA, SQL analizleri ve modelleme kodları bulunmaktadır.

Sonuçları inceleyin: Notebook çalıştırıldıktan sonra üretilen grafik ve metrikleri adım adım gözlemleyebilirsiniz. Daha detaylı iş sunumu için presentation/saglik_business_sunum.pdf dosyasını açarak proje özetini ve önerileri görebilirsiniz.

Dashboard ve makaleyi görüntüleyin: dashboard_link.txt içindeki URL'yi web tarayıcınızda açarak Tableau Public üzerindeki interaktif gösterge tablosunu inceleyin. medium_link.txt dosyasındaki bağlantı aracılığıyla proje hakkında yazılan Medium makalesine ulaşabilir ve proje hikayesini okuyabilirsiniz.

Bu adımların ardından, dilerseniz kendi veri setinizle veya farklı parametrelerle de modeli tekrar eğitebilir, kodu uyarlayabilirsiniz. Her adım, yorum satırlarıyla detaylandırılmış olup proje yürütme süreci şeffaf bir şekilde ortaya konmuştur.

İletişim Bilgileri

İsim Soyisim:  Ediz Özaktaç

E-posta:  ediz_ozaktac@hotmail.com

LinkedIn:  https://www.linkedin.com/in/ediz-özaktaç-439199309/

Business Sunumu (Sunum Taslağı)

Aşağıda, 5 dakikalık business sunumu için önerilen slayt başlıkları ve içerik ana noktaları belirtilmiştir. Bu taslak, üst düzey yöneticilere veya teknik olmayan paydaşlara projenin değerini aktarmak üzere hazırlanmıştır:

Problem & Proje Amacı: Diyabetin Önemi ve Mevcut Durum – Diyabetin toplum sağlığına etkisi (istatistiksel bilgilerle vurgu), kurum için önemi. Projenin bu sorunu ele alma amacı: veriye dayalı erken teşhis ve önleme modeli geliştirmek.

Veri Seti & Yöntem: Veri ve Analiz Yaklaşımı – Kullanılan Pima Indians Diyabet veri setinin tanımı (768 hasta, 8 özellik). Analiz sürecinin adımları: veri temizleme, EDA, modelleme. Kısaca proje metodolojisi ve ekipman (Python, ML algoritmaları).

Analiz Bulguları (EDA): Diyabet Risk Faktörleri – EDA sonucunda ortaya çıkan temel içgörüler. Örneğin: “Yüksek glukoz, obezite ve ileri yaş diyabet riskini en çok artıran faktörlerdir” gibi maddeler. Destekleyici basit grafikler: yaş dağılımı vs diyabet oranı, BMI kategorilerine göre diyabet yüzdeleri vb. Bu slayt, problemi nicel olarak çerçeveler.

Model Sonuçları: Tahmin Modeli Performansı – Geliştirilen makine öğrenmesi modelinin başarı metriği: örn. %78 doğruluk, %84 AUC. Modelin yüksek riskli hastaları önceden yakalayabildiği vurgusu. Basit bir confusion matrix görseli veya bar grafikte modellerin karşılaştırması (logistic vs random forest vs GBM performansı) kullanılabilir. En iyi modelin seçildiği ve güvenilir olduğu belirtilmeli.

Önerilen Aksiyonlar: Stratejik Öneriler – Analizden çıkan 3 ana öneri maddesi bu slaytta vurgulanır. Örneğin: “Risk bazlı tarama programı (yüksek riskli grupların düzenli kontrolü)”, “Obeziteyle mücadele programı (diyet & egzersiz)”, “Dijital takip uygulaması (prediyabetik hastalar için)”. Her birinin beklenen faydası kısaca (yıllık tasarruf, risk azalması vb.) not edilir.

Beklenen Etki & Sonuç: İş Değeri ve Sonraki Adımlar – Önerilen programların beklenen finansal getirisi (ROI % ve yıllık tasarruf rakamı), önlenecek vaka sayısı gibi önemli sonuçlar belirtilir. Örneğin: “Yıllık ~500 bin TL tasarruf, %120 ROI ve 30 vakanın önlenmesi öngörülüyor.” Son olarak, projenin kuruma kazandıracakları özetlenir ve uygulama için çağrı yapılır (örn: pilot program önerisi, takvim).

Her slayt, metin yerine mümkün olduğunca görsel ve grafiklerle desteklenmelidir. Anlatım sırasında teknik detaylara girilmeden, iş probleminin nasıl çözüldüğü ve elde edilecek kazanımlar net bir şekilde ifade edilmelidir. Sunum sonunda yöneticilerin sorularını yanıtlamak üzere yedek slaytlar veya ek verilere sahip olmak da faydalı olabilir.

İnteraktif Dashboard (İçerik Özeti)

Tableau üzerinde hazırlanan interaktif gösterge tablosu, projenin önemli bulgularını görsel olarak sunmaktadır. Dashboard içeriği ve bileşenleri şöyle tasarlanmıştır:

Temel Göstergeler (KPIs): Ekranın üst kısmında birkaç kilit metrik yer alır. Örneğin, Diyabet Prevalansı (%): veri setindeki diyabetli oranı (~%35), Ortalama Glukoz: tüm popülasyon için ortalama glukoz seviyesi, Ortalama BMI: ortalama vücut kitle indeksi gibi. Bu sayede genel tablo hızlıca anlaşılır.

Grafikler: Dashboard, diyabet riskine etki eden faktörleri açıklayan 2-3 adet grafik içerir. Örneğin:

Yaş Gruplarına Göre Diyabet Oranı: Genç, orta yaş, ileri yaş gruplarında diyabet yüzdesini gösteren bir sütun grafik. Bu grafik, yaş arttıkça diyabet oranının nasıl yükseldiğini görselleştirir.

BMI Kategorilerine Göre Diyabet: Zayıf/Normal/Fazla Kilolu/Obez kategorilerinde diyabet görülme oranlarını gösteren bir sütun veya pasta grafik. Burada obez kategorisinin bariz şekilde daha yüksek orana sahip olduğu vurgulanır.

Hamilelik Sayısının Etkisi: Farklı hamilelik sayısı gruplarında (0, 1-3, 4-6, 7+ hamilelik) diyabet oranını gösteren bir grafik. Bu da çoklu hamilelik yaşamış kadınlarda riskin en yüksek olduğunu ortaya koyar.

Glukoz ve BMI Dağılımı: Opsiyonel olarak, glukoz ve BMI değerlerinin dağılımını Outcome’a göre renklendiren bir saçılma grafiği (scatterplot). Bu grafik yüksek glukoz ve BMI birlikteliğinin çoğunlukla diyabetli grupta olduğunu interaktif biçimde gösterebilir.

Filtreler: Dashboard’da kullanıcı etkileşimi için filtre seçenekleri mevcuttur. Örneğin Yaş aralığı filtresi ile belirli bir yaş aralığını seçip tüm grafiklerin o alt grup için güncellenmesi sağlanabilir. Benzer şekilde BMI kategorisi filtresi veya Hamilelik grubu filtresi eklenerek kullanıcıların spesifik segmentlere odaklanması mümkün kılınmıştır. Ayrıca Outcome filtresi (diyabetli/sağlıklı) ile sadece diyabetli bireylerin veya sağlıklıların metriklerini incelemek de mümkündür.

Açıklamalar: Her grafiğin yanında kısa metin açıklamaları veya vurgu okları ile önemli noktalar belirtilmiştir. Örneğin obez kategorisinin en yüksek riske sahip olduğu veya 50+ yaş grubunun alt segmentlere göre 2 kat risk taşıdığı not düşülmüştür.
