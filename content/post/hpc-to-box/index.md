---
title: Transfer Data between Farm HPC and Box
date: 2022-07-21
summary: Backup HPC data on Box
image:
  placement: 2
  caption: 'Data transfer'

authors:
  - admin

# Is this an unpublished draft?
draft: false

tags:
  - HPC

# folder
categories:
  - Data science
  - Note
---

To back up data from HPC to Box, adhere to this [guidance](https://hpc.ucdavis.edu/faq).

1. Go to https://ucdavis.account.box.com/login

2. Create an external password on Box.com - Go to "Account Settings" and set up the password.

3. Create a folder on Box into which files will be transferred

4. Log into the cluster. Go to the level folder in which the folder/files you want to copy over

5. Log into Box from the cluster location:

```bash
lftp -u <Box username which is just ucd email> ftps://ftp.box.com
```

6. Enter the external password for Box.com

7. Use the `mirror` command to copy folder and contents to Box; `-R` flag for reverse (which is the `put` command for putting files from the cluster into
Box); `-L` --dereference flag for transferring symbolic links as actual files:

```bash
mirror -RL --dereference <source> <target>
```

You can use "get" and "put" to upload and download

```bash
get [OPTS] <rfile> [-o <lfile>]
put [OPTS] <lfile> [-o <rfile>]
```

Or use help command to see the list of all available options.

8. Exit out of the Box.