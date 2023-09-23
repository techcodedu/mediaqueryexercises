# Exercise 2

## Build a Responsive Navigation Menu with a Centered Brand Logo

### Objective:
The aim of this exercise is to craft a responsive navigation menu where the brand logo sits at the center, surrounded by two menu items on each side. Moreover, the navigation will overlay atop a striking background image, giving a chic and contemporary visual appeal. Through this exercise, you'll advance your aptitude in accurately positioning elements, while further refining your capabilities in designing responsive layouts via media queries.

### Step-by-step Instructions:

#### 1. **HTML Structure**:
- Begin by creating a fresh HTML file.
- Within the `body` section, incorporate a `nav` element labeled with the class `navigation`.
- Nested within the `navigation`, introduce a `div` identified by the class `menu-left`.
- Within `menu-left`, inject two anchor tags (`a` elements) symbolizing the left menu choices.
- Adjacent to `menu-left`, embed an `img` tag for the brand emblem, labeled with the class `brand-logo`.
- Pursuing the brand emblem, constitute a `div` tagged with the class `menu-right`.
- Inside `menu-right`, incorporate two anchor tags (`a` elements) that symbolize the right menu choices.

Your resultant HTML framework should be:

```html
<nav class="navigation">
    <div class="menu-left">
        <a href="#">Menu 1</a>
        <a href="#">Menu 2</a>
    </div>
    <img src="https://github.com/techcodedu/mediaqueryexercises/raw/main/brandlogo.png" alt="Brand Logo" class="brand-logo">
    <div class="menu-right">
        <a href="#">Menu 3</a>
        <a href="#">Menu 4</a>
    </div>
</nav>
```

**Explanation**: This architecture segregates our navigation into a trio of principal sectors: the left menu, brand emblem, and right menu. Each segment is encapsulated for ease of styling and accurate positioning.

#### 2. **Primary Styling and Background Image**:
- As an outset, appoint the provided background image to envelop the complete body.
- Introduce rudimentary styles for the navigation along with the menu options.

```css
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background-image: url('https://images.pexels.com/photos/10343461/pexels-photo-10343461.jpeg');
    background-size: cover;
    background-position: center;
    height: 100vh;
}

.navigation {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px 0;
}

.menu-left, .menu-right {
    display: flex;
    gap: 20px;
}

.brand-logo {
    height: 50px;
}
```

**Explanation**: Through Flexbox, the navigation naturally spaces its sub-elements. The `max-width` ensures the navigation remains constricted on expansive displays. The background image is designated to cover the viewport while being centralized.

#### 3. **Media Query for Adaptability**:

Considering that the screen's breadth diminishes, the menu components and logo may become constrained or even overlap. To counteract this, we shall fine-tune the layout for smaller screens.

```css
@media (max-width: 768px) {
    .navigation {
        flex-direction: column;
    }
    .menu-left, .menu-right {
        justify-content: center;
        margin: 10px 0;
    }
    .brand-logo {
        margin: 20px 0;
    }
}
```

**Explanation**: For displays with a width less than 768px, the navigation components are stacked vertically. The menu elements centralize themselves, and the brand logo secures an added margin for visual distinction.

---

**Initial output after applying the CSS rules**:

![Desktop View](https://github.com/techcodedu/mediaqueryexercises/raw/main/exercise2.png)

**Output post the application of the media query**:

![Mobile View](https://github.com/techcodedu/mediaqueryexercises/raw/main/mobile%20query.jpg)

