# 🏫 AAU Student Management System

## **Cloud Database System Project**  
*Addis Ababa University - Computer Science Department*

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Last Commit](https://img.shields.io/github/last-commit/getaye21/AAU-CS-Student-System)
![Repo Size](https://img.shields.io/github/repo-size/getaye21/AAU-CS-Student-System)

---

## 🚀 Quick Start

### **1. Live Demo**
**Access your application:**  
👉 **[https://getaye21.github.io/AAU-CS-Student-System/public/](https://getaye21.github.io/AAU-CS-Student-System/public/)**

### **2. Configure Database**
1. Open the live demo above
2. Click **"Configure Database Connection"** in the header
3. Enter your **Supabase credentials**:
   - **URL**: From Supabase Settings → API
   - **Anon Key**: From Supabase Settings → API
4. Click **"Save Configuration"**

### **3. Database Setup**
Run this SQL in your Supabase project:

```sql
CREATE TABLE students (
  id UUID DEFAULT gen_random_uuid() PRIMARY KEY,
  student_id VARCHAR(20) UNIQUE NOT NULL,
  first_name VARCHAR(50) NOT NULL,
  last_name VARCHAR(50) NOT NULL,
  father_name VARCHAR(50) NOT NULL,
  email VARCHAR(100) UNIQUE NOT NULL,
  phone VARCHAR(20),
  hometown VARCHAR(100),
  major VARCHAR(50),
  gpa DECIMAL(3,2),
  created_at TIMESTAMPTZ DEFAULT NOW()
);
