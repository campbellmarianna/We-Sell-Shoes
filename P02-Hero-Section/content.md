---
title: "Creating the Hero!"
slug: creating-the-hero
---


Here comes one of the coolest parts of the landing page. We will build it step by step so you can get a good idea of how to replicate this in future projects.

# Let's create the Hero!
The first thing we will do is create the full-sized ```div``` with a nice background image.

```HTML
<!--closing div for navbar-->
</div>

<div class="hero">


</div>

```

Next we will style our Hero div a bit.

```css
...

.nav-btn.right:hover {
  transform: scale(1.1) rotate(3deg);
}

Copy everything below this line
/*******************
HERO
*******************/

.hero {
  height: calc(99vh - 50px);
  width: 100%;
  background: linear-gradient(rgba(44, 62, 80,.6), rgba(44, 62, 80,.6)), url('https://image.ibb.co/nyaXSK/IMG_5247.jpg');
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}
```

The height has a calc property, taking in 99vh - 50px. This just means, we want it to be 99% of the view height, minus 50 pixels. We do this because we want to show a little bit of the next part so that people will know they should scroll downward.

We also make use of linear-gradients to darken the photo a bit. This is so when we add text it will stand out a little better.

You are more than welcome to change the background image as well.

# Adding some text
We're going to add in a big bold heading that tells the user exactly what our website is about. Lets add this markup!

```HTML
<div class="hero-overlay-text">
  <h1>We Sell Shoes!</h1>
  <a class="call-to-action-btn" href="#">Shop Now</a>
</div>

```
Here we have a parent Div, a heading, and a call to action button.

We can now add the following styles:

```CSS

.hero {
  /*you already have these*/
}

.hero-overlay-text {
  z-index: 5;
  height: calc(100vh - 50px);
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: white;
  font-family: 'Roboto', sans-serif;
}

.hero-overlay-text h1 {
  margin-top: 0rem;
  font-size: 10rem;
  font-family: 'Roboto', sans-serif;
  font-weight: 300;
}

.call-to-action-btn {
  background-color: rgba(253, 253, 253, 1);
  color: #616161;
  border-radius: 40px;
  border: 1px solid #C1C1C1;
  padding: 10px 0;
  text-decoration: none;
  width: 15rem;
  text-align: center;
  transition: all 200ms;
  box-shadow: 0 2px 0px rgba(0,0,0,.3);
}

.call-to-action-btn:hover {
  /*transform: scale(1.02);*/
  box-shadow: 0 2px 1px rgba(0,0,0,.3);
}
```

Before we do anything else, take a look at some of the font-family properties we use.

In order to use the roboto font, we need to import it from google fonts.

We can import google fonts by placing another link tag in our head above our styles link.

```html
<head>

...

<!--add this above the stylesheet link-->
<link href="https://fonts.googleapis.com/css?family=Oswald:200,300,400|Roboto:100,200,300,400" rel="stylesheet">

<!--you already have this one -->
<link rel="stylesheet" href="styles.css">
</head>

```

Now we are able to use the roboto font.

Your page should now look something like this:

![Hero Image Complete](images/hero2.png "Completed hero image")

# onward
We've now got a pretty nice looking hero section. In the next section we will add a section to show off our clients.
