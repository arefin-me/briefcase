# Briefcase

## Software Requirements Specification (SRS)

---

**Project:** Briefcase — Research Collaboration Platform

**Version:** 0.1 — Initial Draft

**Date:** November 19, 2026

**Course:** System Analysis and Design Lab

**Prepared by:** Sultanul Arefin

**Status:** Draft

---

# Revision History

| Version | Date | Author | Changes |
|---|---|---|---|
| 0.1 | 19-11-2026 | [Member 1] | Initial SRS draft |

---

# 1. Introduction

## 1.1 Purpose

This Software Requirements Specification (SRS) describes the functional and non-functional requirements of Briefcase, a research collaboration platform.

The purpose of Briefcase is to help students and researchers showcase their academic work, discover research opportunities, and connect with potential collaborators.

This document is intended for:

- Development team
- Project supervisor and course teacher
- System designers
- Testers and future maintainers

## 1.2 Scope

Briefcase is a web-based platform designed to support academic and research collaboration.

### What the system will do

- Allow users to create and manage research profiles.
- Allow users to showcase previous and ongoing projects.
- Allow users to add project descriptions, links, and supporting documents.
- Allow users to discover research papers and projects.
- Recommend potential collaborators based on research interests and contributions.
- Allow users to publish collaboration requests.
- Allow interested users to respond to collaboration requests.

### What the system will not do

- Conduct research on behalf of users.
- Guarantee the accuracy or quality of uploaded research.
- Automatically verify every academic publication.
- Provide a complete university learning management system.
- Manage research funding or financial transactions.

## 1.3 Definitions

| Term | Meaning |
|---|---|
| Researcher | A user participating in academic or research activities |
| Work Tree | A user's collection of previous and ongoing projects |
| Collaboration | Joint work between two or more researchers |
| Research Interest | A subject or field a user wants to explore |
| Matching | Recommending potential collaborators based on relevant information |
| Discover | The platform's research and project exploration section |

## 1.4 References

1. IEEE 830-1998 — Recommended Practice for Software Requirements Specifications.
2. ISO/IEC/IEEE 29148:2018 — Requirements Engineering.
3. Course-provided HealthBridge BD SRS sample.

## 1.5 Overview

Section 2 describes the overall system. Section 3 explains external interfaces. Section 4 lists functional requirements. Section 5 describes non-functional requirements. Appendix A contains analysis and design models.

---

# 2. Overall Description

## 2.1 Product Perspective

Briefcase is an independent web-based research collaboration platform.

It provides a common environment where users can maintain research profiles, showcase academic contributions, explore research work, and find collaborators.

The platform is intended to connect people based on their academic interests and previous contributions.

## 2.2 Product Functions

| ID | Function | Description |
|---|---|---|
| F1 | User Authentication | Register, log in, and manage accounts |
| F2 | Research Profile | Create profiles containing academic backgrounds and research interests |
| F3 | Work Tree | Add and manage previous and ongoing projects |
| F4 | Discover | Browse research papers and projects |
| F5 | Matching | Recommend potential collaborators |
| F6 | Collaboration Requests | Publish requests for research partners |
| F7 | Collaboration Response | Respond to collaboration requests |
| F8 | Administration | Manage users and reported content |

## 2.3 User Classes

| User | Description |
|---|---|
| Student | Creates a profile, showcases academic work, and searches for collaborators |
| Researcher | Explores research opportunities and connects with other researchers |
| Administrator | Manages user accounts and monitors platform content |

## 2.4 Operating Environment

| Component | Proposed Environment |
|---|---|
| Frontend | Web browser |
| Backend | Server-side application |
| Database | Relational database |
| Operating System | Windows / Linux / macOS |
| Client Devices | Desktop, laptop, tablet |

*Note: The implementation technologies are yet to be finalized by the team.*

## 2.5 Design Constraints

- The system must provide a user-friendly interface.
- User profiles must be accessible only according to defined permissions.
- Project information must be stored consistently.
- The platform must support multiple users.
- Recommendations must be based on available profile and contribution information.

## 2.6 Assumptions and Dependencies

- Users have internet access.
- Users provide accurate information about their academic backgrounds and projects.
- Users have permission to share the documents and links they upload.
- The recommendation feature depends on the information available in user profiles.

---

# 3. External Interface Requirements

## 3.1 User Interface

The platform will provide the following main screens:

1. Registration and Login
2. User Dashboard
3. Research Profile
4. Work Tree
5. Discover
6. Matching
7. Collaboration Requests
8. Administrator Dashboard

The UI designs will be prepared in Figma.

## 3.2 Software Interfaces

The system will interact with:

- Its relational database for storing user and project information.
- A web browser through which users access the platform.

Any additional external API or service will be documented after the implementation decision.

## 3.3 Communication Interfaces

- Client-server communication will use HTTPS.
- Data exchange between the frontend and backend will use a defined application interface.
- User-uploaded files will follow the platform's file validation rules.

---

# 4. Functional Requirements

Requirements use unique IDs and MoSCoW priorities.

## 4.1 User Authentication

| ID | Requirement | Priority |
|---|---|---|
| FR-AUTH-01 | The system shall allow new users to create an account. | Must |
| FR-AUTH-02 | The system shall allow registered users to log in. | Must |
| FR-AUTH-03 | The system shall allow users to log out. | Must |

## 4.2 Research Profile

| ID | Requirement | Priority |
|---|---|---|
| FR-PROF-01 | The system shall allow users to create a research profile. | Must |
| FR-PROF-02 | The system shall allow users to add their academic background. | Must |
| FR-PROF-03 | The system shall allow users to specify their research interests. | Must |
| FR-PROF-04 | The system shall allow users to update their profile information. | Must |

## 4.3 Work Tree

| ID | Requirement | Priority |
|---|---|---|
| FR-WORK-01 | The system shall allow users to add previous projects to their Work Tree. | Must |
| FR-WORK-02 | The system shall allow users to add ongoing projects to their Work Tree. | Must |
| FR-WORK-03 | The system shall allow users to provide project titles and descriptions. | Must |
| FR-WORK-04 | The system shall allow users to attach project links or supporting documents. | Should |
| FR-WORK-05 | The system shall allow users to update their project information. | Must |

## 4.4 Discover

| ID | Requirement | Priority |
|---|---|---|
| FR-DISC-01 | The system shall allow users to browse available research projects. | Must |
| FR-DISC-02 | The system shall allow users to search for research projects by keyword. | Must |
| FR-DISC-03 | The system shall allow users to filter projects by research domain. | Should |

## 4.5 Matching

| ID | Requirement | Priority |
|---|---|---|
| FR-MATCH-01 | The system shall recommend potential collaborators based on overlapping research interests. | Must |
| FR-MATCH-02 | The system shall consider users' recorded project contributions when generating recommendations. | Should |
| FR-MATCH-03 | The system shall display the relevant interests of recommended collaborators. | Must |

## 4.6 Collaboration Requests

| ID | Requirement | Priority |
|---|---|---|
| FR-COL-01 | The system shall allow users to publish collaboration requests. | Must |
| FR-COL-02 | The system shall allow users to specify the research domain of a request. | Must |
| FR-COL-03 | The system shall allow other users to view available collaboration requests. | Must |
| FR-COL-04 | The system shall allow interested users to respond to collaboration requests. | Must |

## 4.7 Administration

| ID | Requirement | Priority |
|---|---|---|
| FR-ADM-01 | The system shall allow administrators to view registered users. | Must |
| FR-ADM-02 | The system shall allow administrators to review reported content. | Should |
| FR-ADM-03 | The system shall allow administrators to suspend accounts that violate platform rules. | Should |

---

# 5. Non-Functional Requirements

| ID | Category | Requirement |
|---|---|---|
| NFR-01 | Performance | The system should display standard pages within 3 seconds under normal operating conditions. |
| NFR-02 | Security | The system shall restrict access to account information according to user permissions. |
| NFR-03 | Usability | The system shall provide a consistent navigation structure across its main sections. |
| NFR-04 | Reliability | The system shall preserve successfully saved user and project information. |
| NFR-05 | Compatibility | The system should support modern versions of major web browsers. |
| NFR-06 | Maintainability | The system should use a modular structure to simplify future updates. |

---

# 6. Other Requirements

## 6.1 Data Management

The system will maintain records of:

- User accounts
- Academic profiles
- Research interests
- Projects and contributions
- Research collaboration requests
- Collaboration responses

## 6.2 Data Backup

The system should maintain regular database backups to reduce the risk of data loss.

## 6.3 Future Enhancements

Possible future features include:

- Advanced collaborator recommendation algorithms.
- Research team workspaces.
- Publication verification.
- Project contribution analytics.
- Direct messaging between collaborators.
