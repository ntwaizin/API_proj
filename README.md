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
