# Integration to Refundo Dashboard

## Data Flow

1. Always the transmitters send a file with letter extention (.Y, .B, etc), Refundo will respond with a numeric extention (.2, .3, etc)
1. First step is enrollment of companies
  * Send Y record
  * Recieve confirmation
1. Then you proceed to send bank applications
  * Send B record
  * Send MEF files
  * Receive confirmation

## Connection

We provide connection with two methods
* FTP
* API (RestFul)

### FTP connection

First, we provide a user account for our staging server. By defualt there are 3 folders:

* IN
  * From transmitter to Refundo
* OUT
  * From Refundo to transmitter
* HISTORY
  * All files

### File Naming Convention

This table describes the file naming conventions agreed by the Transmitter and the bank.

| Type of transaction | Convention |
|  | File name / batch id |
| **XX to Refundo** |  |
| --- | --- |
| MEF Returns | XXR_nnnnnnnnn.yyMMddHHmmss.mef |

## Company Enrollment (.Y Record)

1. Record Layouts
  * [Open Y Record layouts](../blob/master/record_Y.md)
1. Test Cases
  * [Download test cases](../blob/master/test_cases/test_Y-001.Y)


## Bank applications (.B Record)

## Check information record (.6 Record)

## Rejection Codes

## Changes

* Changes](../blob/master/changelog.md)

