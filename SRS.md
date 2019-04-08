# Introduction
## Purpose
The purpose of this SRS document is describes the software requirements for "Chemical.Labels".
Software that allows the user modify, create and print labels based on safety regulations within maquilas for the handling for chemicals. Adapting to the change of security regulations. Likewise it seeks to have a database that has the necessary information for the handling and use of chemical products as well as some other type of product that needs special handling.
Having thus two types of interface, the first one to generate the labels as required and the second one that has a library with all the risk products that are handled within the company, being an interface accessible to employees of different degrees.
## Scope
Chemical.Labels is a web-based which seeks to facilitate the handling of specific labels for the handling of chemicals, using a database to contain information on the regulations and chemicals that can be used within the maquila, as well as the specifications that must be included in the label according to the risk of handling or type of chemical. 

Using a database connected to an external server that will be updating information about the chemicals, the application will be installed inside the computers of the maquiladora in a local way, easy-to-use interface. The software needs internet conection for to update the information of news safety regulations as well as the information for new chemists that could have new functionalities within the way to treat in the safety of their handling. 

The software is exclusive for maquiladoras and companies that require the use of labels in their handling of chemical products with safety rules, seeks to obtain a database that beyond the generation of labels may have information of easy access to the handling of chemicals and other products with special management requirement.
## Definitions, acronyms and abbreviations
Maquiladora: factory, assembly plant.
Chemical product: Products that are formed based on chemical reactions.
High risk: chemicals that contain a great risk to human or environmental health.
## References
## Overview
The rest of this document includes two other chapters as well as an appendix annex.
 The next chapter will talk about the general description of the system as well as its functionality and perspective. The interaction between the interested parties and the interface of the system, the level required to use it and manage it efficiently. a review will be given to the rejections of the systems as well as the assumptions and dependencies, emphasizing in this last position that the level of the system will require the intervention of specified users that configure the system as required in case of updates in the use mode according to look like the company.
 
In the last chapter we will review the specified requirements, as well as a description of the different interfaces of the system, different techniques will be used to obtain the requirements in a more accurate way, adapting to the different users for which the software will be available, during the same Chapter will review the prioritization of the requirements. The appendices at the end of the document include all the results of the prioritization of requirements and a launching plan based on them.
# Overall description
## Product perspective
Chemical.Labels is aimed at different employees whose area of work is related to the handling of chemicals within the maquiladora, so software is needed to facilitate and speed up the labeling process and obtain information related to the handling of said products. the software must be easy to learn to use, so that the implementation and start using as soon as possible, it is intended to be an independent and distributed system with the use of a database, it will be executable in Windows with the possibility of being confirmed for another operating system in case it is required. 
## Product functions
This system is made up of two main functions, the first one that focuses on generating labels according to the information provided by the user, being supported by a database which will contain all the information necessary for the handling of high risk products, focusing on the chemicals and the regulations that regulate it, so when a user enters the type of chemist or product with which they are working as well as some extra specifications that are needed the software will search within the database for all the information regarding that product , likewise there will be two options to proceed in the program, the first one will generate a label for said chemical, to also print it if it is the case, the second option will lead to print a report on how the chemical should be handled, the reports will be handled by levels: for newly admitted personnel and advanced staff in the subject.

Chemical.Labels should be based on the following use cases:

|Class of use cases  |     Use cases    |    Description   |
|--------------------|:----------------:|:-----------------:|
| Use case related to installation | Installation | Creates and initializes working files |
| System authorization | Login | choose the form in which the program will be executed. To configure or query |
| | Change password | change the password for the administrator |
|Use cases related to query | create Queries | specify the product to review |
| | modify the query | change the specific data of the product search |
| | new query | resets the search fields of the query to create a new one |
|Use case related to database | connection | Connect to database |
| | find information | look for the query within the database |
| | enter new information | the administrator can enter new information into the database as required |
| | modify information | the administrator can modify the information found in the database |
| | Delete information | the administrator can delete information that is in the database as required |
| Use case related to create documents | create a report | A report based on the query is created |
| | create a label | a label based on the query and the regulations of the product sought |
| Use case related to print | print the report | the previously created report is printed |
| | print the label | the previously created label is printed |
| Cases of uses related to the configuration | configuration of the format of the documents | The administrator can specify the format in which the report will be created (typeface, spacing, etc.) |
| | configuration of the format of the labels | The administrator can specify the format in which the labels will be created |
## User characteristcs
Regarding the characteristics of users will be two types to which the system is directed, in the following table are described:

| Actors | Description |
|:----:|:------------|
| Administrator | the administrator will have access to various functions within the system that will allow him to modify the information within the database for which a password will be required. The administrator should be instructed in the operation of the program, and how it should be configured. You should have knowledge about the products handled within the maquiladora, as well as the employees that will have access to the system. |
| Employee | The employee will have access to only the main functions of the system, being these the query of reports, generate labels and print these things. For the use of these functions, only the base knowledge (principally names and relationships of treated chemicals) will be required on the products that are handled. |
## Constraints
* 
## Assumptions and dependencies
### Assumptions
* Assumed that the software system has no database limit.
* it is assumed that the system will be able to generate documents based on the configuration of the administrator.
### Dependencies 
* the system requires an internet connection to update the database and make your queries.
* The data must be entered correctly in the query to find the match within the database.
# Specific requirements
## External Interfaces
Here is how the system works for each menu:
* Login Menu: Once the program is started, the first screen will be displayed, which will have an option to continue depending on the administrator or employee. In case of being an administrator, a password will be requested.
* Main Menu: The main menu will have a series of options and text boxes to specify the query
## Appendixes
## Index
