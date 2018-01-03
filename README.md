文件上传到七牛
=================================
* @author crazyfd <crazyfd@qq.com>
* @version 1.0

file upload for qiniu

最近会调整版本

```json
{
  "require": {
    "crazyfd/upload": "*"
  }
}
```
```php
composer install
```

Usage
-----

```php
<?php
$ak = 'sss';
$sk = 'sss';
$domain = 'http://demo.domain.com/';
$bucket = 'demo';
$zone = 'south_china';
use crazyfd\qiniu\Qiniu;
$qiniu = new Qiniu($ak, $sk,$domain, $bucket,$zone);
$key = time();
$qiniu->uploadFile($_FILES['tmp_name'],$key);
$url = $qiniu->getLink($key);
```
