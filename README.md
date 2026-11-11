# AWS-S3-Storage-and-Security

<p align="left">
  <img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="AWS" />
  <img src="https://img.shields.io/badge/Amazon%20S3-569A31?style=for-the-badge&logo=amazon-s3&logoColor=white" alt="Amazon S3" />
  <img src="https://img.shields.io/badge/AWS%20IAM-DD344C?style=for-the-badge&logo=aws-iam&logoColor=white" alt="AWS IAM" />
  <img src="https://img.shields.io/badge/Cybersecurity-000000?style=for-the-badge&logo=shield&logoColor=white" alt="Cybersecurity" />
</p>

## Table of Contents

- [1. Introduction](#1-introduction)
- [2. Project Overview](#2-project-overview)
- [3. Objectives](#3-objectives)
- [6. Architecture](#6-architecture)
- [7. Tools and Technologies](#7-tools-and-technologies)
- [8. Project Implementation](#8-project-implementation)
  - [AWS Console Sign-In & Authentication](#sign-in-----go-to-the-official-aws-management-console-entry-page-httpsconsoleawsamazoncom-click-on-sign-in-to-console-to-open-the-login-page)
  - [Bucket Creation & Security Setup](#create-bucket-----click-on-create-bucket-to-start-setting-up-a-new-s3-storage-bucket)
  - [File Uploads & Object Management](#upload-----use-the-upload-interface-to-drag-and-drop-filesfolders-or-click-add-files-to-upload-data-to-your-s3-bucket)
  - [Static Website Hosting & Versioning](#index-html----uploading-an-indexhtml-file-to-the-s3-bucket-pratiksha-27-for-static-website-hosting)
  - [Access Security Verification & Cleanup](#view-the-xml-error-response-showing-accessdenied-when-attempting-to-access-a-private-s3-object-url-without-public-permissions)
- [9. Security Configurations](#9-security-configurations)
- [10. Future Enhancements](#10-future-enhancements)
- [11. What I Learned](#11-what-i-learned)
- [12. Disclaimer](#12-disclaimer)

---



## 1. Introduction

Amazon Simple Storage Service (Amazon S3) is an object storage service provided by Amazon Web Services (AWS). It allows users to store, retrieve, and manage data from anywhere through the internet.

This project demonstrates the practical implementation of Amazon S3 by creating a storage bucket, uploading files, managing objects, and applying security configurations to protect stored data.

## 2. Project Overview

The purpose of this project is to understand cloud-based storage and learn how to manage data using Amazon S3.

The implementation includes bucket creation, file uploads, object management, versioning, encryption, and access permissions. It also demonstrates how to protect cloud data using AWS security features.

## 3. Objectives

The main objectives of this project are:
1. Understand Amazon S3 and cloud storage.
2.  Create and configure an S3 bucket.
3.  Upload, download, and manage objects.
4. Understand bucket permissions and access control.
5. Enable bucket versioning.
6. Configure server-side encryption.
7. Apply the principle of least privilege.
8. Understand secure cloud storage practices.

   ## 6. Architecture

**Basic S3 Storage Architecture:**

User → AWS Management Console → Amazon S3 → S3 Bucket → Stored Objects

## 7. Tools and Technologies

| Tool | Purpose |
|---|---|
| Amazon Web Services | Cloud platform |
| Amazon S3 | Object storage |
| AWS Management Console | Resource management |
| IAM | Identity and access management |
| AWS KMS / S3 encryption | Data protection |
| Web Browser | Accessing AWS Console |

## 8. Project Implementation

**SIGN IN :--->** *Go to the official AWS Management Console entry page ([https://console.aws.amazon.com](https://console.aws.amazon.com)).
Click on Sign in to console to open the login page.*

<img width="1366" height="546" alt="Screenshot 2026-10-18 194316" src="https://github.com/user-attachments/assets/cfea11d7-a439-49fe-93bf-c55b1f3db4b5" />

**ACCESS YOUR ACCOUNT BY USER TYPE :--->**  *Select "Root user", enter your email address, and click "Next" to proceed.*


<img width="1346" height="634" alt="Screenshot 2026-10-18 194707" src="https://github.com/user-attachments/assets/428cc61b-d82e-45a2-8629-b82a57b9f40a" />

**ADDITIONAL VERIFICATION :--->** *Enter the 6-digit MFA code from your authenticator app and click Sign in.*


<img width="1346" height="631" alt="Screenshot 2026-10-18 194829" src="https://github.com/user-attachments/assets/fc64a665-df67-4290-88d0-23b775d733ab" />

**CONSOLE HOME :--->**  *Successfully authenticated and redirected to the AWS Management Console Home dashboard.*


<img width="1350" height="597" alt="Screenshot 2026-10-18 194942" src="https://github.com/user-attachments/assets/f394dab4-a585-448a-9dfd-55bf22e2b8f0" />


**SEARCH SERVICES :--->** *Search for S3 in the top search bar and click on the S3 service.*


<img width="1349" height="601" alt="Screenshot 2026-10-18 195016" src="https://github.com/user-attachments/assets/8e35b6b5-cdd4-4d06-828f-9da83fcee799" />


**CREATE BUCKET :--->** *Click on **Create bucket** to start setting up a new S3 storage bucket.*
<img width="1366" height="604" alt="Screenshot 2026-10-18 195102" src="https://github.com/user-attachments/assets/b00d9d13-61d4-4f46-95e4-f7b0c8487fc5" />

 **Configure General parameters for the S3 bucket, including AWS Region, Bucket type, and unique Bucket name.**

<img width="1366" height="595" alt="Screenshot 2026-10-18 200207" src="https://github.com/user-attachments/assets/86ae5012-b2bc-43f3-aaf3-2dd35f567053" />

**GENERAL CONFIGURATION :--->** *Enter a unique name for the S3 bucket in the Bucket name field (e.g., pratiksha).*

<img width="1366" height="687" alt="Screenshot 2026-10-18 200435" src="https://github.com/user-attachments/assets/2ef1c44c-2635-424e-b48d-35c9a7177aef" />

**OBJECTT OWNERSHIP :--->** *Keep ACLs disabled (recommended) and ensure Block all public access is enabled for security.*

<img width="1366" height="598" alt="Screenshot 2026-10-18 200539" src="https://github.com/user-attachments/assets/236a29cc-2e3a-4760-bf4a-0a5ebabd8fc0" />


**BLOCK PUBIC ACCESS :--->** *Review and acknowledge the warning when unchecking "Block all public access" for specific use cases (such as static website hosting).*

<img width="1366" height="599" alt="10" src="https://github.com/user-attachments/assets/28c48c3c-b8bc-4ea5-a9c3-02d7a26a80be" />


**BUCKET VERSIONING :--->** *Enable Bucket Versioning to preserve, retrieve, and restore different variants of stored objects, and optionally add resource tags.*

<img width="1366" height="601" alt="buckect version 11" src="https://github.com/user-attachments/assets/afad361f-1ce2-4268-8903-5a8ec6cb816b" />

**DEFAULT ENCRYPTION :--->** *Configure Default encryption settings (selecting server-side encryption type and bucket keys) before finalizing your S3 bucket creation.*

<img width="1366" height="598" alt="default encryption 12" src="https://github.com/user-attachments/assets/469cdfd8-961f-4fa3-9349-e9616140a17a" />

**CREATE BUCKET SUCCESSFUL :--->** *Confirmation message showing that the S3 bucket "pratiksha-27" has been successfully created.*

<img width="1366" height="601" alt="pratu 14" src="https://github.com/user-attachments/assets/6720a000-8058-4ad2-880b-1cfe0ac92d86" />

**UPLOAD :---** *Use the Upload interface to drag and drop files/folders or click Add files to upload data to your S3 bucket.*

<img width="1366" height="598" alt="upload 15" src="https://github.com/user-attachments/assets/401aa4a5-6c0d-4cd0-838b-f65ab8e3852d" />

**DESTINATION :--->** *Use the Upload interface to drag and drop files/folders or click Add files to upload data to your S3 bucket.*

<img width="1366" height="632" alt="destination 16" src="https://github.com/user-attachments/assets/38c0cfaa-9b1d-43ad-9f49-a4570e3628ba" />

**SUCCESSFUL UPLOAD CONFIRMATION :--->** *Successful upload confirmation showing that the file has been uploaded to the S3 bucket*

<img width="1366" height="600" alt="Fand F 17" src="https://github.com/user-attachments/assets/22a1407c-865a-4f41-9026-fef0872f95c9" />

**SUCCESSFULLY UPLOADED :--->** *View the successfully uploaded file listed under the Objects tab inside the pratiksha-27 S3 bucket.*

<img width="1366" height="594" alt="Obj 18" src="https://github.com/user-attachments/assets/0f50c853-0e0e-42fb-8ecc-1e7da5237290" />

**OUTPUT :--->** *Final validation of the uploaded file accessible via the S3 object endpoint URL showing the computer network types diagram.*

<img width="1366" height="716" alt="otp 19" src="https://github.com/user-attachments/assets/1c70fe22-eefc-407e-9909-ce211a0c95ae" />

**INDEX HTML :-->** *Uploading an index.html file to the S3 bucket pratiksha-27 for static website hosting.*

<img width="1366" height="597" alt="20" src="https://github.com/user-attachments/assets/30ec714d-354d-457d-9ad1-7c4df6602ab4" />

   *Upload succeeded summary displaying the successfully uploaded index.html file in bucket pratiksha-27.*
   
   <img width="1366" height="595" alt="21" src="https://github.com/user-attachments/assets/c5d17c1c-fba6-45dc-b40f-99e773742ab6" />

*View both uploaded objects (index.html and the network diagram) listed under the Objects tab inside the pratiksha-27 S3 bucket.*

<img width="1366" height="689" alt="22" src="https://github.com/user-attachments/assets/d90c731b-494d-44c0-b024-2a4a924de0d3" />

**WELCOME TO MY S3 WEBPAGE :--->** *Verify the rendered static webpage displaying "Welcome To My S3 Webpage" accessed via the S3 endpoint URL.*

<img width="1366" height="625" alt="23" src="https://github.com/user-attachments/assets/fde31c78-680f-40d8-b37f-aedb9c3122b1" />

 *Uploading an updated version of the index.html file (1.9 KB) to the S3 bucket pratiksha-27.*

<img width="1366" height="603" alt="24" src="https://github.com/user-attachments/assets/09a2926d-c19a-4b3d-9326-acbf97e4b875" />

*Upload succeeded summary showing the updated index.html file (1.9 KB) successfully uploaded to the S3 bucket pratiksha-27.*

<img width="1346" height="593" alt="25" src="https://github.com/user-attachments/assets/1b4d0e83-e365-42aa-be3e-c23320921a9e" />

*View multiple versions of index.html alongside the network diagram under the Objects tab with versioning enabled in the pratiksha-27 S3 bucket.*

<img width="1366" height="591" alt="26" src="https://github.com/user-attachments/assets/c4c61f79-d19b-4600-a985-b3388afa67f5" />

*View multiple versions of index.html displayed under the Objects tab with version IDs enabled in the pratiksha-27 S3 bucket.*

<img width="1366" height="607" alt="28" src="https://github.com/user-attachments/assets/f2109967-fcfd-444f-99ea-866c06c36219" />

*View the complete list of object versions and files, including multiple iterations of index.html, the PNG asset, and the network diagram, under the Objects tab with versioning enabled in the pratiksha-27 S3 bucket.*

<img width="1366" height="600" alt="29" src="https://github.com/user-attachments/assets/02e91be1-98ca-4eb3-8993-0675da7ebb2c" />

*View the Buckets list dashboard showing the general purpose S3 bucket pratiksha-27 in the us-west-2 region with its creation date.*

<img width="1366" height="597" alt="30" src="https://github.com/user-attachments/assets/1aad9ec3-2444-4b34-9bd1-dfbf323af2d5" />

*View the XML error response showing AccessDenied when attempting to access a private S3 object URL without public permissions.*

<img width="1366" height="587" alt="31" src="https://github.com/user-attachments/assets/181f71f6-bebf-4628-a948-6545a7fa6d70" />

*View the Empty bucket confirmation prompt by typing permanently delete to clear all objects from the pratiksha-27 S3 bucket.*

<img width="1366" height="602" alt="32" src="https://github.com/user-attachments/assets/0370fe4c-6cdd-4d27-bdbf-edb023ef3f75" />

 *View the successful bucket empty confirmation summary showing 5 objects (518.0 KB) deleted from the pratiksha-27 S3 bucket.*

 <img width="1366" height="601" alt="33" src="https://github.com/user-attachments/assets/714fc81a-277e-4fb3-8858-a8c612096229" />

*View the Delete bucket confirmation interface by entering the bucket name pratiksha-27 to permanently delete the S3 bucket.*

<img width="1366" height="602" alt="34" src="https://github.com/user-attachments/assets/557e49ac-79a6-4055-bfa6-b97e25e8fc3e" />

*View the success banner confirming that the S3 bucket pratiksha-27 has been successfully deleted.*

 ### 9. Security Configurations

  Security is an important part of cloud storage management.
  The following security practices are implemented:
- **Block Public Access:** Prevents unintended public access to the bucket.
- **Bucket Permissions:** Controls who can access stored objects.
- **IAM Policies:** Assigns permissions to authorized users.
- **Versioning:** Maintains multiple versions of objects to help recover from accidental changes or deletions.
- **Encryption:** Protects stored data using server-side encryption.
- **Least Privilege:** Provides only the permissions required to perform a task.

### 10. Future Enhancements

In the future, this project can be extended by implementing:

1. S3 Lifecycle Management for automatic object transitions and expiration.
2. Cross-Region Replication for additional data protection.
3. CloudTrail integration for monitoring S3 API activity.
4. CloudWatch monitoring and alerts.
5. AWS CLI automation for bucket management.
6. S3 access logging for auditing access activity.

### 11.What I Learned

Through this project, I learned how Amazon S3 provides cloud-based object storage and how to create and manage buckets and objects. I also gained practical knowledge of file uploads, downloads, versioning, encryption, and IAM permissions. Most importantly, I understood why controlling public access and applying security best practices are essential for protecting data stored in the cloud.

### 12. Disclaimer

This project was created for educational purposes to understand Amazon S3, cloud storage management, and AWS security configurations. All activities were performed in a controlled AWS learning environment. No unauthorized access or testing was performed on third-party resources.

















