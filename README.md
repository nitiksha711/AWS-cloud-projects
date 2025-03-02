**AWS Cloud Project - S3, Lambda, and API Gateway**  
📌 Project Overview
This project demonstrates the integration of AWS services, including S3 (Simple Storage Service), Lambda (serverless computing), and API Gateway (REST API interface). It allows users to upload files to an S3 bucket and trigger a Lambda function via an API Gateway endpoint.  

🚀 Features
✅ Upload files to S3 bucket  
✅ Trigger AWS Lambda function on file upload  
✅ Expose API using API Gateway  
✅ Serverless execution with AWS Lambda  

🛠️ Setup Instructions
1️⃣ Prerequisites
- AWS Account  
- AWS CLI installed and configured (`aws configure`)  
- Node.js or Python installed (for Lambda function)  
- Git installed  

2️⃣ Setting Up S3 Bucket
1. Open AWS Console and navigate to S3 service.  
2. Click "Create Bucket" and give it a unique name (e.g., `my-cloud-project-bucket`).  
3. Uncheck "Block all public access" (if public access is needed).  
4. Click Create bucket.  

3️⃣ Creating AWS Lambda Function
1. Navigate to AWS Lambda service.  
2. Click "Create function" → "Author from scratch".  
3. Give it a name (e.g., `myLambdaFunction`).  
4. Select a runtime (Python 3.x or Node.js).  
5. Under Function code, add a script to handle S3 events.  
6. Choose Execution role → Create a new role with basic Lambda permissions.  
7. Click Create function.  

4️⃣ Deploying API Gateway
1. Go to API Gateway in AWS Console.  
2. Click Create API → REST API.  
3. Name it (e.g., `MyFirstAPI`).  
4. Create a resource (e.g., `/upload`).  
5. Add a method (POST) and link it to your Lambda function.  
6. Deploy the API by creating a new stage (e.g., `prod`).  

---

🚀 Deployment
1. Push your code to GitHub:  
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/nitiksha711/AWS-cloud-projects.git
   git push -u origin main
   ```
2. In AWS Lambda, upload your function code or use the inline editor.  
3. Deploy your API Gateway to generate a public URL.  
4. Test API using Postman or cURL.  

---

⚠️ Challenges Faced
- IAM Role Permissions: Required fine-tuning for Lambda to access S3.  
- CORS Issues: Had to enable CORS in API Gateway for external access.  
- API Gateway Deployment: Needed to manually deploy after changes.  

---

📌 Future Improvements
- Add authentication using AWS Cognito.  
- Improve security with bucket policies and IAM roles.  
- Automate deployment using Terraform or AWS CDK.  
