# Naming Classes
Before thinking about the class name, take your time and choose a good name for an HTML element.

```html
<!-- DO NOT DO THIS !! -->
<h2 class="CardTitle"></h2>
<h2 class="cardtitle"></h2>

<!-- DO THIS -->
<h2 class="card-title"></h2>
```

**Try BEM**

It’s one of the most commonly used conventions by now.

- It looks really weird at first glance, don’t be afraid

```html
<!-- (double underscore __) means children of the element. -->
<!-- (double dash --) means variation of the element. -->
<div class="card">
	<h2 class="card__title">title</h2>
	<div class="card__body">
		<p class="card__body__paragraph">Paragraph</p>
		<a class="card__body__button--primary" href="#">Read more</a>
		<a class="card__body__button--danger" href="#">Delete</a>
	</div>
	<div class="card__footer">
		<a class="card__footer__icon">Facebook</a>
		<a class="card__footer__icon">Instagram</a>
		<a class="card__footer__icon">Twitter</a>
	</div>
</div>
```

# Sass structure


# Comments


# Icons


# Clean Code


# Avoid !important
