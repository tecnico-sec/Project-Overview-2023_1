Instituto Superior Técnico, Universidade de Lisboa

**Network and Computer Security**

# Project Overview

This document describes the organization of the project for the Network and Computer Security / Segurança Informática em Redes e Sistemas (SIRS) course.

You will work in a teams of 3 members.

The project is contextualized in one of a set of business scenarios: Retail, Transportation & Distribution, Restaurants & Tourism, Insurance and Banking, Healthcare, Legal, Industrial, and Utilities.

The project is organized in 3 parts: infrastructure, secure channels, and custom protocol.

The first part - _infrastructure_ - will be mostly supported by the laboratory tutorials.  
The expected result is a virtual environment with networks and machines, with adequate firewall configurations, running application and database servers chosen by the team, providing operations that access a relevant informational entity in the business context of the scenario.

The second part - _secure channels_ - will require the teams to search for documentation to configure secure communication for their chosen combination of application and database servers.
The expected result is an updated version of the environment with all communication with servers protected by existing cryptographic protocol implementations (e.g., TLS, SSH).

The third part - _custom protocol_ - will require the design and implementation of a custom cryptographic protocol.
Each team will choose a security challenge to tackle in the scenario and propose a solution for it.
The proposal should receive teacher feedback before the implementation begins.
The expected final result is the whole virtual infrastructure, standard secure channels, and the implemented custom cryptographic protocol, with tests and detailed trace logs; all working together to demonstrate an overall secure business solution.

This document will now detail the whole project process, stage by stage, and will conclude with a calendar containing all the deadlines, and the grading criteria.

# 1. Project stages

The whole SIRS project process is organized in sequential stages:

| **Stage**                                                             |
| ----------------------------------------------------------------------|
| [1. Assemble team](#11-assemble-team)                                 |
| [2. Pick scenario](#12-pick-scenario)                                 |
| [3. Build infrastructure](#13-build-infrastructure)                   |
| [4. Protect server communications](#14-protect-server-communications) |
| [5. Pick security challenge](#15-pick-security-challenge)             |
| [6. Design security solution](#16-design-security-solution)           |
| [7. Implement solution](#17-implement-solution)              |
| [8. Prepare demonstration](#18-prepare-demonstration)                 |
| [9. Complete report](#19-complete-report)                             |
| [10. Submit code and report](#110-submit-code-and-report)             |
| [11. Check presentation session](#111-check-presentation-session)     |
| [12. Present and defend](#112-present-and-defend)                     |

<br />

Each stage is described in the following subsections.

## 1.1. Assemble team

Assemble a team of 3 students, committed to work together.  
On the first lab, inform the teacher of the group members.

## 1.2. Pick scenario

The scenarios for the project are described in another document, which will be posted on the course web site.

Read the scenario descriptions and, as a team, sort the topics by preference for doing your work.

When the selection form opens, sort all the scenarios by order of preference and submit.
Number 1 will be your most preferred topic.

Each team should be represented by one student only.
In the selection form, identify your team as `CXX`, where `C` is replaced by A(lameda) or T(aguspark) and `XX` is replaced by the two digits of your group number, as assigned by Fénix.
For example, group 22 of Taguspark is T22 and group 7 of Alameda is A07.

To assure topic diversity, there are limited vacancies for each project scenario.
Slots will be assigned on a _first-come-first-served_ basis using the submitted preferences.

The official topic selection list will be posted after the process is concluded, to confirm the topic assigned to each group.  
If your team did not get its first choice, do not worry, as all scenarios have challenging problems to solve!

## 1.3. Build infrastructure

Now that your team has been assigned a scenario, you can start to build the virtual network and machine infrastructure.

All the machines should be named according to the company name and your team identity.

The planned infrastructure will need to have a set of separate (virtual) machines, with network isolation, namely:

- one database server;
- one application server, exposing an application programming interface (API);
- a client machine, to access the application server.

If the client machine only requires a web browser, it can be replaced by a machine outside the virtual network, such as the host machine, for example.

The database will need to store data for _at least_ one informational entity from the business context, e.g., in the Healthcare scenario, it would store the Patient entity.

The application server will need to access the database and perform CRUD operations (Create, Read, Update, Delete) for at least one entity, e.g., update the patient data.
These operations must be made available to clients, providing an application programming interface (API).

The choices of technologies to use will be entirely made by the project team.
We recommend that you use technologies that you are familiar with, from previous courses, but it is not mandatory.

This infrastructure should be presented to the teacher in the labs session, to receive feedback.

## 1.4. Protect server communications

Now that your team has an application infrastructure, it will have to make the communication with servers secure.

The team will have to search in the documentation for the chosen application and database servers how to configure the available secure channel technologies.

All the necessary keys will need to be generated, certified, and distributed in a documented way.

If the chosen servers do not support the configuration of secure communication protocols, the group will have to follow a secure tunnel approach with SSH or similar protocol/tool.

The team should verify the protection of the communication channels using tools that allow traffic interception and inspection, to make due dilligence to assure that encryption is actually being used.

The traffic analisys may look just at the surface and does not need to perform cryptanalysis.

All the configuration (and references) must be documented and the results should be presented to the lab teacher, again, to receive feedback.

## 1.5. Pick security challenge

Now that your team has an application infrastructure with all server communications secure, you are ready to face a security challenge.

The business scenario description includes a short description of existing challenges.
It is up to you to select the challenge and design a solution for it.

The solution will need to use cryptographic primitives to build a custom protocol, for communication, for processing, or for storage.

## 1.6 Design security solution

After having a topic assigned, your team should design a security solution.
The design must be written in a document.

You can bring a draft of the proposal to your lab session or office hours to present it and receive feedback.  
It is highly recommended that the proposal is reviewed by the lab teacher before implementation begins.

## 1.7. Implement solution

Plan a gradual implementation of the solution.
First, develop the more basic components and test them.
Then, move to the more advanced components.

Attend the lab sessions to present your ongoing development and receive early feedback from the teacher.

## 1.8. Prepare demonstration

Once a stable and mostly complete solution is achieved, your team should start preparing the demonstration.
The focus of the presentation should be on the back-end of security, i.e., to show the security mechanisms at work;
it should NOT be on the front-end of the application.
It is very important that the messages and its payloads are clearly presented, with trace logs.

Also at this stage, write a `README` file with step-by-step instructions on how to run your project
(suggested [README template](https://gist.github.com/miguelpardal/36f6ef7864bfdeabe5c57b161aa80f2f)).  

It is also good to record screenshots, screencasts or similar artifacts showing your project in action.

## 1.9. Complete report

The project final report should describe the problem and the implemented solution, along with a presentation of the results.
The report document should update and extend the previous versions of reports.

## 1.10. Submit code and report

Before the final deadline of the project, submit an archive with all the developed code and resources, and the report document.

IMPORTANT: the code archive and the report are submitted separately on the Fénix system.

## 1.11. Check presentation session

The project presentations will occur on the dates following the submission deadline.  
The presentation session calendar will be made available during the final days of the project.

Each team is assigned to a session, in their respective campus, preferably in the time-slot of laboratory they are enrolled to.  
If your group requires a change in the proposed slot, please contact faculty in advance.

Each group will have to attend the full presentation session where they will present and one additional session.  
The presentation slides must be in English and the presenters should also present in English.  
For the discussion questions, students can answer in Portuguese.

The presentations are done by the whole group, in person, on campus.
Each group must attend from the beginning of their assigned session and remain for the duration of it.

## 1.12. Present and defend

The presentation should be organized as follows:

- 8 minutes for presentation of the work done, supported by slides, including a mandatory 2 minute live demo  
(also prepare a video of the demo, as backup, just in case there is a technical problem);
- 7 minutes for questions and answers.

It is highly recommended that each presentation includes slides detailing:

- the built infrastructure;
- the configured secure channels and key distribution;
- the security challenge and motivation for it;
- the developed solution with protocol details;
- main results and conclusions.

Each group member must participate and talk in the presentation, and be prepared to answer individual questions.  
If necessary, a more detailed discussion will be scheduled with each group.

# 2. Deliverable details

## 2.1. Report

The report is the document that describes the most important aspects of the realized project.
It will have different versions, each one adding and revising contents, so that, in the end, the most complete and revised document will be presented.
The intermediate versions must be submitted for future reference, but only the final document is graded.

The following requirements apply to all versions of the report:

- PDF format;
- Mandatory file name `YYYY-MM-DD_CXX.pdf`
(where `C` is A for Alameda, T for Tagus, `XX` is the Fénix group number with two digits, `YYYY-MM-DD` corresponds to year, month and date of the document);

- Report cover: Project title. Headed by course name, group campus, group number.  
In the next row: group members sorted by ascending student number.
For each student, include the number and name.
Next, a photo of the team taken together, with good lighting and faces clearly visible.
This is to assure that the team met at least once :)

- Report body: The font should be no smaller than 11pt, with standard line and character spacing;
- Pages should be numbered (preferably with a label like `Page X of Y` or just `X/Y`);

- The use of UML diagrams, or other standard notations, is recommended for clear and concise communication.

- References - important section that includes the bibliographic and technical references, with clickable links.  
Always include at least the authors, title, "where published", and year.  

Regarding the page limits, the cover and the references do not count for the page limit.
Extra materials can be included as appendix, but do not rely on the reviewer reading that part of the document for understanding the report.

### 2.1.1. Infrastructure report

This is the first version of the report to submit.
It must include the following sections, with a 2 page limit.

I. Business Context  

_Short summary of the business context_

II. Infrastructure Overview

_Brief description of the built infrastructure_

_Diagram representing machines and networks_

_Choices of technologies for database server, application server, API, and tests._

### 2.1.2. Channels report

The second version of the report includes updated chapters I, II, and references.
Add the new chapter specified below.
The size limit is increased to 3 pages.

III. Secure Communications

_Configured secure channels_

_What existing security protocol is being used?_  

_Who is communicating?_

_What keys exist and how are they distributed?_  

### 2.1.3. Solution proposal

Update I, II, III, and references, if necessary, and add chapters IV and V.
The new page limit is 6.

IV. Security Challenge

_What is the main problem being solved?_  

_Which security requirements were identified for the solution?_  
Present as a list.
Identify each requirement with an identifier, e.g., R1, R2, etc.

V. Proposed solution  

_Who will be fully trusted, partially trusted, or untrusted?_  
Write down the trust relationships to make them explicit.  

_How powerful is the attacker? What can he do and not do?_  
Attacker model

Secure protocol(s) to develop  
_Who will communicate?_  
_Which security properties will be protected?_  
_What keys will exist and how will they be distributed?_  
Identify communication entities and the messages they exchange with a sequence or collaboration diagram.  

Succinctly describe the technologies to use - libraries, tools, etc. - and why you chose them.

### 2.1.4. Final report

The final version of the report must update everything and add two more chapters: VI and VII.
The page limit is 8.

VI. Results

_For each requirement - R1, R2, ... - state if it was satisfied, partially satisfied, or not satisfied; with a brief justification for each one._  
Justify main implementation choices.

VII. Conclusion

_State the main achievements of your work_  
_Describe possible future enhancements_

## 2.2. Code archive requirements

The code archive to submit must follow the guidelines:

- ZIP format - without compiled code, only source and build scripts;
- The mandatory file name is `CXX_solution.zip`;
- `ReadMe` file, describing the required platform (e.g., Linux 64-bit, Ubuntu 20.04.3 LTS, Java 8u181) and setup instructions;
- All configuration files and scripts required to configure the solution on the specified platform;
- All developed source code;
- Existing tests and example files;
- Hashes of large files.

For all virtual machine files (or other files >50MB), please submit a file with the same name as the original, with the suffix `.hash`, containing the SHA256 value of its contents.
For computing the hash, you can use the [`sha256sum` command](https://man7.org/linux/man-pages/man1/sha256sum.1.html) on Linux, or the [`certutil -hashfile` command](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/certutil) on Windows, or any other tool that correctly implements the algorithm.

Remember to backup all the virtual machine files (or other files >50MB) _at the time of submission_ and DO NOT touch them (golden template), so that later verification of hashes will hold (e.g. put them as read only).
If any changes are made, make sure you do them on a copy of these files.

## 2.3. Presentation archive requirements

After making the presentation, you will have to submit the presentation and video on Fénix.
The presentation archive must follow the guidelines:

- ZIP format;
- The mandatory file name is `CXX_presentation.zip`;
- Presentation in PDF and also in source format (e.g. PowerPoint);
- Text file containing link(s) to download the demo video and screenshots of the solution.
The links must be valid for one month, at least.
The video can also be published in YouTube or a similar platform.

# 3. Calendar

The relevant dates for the project are shown in the following calendar.

| **Stage**                        | **Deadline**                                                   |
| ---------------------------------|----------------------------------------------------------------|
| 1. Assemble team                 | Inform teacher of team members in your lab, before Friday, November 25th, 2022 |
| 2. Pick scenario                 | Topic list published: Tuesday, November 22nd<br />Form opens: Friday, November 25th, 18:30<br />**Closes: Monday, November 28th, 14:00** |
| 3. Build infrastructure          | During the week of November 28th-December 2nd<br />Submit report for future reference |
| 4. Protect server communications | During the week of December 5th-9th<br />Submit updated report |
| 5. Pick security challenge       | During the week of December 5th-9th |
| 6. Design security solution      | Present design to teacher to discuss and get feedback<br />**Submit updated report with proposal** |
| 7. Implement solution            | During the weeks of December 19th-22nd and<br />January 2nd-6th, 2023 |
| 8. Prepare demonstration         | During the week of January 2nd-6th |
| 9. Complete report               | During the week of January 2nd-6th |
| 10. Submit code and report       | **Friday, January 6th, 17:00** |
| 11. Check presentation session   | Calendar available: Wednesday, January 4th<br />**Changes close: Friday, January 6th, 18:00** |
| 12. Present and defend           | Sessions start Monday, January 9th |

# 4. Grading

The project grade will have the following components:

- Infrastructure (10%);
- Secure Channels (10%);
- Security design/rational (20%);
- Security implementation (30%);
- Report (15%);
- Presentation (15%).

# 5. Conclusion

IMPORTANT: keep track of the course [web site](https://fenix.tecnico.ulisboa.pt/disciplinas/SIRS/2022-2023/1-semestre) for updates and links to online forms.

If there are changes to this document, they can be consulted in the _Git Commit History_.

We wish you all the best in this technical venture!  
Make the most of it and ask for our feedback as much as possible.
A security project that receives regular feedback can be improved earlier and is more likely to achieve a better result.

----

For any questions, please contact:  
[SIRS Faculty](mailto:meic-sirs@disciplinas.tecnico.ulisboa.pt)
