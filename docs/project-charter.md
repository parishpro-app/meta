ParishPro - Project Charter

Version 1.0

Date: March 17, 2026

Author: Destin Gollamudi

1. Project Overview

ParishPro is a free, open source volunteer scheduling platform built for Catholic parishes. It will automate the scheduling process for the various ministries a parish may have for liturgies, and ministries, and miscellaneous parish activities. This will replace the common solution for many parishes of manual google docs and email chains with a role based web application

This project exists since parish scheduling can be unnecessarily complex and existing commercial solutions are too costly for nonprofit religious parishes. The liturgy coordinator at St. Augustine Parish identified a useful solution for a unified schedule system after the parish canceled their Ministry Scheduler Pro subscription since the cost was too high. 

2. Problem Statement

Many parishes currently manage volunteer scheduling through a variety of distributed unified disorganized means. This includes shared google docs, email chain, manual coordination, physical calendars, etc. This process is time consuming, fragmented, costly (when using a vendor solution), prone to errors and miscommunication between volunteers and coordinators.

3. Project Objectives 



* Deliver a low cost, self-hosted web application that manages and automates scheduling for Catholic parishes
* Replace old and fragmented methods with a scheduling service
* Provide coordinators unified view of all ministry schedules
* Enable volunteers to manage their own availability and handle substitute requests without coordinator intervention 
* Become adopted at St. Augustine Parish as first product deployment within one year of project inception 

4. Success Criteria

The project is successful when:



* St. Augustine Parish is using ParishPro in production
* Liturgy coordinator and others report measurable reduction in scheduling overhead and better experience
* At least one other parish has adopted or is interested in adopting this solution
* The codebase is publicly available, well documented, and easily accessible to new contributors 

5. Stakeholders


<table>
  <tr>
   <td>Stakeholder
   </td>
   <td>Role
   </td>
   <td>Interest
   </td>
  </tr>
  <tr>
   <td>Destin Gollamudi
   </td>
   <td>Project Lead
   </td>
   <td>Owns vision, architecture and delivery of project
   </td>
  </tr>
  <tr>
   <td>Coordinators (Liturgy, Altar serving, music)
   </td>
   <td>Primary end Users
   </td>
   <td>Needs unified scheduling to replace manual process
   </td>
  </tr>
  <tr>
   <td>Parish Pastor
   </td>
   <td>Executive Sponsor
   </td>
   <td>Confirmed value of automated scheduling
   </td>
  </tr>
  <tr>
   <td>Open Source Contributors
   </td>
   <td>Development Team
   </td>
   <td>Gaining technical experience while serving the church
   </td>
  </tr>
  <tr>
   <td>Parish ministry volunteers
   </td>
   <td>End users
   </td>
   <td>Need simple interface to manage availability and assignments
   </td>
  </tr>
</table>


6. Scope

In Scope:



* Automated monthly schedule generation
* Minister profile management and availability 
* Ministry and liturgy configuration 
* Substitute request management 
* Automated email notifications 
* Admin dashboard for schedule management
* Self-hosted deployment via Docker

Out of scope:



* Commercial licensing or paid tiers
* Managed hosting service operated by the project
* Financial or donation management 
* Sacramental record keeping
* Mobile native applications (web only for v1)
* Non-scheduling parish management features

7. Project Approach

ParishPro is developed as a community open source project under the AGPL v3 license. Development will be done by volunteers and contributions will not follow a driven specific sprint styled pacing. Contributors self-assign issues from the public project board and work asynchronously at their own pace. 

Phase 1: Pre-development planning

Phase 2: Core development

Phase 3: Beta at St. Augustine's

Phase 4: Public release

8. Constraints and Risks

Constraints:



* No budget - all tooling and infrastructure must be free or self-hosted. Will try to be as cheap as possible so hosting parish spends little expense (just to deploy the server for frontend and backend)
* Volunteer contributors have variable availability 
* Timeline dependent on contributor participation 

Risks:



* Low contributor engagement may slow development
* Stakeholder availability for feedback and testing may be limited 
* Tech stack decisions not yet finalized may cause rework

9. Project Vision

ParishPro will never become a commercial product. It is and will remain free, privately distributed, and operated by parishes centered around technically capable parishioners. This project community serves a dual purpose - delivering useful software to the church while providing contributors with real world technical experience. 

AMDG
