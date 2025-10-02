
# 💻 Command Line Navigation Cheatsheet (Beginner Friendly)

The Command Line (Terminal) lets you interact with your computer using text commands. **Directories** are just files and folders.

## 1️⃣ Essential Navigation (Where & What)
---

| Command | Full Name | Purpose | Example | Result |
| :---: | :---: | :--- | :--- | :--- |
| **`pwd`** | **P**rint **W**orking **D**irectory | Shows the **full path** to the current directory you are inside. | `$ pwd` | `/home/user/documents/projects` |
| **`ls`** | **L**i**s**t | Lists the files and folders **inside** the current directory. | `$ ls` | `images/ files.txt setup.sh` |
| **`clear`** | | Clears all previous commands from the terminal screen, giving you a fresh view. | `$ clear` | (Screen is blanked) |

---

## 2️⃣ Moving Around (The `cd` Command)

The **`cd`** (Change Directory) command is how you move between folders.

| Command | Action | Description | Example Path Change |
| :---: | :---: | :--- | :--- |
| **`cd <folder>`** | **Move In** | Move into a folder *relative to your current location*. | `/home` **$\to$** `/home/user` |
| **`cd ..`** | **Go Up** | Move up one level to the **parent directory**. | `/home/user` **$\to$** `/home` |
| **`cd ../<folder>`** | **Move Across** | Move up one level, then down into an adjacent folder. | `/home/user/a` **$\to$** `/home/user/b` |
| **`cd /<path>`** | **Absolute Path** | Go straight to a specific location from the **root** (`/`). | Anywhere **$\to$** `/var/log` |

---

## 3️⃣ Creating Files & Folders
---

| Command | Purpose | Example | Result |
| :---: | :---: | :--- | :--- |
| **`mkdir <name>`** | **Make** Directory (Folder) | `$ mkdir media` | Creates a new **folder** called `media`. |
| **`touch <name>`** | **Create** File | `$ touch keyboard.txt` | Creates an **empty file** called `keyboard.txt`. |

---

## 4️⃣ Helpful Shortcuts & Tips
---

* **`Tab`**: **Autocomplete**. Start typing a file/folder name and hit `Tab` to automatically complete the rest. (Saves a ton of typing!)
* **`Up` / `Down` Arrows**: Scroll through your history of previous commands.
* **Path Tip**: Use the path separator **`/`** to navigate multiple levels at once:
    ```bash
    $ cd 2015/jan/memory # Relative path, moves multiple levels down
    $ cd ../../         # Moves up two levels
    ```

## ✅ Quick Command Summary for Memory

| Navigation | Creation |
| :---: | :---: |
| **`pwd`** $\to$ **where** you are | **`mkdir`** $\to$ **make** folder |
| **`ls`** $\to$ **what’s** in the folder | **`touch`** $\to$ **make** file |
| **`cd`** $\to$ **move** around | **`clear`** $\to$ **clean** screen |
````
