Titanic Veri Seti: Makine Öğrenmesi Modelleri ile Hayatta Kalma Tahmini
Bu projede, Titanic veri seti kullanılarak yolcuların hayatta kalıp kalmayacakları tahmin edilmiştir. Farklı makine öğrenmesi modelleri eğitilerek performansları karşılaştırılmış ve en iyi model belirlenmiştir. Aşağıda, proje sürecinin adımları, kullanılan yöntemler ve sonuçlar yer almaktadır.

Proje Adımları
1. Veri Seti ve Veri Hazırlığı

Titanic veri seti, Kaggle üzerinde yer alan ve yolcuların özelliklerini içeren bir veri setidir. Veriyi yükledikten sonra:

Eksik Verilerle Başa Çıkma: Yaş ve emekli olma durumu gibi bazı sütunlarda eksik veriler vardı. Bu veriler uygun şekilde dolduruldu.
Kategorik Verilerin Dönüştürülmesi: 'Sex', 'Embarked', 'Who' gibi kategorik veriler LabelEncoder ile sayısal verilere dönüştürüldü.
Yeni Özellikler: Bazı yeni özellikler oluşturuldu, örneğin "Adult Male" ve "Alone" gibi.
2. Eğitim ve Test Setlerinin Ayrılması

Veri seti, %80 eğitim ve %20 test verisi olarak ikiye ayrıldı. Eğitim seti, modelleri eğitmek için kullanılırken, test seti, modellerin doğruluğunu değerlendirmek için kullanıldı.

3. Modellerin Eğitilmesi

Aşağıdaki regresyon ve sınıflandırma modelleri üzerinde eğitim yapıldı:

Logistic Regression
K-Nearest Neighbors (KNN)
Support Vector Machine (SVM)
Decision Tree
Random Forest
XGBoost
Linear Regression
Her modelin eğitilmesinin ardından doğruluk, precision, recall, f1-score gibi metrikler hesaplanarak karşılaştırma yapıldı.

4. Performans Değerlendirmesi

Modellerin performansları aşağıdaki gibi değerlendirildi:

Doğruluk (Accuracy): Modelin doğru tahminlerinin oranı.
Precision: Pozitif tahminlerin ne kadar doğru olduğunu gösterir.
Recall: Gerçek pozitiflerin ne kadarının doğru tahmin edildiğini gösterir.
F1-Score: Precision ve recall arasındaki dengeyi gösterir.
Aşağıda her modelin doğruluk skorları verilmiştir:

Model	                Doğruluk Skoru (%)
Logistic Regression	83.24
K-Nearest Neighbors	82.68
Support Vector Machine	81.56
Decision Tree	        80.45
Random Forest	        83.24
XGBoost	                79.89
Linear Regression	41.86

5. Karışıklık Matrisi ve Model Karşılaştırmaları

Her model için karışıklık matrisi oluşturuldu ve modelin performansı görselleştirildi. Bu matris, doğru ve yanlış tahminleri, yani modelin nasıl çalıştığını gösterir.

Precision: Modelin pozitif sınıf için ne kadar doğru tahminde bulunduğunu gösterir.
Recall: Gerçek pozitiflerin ne kadarının doğru tahmin edildiğini gösterir.
F1-Score: Precision ve recall arasında bir denge sağlar.

6. Hiperparametre Optimizasyonu

Hiperparametre optimizasyonu, modellerin daha iyi sonuçlar verebilmesi için uygulandı. Özellikle Random Forest ve XGBoost modellerinde GridSearchCV kullanılarak en uygun hiperparametreler belirlendi.

7. Sonuçlar ve Öneriler

En İyi Modeller: Logistic Regression ve Random Forest modelleri en yüksek doğruluk skorlarına sahip oldu. Bu modeller, test verisi üzerinde iyi performans gösterdi.
Düşük Performans Gösteren Model: Linear Regression, doğrusal olmayan ilişkiler nedeniyle diğer modellere göre düşük performans gösterdi.
Sonuç: Titanic veri setinde, özellikle doğrusal olmayan modeller (Random Forest, Logistic Regression) daha başarılı sonuçlar verdi.

Kullanılan Kütüphaneler
pandas: Veri manipülasyonu ve analizi için.
numpy: Matematiksel hesaplamalar için.
matplotlib & seaborn: Görselleştirme için.
sklearn: Makine öğrenmesi modelleri ve metrikleri için.
xgboost: XGBoost modelini eğitmek için.