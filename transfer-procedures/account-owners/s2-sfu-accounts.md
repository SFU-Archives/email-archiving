###### [Email Transfer Procedures for Account Owners](./account-owners.md) `|` [1. Before You Start](./s1-before-you-start) `|` 2. SFU Accounts `|` [3. Non-SFU Accounts](./s3-non-sfu-accounts.md) `|` [4. After Transfer](./s4-after-transfer.md)

# 2. SFU Email Accounts
This section describes how to transfer email from an SFU account.

**Contents**
- [2.1 Set up a transfer folder](#2.1-set-up-a-transfer-folder)
- [2.2 Add permissions to the Inbox](#2.2-add-permissions-to-the-inbox)
- [2.3 Add permissions to the transfer folder(s)](#2.3-add-permissions-to-the-transfer-folders(s))
- [2.4 Transfer, validation, accessioning](#2-4-transfer-validation-accessioning)
- [2.5 Remove permissions](#2-5-remove-permissions)

## 2.1 Set up a transfer folder
<img align="right" width="350" src="../../images/transfer-folder.png">

Create a transfer folder in your Inbox.
- The Archives works on Mac computers and Outlook for Mac requires shared folders to be nested under the owner's Inbox.

Move all messages or folders you wish to transfer into the transfer folder.
- You can name the transfer folder however you wish.
- You can move individual messages or folders containing messages into the transfer folder.
- You can add as many folders-within-folders as you wish, but **be aware that you will need to add permissions to every individual folder** (see [step 2.2](#2.2-add-permissions-to-the-inbox) and [step 2.3](#2.3-add-permissions-to-transfer-folders)).

**`In general you should try to maintain messages in their original folder structure as you used them; this provides valuable context for future researchers that will help them understand your email archive.`**

## 2.2 Add permissions to the Inbox

You need to add permissions to every folder (including the `Inbox`) to share them with Archives.
- Permissions should be given to the `archeml` account – this is an account used by Archives uniquely for email transfer.
- The permissions needed on the `Inbox` folder are different (more limited) than those for the other folders.
- The instructions below show how to add permissions; see also IT Services' help page on sharing folders in Outlook.

**Steps**

<img align="right" width="350" src="../../images/permissions-inbox.png" />
Right-click the `Inbox` folder and from the popup menu select "Permissions…"
<br clear="both">
<p></p>

<img align="right" width="350" src="../../images/permissions-inbox.png" />
A new dialog box appears, `Permissions for the Inbox folder`.
- Click the `+` button to add a new permission.
<br clear="both">
<p></p>

<img align="right" width="350" src="../../images/add-email1.png" />
A new dialog box appears prompting you to add the email address of the person you wish to share the folder with.
- Enter "archeml" and click the `Search Directory` button.
<br clear="both">
<p></p>

<img align="right" width="350" src="../../images/add-email2.png" />
The name `Archives Digital Repository – archives_repository@sfu.ca` should appear.
- Click the `Add` button.
<br clear="both">
<p></p>

<img align="right" width="350" src="../../images/set-permissions-inbox.png" />
The Archives will now appear in the list of permissions.
- Make sure it is selected and highlighted.

- Check the box `Folder visible` and leave the `Permission level` drop-down selection to "None."

- Click the `OK` button to complete.
<br clear="both">
<p></p>

These settings mean that your `Inbox` will be visible in the `archeml` account ("folder visible") but its contents cannot be viewed or accessed (permission level = "none"); only the folders that you explicitly designate in the next step will be accessible to the Archives.

## 2.3 Add permissions to the transfer folder(s)

Permissions in Outlook are not inherited by sub-folders from a top-level parent folder: _you need to explicitly add permissions to the transfer folder and each sub-folder inside it._
- Even though a folder is placed within the transfer folder, the Archives will not be able to access its contents unless you explicitly share it with the `archeml` account.

**Steps**

For the transfer folder and every sub-folder contained within it repeat the same steps as you applied to the `Inbox`. The only difference is in the last step, where you specify the actual permissions on the folder.
- Select "Archives Digital Repository" so that it is highlighted.
- In the drop-down box labelled `Permission level` select "Reviewer"; the `Folder visible` box will default to checked; make sure to leave it checked.

**Reviewer** permission means that an archivist will have read-only access to the transfer folders, which is all we need to transfer the email.

The screenshot on the left below shows the settings for Reviewer permissions; and on the right an example of how a shared folder appears in the `archeml` account:

<p align="center">
<img align="right" width="350" src="../../images/set-permissions-reviewer.png" />
<img align="right" width="350" src="../../images/view-shared-folder.png" />
<br clear="both">
</p>

## 2.4 Transfer, validation, accessioning

Your email is now ready for transfer, validation, and accessioning.
- **Transfer** copies the email over to an Archives' account (`archeml`), then exports it from the SFU Mail system.
- **Validation** verifies that all folders you intended to transfer were in fact successfully received.
- **Accessioning** processes the transferred email into the Archives' digital preservation system.

All of these steps are done by the Archives, but they require communication between the account owner and the Archives.

**Steps**

Advise the Archives when you have finished setting up the transfer folder(s) and added permissions.
- If in doubt about who to contact, send an email to `moveit@sfu.ca` (the Archives' generic account for digital transfers) or `archives@sfu.ca` (the Archives' reference desk).

Receive notification from the Archives that it has transferred the email.
- Transfer occurs behind the scenes. You will not notice any change in your own account and the transfer folder and any sub-folders remain in place.
- An archivist has accessed the transfer folder via the shares you created in steps 2.2 and 2.3, copied its contents to the Archives' `archeml` account, and ran a utility (`OfflineImap`) to download the messages and attachments from the SFU mail server to an Archives' computer.

The notification message you receive will include a list of all folder names included in the transfer. Review this list to ensure that the transfer is complete.
- It is possible, for example, that you inadvertently missed some folders when adding permissions in step 3.2.
- If folders are missing from the transfer list, review the permissions on these folders and make sure they have been shared with the Archives.

Reply to the Archives: confirm that the transfer list is either complete or indicate that folders were missed and that permissions on these folders reviewed / added.
- If folders were missed, the Archives will re-run the entire transfer.

Receive an _Accession notice_ from Archives.
- On receipt of your final confirmation, an archivist will accession the transfer (assign it a unique `Accession number`) and upload it to the Archives' digital preservation system (`Archivematica`) to await further processing at a later date.

**`Note that there may be a considerable time lag between completion of transfer (accessioning) and completion of processing (archival description).`**
- For more on this, see [Section 4, What happens to email after transfer?](./s4-after-transfer.md)

## 2.5 Remove permissions

Your transfer is now complete. You should now remove the Archives' permissions from the transfer folders.

Always delete the Archives' permission on your `Inbox`.

If you no longer need to access the email messages transferred, you can now delete them from your account. But see the caution in [Section 1](./s1-before-you-start) – **`once deleted, you will not be able to view transferred email from your SFU account.`** The Archives' access protocols are set up for third parties to access historical email collections in an offline environment. If you need continuing access to the email, do not delete it from your account.

If you do retain some or all of the transferred messages, move them to a folder in your account clearly marked as already transferred (e.g. a folder named `Transferred to Archives`, with sub-folders for each Accession Number). This ensures that you do not inadvertently transfer the same records later on.

If you plan to regularly transfer email to the Archives in the future, you may wish to retain the same set of transfer folders with their permissions so that you do not have to repeat the process of setting up permissions on every folder and sub-folder.

The easiest way to do this is to move the set out of your `Inbox`, leave the permission entry on the top-level transfer folder, but change the settings to `Permission level` = "None" and `Folder visible` = unchecked.

- Then later, when you want make another transfer, simply add back the permission settings, move the set of transfer folders to your `Inbox`, and notify the Archives that you are ready to make another transfer.

###### Last updated: Jul 8, 2020