---
title: "Display all PHP internal functions"
date: 2020-01-08 12:04:09
categories: [programming]
tags: [php]
authors: sedlav
---

We can display all PHP internal functions using `get_defined_functions` like this:

```php
<?php
foreach (get_defined_functions()['internal'] as $func_name) {
    echo $func_name, PHP_EOL;
}
```

## Further reading

- [get_defined_functions](https://www.php.net/manual/en/function.get-defined-functions.php)