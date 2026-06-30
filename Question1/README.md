# Question 1 - Linux Environment Verification

## Command 1

```bash
mkdir Question1
```

### Observation
This command created a new directory named `Question1`. The directory is used to store all files related to Question 1 of the assignment.

---

## Command 2

```bash
cd Question1
```

### Observation
This command changed the current working directory to `Question1`. All subsequent files and commands were executed inside this directory.

---

## Command 3

```bash
pwd
```

### Observation
The `pwd` command displayed the current working directory. It confirmed that I was working inside the `Question1` directory.

---

## Command 4

```bash
whoami
```

### Observation
The `whoami` command displayed the username of the currently logged-in user. This verified the active Linux account.

---

## Command 5

```bash
echo "Username: $(whoami)" >> Environment_Report.txt
```

### Observation
This command stored the username inside the `Environment_Report.txt` file. The `>>` operator appends text to an existing file.

---

## Command 6

```bash
groups
```

### Observation
The `groups` command displayed all groups associated with my user account. These groups determine the permissions assigned to the user.

---

## Command 7

```bash
echo "Groups: $(groups)" >> Environment_Report.txt
```

### Observation
This command appended the group information to the report file for documentation.

---

## Command 8

```bash
echo $SHELL
```

### Observation
This command displayed the current shell being used. The shell is responsible for interpreting Linux commands.

---

## Command 9

```bash
echo "Shell: $SHELL" >> Environment_Report.txt
```

### Observation
This command saved the shell information into the report file.

---

## Command 10

```bash
pwd
```

### Observation
This command displayed the current working directory again before saving it to the report.

---

## Command 11

```bash
echo "Current Directory: $(pwd)" >> Environment_Report.txt
```

### Observation
This command appended the current working directory to the report.

---

## Command 12

```bash
ls -la
```

### Observation
This command listed all files and directories, including hidden files. It also displayed permissions, ownership, and file sizes.

---

## Command 13

```bash
ping -c 4 google.com
```

### Observation
This command tested network connectivity by sending four packets to Google's server. The successful replies confirmed that the internet connection was working properly.

---

## Command 14

```bash
cat Environment_Report.txt
```

### Observation
This command displayed the contents of the report file. It confirmed that all required information had been successfully recorded.