# Bank-Loan-Origination-System
The Corporate Banking Loan Origination System (CBLOS) is a robust web-based solution designed for 
corporate banking sectors to streamline the loan application, evaluation, and disbursement process. The 
system caters to complex workflows required for high-value loans for businesses, providing functionalities 
such as credit evaluation, risk assessment, document management, and disbursement tracking.
The application follows MVC architecture and is built to be compatible with both Java (Spring MVC) and 
.NET (ASP.NET Core MVC) frameworks.
2. Core Modules Description
2.1 Loan Application Management
Manages the end-to-end process of capturing corporate loan applications, loan type selection, 
and tracking of application status.
2.2 Credit Evaluation and Risk Assessment
Assesses the creditworthiness of corporate borrowers and calculates the associated risk scores 
using predefined algorithms and external credit bureaus.
2.3 Document Management
Facilitates document uploads, storage, and validation required for loan processing, such as 
financial statements, collateral proof, and tax records.
2.4 Loan Approval Workflow
Implements a multi-level loan approval process based on predefined business rules and 
authorization hierarchies.
2.5 Disbursement Tracking and Reporting
Tracks loan disbursement schedules, repayment terms, and generates periodic reports for 
compliance and operational insights.
3. Module-Level Design
3.1 Loan Application Management Module
Purpose: Enables corporate clients to initiate and track loan applications.
• Controller:
o LoanApplicationController
▪ submitApplication()
▪ trackApplicationStatus()
▪ viewApplicationDetails()
• Service:
o LoanApplicationService
▪ Validates and saves loan applications to the database.
▪ Retrieves application status and details.
• Model:
o LoanApplication Entity
▪ Attributes:
▪ applicationId (PK)
▪ companyName
▪ loanType
▪ loanAmount
▪ status
▪ submissionDate
3.2 Credit Evaluation and Risk Assessment Module
Purpose: Analyzes borrower creditworthiness and assigns a risk score.
• Controller:
o CreditEvaluationController
▪ evaluateCredit()
▪ getRiskScore()
• Service:
o CreditEvaluationService
▪ Integrates with external credit scoring systems.
▪ Calculates internal risk scores based on financial metrics.
• Model:
o CreditEvaluation Entity
▪ Attributes:
▪ evaluationId (PK)
▪ applicationId (FK)
▪ riskScore
▪ creditScore
▪ evaluationDate
3.3 Document Management Module
Purpose: Handles the upload, validation, and management of documents required for loan processing.
• Controller:
o DocumentController
▪ uploadDocument()
▪ validateDocument()
▪ viewUploadedDocuments()
• Service:
o DocumentService
▪ Manages document uploads and metadata.
▪ Validates documents for format and content.
• Model:
o Document Entity
▪ Attributes:
▪ documentId (PK)
▪ applicationId (FK)
▪ documentType
▪ filePath
▪ uploadDate
▪ isValid
3.4 Loan Approval Workflow Module
Purpose: Automates multi-level approval workflows for corporate loan applications.
• Controller:
o ApprovalController
▪ approveLoan()
▪ rejectLoan()
▪ viewApprovalStatus()
• Service:
o ApprovalService
▪ Enforces business rules for loan approvals.
▪ Tracks approval levels and statuses.
• Model:
o Approval Entity
▪ Attributes:
▪ approvalId (PK)
▪ applicationId (FK)
▪ approverId
▪ approvalLevel
▪ approvalStatus
▪ comments
▪ approvalDate
3.5 Disbursement Tracking and Reporting Module
Purpose: Tracks loan disbursements and generates operational and compliance reports.
• Controller:
o DisbursementController
▪ trackDisbursement()
▪ generateDisbursementReport()
• Service:
o DisbursementService
▪ Manages disbursement schedules.
▪ Generates reports for monitoring and compliance.
• Model:
o Disbursement Entity
▪ Attributes:
▪ disbursementId (PK)
▪ applicationId (FK)
▪ disbursedAmount
▪ disbursementDate
▪ repaymentSchedule
