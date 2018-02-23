# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Kaggle Competition - Starter

## Introduction

Welcome to your first week of work at the Disease And Treatment Agency, division of Societal Cures In Epidemiology and New Creative Engineering (DATA-SCIENCE). Time to get to work!

Due to the recent epidemic of West Nile Virus in the Windy City, we've had the Department of Public Health set up a surveillance and control system. We're hoping it will let us learn something from the mosquito population as we collect data over time. Pesticides are a necessary evil in the fight for public health and safety, not to mention expensive! We need to derive an effective plan to deploy pesticides throughout the city, and that is **exactly** where you come in!

## Dataset

The dataset, along with description, can be found here: [https://www.kaggle.com/c/predict-west-nile-virus/](https://www.kaggle.com/c/predict-west-nile-virus/).

**This is also where you will be submitting your code for evaluation**. We will be using the Kaggle Leaderboard to keep track of your score. The leaderboard uses roughly 30% of the dataset to score an AUC (Area Under Curve) metric. [You can read more about the scoring metric here](https://www.kaggle.com/wiki/AreaUnderCurve).


#### Group Project Recommendations

This project will be executed as a group.
- Set up a GitHub repository.
- Create a Trello board/a Google sheet with tasks assigned to individual members of your team to keep the project organized. (Please tag whoever in your team is taking the lead on any part.)
- Brainstorm a project roadmap.
- Explore the data.
- Produce a model and make predictions for where the Department of Public Health should be spraying.
- Submit your predictions to Kaggle and get an AUC score.  You can submit these as many times as you want to Kaggle, but there is a limit of 5 submissions per day.  Be intentional with your submissions!

## Deliverables

**GitHub Repo**

1. Create a GitHub repository for the group. Each member should be added as a contributor.
2. Retrieve the dataset and upload it into a directory named `assets`.
3. Generate a .py or .ipynb file that imports the available data.

**Project Planning**

1. Define your deliverable - what is the end result?
2. Break that deliverable up into its components, and then go further down the rabbit hole until you have actionable items. Document these using a project managment tool to track things getting done.  The tool you use is up to you; it could be Trello, a spreadsheet, GitHub issues, etc.
3. Begin deciding priorities for each task. These are subject to change, but it's good to get an initial consensus. Order these priorities however you would like.
4. You planning documentation (or a link to it) should be included in your GitHub repo.

**EDA**

1. Describe the data. What does it represent? What types are present? What does each data points' distribution look like? Discuss these questions, and your own, with your partners. Document your conclusions.
2. What kind of cleaning is needed? Document any potential issues that will need to be resolved.

**Note:** As you know, EDA is the single most important part of data science. This is where you should be spending most of your time. Knowing your data, and understanding the status of its integrity, is what makes or breaks a project.

**Modeling**

1. The goal is of course to build a model and make predictions that the city of Chicago can use when it decides where to spray pesticides! Your team should have a clean Jupyter Notebook that shows your EDA process, your modeling and predictions.
2. Conduct a cost-benefit analysis. This should include annual cost projections for various levels of pesticide coverage (cost) and the effect of these various levels of pesticide coverage (benefit). *(Hint: How would we quantify the benefit of pesticide spraying? To get "maximum benefit," what does that look like and how much does that cost? What if we cover less and therefore get a lower level of benefit?)*
3. Your final submission CSV should be in your GitHub repo.

**Presentation**
* Audience: You are presenting to members of the CDC. Some members of the audience will be biostatisticians and epidemiologists who will understand your models and metrics and will want more information. Others will be decision-makers, focusing almost exclusively on your cost-benefit analysis. Your job is to convince both groups of the best course of action in the same meeting and be able to answer questions that either group may ask.
* The length of your presentation should be about 20 minutes (a rough guideline: 2 minute intro, 10 minutes on model, 5 minutes on cost-benefit analysis, 3 minute recommendations/conclusion).  Touch base with your local instructor... er, manager... for specific logistic requirements!

---

**Your project is due at 10:00 AM EST/9:00 AM CST on Friday, March 9.**

### **Competition Evaluation**

The Kaggle competition should be evaluated on the following 4 points:

1. **AUC Scoring**: A clear winning group will be determined based on the AUC Scoring performed by the Kaggle Leaderboard. This is not to say that the winning group's work was the best submission. Remember, just hitting a benchmark is not enough to determine success; the following points are just as important if not more so.

2. **Clearly documented observations**: Students should have some log, whether it is a markdown file, text file, or iPython notebook, describing the observations and decisions they made along the way. This should be submitted to your instructor prior to your final presentation.

3. **Code**: All of your models, pipelines, cleaning techniques, and transformations should be properly coded and documented. Syntax is important, as data scientists are often tasked with building products that will be collaborated upon or maintained by other engineers. It is also important that no mistakes were made while pipelining data. If any data points were corrupted, the results are useless.

4. **Presentation**: Your presentation is expected to be client facing. Describe your data and approach as if your client is in front of you. This includes explaining the decisions made, the means by which you evaluated your decisions, and visualizations to support the story you are telling. This is a storytelling exercise, so be sure to set up, explain, and summarize your work clearly.

---


### Project Feedback + Evaluation

Data science is a field in which we apply data to solve real-world problems. Therefore, projects and presentations are means by which we can assess your ability to solve real-world problems in a data-driven manner.

Your final assessment ("grade," if you will) will be calculated based on a [topical rubric](https://docs.google.com/spreadsheets/d/19k8OZ42xzr7v9GDv2IUyD175yGjJlwTNokcufwX9Ago/edit?usp=sharing). For each category, you will receive a score of 0-3. From the rubric you can see descriptions of each score and what is needed to attain those scores. Make sure you look at the "Rubric P4" tab of the [spreadsheet](https://docs.google.com/spreadsheets/d/19k8OZ42xzr7v9GDv2IUyD175yGjJlwTNokcufwX9Ago/edit?usp=sharing).
