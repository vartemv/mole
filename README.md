# mole script

The mole script is a powerful tool which allows you to manage your files in a flexible and expressive way. It opens
files for editing, keeps track of previously opened files, can filter or sort files according to user-defined
preferences, and generates logs of its operations.

# Usage

```shell
./mole filename
```

This command opens a file named filename for editing.

```shell
./mole -g mygroup filename
```

This command opens a file named filename for editing and assigns it to the group mygroup.

```shell
./mole directory_name
```

This command will display all files that were previously opened with the mole script and assigned to the group mygroup.

```shell
./mole -a YYYY-MM-DD list
```

This command will display all files that were opened after the date YYYY-MM-DD.

```shell
./mole secret-log directory_name
```

This command will write a compressed log to the .mole directory in your home folder, which logs opening dates of the
files in the directory directory_name.

# Common Log

The mole script uses a common log file specified by the environment variable MOLE_RC. The MOLE_RC environment variable
is critical for the script's correct operation. It's value should be set to the desired location for the mole script
operations common log

# List Command (list)

The list command is used to list files that were opened by the script. If it is used with -g flag, it lists all the
files under the given group. If it is used with -a flag, it lists all files that were opened after the specified date.

```shell
./mole list directoryname
./mole -g mygroup list
./mole -a YYYY-MM-DD list
```
