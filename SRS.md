<p align="center">
Universidad Autónoma de Ciudad Juárez</br>
División Multidisciplinaria de Ciudad Universitaria</br>
Departamento de Ingeniería Electricidad y Computación</br>
</p>
<br>
<p align="center">
<img width="270" height="270" 
  src="https://github.com/RequirementEngineering/ch-re-STDBrando/blob/master/Images/Escudo%20uacj%202015-color-sin%20fondo.png">
</p>
<br>
<p align="right">
Desarrollo de requisitos de software</br>
</br>
Chemical labels (SRS) </br>
</br>
Rafael Ernesto Cabrales Corral, 1599060</br>

</br>

</br>
May 2019
</p>

# Table of contents
1. [Introduction](#Introduction)
    - [Purpose](#Purpose)
    - [Scope](#Scope)
    - [Definitions, acronyms, and abbreviations](#Definitions-acronyms-and-abbreviations)
    - [References](#References)
    - [Overview](#Overview)

2. [Overrall description](#Overall-description)
    - [Product perspective](#Product-perspective)
     -[Product Functions](#Product-Functions) 
    -[Uses Cases](#Uses-cases)
    - [User characteristics](#User-characteristics)
    - [Constrains](#Constrains)
    - [Assumptions and dependencie](#Assumptions-and-dependencie)
3. [Specific requirements](#Specific-requirements)
      - [Functional requirements](#Functional-requirements)
       - [Non functional requirements](#Non-functional-requirements) 
    - [General use case](#General-use-case)
    - [External Interfaces](#External-Interfaces)
    - [Logical Data Base requirements](#Logical-Data-Base-requirements)
3. [Appendix](#Appendix) 
   - [Elicitation process](#Elicitation-process)
   - [Business Managment Process](#Business-Process-Diagrams)

---
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
[1][Norma Oficial Mexicana NOM-018-STPS-2015, Sistema armonizado para la identificación y
comunicación de peligros y riesgos por sustancias químicas peligrosas en los centros de trabajo.](https://www.ilo.org/dyn/natlex/docs/ELECTRONIC/101271/121935/F299513823/NOM-018-STPS-2015.pdf)
## Overview
The rest of this document includes two other chapters as well as an appendix annex.
 The next chapter will talk about the general description of the system as well as its functionality and perspective. The interaction between the interested parties and the interface of the system, the level required to use it and manage it efficiently. a review will be given to the rejections of the systems as well as the assumptions and dependencies, emphasizing in this last position that the level of the system will require the intervention of specified users that configure the system as required in case of updates in the use mode according to look like the company.
 
In the last chapter we will review the specified requirements, as well as a description of the different interfaces of the system, different techniques will be used to obtain the requirements in a more accurate way, adapting to the different users for which the software will be available, during the same Chapter will review the prioritization of the requirements. The appendices at the end of the document include all the results of the prioritization of requirements and a launching plan based on them.
# Overall description
## Product perspective
Chemical.Labels is aimed at different employees whose area of work is related to the handling of chemicals within the maquiladora, so software is needed to facilitate and speed up the labeling process and obtain information related to the handling of said products. the software must be easy to learn to use, so that the implementation and start using as soon as possible, it is intended to be an independent and distributed system with the use of a database, it will be executable in Windows with the possibility of being confirmed for another operating system in case it is required. 
## Product functions
This system is made up of two main functions, the first one that focuses on generating labels according to the information provided by the user, being supported by a database which will contain all the information necessary for the handling of high risk products, focusing on the chemicals and the regulations that regulate it, so when a user enters the type of chemist or product with which they are working as well as some extra specifications that are needed the software will search within the database for all the information regarding that product , likewise there will be two options to proceed in the program, the first one will generate a label for said chemical, to also print it if it is the case, the second option will lead to print a report on how the chemical should be handled, the reports will be handled by levels: for newly admitted personnel and advanced staff in the subject.

## Uses Cases

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
## Functional Requirements

The software will allow the user to enter information that will be divided into fields (being keywords, specific details about the chemicals that are searched) for the location of the required data.
Also entering the system as an administrator you can update the stored data, you can delete, modify or create new data, you can also configure the details of the documents that are generated (labels and reports).
The user can send to print the documents when ready.

## Non-functional requirements
- It connects to a database.
- The system uses a database to compare the data provided by the user and thus obtain the information required to generate a label or report as the user wants.
- The system joins the data found in the database to create a label, using as a basis the information of company regulation[1] thus generating a test image for the user to confirm the label.
- The system joins the data found in the database to create a report about the chemical of interest, thus joining all the regulations found in NOM-018-STPS-2015 [1]. Following an order:

1.- Basic information of the chemical

2.- Advetences

3.- Health risk

4.- How to handle the chemical

## General use case
![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/Use%20case/Casos%20de%20uso%20general.jpg)


![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/Use%20case/tabla%20general.jpg)

## Specific use case
### LOGIN
![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/Use%20case/admin-login.jpg)

![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/Use%20case/tabla%20admin-login.jpg)

![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/Use%20case/empleado-login.jpg)

![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/Use%20case/tabla%20empleado-login.jpg)

## CONSULTAS

![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/Use%20case/Consultas%20admin.jpg)

![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/Use%20case/Tabla%20cons%20admin.jpg)

![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/Use%20case/Consultas%20empleado.jpg)

![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/Use%20case/Tabla%20cons%20empleado.jpg)

## DOCUMENTOS

![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/Use%20case/documentos%20administrador.jpg)

![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/Use%20case/tabla%20doc%20admin.jpg)

![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/Use%20case/documentos%20empleado.jpg)

![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/Use%20case/Tabla%20doc%20empleado.jpg)

## CONFIGURACION

![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/Use%20case/configuracion%20administrador.jpg)

![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/Use%20case/Tabla%20conf.jpg)

## External Interfaces
Here is how the system works for each menu:
* Login Menu: Once the program is started, the first screen will be displayed, which will have an option to continue depending on the administrator or employee. In case of being an administrator, a password will be requested.
* Main Menu: The main menu will have a series of options and text boxes to specify the query: 
In the event that you are logged in as an administrator apart from having the text boxes and options to specify the query, you will have an extra button to go to the program configuration screen. Within the specifications for the query will have two buttons to track one of the following two screens. One will take you to the label generation screen and the other will take you to the report generation screen.

* Label Screen: In this screen the image will be shown in the first instance showing an example of what the label would be according to the query made in the previous screen, you will have several options, you can go back to the previous screen to modify the query, accept the label and go to the print screen, generate a report of the created label.

* Report screen: Within this screen an example of the generated document will be shown based on the query of the previous screen, it will contain several options. You can print the report by going to the print screen, return to the previous screen to modify the query.

* Printing screen: In this screen you will see several options to modify the printing that will be made (either of the label or a report). The number of prints can be modified, if it will be done in black and white or in color, and to which printer the printing will be sent.

* Configuration screen: Within this screen the options are presented for the administrator to modify as required the operation of the software. Having thus a series of options to modify the relation of the labels and their form of impression, as well as the nature of the document (type of letter, size, margin, sangria, etc.)
 Within said screen you will have the option to modify the information of the database, being able to add, delete or modify data as required.

## Logical Data Base requirements
The system connects with a database containing three tables that will be described in the following:

*Label table* contains the following attributes:

* chemical code(foreing key)

* Warning code(foreign key)

* symbol

* word of warning

* indication of danger

* prudence advice code(foreing key)

* Personal protective equipment symbol

*chemical tables*

* Warning code(foreign key)

* prudence advice code(foreing key)

* chemical code(primary key)

* name

* physicochemical properties

*prudence advice* 

* prudence advice code(primary key)

* description 

*Warning*

* Warning code(primary key)

* indication of danger

* kind of danger

* category of danger

All the data described here that are required for the creation of the labels are based on the norm-018-STPS-2015.[1]

## Appendixes
### Elicitation Process

The process with which the client's requirements for the software were obtained was through an interview with the head of the area where the system will be used. First, he gave a general outline of how he would expect the program to be and the main things he needed so that he would be optimal in the work area.

#### General view:
The client was looking for reliable software when looking for information and as simple as possible so that employees could understand its operation without taking much time.
He described it as "a direct use program that may be able to generate labels and reports without the need to take a lot of time" (Anonymous, 2019)
It was requested that the main function of the software was to be able to generate labels to mark chemists following the regulations that are required to the company, likewise power from the application to send the impression of said labels.

#### Conclusions:

Based on general questions made to the client, different conclusions could be reached in the expected areas.

 - The information search method to generate the documents has to be simple and with general fields to fill to speed up the process.
 - To be able to generate both labels and reports of the chemicals that will be sought.
 - The client requests that an administrator can be had to configure details of the documents.
 - Having a database that contains the information of the chemicals that are generated, the administrator can modify it, adding information, modifying the existing one and eliminating the obsolete one.
 - The administrator requires a password to be able to enter the configuration screen.
 - The program connects with a printer to send to print the files, in the same way you can download them to print from the computer's method.
 
 At the end, what was said with the client was reviewed so that the whole scheme could be confirmed, other participants were taken (potential actors of the system) but it was informed by the area manager that a meeting had been made internally, according to what would be asked for. the system, she being the spokesperson.
 
 ### Business process diagrams.

 ![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/BMD/BMD%20general.jpg)
 
 ##### Configuration diagram.
 ![Alt text](https://github.com/RequirementEngineering/ch-re-Rafael159960/blob/master/BMD/diagrama%20de%20configuracion.jpg)
 
 
## Index
