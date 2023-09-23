# Exercise 1

## Build a Responsive Card Layout

### Objective:
The goal of this exercise is to acquaint you with the foundational techniques of Flexbox, CSS Grid, and media queries by creating a responsive card layout. Upon completing this exercise, you should be adept at crafting adaptable layouts for various screen sizes.

### Step-by-step Instructions:

#### 1. **HTML Structure**:
- Create a new HTML file.
- Inside the body, add a `div` with the class `card-container`.
- Inside the `card-container`, create three `divs` with the class `card`.
- Each `card` will contain:
  - An `h2` for the card title.
  - A `p` for the card description.
  - An `img` for the card image.

**Explanation**: This structure serves as the scaffold for our layout. The outer `card-container` will manage the placement of individual cards, while each `card` will host a title, description, and image.

#### 2. **Initial Styling**:
Add the following styles to your CSS:

```css
* {
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    margin: 20px;
    padding: 0;
}

.card {
    border: 1px solid #ccc;
    padding: 20px;
    width: 300px;
}
```

**Explanation**: This basic styling ensures a consistent appearance for the cards. The `box-sizing` rule makes it simpler to size elements, as it incorporates padding and border into the element's total width and height.

#### 3. **Flexbox for Card Container**:
Append the following CSS:

```css
.card-container {
    display: flex;
    justify-content: space-between;
}
```

**Explanation**: By employing Flexbox on the `card-container`, its child elements (cards) will naturally line up in a row. The property `justify-content: space-between;` ensures that the cards distribute themselves evenly across the container, maximizing space between them.

#### 4. **CSS Grid for Card Content**:
Update the `.card` class in your CSS:

```css
.card {
    display: grid;
    grid-gap: 10px;
    grid-template-rows: auto auto 1fr;
}
```

**Explanation**: Shifting the `card`'s display to grid allows for precise arrangement of its contents using CSS Grid. The rows for title, description, and image are defined with `grid-template-rows`, ensuring a dynamic, adaptable layout for each card's contents.

#### 5. **Media Query for Responsiveness**:
Incorporate the following media query to your CSS:

```css
@media (max-width: 768px) {
    .card-container {
        flex-direction: column;
        align-items: stretch;
    }

    .card {
        width: 100%;
        margin-bottom: 20px;
    }
}
```

**Explanation**: This media query activates when the viewport width drops below 768px, typically on tablets and mobile devices. Within this rule, the cards will stack vertically due to the `flex-direction: column;`, and each card will expand to fit the container's full width.

#### 6. **Fit the Image in the Card using `object-fit`**:

Amend the `.card img` selector in your CSS:

```css
.card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    display: block;
}
```

**Explanation**: This rule ensures images within cards adapt responsively. The `object-fit: cover;` property ensures the image scales and crops (if necessary) to cover the entire card without distorting its aspect ratio.
