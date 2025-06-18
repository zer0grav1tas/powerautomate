# Save Attachments in SharePoint and Create List Item

## Get new email attachments and copy to SharePoint Document Library, read contents and populate SharePoint List.

This PowerAutomate flow will trigger when a message is received into a mailbox. The attached invoice will be read and copied to a SharePoint document library. The data in the invoice will be read and entered in to a SharePoint List.

This process requires an Encodian API key as it uses [PDF - Apply OCR (All)](https://support.encodian.com/hc/en-gb/articles/14286080106908-PDF-Apply-OCR-AI)

You can get an Encodian API key - 30 day free trial (No card) [Get an API Key](https://support.encodian.com/hc/en-gb/articles/360034587474-Get-an-API-Key-30-Day-Trial-Subscription)

This process requires a SharePoint List with the following columns:
- InvoiceDate
- InvoiceTotal
- InvoiceID

The example PDF contains a simple data sample:
INVOICE - BlueWaterKitchens 
Amount: £400 
Date: 15/6/2025 
Number: 123456 

**Trigger:** When a new email arrives  
**To:** Email address to monitor  
**Include Attachments:** Yes

**Condition:** Foreach  
**Select an output from previous steps:** Attachments

### In ForEach Loop

**Action:** Get Attachment  
**Message Id:** `triggerOutputs()?['body/id']`  
**Attachment Id:** `items('Foreach')?['id']`

**Condition:** `AND outputs('Get_Attachment')?['body/name'] contains .pdf`

**True:**
- **Action:** AI - Process Invoice
- **Parameters:** `outputs('Get_Attachment')?['body/contentBytes']`

- **Action:** Create Item (SharePoint Action)
- **Site Address:** URL of Site Collection
- **List Name:** Name of List
- **Title:** `outputs('Get_Attachment')?['body/name']`
- **InvoiceDate:** `json(outputs('AI_-_Process_Invoice')?['body/result'])['InvoiceDate']`
- **InvoiceTotal:** `json(outputs('AI_-_Process_Invoice')?['body/result'])['InvoiceTotal']`
- **InvoiceID:** `json(outputs('AI_-_Process_Invoice')?['body/result'])['InvoiceId']`

- **Action:** Create file (SharePoint Action)
- **Site Address:** URL of Site Collection  
- **Folder Path:** `/Shared Documents`
- **File Name:** `outputs('Get_Attachment')?['body/name']`
- **File Content:** `outputs('Get_Attachment')?['body/contentBytes']`