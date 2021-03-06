
# Locatefile

Locate a file or directory from a custom database.

The database is created by you and consists of plain text documents containing file and directory paths.

## Examples

### 1. Locate a file

1. Locate a file using any part of its name.

```bash
locatefile my-doc # "/home/user/documents/my-document.txt"
```

```bash
locatefile oje # "/home/user/archives/backup/projects.txt"
```

*Note: The first match will be returned.*

2. Locate a file in a mounted drive (please see variable MOUNTPOINT_PATHS in [CONFIGURATIONS](CONFIGURATIONS) for more information).

```bash
locatefile my-notes # "MNTPNT_PATH/general/notes/my-notes.txt", where MNTPNT_PATH is
                    # one of the mountpoint paths specified in MOUNTPOINT_PATHS in CONFIGURATIONS
```

### 2. Locate a directory

```bash
locatefile -d arc # "/home/user/archives"
```

## Usage

1. Adjust any needed configurations in [CONFIGURATIONS](CONFIGURATIONS) (note: the only variable that really needs to be changed is DATABASE_FILE_NAMES).
2. Define the file and directory paths that will be sent to the database in [FILEPATHS](FILEPATHS).
3. Run [updatedb](updatedb).

## Notes

Locatefile...

* ...accepts regular expressions.
* ...does not support file names with spaces.

## Download

Run the following command to download Locatefile:

```bash
bash <(curl -s 'https://raw.githubusercontent.com/computingfoundation/'\
'gnu-linux-shell-usage.packaged-solutions/helper_scripts/cf-glsu.ps-download-locatefile.sh')
```

