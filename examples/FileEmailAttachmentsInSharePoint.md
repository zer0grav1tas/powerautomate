# Save Attachments in SharePoint

## Get new email attachments and copy to SharePoint Document Library

This PowerAutomate flow will trigger when a message is received into a mailbox. The attachment will be read and copied to a SharePoint document library.

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
- **Action:** Create file
- **Site Address:** URL to Site Collection  
- **Folder Path:** `/Shared Documents`
- **File Name:** `outputs('Get_Attachment')?['body/name']`
- **File Content:** `outputs('Get_Attachment')?['body/contentBytes']`