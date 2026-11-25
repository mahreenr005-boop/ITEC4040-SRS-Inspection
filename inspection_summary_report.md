# Inspection Summary Report


## Inspection Identification

- **Project:** ITEC 4040 Term Project – SRS Inspection of the South Northern University (SNU) Faculty of Science Grants Management System
- **Meeting Date:** Sunday, November 22, 2026, 2:30 PM start on Zoom (booked 2:00 to 4:00 PM; the meeting itself took 1 hour 11 minutes 44 seconds, and we started around 2:30)

## Work Product Description

- **Work product:** SRS draft for the SNU Faculty of Science Grants Management System, received for inspection. 
- **Format:** Anonymized GitHub-friendly markdown, received as a ZIP file and opened in Obsidian. The root document is `Main.md`, with use cases, data requirements, interfaces, quality attributes, business rules and interview evidence in separate files. 
- **Version:** "Draft for Inspection", received on Thursday November 19, 2026. 
- **Size:** 18 in-scope files, about 9,850 words (about 20 pages at 500 words per page, since markdown has no page numbers). 
- **Scope inspected:** 
    - Sections 1 and 2 
    - Section 3, features up to and excluding review and adjudication 
    - Section 4.3 (data acquisition, integrity, retention and disposal) 
    - Section 5.2 (software interfaces) 
    - Section 6.5 (Security, the one quality requirement chosen by the authors) 
    - Appendices: Business Rules and Domain Evidence 
- **Not inspected:** sections that authors were told to leave out of the draft    (4.1, 4.2, 5.1, 5.3, 5.4, other quality attributes, glossary).


## Inspectors

| #   | Role      | Inspector | Preparation Time (hours) |
| --- | --------- | --------- | ------------------------ |
| 1   | Author    |   N/A        |       N/A                   |
| 2   | Moderator, Inspector |     Hana Khan      | 2 |
| 3   | Recorder, Inspector  |   Mahreen Rahman        | 2.5 |
| 4   | Reader, Inspector    |  Ali Fareed         | 2.5 |
| 5   | Reader, Inspector |  Syed Ahmed         | 3 |

## Inspection Data

| Metric                   | Value              |
| ------------------------ | ------------------ |
| Planned for Inspection   | about 20 pages (18 in-scope files, about 9,850 words at 500 words per page) |
| Actually Inspected       | about 20 pages (all in-scope sections) |
| Meeting Time             | 1.20 hours (1 hour 11 minutes 44 seconds, about 71.7 minutes) |
| Total Planning Effort    | 3 labor hours |
| Total Overview Effort    | 0 labor hours (no separate overview meeting) |
| Total Preparation Effort | 10 labor hours (Hana 2 + Mahreen 2.5 + Ali 2.5 + Syed 3) |
| Actual Rework Effort     | N/A|

## Inspection Process Description

**Planning**
- We received the anonymized SRS draft through our group forum.
- We booked a 2-hour slot (Sunday, November 22, 2026, 2:00 to 4:00 PM on Zoom, but we started around 2:30 instead) and posted it in the group forum and Jira.
- Roles: Hana as Moderator, Ali and Syed as Readers, Mahreen as Recorder. All four members also acted as inspectors. The authors were not present because the SRS was anonymized.
- We divided the document between the readers and inspectors so every section had someone responsible for it.

**Preparation**
- Each member reviewed the full in-scope document individually before the meeting using the Inspector's Checklist from the course slides (Validation, slides 13–14). 
- Each member brought their own list of issues with exact locations and tracked their preparation time.
- Typos were kept on a separate list and not discussed in the meeting.

**Meeting**
- We met on Zoom and recorded the meeting. Everyone identified themselves by voice at the start.
- Hana (Moderator) followed the Moderator's Checklist: confirmed the version, introduced the roles, ground rules and objectives, collected and added up everyone's preparation time, and invited positive comments and global observations before starting.
- The SRS was inspected in 14 chunks, in this order: Sections 1 and 2; the Section 3 overview and use case diagram; the 8 use cases one at a time; Section 4.3; Section 5.2; Section 6.5; and the appendices.
- In each chunk the reader paraphrased the section in their own words. Syed and Ali alternated as reader (Syed read Section 1 and Ali read Section 2 in the first chunk).
- Turns followed a fixed order in every chunk: the other reader first, then the reader, then Mahreen, and Hana last. Each person gave one positive comment, then their issues. This kept turns balanced and everyone participated.
- Mahreen logged each issue in the issue log with a number, location, type and severity. Typos were kept on a separate list.
- Discussion was limited to about 1-5 minutes per issue. Anything not settled was logged as an open question and we moved on. Hana kept time.
- The group voted on the appraisal at the end, then covered the pages inspected, lessons learned and next steps.
- The meeting took 1 hour 11 minutes 44 seconds (about 71.7 minutes), shorter than the 2-hour slot.
- We inspected every in-scope section.
- Left out: the sections the authors were told to leave out (4.1, 4.2, 5.1, 5.3, 5.4, the other quality attributes and the glossary), and everything about reviewing and adjudicating applications.

## Summary of Issues

We logged 86 issues: 15 major and 71 minor. By type: Incomplete 31, Inconsistent 13, Invalid 13, Untraceable 10, Ambiguous 10, Unverifiable 9. The most important ones, and the ones that kept repeating:

**Major issues**
- Untraceable evidence: Sections 4.3, 5.2 and 6.5 cite "Annex A" and numbered interview questions that do not exist, and the facts in Section 2 never cite the interview they came from.
- Not testable: Section 4.3 and Section 6.5 have no numbers (purge time, backup frequency, recovery time, encryption standard, lockout, timeout), so they cannot be verified.
- Missing functionality: no use case for applicants to check status or be notified, no flow for a Chair who does not respond, no CRUD authorization matrix, no audit logging, and 4.3 is missing initial data acquisition and a lock after submission.
- Conflicts with the stakeholder evidence: BR-5 says late applications are always rejected, but RO-07 accepts them; BR-9 conflicts with RO-02 and RO-07; Section 2.4 says no language is chosen, but IT-08 says Java is strongly preferred; 3.5.1 uses reviewer "assignments", but CHAIR-03 says everyone reads all applications.
- Inconsistent application statuses (Draft, Submitted, ready for review distribution, correction-required) that are never defined, with no state diagram.
- Duplicated completeness check in 3.4.1 and 3.2.2, and use case 3.5.2 is outside the scope of the draft.

**Issues that kept repeating**
- Use cases have no diagrams or mock-ups, no numbered pre- and postconditions, and alternative flows and exceptions that do not say which step they branch from.
- Requirements that cannot be tested because of vague wording or undefined terms ("clear", "specific and understandable", "permitted lengths", "flagged or uncertain cases").
- Open items marked "to be confirmed" that the evidence already answers (eligibility APP-08, late submissions RO-07).
- Broken or misleading links and leftover template text (Main.md links to 4.2 and 5.2.SI, template examples in the acceptance tests, a stub BR-1).
- Missing YAML headers in 4.3, 5.2 and 6.5, and inconsistent evidence labels (Appendix B vs D, a placeholder interview date).
- No source cited for the business rules or for facts like "1 to 3 IT admins".

## Product Appraisal

**RECOMMENDATION**
- [ ] accepted as is
- [ ] conditionally accepted upon verification
- [x] reinspect following rework
- [ ] inspection not completed

**OTHER COMMENTS**
- The group voted to reinspect following rework. The draft has 15 major issues, mainly untraceable evidence, requirements that cannot be tested, missing functionality and conflicts with the stakeholder evidence, and fixing them will change the document enough that a second inspection is needed.
- Positives: the use cases follow a consistent structure, the requirements are tied to stakeholder evidence in most places, and the business rules and interview summaries are easy to find.
- Suggested follow-up: the authors fix the major issues first, add real numbers to 4.3 and 6.5, define the application statuses once, and fix all links and YAML headers before reinspection.
- Meeting time: 1 hour 11 minutes 44 seconds (about 71.7 minutes).

----
*Copyright © 2001 by Karl E. Wiegers. Permission is granted to use, modify, and distribute this document.*
