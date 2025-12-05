# 📌 UiPath Loan Application Automation (REFramework)

This project is an end-to-end Loan Application Automation built using UiPath Studio and the Robotic Enterprise Framework (REFramework).
It automates the process of validating customer loan application data, performing business rule checks, updating records, and generating results with error handling and transaction management.


## 🚀 1. Project Overview

The automation processes loan applications from an input data source (Excel/CSV).
For every loan record, it:

- Reads customer details
- Validates mandatory fields
- Applies business rules (age, salary, credit score, loan amount)
- Decides whether the loan is Approved or Rejected
- Logs results
- Updates the output file
- Handles exceptions and retries using REFramework

This project demonstrates full RPA development lifecycle, including:
Input validation, exception handling, reusable components, and clean architecture.



## 🧠 2. Technologies & Tools Used

| Tool                                 | Purpose                                |
| ------------------------------------ | -------------------------------------- |
| UiPath Studio                        | Workflow development                   |
| UiPath REFramework                   | Transaction handling + Retry + Logging |
| Excel Application Scope              | Input/output data                      |
| Orchestrator Assets                  | Config & credentials                   |
| Log Message                          | Logging and debugging                  |
| Exception Handling                   | Business/application exception flows   |



##  3. Project Architecture (REFramework)

The solution follows REFramework standards:

### Initialization (Init State)

- Reads Config.xlsx
- Loads input loan data
- Prepares system environment

### Get Transaction Data

- Fetches the next loan application row

### Process Transaction

- Validates input fields
- Applies business rules
- Generates loan decision
- Updates output sheet

### End Process

- Close applications
- Final logging



## 📂 4. Folder Structure

```
UiPathLoanApplicationAutomation/
│── Framework/               # REFramework internal workflows
│── BusinessRules/           # Custom business validation workflows
│── Data/                    # Input and output Excel files
│── Config/                  # Config.xlsx, Orchestrator settings
│── Main.xaml                # Entry point
│── project.json
│── README.md
```

## 5. Loan Validation Rules Applied

The automation validates:

- Age ≥ 18
- Monthly Salary ≥ Threshold
- Credit Score ≥ Minimum Score
- Loan Amount ≤ 3× Annual Salary
- Mandatory fields not empty
- Format validations (numbers, strings, dates)

Business rules can be easily modified in the BusinessRules folder.

## 📋 6. How to Run the Project

### ✔️ Prerequisites

- UiPath Studio installed (Community or Enterprise)
- Excel file with loan applications placed in `/Data` folder
- Latest UiPath dependencies restored

### ✔️ Steps to Run

1. Clone the repository

   ```bash
   git clone https://github.com/Abhishek9849/UiPathLoanApplicationAutomation
   ```
2. Open UiPath Studio
3. Click Open Project → select the project folder
4. Update file paths in Config.xlsx (if needed)
5. Run Main.xaml



## 🛠️ 7. Features Implemented

✔️ REFramework structure
✔️ End-to-end input to output automation
✔️ Config-driven architecture
✔️ Retry mechanism for failures
✔️ Robust exception handling
✔️ Clear logging for debugging
✔️ Easily scalable for real enterprise use



## 📈 8. Sample Input/Output

### Input (Loan Applications)

| Name | Age | Salary | CreditScore | LoanAmount |
| ---- | --- | ------ | ----------- | ---------- |
| John | 29  | 40000  | 720         | 200000     |

### Output (Results)

| Name | Result   | Reason             |
| ---- | -------  |--------------------|
| John | Approved | Meets all criteria |



## 💡 9. Future Enhancements

- Connect to Orchestrator Queue
- Integrate with API for live credit check
- Generate PDF summary report
- Send approval/rejection emails automatically



## 👤 10. Author

Dandetikar Abhishek
Certified UiPath RPA Developer
GitHub: [https://github.com/Abhishek9849](https://github.com/Abhishek9849)

