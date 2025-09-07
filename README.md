# Serverless-Attendance-System-Using-Face-Recognition
Overview
A modern, cloud-powered Face Recognition Attendance System built using AWS Lambda, Amazon Rekognition, DynamoDB, and S3. This serverless web app allows seamless, accurate employee attendance marking and provides real-time analytics for admins.
Key Features:
Face recognition-based marking with >90% accuracy
Instant dashboard analytics (daily, weekly summary)
Secure, scalable, and cost-effective AWS architecture

Table of Contents
Architecture
Features
Setup & Deployment
Usage
Tech Stack
Project Structure

Architecture
Frontend: Static website hosted in Amazon S3 (HTML/JS/CSS)
Backend: AWS Lambda functions (Python), integrated via API Gateway/Lambda Function URL
Face Processing: Amazon Rekognition Collection
Data Storage: DynamoDB for attendance records, S3 for image uploads

Features
Fast & Accurate Attendance: Attendance is marked automatically for faces matching >90% similarity.
Admin Dashboard: Real-time view of daily and weekly attendance, total present employees, advanced analytics.
Robust Security: All user images are base64-encoded and securely transmitted.
Easy Integration: RESTful APIs with correct CORS headers; simple deployment; extensible for other business scenarios.

Setup & Deployment
Clone the repository

bash
git clone https://github.com/YOUR_USERNAME/face-attendance-aws.git
cd face-attendance-aws

Frontend
Place static files (index.html, index.js, style.css) inside /frontend
Host the frontend on Amazon S3 (static website hosting enabled)

Backend
Write Lambda functions in /backend/lambda_function.py
Deploy Lambda function and set up API Gateway or Lambda Function URL
Connect Lambda to DynamoDB table and Rekognition collection

AWS Resources
Create DynamoDB table (e.g., EmployeeAttendance)
Create an S3 bucket for image uploads
Create a Rekognition collection (e.g., employee_faces)

Configuration
Update config variables in frontend (apiUrl, etc.)

Usage
Employee: Scan face via browser, attendance is marked automatically.
Admin: Login to dashboard, view daily/weekly summaries, export data.

Tech Stack
AWS Lambda (Python)
Amazon Rekognition
DynamoDB
S3 (Static web hosting, image storage)
HTML, CSS, JavaScript (frontend)
