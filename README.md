# 2019-powerup-2
2018 powerup code built with 2019 framework

## Adding local code to remote repository

When using the WPILIB import Eclipse project, the code is copied to a new directory.
However, the .git directory is not copied, and therefore any changes are not related to an existing git repository.

These steps add the locally modified files to a new remote repository:

git init <br>
git remote add origin <path/to/repo> <br>
git fetch <br>
git pull origin <br>

git add file1.cpp ... etc  <br>
git commit -m "commit message" <br>

git push --set-upstream origin master <br>

## CTRE libraries
CTRE libraries are found here: C:\Users\Public\frc2019\maven\com\ctre\phoenix

When the **Manage Vendor Libraries** step is performed, these libraries are expanded to:
- build/tmp/expandedArchives

If the CTRE libraries are not expanded, then the build will fail with "No such file" errors.

## Linux build issue:
**undefined reference to symbol 'HAL_Report'**
```
> Task :linkFrcUserProgramLinuxx86-64DebugExecutable FAILED
/usr/bin/ld: /home/raven3/development/2019-powerup-2/build/tmp/expandedArchives/wpilibc-cpp-2019.1.1-linuxx86-64debug.zi
p_b5ee0a5c71aefcaf2253eeecb8d95603/linux/x86-64/shared/libwpilibcd.so: undefined reference to symbol 'HAL_Report'
/home/raven3/development/2019-powerup-2/build/tmp/expandedArchives/hal-cpp-2019.1.1-linuxx86-64debug.zip_0abaf7b418796dc825166bbbc9d08299/linux/x86-64/shared/libwpiHald.so: error adding symbols: DSO missing from command line
collect2: error: ld returned 1 exit status
```
