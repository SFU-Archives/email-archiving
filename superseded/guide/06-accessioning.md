###### [Email Archiving](../README.md) > [Guide](./00-introduction.md)
###### [1. Software](./01-software.md) `|` [2. Formats](./02-formats.md) `|` [3. Workflow](./03-workflow.md) `|` [4. Acquisition](./04-acquisition.md) `|` [5. Transfer methods](./05-transfer-methods.md) `|` 6. Validation and accessioning `|` [7. Appraisal and selection](./07-appraisal-selection.md) `|` [8. Arrangement and description](./08-arrangement-description.md) `|` [9. Preservation](./09-preservation.md) | [10. Access](./10-access.md)

# 6. Validation and Accessioning
On receipt of an email transfer, an archivist validates and accessions the transfer. Detailed instructions are given in the Transfer procedures; this page just provides an overview.

**Contents**
- [6.1 Virus scan](#61-virus-scan)
- [6.2 Conversion to mbox](#62-conversion-to-mbox)
- [6.3 Validation](#63-validation)
- [6.4 Accessioning](#64-accessioning)

## 6.1 Virus scan
An archivist uses ClamAV to scan transferred email for files containing virus or other malware.

For email from SFU accounts, the scan should be run on the `maildir` output from OfflineImap and before conversion to `mbox`. Because `maildir` structures each email message and its attachments as a single text file, it is easier to isolate and remove infected files when they are still in `maildir` form. On conversion to `mbox` all messages and attachments from the same mailbox folder are aggregated into a single file, so that infection of a single message will affect the entire folder.

Infected files should be removed, so that they are not included in the `mbox` files that are ingested to Archivematica and processed by ePADD. The scan log and a list of infected files should be included in the documentation filed with the Accession record on the fonds collection file.

See the [Transfer procedures for SFU archivists, section 3](../transfer-procedures/archives/03-virus-scan.md) for detailed instructions.

## 6.2 Conversion to mbox
Any email transferred to SFU Archives must be in `mbox` format or a format that allows for conversion to `mbox`. For SFU accounts, this is handled by using OfflineImap to export the email as `maildir`, then running a Python script to convert the `maildir` to `mbox`.

See [section 2 in this Guide](./02-formats.md) for more information on formats, and the [Transfer procedures for SFU archivists, section 4](../transfer-procedures/archives/04-convert-to-mbox.md) for detailed instructions for conversion.

## 6.3 Validation
Validation is an operation to verify that all the email messages that the account owner intended to transfer were in fact successfully transferred. For SFU accounts, this means that all messages were successfully exported in the `maildir` output generated by OfflineImap and that all transfer folders are represented as `mbox` files.

There is no way currently to easily generate and compare pre- and post-export counts of messages and attachment. The Archives should explore ideas and utilities for addressing this gap in the future.

The archivist does generate a list of all `mbox` files created (corresponding to the transfer folders exported) and includes this list in the notification message sent to the account owner following transfer. The owner is expected to review the list and confirm that all (and only those) folders intended for transfer were captured. Because the owner must manually add explicit permissions to each and every folder that is transferred, it is easy to make mistakes here. The confirmation review of folders at least offers a check on this aspect of the process.

For more details, see the [Transfer procedures for SFU archivists, section 5](../transfer-procedures/archives/05-validate-transfer.md).

## 6.4 Accessioning
When an archivist has validated an email transfer, the transfer is formally accessioned into the Archives' holdings. This means it is registered in the Archives' AIS FileMaker database, assigned a unique accession number, and provided with a minimal description. The `mbox` file(s) are ingested to Archivematica and fully processed as AIPs – see [section 9 in this Guide (Preservation)](./09-preservation.md) for more on Archivematica processing.

The Accession table in the AIS database broadly follows the [Canadian Archival Accession Information Standard (CAAIS)](http://archivescanada.ca/CWG_AccessionStandard). Database documentation is available elsewhere (and will eventually be migrated to this GitHub site). Email-specific application of certain fields are noted in the [Transfer procedures for archivists](../transfer-procedures/archives/00-introduction.md).

###### Last updated: Aug 13, 2020