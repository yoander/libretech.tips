---
title: "How to get file size from PHP?"
date: 2017-08-04 16:43:57
categories: [programming]
tags: [php]
authors: sedlav
---

You can get file size from PHP in 2 ways

## Using stat function

```php
<?php
echo stat($file_path)['size'];
```

## Using SplFileInfo class

```php
<?php
echo (new SplFileInfo($filePath))->getSize();
```

**Note:** file size is reported in bytes.