# Blog des Lauréats — Project Framing Document

## 1. Présentation du Projet & Contexte Institutionnel

### Project presentation

**Blog des Lauréats** is a digital platform that lets former students share their success stories and useful experiences. It has two parts:

- **Website (Web):** Administrators publish, edit, organize, and manage articles. The public can read stories and discover former students.
- **Mobile application:** Learners and visitors can browse and read articles easily from their smartphones.

**Simple example:** A student finishes training, gets a good job, and becomes successful. They write an article to explain how they reached that goal. Other students read the article and learn from this real experience.

### Institutional context

The project is created for a training center like Solicode. The center has many learners and former students, but their success stories may not be easy to find or share. The platform gives these stories one simple and organized place.

The project does not include building or coding the website or mobile application in this document. This document only defines **what must be done, why it is needed, who is involved, and what risks may happen**.

### Main expected features

- Public pages to display published articles
- Articles organized by category, theme, or promotion
- Search and article detail pages
- Administrator access to create, edit, publish, archive, and delete articles
- Mobile-friendly reading for smartphones
- Contact or sharing options if confirmed as useful

## 2. Objectifs Stratégiques & SMART

| ID | SMART objective | Success measure | Target date |
|---|---|---|---|
| O1 | Inspire current learners with real success stories. | Publish at least **12 quality articles** by former students. | Before the final project launch |
| O2 | Make content easy to discover on the web. | Allow users to find an article by **title, category, or keyword** during acceptance tests. | Before user testing |
| O3 | Give administrators a simple content workflow. | An authorized administrator can create, edit, publish, and archive an article in **less than 10 minutes**. | Before training and delivery |
| O4 | Provide a useful mobile reading experience. | The mobile app passes **basic usability tests on 3 common smartphone sizes**. | Before mobile validation |
| O5 | Keep content accurate and professional. | **100% of published articles** are reviewed and approved before publication. | Continuously |
| O6 | Protect user and administrator information. | No unauthorized person can access administrator functions or published user data. | Before production |

### Strategic goals

1. Increase motivation by showing real careers and journeys.
2. Improve the center's visibility and reputation.
3. Preserve useful experience from former students.
4. Help learners make better career choices.
5. Build one clear communication channel for web and mobile users.

## 3. Matrice de Périmètre (In-Scope / Out-of-Scope)

| Area | In-Scope | Out-of-Scope |
|---|---|---|
| Web platform | Public article pages, article search, categories, article details, responsive design | Native desktop applications or separate social network platform |
| Mobile application | Reading articles, navigation, search, simple responsive interface | Creating or publishing articles inside the mobile application |
| Administrators | Create, edit, preview, publish, archive, and manage articles | Full technical server administration and infrastructure sales |
| Content | Former-student profiles, success stories, images, categories, and article tags | Unverified news, illegal content, or advertising campaigns |
| User experience | Simple navigation, clear titles, readable pages, and basic accessibility | Advanced personalization or artificial-intelligence recommendations |
| Comments and interaction | Only if requested and approved | Public forums and complex social messaging |
| Security | Login for administrators, role-based access, input validation, backups | High-level security certification or intrusion testing as a separate service |
| Project documentation | Planning, requirements, stakeholder list, risks, and acceptance criteria | Detailed technical implementation in this current phase |

### Scope rule

A feature is in scope only if it is needed for the main goal: **publish real success stories and allow learners to read them on web and mobile**. Features that are not approved by the Product Owner should not be started.

## 4. Parties Prenantes

| Stakeholder | Role | Interests and responsibilities |
|---|---|---|
| Product Owner — Group 1 | Main decision-maker | Validate scope, priorities, requirements, and final planning document |
| Project manager / Scrum Master | Organize the team | Plan meetings, remove problems, and track progress |
| Development team | Build the platform later | Develop, test, document, and report blockers |
| Junior developers | Implement assigned tasks | Follow priorities and ask for help early when blocked |
| Administrators / Content managers | Manage articles | Create, review, publish, edit, and archive valid stories |
| Former students (Lauréats) | Content providers | Share accurate and approved success stories |
| Learners and current students | Main readers | Read articles and provide feedback on usefulness |
| Visitors | Public readers | Browse public stories easily |
| Training center management | Institutional sponsor | Support communication and approve institutional use |
| Teachers and coaches | Mentors and reviewers | Help validate content and guide learners |
| Communication / Marketing team | Promotion | Share valuable articles with the right audience |
| Security / Technical support | Technical support | Help protect accounts, data, and availability if needed |

### RACI summary

- **Product Owner:** Responsible for acceptance and priorities.
- **Project team:** Responsible for analysis and future implementation.
- **Administrators:** Responsible for daily content quality.
- **Former students:** Responsible for the accuracy of their own stories.
- **Management:** Accountable for institutional approval and resources.

## 5. Risques Identifiés & Stratégies d'Atténuation

| Risk | Probability | Impact | Main effect | Mitigation strategy |
|---|---|---|---|---|
| Too many features are requested. | Medium | High | Delays and confusion | Use the scope matrix, rank features, and require Product Owner approval for changes. |
| Articles have low quality or wrong information. | Medium | High | Loss of trust | Create a review process; teachers or an editor must validate each article. |
| Former students do not provide stories. | Medium | Medium | Few articles at launch | Prepare a simple submission form, a clear example, reminders, and a small writer group. |
| The web and mobile versions look different. | Medium | Medium | Confusing user experience | Use a shared design system and agree on common screens before development. |
| Administrator accounts are compromised. | Low | High | Unauthorized changes or data loss | Use strong passwords, role-based access, HTTPS, and regular backups. |
| Personal or sensitive information is published. | Medium | High | Privacy and legal problems | Ask permission, remove sensitive data, and obtain final approval before publication. |
| Development becomes too complex. | Medium | High | Missed deadlines | Split work into small tasks, build a simple first version, and test it regularly. |
| The application is slow or unavailable. | Low | Medium | Users stop using it | Use image compression, caching, monitoring, and simple hosting for the expected load. |
| Mobile design does not work on older phones. | Medium | Medium | Difficult reading | Test on several common screen sizes and keep the interface lightweight. |
| Team members leave or become unavailable. | Low | High | Progress stops | Share tasks and documentation; keep one backup person for each critical area. |
| Requirements change after work starts. | High | Medium | Rework and delays | Record all changes, estimate their cost, and accept only approved changes. |
| Copyright or image permission is missing. | Medium | Medium | Legal and reputational risk | Use only owned or properly licensed images and keep written permission from contributors. |

### Risk rules

1. Review major risks every week during project meetings.
2. Assign one person to follow each important risk.
3. Stop and report the risk if it can affect scope, security, quality, or the launch date.
4. Update the mitigation plan after every significant change.
