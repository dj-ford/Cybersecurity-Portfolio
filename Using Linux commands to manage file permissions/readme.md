# Using Linux Commands to Manage File Permissions

## Project Description
As a security professional supporting the research team, my role involves ensuring that users have appropriate access to files and directories. The projects directory contained files and folders with permissions that did not align with the organization’s authorization requirements. My task was to inspect existing permissions and update them to remove unauthorized access, helping maintain system security.

---

## Check File and Directory Details
To start, I used Linux commands to examine the existing permissions on the files and directories within the projects directory. The `ls -la` command provides a detailed listing of all files, including hidden files, and their current permission settings.



The output indicated:

- One directory named `drafts`
- One hidden file `.project_x.txt`
- Five additional project files  

The first column shows a 10-character permissions string representing access levels for the user, group, and others.

---

## Describe the Permissions String
The 10-character string can be interpreted as follows:

- **1st character**: `d` for directory, `-` for a file  
- **2nd–4th characters**: User permissions (read `r`, write `w`, execute `x`)  
- **5th–7th characters**: Group permissions (read `r`, write `w`, execute `x`)  
- **8th–10th characters**: Others’ permissions (read `r`, write `w`, execute `x`)  

**Example:** `-rw-rw-r--` for `project_t.txt` indicates:  

- It is a file (`-`)  
- User: read/write  
- Group: read/write  
- Others: read only  

---

## Change File Permissions
The organization determined that “others” should not have write access to any files. Using the permissions output from `ls -la`, I identified `project_k.txt` as needing modification.


This removed write permissions from others for project_k.txt.

---
## Change File Permissions on a Hidden File

The hidden file .project_x.txt had been archived. The research team required that the user and group maintain read access, but no write access.

chmod u-w .project_x.txt
chmod g-w,g+r .project_x.txt
ls -la

---
## Change Directory Permissions

The drafts directory should only be accessible to researcher2. No other users should have execute permissions.

This removed execute permissions from the group while preserving access for researcher2.

---

## Summary

I reviewed and updated permissions for files and directories in the projects directory to reflect the correct authorization levels. Starting with ls -la, I identified existing permissions, then applied chmod commands to:

- Remove unauthorized write access for others
- Update hidden files to ensure proper read/write access
- Restrict directory access to specific users

These steps strengthened the organization’s file system security while aligning permissions with user roles.
