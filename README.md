# Integration to Refundo Dashboard

`Version 3.0`

## Data Flow

1. The transmitters send a file with a letter extention (.Y, .B, etc), Refundo will respond with a numeric extention (.2, .3, etc)
1. The first step is the enrollment of companies
  * Send Y record
  * Receive confirmation
1. Then proceed to send bank applications
  * Send B record
  * Send MEF files
  * Receive confirmation
1. When the checks and fees are ready, Refundo will send records to notify

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

Type of transaction | Convention
--- | ---
 | **File name / batch id**
 **XX to Refundo** | 
MEF Returns | XXR_nnnnnnnnn.yyMMddHHmmss.mef
RT application (Can contain both RT and NOW). B record | XXR_nnnnnnnnn.yyMMddHHmmss.b


## Company Enrollment (.Y Record)

1. Record Layouts
  * [Open Y Record layouts](record_layouts/record_Y.md)
1. Test Cases
  * [Download test cases](test_cases/test_Y-001.Y)


## Bank applications (.B Record)

1. Algorithm for generating account numbers
  * [Pseudo Code](record_Y.md)
  * Libraries
    * [CPP](libraries/library.txt)
    * [C#](libraries/library.txt)
    * [VB](libraries/library.txt)
    * [PHP](libraries/library.txt)
1. Record Layouts

## Check information record (.6 Record)

## Rejection Codes

## Changes

* [Changes](changelog.md)

