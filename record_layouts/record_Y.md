| Rec. Type | Field No. | Field Name | Field Type | Position Start | Length | Required | Description | Comments |
| --- | :---: | --- | --- | :---: | :---: | :---: | --- | --- |
| Y | 1 | **RECORD TYPE** | PIC X(1) | 1 | 1 | X | Always 'Y'.| |
| Y | 2 | **RECORD SUBTYPE** | PIC X(1) | 2 | 1 | X | Valid values are (A, U, C)<br>A = Add ERO to Refundo's System<br>U = Update or Add ERO to Refundo's System<br> | Change: 8/24/2015 - Removing 'C'onfirmation subtype since reverse enrollment is being deconstructed |
