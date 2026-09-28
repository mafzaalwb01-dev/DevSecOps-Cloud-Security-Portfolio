# 02 — Files and Directories

## 🎯 Objective

In this section, I practiced how to create, manage, read, copy, move and delete files and directories in Linux.

These are basic but important skills for working with Linux servers in Cloud Engineering.

---

## 🧪 Commands Practiced

| Command | Purpose |
|---|---|
| `mkdir` | Create a directory |
| `cd` | Move between directories |
| `pwd` | Show current directory |
| `touch` | Create a file |
| `echo` | Write text into a file |
| `cat` | Read file content |
| `cp` | Copy files or directories |
| `mv` | Move or rename files |
| `rm` | Delete a file |
| `ls -la` | List files and directories |

---

## 💻 Practical Task

I created a project directory, created files, added content, created a backup directory, copied a file and renamed a file.

### Commands Used

```bash
mkdir project
cd project
touch app.txt
echo "Linux Cloud Practice" > app.txt
cat app.txt
mkdir backup
cp app.txt backup/app-backup.txt
mv app.txt application.txt
ls -la
ls -la backup
