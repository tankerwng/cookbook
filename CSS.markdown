## 100% height view

```css
/* =======
   html
   |- body
      |- #container
   ======= */

html {height: 100%}
body {height: 100%}
#container {height: 100%}
```

## [@font-face 语法](http://www.fontspring.com/blog/the-new-bulletproof-font-face-syntax)

```css
font-face {
	font-family: 'MyFontFamily';
	src: url('myfont-webfont.eot?#iefix') format('embedded-opentype'),
	     url('myfont-webfont.woff') format('woff'),
	     url('myfont-webfont.ttf')  format('truetype'),
	     url('myfont-webfont.svg#svgFontName') format('svg');
}
```
