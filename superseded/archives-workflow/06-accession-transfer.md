###### [Email Archiving](../README.md) > [Guide](./00-introduction.md)
###### [1. Software](./01-software.md) `|` [2. Formats](./02-formats.md) `|` [3. Workflow](./03-workflow.md) `|` [4. Acquisition](./04-acquisition.md) `|` [5. Transfer methods](./05-transfer-methods.md) `|` [6. Accessioning](./06-accessioning.md) `|` [7. Appraisal and selection](./07-appraisal-selection.md) `|` [8. Arrangement and description](./08-arrangement-description.md) `|` [9. Preservation](./09-preservation.md) | [10. Access](./10-access.md)

# 6. Accessioning

All email transfers are accessioned in the Archives' FileMaker AIS database. This page provide a guide to data entry in the Accession record. The AIS Accession table generally follows the [Canadian Archival Accession Information Standard (CAAIS)](http://www.archivescanada.ca/CWG_AccessionStandard).

The Accession record must be created prior to ingest to Archivematica, so that the `Accession number` can be entered in the Archivematica Dashboard when processing the transfer.

**Contents**
- [6.1 Identity tab](#61-identity-tab)
- [6.2 Archival units tab](#62-archival-units-tab)
- [6.3 RRSDAs tab](#63-rrsdas-tab)
- [6.4 Sources tab](#64-sources-tab)
- [6.5 Materials tab](#65-materials-tab)
- [6.6 Storage tab](#66-storage-tab)
- [6.7 Management tab](#67-management-tab)
- [6.8 Workflow tab](#68-workflow-tab)

## 6.1 Identity tab
The `Identity tab` contains fields that uniquely identify the email transfer.

### Accession number
Automatically assigned by the system with the next available serial number in the form `YYYY-NNN`

```
Example
2020-002
```

### Accession title
Use the account owner's name + "email": `<creator_name> email`.

```
Example
Michael Fellman email
```

### Other identifiers
Enter the account email address.

```
Example
fellman@sfu.ca
```

### Relation to SFU
This field is intended to indicate whether or not the material are university records (subject to FIPPA) or personal records. In the case of the email of SFU faculty or staff, this is likely to be a mix.

Options:
- "University" = account owner was mainly acting in their capacity as a university administrator or officer; use this for senior administrators' email.
- "Campus community" = account owner is a member of the SFU community (SFU student, faculty, staff, or officer) and the email mainly reflects their personal correspondence; use this for private donations of faculty members' email.
- "Non-SFU" = account owner is not a member of the SFU community.

In general: if the email was transferred under a Records Retention Schedule and Disposal Authority (RRSDA), use "University"; if they were transferred under Donation Agreement (e.g. with the account owner's estate) use "Campus community" or "Non-SFU" as appropriate.

### Accession type

### Type of material

### Acquisition method

#### Transfer method

### Packaged with SFU MoveIt?

### Status

## 6.2 Archival units tab
Level of description
Reference code
Unit title

## 6.3 RRSDAs tab
RRSDA number

## 6.4 Sources tab
Source: Creator
Source: Donor
Provenance note
Custodial history note

## 6.5 Materials tab

Dates
Content types
Scope and content
Languages

## 6.6 Storage tab
AIPs

## 6.7 Management tab
Donor negotiated restrictions?
Known sensitive personal / confidential information?
Note on access
Donor copyright
Note on use and copyright
Note on appraisal
Conservation actions required?
Note on preservation
Documentation

## 6.8 Workflow tab

Staff responsible
Date accession record started
Transfer of custody (physical)
Transfer of control (legal)
Other events
Dipsoal project
Processing project

###### Status: under development

###### Last updated: Jul 22, 2020
