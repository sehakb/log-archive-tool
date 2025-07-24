

# log-archive-tool

This is a simple command-line tool that compresses the contents of the `/var/log` directory into a `.tar.gz` archive file and saves it to a folder you specify.

## What it does

- Compresses the `/var/log` directory
- Adds a timestamp to the archive filename
- Saves the archive in the folder you provide
- Prints the archive path after it is created

## How to use

First, make the script executable and move it to your system path:

```bash
chmod +x log-archive
sudo mv log-archive /usr/local/bin/log-archive
````

Then run it like this:

```bash
sudo log-archive /path/to/target-folder
```

Example:

```bash
sudo log-archive /home/vagrant/logs
```

This will create a file like:

```
logs_archive_20250724_231000.tar.gz
```

and place it in the folder you chose.


The date and time are automatically added based on when you run the command.

## Notes

* Some files in `/var/log` require root access, so `sudo` is needed.
* The `.tar.gz` archive files are excluded from version control using `.gitignore`.
