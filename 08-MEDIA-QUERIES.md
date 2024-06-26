# Responsive design and CSS Media Queries

---

### The problem

As mobile devices and Desktops became widely available, developers had a problem... how do we create websites that look good on all screen sizes ?

### One approach

Early on, it was common to create separate stylesheets for different devices, or even completely different websites for each size.

### Enter responsive

These days, we tipically create ONE website and stylesheet that is able to respond to different device sizes and features.

---

## Media queries

Media queries allow us to modify our styles depending on particular parameters like screen width or device type.

![Alt text](./assets/mediaquery.png)

---

Let's do a little guided exercise :

- Create index.html, style.css etc. etc.
- Copy this code inside your body :

```html
<h1>I am on a :</h1>
<hr />
<h2 class="a">Mobile</h2>
<h2 class="b">Tablet</h2>
<h2 class="c">Laptop 13 inches</h2>
<h2 class="d">Laptop</h2>
<h2 class="e">Desktop</h2>
```

Instructions :

- On mobile the body should have a background `gold` and only the h2 `Mobile` should appear

- From 768px (tablet) : background : `pink` and only the h2 `Tablet` should apppear.

- From 1280px (laptop 13') : background : `chocolate` and only the h2 `Laptop 13 inches` should apppear.

- From 1440px (laptop) : background : `cadetblue` and only the h2 `Laptop` should apppear.

- From 1920px (desktop) : background : `cornflowerblue` and only the h2 `Desktop` should apppear.

Great ! Now :

- In your inspector, play with the responsiveness. Select different screen sizes and see the result. Play with the "responsive" GUI to increase and decrease the width of the viewport.

MAGIC ! The content changes relative to the viewport width !

---

Let's do another one :

- In a new project (index.html and style.css)
- Create a container to center the content in the page
- Inside of it, create a flex container and inside 6 divs.
- Give each div a width of 100% (it will take the maximum available space) and a height of 100px
- Give each div a different background color.
- Look at it in a laptop view (1440)
- In the inspector, play with the responsiveness.
- Look how small they get in a mobile size !!!!
- Let's stack them ! Use a media query to give the flex container a column direction on mobile and row direction on a bigger scree.
- TIP : Even tough we can use `max-width` in the media query, the highly recommended worflow is **mobile-first** ! So declare your css for mobile and then with media query use `min-width`.

---

Looks great ?
Let's change the code in order to use GRID now :

- Instead of a `display: flex `, use now a display grid.
- Give the template columns **two** `1fr`
- For tablet give **three** `1fr`
- For laptops give **six** `1fr` (think of the function `repeat`)

**Congratulations ! Give yourself a hug !**

![](https://media.giphy.com/media/u04bOWYPdInzmZCOqR/giphy.gif)
