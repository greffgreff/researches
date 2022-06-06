# Group Project

POS - Point of service, refers to the digital menu with categories
KDS - Kitchen display system, refers to the system where orders are displayed and be managed by ktichen staff
IMS - Inventory management system, refers to the system where inventory of all ingredients are managed   

Frontend predominantly. Offset my lack in backend dev with IP, where I built a RESTful API in Spring Boot.

## LO1: Web Application

### User-friendly
> The goal of usability testing is to understand how real users interact with your website and make changes based on the results

### Full-stack
The project is a full-stack application. The frontend uses the popular ReactJS framework in javascript and the backend, ASP in C#. While the frontend handles the POS, the KDS, and the IMS combined, the backend handles CRUD functionality on a MySQL database in a RESTful manner. Architecture diagram of the system the team built:

![architecture](https://i.imgur.com/RQ64cmJ.png)

The frontend was developed in a way that is common in the industry, where blocks of UI are decomposed into smaller and reusable React components. The frontend is deployed on a Firebase instance and can be accessed though [here](https://hummus.tycho.dev/).

The backend relies on the Entity framework to simplify database-backend interactions though ORM. The backend is first containerized on Dockerhub and then deployed through a Digital Ocean instance.

You design and build a full stack application using commonly accepted front end (Javascript-based framework) and back end techniques (e.g. Object Relational Mapping) choosing and implementing relevant communication protocols and addressing asynchronous communication issues.

## LO3: Agile method
> You are aware of most popular agile methods and their underlying agile principles. You are able to implement the process of your software project according to a chosen methodology.

## LO5: Cultural differences and ethics
> Recognize:  Recognition is based on theoretically substantiated awareness of cultural differences and ethical aspects in software engineering.
> 
> Take into account:
> - Adapt your communication, working, and behavior styles to work with other developers from different cultures; 
> - Address one of the standard Programming Ethical Guidelines (e.g., ACM Code of Ethics and Professional Conduct) in your work. 

## LO6: Requirements and Design
> Multipletypes of test techniques: You apply user acceptance testing and stakeholder feedback to validate the quality of the requirements. You evaluate the quality of the design (e.g., by testing or prototyping) taking into account the formulated quality properties like security and performance.

## LO7: Business processes
> Simple: predominantly sequential processes with one or two alternative paths.
> Relate: understanding the relationships between the process and software.

## LO8: Professional
> Professional manner:
You develop software as a team effort according to a prescribed software methodology and following team agreements. You are able to track your work progress and communicate your progress with the team.
You  independently recognize and decide where your knowledge falls short to solve a software problem and  communicate which new knowledge and skills you need to learn.
