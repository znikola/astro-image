# Minimal repro for Astro's assets image problem

Open the `index.astro` and note the imported `test` image from `../assets/test.jpg`. The `test.jpg` is quite large, and I would like to optimize it by converting it to `webp`.

According to the docs, this should be possible by declaring the desired type on the `<Image>` tag itself:

```html
<image {...test} format="webp" alt="just a test image" />
```

However, after running `npm run build` or `npm run dev`, the image remains in the `.jpg` format.

I tried with both squoosh and sharp, and the result is the same.
