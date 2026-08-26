# GitHub API Endpointleri

Bu klasör projede kullanılan GitHub REST API endpointlerini ve sorgu yapılarını içermektedir.

## Repository Search

GitHub üzerindeki en popüler repositoryleri yıldız sayısına göre sıralamak için:

https://api.github.com/search/repositories?q=stars:%3E1&sort=stars&order=desc&per_page=100

## Release API

Repository release bilgilerini almak için kullanılacak yapı:

/repos/{owner}/{repo}/releases
