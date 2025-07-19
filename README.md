
# Cloud-Based Document Management System

This project is a Laravel-powered cloud-based service for basic data analytics and document management. It was developed as part of the "Cloud and Distributed Systems (SICT 4313)" course at the Islamic University of Gaza.

The system allows users to upload PDF and DOCX documents to the cloud (Dropbox), automatically extract and store their metadata, perform full-text search with highlighted results, and classify them based on predefined categories. It is deployed on ByetHost and uses Dropbox for storage.

---

## 📌 Features

- **File Upload**
  - Supports PDF and Word (DOCX) documents
  - Files are validated, uploaded to Dropbox, and metadata is extracted automatically

- **Metadata Extraction**
  - Extracts title, size, type, and original name from files
  - Extracts and indexes full document text

- **Sorting**
  - Sorts documents alphabetically based on title (from metadata or content)

- **Search**
  - Full-text search with case-insensitive keyword matching
  - Results show highlighted keyword matches

- **Classification**
  - Documents are automatically categorized based on keyword matching rules
  - Supports nested categories (parent-child)

- **Statistics Dashboard**
  - Displays total documents, storage usage, and average operation times

- **Security**
  - User authentication (Laravel Sanctum)
  - File validation and access protection
  - Dropbox token and credentials secured via `.env`

---

## 🧰 Technologies Used

- Laravel 10 (PHP framework)
- MySQL (Relational Database)
- Dropbox API (Cloud storage)
- Bootstrap 5 (Responsive UI)
- Blade Templating (Laravel Views)
- Spatie Flysystem Dropbox (Dropbox integration)
- PhpOffice\PhpWord and Smalot\PdfParser (Text extraction)

---

## 📂 Architecture Overview

- **Frontend**: Laravel Blade + Bootstrap 5 for a responsive and clean UI
- **Backend**: Laravel controllers and jobs manage uploads, metadata, search, and classification
- **Cloud Storage**: Dropbox (files stored externally)
- **Database**: MySQL database hosted on ByetHost (stores metadata, classification, and stats)
- **Hosting**: ByetHost (cPanel + FTP deployment)

---

## 🚀 Live Demo

🔗 Live system: [https://documents.byethost10.com/documents](https://documents.byethost10.com/)  
🔗 Dropbox Storage: [https://www.dropbox.com/home/documents](https://www.dropbox.com/home/documents)  
🔐 Login credentials:  
- Email: `rbaraka@iugaza.edu.ps`  
- Password: `myPassword33`

---

## 🧪 How to Use

- Upload a document through the upload page
- Automatically processes the file: stores in Dropbox + extracts content
- System assigns category based on keywords
- Use the search bar to find keywords and view results with highlights
- Browse documents in dashboard, sorted by title

---

## 📜 License

This project is developed for educational purposes only under the Cloud and Distributed Systems course at the Islamic University of Gaza.

Instructor: Dr. Rebhi S. Baraka  
Contributors: Aya Nabil AlHarazin, Rania Raid Kashkash
