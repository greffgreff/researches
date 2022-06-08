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
After careful consultation with the product owners, we established that the most important aspect of the solution is to revamp the conventional flow of ordering food at a restaurant with hardcover menus.

Below is a diagram of this flow. The interactions takes place between the waiter and the customer:
![ordering food](https://i.imgur.com/4RyGduE.jpg)
> Note that the diagram shows waiters need to wait for customers to chose. Conversely, customer may also wait for waiters once ready, though this is not shown on the diagram.

With the input of the client, we developed the system in such a way that some bottlenecks such as waiting time and the need for a waiter are almost entirely removed. Below is our proposed flow of ordering food using our system:
![ordering food with system](https://i.imgur.com/ROW0Dr3.jpg)

The new flow gives not only the customer a lot more freedom and ease in ordering, but also frees waiters for other takes. The clients specifically wished for waiters to still be part of the process for greeting customers. No longer are orders needed to be written down by a waiter and brought to the kitchen on paper. Placed orders are immediately redirected to the kitchen, where they are managed digitally.

Futhermore, along side placing orders, the payment process has also been rethought. The conventional flow dictates that a waiter must take payment from customers like so:
![payment](https://i.imgur.com/sjIy4Yy.jpg)

Using our solution, the payment no longer requires the interaction of a waiter nor does the need to pass payment in the form of cash or card needed by hand:
![payment with system](https://i.imgur.com/JrTml8E.jpg)
> Payment assurance was deemed out of scope for the project. Whether payments are honored by customers is not handled on the system as per the client. 

## LO8: Professional
> Professional manner:
You develop software as a team effort according to a prescribed software methodology and following team agreements. You are able to track your work progress and communicate your progress with the team.
You  independently recognize and decide where your knowledge falls short to solve a software problem and  communicate which new knowledge and skills you need to learn.
