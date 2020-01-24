hipages Full Stack .Net Engineer Tech Challenge
==========================================
Welcome to the hipages Full Stack .Net Engineer Tech Challenge!  The purpose of this challenge is to help us assess your technical skills.  We know that you have limited time to devote to this task and may not be able to provide the as complete solution as you would given more time, so we suggest you focus on the core requirements first, then any additional features if you have time left over.

## The Task
Your task is to create a lead management UI for a tradie.  
This should be presented as a single page application (SPA) using a modern JS framework of your choice, backed by .Net Core Web API and using database of your choice (SQL or NoSQL).

### Invited Tab
The first view you need to create is the **Invited** tab, which contains all leads in the **new** status.
![Invited Tab](/invited_tab.png?raw=true "Invited Tab")

As you can see in the screenshot, each lead is a card in a list which contains the following pieces of information:
* Contact first name
* Date created
* Suburb
* Category
* ID
* Description
* Price

Along with that information you can see two buttons: **Accept** and **Decline**
* Upon clicking on **Accept**, the lead must be updated to the **accepted** status in the domain/database. If the Price is higher than $500, then 10% discount needs to be applied to the price. 
After acceptance, the system needs to send email notification to sales (sales@techtest.com), note that you don't need to send the actual email, you can create a fake email service that does nothing or simply create a text file instead.
* Upon clicking on **Decline**, the lead must be updated to the **declined** status in the database

### Accepted Tab
The second view you need to create is the **Accepted** tab, which contains all leads in the **accepted** status.
![Accepted Tab](/accepted_tab.png?raw=true "Accepted Tab")

As you can see in the screenshot, the lead cards follow a similar format and contain some additional data:
* Contact full name
* Contact phone number
* Contact email

### Notes
* For the icons in the UI, you can use something like font-awesome or SVG icons, whatever you choose.
* There are jobs already loaded into the database using a script executed by docker-compose as sample you can use

## Getting Started
We have provided a bit of boilerplate code to create sample mysql data that you can use to get started.  You are **not** required to use this boilerplate, so feel free to throw it all away and start fresh if you prefer.

The boilerplate code assumes you have Docker running on your machine.  If you do not, they offer easy to install binaries ([Mac](https://docs.docker.com/docker-for-mac/install/)) ([Windows](https://docs.docker.com/docker-for-windows/install/)).

From the root of the project, run `docker-compose up -d`
* You should now have the UI running at https://localhost:8091/ or http://localhost:8090
* You should also have a MySQL database running at localhost:3306
    * The username is `root`
    * The password is `hipages`
    * The database is `hipages`
* Note that SPA (UI) project has not been created in this boilderplate as it might vary depending on the framework of choice (Ideally React or Angular).

If at any point you want to refresh the database, you can stop the Docker containers (`docker-compose down`) and start them again

## Deliverables
### Required
* .Net Core 3.1 Web API to provide RESTful service
* SPA (React, Anular or any modern framework of your choice)
* Database (SQL or NoSQL)

### Nice to Have (Advanced)
* CQRS - Ideally using MediatR
* Following DDD principles for business logic (Domain Driven Design)

### Nice to Have (Super Advanced)
* Use EventSourcing

## Evaluation Criteria
Evaluation is based on clean coding skills, design & problem solving skills and the use of modern technologies.
    
## Submission
Please document your solution in the SOLUTION.md file.  This should explain why you've made the design choices that you have and clarify anything you feel isn't obvious.  Feel free to also include what else you would have done given more time.

**Please include instructions on how to run your app if it is not using the boilerplate provided.**

Once completed, please upload your solution to a public Github repo and share the link with **niclaswessblad@hipagesgroup.com.au**
