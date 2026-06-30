# Question 5 - Storage Health Assessment and Documentation

## Objective

The objective of this experiment was to assess the storage resources available on the Linux system. Storage devices, mounted file systems, disk usage, inode utilization, and overall storage health were examined. The report was created using the `vi` editor as required.

---

## Command 1

```bash
mkdir Question5
```

### Observation

This command created a new directory named `Question5` to store all files related to this experiment. Keeping each question in a separate directory improves organization.

---

## Command 2

```bash
cd Question5
```

### Observation

This command changed the current working directory to `Question5`. All subsequent files and commands were executed inside this directory.

---

## Command 3

```bash
touch README.md
mkdir screenshots
```

### Observation

These commands created the documentation file (`README.md`) and a folder to store screenshots taken during the experiment.

---

## Command 4

```bash
vi Storage_Assessment_Report.txt
```

### Observation

This command opened the `vi` editor and created the `Storage_Assessment_Report.txt` file. The report was prepared using the `vi` editor as required by the assignment.

---

## Command 5

```bash
lsblk
```

*(If `lsblk` was unavailable, `df -h` was used instead.)*

### Observation

This command displayed the available storage devices attached to the system. It provided information such as device names, sizes, and partitions.

---

## Command 6

```bash
mount
```

### Observation

This command displayed all mounted file systems currently available on the system. It showed the mount points and the corresponding storage devices.

---

## Command 7

```bash
df -h
```

### Observation

This command displayed disk usage statistics in a human-readable format. It showed the total size, used space, available space, and percentage utilization of each mounted file system.

---

## Command 8

```bash
df -i
```

### Observation

This command displayed inode usage statistics for each mounted file system. It helped determine whether sufficient inodes were available for creating additional files.

---

## Command 9

```bash
cat Storage_Assessment_Report.txt
```

### Observation

This command displayed the completed storage assessment report, confirming that all required storage information and observations had been successfully recorded.

---

# Storage Health Observations

- The mounted file systems were accessible and functioning correctly.
- Disk usage was within acceptable limits.
- Inode utilization indicated sufficient capacity for creating additional files.
- No storage-related issues were observed during the assessment.

---

# Recommendations

- Monitor disk usage regularly to prevent storage exhaustion.
- Remove unnecessary files and logs periodically.
- Archive old data to reduce disk usage.
- Perform regular system backups.
- Monitor inode usage along with disk space to avoid filesystem limitations.

---

# Conclusion

This experiment demonstrated how Linux provides tools for monitoring storage resources and filesystem health. Commands such as `lsblk`, `mount`, `df -h`, and `df -i` provide valuable information for system administrators to monitor storage devices, mounted file systems, disk utilization, and inode usage. Regular monitoring and maintenance help ensure reliable system performance and efficient storage management.