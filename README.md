# Automated AWS Receipt Processing System

## ☁️ Overview of Project

This project focuses on automating receipt processing using AWS services.  
Instead of manually handling receipts—which can be time-consuming, error-prone, and difficult to scale—this system extracts structured data from receipts and stores it efficiently for record-keeping and auditing.

The architecture consists of:

- **Storage Layer**: Amazon S3 stores receipt images and PDFs.  
- **Processing Layer**: Amazon Textract extracts text from receipts using AI-powered OCR.  
- **Database Layer**: DynamoDB stores the extracted data in a structured format.  
- **Notification System**: Amazon SES sends email alerts with receipt details.  
- **Compute Layer**: AWS Lambda automates the workflow by processing the receipts in real-time.

---

## 🛠 Services Used

- **Amazon S3** – Stores uploaded receipt images and PDFs. _(Storage)_  
- **Amazon Textract** – Extracts text and structured data from scanned receipts. _(AI/ML)_  
- **Amazon DynamoDB** – Stores extracted receipt data in a structured format. _(Database)_  
- **Amazon SES** – Sends email notifications with extracted receipt details. _(Messaging)_  
- **AWS Lambda** – Automates the processing workflow for real-time execution. _(Compute)_  
- **IAM Roles & Policies** – Ensures secure access between services. _(Security)_

---

## ✍️ Architectural Diagram

![AWS Receipts Diagram](https://github.com/user-attachments/assets/3681ac55-5528-4ce9-a654-d865a8fe075d)

---

## ⚙️ Estimated Time & Cost

- **Time**: ~2 hours  
- **Cost**: Free (AWS Free Tier Eligible)

---

## 👩‍💻 Steps to be Performed

1. **Storage and Database Setup**:  
   Create an S3 bucket and DynamoDB table.

2. **Notification Setup**:  
   Configure Amazon SES for email alerts.

3. **Processing Setup**:  
   Create a Lambda function to handle receipt processing.

4. **Integration and Testing**:  
   Tie everything together and run tests to validate.

---

## 🗑️ Clean-Up (so that no charges are incurred due to prolonged use of AWS resources)

1. **Delete S3 Bucket**  
   Remove all uploaded receipt files, then delete the bucket.

2. **Stop Textract Processing**  
   Ensure no further API calls are made to avoid extra costs.

3. **Delete DynamoDB Table**  
   Remove stored receipt data, then delete the table.

4. **Disable SES Notifications**  
   Remove verified email addresses if SES was configured.

5. **Remove IAM Roles and Policies**  
   Delete the IAM role created for the Lambda function.
