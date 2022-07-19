###### [Email Archiving](../../README.md) > [Transfer procedures (Archives)](./00-introduction.md)
###### [1. Transfer folders](./01-transfer-folders.md) `|` [2. Transfer entire account](./02-transfer-account.md) `|` 3. Virus scan `|` [4. Convert to mbox](./04-convert-to-mbox.md) `|` [5. Validate](./05-validate-transfer.md) `|` [6. Accession](./06-accession-transfer.md) `|` [7. Archivematica ingest](./07-archivematica-ingest.md) `|` [8. Complete transfer](./08-complete-transfer.md)

# 3. Run virus scan

###### Status: under development

This step uses ClamAV software against the `maildir` output in [step 1](./01-transfer-folders.md) or [step 2](./02-transfer-account.md) to identify any messages or attachments that contain viruses or other malware.
- Infected files should be removed before conversion to `mbox` ([section 4](./04-convert-to-mbox.md).
- Deletion of infected files should be documented.

**Contents:**
- [3.1 Create a folder for infected files](#31-create-a-folder-for-infected-files)
- [3.2 Update virus definitions](#32-update-virus-definitions)
- [3.3 Run scan](#33-run-scan)
- [3.4 Remove infected files](#34-remove-infected-files)

## 3.1 Create a folder for infected files
Create a folder on your computer (e.g. desktop) to store copies of infected files; name the folder however you like (e.g. `Clamscan` or `infected_files`).

## 3.2 Update virus definitions
Make sure ClamAV's virus / malware definitions are up to date.
- Open a Terminal window and run the command `freshclam` to download the latest definitions.
- If you have not run this step for a while, it may take some time to complete.

## 3.3 Run scan
Open a Terminal window to run the ClamAV `clamscan` command.

```
Structure:
$ clamscan -ri --copy=<path/to/infected/files/folder> <path/to/target/folder>
```

```
Example:
$ clamscan -ri --copy=/Users/radancy/Desktop/Clamscan /Users/radancy/Desktop/maildir_output
```

The `clamscan` command has the following options:

`clamscan` = ClamAV command.

`-r` = recursive; all sub-directories in the target folder will be scanned.

`i` = infected; only infected files will be displayed in the Terminal output.

`--copy=<path/to/infected/files/folder` = file path of folder for copies of files identified as infected.
- This should be the folder you created above in step 3.1.
- ClamAV will makes a copy of any infected files it finds.

`<path/to/target/folder>` = file path of the target folder containing items to be scanned.
- This will be the `maildir` folder you created in [section 1](./01-transfer-folders.md) or [section 2](./02-transfer-account.md)

When the scan is complete, you will get a `scan summary` report in Terminal.

```
----------- SCAN SUMMARY -----------
Known viruses: 8153447
Engine version: 0.102.3
Scanned directories: 2
Scanned files: 9
Infected files: 0
Data scanned: 0.12 MB
Data read: 0.12 MB (ratio 1.00:1)
Time: 16.040 sec (0 m 16 s)
```

## 4.4 Remove infected files
Any infected files will be listed your Terminal window and a copy created and stored in the `infected_files` folder you specified in the `copy=` option.

If there are infected files:
- Identify and locate the infected files.
- **Delete the actual file(s) from the `maildir` folder.**
- Copy and paste the Terminal window output (list of infected files + `scan summary` report) to a text file.
- Save the text file for eventual upload to the AIS Accession record (see [section 6, Accession transfer](./06-accession-transfer.md) in this procedures).

###### Last updated: Jul 22, 2020
