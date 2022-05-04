# learning-schdule

1. https://www.freecodecamp.org/news/what-is-debugging-how-to-debug-code/
2. https://nextjs.org/learn/foundations/about-nextjs

## Visualstudio Code
Set default termminal:https://neutrondev.com/vs-code-integrate-git-bash-default-terminal/

## Thinking like a programmer
1. Methodical thinking - more orderly thinking
2. Break problems down - decomposition
3. Think algorithmically - steps to achieve outcome

## Problem solving
1. Define your problem
2. Make sure you've fully understood the problem
3. Break the problem down into small and manageable piece
4. Go as deep as you can until you can get to easy yes or no questions
5. Work yourway up from the bottom until the problem is solved

https://www.youtube.com/watch?v=x77-gT8bWLo


https://www.youtube.com/watch?v=UFc-RPbq8kg

## Courses
https://www.udemy.com/course/nextjs-react-the-complete-guide/

## TDD
Three types of TDD


· fake it to make it - minimum increment until finished

· obvious implementation - if clear what logic is needed

## Techdesign
📜 Context

The team have been working on

which looks to provide a way to get access to protected cloudfront environments via OTS urls generated from our Cookie Cutter Application.

As part of this we’ve re-configured our applications with cookie cutter integration to not be publicly accessible unless Cookie Cutter grants access. This has meant our CI runners which typically interacts with our applications post deployment can no longer test journeys end to end. This ticket looks to ensure our CI can execute successful Smoke Tests (i.e. 200 OK) for our application.

✅ Acceptance Criteria

·        Hello World Smoke Tests validate that the application is successfully deployed.

In Scope

·        Hello world smoke tests

·        Ephemeral environments

Out of Scope

·        DAST tests in Hello World

·        JISA Smoke tests

·        Dev Main Environment

·        DNS verification

 

📐Technical Design

Work to help understand what technical work needs to be carried out on this ticket, you may want to consider, as examples;

·        Scenarios (these should be limited to a particular path, happy, sad, alternative)

·        Sequence Diagrams

·        UML Diagrams

·        C4 Diagrams

·        What security concerns need to be thought about

·        How you may deploy this application (through IaC)

·        What tests you need and how to implement these

·        What technologies you may need

·        Potentially drafting API specifications

·        Potentially drafting ADRs around any decisions

·        Whether or not you first need to answer questions via Spike

·        What dependencies you may have on others

❔ Questions

Questions
	

Answers

What is love?
	

Baby don't hurt me

—

📝 Notes

📗Glossary

Term
	

Definition

🔗 Links

· triangulation - 2 tests to prove functionality

Tools

IDEs can generate code if function doesn't exist of needs to be imported


Requirements
 
When naming variables the requirements can help, it's best to use the same terminology etc as the business

## Presentation skills
Presenting is highly regarded transferable skill

Enhances reputation and networking skills

 

**Presentation do's**

Prepare

Practise

Know your audience - what language to use

Use examples and stories to transform our communications

Have a clear, defined structure

Visual aids and imagery can further the engage the audience

Remember to check your tone and pace

Keep text on slides to a minimum - people talk fast when nervous, short sentences allow pauses and keeping pace

 

 

**Presentations don't**

Don't be afraid to go off-piste

Do not read directly from the slides

Use jargon/technical language

Don’t try to force humour during the session

If you stumble then carry on - it's likely the audience won't have noticed

 

 

 

When using images, don't clutter the page, make any text easy to read not in several places

 

**The introductions**

Set the scene at the start

Why should they listen?

Housekeeping - timing and question handling

Nailing the intro boosted your confidence

 

 

**Delivery**

Confidence

Pace

Tone

 

**Nervousness**

A slight degree of nervousness is positive

Preparation and practise

Nail your introduction

Anticipate what's causing nerves

 

**Virtual presenting**

Look into the camera

Smile

Structure the session like a story

If appropriate use the interactive tools

 

**Key 4 tips**

Be confident - nail the introduction

Page your delivery

Be enthusiastic, get engagement

practice


## OWASP

**Invalidate redirect**

When a redirect send users to a different site than they wanted to go to.

When using redirects use history.pushState() as it doesn't allow different host sites to be passed in.


**Cross site request forgery CSRF**

Tricks users to doing things on sites they've logged into

The token is a random generated string and should be transferred to the server with requests

Before sending data for things like purchases confirming a client password or secret can prevent csrf

Unprotected transport of credentials

Data is transported as plain text

Use ssl (https) on requests, make sure this is used in all requests


**Code injecting**

User code is executed on the server

Don't use eval, use json.parse


**HTTP injection**

CRLF - insert an encoded crlf in a url allowing manipulation of server files


**Reflected cross site scripting**

Email is sent with script tags which aren't validated

Don't allow any client code to be run, it must be interpreted as a string


**Threat modeling**

Assets - what needs to be protects

Vulnerabilities

Threats - potential damages

Threat agents


**Assement**

Threat agent identitifications

Threat identification

Threat prooritization

Remediation of threats

 

Most effect when done early

 

**S.T.R.I.D.E**

Threat modeling methodology

Application designers, developer tests and security experts

 

|Threat | Desired property|
|------- | ---------------|
|Spoofing | Authentication|
|Tampering | Integrity|
|Repudiation | non-repudiation|
|Information disclosure | Confidentiality|
|Denial of service | Availability|
|Elevation of privilege | Authorization|

**Logical Error**

Business logic used to exploit vulnerabilities

Business rules need to be clearly defined
 
**Information Exposure**

_What is it?_

Configuration is insecure and can be overwrote

_Causes_

Misconfiguration happens when no secure configuration has been applied to the frameworks, application server, web server, database server or the platform of the application.

_Prevention_

* Define `secure settings` and implement a process to deploy them on all parts of the system.

* Implement a process to keep all software up to date. This should involve running automates scans and performing audits on a regular bases to help detect misconfigured parts of the system.

* Ensure that a strong application architecture is put in place. This should include effective, secure separation between components.

_Hazards_

Exposure of private and client information.

Can prevent access to services

**Using Known Vulnerable Components**

_What is it?_

Occurs when an application uses third-party libraries, frameworks, components or other software that is out of data and contains published vulnerabilities.

_Causes_

This vulnerability occurs because low priority is usually given to ensuring that used libraries and components are up to date.

Dependencies can further complicate the effort of using the most secure components.

_Prevention_

* Implement a process to manage the security of third-party software including identifying third party components, their versions and dependencies. Check them regularly against vulnerability lists and update them when needed.

* Subscribe to cyber-security related mailing lists from Information Security (InfoSec) sites and software vendors and regularly search vulnerability databases.

* Implement security policies governing components use, to define, evaluate and ensure safety of components. Restrict the use of unused, insecure or unsafe component functionalities

_Hazards_

Exposure to information or system take over, site could be unreachable.


**Using Components From Untrusted Source**

_What is it?_

Adding third party software to applications.

_Causes_

Using software from a third part which has deliberate vulnerabilities.

_Hazards_

Information can go to untrusted sources

_Prevention_

* Set up a patch management process to continually monitor components throughout the software lifecycle

* Acquire components from official sources only, via secure links

* Inventory client and server-side components to check for security, using tools like NVD or CVE

* Remove any unused dependencies and unnecessary features and files

* Used integrity checks to verify that resources from third parties have been delivered without any manipulation

 

When using a third party library use 'integrity' and 'crossorigin' attributes on the script tag
