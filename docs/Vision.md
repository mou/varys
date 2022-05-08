---
title: Vision
tags:
  - varys
  - documentation
  - concepts
---

In recent years, there has been a clear change in attitudes towards information security issues. Regardless of industry, country or scale, companies are implementing more and more best practices in the field of information security.

Today, it is less and less common to find a situation of storing credentials or other secrets in software source codes. Depending on the requirements, companies implement software and hardware solutions for storing sensitive information. They allow them minimize the access of employees or other people to such data, and as a result reduce the risks of compromise.

However, this subject area has not only technical tasks, but also process and organizational ones. But unfortunately, systems for storing credentials and sensitive information, at best, allow you to determine the conditions of rotation and access rights. And even if they provide possibility to attach metadata to secrets, there are no tools to query them or to build some managements solution on top of.

The idea of Varys is to provide a tool for tracking and accounting of sensitive information without affecting the operation of systems where they are stored. The main questions that Varys should help answer are:

* When and by whom was the secret registered? To whom can I address questions about him?
* Which system is the secret used to access? Which systems use it?
* When does secret expire?
* Where is this secret mentioned (code, documentation)?
* What secrets urgently need updating or transfer of responsibility for them in connection with the resignation of the responsible person?
* Who, in a third-party organization, should I call or write to in case of problems with credentials or secrets?
  and many others
