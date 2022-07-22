###### [Email Archiving](../README.md) > Transfer Workflow for Archivists
###### [Overview](overview.md) `|` [Pre-transfer](pre-transfer.md) `|` Transfer `|` [Validation](validation.md) `|` [Appraisal](appraisal.md) `|` [Ingest](ingest.md) `|` [Completion](completion.md)

# B. Transfer
During the **transfer phase** SFU IT Services makes a copy of the `Transfer Folder` to the Archives' dedicated email transfer account. An archivist exports the email in `maildir` format, runs virus checks, then converts the `maildir` to `mbox` format.

## Contents
- [Receive notice from ITS](#receive-notice-from-its)
- [Export as maildir](#export-as-maildir)
- [Check for viruses and malware](#check-for-viruses-and-malware)
- [Convert maildir to mbox](#convert-maildir-to-mbox)

## Receive notice from ITS
[Workflow Diagram, steps B1-B4](../images/transfer-workflow.png)

ITS will make a copy of the producer's `Transfer Folder` to the Archives' transfer account and notify the archivist who submitted the service request ticket when this is complete.

## Export as maildir
[Workflow Diagram, step B5](../images/transfer-workflow.png)

An archivist runs OfflineImap on the `Transfer Folder` to export all messages and attachments.
- For installation instructions and more information about this utility, see the OfflineImap page in the Archives' [Digital Repository Utilities GitHub documentation site](https://github.com/SFU-Archives/digital-repository-utilities).

### Config file
The first time you run OfflineImap you will need to edit the configuration file.
- This is a Mac "hidden" file stored in your Home directory at `~/.offlineimaprc`.
- You can view Mac hidden files by pressing `SHIFT` + `COMMAND` + `.`
- Edit the config file with a text editor, e.g. BBEdit.
- See the [OfflineImap config file template](../downloads/offlineimap-config-file.txt).

The main settings you need to specify are:
- `localfolders` = folder for output on your local computer.
- `remoteuser` = user name of Archives' sponsored email account for transfer.
- `remotepass` = account password; you can enter or delete this line; if deleted you will be prompted for the password when running OfflineImap; if used, **delete this line when you have finished the transfer.**
- See the Archives' internal wiki for full settings.

You will not need to change these settings (except perhaps `remotepass`) if you subsequently run OfflineImap on the entire Archives' transfer account (i.e. the account contains only a single `Transfer Folder` and its Contents).

If the transfer account holds multiple transfer folders, you will need to specify the individual target folder (plus all its subfolders) in the config file:
- `folderfilter = lambda folder: folder in ['folder1', 'folder1/folder2']`
- If exporting the entire transfer account, delete the `folderfilter` line from the config file.

Listing all sub-folders in `folderfilter` can be time-consuming for transfers with a complex folder hierarchy; that is why it is advisable and simpler to process one transfer at a time through the Archives' email transfer account, export the entire account, then empty it out for the next one.

### Run the program
To run OfflineImap:
- Open a Terminal window.
- Enter `$ offlineimap` and hit return.

If you did not include the account password in the `remotepass` flag in the config file, you will prompted to enter the password in the Terminal window.

The utility will export all messages with attachments to the `localfolders` location specified in the config file.

## Check for viruses and malware
[Workflow Diagram, steps B6-B8](../images/transfer-workflow.png)

Check for viruses and malware by running ClamAV on the `maildir` output.
- It is important to do this before converting to `mbox`: with `maildir`, individual infected messages can be deleted, whereas with `mbox` one virus in one message means the whole folder (entire `mbox` file) is compromised.
- For installation instructions and more information about this utility, see the [ClamAV page] in the Archives' [Digital Repository Utilities GitHub documentation site](https://github.com/SFU-Archives/digital-repository-utilities).

Open a Terminal window to run ClamAV.

```
$ freshclam
$ clamscan -ri --log=<<PATH_TO_LOG/log.txt>> <<PATH_TO_MAILDIR_FOLDER>
```

The `freshclam` command updates the virus database.

The `clamscan` command runs the virus scan.
- `-r` flag = recursive, i.e. it will run on all sub-folders and their contents.
- `-i` flag = show only infected files.
- `--log` flag = write results to a log file at the location specified; the `log.txt` file should already exist before you run the scan.
- You can omit writing to a log file; in either case, the output will show in your Terminal window.
- To get the path to the `maildir` folder, you can you just drag it into your Terminal window.

### If you find infected files
If ClamAV turns up infected files, document this in a note to the collection file and remove and delete the files.
- You should advise the producer if you find extensive viruses and malware in their email.

## Convert maildir to mbox
[Workflow Diagram, step B9](../images/transfer-workflow.png)



###### Last updated: Jul 21, 2022
