<h1 align="center">Welcome to JPG to PNG Converter 🌄</h1>
<p>
<img alt="Version" src="https://img.shields.io/badge/version-3.1.0-blue.svg?cacheSeconds=2592000" />
  <a href="https://github.com/iqbalgithub1998/jpg_to_png_converter" target="_blank">
</p>

> A Node.js library that convert jpg to png

### 🏠 [Homepage](https://github.com/iqbalgithub1998/jpg_to_png_converter)

## Description

This module exposes a function that convert JPG image to PNG image. We used [nodejs](https://nodejs.org/en/), [express](https://expressjs.com/), [multer](https://www.npmjs.com/package/multer) and [webp-converter](https://www.npmjs.com/package/webp-converter).
Just clone the project and follow the steps.

## Steps

```sh
npm install
# or
nodemon App.js
```

### Simple example

```js
app.post("/", (req, res) => {
  upload(req, res, (err) => {
    if (err) throw err;

    console.log(req.file.path);

    var output_path = Date.now() + "result.png";

    const result = webp.cwebp(req.file.path, output_path, "-q 80");
    result.then((response) => {
      res.download(output_path);
    });
  });
});
```
