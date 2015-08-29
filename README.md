# Tema News/Info NovelVisual

Tema wordpress ini dibangun menggunakan [Sage](https://github.com/roots/sage).

## Requirements

| Minimal         | Cara cek versi | Cara Install |
| --------------- | -------------- | ------------ |
| PHP >= 5.4.x    | `php -v`       | [php.net](http://php.net/manual/en/install.php) |
| Node.js 0.12.x  | `node -v`      | [nodejs.org](http://nodejs.org/) |
| gulp >= 3.8.10  | `gulp -v`      | `npm install -g gulp` |
| Bower >= 1.3.12 | `bower -v`     | `npm install -g bower` |

For more installation notes, refer to the [Install gulp and Bower](#install-gulp-and-bower) section in this document.

## Features

TO DO features

## Instalasi

Clone repo git nya - `git clone https://github.com/pikarin/wp-theme-nv-news.git` ke dalam folder tema wordpress kemudian rename direktori ke `novelvisual-news` (atau bebas).

Kalau tidak menggunakan [Bedrock](https://github.com/roots/bedrock), maka tambahkan kode dibawah ke dalam `wp-config.php` di instalasi develpment mu:

```php
define('WP_ENV', 'development');
```

## Theme development

Install [node.js](http://nodejs.org/download/) jika belum ada node.js di komputer.

### Install gulp dan Bower

Untuk update npm ke versi terbaru: `npm install -g npm@latest`.

Dari dalam command line:

1. Install [gulp](http://gulpjs.com) dan [Bower](http://bower.io/) secara global dengan `npm install -g gulp bower`
2. Navigate (masuk) ke dalam direktori tema, kemudian run `npm install`
3. Run `bower install`

Sekaram kamu telah memiliki dependensi yang dibutuhkan untuk run proses build nya.

### Gulp command yang tersedia

* `gulp` — Compile dan optimize file yang di dalam direktori assets
* `gulp watch` — Akan meng-Compile assets ketika file change (otomatis compile ketika save)
* `gulp --production` — Compile assets untuk production (no source maps).

### Menggunakan BrowserSync

Untuk menggunakan BrowserSync saat run command `gulp watch` kamu harus edit `devUrl` yang terdapat pada `assets/manifest.json` (barisan paling bawah) dengan hostname local development mu.

Contoh, local development URL adalah `http://localhost/wordpress` maka update filenya jadi:
```json
...
  "config": {
    "devUrl": "http://localhost/wordpress"
  }
...
```

## Documentation

Dokumentasi dari Sage [https://roots.io/sage/docs/](https://roots.io/sage/docs/).