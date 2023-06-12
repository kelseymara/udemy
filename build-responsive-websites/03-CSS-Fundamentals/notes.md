# HTML fundamentals notes continued 
from https://adp-gptlearning.udemy.com/course/design-and-develop-a-killer-website-with-html5-and-css3/?learning_path_id=601838#overview

## Skeleton 
```HTML
<!DOCTYPE html>
<html lang="en>
    <head>
    <meta charset="UTF-8"/>
    <title>The Basic Language of the Web: HTML</title>
    </head>

    <body>

    <h1>The Code Magazine</h1>
    <p>This is a paragraph</p>

    </body>

</html>

```

## Image
```HTML
<img src="images/post-img.png"
    alt= "HTML code on a screen"
    width= "500"
    height= "200"
    >
```
## Link  (anchor element with href)
```HTML
<a href="https://developer.mozilla.org/en-US/docs/Web/HTML">MDN Web Docs</a>
```
## Open URL in new tab 
```HTML
<a href="https://developer.mozilla.org/en-US/docs/Web/HTML">
target="_blank"
MDN Web Docs</a>
```
## Link to internal page 
```HTML
<a href="blog.html">Blog</a>
```
## Placeholder Link
```HTML
<a href="#">Challenges</a>
```

## Navigation Bar
```HTML
    <nav>
    <a href="blog.html">Blog</a>
    <a href="#">Challenges</a>
    <a href="#">FlexBox</a>
    <a href="#">CSS Grid</a>
    </nav>
```

## Header
```HTML
    <header>
    <h1>The Code Magazine</h1>

    <nav>
    <a href="blog.html">Blog</a>
    <a href="#">Challenges</a>
    <a href="#">FlexBox</a>
    <a href="#">CSS Grid</a>
    </nav>
    
    </header>
```
## Footer
```HTML
<footer>
</footer>
```

## Inline CSS (avoid)
```HTML
<h1 style="color: blue"The Code Magazine</h1>
```

## Link HTML and CSS files
```HTML
<link href="style.css" rel="stylesheet"/>   
```

## ID (can not use the same ID more than once)
index.html
```HTML
<p id="author">Posted by <strong>Laura Jones</strong> on Monday, June 21st 2027</p>
```
style.css
```CSS
#author{
    font-size:italic;
}
```

## class
```HTML
<p class="related-author>Author One</p>
<p class="related-author>Author Two</p>
<p class="related-author>Author Three</p>
```
```
.related-author{
    font-size:18px;
    font-weight:bold;
}
```

## border
```CSS
border: 5px solid #1098ad;
```

## How Inheritance Works
HTML
```HTML
<body>
    <nav>
        This is the navigation
    </nav>

    <h1>My website</h1>

    <p>
        Paragraph text
    </p>
</body>
```
CSS- styles for body element
```CSS
body{
    color:grey;
    font-size: 16px;
    font-faimly: sans-serif;

    border-top: 10px solid #1098ad;
}
```
- The body element is the parent element of the 3 elements (nav,header,paragraph)
- So therefore to inheritance, the 3 elements get access to all of the body properties (not all properties get inherited here- mostly the properties related to text)

Add new rule for H1 element: 
```CSS
h1{
    color: blue;
    font-size: 32px;
    text-transform: uppercase;
}
```
What happens now: 
- these 2 declarations <strong>override the inherited styles</strong>, therefore for H1 the color is no longer grey and the font size is no longer 16px. instead, it is blue and 32px; 

Another example: 
