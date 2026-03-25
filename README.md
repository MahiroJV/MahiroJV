# 📋 Task Tracker CLI

> Built from scratch in Java — no frameworks, no shortcuts, just raw code and good vibes.

---

## 👋 About

Hey! I'm **MahiroJV** — I mess around with Linux, play with shell scripts, and build projects from [roadmap.sh](https://roadmap.sh) just for the fun of it.

This is my take on the [Task Tracker](https://roadmap.sh/projects/task-tracker) project from roadmap.sh.
No external libraries. No fancy frameworks. Just Java, a JSON file, and a terminal. 🖥️

---

## ⚡ What it does

A dead simple CLI to manage your tasks right from the terminal.

```bash
taskcli add "Fix that bug"
taskcli list
taskcli mark-done 1
taskcli list done
```

That's it. No mouse. No GUI. Pure terminal energy. 😎

---

## 🚀 Getting Started

**Requirements:**
- Java 11+

```bash
# Check if you have Java
java -version
javac -version
```

**Clone & compile:**
```bash
git clone https://github.com/MahiroJV/TaskTrackerCLI
cd TaskTrackerCLI

# Compile
javac -d bin src/package1/*.java
```

**Install the command globally:**
```bash
chmod +x taskcli
sudo mv taskcli /usr/local/bin/taskcli
```

Now you can type `taskcli` from anywhere. ✅

---

## 📖 Commands

| Command | What it does |
|---|---|
| `taskcli add "description"` | Add a new task |
| `taskcli update <id> "description"` | Update a task |
| `taskcli delete <id>` | Delete a task |
| `taskcli mark-in-progress <id>` | Mark as in-progress |
| `taskcli mark-done <id>` | Mark as done |
| `taskcli list` | List all tasks |
| `taskcli list todo` | List todo tasks only |
| `taskcli list in-progress` | List in-progress tasks only |
| `taskcli list done` | List done tasks only |

---

## 🗂️ Project Structure

```
TaskTrackerCLI/
├── src/
│   └── package1/
│       ├── taskCli.java       ← Entry point, reads your commands
│       ├── task.java          ← Task model (id, description, status...)
│       ├── taskManager.java   ← Business logic (add, delete, list...)
│       └── jsonStore.java     ← Reads & writes tasks.json manually
├── bin/                       ← Compiled .class files
├── tasks.json                 ← Auto-created on first use
└── taskcli                    ← Shell wrapper script
```

---

## 🛠️ How it works

- Tasks are stored in a **`tasks.json`** file — created automatically when you add your first task
- JSON is parsed **manually** with no external libraries (yes, really)
- Each task has: `id`, `description`, `status`, `createdAt`, `updatedAt`

```json
[
  {
    "id": 1,
    "description": "Buy groceries",
    "status": "todo",
    "createdAt": "2024-03-17T10:00:00",
    "updatedAt": "2024-03-17T10:00:00"
  }
]
```

---

## 🗺️ Part of my roadmap.sh journey

This project is from [roadmap.sh/projects/task-tracker](https://roadmap.sh/projects/task-tracker).
I'm working through projects on roadmap.sh to sharpen my skills and have fun doing it.

Check out my other projects → [github.com/MahiroJV](https://github.com/MahiroJV)

---

## 📜 License

Do whatever you want with it. It's just for fun anyway. 🙂
