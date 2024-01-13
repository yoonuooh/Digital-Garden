---
date: 2023-08-13
tags: PHP, Linux
---

## 로컬 폴더 경로

- `cd /$PREFIX/share/apache2/default-site/htdocs`



## 설정 파일

- `vi /data/data/com.termux/files/usr/etc/apache2/httpd.conf`

```
LoadModule mpm_prefork_module libexec/apache2/mod_mpm_prefork.so
LoadModule php_module /data/data/com.termux/files/usr/libexec/apache2/libphp.so
<FilesMatch \.php$>
	SetHandler application/x-httpd-php
</FilesMatch>
```
