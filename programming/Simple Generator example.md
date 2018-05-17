---
title: "Simple Generator example"
date: 2017-08-08 20:18:04
categories: [programming]
tags: [php]
authors: sedlav
---

This a simple Generator example

```php
<?php
function gen() {
    foreach (['a', 1, new Exception()] as $e) {
        yield $e;
    }

}

foreach (gen() as $e) {
    $type = gettype($e);
    if ($type == 'object') {
        echo get_class($e), PHP_EOL;
    } else {
        echo $type, PHP_EOL;
    }
}
```

The above will print

```
string
integer
Exception
```