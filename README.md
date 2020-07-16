# SQLDEV300_HW1

## 1. Ingress (Import)
Create a PowerShell script or scripts creating appropriate tables, and importing the information

- King County information should be imported daily except

- WA and OR data should be imported on weekends

![Image of Ingress](/images/scheduledtasks.png)
![Image of Ingress](/images/wa and or data.png)

- empty table 'Uploads' with the columns: "SourceFile, DestTable, UploadStartTime, UploadEndTime, Status"
![Image of Ingress](/images/empty table.png)
Create another PowerShell script to import (and create necessary tables) for the

- US Population data

As an upload begins, the respective row in Uploads table should have Status='Started'. After the upload, it should be 'Finished' or 'Failed'. Update other fields as appropriate.

![Image of Ingress](/images/testing.png)


## 2. Testing
Provide sanity testing for the US population data

### test total record count is within reason. Explain your choice in comments.

### test the total 'US population' is within range. Explain your choice in comments.

### test a specific county population is within range.  Explain your choice in comments.

Provide sanity testing for the US population data

### Provide 3 tests and execute them. Explain your choice in comments.
`Please see population.ps1`
Discuss what kind of incorrect or corrupt files your tests did and did not detect

![Image of Ingress](/images/tesing.png)

## 3. Reporting
Execute a query displaying on the screen the total number of H-19 cases in King and Pierce counties yesterday (whenever yesterday is)

![Image of Ingress](/images/reporting.png)

## 4. Maintenance
### Describe in a paragraph an automated maintenance you could implement for the database, and why.

`Generate daily and weekly report of import, export and report error.`

## 5. Egress (Export)
### export an XML file with a limited output of the reporting in #3:

Format is up to you but - for example:

<data><county>King</county><data>1/1/2020</date><cases>999</cases></data>

At this point, you can use a temporary table if you wish and the AS XML, or hand-craft the XML . Justify your choice.

![Image of King Count XML](/images/king_xml.png)
![Image of Pierce county XML](/images/pierce_xml.png)

- Describe in a paragraph another automated export task you could implement for the database, and why.

` Generate daily and weekly report that shows the county cases in greater details.
 - total cases, heat map with fastest case growth
 - import/export error`
