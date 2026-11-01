# Jirani Kahawa: The Neighbor's Cup (source files)

These are the editable sources behind `jirani-kahawa.mp4`, `jirani-kahawa-reel.mp4` and the `carousel/` images.

| Folder | Makes | Size |
|---|---|---|
| `video-landscape/` | `jirani-kahawa.mp4` | 89 s, 1920×1080 |
| `video-reel/` | `jirani-kahawa-reel.mp4` | 59.5 s, 1080×1920 |
| `carousel/` | `carousel/jirani-carousel-1.png` … `-9.png` | 1080×1350 each |

## Videos

Both videos are [HyperFrames](https://github.com/heygen-com/hyperframes) projects. Each scene is one file in `compositions/`, and `index.html` sets the order and timing.

```bash
cd video-landscape        # or video-reel
npx hyperframes@0.8.200 check
npx hyperframes@0.8.200 render -o out.mp4
```

The narration is in `assets/voice/`, made with the local Kokoro voice `bm_george` at 0.95 speed. To use your own voice, replace a `.wav` file and update that clip's `data-duration` in `index.html`.

## Carousel

`carousel/carousel.html` holds all nine slides as one page. Each slide is a 1080×1350 `<div class="slide">`. Open it in a browser and screenshot each slide, or use Playwright to capture each element.

The maps come from Natural Earth data, via the `world-atlas` and `us-atlas` packages.
