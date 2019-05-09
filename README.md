# Wavy BG

Here are four resizable/colorable SVG backgrounds with the 2019 trending curve.
Free for all, hope it helps. If you want to setup and customize you need NodeJS.

---

<!-- TOC -->

- [Wavy BG](#wavy-bg)
  - [Paths and Files](#paths-and-files)
  - [The SVG Images](#the-svg-images)
  - [Colorizing the SVG](#colorizing-the-svg)
  - [(Optional) Build and Bundle](#optional-build-and-bundle)
    - [Install Bundler](#install-bundler)
    - [Running the Transpiler](#running-the-transpiler)

<!-- /TOC -->

---

<img src="https://raw.githubusercontent.com/JREAM/svg-curved-backgrounds/master/preview.png" alt="preview" />

---

## Paths and Files

This all may not be necessary. You can just download the images where they are located below, do what you
please if you enjoy! You do not have to "credit Jesse", It took a few minutes to draw, the license is to
stay out of trouble -- who knows what goes on the interwebs anymore.

- src/
  - assets/
    - images/
      - `bg-inward-deep.svg`
      - `bg-inward.svg`
      - `bg-outward.svg`
      - `bg-wave.svg`
    - styles
      - `_normalize.scss` -- This isn't needed here, it's just for demo's.
      - `main.scss` -- This is really all you need (the `dist`) folder will have an **uncompressed CSS** copy.
  - `index.html` -- This is the **entrypoint** for Parcel which includes the `main.scss` file, and ends up in `./dist/main.css`.

## The SVG Images

In each SVG, they contain the same `class="bg-<name>`, remove or adjust how you like.

If you wanted to manually add CSS within the SVG, you would add `<defs><style>...` like below, and add a class to
the `svg path`.

```xml
  <defs>
    <style>.bg-outward {fill:red;}</style>
  </defs>
  <path class="bg-outward" ... />
```

## Colorizing the SVG

You can use the `filter` property, or probably CSS `masks`.

```css
filter: hue-rotate(40deg) saturate(0.5) brightness(390%) saturate(4);
```

## (Optional) Build and Bundle

I added [Parcel Bundler](http://parceljs.org) to turn out SCSS and any assets because it's simple with
zero-configuration.

### Install Bundler

```sh
yarn
npm i
```

### Running the Transpiler

By default, this runs at: [http://localhost:1234](http://localhost:1234)

```sh
yarn develop  # ( alias: yarn start )
yarn build

npm run develop  # ( alias: npm run start )
npm run build
```

> In Windows you may need to change `$npm_package_main` to `%npm_package_main%`, I'm chilling with Ubuntu.

---

Open Source MIT

&copy 2019 Jesse Boyer <[https://jream.com](JREAM)>
