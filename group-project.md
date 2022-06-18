# Group Project

## About the project

Upon arrival at a restaurant, customers are greeted by a waiter start a new session on the system and hands them a 4-digit PIN, a way to keep track of customers within the restaurant. 

Afterwards, customers are free to sit at any table they would like and can scan a QR code placed on the table. The QR code redirects to a digital menu after the PIN is entered. 

From there, customers can see and select dishes orgranized in categories, can place orders, view previous ones, and finally make payment through the system. 

<p>POS - Point of service, refers to the digital menu with categories</p>
<p>KDS - Kitchen display system, refers to the system where orders are displayed and be managed by ktichen staff</p>
<p>IMS - Inventory management system, refers to the system where inventory of all ingredients are managed</p>

## Learning outcomes

<details>
  <summary>LO1: Web Application</summary>
  <br />

  The project is a full-stack application. The frontend uses the popular ReactJS framework in javascript and the backend, ASP in C#. While the frontend handles the POS, the KDS, and the IMS combined, the backend handles CRUD functionality on a MySQL database in a RESTful manner. Architecture diagram of the system the team built:
  ![architecture](https://i.imgur.com/RQ64cmJ.png)

  The frontend was developed in a way that is common in the industry, where blocks of UI are decomposed into smaller and reusable React components. The frontend is deployed on a Firebase instance and can be accessed though [here](https://hummus.tycho.dev/).

  The backend relies on the Entity framework to simplify database-backend interactions though ORM. The backend is first containerized on Dockerhub and then deployed through a Digital Ocean instance.

  You design and build a full stack application using commonly accepted front end (Javascript-based framework) and back end techniques (e.g. Object Relational Mapping) choosing and implementing relevant communication protocols and addressing asynchronous communication issues.

  Source code for the backend can be found [here](https://github.com/hummusteam/HummusApp).

  Source code for the frontend can be found [here](https://github.com/hummusteam/HummusFront).

  <br />  
</details>


<details>
  <summary>LO3: Agile method</summary>
  <br />

> You are aware of most popular agile methods and their underlying agile principles. You are able to implement the process of your software project according to a chosen methodology.
  
  Agile Scrum 
  
  What is agile? It embraces:
  - Collaboration between the development team and between the dev team and the customer interactions
  - Continous software dev
  - Quickly respond to change in software requirements
  
  We settled on using shortcut.com to manage our project with user stories, epics, and smaller tasks. Throughout the project, the team and I closely followed and manage the our backlog on the platform. 

  The project unfolded in a total of 5 sprints of a few weeks each. At the start of each new sprint, the development team and the product owners conducted sprint reviews, where the team first showcases the the implementation of new features followed by the stakeholder's feedback. Reviews concluded with discussions about things that have been completed and things that still need attention for the next sprint.
  
  Scrum roles were defined at the beginning of the project to each memeber of the team, including scrum master, note takers, time keepers. Those roles were cycled between ourselves throughout the project. 
  
  Every project day, Mondays and Tuesdays, the team had standups, where team members took turn on the things he completed and what he has planned for the day.
  
https://www.atlassian.com/agile/scrum/standups
  
  <br />  
</details>


<details>
  <summary>LO5: Cultural differences and ethics</summary>
  <br />

  To best showcase this learning outcome, I discuss my personal experience with working with people of other traditional and cultural backgrounds and other events in my life. 
  
  Cultural clusters, in my own words, are a set of personality and behavioural traits that I believe are revealed from ones self and others anywhere, including during work. There are three cultural clusters, linear-active, multi-active, and reactive. From the [material](https://fhict.instructure.com/courses/12075/pages/group-management-can-you-work-with-people-from-other-cultures) on Canvas and the presentation cultural clusters:
  
  Linear-active — A person introverted, quiet, and likes privacy. He plans ahead, accepts favours reluctantly, limited body language, and is brief on telephone.
  Multi-active — A person extroverted, impatient, inquisitive, and talkative. He seeks favours. Speaks with his body.
  Reactive — Introvert, patient, silent, respectful, good listener. Doesn’t interrupt, subtle body language. summarises well, must not lose face, avoids confrontation.
  
  While it is not a perfect match, I can categories myself in-between the Reactive and Linear-active categories. 
  I am introverted, prefer to keep conversations on phones short and sweet, and appreciates privacy. There are traits that I can see myself with when working with others. I like to see myself as a patient person. Throughout the semester, I found myself helping others for long hours since I like helping others. 
  
  To me it seemed logical to help others with things I was knowledgeable in. However, I was surprised to see a person much more knowledgable than me becoming frustrated with the same person I helped after a couple of minutes of explanation. Perhaps this person was part of the Multi-active category. 
  
  > Please note that I don’t categories people. This was only part of this discussion and I am making gross generalisations. 
  
  Taking a step back, according to a diagram on the presentation on cultural types, between Reactive and Linear-active types, nationalities that more closely match Reactive type include Northern-European countries (U.K., Sweden, Finland) while Southern-Asian countries match Linear-active type. Interestingly enough, this correlates more or less with the places I have lived in (China and France).
  
  I can also say with confidence that France, my country of origin, is well placed between Linear-active and Multi-active types. From experience, French people have more difficulty summarising things and I found that true for myself as well. 
  
  French people explain things with a curtain of bureaucratic and redundant curtesy. While I like helping others, I am afraid of explaining things with a lack of manner, what would another French person expects. As a results explanations are often long and the point necessarily takes time to get across at times.
  
  Additionally, being a student slowly nearing professional life, I have learned to rely on others more frequently during projects. Among other things under the [ACM Code of Ethics](https://www.acm.org/code-of-ethics) including 1.2 Avoid Harm and 1.5 Respecting others, being 1.3 Honest and Trustworthy more perhaps the most important characteristics in letting others rely on you. 
  
  One of the things I improved upon is my transparency during stand ups. Occasionally, I am unable to complete certain tasks on time. Mentioning this clearly to others during meetings is crucial in letting others know not only how much work is needed still but also how much you can handle alone as a developer. Since the project relies on Agile Scrum, this kind of setbacks are lenient after all.
  
  <br />  
</details>


<details>
  <summary>LO6: Requirements and Design</summary>
  <br />

> Multipletypes of test techniques: You apply user acceptance testing and stakeholder feedback to validate the quality of the requirements. You evaluate the quality of the design (e.g., by testing or prototyping) taking into account the formulated quality properties like security and performance.

  Given that this project was conducted using Agile Scrum, requirements may change and may be added according to feedback and progress of the project. There were times where I had the opportunity with the team to formulate prototypes for requirements that needed rethinking for the client. 

  For instance, one such occasion presented itself when customer session management need implementation. In an exchange email, we discussed on how session initialization was going to be made:
  
  Email sent:
  <p align="center">
    <img src="https://i.imgur.com/V8b8wGw.png" width=500 />
  </p>
  
  Response:
  <p align="center">
    <img src="https://i.imgur.com/Xm4j0Q7.png" width=500 />
  </p>

  On the subject of UI design, I conducted UX testing research directly on my website's design using a tool called Hotjar. With the addition of datasets, this tool generated these heatmap:
  
  <p align="center">
    <img src="https://i.imgur.com/38AUB0l.png" width=400 />
    <img src="https://i.imgur.com/bMkoB62.png" width=400 />
  </p>
  
  Those designs were brainstormed and conceptualised using Figma:
  
  <p align="center">
    <img src="https://i.imgur.com/ADfZeXQ.jpg" width=400 />
    <img src="https://i.imgur.com/b8atQSi.png" width=400 />
  </p>
  
  More information regarding my findings can be found on the research [here](https://github.com/greffgreff/semester-content/blob/main/ux-testing.md).
  
  Finally, in regards to software architectural design, I made a C4 model (level 2) for my individual project:
  
  <img src="https://i.imgur.com/34Nvkd4.png" />
  
  <br />  
</details>


<details>
  <summary>LO7: Business processes</summary>
  <br />

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

  <br />  
</details>


<details>
  <summary>LO8: Professional</summary>
  <br />

  From the start, the work was divided amongst ourselves depending on our already extensive or limited knowledge on a particular field. The idea behind this is to ensure that everyone can work confortably on the group project and focus on the things we don't know on the individual project.

  Given that some team members had already worked on our choosen backend (ASP.NET) and that I felt must confortable working on the frontend (with ReactJS), I decided to work on it. 

  This also gave me the opportunity to help other members regarding frontend development for their individual projects, including how to strucutre a project, best practices, etc. On multiple occasions, I made PRs to other group memebers in an attempt to help and improve their project's frontend. One such example can be found on [this PR](https://github.com/Sawaholding/RWS-FrontEnd/pull/7), where I refactor some code to follow conventions along side styling the project.

  I worked exclusively on the frontend for the group project, however, communication between the frontend and the backend was tightly maintained all throughout the project in standups and standdowns. It is a fullstack application conducted in Agile Scrum afterall.

  > I offset my lack in involvement in the backend in the group project with my individual project, where I spent most of my time building a restful API using Spring Boot.
  
  Additionally, using the DOT framework, I've done research on things related to the context of my project, inlucing research on [JWT](https://github.com/greffgreff/semester-content/blob/main/jwt.md) where I used literary study, pro and con comparisons, and available product analysis as research methods, and [UX testing research](https://github.com/greffgreff/semester-content/blob/main/ux-testing.md) where I used basic data analysis, observation, and usability test.

  Also, communication between various stakeholders in the project was done in a professional manner. Please see email under "Requirements and Design" as proof.
  
  <br />  
</details>
