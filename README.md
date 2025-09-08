# MWAD-EX_03-To-Do-List-using-JavaScript
## Date: 08/09/2025
## Name: Sanjay Ashwin P
## Reg no: 212223040181

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
### index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sanjay's To-Do App</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="box">
    <h1>📝Sanjay's To-Do List</h1>

    <div class="inputs">
      <input type="text" id="taskInput" placeholder="Enter task...">
      <button id="addBtn">Add</button>
      <button id="clearAll">Clear All</button>
    </div>

    <p id="counter">Pending: 0 | Completed: 0</p>

    <ul id="list"></ul>
  </div>

  <script src="script.js"></script>
</body>
</html>
```
### style.css
```
body {
  background: #5c07d3;
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  min-height: 100vh;
  padding: 40px;
}

.box {
  background: #fff;
  padding: 20px;
  border-radius: 10px;
  width: 370px;
  box-shadow: 0px 5px 10px rgba(0,0,0,0.1);
}

h1 {
  text-align: center;
  margin-bottom: 15px;
}

.inputs {
  display: flex;
  gap: 5px;
  margin-bottom: 15px;
}

#taskInput {
  flex: 1;
  padding: 8px;
  border: 1px solid #aaa;
  border-radius: 5px;
}

button {
  background: #4a76f7;
  color: #fff;
  border: none;
  padding: 8px 12px;
  border-radius: 5px;
  cursor: pointer;
}
button:hover {
  background: #3455c6;
}

#clearAll {
  background: #f44336;
}
#clearAll:hover {
  background: #c62828;
}

#counter {
  text-align: center;
  font-weight: bold;
  margin: 10px 0;
}

#list {
  list-style: none;
  padding: 0;
  margin: 0;
}

#list li {
  background: #f9f9f9;
  margin-bottom: 8px;
  padding: 8px 10px;
  border-radius: 5px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

#list li.done {
  text-decoration: line-through;
  background: #d3ffd3;
}

#list button {
  background: transparent;
  border: none;
  cursor: pointer;
  font-size: 14px;
}
#list button:hover {
  color: red;
}
```
### script.js
```
const taskInput = document.getElementById("taskInput");
const addBtn = document.getElementById("addBtn");
const taskList = document.getElementById("list");
const counter = document.getElementById("counter");
const clearAllBtn = document.getElementById("clearAll");

addBtn.addEventListener("click", addTask);

taskInput.addEventListener("keypress", (e) => {
  if (e.key === "Enter") addTask();
});

// Clear All button
clearAllBtn.addEventListener("click", () => {
  taskList.innerHTML = "";
  updateCounter();
});


function addTask() {
  const text = taskInput.value.trim();
  if (text === "") {
    alert("Please enter a task!");
    return;
  }

  const li = document.createElement("li");

  const span = document.createElement("span");
  span.textContent = text;

  const doneBtn = document.createElement("button");
  doneBtn.textContent = "✔";
  doneBtn.addEventListener("click", () => {
    li.classList.toggle("done");
    updateCounter();
  });

  const editBtn = document.createElement("button");
  editBtn.textContent = "✎";
  editBtn.addEventListener("click", () => {
    const newText = prompt("Edit your task:", span.textContent);
    if (newText !== null && newText.trim() !== "") {
      span.textContent = newText.trim();
    }
  });


  const delBtn = document.createElement("button");
  delBtn.textContent = "✖";
  delBtn.addEventListener("click", () => {
    li.remove();
    updateCounter();
  });

  li.appendChild(span);
  li.appendChild(doneBtn);
  li.appendChild(editBtn);
  li.appendChild(delBtn);

  taskList.appendChild(li);

  taskInput.value = "";
  updateCounter();
}

function updateCounter() {
  const total = taskList.getElementsByTagName("li").length;
  const completed = taskList.querySelectorAll(".done").length;
  const pending = total - completed;
  counter.textContent = `Pending: ${pending} | Completed: ${completed}`;
}
```
## OUTPUT


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
