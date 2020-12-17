`
#### L29 examples
##### add refered link of fonts
Turn to [google fonts](https://fonts.google.com/) and search the quired font type. 
e.g. search type **Oxygen**, and copy the link of it and paste into the specific area
```
<head>
<link href="https://fonts.googleapis.com/css2?family=Oxygen&display=swap" rel="stylesheet">
</head>
```
##### view the synchronic web
open the command
```
$ browser-sync start --server --directory --files "*"
```
and the website position is 
```
 Local: http://localhost:3000
```
and the sync web is UI
```
UI: http://localhost:3001
```

#### L30-1 coding basics of navbar header

##### add the nav bar
add the header in the body 
```
  <header>
    <nav id="header-nav" class="navbar navbar-default">
      <div class="container">
      </div>
    </nav>
  </header>
```
find a **white line** at the top of the website, then edit the type of it in css
```
#header-nav{
	background-color: #f6b319;
	border-radius:0;
	border:0;
}
```
`border-radius` is the shape of this grid [border-radous detail](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius)

### place a symbol in the nav bar
find the **nav bar** details at [getbootstrap.com nav bar](https://getbootstrap.com/docs/5.0/components/navbar/)
```
<header>
    <nav class="header-nav" class="navbar navbar-default">
      <div class="container">
        <div class= "navbar-header">
            <a href="index.html" class="">
              <div class= "logo-box">
                <img src="../L29-images/restaurant-log_large.png" alt="logo-img">
              </div>
            </a>
        </div>
      </div>
    </nav>
  </header>
```
the related css file:
**How to adjust the img size to the given size**
The problem of adjust the size of this img is that:`div` the grid size 
e.g.`<div class= "logo-box">` in css file `.logo-box{} ` with absolute size of `	width: 150px;  height:150px;`.Then apply the **img** of `max-width: 100%;
    max-height: 100%;` to adjust to the given box size.The general idea follows [adjust img size](https://shazhenyu.blog.csdn.net/article/details/80403946?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromBaidu-2.control&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromBaidu-2.control)

	
```
.logo-box{
	width: 150px;
	height:150px;
	margin: 10px 15px 10px 0px;
}
.logo-box img{
	max-width: 100%;
    max-height: 100%;
}
```

ps: the `alt` means if the img can not show, the text will show on that place. The details of [<img> usage](https://www.w3school.com.cn/tags/tag_img.asp)

**how to edit multiple imgs size setting**
I use `.logo-box img{}` the **img** is set within the class of **`class= "logo-box"`**  The idea is inpired from [here](https://shazhenyu.blog.csdn.net/article/details/80403946?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromBaidu-2.control&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromBaidu-2.control)

#### L30-2 coding basics of Navbar Header
##### add the navbar-brand
- [pull-left](https://www.geeksforgeeks.org/pull-left-and-pull-right-classes-in-bootstrap-4/): we use it to make the tile show in the left top `class="pull-left visible-md"`
- [visible-md](https://getbootstrap.com/docs/4.0/migration/#responsive-utilities): we use it in this example to not show the log when in the small screen, `class="pull-left visible-md"`
- [text-decoration](https://www.w3schools.com/cssref/pr_text_text-decoration.asp): in this example we use ` text-decoration: none;` to eliminate the text type of this link
- [text transform](https://www.w3schools.com/cssref/pr_text_text-transform.asp): In this example ` text-transform: uppercase;` to change the brand name
- [vertical align](https://www.w3schools.com/cssref/pr_pos_vertical-align.asp)
```
<div class="container">
        <div class= "navbar-header">
          
            <a href="index.html" class="pull-left visible-md visible-lg">
              <div class= "logo-box">
                <img src="../L29-images/restaurant-logo_large.png" alt="logo">
              </div>
            </a>

             <div class="navbar-brand">
                <a href="index.html" ><h1>David Chu's China Bistro</h1></a>
                <p>
                  <img src="../L29-images/star-k-logo.png" alt="Kosher certification">
                  <span>Kosher Certified</span>
                </p>
              
            </div>
        </div>
```

and the relative css file
```
/**navbar brand **/
.navbar-brand {
  padding-top: 25px;
}

.navbar-brand h1 { /* Restaurant name */
  font-family: 'Lora', serif;
  color: #557c3e;
  font-size: 1.5em;
  text-transform: uppercase;
  font-weight: bold;
  text-shadow: 1px 1px 1px #222;
  margin-top: 0;
  margin-bottom: 0;
  line-height: .75;
}

.navbar-brand a:hover, .navbar-brand a:focus {
  text-decoration: none;
}
.navbar-brand p { /* Kosher cert */
  color: #000;
  text-transform: uppercase;
  font-size: .7em;
  margin-top: 15px;
}
.navbar-brand p span { /* Star-K */
  vertical-align: middle;
}
```
Here we look the css styles line by line:

