---
title: 'Test the video tag'
date: '2020-03-30'
---

## Test

Try to use the `<video>` tag in Markdown content:

```HTML
<video controls="true" width="100%" preload="metadata" playsinline>
  <source src="/videos/demo.mp4" type="video/mp4" />
  Fallback: Your browser does not support this media.
</video>
```

<video controls="true" width="100%" preload="metadata" playsinline>
  <source src="/videos/demo.mp4" type="video/mp4" />
   Fallback: Your browser does not support this media.
</video>

It worked fine in Chrome on my mac, but failed in Safari on my iOS device.

Try to set the video in `<img>` tag which I learnt from [the Apple webkit docs](https://developer.apple.com/documentation/webkit/delivering_video_content_for_safari?language=objc#3030249) that says:

> GIFs can be up to 12 times as expensive in bandwidth and twice as expensive in energy use when compared to a modern video codec. Instead, use H.264-encoded MP4 files for animations; for example:
> ```HTML 
> <img src="explosion.mp4" alt="An explosion of colors.">
> ```
> By placing your videos in <img> elements, the content loads faster, uses less battery power, and gets better performance. To maintain compatibility with other web browsers, also include a fallback image:
>```HTML
><picture>
>   <source srcset="explosion.mp4" type="video/mp4">
>   <img src="explosion.jpg" alt="An image of an explosion.">
></picture>
>```

The we try it in Markdown with:
```md
![video](/videos/demo.mp4)
```

And it shows:

![video](/videos/demo.mp4)

It works in Safari on iOS, but does not work in Chrome on Desktop now......

Nevertheless, when replaced the video source with one from other website,

```HTML
<video controls="true" width="100%" preload="metadata" playsinline>
  <source src="https://www.sample-videos.com/video123/mp4/720/big_buck_bunny_720p_2mb.mp4" type="video/mp4" />
</video>
```

<video controls="true" width="100%" preload="metadata" playsinline>
  <source src="https://www.sample-videos.com/video123/mp4/720/big_buck_bunny_720p_2mb.mp4" type="video/mp4" />
</video>

It does work fine in Safari on iOS. Weird. I'll try to figure it out.

[Help wanted](https://github.com/vercel/next.js/discussions/23552).