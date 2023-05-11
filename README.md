# HexColor-ColorGenerator

This repository contains a simple web page that generates random hex color codes and changes the background color of the page accordingly. The project is named "Hex Color".

## Functionality

The `changeColor()` function generates a random hex color code by selecting random characters from an array of hex numbers. It then sets the generated hex code as the inner HTML of an element with the id "hex-code" and changes the background color of the `document.body` element.

## Usage

To use the hex color generator, follow these steps:

1. Include the HTML and CSS files in your project.
2. Add the following HTML markup to your webpage:

```html
<div class="project">
  <div class="section">
    <h2>Hex Color Generator</h2>
    <button onclick="changeColor()">Generate Color</button>
    <p id="hex-code"></p>
  </div>
</div>
```

3. Include the provided CSS styles in your project to ensure proper styling of the elements.

## Script

```javascript
function changeColor() {
  var hex_numbers = ["0","1","2","3","4","5","6","7","8","9","A", "B", "C", "D", "E", "F"];

  var hexcode = '';

  for (var i = 0; i < 6; i++) {
    var random_index = Math.floor(Math.random() * hex_numbers.length);
    hexcode += hex_numbers[random_index];
  }

  document.getElementById("hex-code").innerHTML = hexcode;
  document.body.style.backgroundColor = '#' + hexcode;
}
```

## CSS Styles

```css
/* Base Styles */
body {
  font-family: 'Times New Roman', Times, serif;
}

.project {
  width: 95%;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  transition: all 0.4s ease;
}

.section {
  width: 100%;
  text-align: center;
}

/* Header Styles */
.section h2 {
  margin-top: 20px;
  font-size: 40px;
  font-family: 'Times New Roman', Times, serif;
}

/* Button Styles */
.section button {
  margin-top: 20px;
  cursor: pointer;
  background-color: grey;
  padding: 20px;
  text-transform: uppercase;
  user-select: none;
  color: white;
}
```

Feel free to customize the styles and integrate this hex color generator into your project. Enjoy!
