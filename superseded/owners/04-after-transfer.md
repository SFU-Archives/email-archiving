###### [Email Archiving](../../README.md) > [Transfer procedures (account owners)](./00-introduction.md)
###### [1. Before you start](./01-before-you-start.md) `|` [2. SFU accounts](./02-sfu-accounts.md) `|` [3. Non-SFU accounts](./03-non-sfu-accounts.md) `|` 4. After transfer `|` [5. Checklist](./05-checklist.md)

# 4. What happens to email after transfer?

Through the transfer process, SFU Archives acquires or makes a copy of your email and stores it offline in the `mbox` format.

For SFU email, the Archives uses a tool called [OfflineImap](http://www.offlineimap.org) to download messages and attachments from the SFU mail server in `maildir` format, then runs a Python script to convert the `maildir` to `mbox`. For email originating in other systems, the donor must be able to provide it already exported to `mbox` or in a format that the Archives can convert to `mbox` (see [section 3, Non-SFU Accounts](./03-non-sfu-accounts)).

When a transfer is complete, an archivist accessions it (assigns a unique `Accession number` to the transfer), then uploads the records to the Archives' digital repository using [Archivematica software](https://www.archivematica.org/en/). Here the email remains in "backlog." At a later date, an archivist will further process the email using [ePADD software](https://library.stanford.edu/projects/epadd). This will typically involve further appraisal, selection, description, and curation; and the archivist will prepare preservation and access packages for long-term storage in the digital preservation system.

When processing is complete, the archivist updates the Archives' online catalog, [SFU AtoM](https://atom.archives.sfu.ca), with a series-level description of the email records in the context of the creator's entire holdings ("fonds").

Email archives often contain sensitive personal information of third parties, as well as other confidential information. Requests for access are handled on a case-by-case basis, and access for researchers will typically require a [Research Agreement](http://www.sfu.ca/content/dam/sfu/archives/ARMDForms/Research%20Agreement.pdf). The Archives delivers access to the records through a dedicated offline terminal in the Archives' reading room using the [ePADD platform](https://library.stanford.edu/projects/epadd).

For more information on the Archives' workflows and processes for handling email, see the broader discussion in [Guide for Email Archives](../../guide/00-introduction.md) (under development).

###### Last updated: Jul 21, 2020
