 **# University Telephone Directory (Spring Project)**

**## Overview**

This project aims to create a comprehensive telephone directory for university members using Spring technologies. It will enable users to manage their contact information, search for contacts, and access essential directory services.

**## Functional Requirements**

* **User Management:**
  - Registration for students, faculty, and staff with basic information (name, email).
  - Admin creation and management of user accounts (assigning roles).
* **Contact Management:**
  - User addition of own contact information (name, department, phone number, email).
  - User editing of own contact information.
  - Admin editing of any contact information.
* **Search:**
  - User search for contacts by name, department, or both.
  - Display of relevant contact details (name, department, phone number, email) in search results.
* **Permissions:**
  - User viewing of only their own contact information and limited details of others.
  - Admin viewing and editing of all contact information.
* **Additional Features:**
  - Pagination for large search results.
  - Option to export search results in CSV format.
  - Auditing of contact information (track changes made by admins).

**## REST API Endpoints**

* **User Management:**
  - POST /users
  - GET /users/{id} (Admin only)
  - PUT /users/{id} (Admin only)
  - DELETE /users/{id} (Admin only)
* **Contact Management:**
  - POST /contacts
  - GET /contacts/{id} (User can only access their own)
  - PUT /contacts/{id} (User can only update their own)
  - DELETE /contacts/{id} (Admin only)
* **Search:**
  - GET /contacts?name={name}&department={department} (optional)
* **Additional Endpoints:**
  - GET /contacts/export (Admin only)
  - GET /contacts/audit (Admin only)

**## Technologies Used**

- Java
- Spring Boot
- Spring Security
- Spring Data JPA
- PostgreSQL