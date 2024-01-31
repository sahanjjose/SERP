# College Management System
A college management system built using Django framework. It is designed for interactions between students and teachers. Features include attendance, marks and time table. The info application keeps record of data efficiently and allows easy editing.

## Installation

Python and Django need to be installed

```bash
pip install django
```

## Usage

Go to the Capstone folder and run

```bash
python manage.py runserver
```

Then go to the browser and enter the url **http://127.0.0.1:8000/**

## Understanding
In the code is a Django project called Capstone that contains a single app called info.

First, open up info/urls.py, where the URL configuration for this app is defined. Some of the routes associated with the views function added are attendance, timetable, attendance_detail, etc.

Now, let’s look at info/views.py. There’s just one view here now, the login_required view. This view returns templates from info/templates/info/which are - login.html, logout.html, homepage.html, attendance.html, etc.

Finally, take a look at info/models.py. The Models we have defined are a User model that represents each user of the application because it inherits from AbstractUser, it will already have fields for a username, email, password, etc. A Dept Model which returns the user name. A course model which returns the course name. A Student model which returns the student model and many more like Teacher, Class, Assign, Attendance, etc. The file has a total of 25 Models approximately.

The main purpose of this project is to illustrate the requirements of the project Capstone(CollegeERP) and is intended to help any organization to maintain and manage personal data. It is a comprehensive project developed from the ground up to fulfill the needs of colleges as they guide their students. This integrated information management system connects daily operations in the college environment ranging from Attendance management to communicational means among students and teachers. This reduces data error and ensures that information is always up-to-date throughout the college. It provides a single source of data repository for streamlining your processes and for all reporting purposes. It has a simple user interface and is intuitive. This insures that the users spend less time in learning the system and hence, increase their productivity. Efficient security features provide data privacy and hence, increase their productivity.

Information regarding students, teachers and courses are stored in the database. Every user can view only certain information based on their user class. For example, a teacher can view student and course information that they are handling. This feature is important as the information must be viewed by only the authorized users.

## System Design
Various Design concepts and processes were applied to this project. Following concepts like separation of concerns, the software is divided into individual modules that are functionally independent and incorporates information hiding. The software is divided into 3 modules which are students, teachers and administrators. We shall look at each module in detail.

**(A) Student:**

Each student belongs to a class identified by semester and section. Each class belongs to a department and are assigned a set of courses. Therefore, these courses are common to all students of that class. The students are given a unique username and password to login. Each of them will have a different view. These views are described below.

1. Student information:
Each student can view only their own personal information. This includes their personal details like name, phone no, address etc. Also, they can view the courses they are enrolled in and the attendance, marks of each of those.
2. Attendance information:
Attendance for each course will be displayed. This includes the number of attended classes and the attendance percentage. If the attendance percentage if below a specified threshold, say 75%, It will be marked in red otherwise it be in green. There will also be a day wise attendance view for each course which shows the date and status. This will be presented in a calender format.
3. Marks information:
There will be 5 events and 1 semester end examination for each course. The marks for each of these will be provided in the ERP system.

(**B**) **Teacher Information:**

Each teacher belongs to a department and are assigned to classes with a course. Teachers will also have a username and password to login. The different views for teachers are described below.

1. Information:
The teachers will have access to information regarding the courses and classes they are assigned to. Details of the courses include the credits, the syllabus plan. Details of the class include the department, semester, section and the list of students in each class. The teacher will also have access to information of students who belong to the same class as as the teacher.
2. Attendance:
The teacher has the ability to add and also edit the attendance of each student. For entering the attendance, they will be given the list of students in each class and they can enter the attendance of the whole class on a day to day basis. There will be two radio buttons next to each student name, one for present and the other for absent. There will also be an option for extra classes. Teachers can edit the attendance of each student either for each student individually or for the whole class.
3. Marks
The teacher can enter the marks for the 5 events and 1 SEE for each course they are assigned. They also have the ability to edit the marks in case of any changes. Reports such as the report card including all the marks and CGPA of a student can be generated.

**(C) Administrator**

The administrator will have access to all the information in the different tables in the database. They will access to all the tables in a list form. They will be able to add a entry in any table and also edit them. The design of the view for the admin will provide a modular interface so that querying the tables will be optimized. They will be provided with search and filter features so that they can access data efficiently.

## Login

The login page is common for students and teachers.
The username is their name and password for everyone is 'mango270'.
Example usernames:
student- 'Sahanj'
teacher- 'David'

You can access the django admin page at **http://127.0.0.1:8000/admin** and login with username 'admin' and the password 'project123'.

Also a new admin user can be created using

```bash
python manage.py createsuperuser
```

## Users

New students and teachers can be added through the admin page. A new user needs to be created for each.

The admin page is used to modify all tables such as Students, Teachers, Departments, Courses, Classes etc.

## Specifications:
There are several types of end users for the college ERP system. They are broadly divided as Students, Staff and the Administrator. Each of these classes have their own set of features.

The student has the following features:
1. View the Attendance status of the courses to which they are enrolled.
2. View the Marks of the courses to which they are enrolled.
3. View the notification from the college administrator.
4. Communicate or give feedback to their respective teachers.
5. Communicate with other students of the same university.

The staff has the following features:
1. Access to the information of all students that attend their courses.
2. Add and edit the Attendance status of those students.
3. Add and edit the exam marks of those students.
4. Avail the different types of leave.
5. Swap classes with other teachers who teach for the same class.

The administrator has the following features:
1. Add and update students, teachers and courses.
2. Assign teachers and students to courses

## Justification
Tittle of the project as College ERP System is the system that deals with the issues related to a particular institution. It is the very useful to the student as well as the faculties to easy access to finding the details. The college ERP provides appropriate information to users based on their profiles and role in the system. This project is designed keeping in view the day to day problems faced by a college system.

The fundamental problem in maintaining and managing the work by the administrator is hence overcome. Prior to this it was a bit difficult for maintaining the time table and also keeping track of the daily schedule. But by developing this web-based application the administrator can enjoy the task, doing it ease and also by saving the valuable time. The amount of time consumption is reduced and also the manual calculations are omitted, the reports can be obtained regularly and also whenever on demand by the user. The effective utilization of the work, by proper sharing it and by providing the accurate results. The storage facility will ease the job of the operator. Thus the system developed will be helpful to the administrator by easing his/her task.

This System provide the automate admissions no manual processing is required. This is a paperless work. It can be monitored and controlled remotely. It reduces the man power required. It provides accurate information always. All years together gathered information can be saved and can be accessed at any time. The data which is stored in the repository helps in taking intelligent decisions by the management providing the accurate results. The storage facility will ease the job of the operator. Thus the system developed will be helpful to the administrator by easing his/her task providing the accurate results. The storage facility will ease the job of the operator.


**Thank You!**
