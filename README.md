# React Lab Exercise 8: React User Interactions onChange and onSubmit

## Name: LOGESH S
## Roll no: 2305001014
## Department: CSE

## AIM
### To implement React form interactions using the onChange and onSubmit events to capture user input, update state, and handle form submission.

## PROGRAM

### i) App.jsx
```jsx
import { useState } from "react";
import "./App.css";

function App() {
  const [name, setName] = useState("");
  const [email, setEmail] = useState("");

  const handleChange = (event) => {
    const { name, value } = event.target;

    if (name === "name") {
      setName(value);
    } else if (name === "email") {
      setEmail(value);
    }
  };

  const handleSubmit = (event) => {
    event.preventDefault();

    if (name.trim() === "" || email.trim() === "") {
      alert("Please fill in all fields!");
      return;
    }

    alert("Hello " + name + "\nEmail: " + email);
  };

  return (
    <div className="container">
      <h1>Student Form</h1>

      <form onSubmit={handleSubmit}>
        <label>Name:</label>
        <input
          type="text"
          name="name"
          value={name}
          onChange={handleChange}
          placeholder="Enter your name"
        />

        <label>Email:</label>
        <input
          type="email"
          name="email"
          value={email}
          onChange={handleChange}
          placeholder="Enter your email"
        />

        <button type="submit">Submit</button>
      </form>

      <div className="preview">
        <h3>Live Preview</h3>
        <p>Name: {name || "Not entered"}</p>
        <p>Email: {email || "Not entered"}</p>
      </div>
    </div>
  );
}

export default App;
```

### ii) App.css
```css
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background-color: #f2f5f9;
}

.container {
  max-width: 400px;
  margin: 50px auto;
  padding: 25px;
  background-color: white;
  border-radius: 10px;
  box-shadow: 0 4px 12px #0000001a;
}

h1 {
  text-align: center;
  color: #1976d2;
}

label {
  display: block;
  margin-top: 15px;
  font-weight: bold;
}

input {
  width: 100%;
  padding: 10px;
  margin-top: 5px;
  border: 1px solid #cccccc;
  border-radius: 5px;
  box-sizing: border-box;
}

button {
  width: 100%;
  margin-top: 20px;
  padding: 12px;
  background-color: #1976d2;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #125ca1;
}

.preview {
  margin-top: 25px;
  padding: 15px;
  background-color: #eef5ff;
  border-radius: 5px;
  overflow-wrap: anywhere;
}
```

## OUTPUT
<img width="1125" height="616" alt="image" src="https://github.com/user-attachments/assets/79ba0ae6-0fe5-4635-b0ad-697725f0b75f" />
<img width="1125" height="618" alt="image" src="https://github.com/user-attachments/assets/1704787a-4dba-405a-a6ba-7ca54aa582ca" />
<img width="575" height="233" alt="image" src="https://github.com/user-attachments/assets/af8096f0-274f-4c15-b427-9def878d7b3d" />


## RESULT
### Thus, React user interactions were successfully implemented using the onChange and onSubmit events. The application captured the student's name and email, updated the live preview dynamically, and handled form submission using event.preventDefault().
