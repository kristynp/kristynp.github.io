---
layout: post
title:      "Verily Projects CLI"
date:       2019-11-26 04:37:10 +0000
permalink:  verily_projects_cli
---


This gem allows the user to read descriptions of the projects that are currently being worked on by Verily. 

It shows a list of the current projects and allows the user to select from a list to retrieve information about the chosen project. After the description is given, the CLI will ask the user whether they would like more information on any of the other projects. If so, it will show the list again and allow for a new selection. When the user no longer wants more information, the CLI will wish them a good day, and the program will be completed.

Structure

This CLI gem is comprised of three classes within the VerilyProjects module. The CLI class interfaces with the user and controls the flow of the program. The Scraper class handles scraping data from the verily website using Nokogiri and Open Uri. The Project class creates and tracks project objects from the scraped data.

Function

When the program begins, a new instance of the CLI class is initialized, the user is welcomed, and a method is called to get_projects.  This get_projects method assigns the @projects variable to the return value it receives after it calls the self.all class method in the Project class. That class method is responsible for checking whether the @@all variable that tracks all projects is empty. If it is empty, then the method will call the scrape_projects method in the Scraper class to scrape the verily projects page and properly format it into an array of project names. It will then iterate through each of these items in the array, and do some additional removal of whitespace. For each item that is not empty, it will call on the Project class to initialize a new Project with the attributes of name and info. Initializing a new project will also call the Save method, which will save the project in the @@all array. The CLI class will then call the list_projects method, which will iterate through the @projects variable, list the name of each project next to a number, and ask the user to select a number corresponding to the project they would like more information on. The get_user_project method will call the valid_input? method to check whether the number is a valid choice from the list, and if so, it will call the show_info_for method for the chosen project. The show_info_for method will call the scrape_info method in the Scraper class to scrape the project page for the chosen project and assign the information to the info attribute of the project passed in. The show_info_for method will then display the value of the info attribute. The CLI will then ask for the user to choose whether they would like information on another project using the get_continue_response. If the user responds with yes, it will loop back to the beginning of the program, just after the welcome. If not, it will wish them a great day, and the program will end. 

Creation Process

I was very happy with this assignment. While I felt overwhelmed with starting from scratch for the first time, I also felt like there was adequate resources given for the initial and as yet unfamiliar setup of the gem, and it gave me more confidence in using resources that are publicly available. I recognize that this particular CLI is not adding any remarkable value to the world, since you can find the info fairly easily by using the Verily website, but it gives me far more confidence in my ability to build somthing on my own that is useful and creates value in the future. 

I enjoyed the process of stubbing out the code and making notes about how I wanted the flow to go, so that I could simply elaborate on each point to start putting it together. 

This was the first time that I used fake data to get methods to be functional before adding more complexity with scraping new data and passing it in. I really liked how quickly that makes everything fall into place. I also started to get into the flow of creating the code you wish you had, then building through the errors. It was exciting to see it starting to come together. Though I know this is a simple CLI, I feel proud of it, and I enjoyed the process.




