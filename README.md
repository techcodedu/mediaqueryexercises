# Exercise 1

## Build a Responsive Card Layout

### Objective:
Introduce foundational techniques of Flexbox, CSS Grid, and media queries to craft a responsive card layout. By the end, learners should be able to construct adaptable layouts for various screen sizes.

### Step-by-step Instructions:

#### 1. **HTML Structure**:
- Create a new HTML file.
- Within the body, add a `div` with the class `card-container`.
- Within the `card-container`, add three `divs` each with the class `card`.
- Each `card` should contain:
  - An `h2` for the card title.
  - A `p` for the card description.
  - An `img` for the card image.

**Explanation**: This structure lays the foundation for our design. The `card-container` will manage individual card placements, while each `card` houses a title, description, and image.

#### 2. **Initial Styling**:
In your CSS, apply the following styles:

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

**Explanation**: This primary styling ensures the cards have a consistent look. The `box-sizing` rule simplifies element sizing by integrating padding and border into the total width and height.

#### 3. **Flexbox for Card Container**:
Add this CSS:

```css
.card-container {
    display: flex;
    justify-content: space-between;
}
```

**Explanation**: Using Flexbox on the `card-container` naturally aligns its child cards in a row. The `justify-content: space-between;` maximizes space between each card.

#### 4. **CSS Grid for Card Content**:
Modify the `.card` class in your CSS:

```css
.card {
    display: grid;
    grid-gap: 10px;
    grid-template-rows: auto auto 1fr;
}
```

**Explanation**: By converting the `card` display to grid, you can organize its contents more effectively. `grid-template-rows` defines rows for the title, description, and image, ensuring a flexible layout.

#### 5. **Fit the Image in the Card**:

Adjust the `.card img` selector:

```css
.card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    display: block;
}
```

**Explanation**: This makes the image in each card responsive. `object-fit: cover;` ensures the image scales and crops to fill the card without altering its original aspect ratio.

**Outcome**: After implementing the CSS rules, your layout should resemble this visual: ![Normal Screen Result](https://github.com/techcodedu/mediaqueryexercises/blob/main/normal%20screen.PNG).

#### 6. **Media Query for Responsiveness**:

Incorporate this media query:

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

**Explanation**: The media query activates for screens below 768px, typical for tablets and mobile devices. Cards stack vertically with `flex-direction: column;` and stretch across the container width.

**Outcome**: On screens under 768 pixels, your layout should align with this visual: ![Smartphone Screen Result](https://github.com/techcodedu/mediaqueryexercises/blob/main/smartphone.PNG).

---

# Challenge:

## Redesign the Card Layout for Mobile

### Objective:
Using the knowledge you've gained, modify the `.card` layout for screens less than 768px. You're not being given the exact steps. Instead, you have the desired outcome and a reference to guide your CSS changes.

**Expected Result**: Your card layout for smaller screens should look like this visual:![Challenge Result](https://github.com/techcodedu/mediaqueryexercises/blob/main/exercise.PNG).

**Hints**:
1. You'll continue working within the media query for screens below 768px.
2. Make modifications to the `.card` layout using CSS Grid properties.
3. Adjust elements within the card (`h2`, `p`, `img`) to achieve the expected layout.

Good luck!
