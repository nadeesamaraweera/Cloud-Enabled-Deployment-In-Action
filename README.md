# Cloud Enabled Deployment In Action with AWS and GCP

This repository contains four projects:

- course-service (Spring Boot + MySQL)
- student-service (Spring Boot + MongoDB)
- media-service (Spring Boot + Local file storage, can be extended to S3/MinIO)
- frontend-app (React + TypeScript)

## Backend Services

### 1. course-service
- Entity: Course(id, name, duration)
- Endpoints:
  - GET /courses
  - GET /courses/{id}
  - POST /courses
  - DELETE /courses/{id}
- Default port: 8081
- Configure MySQL settings

### 2. student-service
- Document: Student(registrationNumber, fullName, address, contact, email)
- Endpoints:
  - GET /students
  - GET /students/{id}
  - POST /students
  - DELETE /students/{id}
- Default port: 8082
- Configure MongoDB settings

### 3. media-service
- Resource: files
- Endpoints:
  - POST /files (multipart/form-data: file)
  - GET /files (list)
  - GET /files/{id} (fetch)
  - DELETE /files/{id} (delete)
- Default port: 8083
- Uses local disk storage at `./data/media` by default (override with env var `MEDIA_STORAGE_DIR`).

## Frontend (frontend-app)
- React + TypeScript + MUI + Axios + Vite app with 3 sections: Courses, Students, Media
- Scripts:
  - npm run dev (Vite dev server)
  - npm run build (TypeScript build + Vite build)
  - npm run preview (Preview built app)

## Build

- Backend: run `mvn -q -e -DskipTests package` at repo root to build services.
- Frontend: run `npm install` then `npm run dev` inside `frontend-app`.

---  

## 🌐 Cloud Deployment

- **Docker**: Containerize backend services and frontend.
- **AWS / GCP**: Connect cloud-managed MySQL and MongoDB instances.
- **Local / Cloud Storage**: Media files can be stored locally or in S3/MinIO. 

## 🛠️ Built With 
![Springboot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
[![React.js](https://img.shields.io/badge/React-000000?style=for-the-badge&logo=react&logoColor=61DAFB)](https://react.dev/)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![MySQL](	https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)

## 📂 Clone Project  
```bash
  https://github.com/nadeesamaraweera/Cloud-Enabled-Deployment-In-Action.git
``` 

## 🌐 Cloud Database Configurations  
[View AWS / GCP Configurations](https://www.notion.so/Connecting-Database-Instances-in-AWS-and-GCP-26c8b164115e80e3a636e3e263fb9fe7?source=copy_link)

## 🎥 Demo Video
[Watch Demo](https://drive.google.com/file/d/1hjJYZSEHpl9djVByP6yV3Cdig5NA4Sj-/view?usp=sharing) 

---
## 👤 Student Information
- Name: Nadeesha Thejangani Samaraweera
- Student Registration Number: 2301682018
- Email Address: nadeesamaraweera2000@gmail.com

## 📝 License
This project is licensed under the [MIT License](LICENSE)
