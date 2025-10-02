
# 📘 CSS Box Model Cheat Sheet (Interview Ready)

## 🔹 What is the Box Model?

Every HTML element is treated as a **box** by the browser. The box consists of four layers, from inside out: **Content, Padding, Border, Margin**.

| Layer | Location | Purpose |
| :---: | :---: | :--- |
| **Margin** | Outside the border | **Outside space** (between elements) |
| **Border** | Around the padding | **Frame** around the element |
| **Padding** | Inside the border | **Space between content & border** |
| **Content** | Center | Actual text/image inside |

---

## 🔹 Core Components & Properties

### 1. Content

* Holds text, images, or other content.
* Size controlled by:
    ```css
    width: 200px;  
    height: 100px;
    ```

### 2. Padding (Inside Spacing)

* Space between the **Content** and the **Border**.
* **Expands the background color** of the element.
* Example:
    ```css
    padding: 10px; /* all 4 sides */
    padding: 5px 10px; /* top/bottom: 5px, left/right: 10px */
    padding: 6px 10px 4px 12px; /* top, right, bottom, left */
    ```

### 3. Border (Frame)

* A frame separating the **Padding** (inside) from the **Margin** (outside).
* Example:
    ```css
    border: 3px solid coral;
    border-radius: 10px; /* for rounded corners */
    ```

### 4. Margin (Outside Spacing)

* Space **outside** the border, used to separate the element from others.
* Example:
    ```css
    margin: 20px; /* all 4 sides */
    margin: 10px auto; /* top/bottom: 10px, left/right: auto (centers element) */
    ```

---

## 🔹 Key Interview Concepts

### Margin Collapse

* **Vertical Margins (Top/Bottom) Collapse:** When two vertical margins meet, they combine into a **single space** equal to the **largest** of the two margins, not their sum.
* **Horizontal Margins (Left/Right) Add Up:** Horizontal margins never collapse; they always sum together.

### Element Size Calculation

**Standard (Content-Box) Model:**
$$
\text{Total Width} = \text{Width} + \text{2} \times \text{Padding} + \text{2} \times \text{Border}
$$
**Interviewer Tip:** Content width is literally the `width` property.

### `box-sizing: border-box` (Modern Standard)

* **Crucial for Layouts:** Changes how the element size is calculated.
* The set **`width`** and **`height`** now include the **Content, Padding, AND Border**.
* This makes layout calculation much more intuitive.
    ```css
    * {
      box-sizing: border-box; 
    }
    /* Now, width: 200px is the total visible width */
    ```

---

## 🔹 Control & Display

### Visibility vs. Display

| Property | Effect | Space Occupied? |
| :---: | :---: | :---: |
| `display: none;` | **Removes** element completely from the document flow. | **No** (as if the element doesn't exist) |
| `visibility: hidden;` | **Hides** the element, but it still takes up its original space. | **Yes** (space remains empty) |

### Centering a Block Element

1.  **Set a defined `width`**.
2.  Use **`margin: 0 auto;`**
    ```css
    div {
      width: 400px;
      margin: 0 auto; /* Horizontally centers the div */
    }
    ```

### Overflow

Controls content when it exceeds the box dimensions:

```css
overflow: hidden; /* Content is cut off/clipped */
overflow: scroll; /* Always adds scrollbars */
overflow: auto; /* Adds scrollbars only if content overflows */
overflow: visible; /* Default, content overflows outside the box */
````

```
```
