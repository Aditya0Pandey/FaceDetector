Face Vision App (Deployed on AWS)

A facial recognition web app using Microsoft Azure Face API for facial analysis.  
This version is deployed using **AWS S3**, **CloudFront**, and a custom subdomain under `devbypandey.xyz`.

---

🚀 Features

- Upload an image and analyze detected faces using Azure's Face API.
- Displays attributes such as:
  - Age
  - Emotion
  - Gender
  - Glasses
  - Facial landmarks

---

🛠 Technologies Used

- HTML / JS / MJS frontend
- Microsoft Azure Face API
- AWS S3 (for static hosting)
- AWS CloudFront (for CDN & SSL)
- AWS Route 53 (for subdomain and DNS)

---

🧪 Setup & Deployment

  🔧 Azure Setup
1. Create an Azure account.
2. Setup **Azure Face API** in Azure Portal.
3. Get your **API Key** and **Endpoint URL**.

  📁 Local Configuration
1. In `app.mjs`, replace:
   
   const API_KEY = 'YOUR_AZURE_KEY';
   const ENDPOINT = 'https://<region>.api.cognitive.microsoft.com';
   
2. Save the changes.

---

☁️ AWS Hosting (Static)

### ✅ Upload to S3
1. Compress all files into a `.zip` (if needed).
2. Go to **S3 Console**, upload contents to your bucket.
3. Make files public or use a CloudFront distribution.

### 🌍 Setup Custom Subdomain
1. Go to **Route 53 → Hosted Zones** → `YOUR DOMAIN`.
2. Add a CNAME or A Record pointing your subdomain (`subdomain`) to the CloudFront distribution.

### 🔐 SSL
SSL is automatically enabled via CloudFront if using a valid ACM certificate.

### 🔄 Deployment Updates
- Reupload updated files to S3.
- Go to CloudFront → Create Invalidation → `/*` to clear cache.

---

📸 Live Demo

🔗 [https://face.devbypandey.xyz](https://face.devbypandey.xyz)

---

## 📄 License

MIT License. This is a modified version of [benc-uk/face-vision-app](https://github.com/benc-uk/face-vision-app).
```

---
