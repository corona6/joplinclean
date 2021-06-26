# joplinclean
Joplin cleaner for file system synchronise.

delete unused resources/revisions/tags for [Joplin](https://joplinapp.org/)

## Warning

- This is does not support for encryption.
- Only can use for file system synchronise.

## Install

```
$ curl --create-dirs -o ~/.joplinclean-bin/joplinclean https://raw.githubusercontent.com/corona6/joplinclean/master/joplinclean
$ chmod +x ~/.joplinclean-bin/joplinclean
$ sudo ln -s ~/.joplinclean-bin/joplinclean /usr/local/bin/joplinclean
```

## Usage

```
Usage:
  joplinclean [options] absolute-path

Examples:
  # delete image or file that not used in the note
  joplinclean /path/to/synchronise/directory

  # delete the history (revisions) of the note which are already deleted
  joplinclean -r /path/to/synchronise/directory

  # delete the tags that not link to any notes
  joplinclean -t /path/to/synchronise/directory

  # archive notebook will delete from Joplin and create zip file
  joplinclean /path/to/synchronise/directory --archive notebook-name /path/to/archive/notebook-name.zip

  # import notebook from zip file
  joplinclean /path/to/synchronise/directory --import /path/to/archive/notebook-name.zip

Options:
  -d, --data          Delete unused resources
  -f, --force         Delete unused resources even if it's in the revision
  -r, --revision      Delete unused revisions
  -t, --tag           Delete unused tags
  -y, --yes           Automatic yes to all prompts
  -h, --help          Print this help
  --archive           Archive notebook (Sub-notebooks are not supported)
  --import            Import notebook
```

## Example

```
joplinclean /Users/corona6/joplin
```

![](joplin_synchronise_directory.png)