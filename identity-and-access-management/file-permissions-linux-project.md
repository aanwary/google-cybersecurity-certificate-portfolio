# File Permissions Project: Linux 

## Project Description
This project is part of my coursework for the **Google Cybersecurity Professional Certificate**. This project demonstrates my ability to check, interpret, and update file permissions in Linux, ensuring that the system remains secure by limiting unauthorized access. 

## Overview
The research team at my organization needs to update file permissions for certain files and directories within the `projects` directory to align with our security policies. Currently, the permissions do not reflect the necessary level of access. 

## Supporting Document:
  [Current File Permissions](https://docs.google.com/document/d/1F3-8XQZsNagSzTkJwFzOGY5OHbGbMRtlb8GbmXE_gCc/template/preview?resourcekey=0-UUEu0EyFFvMf0SAipcel6w)

---

## Check File and Directory Details

1. **Command Used**: `ls -la /home/researcher2/projects`
   - **Explanation**: I used the `ls -la` command to display a detailed list of files and directories, including hidden files, within `/home/researcher2/projects`. This output includes permissions in a 10-character string format, which I used to determine current access settings. The list showed one directory (`drafts`), one hidden file (`.project_x.txt`), and five other project files.

   - **Permissions Output**:
     ```bash
     -rw-rw-rw- 1 researcher2 researcher2 1024 Nov 9 10:15 project_k.txt
     -rw-r----- 1 researcher2 researcher2 2048 Nov 9 10:15 project_m.txt
     -rw-rw-r-- 1 researcher2 researcher2 1024 Nov 9 10:15 project_r.txt
     -rw-rw-r-- 1 researcher2 researcher2 1024 Nov 9 10:15 project_t.txt
     -rw-rw---- 1 researcher2 researcher2 1024 Nov 9 10:15 .project_x.txt
     drwx--x--- 2 researcher2 researcher2 4096 Nov 9 10:15 drafts
     ```

---

## Describe the Permissions String

- **Example String**: `-rw-rw-r--` for `project_t.txt`
   - **Explanation**:
     - `-` : Indicates it’s a regular file.
     - `rw-` : User (owner) can read and write.
     - `rw-` : Group members can read and write.
     - `r--` : Others can only read.

   This string shows that `project_t.txt` is accessible by others for reading but limits write permissions to the user and group only. No one has execute permissions for this file, which matches our intended access policies.

---

## Change File Permissions

1. **File Example**: `project_k.txt`
   - **Commands Used**:
     ```bash
     chmod o-w /home/researcher2/projects/project_k.txt
     ls -la /home/researcher2/projects/project_k.txt
     ```
   - **Explanation**: To comply with our policy that prevents others from having write access, I removed the write permission for “others” on `project_k.txt`. The `chmod o-w` command ensures only the user and group retain write access, while others have read-only access. I then confirmed the updated permissions with `ls -la`.

   - **Updated Permissions**: 
     ```bash
     -rw-rw-r--
     ```

---

## Change File Permissions on a Hidden File

1. **File Example**: `.project_x.txt`
   - **Commands Used**:
     ```bash
     chmod u-w /home/researcher2/projects/.project_x.txt
     chmod g-w /home/researcher2/projects/.project_x.txt
     chmod g+r /home/researcher2/projects/.project_x.txt
     ls -la /home/researcher2/projects/.project_x.txt
     ```
   - **Explanation**: I modified the permissions for `.project_x.txt`, an archived file, to make it read-only for both the user and group. The sequence of `chmod` commands removed write access for the user (`u-w`) and the group (`g-w`) while ensuring the group has read access (`g+r`). I verified the permissions with `ls -la`.

   - **Updated Permissions**: 
     ```bash
     -r--r-----
     ```

---

## Change Directory Permissions

1. **Directory Example**: `drafts`
   - **Commands Used**:
     ```bash
     chmod g-x /home/researcher2/projects/drafts
     ls -la /home/researcher2/projects/drafts
     ```
   - **Explanation**: I restricted the `drafts` directory to ensure only `researcher2` can access it fully. By using `chmod g-x`, I removed execute permissions for the group, limiting access to only the user. This change protects the contents of `drafts` from unauthorized viewing or modifications, as only the `researcher2` user retains full access.

   - **Updated Permissions**:
     ```bash
     drwx------
     ```

---

## Summary
Through this project, I examined and modified permissions for files and directories within the `/home/researcher2/projects` directory to match our organization’s security requirements. By using the `ls -la` and `chmod` commands, I effectively managed access control, ensuring that only authorized users have the necessary permissions. This task highlights essential skills in file management and demonstrates the role of access control in maintaining secure systems.

---
