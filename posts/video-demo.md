---
title: 'Test the video tag'
date: '2020-03-30'
---

## Test

Try to use the `<video>` tag in Markdown content:

```HTML
<video controls="true" width="100%" preload="metadata" playsinline>
  <source src="/videos/demo.mp4" type="video/mp4" />
</video>
```

<video controls="true" width="100%" preload="metadata" playsinline>
  <source src="/videos/demo.mp4" type="video/mp4" />
</video>

It worked fine in Chrome on my mac, but failed in Safari on my iOS device.

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