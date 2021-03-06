[![EnterIN](http://enterin.github.io/img/b-enterin.jpg)](http://enterin.github.io)

### Write HTML logic
```html
<div id="enterin-wrapper">
   <div class="enterin-slide slide1"></div>
   <div class="enterin-slide slide2"></div>
   <div class="enterin-slide slide3"></div>
   <div class="enterin-slide slide4"></div>
   <div class="enterin-slide slide5"></div>
</div>

<div id="enterin-ctrl">
   <a href="javascript:;" data-enterin="1">Slide 1</a>
   <a href="javascript:;" data-enterin="2">Slide 2</a>
   <a href="javascript:;" data-enterin="3">Slide 3</a>
   <a href="javascript:;" data-enterin="4">Slide 4</a>
   <a href="javascript:;" data-enterin="5">Slide 5</a>
</div>
```

### Set property CSS rules

Example: 

```css
#enterin-wrapper,
#enterin-wrapper .enterin-slide
{
   width:100%;
   height:100%;
   min-height:100%;
}

#enterin-wrapper .enterin-slide.slide1 {
   background: url('path/to/transparent/image1.png') center center no-repeat transparent;
   background-size: 80%;
}
#enterin-wrapper .enterin-slide.slide2 {
   background: url('path/to/transparent/image2.png') center center no-repeat transparent;
   background-size: 80%;
}
#enterin-wrapper .enterin-slide.slide3 {
   background: #999999;
}
...

```

### Add jQuery and EnterIN .js at end of document

```html
   ...
   <script src="path/to/js/jquery.min.js"></script>
   <script src="path/to/js/jquery.enterin.min.js"></script>
</body>
```

### Call EnterIN

```html
	<script>
	
	jQuery("#enterin-wrapper").enterin({
	   controllers: '#enterin-ctrl',
	   maxScale: 20,
	   effectTime: 3.0,
	   ease: 'linear',
	   endCallback: function(current_index) {
	      // your code here
	   }
	});
	
	</script>
```

© 2013 Gianfilippo Balestriero under [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)
