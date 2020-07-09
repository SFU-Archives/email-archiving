###### [Email Archiving Home](../../README.md) > [Email Transfer Procedures for Account Owners](./account-owners.md)
###### [1. Before You Start](./s1-before-you-start.md) `|` [2. SFU Accounts](./s2-sfu-accounts.md) `|` [3. Non-SFU Accounts](./s3-non-sfu-accounts.md) `|` 4. After Transfer `|` [5. Checklist](./s5-checklist.md)

# 4. What Happens to Email After Transfer?

Through the transfer process, SFU Archives acquires or makes a copy of your email (and associated attachments) and stores it offline in the `mbox` format.

For SFU email, the Archives uses a tool called [OfflineImap](http://www.offlineimap.org) to download email from the SFU mail server in `maildir` format, then runs a Python script to convert the `maildir` to `mbox`. For email originating in other systems, the donor must be able to provide it already exported to `mbox` or in a format that the Archives can convert to `mbox` (see [Section 3, Non-SFU Accounts](./s3-non-sfu-accounts)).

When a transfer is complete, an archivist accessions the records (assigns a unique `Accession number`) and uploads the transfer to the Archives digital repository using [Archivematica software](https://www.archivematica.org/en/). Here the email remains in "backlog." At a later date, an archivist will further process the transfer using [ePADD software](https://library.stanford.edu/projects/epadd). This will typically involve further appraisal, selection, description, and curation; and the archivist will prepare preservation and access packages for long-term storage in the digital preservation system.

When processing is complete, the archivist updates the Archives' online catalog, [SFU AtoM](https://atom.archives.sfu.ca), with a series-level description of the email records in the context of the creator's entire holdings ("fonds").

Email archives often contain confidential and / or sensitive personal information of third parties. Requests for access are handled on a case-by-case basis, and access for researchers will typically require a [Research Agreement](http://www.sfu.ca/content/dam/sfu/archives/ARMDForms/Research%20Agreement.pdf). The Archives delivers access to the records through a dedicated offline terminal in the Archives' reading room using the [ePADD platform](https://library.stanford.edu/projects/epadd).

For more information on the Archives' workflows and processes for handling email, see the more detailed guidelines on [Email Archiving at SFU Archives](../../guide-email-archiving/gde-home.md) (forthcoming).

###### Last updated: Jul 8, 2020
