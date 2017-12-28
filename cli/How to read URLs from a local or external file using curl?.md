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
$ xargs -a urls.txt -I{} curl -# -O {} 
```

## Method 2. Using -K option

```
curl -# -K url.txt
```

url.txt has this format:

```
url = "url1"
output = "name1"

url = "url2"
output = "name2"
```

## Method 3. Using -K option, reading standard input and HEREDOC

```
$ curl -# -K - <<URL
    url = "https://download.libsodium.org/libsodium/releases/libsodium-1.0.16.tar.gz"
    output = "libsodium-1.0.16.tar.gz"

    url = "https://download.libsodium.org/libsodium/releases/libsodium-1.0.16.tar.gz.sig"
    output="libsodium-1.0.16.tar.gz.sig"
URL
```

## Further reading

- man curl