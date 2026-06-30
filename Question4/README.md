# Question 4 - File Access and I/O Investigation

## Objective

The objective of this experiment was to investigate Linux file access and input/output (I/O) operations. The experiment involved identifying open file descriptors, demonstrating output and error redirection, observing system resource limits, and understanding how Linux manages file I/O.

---

## Command 1

```bash
mkdir Question4
```

### Observation

This command created a new directory named `Question4` to store all files related to this experiment. Organizing files into separate directories improves project management.

---

## Command 2

```bash
cd Question4
```

### Observation

This command changed the current working directory to `Question4`. All files created during this experiment were stored inside this directory.

---

## Command 3

```bash
touch IO_Investigation_Report.txt
touch README.md
touch output.txt
mkdir screenshots
```

### Observation

These commands created the report file, documentation file, an output file for testing file I/O, and a folder to store screenshots of command executions.

---

## Command 4

```bash
ls -l /proc/$$/fd
```

### Observation

This command displayed the file descriptors currently used by the shell process. It showed the standard input (0), standard output (1), standard error (2), and any additional file descriptors opened by the process.

---

## Command 5

```bash
echo "Linux I/O Investigation" > output.txt
```

### Observation

This command redirected standard output to the file `output.txt`, creating the file and writing sample content into it. The `>` operator overwrites the file if it already exists.

---

## Command 6

```bash
cat output.txt
```

### Observation

This command displayed the contents of `output.txt`, confirming that the text was successfully written using output redirection.

---

## Command 7

```bash
ls > directory_list.txt
```

### Observation

This command redirected the output of the `ls` command into `directory_list.txt` instead of displaying it on the terminal. This demonstrates standard output redirection.

---

## Command 8

```bash
cat directory_list.txt
```

### Observation

This command displayed the contents of `directory_list.txt`, confirming that the directory listing had been successfully redirected into the file.

---

## Command 9

```bash
ls non_existing_file 2> error.txt
```

### Observation

This command attempted to list a file that does not exist. The error message was redirected into `error.txt` using `2>`, demonstrating standard error redirection.

---

## Command 10

```bash
cat error.txt
```

### Observation

This command displayed the contents of `error.txt`, confirming that the error message had been successfully redirected and stored in a separate file.

---

## Command 11

```bash
ulimit -a
```

### Observation

This command displayed the current resource limits of the shell process, including limits related to open files, memory usage, process count, and stack size.

---

## Command 12

```bash
cat IO_Investigation_Report.txt
```

### Observation

This command displayed the completed investigation report. It verified that all required observations, command outputs, and explanations had been successfully recorded.

---

# Technical Observations

- Linux assigns file descriptors to every process for handling file input and output.
- File descriptor **0** represents standard input.
- File descriptor **1** represents standard output.
- File descriptor **2** represents standard error.
- Output redirection (`>`) stores command output in a file instead of displaying it on the terminal.
- Error redirection (`2>`) stores error messages separately without affecting normal output.
- Resource limits displayed by `ulimit` help control system resource usage and improve system stability.

---

# Conclusion

This experiment demonstrated how Linux manages file input/output using file descriptors and redirection operators. Standard output and standard error can be redirected independently to different files, making debugging and logging easier. The `ulimit` command provided information about process resource limits, illustrating how Linux controls system resources to maintain stability and security.