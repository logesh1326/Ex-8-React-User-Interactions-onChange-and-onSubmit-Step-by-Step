# Ex. 8 React User Interactions: onChange and onSubmit — Step by Step

## Exercise Number
Exercise 8

## Subject
AI1067 - Modern Web Application Development (React JS Lab)

## Student Details
- **Name:** LOGESH S
- **Roll No:** 2305001014
- **Department:** B.Tech CSE
- **College:** IST, NMV University

## Objective
React JS Lab Exercise

## Description
Ex. 8 React User Interactions: onChange and onSubmit — Step by Step 
React forms mainly use onChange and onSubmit to handle user interactions. 
User enters data 
      ↓ 
   onChange 
      ↓ 
Update React state 
      ↓ 
User clicks Submit 
      ↓ 
   onSubmit 
      ↓ 
Validate / Process data 
 
1. onChange Event 
What is onChange? 
onChange is triggered whenever the value of an input element changes. 
Example: 
<input onChange={handleChange} /> 
It is commonly used with: 
• Text boxes 
• Email fields 
• Password fields 
• Checkboxes 
• Select/dropdown elements 
 
2. Step 1 — Create State 
First, import useState: 
import { useState } from "react"; 
Create a state variable: 
const [name, setName] = useState(""); 
Here: 
• name → stores the input value 
• setName → updates the value 
• ""

## Technologies Used
- React JS
- Vite
- JavaScript (JSX)
- HTML5 / CSS3

## How to Run
```bash
npm create vite@latest my-app -- --template react
cd my-app
npm install
npm run dev
```

## Exercise Content
See `exercise.txt` for complete exercise content and source code.
