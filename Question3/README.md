# Question 3 - File System and Link Analysis

## Objective

The objective of this experiment was to understand the behavior of Linux hard links and symbolic links by creating both types of links, comparing their inode numbers, examining file metadata, and observing what happens after deleting the original file.

---

## Command 1

```bash
mkdir Question3
```

### Observation

This command created a new directory named `Question3` to store all the files related to the third question. It helps keep the assignment organized.

---

## Command 2

```bash
cd Question3
```

### Observation

This command changed the current working directory to `Question3`. All subsequent files and commands were executed inside this directory.

---

## Command 3

```bash
touch Link_Analysis_Report.txt
```

### Observation

This command created an empty report file named `Link_Analysis_Report.txt`. The report was later used to store the results of the experiment.

---

## Command 4

```bash
touch README.md
```

### Observation

This command created a `README.md` file to document the commands executed and the observations made during the experiment.

---

## Command 5

```bash
echo "Linux Link Analysis Experiment" > original.txt
```

### Observation

This command created the original file and stored sample content inside it. The file served as the source for creating both hard and symbolic links.

---

## Command 6

```bash
ln original.txt hardlink.txt
```

### Observation

This command created a hard link named `hardlink.txt`. A hard link shares the same inode as the original file and directly references the file's data.

---

## Command 7

```bash
ln -s original.txt symlink.txt
```

### Observation

This command created a symbolic link named `symlink.txt`. Unlike a hard link, a symbolic link stores only the pathname of the target file.

---

## Command 8

```bash
ls -li
```

### Observation

This command displayed the inode numbers of all files. The output confirmed that the original file and hard link shared the same inode number, while the symbolic link had a different inode.

---

## Command 9

```bash
stat original.txt hardlink.txt symlink.txt
```

### Observation

This command displayed detailed metadata such as inode number, permissions, timestamps, ownership, and file type. It provided additional information about how Linux stores and manages different link types.

---

## Command 10

```bash
rm original.txt
```

### Observation

This command deleted the original file. It was performed to observe how the hard link and symbolic link behave after the source file is removed.

---

## Command 11

```bash
ls -li
```

### Observation

This command listed the remaining files after deleting the original file. The hard link continued to exist, while the symbolic link became a broken link pointing to a non-existent target.

---

## Command 12

```bash
cat hardlink.txt
```

### Observation

This command displayed the contents of the hard link. The file remained fully accessible because the hard link still referenced the original inode.

---

## Command 13

```bash
cat symlink.txt
```

### Observation

This command failed because the symbolic link pointed to a file that no longer existed. This demonstrated that symbolic links depend on the existence of the original target file.

---

## Command 14

```bash
cat Link_Analysis_Report.txt
```

### Observation

This command displayed the completed report. It confirmed that all required information, including inode numbers, metadata, comparison, and conclusions, had been successfully recorded.

---

# Summary of Findings

- The original file and hard link shared the same inode number.
- The symbolic link had a different inode because it stored only the file path.
- Deleting the original file did not affect the hard link.
- The symbolic link became invalid after the original file was removed.
- This experiment demonstrated the fundamental difference between hard links and symbolic links in Linux.

---

# Conclusion

Hard links provide direct access to the file's data by sharing the same inode as the original file. Symbolic links only reference the file's pathname and therefore become broken if the original file is deleted. This experiment highlights why hard links remain functional after deletion of the original file, while symbolic links do not.