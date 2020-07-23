###### [Email Archiving](../README.md) > [Guide](./00-introduction.md)
###### [1. Software](./01-software.md) `|` [2. Formats](./02-formats.md) `|` [3. Workflow](./03-workflow.md) `|` [4. Acquisition](./04-acquisition.md) `|` 5. Transfer methods `|` [6. Appraisal and selection](./06-appraisal-selection.md) `|` [7. Arrangement and description](./07-arrangement-description.md) `|` [8. Preservation](./08-preservation.md) | [9. Access](./09-access.md)

# 5. Transfer methods

Transfer is an operation that exports email from an email server and copies it to a machine or storage device in the Archives' custody or control. Five main approaches have been identified; different methods may be appropriate in different circumstances. All but one ([method 5.3](#53-user-self-export-and-transfer)) requires the use of the open-source utility OfflineImap to export email out of the original system.

**Contents**
- [5.1 ITS backup and restore](#51-its-backup-and-restore)
- [5.2 Archives export from a shared folder](#52-archives-export-from-a-shared-folder)
- [5.3 User self-export and transfer](#53-user-self-export-and-transfer)
- [5.4 In-person assisted export](#54-in-person-assisted-export)
- [5.5 Temporary transfer of account ownership](#55-temporary-transfer-of-account-ownership)

## 5.1 ITS backup and restore
This was the Archives' original transfer method, used from 2013-2016.

The university's IT Services made a backup copy of an account, stored it offline, then restored the backup to a transfer account under the Archives' control. The Archives would then run OfflineImap to export and transfer the email.

This method was most suitable for transfers of inactive SFU accounts (take the entire account). It was successfully used with SFU's previous email platform, the Zimbra Collaboration Suite (used at the university from 2009-2018). It has now been superseded by [method 5.5 below](#55-temporary-transfer-of-account-ownership) in SFU's present Microsoft email system.

##5.2 Archives export from a shared folder
This is the preferred method for transfers of email from ongoing, active SFU accounts, e.g. current staff, staff / faculty who retire but retain their accounts, or role-based departmental accounts.

The account owner creates a transfer folder within their account, moves emails to the transfer folder, and creates permissions that share the transfer folder(s) with Archives. The Archives then run OfflineImap on the shared folder to export and transfer the email.

The [Transfer procedures page](../transfer-procedures/transfer-home.md) contains documentation for both [account owners](../transfer-procedures/account-owners/00-introduction.md) and [SFU archivists](../transfer-procedures/archives/00-introduction.md).

The main drawback with this method is that it requires account owners to add permissions to each and every folder included in the transfer. Depending on how the owners structured their email account, this may entail considerable work (e.g. if they organized their email into a large number of folders, sub- and sub-sub-folders). [Method 5.4](#54-in-person-assisted-export) provides a workaround.

## 5.3 User self-export and transfer
This is the preferred method for transfers of non-SFU email.

The account holder exports their own email by themselves into a format acceptable to the Archives, then transfers it following the Archives' standard digital transfer procedures. Some donors may lack sufficient technical knowledge to manage their own export. The Archives may be able to provide support on a case-by-case basis depending on the email system and the donor's computing environment.

At present, the only acceptable transfer formats are `mbox` and `maildir` (see in this Guide [section 2, Formats](./02-formats.md).

The approach was successfully tested in 2019 with Gmail, which can be easily exported in `mbox` formats; see [transfer procedures for accounts owners, section 3.1](../transfer-procedures/account-owners/03-non-sfu-accounts.md5) for instructions for Gmail.

The Archives' standard digital transfer procedures are documented in a separate repository on this GitHub site.

## 5.4 In-person assisted export
This method provides an alternative to [5.2, export from a shared folder](#52-archives-export-from-a-shared-folder), and it provides a workaround when the account owner is unable or unwilling to manually add permissions to a large number of transfer folders.

In this scenario, an archivist meets with the account owner and uses the Archives' own utilities to transfer the email. For example, the donor may come in person to the Archives, or an archivist may visit the donor with an Archives' laptop computer. The archivist runs OfflineImap on the holder's account, with the account owner entering their credentials (password) when prompted to export the email to an Archives' machine or storage device. The account owner's password is not stored or retained by the Archives.

With this method the Archives may take either targeted transfer folders or a copy of the entire account, depending on the agreement with the donor.

In principle OfflineImap should work with any IMAP-based email system, so that this method is not limited to SFU account. But in practice, the Archives has to date only tested it with SFU email.

## 5.5 Temporary transfer of account ownership
This is the preferred method for transfers of inactive accounts, e.g. the account of an administrator or faculty member who passes away and the estate agrees to donate their email.

In this scenario ITS transfers temporary ownership of the account to the Archives, i.e. it re-sets the account password and provides this to Archives. The Archives then runs OfflineImap against the account to export the email to one of its own machines. ITS then re-sets the password so the Archives has no further access.

This method has not yet been tested, but should be fairly straightforward.

Note that SFU does not currently have a formal policy relating to the retention and disposal of inactive email accounts. The Archives generally treats this as a donation of records negotiated with the account owners or their estate.

###### Page last updated: Jul 21, 2020
