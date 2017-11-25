---
title: How to cut a video with ffmpeg
date: 2017-11-25 12:25:57
categories: [media]
tags: [ffmpeg]
author: sedlav
---

To cut a video with a ffmpeg type:

```bash
$ ffmpeg -ss 00:00:42 -i video.mp4  -t 00:03:55 -acodec copy -vcodec copy video-cut.mp4
```

**where**

* **-ss**: where the cut video will start
* **-t**: duration of cut video

## Further reading

- man ffmpeg