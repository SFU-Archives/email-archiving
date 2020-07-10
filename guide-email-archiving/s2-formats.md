###### [Email Archiving Home](../README.md) > [Guide for Email Archives](./gde-home.md)
###### [1. Software](./s1-software.md) `|` 2. Formats `|` [3. Workflow](./s3-workflw.md) `|` [4. Acquisition](./s4-acquisition.md) `|` [5. Transfer Methods](./s5-transfer-methods.md) `|` [6. Appraisal and Selection](./s6-appraisal-and-selection.md)] `|` [7. Arrangement and Description](./s7-arrangement-and-description.md) `|` [8. Preservation](./s8-preservation) | [9. Access](./s9-access)

# 2. Formats
<img align="right" width="350" src="../images/email-formats.png">

The Archives' preferred formats for managing email are:

**Transfer:** `maildir`, `mbox`

**Ingest:** `mbox`

**Preservation:** `mbox`

**Access:** `ePADD`

<br clear="both>
<p></p>

## SFU email platform
The university's email system (SFU Mail) runs on Microsoft Exchange (server) and Outlook (client). SFU switched to Microsoft for email in 2018. From 2009-2018 the university used the [Zimbra Collaboration Suite](https://www.zimbra.com) as SFU Connect, and the Archives' first email transfers originated from the Zimbra system.

## Mbox
`mbox` originated with the Unix operating system as a format for storing email messages, and there are several variants within the `mbox` family. In 2005 the Internet Engineering Task Force (IETF) defined a standard `application/mbox` media type ([RFC4155](https://tools.ietf.org/html/rfc4155)), and `mbox` has become a defacto standard for moving email between different email systems and clients.

A single `mbox` file represents a folder and its contents in an email system.
- It aggregates into a single text file all the messages contained in an email folder, along with their attachments.
- Message headers and body are represented in plain text.
- Attachments are encoded in [Base64](https://en.wikipedia.org/wiki/Base64) as ASCII text appended to the message.

`mbox` files are mainly designed for storage. While they can be opened with any text editor and the header and body of messages (but not the attachments) are human-readable, access to `mbox` is generally via an email client / reader.

Given its wide use and the availability of cross-platform tools that can work with it, `mbox` is the Archives' preferred **preservation format**. But the Archives' digital preservation software, Archivematica, cannot normalize email to `mbox`; this must be done independently prior to ingest. Similarly, ePADD needs email already in `mbox` format for upload. For these reasons, `mbox` is also our preferred **ingest** format.

While some email systems may be able to natively export to `mbox` (e.g. Gmail), others (including SFU Mail) may do so poorly or require the production of an intermediary. SFU Archives uses a tool (OfflineImap) to export email out of the active system in `maildir` format, then runs a Python script to convert the `maildir` to `mbox`.

In general, for a format to be acceptable for transfer to SFU Archives, there must be a tool that allows conversion to `mbox`.

## Maildir
Like `mbox`, `maildir` is also an email storage format that represents email messages (header, body, attachments) as text files, with attachments encoded as Base64 ASCII. But where `mbox` aggregates all messages from the same mailbox into a single file, `maildir` stores each individual email message (plus attachments) as its own separate text file.

`mbox` seems to be more widely used, perhaps because it can store the same amount of email in a much smaller number of files. But the Archives' main export / transfer tool, OfflineImap, outputs only to `maildir`. For the Archives, therefore, `maildir` is intermediary **transfer format**. We use a Python script to convert it to `mbox` for ingest, and we do not retain the `maildir` copy once ingest is complete.

## ePADD

## Attachments

###### Last updated: Jul 10, 2020
