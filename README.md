# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>DOM Manipulation Example</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
    }
    .highlight {
      color: white;
      background-color: darkblue;
      padding: 10px;
    }
  </style>
</head>
<body>
  <header>
    <h1 id="main-title">Welcome to My Page</h1>
  </header>

  <main>
    <section>
      <p id="dynamic-text">This text will change dynamically.</p>
      <button onclick="changeText()">Change Text</button>
      <button onclick="changeStyle()">Change Style</button>
    </section>

    <section>
      <button onclick="addElement()">Add Element</button>
      <button onclick="removeElement()">Remove Element</button>
      <div id="container"></div>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 JavaScript DOM Practice</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>



// Change text dynamically
function changeText() {
  const textElement = document.getElementById("dynamic-text");
  textElement.textContent = "The text has been changed using JavaScript!";
}

// Change style dynamically
function changeStyle() {
  const textElement = document.getElementById("dynamic-text");
  textElement.classList.toggle("highlight");
}

// Add a new element
function addElement() {
  const container = document.getElementById("container");
  const newPara = document.createElement("p");
  newPara.textContent = "I am a new paragraph added to the DOM!";
  newPara.id = "new-paragraph";
  container.appendChild(newPara);
}

// Remove the newly added element
function removeElement() {
  const element = document.getElementById("new-paragraph");
  if (element) {
    element.remove();
  }
}

