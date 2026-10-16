# Lab 05 Challenge: Security Detective

## Q1. Current User and Home Directory

**Commands:**
- `whoami`
- `echo $HOME`

**Results:**
- Current user: `sananoorbhatti`
- Home directory: `/home/sananoorbhatti`

## Q2. Hostname and Ubuntu Version

**Commands:**
- `hostname`
- `cat /etc/os-release | head -2`

**Results:**
- Hostname: `ubuntu`
- Operating system: Ubuntu 26.04.1 LTS

## Q3. Available RAM and Disk Space

**Commands:**
- `free -h`
- `df -h /`

**Results:**
- Total RAM: 3.3 GiB
- Available RAM: 2.5 GiB
- Root filesystem size: 9.8 GB
- Used disk space: 4.8 GB
- Available disk space: 4.5 GB
- Disk usage: 52%

## Q4. Users with `/bin/bash` Login Shells

**Command:**
`grep '/bin/bash' /etc/passwd`

**Results:**
- `root`
- `sananoorbhatti`

These are the two users returned by the command with `/bin/bash` as their login shell.

## Q5. Number of Processes

**Command:**
`ps aux | wc -l`

**Result:** 244 lines.

The command counts the lines in the process listing, including the header, so the number of actual process entries is generally one fewer than the output.

## Q6. Creation and Deletion of `lab5user`

**Command:**
`sudo grep lab5user /var/log/auth.log`

**Results from the authentication log:**
- Account creation requested: `2026-10-16 04:58:23 UTC`
- User account created: `2026-10-16 04:58:23 UTC`
- User session opened: `2026-10-16 05:00:38 UTC`
- User session closed: `2026-10-16 05:06:22 UTC`
- Account deletion requested: `2026-10-16 05:08:04 UTC`
- User account deleted: `2026-10-16 05:08:04 UTC`

The logs show that `lab5user` was created successfully, used for testing, and then deleted along with its home directory.
