---
title: How to read URLs from a local or external file using curl?
date: 2017-12-27 23:03:05
categories: [cli]
tags: [xargs, curl]
authors: sedlav
---

If you want to read multiple URLs using curl like wget -i style you can follow one of these methods:

## Method 1. Using xargs and curl

```
$ xargs -a urls.txt -I{} curl -O {} 
```

# Method 2. Using -K option

```
curl -K url.txt
```

url.txt has this format:

```
url = "url1"
output = "name1"

url = "url2"
output = "name2"
```

# Method 2. Using -K option, reading standard input and HEREDOC

```
$ curl -# -K - <<URL
    url = "https://download.libsodium.org/libsodium/releases/$libsodium"
    output = "$libsodium"

    url = "https://download.libsodium.org/libsodium/releases/$libsodium.sig"
    output="$libsodium.sig"
URL
```


If you want to empty several files in one operation you can type a sentence like this

```bash
$  find -type f -name '*.xml' -print0|xargs -0 -I {} bash -c "> {}"
```

## Further reading

- man curl