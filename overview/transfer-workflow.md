###### [Email Archiving](../README.md)
###### [Email Archiving at SFU](email-archiving-at-sfu.md) `|` [Software](software.md) `|` [Formats](formats.md) `|` Transfer Workflow

# Transfer Workflow
The page outlines in brief the workflow for transfers of SFU email. For more detail (from the archivist's point of view), see the section on [Transfer Workflow](../archivist-workflow/overview.md).

![Workflow diagram](../images/transfer-workflow.png)

### Pre-transfer
The account owner and archivist negotiate transfer agreement and determine the scope of transfer (entire account or folder). The archivist sends the account owner a formal **Email Transfer Request** email, the account owner replies to signal consent, the archivist forwards the request to IT Services (ITS).

### Transfer
ITS uses the information in the **Email Transfer Request** to make a backup copy of the targeted email and copies it to a dedicated email account controlled by the Archives. The archivist uses `OfflineImap` to export the messages + attachments as `maildir`, runs a virus scan, then converts the `maildir` to `mbox` format.

### Validation
The archivist opens the `mbox` files in `Thunderbird` email client to get a count of messages transferred and compares this against the number of messages in the transfer account in SFU Mail. The archivist accessions the transfer in the `AIS database`, uses `SFU MoveIt` to package the `maildir` and `mbox` files and then uses `Bagger` to validate the resulting package, adds the `Accession number` and saves as the `transfer package` ready for ingest.

### Ingest
The archivist uploads the `transfer package` to the staging server on SFU Cloud, processes completely through Archivematica, and registers the `AIP` in the `AIS database`.

### Completion
The archivist notifies the account holder that the transfer has been completed, completes the `Accession record`, and deletes all transitory copies from SFU Mail, desktop, and staging server. The account holder receives the completion notice and may now delete the transferred email if desired.

<br clear="both">

###### Last updated: Apr 21, 2022
