 # PROJECT 1 PORTOFOLIO KELAS EXPERTISE CLOUD COMPUTING

##### KASUS
Sebagai Cloud Dev Engineer anda diminta membuat website company profile 
perusahaan. Anda diminta membuatnya di AWS dengan memperhitungkan
biaya terendah

##### GOAL
1. User dapat membuat website company profile
2. File website disimpan pada S3
3. User dapat mengakses website menggunakan DNS S3
4. User dapat mengakses website menggunakan DNS CDN

##### PREREQUISITE
1. AKUN GITHUB (SELURUH PROJECT DI UPLOAD DI GITHUB)

##### PERANGKAT LUNAK YANG DIGUNAKAN

[![Visual Studio](https://badgen.net/badge/icon/visualstudio?icon=visualstudio&label)](https://visualstudio.microsoft.com)
[![Build Status](https://img.shields.io/badge/HTML-239120?style=for-the-badge&logo=html5&logoColor=white)](https://github.com/muhammadalfinnurrizki/Project-UKK-AWS-Web-Statis)
[![Build Status](https://img.shields.io/badge/CSS-239120?&style=for-the-badge&logo=css3&logoColor=white)](https://github.com/muhammadalfinnurrizki/Project-UKK-AWS-Web-Statis/tree/main/css)
[![Build Status](https://img.shields.io/badge/Amazon_AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)

##### MATERI
1. WEB STATIS (HTML DAN CSS)
2. STORAGE (S3)
3. ADD ON (CDN)

##### KETENTUAN WEBSITE
1. MINIMAL 2 HALAMAN
2. ADA LOGO
3. ADA GAMBAR PRODUK
4. UI/UX DIBUAT SEMAKSIMAL MUNGKIN

### TOPOLOGI
![Topologi](https://i.postimg.cc/sf9nT2Sy/image.png)

# How To Deploying On AWS

## A. Bucket S3
###### 1. Create Bucket
Name	: 
###### Enable Public Access
###### Checklist “I acknowledge …”

###### 2. Setting Bucket
Permissions 
Bucket Policy - edit

```bash
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": [
                "s3:GetObject"
            ],
            "Resource": [
                "arn:aws:s3:::Bucket-Name/*"
            ]
        }
    ]
}
```

Properties
Enable Static Website Hosting
Index document : index.html

###### 3. Upload File/Folder Website
Test	: Bucket Website Endpoint

## B. Cloud Front
###### Create Distribution
Origin Domain		: your S3 - use website endpoint
Name			: 
Test	: Distribution Domain Name

