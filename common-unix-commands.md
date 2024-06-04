### UNIX OS Commands

#### Navigating Directories
* **pwd: Print working directory**

| Command | Description                                           |
|---------|-------------------------------------------------------|
| `pwd`   | Print the current working directory                   |
| `pwd -L`| Print the logical current working directory (default) |
| `pwd -P`| Print the physical current working directory, avoiding symlinks |

---
* **cd [directory]**: Change directory.

| Command          | Description                                           |
|------------------|-------------------------------------------------------|
| `cd`             | Change to the home directory                          |
| `cd ~`           | Change to the home directory                          |
| `cd /path/to/dir`| Change to a specified directory                       |
| `cd ..`          | Change to the parent directory                        |
| `cd -`           | Change to the previous directory                      |
| `cd /`           | Change to the root directory                          |
| `cd ~username`   | Change to another user's home directory               |
| `cd ../..`       | Move up two directory levels                          |
| `cd /d /path`    | Change directory and drive in Windows (Command Prompt)|

---
* **ls [directory]**: List directory contents.

| Command     | Description                                                                                  |
|-------------|----------------------------------------------------------------------------------------------|
| `ls -l`     | List detailed information of the files                                                       |
| `ls -la`    | List detailed information, including hidden files                                            |
| `ls -lh`    | List detailed information with readable file sizes                                           |
| `ls -ls`    | List detailed information with file sizes                                                    |
| `ls -a`     | List all files, including hidden files starting with ‘.’                                     |
| `ls --color`| Show colored list, options: always/never/auto                                                |
| `ls -d`     | List directories                                                                             |
| `ls -F`     | Add a character to the entries                                                               |
| `ls -i`     | List all files, ignoring case                                                                |
| `ls -r`     | List in reverse order                                                                        |
| `ls -R`     | List directory tree recursively                                                              |
| `ls -s`     | List file sizes                                                                              |
| `ls -S`     | Sort by file size                                                                            |
| `ls -t`     | Sort by time and date                                                                        |
| `ls -X`     | Sort by extension name                                                                       |

---
### Managing Files and Directories
* **mkdir [directory]**: Create a new directory.

Here's the updated table with examples included:

| Command                | Description                                                        | Example                                    |
|------------------------|--------------------------------------------------------------------|--------------------------------------------|
| **mkdir [directory]**  | Create a new directory                                             | `mkdir tinitiate`                          |
| `mkdir directory`      | Create a new directory                                             | `mkdir tinitiate`                          |
| `mkdir -p path`        | Create nested directories (create parent directories as needed)    | `mkdir -p usr/tinitiate`                   |
| `mkdir -m mode directory` | Set file mode (permissions) for the new directory               | `mkdir -m 755 tinitiate`                   |
| `mkdir --help`         | Display help information about the `mkdir` command                 | `mkdir --help`                             |
| `mkdir -v directory`   | Verbosely create directories, showing each one being created       | `mkdir -v tinitiate`                       |
| `mkdir -Z directory`   | Set SELinux security context of the new directory                  | `mkdir -Z tinitiate`                       |

---
* **rmdir [directory]**: Remove an empty directory.

Here's the updated table with examples included:

| Command                             | Description                                                       | Example                                          |
|-------------------------------------|-------------------------------------------------------------------|--------------------------------------------------|
| **rmdir [directory]**               | Remove an empty directory                                         | `rmdir tinitiate`                                |
| `rmdir directory`                   | Remove an empty directory                                         | `rmdir tinitiate`                                |
| `rmdir -p path`                     | Remove directory and its parent directories if they are empty     | `rmdir -p usr/tinitiate`                         |
| `rmdir --ignore-fail-on-non-empty directory` | Ignore errors when directory is not empty               | `rmdir --ignore-fail-on-non-empty tinitiate`     |
| `rmdir --help`                      | Display help information about the `rmdir` command                | `rmdir --help`                                   |
| `rmdir -v directory`                | Verbosely remove directories, showing each one being removed      | `rmdir -v tinitiate`                             |

---
* **rm [file]**: Remove a file.

Here's the updated table with examples included:

| Command                        | Description                                                              | Example                                     |
|--------------------------------|--------------------------------------------------------------------------|---------------------------------------------|
| **rm [file]**                  | Remove a file                                                            | `rm file.txt`                               |
| `rm file`                      | Remove a file                                                            | `rm file.txt`                               |
| `rm -r directory`              | Recursively remove a directory and its contents                          | `rm -r tinitiate`                           |
| `rm -f file`                   | Force removal of a file without prompting                                | `rm -f file.txt`                            |
| `rm -i file`                   | Prompt before each file removal                                          | `rm -i file.txt`                            |
| `rm -d directory`              | Remove an empty directory                                                | `rm -d tinitiate`                           |
| `rm -v file`                   | Verbosely remove files, showing each file being removed                  | `rm -v file.txt`                            |
| `rm --help`                    | Display help information about the `rm` command                          | `rm --help`                                 |
| `rm --one-file-system`         | Skip directories on different file systems while removing recursively    | `rm --one-file-system tinitiate`            |
| `rm -rf directory`             | Forcefully and recursively remove a directory and its contents           | `rm -rf tinitiate`                          |
| `rm --preserve-root`           | Do not remove the root directory (default behavior)                      | `rm --preserve-root tinitiate`              |
| `rm --no-preserve-root`        | Override the default behavior and allow removal of the root directory    | `rm --no-preserve-root tinitiate`           |
---
* **cp [source] [destination]**: Copy files or directories.

Here's the updated table with examples included:

| Command                               | Description                                                              | Example                                           |
|---------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------|
| **cp [source] [destination]**         | Copy a file to a destination                                             | `cp file.txt tinitiate/`                          |
| `cp source destination`               | Copy a file to a destination                                             | `cp file.txt tinitiate/`                          |
| `cp -r source destination`            | Recursively copy a directory and its contents                            | `cp -r tinitiate/ backup/`                        |
| `cp -f source destination`            | Force copy by removing the destination file if it exists                 | `cp -f file.txt tinitiate/`                       |
| `cp -i source destination`            | Prompt before overwrite                                                  | `cp -i file.txt tinitiate/`                       |
| `cp -u source destination`            | Copy only when the source file is newer than the destination file or when the destination file is missing | `cp -u file.txt tinitiate/`           |
| `cp -v source destination`            | Verbosely copy files, showing each file being copied                     | `cp -v file.txt tinitiate/`                       |
| `cp -a source destination`            | Archive mode; preserves attributes and recursively copies                | `cp -a tinitiate/ backup/`                        |
| `cp -p source destination`            | Preserve file attributes (mode, ownership, timestamps)                   | `cp -p file.txt tinitiate/`                       |
| `cp --help`                           | Display help information about the `cp` command                          | `cp --help`                                       |
| `cp --no-preserve=ATTR source destination` | Do not preserve the specified attributes                               | `cp --no-preserve=mode file.txt tinitiate/`       |
| `cp --parents source destination`     | Copy files along with their parent directories                           | `cp --parents src/file.txt tinitiate/`            |
| `cp -l source destination`            | Create hard links instead of copying                                     | `cp -l file.txt tinitiate/`                       |
| `cp -s source destination`            | Create symbolic links instead of copying                                 | `cp -s file.txt tinitiate/`                       |
| `cp --backup[=CONTROL] source destination` | Make a backup of each existing destination file                     | `cp --backup file.txt tinitiate/`                 |
---
* **mv [source] [destination]**: Move or rename files or directories.

Here's the updated table with examples included:

| Command                                       | Description                                                              | Example                                           |
|-----------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------|
| **mv [source] [destination]**                 | Move or rename a file or directory                                       | `mv file.txt tinitiate/`                          |
| `mv source destination`                       | Move or rename a file or directory                                       | `mv file.txt tinitiate/`                          |
| `mv -i source destination`                    | Prompt before overwrite                                                  | `mv -i file.txt tinitiate/`                       |
| `mv -f source destination`                    | Force move by overwriting the destination file without prompt            | `mv -f file.txt tinitiate/`                       |
| `mv -u source destination`                    | Move only when the source file is newer than the destination file or when the destination file is missing | `mv -u file.txt tinitiate/`           |
| `mv -v source destination`                    | Verbosely move files, showing each file being moved                      | `mv -v file.txt tinitiate/`                       |
| `mv --help`                                   | Display help information about the `mv` command                          | `mv --help`                                       |
| `mv --backup[=CONTROL] source destination`    | Make a backup of each existing destination file                          | `mv --backup file.txt tinitiate/`                 |
| `mv -n source destination`                    | Do not overwrite an existing file                                        | `mv -n file.txt tinitiate/`                       |
| `mv --strip-trailing-slashes source destination` | Remove any trailing slashes from each source argument                    | `mv --strip-trailing-slashes file.txt tinitiate/` |
| `mv -t target directory source`               | Move files into the target directory                                     | `mv -t tinitiate/ file.txt`                       |

### Viewing and Editing Files
* cat [file]: Display file contents.
* less [file]: View file contents page by page.
* nano [file]: Edit file using Nano text editor.
* vi [file]: Edit file using Vi text editor.
