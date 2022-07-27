###### [Email Archiving](../README.md) > Transfer Workflow for Archivists
###### [Overview](overview.md) `|` [Pre-transfer](pre-transfer.md) `|` [Transfer](transfer.md) `|` Validation `|` [Appraisal](appraisal.md) `|` [Ingest](ingest.md) `|` [Completion](completion.md)

# Validation
<img align="right" width = "450" src="../images/workflow-phaseC.png">

During the **validation phase** the archivist confirms that no data was lost during transfer / export / conversion process. There is no easy way to do this. For now, the Archives relies on a comparison between (i) the number of messages in the `Transfer folder` after ITS copies it to the Archives' transfer account and (ii) the number of messages in an email browser (Thunderbird or Mac Mail) after the `mbox` files are loaded.

## Contents
- [Load mbox files into an email browser](#load-mbox-files-into-an-email-browser)
- [Compare message counts](#compare-message-counts)
- [If message counts do not match](#if-message-counts-do-not-match)
- [Generate tree view of folder structure](#generate-tree-view-of-folder-structure)

## Load mbox files into an email browser
[Workflow Diagram, step C1](../images/transfer-workflow.png)

You use Mac Mail or Thunderbird to load the `mbox` files in order to get message counts by folder.
- Mac Mail is generally easier to use **if you are not actively using this app for your current mail.**
- Both apps will display the number of "unread" messages by folder.
- By default, all messages are flagged as "unread" on first opening of the email client.

### Mac Mail:
Select `File > Import Mailboxes > Import data from ... Messages in mbox format` and navigate to the set of `mbox` files representing the `Transfer Folder`.
- The folders will appear in Mac Mail under `Smart Mailboxes > Import`.

### Thunderbird:
Copy the `mbox` files to Thunderbird's `Local Folders` directory.
- To access, turn on Mac hidden files (`SHIFT` + `COMMAND` + `.`) and navigate to `~/Library/Thunderbird/Profiles/<<random-text>>.default/Mail/Local Folders.`
- Open / restart Thunderbird, the `Transfer Folder` and its sub-folders will appear under `Local Folders`.

## Compare message counts
[Workflow Diagram, steps C2-C3](../images/transfer-workflow.png)

In the [Transfer phase](transfer.md#record-message-counts) at step B5, you should have recorded message counts by folder (e.g. in a spreadsheet) following the copying by ITS of the `Transfer Folder` to the Archives' transfer account. You can now compare these numbers to the counts you get from Mac Mail or Thunderbird.
- This will indicate whether any messages were lost on export to `maildir` and conversion to `mbox`.

## If message counts do not match
[Workflow Diagram, step C4](../images/transfer-workflow.png)

If message counts do not match, try re-running the [export](transfer.md#export-as-maildir) and [conversion](transfer.md#convert-maildir-to-mbox) steps.

If the message counts still do not match, this likely points to some data corruption or loss during export / conversion and options at this point are limited. The Archives has not yet encountered this issue. Some possibile actions:
- Investigate the folders in both SFU Mail (Outlook) and Mac Mail or Thunderbird to identify missing messages.
- Compare the corresponding `maildir` and `mbox` files to see where the problem originated (export or conversion).
- Document the extent of missing messages in a note for the collection file.
- You can consult with ITS and Artefactual to see if they have any insight into the problem, but be aware that neither is responsible for supporting the Archives' export and conversion utilities (OfflineIMAP, maildir2mbox, Emailchemy) or ensuring they work as expected.

In the end, you may just be left with a decision as to whether the extent of the losses is acceptable or not and whether to continue or cancel the email transfer project.

## Generate tree-view of folder structure
[Workflow Diagram, step C5](../images/transfer-workflow.png)

Use [Tree](https://github.com/SFU-Archives/digital-repository-utilities/blob/master/utilities/tree.md) to generate a tree-view of the email folder structure.
- This provides documentation for the collection file of the original directory structure.
- It can be used during the [Appraisal phase](appraisal.md) and can be copied into an [Appraisal report](appraisal.md#appraisal-report).

Open a Terminal window and run Tree on the top-level folder of the `mbox` output.
- `$ tree -o <<file/path/for/output/report/tree.txt>> <<target_folder>>`
- The `-o` flag tells the program to output the data to a text file; omit if you want the output to print to the Terminal window instead (from there you can copy and paste to a text file).

You can clean up the text in several ways with a text editor (e.g. BBEdit).
- Find and replace blank spaces that Tree represented with escape characters (replace `\ ` with ` `).
- Find and replace the `.mbox` file extensions (replace `.mbox` with nothing).

For more information on installation and use of Tree, see the [entry for Tree](https://github.com/SFU-Archives/digital-repository-utilities/blob/master/utilities/tree.md) in the Archives' [Digital Repository Utilities site](https://github.com/SFU-Archives/digital-repository-utilities).

###### Last updated: Jul 26, 2022
