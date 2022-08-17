---
date: 2021-05-26
description: "Creating a web-based tool for age prediction."
featured_image: "/images/project-3-0.jpg"
tags: ["R", "Shiny"]
title: "Project 3: Abalone"
---

- A non-machine learning study by Nash et. al gave rise to the popular abalone dataset. 
- When used in a machine learning context, the goal is generally to construct a model which is able to predict the number of rings on the body of given abalone. 
- This measure is useful since the number of rings can be used to estimate abalone age, adding 1.5 to the number of rings gives the age. 
- It is highlighted in the dataset description that such machine learning models may be useful to scientists involved in abalone research since it will allow them to predict age without performing the labourius task of 'cutting the shell through the cone, staining it, and counting the number of rings through a microscope'. 
- The features used in the dataset are easy to obtain which can allow for a mobile app to accompany field researchers involved in abalone research. 
- Therefore the aim of this project was to create such an app which can be of use to predict abalone age or at the very least give a decent approximation of age.

{{< figure src="/images/project-3-1.PNG" title="" >}}

Links:

- [Abalone (UCI)](https://archive.ics.uci.edu/ml/datasets/Abalone)
- [RPubs notebook](https://rpubs.com/davidmh/Abalone_Age)
- [R Shiny web app](https://davidmh.shinyapps.io/abalone_age_predictor/)

How to use the Shiny app?  
Download 'shinytestdata.csv' from GitHub page for the project (link below) which is under the 'data' directory. Alternatively you can test it out using your own data simply by grabbing a subset of the UCI Abalone dataset, ensuring that it fits the format of the sample file. Once you have a file with data, you can interface with the app.

{{< figure src="/images/project-4-3.PNG" title="" >}}

View the project on **Github**:  
[David-dmh/Abalone](https://github.com/David-dmh/Abalone)

