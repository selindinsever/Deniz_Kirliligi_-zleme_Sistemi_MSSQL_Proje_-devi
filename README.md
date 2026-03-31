# Deniz_Kirliligi_Izleme_Sistemi_MSSQL_Proje_Odevi

Deniz Kirliliği İzleme Sistemi (Veri Tabanı Projesi)
Bu proje, deniz kirliliğini ölçmek, analiz etmek ve önlem almak amacıyla geliştirilmiş kapsamlı bir ilişkisel veri tabanı yönetim sistemidir. İnsan faaliyetlerinin deniz ekosistemi üzerindeki olumsuz etkilerini izlemek ve toplumsal farkındalığı artırmak için tasarlanmıştır.

Hazırlayan: Selin Dinsever 
Öğrenci Numarası: 20242425014 
Eğitim Görevlisi: Mehmet Hepkorucu 
Ders Kodu: MBP 108 
Tarih: 02.05.2025

Projenin Amacı

"Deniz Kirliliği İzleme Sistemi", deniz kirliliğine dair olayları, kaynakları ve bilimsel analizleri kayıt altına alarak kapsamlı bir değerlendirme aracı sunar. Proje, kirlilik olaylarının nedenleri, etkileri ve dağılımı üzerine odaklanarak çevreye yönelik daha bilinçli adımlar atılmasını hedeflemektedir.

Teknik Özellikler ve Veri Yapısı
Sistem, birbirleriyle ilişkili 14 ana tablo üzerinden yönetilmektedir . Proje kapsamında aşağıdaki ileri seviye SQL yetenekleri kullanılmıştır:

1. SQL Sorguları ve İlişkiler(Joins ve Inner Join): Ölçüm değerleri ile lokasyon adlarını eşleştirerek listeler.
2. Left/Right Join: Meteorolojik veriler ile deniz akıntılarını veya ölçümlerle kirlilik olaylarını eşleşme olmasa dahi raporlar.
3. Full Outer Join: Raporlar ve uzman kadrosu tablolarını birleştirerek tüm kayıtları eksiksiz listeler.
4. Stored Procedures: Yeni kirlilik olayı ekleme (SP_KIRLILIK_OLAYI_EKLEME).
5. Güncelleme: Mevcut olayların bilgilerini revize etme (SP_Kirlilik_Olayi_Guncelleme).
6. Güvenli Silme: TRY-CATCH ve TRANSACTION blokları kullanarak hata kontrollü veri silme (SP_Kirlilik_Olayi_Silme).
7. Functions: Verilen parametrelere göre değer hesaplayan FN_LokasyonId_Gore_Deger_Hesaplama ve FN_Akinti_Hizi_Hesaplama  fonksiyonları.
8. Tablo Döndüren Fonksiyonlar: Belirli bir yıla veya lokasyona göre filtreleme yapan dinamik sorgu fonksiyonları.
9. Triggers: Kirlilik_Olaylari tablosuna eklenen her kayıt anlık olarak Kirlilik_Olaylari_Yedek tablosuna da eklenir.
10. Instead Of Delete: Veriler fiziksel olarak silinmez, yedek tabloda "SilindiMi" işaretlenerek kayıt altında tutulur.
