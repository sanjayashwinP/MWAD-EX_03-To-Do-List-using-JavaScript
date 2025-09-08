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
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>My To-Do List</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="box">
    <h1>📝 Sanjay's To-Do App</h1>

    <input type="text" id="search" placeholder="Search...">
    <div class="inputs">
      <input type="text" id="taskInput" placeholder="Enter task here...">
      <select id="priority">
        <option value="low">🟢 Low</option>
        <option value="medium">🟡 Medium</option>
        <option value="high">🔴 High</option>
      </select>
      <input type="date" id="date">
      <button id="addBtn">Add</button>
    </div>
    <p id="counter">Tasks: 0 | Completed: 0</p>
    <ul id="list"></ul>
    <button id="clearBtn">Clear Completed</button>
  </div>
  <script src="script.js"></script>
</body>
</html>
```
### style.css
```
body {
  background: #4503aeba;
  color: #111;
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  min-height: 100vh;
  padding: 40px;
}

.box {
  background: #fff;
  color: #111;
  padding: 20px;
  border-radius: 12px;
  width: 420px;
  box-shadow: 0px 5px 15px rgba(0,0,0,0.15);
}

h1 {
  text-align: center;
  margin-bottom: 15px;
}

#search {
  width: 100%;
  padding: 10px;
  margin-bottom: 15px;
  border-radius: 6px;
  border: 1px solid #aaa;
  box-sizing: border-box;
  font-size: 14px;
}

/* input area */
.inputs {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 15px;
}

.inputs input[type="text"] {
  flex: 2;
}

.inputs select {
  flex: 1;
}

.inputs input[type="date"] {
  flex: 1.2;
}

.inputs button {
  flex: 0.8;
  min-width: 70px;
}

input[type="text"], input[type="date"], select {
  padding: 8px;
  border: 1px solid #aaa;
  border-radius: 6px;
  box-sizing: border-box;
  font-size: 14px;
}

button {
  background: #4a76f7;
  color: #fff;
  border: none;
  padding: 8px 12px;
  border-radius: 6px;
  cursor: pointer;
  font-size: 14px;
}

button:hover {
  background: #3455c6;
}

#counter {
  margin: 10px 0;
  font-size: 14px;
  font-weight: bold;
  text-align: center;
}

#list {
  list-style: none;
  padding: 0;
  margin: 15px 0;
}

#list li {
  background: #f9f9f9;
  margin-bottom: 8px;
  padding: 10px 12px;
  border-radius: 6px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 14px;
}

#list li.low { border-left: 5px solid green; }
#list li.medium { border-left: 5px solid orange; }
#list li.high { border-left: 5px solid red; }

#list li.done {
  text-decoration: line-through;
  background: #d3ffd3;
}

#list .doneBtn, #list .editBtn, #list .delBtn {
  background: transparent;
  border: 1px solid rgba(0,0,0,0.15);
  padding: 3px 7px;
  margin-left: 5px;
  border-radius: 6px;
  cursor: pointer;
  font-size: 13px;
}
#list .doneBtn:hover, #list .editBtn:hover, #list .delBtn:hover {
  background: #eee;
}

#clearBtn {
  width: 100%;
  margin-top: 10px;
  padding: 10px;
  border-radius: 6px;
  font-weight: bold;
}
```
### script.js
```

```
## OUTPUT


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
