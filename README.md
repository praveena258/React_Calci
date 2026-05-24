# Ex04 Simple Calculator - React Project
## Date:24.05.26

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
calculator.jss
```
import React, { useState } from "react";
import "./calculator.css";

function Calculator() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const clearInput = () => {
    setInput("");
  };

  const calculateResult = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator-container">
      <div className="calculator">
        <h2>Simple Calculator</h2>

        <input
          type="text"
          value={input}
          readOnly
          className="display"
        />

        <div className="buttons">
          <button onClick={clearInput}>C</button>
          <button onClick={() => handleClick("/")}>/</button>
          <button onClick={() => handleClick("*")}>*</button>
          <button onClick={() => handleClick("-")}>-</button>

          <button onClick={() => handleClick("7")}>7</button>
          <button onClick={() => handleClick("8")}>8</button>
          <button onClick={() => handleClick("9")}>9</button>
          <button onClick={() => handleClick("+")}>+</button>

          <button onClick={() => handleClick("4")}>4</button>
          <button onClick={() => handleClick("5")}>5</button>
          <button onClick={() => handleClick("6")}>6</button>

          <button onClick={() => handleClick("1")}>1</button>
          <button onClick={() => handleClick("2")}>2</button>
          <button onClick={() => handleClick("3")}>3</button>

          <button onClick={() => handleClick("0")}>0</button>
          <button onClick={() => handleClick(".")}>.</button>
          <button onClick={calculateResult}>=</button>
        </div>
      </div>
    </div>
  );
}

export default Calculator;
```
calculator.css
```
body {
  margin: 0;
  padding: 0;
  background: #2f2f5f;
  font-family: Arial, sans-serif;

}

.calculator-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.calculator {
  background: white;
  padding: 20px;
  border-radius: 15px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
  width: 320px;
}

h2 {
  text-align: center;
  margin-bottom: 20px;
}

.display {
  width: 100%;
  height: 50px;
  font-size: 24px;
  text-align: right;
  margin-bottom: 15px;
  padding: 10px;
  border: 2px solid #ccc;
  border-radius: 8px;
  box-sizing: border-box;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 15px;
  font-size: 20px;
  border: none;
  background: #5985b5;
  color: white;
  border-radius: 8px;
  cursor: pointer;
}

button:hover {
  background: #0056b3;
}

@media (max-width: 500px) {
  .calculator {
    width: 90%;
  }

  button {
    font-size: 18px;
    padding: 12px;
  }
}
```

app.js
```
import React from "react";
import Calculator from "./calculator";

function App() {
  return <Calculator />;
}

export default App;
```
## OUTPUT
<img width="935" height="1057" alt="image" src="https://github.com/user-attachments/assets/9f74193d-093b-462b-909c-c3875cad9a5a" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
