# Task 2 — User Management

Created a new user and added it to the `adm` group for administrative access.

## Creating User

![User Creation](../image_for_md/task2-createuser-and-appendadm.png)

Using `sudo adduser newuser` and `sudo usermod -aG adm newuser`

## Verification

![Passwd Output](../image_for_md/task2-passwd.png)

Output of `cat /etc/passwd` showing the new user entry.
