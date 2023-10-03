## CSS Solar System Visualization

This project offers a visual representation of our Solar System, showcasing the sun and the planets revolving around it. The animation is made using pure CSS3, which results in smoother transitions and reduced load on the browser. This README provides a detailed understanding of the code and its functionality.

### Table of Contents

- [Project Structure](#project-structure)
- [HTML Structure](#html-structure)
- [CSS Styling](#css-styling)
- [JavaScript Functionality](#javascript-functionality)
- [Keyframes & Animation](#keyframes-animation)

### Project Structure

The project consists of:

1. An HTML file (`index.html`) which defines the structure.
2. A CSS file (`styles.css`) that provides the design and animation.
3. Images for each planet in the `Images` directory.

### HTML Structure

The solar system is structured using nested `<div>` elements.

1. The `solar-system-wrapper` centers the entire solar system on the screen.
2. The `solar-system-container` holds all the planets and the sun.
3. Each planet, including the sun, has its own designated `<div>`.
4. Planets are wrapped inside their corresponding orbits.

### CSS Styling

1. **General Styling**: The `body` and `html` are set with a `background-color` of `#212121` to simulate space, with default margins and paddings removed.
2. **Solar System Centering**: The solar system is centered using flex properties in the `.solar-system-wrapper`.
3. **Orbits**: They use `border-radius: 50%` to make them circular, and are positioned absolutely with `transform-origin` set to the center to allow rotation.
4. **Planets**: They are styled using the `.planet` class with variations depending on the planet. Each planet is given a specific size and placed within its orbit. Each planet rotates on its path defined by its parent orbit.
5. **Sun**: Placed at the center of the system. It has a shadow effect to give a glowing appearance.

### JavaScript Functionality

A small script is run once the window loads to set the `zoom` property of the body. This ensures that the entire solar system fits within the viewport.

```javascript
window.onload = function() {
    document.body.style.zoom = "25%";
}
```

### Keyframes & Animation

1. **Orbit Rotation (`@keyframes Orbit`)**: This makes the orbits rotate around the sun, simulating planet rotation.
2. **Planet Correct (`@keyframes correct`)**: This counter-rotates the planets to ensure they don't spin around their own axis while moving around the sun. They should always face the same direction.
3. **Planet Visibility (`@keyframes hidePlanet`)**: This swaps the z-index at the midpoint of the rotation to handle overlapping orbits and ensure planets are visible only when they should be.

---

For a developer or an enthusiast trying to understand or enhance this project, this guide offers insights into the code's structure and functionality. You can fork or clone the repository and try adding more celestial objects, animations, or interactivity. Enjoy exploring the digital universe!
