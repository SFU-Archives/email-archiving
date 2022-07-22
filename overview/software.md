###### [Email Archiving](../README.md)
###### [Email Archiving at SFU](email-archiving-at-sfu.md) `|` Software `|` [Formats](formats.md) `|` [Transfer Workflow](transfer-workflow.md)

# Software

SFU Archives uses a number of software programs and utilities in its email archiving process. This page provides a basic list, with links to more detailed documentation (when available) on the Archives [Digital Repository Utilities](https://github.com/SFU-Archives/digital-repository-utilities) site.

The Archives' desktop computers run on Mac OS and all utilities must be able to run in that environment. Archivematica and AtoM are installed on Linux servers, but the user interface is web-based and OS-neutral.

### Microsoft Exchange / Outlook
The current platform for SFU's email system.
- [SFU Mail](https://www.sfu.ca/sfumail.html)).

### ePADD
Open-source software for processing historical email collections. Used by Archives for appraisal, selection, processing, and delivery of access to email archives.
- [ePADD project site](https://library.stanford.edu/projects/epadd)

### Archivematica
Open-source software for digital preservation. Used by Archives to create standardized Archival Information Packages (AIPs) for long-term preservation of transferred email.
- [Archivematica project site](https://www.archivematica.org/en/)

### AtoM (Access to Memory)
Open-source software for archival description and access, platform for Archives' online catalog of finding aids, [SFU AtoM](https://atom.archives.sfu.ca). Used by Archives to provide series-level descriptions of email archives in the context of the creator's fonds. For email, SFU AtoM contains descriptions only; access to the actual messages is provided via ePADD.
- [AtoM project site](https://www.accesstomemory.org/en/)
- [SFU AtoM site](https://atom.archives.sfu.ca)

### OfflineImap
Open-source utility for exporting email from IMAP-based email systems. Used by Archives as the main transfer mechanism, exporting email from a target SFU account; outputs email in `maildir` format.
- [OfflineImap project site](http://www.offlineimap.org)

### ClamAV
Open-source anti-virus utility used by Archives to scan transferred email (`maildir`) for viruses and malware.
- [ClamAV project site](https://www.clamav.net).
- [SFU Archives ClamAV documentation](https://github.com/SFU-Archives/digital-repository-utilities/blob/master/utilities/clamav.md)


### Emailchemy
Proprietary software able to convert email from / to various formats. Used by Archives to convert OfflineImap output (`maildir`) to `mbox` format for upload to ePADD for processing and Archivematica for preservation.
- [Emailchemy software site](https://weirdkid.com/emailchemy/)

### Python maildir2mbox script
Customized python script running on command line to convert `maildir` to `mbox`. This was the Archives' original method for getting SFU email in `mbox` format, and it provides an open-source alternative to Emailchemy. Emailchemy with its interface is simpler to use.

### Correspondents normalizer utility
Custom FileMaker database to support / automate normalization of an ePADD list of correspondents in an email archive.

### Archives Information System (AIS) database
Archives' custom in-house FileMaker database. Used to accession email transfers and register AIPs. Documentation available on the Archives' internal wiki.

###### Last updated: Jul 22, 2022
