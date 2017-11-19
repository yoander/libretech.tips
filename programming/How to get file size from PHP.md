---
Title: "How to get file size from PHP"
Date: 2017-08-04 16:43:57
Categories: [programming]
tags: [php]
Authors: sedlav
---

You can get file size from PHP in 2 ways

1. Using stat function

```php
<?php
echo stat($file_path)['size'];
```

2. Using SplFileInfo class

```php
<?php
echo (new SplFileInfo($filePath))->getSize();
```

**Note:** file size is reported in bytes.