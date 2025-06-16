# Junior Power Automate Engineer - Skills Test

### Task 1: Invoice Processing Automation (Fundamentals Test)
**Platform:** Power Automate Cloud

**Scenario:** Create an automated workflow that processes incoming invoices from email attachments and routes them for approval.

**Requirements:**
- Monitor shared mailbox for emails with PDF attachments
- Extract invoice details (amount, vendor, date, invoice number)
- Validate data format and completeness
- Route to appropriate approver based on amount thresholds
- Store approved invoices in SharePoint with proper naming convention
- Send confirmation emails to vendors
- Handle basic error scenarios

**What We're Testing:**
- Understanding of triggers and conditions
- Data extraction and manipulation skills
- Basic approval workflow logic
- Error handling fundamentals
- Email and SharePoint integration

---

### Task 2: Data Validation and Cleansing Challenge
**Platform:** Power Automate Cloud

**Scenario:** Build a flow that validates and cleanses customer data from multiple sources before updating the CRM system.

**Given Data Issues:**
- Inconsistent phone number formats
- Mixed case names and addresses
- Missing required fields
- Duplicate entries across sources
- Invalid email addresses

**Requirements:**
- Standardize phone numbers to (XXX) XXX-XXXX format
- Proper case conversion for names
- Email validation
- Flag incomplete records for manual review
- Identify potential duplicates using fuzzy matching
- Update CRM only with clean, validated data
- Generate data quality report

**Technical Skills Tested:**
- String manipulation functions
- Data validation logic
- Conditional logic implementation
- Array processing
- Compose and variable usage

---

### Task 3: Power Automate Desktop - Excel Automation
**Platform:** Power Automate Desktop

**Scenario:** Automate the monthly consolidation of financial reports from 5 different Excel workbooks into a master summary report.

**Requirements:**
- Open multiple Excel files from a specified folder
- Extract data from specific sheets and ranges
- Perform basic calculations (sum, average, variance)
- Handle missing files gracefully
- Create formatted summary report
- Save with timestamp in filename
- Send completion notification

**Advanced Elements:**
- Use loops to process variable numbers of files
- Implement basic error recovery (file not found, format issues)
- Dynamic range selection based on data size
- Basic Excel formatting (headers, borders, number formatting)

**What We're Evaluating:**
- Desktop automation fundamentals
- File system operations
- Excel manipulation skills
- Loop and conditional logic
- Error handling approach

---

### Task 4: REST API Integration and Data Processing
**Platform:** Power Automate Cloud

**Scenario:** Integrate with a fictional bank API to retrieve daily transaction data and process it for reporting.

**Mock API Details:**
- Endpoint: GET /api/transactions/{date}
- Authentication: API key in header
- Response: JSON array of transactions
- Rate limit: 10 requests per minute

**Requirements:**
- Authenticate with API using provided credentials
- Retrieve transactions for current date
- Parse JSON response
- Filter transactions by type and amount
- Calculate daily totals by category
- Store results in SharePoint list
- Handle API errors and rate limiting

**Skills Assessment:**
- HTTP action configuration
- JSON parsing and manipulation
- Authentication handling
- Data transformation
- Error response handling

---

### Task 5: Problem-Solving Scenario (No Coding)
**Format:** Discussion

**Scenario:** "A department manager complains that their monthly budget reconciliation process takes 2 full days. They currently download reports from 3 different systems, manually copy data into Excel, perform calculations, and email results to 15 stakeholders."

**Questions:**
1. "Walk me through how you would analyze this process for automation opportunities"
2. "What questions would you ask the manager to understand their requirements?"
3. "What potential challenges do you see in automating this process?"
4. "How would you prioritize which parts to automate first?"
5. "What would success look like for this automation project?"

**Evaluation Focus:**
- Business process analysis skills
- Stakeholder communication approach
- Risk identification
- Project planning thinking
- Change management awareness

---

### Task 6: Debugging and Troubleshooting Challenge
**Platform:** Power Automate Cloud (Pre-built broken flow)

**Scenario:** Fix a broken approval workflow that has multiple issues preventing it from running correctly.

**Pre-built Flow Issues:**
- Trigger configured incorrectly
- Missing required fields in actions
- Incorrect condition logic
- Approval timeout not set
- Email template has syntax errors
- SharePoint list updates failing

**Requirements:**
- Identify all issues in the flow
- Explain what each problem would cause
- Fix the issues to make the flow functional
- Suggest improvements for better reliability
- Demonstrate testing approach

**Skills Tested:**
- Debugging methodology
- Understanding of flow mechanics
- Problem identification skills
- Testing and validation approach