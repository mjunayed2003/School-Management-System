🏫 School Management System - Backend
Project Overview

This is a School Management System backend API built with Node.js, Express, and MongoDB. It manages students, teachers, classes, subjects, attendance, exam results, notices, and complaints, and provides endpoints for admin, teacher, and student operations.

The system supports role-based operations, attendance tracking, exam management, and school notices handling.

Features
Admin

Register and login admin users

View admin details

Students

Register and login students

View student list and details

Update student information

Delete students individually or by class

Track and manage attendance (per subject or overall)

Update exam results

Teachers

Register and login teachers

View teacher list and details

Update assigned subjects

Track teacher attendance

Delete teachers individually or by class

Classes (Sclass)

Create, view, update, and delete classes

View students in a class

Subjects

Create subjects and assign to classes

View all subjects, class-specific subjects, or free subjects

Delete subjects individually or by class

Notices

Create, view, update, and delete notices

Complaints

Create and view complaints

Installation

Clone the repository

git clone <your-repo-url>
cd school-management-backend


Install dependencies

npm install


Create a .env file in the root folder with:

MONGO_URI=<your-mongodb-connection-string>
JWT_SECRET=<your-jwt-secret>
PORT=5000


Start the server

npm run dev

API Routes
Admin
Method	Route	Description

POST	/AdminReg	Register admin

POST	/AdminLogin	Admin login

GET	/Admin/:id	Get admin details

Students
Method	Route	Description

POST	/StudentReg	Register student

POST	/StudentLogin	Student login

GET	/Students/:id	Get students by class or school

GET	/Student/:id	Get student details

PUT	/Student/:id	Update student info

PUT	/UpdateExamResult/:id	Update exam result

PUT	/StudentAttendance/:id	Record student attendance

PUT	/RemoveAllStudentsSubAtten/:id	Clear attendance by subject

PUT	/RemoveAllStudentsAtten/:id	Clear all attendance

DELETE	/Student/:id	Delete a student

DELETE	/Students/:id	Delete multiple students

DELETE	/StudentsClass/:id	Delete students by class
Teachers

Method	Route	Description
POST	/TeacherReg	Register teacher

POST	/TeacherLogin	Teacher login

GET	/Teachers/:id	Get teachers

GET	/Teacher/:id	Get teacher details

PUT	/TeacherSubject	Update assigned subjects

POST	/TeacherAttendance/:id	Record teacher attendance

DELETE	/Teacher/:id	Delete teacher

DELETE	/Teachers/:id	Delete multiple teachers

DELETE	/TeachersClass/:id	Delete teachers by class

Classes (Sclass)
Method	Route	Description

POST	/SclassCreate	Create class

GET	/SclassList/:id	List all classes

GET	/Sclass/:id	Get class details

GET	/Sclass/Students/:id	Get students in class

DELETE	/Sclass/:id	Delete class

DELETE	/Sclasses/:id	Delete multiple classes

Subjects
Method	Route	Description

POST	/SubjectCreate	Create subject

GET	/AllSubjects/:id	List all subjects

GET	/ClassSubjects/:id	List class-specific subjects

GET	/FreeSubjectList/:id	List subjects not assigned

GET	/Subject/:id	Get subject details

DELETE	/Subject/:id	Delete subject

DELETE	/Subjects/:id	Delete multiple subjects

DELETE	/SubjectsClass/:id	Delete subjects by class
Notices

Method	Route	Description
POST	/NoticeCreate	Create notice

GET	/NoticeList/:id	List notices

PUT	/Notice/:id	Update notice

DELETE	/Notice/:id	Delete notice

DELETE	/Notices/:id	Delete multiple notices
Complaints

Method	Route	Description
POST	/ComplainCreate	Create complaint

GET	/ComplainList/:id	List complaints
