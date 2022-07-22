###### [Email Archiving](../README.md)
###### [Email Archiving at SFU](email-archiving-at-sfu.md) `|` [Software](software.md) `|` [Formats](formats.md) `|` Transfer Workflow

# Transfer Workflow
The page outlines in brief the workflow for transfers of SFU email. For more detail (from the archivist's point of view), see the sections on [Transfer Workflow](../archivists/overview.md).

![Workflow diagram](../images/transfer-workflow.png)

### [Pre-transfer](../archivists/transfer.md)
Negotiate a transfer agreement with an account owner ("producer") and determine the scope of transfer (entire account or specific folders). The producer prepares a `Transfer Folder`, the archivist submits a service request ticke to SFU IT Services (ITS).

### [Transfer](../archivists/transfer.md)
Receive a copy of the targeted email `Transfer Folder` from ITS into the Archives' dedicated email account; use OfflineImap to export the messages + attachments as `maildir`, run a virus scan, then convert the `maildir` to `mbox` format.

### Validation
Determine whether transfer / export / conversion was successful (no data lost) by comparing message counts in the transfer account in SFU Mail vs. the `mbox` files when opened in Thunderbird or Mac's Mail email client; generate a tree-view of the folder directory structure.

### Appraisal
Where feasible, conduct folder-level appraisal, document appraisal decisions and eliminate folders not selected for long-term preservation.

### Ingest
Re-export appraised / selected email, convert to `mbox`, upload to the staging server, ingest to Archivematica and register the AIP in the AIS database.

### Completion
Notify the producer that the transfer has been completed, finalize the `Accession record`, and delete all transitory copies from SFU Mail, desktop, and staging servers. The producer may now delete the transferred email if desired.

<br clear="both">

###### Last updated: Jul 22, 2022
