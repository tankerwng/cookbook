##100% height view

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

##[@font-face 语法](http://www.fontspring.com/blog/the-new-bulletproof-font-face-syntax)

```css
font-face {
	font-family: 'MyFontFamily';
	src: url('myfont-webfont.eot?#iefix') format('embedded-opentype'),
	     url('myfont-webfont.woff') format('woff'),
	     url('myfont-webfont.ttf')  format('truetype'),
	     url('myfont-webfont.svg#svgFontName') format('svg');
}
```

##[CSS Yellow Fade](http://snook.ca/archives/html_and_css/yellow-fade-technique-css-animations)

[:target](https://developer.mozilla.org/en/CSS/%3Atarget) // [@keyframes](https://developer.mozilla.org/en/CSS/@keyframes)

```css
:target {
    -webkit-animation: target-fade 3s 1;
    -moz-animation: target-fade 3s 1;
}

@-webkit-keyframes target-fade {
    0% { background-color: rgba(0,0,0,.1); }
    100% { background-color: rgba(0,0,0,0); }
}
@-moz-keyframes target-fade {
    0% { background-color: rgba(0,0,0,.1); }
    100% { background-color: rgba(0,0,0,0); }
}
```
