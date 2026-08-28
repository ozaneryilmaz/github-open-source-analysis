# GitHub API Endpointleri

Bu klasör projede kullanılan GitHub REST API endpointlerini ve sorgu yapılarını içermektedir.

## Repository Search

GitHub üzerindeki en popüler repositoryleri yıldız sayısına göre sıralamak için:

https://api.github.com/search/repositories?q=stars:%3E1&sort=stars&order=desc&per_page=100

## Release API

Repositorylerin release bilgilerini almak için aşağıdaki endpoint kullanılmıştır:

`GET /repos/{owner}/{repo}/releases`

Projede her repository için son 20 release incelenmiştir.

Örnek:

`https://api.github.com/repos/cli/cli/releases?per_page=20`

Release verileri içerisindeki `assets` alanı açılarak aşağıdaki bilgiler kullanılmıştır:

- `name`
- `download_count`
- `browser_download_url`

`download_count` değeri yalnızca ilgili release asset dosyasının indirilme sayısını ifade eder.

Bu değer:

- repository clone sayısını,
- package manager indirmelerini,
- source code archive indirmelerini,
- benzersiz kullanıcı sayısını

temsil etmez.

API istek limitlerini yönetebilmek amacıyla release analizi, yıldız sayısına göre seçilen en popüler 30 repository ve repository başına son 20 release ile sınırlandırılmıştır.
