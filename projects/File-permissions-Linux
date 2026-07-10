# Linux File Permissions

## Project Description

This project demonstrates how I inspected and modified file and directory permissions in Linux using the `ls` and `chmod` commands. The objective was to ensure that access permissions matched the organization's security requirements and followed the principle of least privilege.

## Objectives

- Inspect existing file and directory permissions.
- Understand Linux permission strings.
- Remove unnecessary write permissions.
- Secure hidden files.
- Restrict directory access to authorized users only.

---

## Step 1 – Check File and Directory Details

I used the following command to inspect the permissions of all files, including hidden files:

```bash
ls -la
```

This command displayed:

- The `drafts` directory
- The hidden file `.project_x.txt`
- Five project files
- The permission string for each file and directory

---

## Understanding Linux Permission Strings

Each permission string contains 10 characters.

Example:

```text
-rw-rw-r--
```

Meaning:

| Characters | Description |
|------------|-------------|
| 1 | File type (`-` = file, `d` = directory) |
| 2–4 | User permissions (read, write, execute) |
| 5–7 | Group permissions |
| 8–10 | Other users' permissions |

Example:

```
-rw-rw-r--
```

- User: Read and Write
- Group: Read and Write
- Others: Read only

---

## Step 2 – Remove Write Permission from Others

The organization required that **other users should not have write access** to project files.

Command used:

```bash
chmod o-w project_k.txt
```

After updating the permissions, I verified the changes using:

```bash
ls -la
```

---

## Step 3 – Secure the Hidden File

The archived file `.project_x.txt` required stricter permissions.

Requirements:

- User: Read only
- Group: Read only
- Others: No write access

Commands used:

```bash
chmod u-w .project_x.txt
chmod g-w .project_x.txt
chmod g+r .project_x.txt
```

---

## Step 4 – Restrict Directory Permissions

Only the user **researcher2** should have execute access to the `drafts` directory.

Command used:

```bash
chmod g-x drafts
```

This removed execute permissions from the group while keeping access available only to the authorized user.

---

## Skills Demonstrated

- Linux command line
- File permission management
- Access control
- Principle of Least Privilege
- Linux security administration

---

## Commands Used

```bash
ls -la
chmod o-w project_k.txt
chmod u-w .project_x.txt
chmod g-w .project_x.txt
chmod g+r .project_x.txt
chmod g-x drafts
```

---

## Summary

In this project, I successfully inspected and modified Linux file and directory permissions to align with organizational security requirements. By using the `ls -la` and `chmod` commands, I ensured that users, groups, and others were granted only the permissions necessary to perform their tasks, improving the overall security of the system.

---

## Screenshots

Add your screenshots below:

1. Checking file permissions
2. Removing write permission from `project_k.txt`
3. Updating `.project_x.txt` permissions
4. Restricting access to the `drafts` directory
