# Numer.AI Tournament Submission and Automation Walkthrough

# Installations

Just do a `pip install -r requirements.txt` with the provided requirements file, and you're good to go!

# Project Motivation

Three major reasons for me creating this repository:
* Explore the numer.ai competition from as fresh of a perspective as possible
* Automate the numer.ai competition in a new way which does not require AWS (Lets go IBM Cloud!)
* To serve as a Capstone project for Udacity 😜 **

[Numer.ai](numer.ai) is an ongoing open source data science tournament which accepts weekly submissions from participants. The project aims to be "The World's Last Hedge Fund" by crowd-sourcing the technical work to a community of data scientists. Data scientists can participate in the competition to either strictly work on their skills , or they could also invest real funds into the performance of their predictions.

It should be noted that directly from their home page, a link is available for an example package of not only the tournament data, but also scripts for example model building, data exploration, and tips and analysis to help users get started. If you're interested in some more advanced material and do not wish to automate through IBM Cloud, I recommend checking out their available work from the [official repository](https://github.com/numerai)

Within this repository is a novel solution to automate the numer.ai workflow using IBM Cloud services at no cost to the users. I hope this motivates more users to use the IBM platform to automate their workflows. In the future I aim to automate more than just submissions; things like automatic model optimization for specific metrics sound attractive and doable. Besides automating the workflow for this competition, I also expand on the problem itsself, and conduct deep-dives into all aspects of data exploration, visualization, and modeling. This project will continue to evolve and adapt with the data, and for future updates, I'll continue to refine the automation process.

# File Descriptions
* notebooks folder
  * `Exploratory Data Analysis` - This file contains some preliminary data exploration and visualization for the competition.
  * `Model_Building` - This file contains some functions I used in the preliminary stages of model building. I explore mdoel performance, define the evaluation metrics, and compare results of many different ML algorithms in this notebook. By the end of this notebook I save a best-performing model.
  * `Model Scoring and Prediction Upload Job` - This notebook serves as a template which can be adapted to whoever's looking to automate their work through IBM cloud. It covers every step of the competition, from importing new data, setting up an API connection, creating predictions, uploading them to the competition, and some additional useful commands for understanding how the competition's ecosystem works.

# How to work with the Project

To begin, you will need to have a [numer.ai](numer.ai) account. Go sign up for one, go to your account settings, and create a model. While you're there, create a public and private API Key and save the credentials somewhere, you'll need them shortly!

Most of the notebooks contain typical data science work for solving a problem. These notebooks have their own readme's in the notebooks folder, so explore there for more in-depth analysis about what was done. In this readme I'll focus on creating  a step by step guide to automate the process of actually participating in this contest using IBM cloud.

An end-to-end solution can be implemented solely from the third notebook. To successfully automate your solution, here is a quick list of steps.
1. Download the Deployment notebook from the notebooks folder


2. Sign up for an [IBM Cloud Account](https://cloud.ibm.com/login)
<img src="assets\2.IBM_Cloud_Signup.png" alt="cloud_signup" width="200" height="200">

3. Create a resource for Watson Studio
<img src="assets\3.Watson_Studio_Resource.png" alt="watson_studio" width="200" height="200">

4. Create a new project space with Watson Studio
<img src="assets\4.New_Project.png" alt="new_project" width="400" height="200">

5. Create a custom software specification with the numerapi added
5.1
<img src="assets\5.1.custom_software_spec.png" alt="custom_software1" width="600" height="400">
5.2
<img src="assets\5.2.custom_software_spec.png" alt="custom_software2" width="600" height="200">

6. Upload the above notebook to your project space
<img src="assets\6.Upload_Notebook.png" alt="upload_notebook" width="400" height="300">

7. Set up a notebook job for automatically running the notebook
<img src="assets\7.notebook_job.png" alt="notebook_job" width="600" height="400">

8. Pat yourself on the back , you're all set!

# Licensing, Authors, Acknowledgements, etc.

All notebooks and IP are covered under their respective licensing

Author - David Cruz

Acknowledgements to the IBM Data Science Elite Team and the Numer.ai Community for all of the different contributions made!


** After passing the Udacity Capstone, I'll continue to update this repository with much more community-driven content and advanced techniques.
