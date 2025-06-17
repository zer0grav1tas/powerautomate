# Senior Power Automate Engineer - SKills Test

### Task 1: Complex Financial Data Integration & Processing
**Platform:** Power Automate Cloud + Power Automate Desktop

**Scenario:** Design and implement a solution that processes daily bank statement files from multiple financial institutions, validates transactions, identifies discrepancies, and updates multiple downstream systems.

**Requirements:**
- Handle CSV, Excel, and PDF bank statements from 5+ different banks
- Implement data validation rules for transaction amounts, dates, and reference numbers
- Detect duplicate transactions across different sources
- Flag transactions exceeding $50,000 for manual review
- Update SharePoint lists, SQL databases, and send notifications to relevant teams
- Implement comprehensive error handling and retry mechanisms
- Ensure all sensitive data is properly handled according to financial regulations

**Evaluation Criteria:**
- Architecture design and flow organization
- Error handling sophistication
- Data validation logic
- Security implementation
- Performance optimization strategies
- Documentation quality

---

### Task 2: Automated Financial Reporting with Dynamic Approvals
**Platform:** Power Automate Cloud

**Scenario:** Create an intelligent approval workflow for expense reports that dynamically routes based on amount, department, and expense type, with integration to financial systems.

**Requirements:**
- Dynamic approval routing (amounts >$1000 require CFO approval, department heads for $500-$1000, etc.)
- Integration with SharePoint, Teams, and external ERP system
- Automatic expense categorization using AI Builder or custom logic
- SLA tracking with escalation procedures
- Audit trail maintenance
- Budget validation against department allocations
- Multi-currency support

**Technical Challenges:**
- Implement parallel approval branches for complex scenarios
- Handle approval delegation during employee absences
- Create custom connector if needed for ERP integration
- Implement caching mechanisms for frequently accessed data

---

### Task 3: Power Automate Desktop - Legacy System Integration
**Platform:** Power Automate Desktop

**Scenario:** Automate the extraction of data from a legacy mainframe terminal application and input it into a modern web-based financial system.

**Requirements:**
- Screen scraping from terminal application with dynamic data positions
- Data transformation and validation
- Web automation for data entry into modern system
- Handle network timeouts and application crashes gracefully
- Implement logging and monitoring
- Process 500+ records per run with error recovery
- Schedule coordination with cloud flows

**Advanced Elements:**
- Use OCR for certain data elements that aren't text-selectable
- Implement intelligent wait strategies for slow legacy systems
- Create dynamic selectors that adapt to interface changes
- Handle popup windows and unexpected dialog boxes

---

### Task 4: Enterprise Architecture & Governance Challenge
**Format:** Design Discussion + Documentation

**Scenario:** Design a Power Platform governance framework for our finance organization with 200+ users across 15 departments.

**Requirements:**
- Environment strategy (dev, test, prod separation)
- Solution lifecycle management
- Security and compliance framework
- Monitoring and analytics strategy
- Connector usage policies
- Data loss prevention implementation
- Business value measurement framework

**Discussion Points:**
- How would you handle solution deployment across environments?
- What monitoring strategies would you implement?
- How would you ensure compliance with financial regulations?
- How would you manage connector security and data sovereignty?

---

### Task 5: Performance Optimization & Troubleshooting
**Platform:** Mixed

**Scenario:** You inherit a slow-performing automated reconciliation process that times out frequently and has poor error reporting.

**Given Information:**
- Current flow processes 10,000 transactions daily
- Takes 6+ hours to complete (should be 2 hours)
- Fails 30% of the time with unclear error messages
- Uses 47 HTTP requests per transaction
- No retry logic implemented
- Users complain about lack of progress visibility

**Requirements:**
- Identify performance bottlenecks and propose solutions
- Redesign for optimal performance and reliability
- Implement proper error handling and logging
- Add progress tracking and user notifications
- Ensure solution can scale to 25,000 transactions daily

---

### Task 6: Real-Time Financial Monitoring System
**Platform:** Power Automate Cloud + Custom Connectors

**Scenario:** Create a real-time monitoring system for suspicious financial transactions that integrates with multiple data sources and compliance systems.

**Requirements:**
- Monitor incoming transactions in real-time from multiple APIs
- Implement complex business rules for fraud detection
- Integration with external compliance databases
- Real-time alerting via Teams, email, and SMS
- Dashboard updates using Power BI
- Maintain detailed audit logs
- Handle high-volume transaction processing (1000+ per minute)

**Advanced Features:**
- Implement custom connectors for proprietary systems
- Use AI Builder for anomaly detection
- Create adaptive thresholds based on historical patterns
- Implement geolocation validation for transactions