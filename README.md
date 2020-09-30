# Naming Classes

Before thinking about the class name, take your time and choose a good name for an HTML element.
Use meaningful names for your Ids and Classes. They should be short, descriptive and represent only one concept. It’ll make your HTML clearer and the styling process easier.
Don’t you think it’d be better if you named your class “wrapper” instead of “wpr”?

```html
<!-- DO NOT DO THIS !! -->
<h2 class="CardTitle"></h2>
<h2 class="cardtitle"></h2>
<h2 class="ct"></h2>

<!-- DO THIS -->
<h2 class="card-title"></h2>
```

<img src="https://miro.medium.com/max/640/1*RrFFM_EwTp3RVKUFuViqFw.gif" />

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
# Use Whitespace
Many people write smashed-together code without using white spaces. The result? It’s like reading a book with no punctuation or paragraphs.
leave an empty line between every big section

# Sass Architecture Structure

I already made a <a href="https://github.com/0x1e0000/sass-structure.git">repository</a> for this

# Comments
Your code won’t be easier to understand just because you add comments everywhere. You can use them to make things a bit more clear (for example, to show you’re closing a div after many lines of code). But don’t comment things that are obvious or code that is badly written.
**“Don’t comment bad code. Rewrite it.” — Brian W. Kernighan**
```html
<!-- [BEGIN] About Us -->
<section class="about-us">
	...
</section>
<!-- [END] About Us -->
```

# Icons
Every clickable icon should be an SVG element, so we can give it a style with CSS whenever we hover or click over it.

# Clean Code
Writing clean code should be one of your biggest concerns. You don’t want to mess up the foundations of the site. It’s just wrong and embarrassing.
Your code reflects the kind of developer you are

**“Clean code is a code that is written by someone who cares” — Michael Feathers**


Bad HTML Code:
```html
  <footer id="footer-bottom">
<div class="container">
 <div class="row">
 <div id="footer-copyrights" class="col-md-6">
<p> &copy; 2018 All Rights Reserved.</p>
  </div>
  <div id="footer-menu" class="col-md-6">
  <ul><li>Home</li>
  <li>Team</li>
  <li>Pricing</li></ul>
</div>
</div>
</div>
  </footer>
```

Better HTML Code:

```html
<!-- [BEGIN] Footer -->
<footer id="footer-bottom">
  <div class="container">
    <div class="row">
      <div id="footer-copyrights" class="col-md-6">
        <p> &copy; 2018 All Rights Reserved.</p>
      </div>
      <div id="footer-menu" class="col-md-6">
        <ul>
          <li>Home</li>
          <li>Team</li>
          <li>Pricing</li>
        </ul>
      </div>
    </div>
  </div>
</footer>
<!-- [END] Footer -->
```
<br /><br />
Bad HTML Code:
```html
<div id="content">
  <div class="headline">Headline</div>
  <div class="subtitle">Subtitle</div>
  <div class="post">Post Content</div>
  <div class="list"> 
    <ul> 
      <li>Element 1</li> 
      <li>Element 2</li>
    </ul> 
  </div>
</div> <!-- end content div -->
```

Better HTML Code:

```html
<!-- [BEGIN] Content -->
<secton id="content">
  <h1>Headline</h1>
  <h2>Subtitle</h2>
  <p>Post Content</p>
  <ul> 
    <li>Element 1</li> 
    <li>Element 2</li>
  </ul> 
</secton>
<!-- [BEGIN] Content -->
```
# !important
Avoid using too many !important

All !important does is increase specificity. To avoid using !important, all you need to do is increase specificity.

for example:
```html
<div class="card">
	...
</div>
```
```css
/* weak */
div{color:red;}
/* strong */
.card{color:red;}
/* much stronger */
div.card{color:red;}
```
