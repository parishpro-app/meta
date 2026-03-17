ParishPro - Use Case Document

Version: 1.0

Date: March 17, 2026

Author: Destin Gollamudi

1. Introduction

This document describes the functional interactions between users and 

the ParishPro system. Each use case represents a discrete goal a user 

can accomplish. This document should be read alongside the Software 

Requirements Specification v1.2.

Actors:

- Administrator: Full system access across all ministries

- Coordinator: Scoped access to their assigned ministry domain only

- Volunteer: Self-service access to personal schedule and availability

2. Use Cases

---

UC-01: Create and Manage Liturgy Templates

Actor: Administrator

Preconditions: Administrator is logged in

Main Flow:

1. Administrator navigates to liturgy management

2. Administrator creates a new liturgy template with day, time, and name

3. System saves the liturgy template

4. Template is now available for schedule generation

Alternative Flows:

- A2. Administrator edits an existing liturgy template

- A3. Administrator deletes a liturgy template that has no future 

     scheduled assignments

- A4. Administrator creates a one-off special liturgy for a specific 

     date such as Christmas or Easter

Postconditions: Liturgy template is saved and available for use

---

UC-02: Create and Manage Ministries

Actor: Administrator

Preconditions: Administrator is logged in

Main Flow:

1. Administrator navigates to ministry management

2. Administrator creates a new ministry with a name

3. Administrator defines the number of volunteers required per liturgy

4. System saves the ministry configuration

Alternative Flows:

- A2. Administrator edits an existing ministry

- A3. Administrator deletes a ministry with no active assignments

- A4. Administrator assigns a Coordinator to the ministry

Postconditions: Ministry is saved and available for volunteer assignment 

and schedule generation

---

UC-03: Create and Manage Volunteer Accounts

Actor: Administrator

Preconditions: Administrator is logged in

Main Flow:

1. Administrator navigates to volunteer management

2. Administrator creates a new volunteer account with first name, 

   last name, and email address

3. Administrator assigns the volunteer to one or more ministries

4. System creates the account and sends a welcome email to the volunteer

Alternative Flows:

- A2. Administrator edits an existing volunteer profile

- A3. Administrator deactivates a volunteer account

- A4. Administrator groups volunteers into a family unit to ensure 

     they are scheduled together

Postconditions: Volunteer account is created and volunteer can log in

---

UC-04: Generate Monthly Schedule

Actor: Administrator

Preconditions: 

- Administrator is logged in

- Liturgy templates are configured

- Ministries are configured with required volunteer counts

- Volunteers are assigned to ministries

- Target month is specified

Main Flow:

1. Administrator navigates to schedule generation

2. Administrator selects the target month

3. Administrator triggers the auto-scheduler

4. System generates a draft schedule applying all constraints:

   - Availability: only schedules volunteers who are available

   - Qualification: only schedules volunteers for their assigned 

     ministries

   - No double booking: no volunteer scheduled twice on the same day

   - Fairness: distributes assignments evenly across volunteers

   - Family grouping: prioritizes scheduling family members together

5. System displays the draft schedule with any unfilled slots 

   clearly indicated

6. Administrator reviews the draft

Alternative Flows:

- A5. Scheduler cannot fill all slots due to insufficient available 

     volunteers - slots remain empty and are clearly marked

Postconditions: Draft schedule is generated and available for review 

and editing

---

UC-05: Review and Edit Draft Schedule

Actor: Administrator

Preconditions:

- Administrator is logged in

- Draft schedule exists for the target month

Main Flow:

1. Administrator views the draft schedule

2. Administrator identifies assignments to change

3. Administrator manually adds, removes, or swaps volunteer assignments

4. System validates changes against scheduling constraints

5. Administrator saves changes to the draft

Alternative Flows:

- A3. Administrator manually fills an empty slot the auto-scheduler 

     could not fill

- A4. Swap causes a conflict - system warns the Administrator

Postconditions: Draft schedule reflects all manual edits and is ready 

for publishing

---

UC-06: Publish Schedule

Actor: Administrator

Preconditions:

- Administrator is logged in

- Draft schedule exists and has been reviewed

Main Flow:

1. Administrator reviews the final draft schedule

2. Administrator publishes the schedule

3. System marks the schedule as published

4. System sends email notifications to all scheduled volunteers

5. Schedule is now visible to all volunteers in the Minister portal

Alternative Flows:

- A4. Some volunteers do not have valid email addresses - system logs 

     failed notifications and alerts the Administrator

Postconditions: Schedule is published and all volunteers are notified

---

UC-07: Manually Fill Empty Slots

Actor: Administrator, Coordinator

Preconditions:

- User is logged in with appropriate access

- Published or draft schedule contains empty slots

Main Flow:

1. User navigates to the schedule and identifies an empty slot

2. User selects a qualified available volunteer for the slot

3. System assigns the volunteer to the slot

4. If schedule is already published, system notifies the assigned 

   volunteer

Alternative Flows:

- A2. No qualified volunteers are available - slot remains empty

Postconditions: Slot is filled and volunteer is notified if schedule 

is published

---

UC-08: Send Bulk Email Communications

Actor: Administrator

Preconditions: Administrator is logged in

Main Flow:

1. Administrator navigates to the mailer

2. Administrator selects recipients

3. Administrator selects or composes a message template

4. Administrator inserts tokens such as first name and schedule link

5. Administrator sends the message

6. System delivers emails to all selected recipients

Alternative Flows:

- A2. Administrator saves draft message for later

- A6. Some emails fail to deliver - system logs failures and alerts 

     the Administrator

Postconditions: Emails are delivered to selected recipients

---

UC-09: View Ministry Schedule

Actor: Coordinator

Preconditions:

- Coordinator is logged in

- Published schedule exists for their ministry domain

Main Flow:

1. Coordinator navigates to their ministry schedule view

2. System displays the published schedule scoped to their ministry only

3. Coordinator views assignments, dates, and volunteer details

Alternative Flows:

- A2. No published schedule exists - system displays a message 

     indicating no schedule is available

Postconditions: Coordinator has viewed their ministry schedule

---

UC-10: Manage Substitute Requests

Actor: Coordinator

Preconditions:

- Coordinator is logged in

- Open substitute requests exist within their ministry domain

Main Flow:

1. Coordinator navigates to substitute request management

2. System displays all open substitute requests within their ministry

3. Coordinator reviews open requests

4. Coordinator can manually assign a qualified volunteer to fulfill 

   the request if needed

Alternative Flows:

- A4. No qualified volunteers are available - slot remains open

Postconditions: Substitute request is reviewed and actioned if possible

---

UC-11: Log In and View Personal Schedule

Actor: Volunteer

Preconditions:

- Volunteer has an active account

- Published schedule exists

Main Flow:

1. Volunteer navigates to the ParishPro portal

2. Volunteer logs in with email and password

3. System displays the volunteer's personal schedule

4. Volunteer views their upcoming assignments in list and calendar view

Alternative Flows:

- A2. Invalid credentials - system displays error and prompts retry

- A3. No published schedule exists - system displays message indicating 

     no schedule is available yet

Postconditions: Volunteer has viewed their personal schedule

---

UC-12: Submit Unavailability

Actor: Volunteer

Preconditions: Volunteer is logged in

Main Flow:

1. Volunteer navigates to availability management

2. Volunteer selects dates or date ranges when they cannot serve

3. System saves the unavailability

4. Saved unavailability is applied during the next schedule generation

Alternative Flows:

- A2. Volunteer submits unavailability for a date already scheduled - 

     system notifies volunteer they must use the substitute request 

     system for existing assignments

Postconditions: Unavailability is saved and will be respected by the 

scheduling engine

---

UC-13: Initiate Substitute Request

Actor: Volunteer

Preconditions:

- Volunteer is logged in

- Volunteer has a published assignment they cannot fulfill

Main Flow:

1. Volunteer navigates to their schedule

2. Volunteer selects an assignment they cannot fulfill

3. Volunteer initiates a substitute request

4. System notifies all qualified volunteers in the same ministry of 

   the open slot

5. Sub request remains open until accepted or until end of day of 

   the liturgy event

Alternative Flows:

- A5. No qualified volunteers accept before the event day ends - 

     sub request expires and Administrator is notified

Postconditions: Sub request is open and qualified volunteers are 

notified

---

UC-14: Accept Substitute Request

Actor: Volunteer

Preconditions:

- Volunteer is logged in

- Open substitute request exists in a ministry the volunteer is 

  qualified for

- Sub request has not yet expired

Main Flow:

1. Volunteer views open substitute requests

2. Volunteer selects a request to accept

3. System transfers the assignment to the accepting volunteer

4. System removes the original volunteer from the assignment

5. System notifies the original volunteer and Administrator of 

   the accepted substitution

Alternative Flows:

- A2. Sub request was already accepted by another volunteer - system 

     notifies volunteer the request is no longer available

Postconditions: Assignment is transferred, original volunteer is 

released, and all parties are notified

---

3. Change Log

Version 1.0 (March 17, 2026):

- Initial use case document created

- 14 use cases defined covering Administrator, Coordinator, 

  and Volunteer actors
