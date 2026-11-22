# Inspection Issue Log

**Project:** ITEC 4040 Term Project – SRS Inspection of the South Northern University (SNU) Faculty of Science Grants Management System
**Meeting Date:** Sunday, November 22, 2026, 2:30 PM to 4:08 PM (Zoom)
**Recorder:** Mahreen Rahman


- **Type:** 
	- For individual requirements: **Incomplete** (missing parts), **Invalid** (does not follow from stakeholder needs), **Infeasible**, **Ambiguous**, **Unverifiable**, **Untraceable**. 
	- For sets (e.g. the entire feature): **Incomplete**, **Inconsistent**, **Untraceable**
- **Severity:** **Major**, **Minor** 
- **Location:** Offer section and file name (the SRS is in markdown, so there are no page numbers).

## Issues

| #   | Type | Severity | Location | Description | Raised By |
| --- | ---- | -------- | -------- | ----------- | --------- |
| 1 | Inconsistent | Major | Whole SRS (use cases 3.2.1–3.5.1) | Application statuses (Draft, Submitted, Complete, Incomplete, correction-required, ready for review distribution) are used inconsistently and never defined. No state model. | Ali |
| 2 | Inconsistent | Minor | Whole SRS | Terms are mixed: grant cycle, funding call, call and submission period seem to mean the same thing, and endorsement and signature are mixed. | Syed |
| 3 | Invalid | Minor | `Main.md` Acceptance Criteria and Tests | Template examples (Assignment Management, Student Report Submission) left in. Unrelated to grants and the links go nowhere. | Mahreen |
| 4 | Untraceable | Major | `datareqs/4.3`, `ifaces/5.2`, `qualities/6.5` | Evidence cited as "Annex A/C, Dean Interview, Question N", but interviews have no question numbers and there is no Annex A or C in the SRS. | Mahreen (also Ali) |
| 5 | Invalid | Minor | `Main.md` 2.5 | Lists Keycloak and HR/SIS as dependencies, which repeats the interfaces already in 5.2. | Syed |
| 6 | Unverifiable | Minor | `Main.md` 2.3 | "Supports increased activity around the February and October periods" has no measurable value. | Syed |
| 7 | Invalid | Minor | `Main.md` 2.2 | Accounting and IT are listed as user classes, but they are stakeholders who do not use the system. | Ali |
| 8 | Untraceable | Major | `Main.md` 2.2–2.5 | Facts about users, servers and the login system never cite the interview they came from (e.g. 17 Department Chairs from DEAN-01). | Mahreen |
| 9 | Untraceable | Minor | `Main.md` 2.2 | "1–3 IT System Administrators" is not supported by the IT interview. | Mahreen |
| 10 | Ambiguous | Minor | `Main.md` 2.2 | "9 faculty, with Chair" is unclear about whether the Chair is one of the 9. CHAIR-01 says 11 voting members (9 faculty and 2 students). | Mahreen |
| 11 | Incomplete | Minor | `Main.md` 1.2 | Does not explain the ID labels used throughout (BR-nn, DR-4.3-nn, SI-5.2-nn, QR-6.5-nn) or the evidence codes (DEAN-nn, RO-nn). | Mahreen |
| 12 | Incomplete | Major | `Main.md` 2.4 | Says no programming language is chosen, but IT-08 says the Java ecosystem is strongly preferred and a code licence and support agreement are essential. | Hana |
| 13 | Incomplete | Minor | `Main.md` 3.0 | No log-in use case, although every user must sign in through Keycloak (5.2). | Ali |
| 14 | Incomplete | Major | `Main.md` 3.0 | No use case for the applicant to check status or receive notifications (APP-02, APP-07, BR-15, BR-16). | Syed |
| 15 | Incomplete | Minor | `Main.md` 3.0, `images/GMS-UseCaseDiagram.png` | Use case diagram is a PNG image, not Mermaid or PlantUML source (Term Project 7.2.1). | Mahreen |
| 16 | Incomplete | Minor | `Main.md` 3.0 | Editing and withdrawing an application are not separate use cases, although CRUD should be represented through distinct use cases. | Hana |
| 17 | Incomplete | Minor | `Main.md` 3.0 | No use case for managing user roles or Chair–department assignments (IT-02), which 3.3.1 depends on. | Hana |
| 18 | Incomplete | Minor | All 8 use cases, Diagram and Mock-ups | No SSD, activity diagram or mock-up in any use case. All say "No separate interaction diagram is included". | Ali |
| 19 | Invalid | Minor | All 8 use cases, Actors | "GMS (system)" is listed as an actor. | Ali |
| 20 | Untraceable | Minor | All 8 use cases | Preconditions and postconditions are not numbered (PRE-n, POST-n) and steps are not split into user and system actions, which makes them hard to reference from tests. | Ali |
| 21 | Incomplete | Minor | All 8 use cases, Alternative Flows and Exceptions | Alternative flows and exceptions do not say which step they branch from or return to. | Ali |
| 22 | Inconsistent | Minor | `uc/3.1.1` Frequency of Use | "Twice per year", but each of the 4 programs has its own call. | Syed |
| 23 | Incomplete | Minor | `uc/3.1.1` Success Scenario | No step where the grant cycle is actually created. | Ali |
| 24 | Ambiguous | Minor | `uc/3.1.1` Postconditions | Too general. Does not state exactly what exists afterwards (e.g. a call with status Open). | Ali |
| 25 | Ambiguous | Minor | `uc/3.1.1` Alternative Flow 2 | Revising a call is large enough to be its own use case. | Ali |
| 26 | Inconsistent | Minor | `uc/3.1.1` YAML and Evidence | DEAN-09 is cited in the Evidence section but missing from the YAML related-evidence. | Mahreen |
| 27 | Incomplete | Minor | `uc/3.1.1` Success Scenario | No step checks that a program is configured in its correct cycle (BR-2: MRG and JF in October, DF and SRG in February). | Hana |
| 28 | Ambiguous | Minor | `uc/3.1.1` Alternative Flow 2 | "Subject to an agreed policy" for impact on existing submissions is undefined and not marked TBD. | Hana |
| 29 | Untraceable | Minor | `uc/3.2.1` Quality Requirements | Does not refer to 6.5 Security, although the use case handles applications and uploads. | Ali |
| 30 | Incomplete | Minor | `uc/3.2.1` Preconditions | Does not say how eligibility is determined (APP-08: rank and unit). "Subject to confirmation of its precise criteria" cannot be tested. | Syed |
| 31 | Unverifiable | Minor | `uc/3.2.1` Quality Requirements | "Word/PDF compatibility should be maintained" names no formats or size limits. | Syed |
| 32 | Incomplete | Minor | `uc/3.2.1` Exception 3 | Enforces one application per program per applicant (RO-08), but no business rule states it. | Mahreen |
| 33 | Incomplete | Minor | `uc/3.2.2` Step 5 | Confirms receipt but does not send an email acknowledgment (APP-02, BR-16). | Syed |
| 34 | Ambiguous | Minor | `uc/3.2.2` Actors, Step 3 | Chair endorsement is required here and the Chair is listed as an actor, but the Chair does nothing in this use case. Link to 3.3.1 is unclear. | Ali |
| 35 | Invalid | Minor | `uc/3.2.2` YAML questions | The listed question is a note, not a question. | Ali |
| 36 | Ambiguous | Minor | `uc/3.2.2` Flows | Several steps are too general and should be split into specific steps. | Ali |
| 37 | Inconsistent | Minor | `uc/3.2.2` Assumptions | Says late-submission rules will be settled with the RO and CoR Chair, but RO-07 already answers it. | Ali |
| 38 | Invalid | Major | `br/BusinessRules.md` BR-5, `uc/3.2.2` Exception 2 | BR-5 rejects all late submissions, but RO-07 says late applications are accepted unless already sent to the committee. Rule is written as final. | Mahreen (also Ali) |
| 39 | Unverifiable | Minor | `uc/3.2.2` Quality Requirements | "Submission acknowledgment and status must be clear to the applicant" cannot be tested. | Mahreen |
| 40 | Inconsistent | Minor | `uc/3.2.2` YAML and Evidence | APP-07 is cited in the Evidence section but missing from the YAML related-evidence. | Mahreen |
| 41 | Ambiguous | Minor | `uc/3.3.1` Exception 1 | Unclear whether this is an exception or an alternative flow. | Ali |
| 42 | Incomplete | Major | `uc/3.3.1` | No flow for a Chair who does not respond (no reminder or escalation). APP-01 says the wait is unpredictable and requires nagging. | Syed |
| 43 | Unverifiable | Minor | `uc/3.3.1` Exception 2 | "The team uses an authorized existing signature process" describes the team, not the system, and cannot be tested. | Syed |
| 44 | Incomplete | Minor | `uc/3.3.1` Exception 1 | Nothing says how the system knows the applicant's department or Chair. | Mahreen |
| 45 | Invalid | Minor | `uc/3.4.1` Actors | Research Officer is the primary actor, but the system performs almost every step. | Syed |
| 46 | Unverifiable | Minor | `uc/3.4.1` Step 2 | Checks "permitted lengths", but no lengths are defined anywhere in the SRS. | Syed |
| 47 | Inconsistent | Major | `uc/3.4.1`, `uc/3.2.2` Step 3 | Completeness is checked in both 3.2.2 and 3.4.1. Unclear which use case owns validation and when the RO is involved. | Ali |
| 48 | Ambiguous | Minor | `uc/3.4.1` Step 4 | "Flagged or uncertain cases" does not define "uncertain". | Mahreen |
| 49 | Ambiguous | Minor | `uc/3.4.2` Exceptions 1 and 2 | The two exceptions look the same and the difference is unclear. | Ali |
| 50 | Inconsistent | Major | `uc/3.4.2` Step 5, BR-9 | "Permitted submission period under the current policy" is undefined. BR-9 requires corrections before the deadline, but RO-02 and RO-07 say late corrections are accepted. | Syed |
| 51 | Incomplete | Minor | `uc/3.4.2` Exception 2 | Does not say which states prevent corrections. | Syed |
| 52 | Unverifiable | Minor | `uc/3.4.2` Quality Requirements | "Correction reasons must be specific and understandable" cannot be tested. | Mahreen |
| 53 | Incomplete | Minor | `uc/3.4.2` | No time limit or reminder when an applicant does not respond to a correction notice (RO-03). | Mahreen |
| 54 | Invalid | Major | `uc/3.5.1` | Adds reviewer assignments, but CHAIR-03 says every member reads all 30–40 applications. | Syed |
| 55 | Inconsistent | Minor | `uc/3.5.1` Alternative Flow 2 | Printable packages have no handling rule, which conflicts with confidentiality in BR-18. | Syed |
| 56 | Incomplete | Minor | `uc/3.5.1` Preconditions | RO being logged in and authorized is not stated as a precondition. | Ali |
| 57 | Incomplete | Minor | `uc/3.5.1` Postconditions | Does not state that distributed applications receive a Distributed status. | Ali |
| 58 | Invalid | Minor | `uc/3.5.1` | Possibly outside draft scope, since distribution may be the start of review. Open question for the authors. | Mahreen |
| 59 | Invalid | Minor | `br/BusinessRules.md` BR-11 | Conflict-of-interest rule is wider than the evidence. CHAIR-07 says it only applies when the applicant is on the committee. | Mahreen |
| 60 | Incomplete | Minor | `uc/3.5.1` | Reviewers are given access but are not notified that applications are ready. | Hana |
| 61 | Invalid | Major | `uc/3.5.2` | Covers committee scoring, which the instructor excluded from the draft (features up to and excluding review and adjudication). | Mahreen |
| 62 | Unverifiable | Major | `datareqs/4.3` | Requirements are not measurable: no purge deadline after 3 years, no backup frequency, no recovery time. DR-4.3-01 to 05 mostly repeat the use cases. | Syed |
| 63 | Incomplete | Major | `datareqs/4.3` | Does not say how initial data (faculty, eligibility, program limits, committee members) is acquired. No audit trail or lock after submission. | Syed |
| 64 | Unverifiable | Minor | `datareqs/4.3` DR-4.3-08, DR-4.3-11 | Backup schedule and purge procedure are deferred to IT and cite the Vision and Scope instead of an interview. Cannot be tested as written. | Ali |
| 65 | Untraceable | Minor | `Main.md` 4.3 link | Opens the empty file 4.2.AcquisitionIntegrityRetentionDisposal instead of the completed 4.3 file (link inherited from template). | Mahreen |
| 66 | Inconsistent | Minor | `datareqs/4.3` DR-4.3-09, BR-19 | Three-year retention conflicts with APP-05 asking for deletion after two years. The conflict is not mentioned. | Mahreen |
| 67 | Incomplete | Minor | `datareqs/4.3`, `ifaces/5.2`, `qualities/6.5` | Files have no YAML header (Term Project 7.2.1). | Hana |
| 68 | Incomplete | Minor | `ifaces/5.2` | No sequence diagrams for the interfaces. | Ali |
| 69 | Inconsistent | Minor | `ifaces/5.2`, `qualities/6.5` | 5.2 names Google Authenticator as the 2FA method, but 6.5 only says "the required two-factor authentication mechanism". | Ali |
| 70 | Invalid | Minor | `ifaces/5.2` SI-5.2-03 | Export to Accounting happens after adjudication, so it may be outside the draft scope. | Ali |
| 71 | Incomplete | Minor | `ifaces/5.2` | No email interface, although BR-16 and use cases 3.2.2, 3.3.1 and 3.4.2 send notifications and IT-07 requires email to any address. Belongs in 5.4, to be added later. | Syed |
| 72 | Incomplete | Minor | `ifaces/5.2` | Does not say what data is exchanged, in which direction, how often, or what happens if the other system is down. | Syed |
| 73 | Untraceable | Minor | `Main.md` 5.2 link | Points to `ifaces/5.2.SI`, which does not exist. The file is `5.2.SoftwareInterfaces.md` (link inherited from template). | Mahreen |
| 74 | Untraceable | Minor | `ifaces/5.2` SI-5.2-01 to 03 | Cites only the Vision and Scope, not the IT interview (IT-01, IT-02). Also unclear that roles are managed inside the GMS, not Keycloak (IT-02). | Mahreen |
| 75 | Incomplete | Major | `qualities/6.5` | No CRUD authorization matrix, and nothing says who assigns roles (IT-02). | Syed |
| 76 | Incomplete | Minor | `qualities/6.5` | No audit logging requirement, although 3.3.1 asks for an auditable endorsement status and IT-04 says logging would be prudent. | Syed |
| 77 | Unverifiable | Major | `qualities/6.5` QR-6.5-01 to 04 | No measurable criteria: no encryption standard, failed-login lockout or session timeout. | Mahreen |
| 78 | Invalid | Minor | `br/BusinessRules.md` BR-12 to BR-14 | Rules cover scoring and decision letters (after review). Nothing in the draft uses them. | Ali |
| 79 | Incomplete | Minor | `evidence/` | Evidence files read like summaries, not interview transcriptions. | Ali |
| 80 | Untraceable | Minor | `br/BusinessRules.md` | No business rule cites its source, although the file says sources use codes like DEAN-nn. | Syed |
| 81 | Untraceable | Minor | `br/BusinessRules.md` top | Template placeholder "BR-1 – Business Rule 1 / Rule Description" left in. Two BR-1 headings, so BR-1 links jump to the placeholder. | Mahreen |
| 82 | Ambiguous | Minor | `br/BusinessRules.md` BR-10, BR-15 | BR-10 hides all comments from applicants, but BR-15 allows "authorized feedback" without defining it. APP-06 asks for written comments. | Mahreen |
| 83 | Incomplete | Minor | `br/BusinessRules.md` BR-4 | Eligibility marked "still to be confirmed", but APP-08 says rank and unit determine eligibility. | Mahreen |
| 84 | Inconsistent | Minor | `evidence/stakeholder*interview.md` headers | Codes described as "cited from Appendix B", but the files are Appendix D. Appendix B is Business Rules (Term Project 7.1). | Mahreen |
| 85 | Inconsistent | Minor | `Main.md` Domain Evidence | Appendix order does not match files: D.1, D.3, D.4, D.5, D.2. | Mahreen |
| 86 | Incomplete | Minor | `evidence/stakeholder*interview.md` YAML | Interview dates are a placeholder range "[2026-10-10 – 2026-11-06]" instead of real dates. | Mahreen |


## Typo List

| Location | Typo | Correction |
| -------- | ---- | ---------- |
| `Main.md` 2.5 | Dependancies | Dependencies |
| `Main.md` 1.3 | email motivated | email-based |




--- 
*Copyright © 2001 by Karl E. Wiegers. Permission is granted to use, modify, and distribute this document.*
