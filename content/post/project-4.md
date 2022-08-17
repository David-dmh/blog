---
date: 2021-09-19
description: "Email scheduler for international public holidays."
featured_image: "/images/test51_.jpg"
tags: ["Python", "Django"]
title: "Project 4: Holiday ETL"
---

- Calendar-based Application Programming Interfaces (APIs) are used extensively in industries such as travel, banking, finance and supply chain.
- Looking to familiarise myself with the ETL (Extract Transform Load) process, these APIs inspired me to create an app for automation of extraction and delivery of calendar data to end-users.
- With automated information retrieval from the API service, the tedious process of working with the API directly is avoided.
- Django and APScheduler were primarily used to schedule emails from the [nager.date](https://date.nager.at/) open-source API.
- The app is configured to alert subscribers of public holidays at 9:00 daily (host time zone). The Django admin user interface also allows customised newsletter-type alerts to be sent to subscribers.

How to use the web app?
- Create new folder and virtual environment.
- Clone the HolidayETL git repository.
- Pull and save API [Docker image](https://hub.docker.com/r/nager/nager-date) and place in folder named *nager-date API Docker image/* within *jobs/*. This is done by navigating to the newly created folder and running the two commands below:  
1) `docker pull nager/nager-date`  
2) `docker save -o nager-date.tar <repo>:<tag>`  
- Sign-up for a free [Sendgrid account](https://sendgrid.com/) and authenticate a sender. Then redefine the FROM_EMAIL and SENDGRID_API KEY variables to your email and key in settings.py
- If desired, use django-heroku to prepare production app taking note to hide personal data like API keys beforehand.

Keeping holiday data updated:

Once the app is deployed it will update holiday related data on New Year's Day. In order to sucessfully do so, the self-hosted API service needs to be running. This is accomplished by starting the Docker daemon before the new year and executing the following two terminal commands. The last command also runs Swagger UI to be able to interact more easily with the API if desired:  
1) `docker load --input nager-date.tar`  
2) `docker run -e "EnableCors=true" -e "EnableIpRateLimiting=false" -e "EnableSwaggerMode=true" -p 80:80 nager/nager-date`  

{{< figure src="/images/project-4-0.png" title="" >}} 

{{< figure src="/images/project-4-1.png" title="" >}}

View the project on **Github**:  
[David-dmh/HolidayETL](https://github.com/David-dmh/HolidayETL)
