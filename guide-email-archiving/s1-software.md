###### [Email Archiving Home](../README.md) > [Guide for Email Archives](./gde-home.md)
###### 1. Software `|` [2. Formats](./s2-formats.md) `|` [3. Workflow](./s3-workflw.md) `|` [4. Acquisition](./s4-acquisition.md) `|` [5. Transfer Methods](./s5-transfer-methods.md) `|` [6. Appraisal and Selection](./s6-appraisal-and-selection.md)] `|` [7. Arrangement and Description](./s7-arrangement-and-description.md) `|` [8. Preservation](./s8-preservation) | [9. Access](./s9-access)

# Software

This section provides a brief overview of the software programs and utilities used by SFU Archives in its email archiving process. The Archives' desktop computers run on Mac OS and all utilities must be able to run in that environment. Archivematica and AtoM are installed on Linux servers, but the user interface is web-based and OS-neutral.

**Microsoft Exchange / Outlook**
- The current platform for SFU's email system (SFU Mail).

**ePADD**
- [Open-source software](https://library.stanford.edu/projects/epadd) for processing historical email collections.
- Used by Archives for appraisal, selection, processing, and delivery of access to email archives.

**Archivematica**
- [Open-source software](https://www.archivematica.org/en/) for digital preservation.
- Used by Archives to create standardized Archival Information Packages (AIPs) for transferred email and send them to storage for long-term preservation.

**AtoM (Access to Memory)**
- [Open-source software](https://www.accesstomemory.org/en/) for archival description and access, platform for Archives' online catalog of finding aids, [SFU AtoM](https://atom.archives.sfu.ca).
- Used by Archives to provide series-level descriptions of email archives in the context of the creator's fonds.
- For email, SFU AtoM contains descriptions only; access to the actual messages is provided via ePADD.

**OfflineImap**
- [Open-source utility](http://www.offlineimap.org) for exporting email from IMAP-based email systems.
- Used by Archives as the main transfer mechanism, exporting email from a target SFU account.
- Outputs email in `maildir` format.

**ClamAV**
- [Open-source anti-virus utility](https://www.clamav.net).
- Used by Archives to scan transferred email (`maildir`) for viruses and malware.

**Maildir conversion script**
- Custom Python script to convert OfflineImap output (`maildir`) to a format (`mbox`) that can be uploaded to ePADD for processing and Archivematica for preservation.

**Correspondents normalizer utility**
- Custom FileMaker database to support / automate normalization of an ePADD list of correspondents in an email archive.

**Archives Information System (AIS) database**
- Archives' custom in-house FileMaker database.
- Used to accession email transfers and register AIPs.

**AIP and DIP retrieval scripts**
- Custom scripts to download AIPs and DIPs in order to verify successful ingest and support researcher access.

###### Last updated: Jul 10, 2020
