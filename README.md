# 📝 To-Do List By TypeScript

A simple and interactive **To-Do List application** built using **TypeScript, HTML, and CSS**.

This project was created to practice TypeScript fundamentals, Object-Oriented Programming (OOP), DOM manipulation, modules, and browser Local Storage while building a real-world frontend application.

---

## 🚀 Demo

You can run the project locally using Vite.

```bash
npm install
npm run dev
```

Then open the local URL provided by Vite in your browser.

---

## 📸 Features

* ➕ Add new tasks
* 📋 Display all tasks
* 🗑️ Clear all tasks
* 💾 Store tasks using Local Storage
* 🔄 Load saved tasks when the application starts
* ⌨️ Add tasks using the form
* ✅ Prevent adding empty tasks
* 🔢 Generate unique IDs for list items
* 📱 Responsive and clean user interface

---

## 🛠️ Technologies Used

* **TypeScript**
* **HTML5**
* **CSS3**
* **Vite**
* **Local Storage**
* **DOM API**
* **Object-Oriented Programming (OOP)**
* **ES Modules**

---

## 📂 Project Structure

```text
To-Do List Typescript/
│
├── src/
│   ├── css/
│   │   └── style.css
│   │
│   ├── model/
│   │   ├── FullList.ts
│   │   └── ListItem.ts
│   │
│   ├── templates/
│   │   └── ListTemplate.ts
│   │
│   └── main.ts
│
├── index.html
├── package.json
├── tsconfig.json
└── README.md
```

---

## 🧠 Project Architecture

The application separates responsibilities into different classes and modules.

### `ListItem`

Responsible for representing a single task in the list.

```typescript
new ListItem(itemId, newEntryText)
```

Each item contains information such as:

* Item ID
* Item text
* Completion state

---

### `FullList`

Responsible for managing the complete list of tasks.

It handles operations such as:

* Adding items
* Clearing the list
* Loading saved items
* Managing the list data
* Saving data to Local Storage

The project uses a **Singleton pattern** through:

```typescript
FullList.instance
```

This ensures that the application works with a single list instance.

---

### `ListTemplate`

Responsible for rendering the list in the DOM.

```typescript
template.render(fullList)
```

It also provides functionality for clearing the displayed list:

```typescript
template.clear()
```

This separates the application's **data management** from its **UI rendering**.

---

## 🔄 How It Works

When the application starts:

```text
DOMContentLoaded
       ↓
    initApp()
       ↓
Load saved list
       ↓
Render list
```

When the user adds a new task:

```text
User enters task
       ↓
Submit form
       ↓
Prevent default browser behavior
       ↓
Validate input
       ↓
Create ListItem
       ↓
Add item to FullList
       ↓
Render updated list
       ↓
Save to Local Storage
```

When the user clicks **Clear**:

```text
Click Clear
     ↓
Clear FullList
     ↓
Clear rendered items
     ↓
Update Local Storage
```

---

## 💻 Main TypeScript Logic

The application initializes the list and template:

```typescript
const fullList = FullList.instance
const template = ListTemplate.instance
```

It then listens for the form submission:

```typescript
itemEntryForm.addEventListener("submit", (event: SubmitEvent): void => {
    event.preventDefault()

    const input = document.getElementById("newItem") as HTMLInputElement
    const newEntryText: string = input.value.trim()

    if (!newEntryText.length) return

    // Create and add new item
})
```

The project also uses TypeScript type annotations and DOM type casting:

```typescript
const input = document.getElementById("newItem") as HTMLInputElement
```

and:

```typescript
const clearItems = document.getElementById("clearItemsButton") as HTMLButtonElement
```

---

## 🎯 What I Practiced

Through this project, I practiced:

* TypeScript syntax and type annotations
* Interfaces and classes
* Object-Oriented Programming
* TypeScript modules
* DOM manipulation
* Event handling
* Form submission handling
* Type casting
* Local Storage
* Singleton pattern
* Separation of concerns
* Working with Vite
* Structuring a frontend project

---


## 👨‍💻 Author

**Omar Ahmed Sallam**

Junior Full-Stack (.NET & Angular) Developer

* GitHub: [Omar-SallaM0](https://github.com/Omar-SallaM0)
* LinkedIn: [Omar Sallam](https://www.linkedin.com/in/omar-sallam-9aa483259/)

