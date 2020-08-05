# WizAud - the audit, inspection and wizard all purpose canvas Power App
Sample audit, inspection, wizard Canvas Power App. Fields in app are dynamically "created" based on field definitions managed through admin model driven app. Taking the word Wizard and Audit and combining to get the name WizAud.

## Background
I wanted to create a generic canvas Power App which could render fields / questions dynamically based on a question list defined elsewhere. This is because I was being asked frequently to create demo apps for organisations, and each one has a similar construct but different set of questions / fields to be shown to the user. This app now allows me to create demo apps which capture data without having to edit or create controls on a Power App.

This sample app could be useful in the following scenarios:
1. Site Inspections or Audits
2. Wizard style data capturing application

The canvas Power App supports offline usage scenarios too. That is, the person completing the inspection / audit doesnt need to have internet connectivity on their mobile device in order to capture the data. Once connected later, they can see saved records and submit them.

## Its a sample
Please do note, this is a sample application that is not intended to be used in production environments as is. It is intended to help a Power Apps developer to learn how they could assemble such an application. It is certainly not a perfect solution, it hasn't been well tested, and is missing some key features that I hope to add over time.

## How it works
There are 2 main applications which makeup this solution. 
1 - Admin Model Driven App
2 - User Canvas App

All data resides in the Common Data Service (CDS), both WizAud definitions and responses.

The admin model driven app is where you setup your WizAuds. A WizAud is something you want to capture e.g. Site Inspection, Vehicle Inspection, Request for Leave etc. Within a WizAud you define what fields (questions) you would like a person using the Canvas app to complete. A WizAud has a name, option start and end date, and some future feature flags e.g. generate PDF, request final signature etc. Each field has a data type, and order where it appears in the list of questions, required or not, if notes field should be displayed and if images should be captured for the question (future feature).

The canvas app is a 2 screen sample app designed for phone form factor. First screen lists the WizAuds available for the user to complete, and also shows draft responses and previous responses. When you select a WizAud to complete, you are take to the second screen which lists the questions/fields the user should complete. Save as Draft will allow you to save a response to be submitted later e.g. because you are offline, and Submit button submits data to backend (CDS). Submit button is not available if offline.

Solution file and overview PPT is in the solution folder.

