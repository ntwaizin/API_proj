# API_proj

1. Introduction

The RACE_DAY database is designed to manage running, cycling and walking events. The database stores information about users, events, categories, enrolments, results and event images.

The database uses relationships between tables to make sure that the information is organised and easy to access.

2. Database Name

The database is called:

RACE_DAY

3. Tables Used

The database contains the following tables:

USERS

Stores information about users of the system.

It contains:

UserID
FirstName
LastName
Email
Password
Role

Users can be either Organisers or Participants.

EVENTS

Stores information about race and sporting events.

It contains:

EventID
EventName
EventDescription
EventDate
Location
Distance
EventType
OrganiserID

Each event has an organiser.

CATEGORIES

Stores the different categories available for each event.

It contains:

CategoryID
CategoryName
EventID

ENROLMENTS

Stores information about participants who enrol for events.

It contains:

EnrolmentID
ParticipantID
EventID
CategoryID
EnrolmentStatus

RESULTS

Stores the results of participants who completed an event.

It contains:

EVENT_IMAGES

Stores images associated with events.

It contains:

ImageID
EventID
ImageURL

ResultID
EnrolmentID
FinishTime
FinishingPosition

4. Relationships

The database has the following relationships:

A USER can organise one or more EVENTS.
An EVENT belongs to an organiser.
An EVENT can have multiple CATEGORIES.
A PARTICIPANT can enrol in multiple EVENTS.
An ENROLMENT belongs to a participant, event and category.
An ENROLMENT can have a RESULT.
An EVENT can have multiple EVENT_IMAGES.

5. SQL Operations

The SQL script performs the following operations:

Creates the RACE_DAY database.
Selects the database using USE RACE_DAY.
Creates all the required tables.
Adds primary keys.
Adds foreign keys to connect the tables.
Inserts sample data into the tables.
Uses SELECT statements to display the data.
Uses INNER JOIN statements to combine information from related tables.

6. INNER JOIN

An example of an INNER JOIN used in the database is:

SELECT
    USERS.FirstName,
    USERS.LastName,
    EVENTS.EventName
FROM USERS
INNER JOIN EVENTS
    ON USERS.UserID = EVENTS.OrganiserID;

This query displays the first name, last name and event name of users who are organisers.

The INNER JOIN only displays records where there is a matching value between the two tables.

7. Sample Data

The database contains sample users such as:

John Mokoena
Thabo Nkosi
Mphiwa Bucibo
Sihle Dlamini

The sample events include:

Soweto Marathon
Johannesburg Cycle Tour
Cape Town Fun Walk

8. How to Run the Database

To run the database:

Open MySQL or SQL Server.
Copy the SQL code into the SQL editor.
Run the database creation section first.
Run the table creation statements.
Run the INSERT statements.
Run the SELECT statements to view the data.
Run the INNER JOIN queries to view information from multiple tables.

9. Purpose of the Database

The purpose of the RACE_DAY database is to provide an organised way of managing sporting events, participants, organisers, event categories, enrolments and race results.

It reduces the need to store information manually and makes it easier to retrieve related information using SQL queries.

9. Primary Keys

Primary keys are used to uniquely identify each record in a table.

The database uses the following primary keys:

UserID in the USERS table
EventID in the EVENTS table
CategoryID in the CATEGORIES table
EnrolmentID in the ENROLMENTS table
ResultID in the RESULTS table
ImageID in the EVENT_IMAGES table

A primary key cannot contain duplicate values.
