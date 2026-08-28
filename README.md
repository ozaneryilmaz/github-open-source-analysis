# GitHub Açık Kaynak Projelerinde Popülerlik ve İndirme Analizi

Bu proje, GitHub REST API üzerinden açık kaynak repository verilerinin alınması ve Power BI kullanılarak analiz edilmesi amacıyla geliştirilmiştir.

## Projenin Amacı

GitHub üzerindeki popüler açık kaynak projelerin yıldız, fork, programlama dili ve release indirme verilerini incelemek ve elde edilen sonuçları Power BI ile görselleştirmektir.

## Kullanılan Teknolojiler

- GitHub REST API
- JSON
- Power Query
- Power BI
- Git / GitHub

## Yapılan Analizler

- En çok yıldız alan GitHub projeleri
- En çok fork alan GitHub projeleri
- Top 100 repository içerisinde programlama dili dağılımı
- Release ve indirme analizi

## Durum

Proje geliştirme aşamasındadır. Repository popülerlik analizi tamamlanmış olup release indirme verilerinin API üzerinden alınması üzerinde çalışılmaktadır.

## Veri Kaynağı

Proje verileri GitHub REST API üzerinden alınmaktadır. Repository Search API kullanılarak yıldız sayısına göre en popüler 100 açık kaynak repository analiz edilmektedir.

## Yapılan Analizler

- GitHub üzerindeki en popüler 100 repository yıldız sayılarına göre analiz edildi.
- Repositorylerin fork sayıları karşılaştırıldı.
- Top 100 repository içerisinde kullanılan programlama dillerinin dağılımı incelendi.
- GitHub Topics verileri kullanılarak en çok ele alınan konular analiz edildi.
- Popüler repositorylerin release verileri GitHub REST API üzerinden çekildi.
- Release asset dosyalarının download_count değerleri kullanılarak indirme analizi gerçekleştirildi.
- Repository yıldız sayıları ile release asset indirmeleri karşılaştırıldı.
- Power BI üzerinde KPI kartları ve etkileşimli slicerlar kullanılarak genel bir dashboard oluşturuldu.

## Veri Modeli

Power BI içerisinde üç temel tablo kullanılmıştır:

- GitHubRepositories
- GitHubTopics
- GitHubReleases

Tablolar `FullName` alanı üzerinden ilişkilendirilmiştir.

GitHubRepositories tablosu ana repository tablosu olarak kullanılmış ve diğer tablolarla 1:N ilişkiler kurulmuştur.

## DAX Ölçüleri

Projede kullanılan temel ölçüler:

- ToplamIndirme
- AssetSayisi
- OrtalamaAssetIndirme
- RepositoryStars
- RepositorySayisi

Bu ölçüler KPI kartlarında ve analiz görsellerinde kullanılmıştır.

## Önemli Bulgular

- Top 100 repository içerisinde Python ve TypeScript öne çıkan programlama dilleri arasındadır.
- AI, Python, JavaScript ve LLM gibi konular en sık kullanılan GitHub Topics arasında yer almaktadır.
- Release asset indirme sayılarının yalnızca repository popülerliğine bağlı olmadığı görülmüştür.
- Release sayısı ve repository başına sunulan asset sayısı da toplam indirme miktarını önemli ölçüde etkilemektedir.

## Sınırlamalar

Release indirme analizinde GitHub API tarafından sağlanan `download_count` alanı kullanılmıştır.

Bu değer yalnızca GitHub Releases altında bulunan asset dosyalarının indirme sayılarını temsil eder.

Repository clone işlemleri, package manager üzerinden yapılan indirmeler veya benzersiz kullanıcı sayıları bu veriye dahil değildir.

Release analizi API istek sınırlarını yönetebilmek amacıyla en popüler 30 repository ve repository başına son 20 release ile sınırlandırılmıştır.

## Power BI Dashboard

Proje kapsamında Power BI üzerinde:

- Popülerlik ve Dil Analizi
- Top 100 Repository
- Topics Analysis
- Release & Download Analysis
- Overview

sayfaları oluşturulmuştur.
