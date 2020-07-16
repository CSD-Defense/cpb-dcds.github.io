---
title: "DCDS Development Practices"
keywords: development practices
sidebar: mydoc_sidebar
permalink: dev_practices.html
---

## **1 - DCDS Manifesto and 12 Principles**

### **1.1 - Manifesto for Agile Software Development**
> _Individuals and interactions over processes and tools_
> 
> _Working software over comprehensive documentation_
>
> _Customer collaboration over contract negotiation_
> 
> _Responding to change over following a plan_

### **1.2 - DCDS 12 Principles**
1. **Our higher priority is to support operations** through early and
   continuous delivery of valuable software.
2. Welcome changing requirements, even late in development. **Agile
   processes harness change for a competitive advantage in cyberspace
   operations.**
3. **Deliver working software frequently**, from a couple weeks to a couple
   months, with a preference to the shorter timescale.
4. **Mission planners and developers must work together frequently** throughout
   the project.
5. Build projects around motivated individuals. Give them the environment and
   support they need, and trust them to get the job done.
6. The most efficient and effective method of conveying information to and
   within DCDS is **face-to-face conversation**.
7. **Working software used in operations is the primary measure of progress.**
8. Agile processes promote sustainable development. Mission planners and
   developers should be able to maintain a constant pace indefinitely through
   **continuous feedback loops**.
9.  Continuous attention to **technical excellence and good design** enhances
   agility.
11. **Simplicity** – the art of maximizing the amount of work not done – is
    essential.
12. The best architectures, requirements, and designs emerge from teams where
    **technical expertise is valued over military rank**.
13. At regular intervals, the team reflects on how to become more effective,
    then tunes and adjusts its behavior accordingly.

&nbsp;

## **2 - DCDS Daily Standup**
At the beginning of everyday, members of DCDS will participate in a daily stand
up. This is a quick meeting focused on improving efficiency by identifying and
coordinating issues. The desired end state is to remain focused on current
issues, and coordinate between developers if necessary.

### **2.1 - Schedule**
The daily standup occurs from 0930-0945 each day.

### **2.2 - Topics**
While daily standups can cover a variety of topics, some common ones include:
- Blockers
- Daily priorities of work
- Status of current sprint
- Establish/refine any time constraints


&nbsp;
## **3 - DCDS Sprint Planning**
In order to promote successful development operations, DCDS will adhere to the
[DCDS Manifesto and 12 Principles](#1---dcds-manifesto-and-12-principles)
during sprint planning.

There are two collaborative locations that will hold information pertaining to
DCDS sprints. The only open location will be on Confluence. The GitHub
location will primarily hold information to be used by DCDS development
internally. Updates to these locations will happen at separate iterations.
GitHub updates will happen real time with development, while the updates to
Confluence will happen on a weekly basis or as needed. The weekly update will
contain issue validation, and other weekly related updates. This update will
occur on Fridays, or the last day of the duty week.

### **3.1 - Sprints**
DCDS sprints will last 15 working days (~3 weeks).

A sprint will focus on the development **of a single project**. Once a sprint
is complete, DCDS will reevaluate priorities and potentially switch projects.

&nbsp;

### **3.2 - Confluence**

#### 3.2.1 - User Story / Feature Checklist
The primary way DCDS tracks features is through user stories. A user story is
in the general format **`<Type of end-user / customer>`** will do **`<action>`**
in order to **`<accomplish task / meet mission requirement>`**. By constructing
our feature list in this way, it ensures we are always making features with the
end-user in mind.

The User Story checklist will be a living document during the duration of
development on a project. Each Sprint Review and Sprint Planning session will
be focused on the curation this document. Once user stories have been
identified, they are decomposed into tasks and features that map back to user
stories.

&nbsp;

#### 3.2.2 - Sprint Reviews
At the end of each sprint, DCDS will sync with the supported organization /
customer and demo the current state of the project. Ideally, teams will be able
to take this partially complete product and use it on mission and provide
feedback to drive our next sprint.

DCDS will also validate that the subset of features and user stories tackled
during this sprint are fully complete.

&nbsp;

### **3.3 - GitHub**

#### 3.3.1 - Issue Template
Internally, we use issue templates to document user stories, features, and bugs
on our issue board. Each issue is labeled, and depending on the label, a
certain issue template is used to have relevant information such as logs,
problem description, external references, etc.

&nbsp;

#### 3.3.2 - Sprint Board
Sprints are mapped to milestones. A milestone is a way to group issues within a
specific start and end date. Since sprints have a start date and end date,
using sprint boards that filter based on milestone enables us to easily see the
list of issues that we plan to accomplish during a given sprint.

&nbsp;

#### 3.3.3 - Issue Weights and estimated weights vs actual weights
Issue weights are a rough estimate of the complexity of an issue. **Issue
weights do not represent the amount of time estimated to complete an issue.**
Instead, reference stories are created for each type of issue that the team
uses internally as a relative reference on the amount of work.

Issue weights roughly follow the Fibonacci sequence from 1 to 100 (1, 2, 3, 5,
8, 13, 21, 34, 55, 100) to estimate technical complexity. An issue with a
complexity of 21 is roughly 20 times harder than an issue with a complexity of
1\. An issue with a complexity of 8 is roughly 2.5 times as difficult as an
issue with a complexity of 3. These relative abstractions of complexity,
independent of time, are useful to prevent us from falling into the trap of
generating inaccurate time estimates.

&nbsp;

#### 3.3.4 - Pull Request templates
Once an issue has been completed, a pull request is created to merge the new
feature or bug fix into the master branch. The default pull request template
ensures that all relevant information about the pull request is captured for
the reviewer that approves the pull request.

&nbsp;

## **4 - DCDS Documentation**
The README.md should be placed at the root level of the application repository.
All other documentation should be placed in a root-level docs/ folder.

### **4.1 - README.md**
The README file is the starting point for all documentation. A good README file
provides a clear and concise description of the the purpose of the application,
how to install it, and example usage. The README should also contains links to
the other pieces of documentation defined below.

&nbsp;

### **4.2 - GettingStarted.md**
The GettingStarted file should provide a streamlined set of instructions for
taking a brand new device and getting the application running. For example, if
the application is written in Python and uses a virtualenv, the GettingStarted
document should provide instructions for how to install Python, create a
virtual environment, install dependencies in the virtual environment, and run
the application with default settings.

&nbsp;

### **4.3 - Requirements.md**
The Requirements file contains the user requirements from the customer. This
document should evolve over time with the agile development of the application.

&nbsp;

### **4.4 - Design.md**
The Design file should describe the application architecture and design. It
should focus on making it clear how the application fulfills the requirements
defined in the Requirements file.

&nbsp;

### **4.5 - UserGuide.md**
The UserGuide file should contain an in-depth description of how to use the
application. All configuration options, testing procedures, and installation
instructions should be documented in detail.

&nbsp;

## **5 - DCDS DevSecOps**

### **5.1 - Containerization**
The advent of containers is one of the most impactful technologies in the past
decade. Containers enable development teams to create an idempotent build
process, dramatically reducing the number of potential problems that tend to
occur throughout the development lifecycle. DCDS will strive to use containers
as early and as often as possible in order to speed up development and minimize
build up of technical debt between sprints and projects.

### **5.2 - Application Isolation and Dependency Management**
DCDS capabilities should minimize the creation of artifacts on the customer's
infrastructure. They should also not require an unnecessarily complex
installation process with a slew of dependencies and build tools spread across
various directories, potentially altering or overwriting existing libraries and
tools. In order to achieve this goal, DCDS will prefer using virtual
environments and modules available in many common programming languages such as
`virtualenv` for Python, `go.mod` for Go, and `rustenv` for Rust.

### **5.3 - Automation and Packaging**
In order to test our capabilities, DCDS will need to be able to rapidly deploy
complex network and system architectures that represent the customer
environment. To do this, we will use modern infrastructure automation
technologies such as Vagrant, Ansible, and Terraform. When applicable, we will
also use Packer to package these infrastructure components so that, depending
on the infrastructure available, we can deploy our test infrastructure across a
variety of providers.

### **5.4 - Continuous Integration and Testing**
DCDS will automate as much of the testing process as possible in order to speed
up overall development time. To do so, we will leverage the features built into
GitHub to deploy a Continuous Integration / Continuous Delivery (CI / CD)
pipeline that automates a majority of the building and testing process.

&nbsp;

## **6 - DCDS Code Style Guide**

### **6.1 - Python**
- Use [autopep8](https://pypi.org/project/autopep8/) on your code for
  formatting and linting
- Use [Sphinx](https://sphinx-rtd-tutorial.readthedocs.io/en/latest/docstrings.html)
  docstring format
- Use [Pipenv](https://github.com/pypa/pipenv) to manage virtual environments and isolate dependencies per
  project
- Never use Python2

&nbsp;

### **6.2 - Golang**
- Use [Go Modules](https://github.com/golang/go/wiki/Modules) to isolate
  dependencies per project
- Run `go fmt` on your package to format all source code files
- Use [good directory layout patterns](https://github.com/golang-standards/project-layout)

&nbsp;

### **6.3 - JavaScript**
- Use `npm` to manage packages (not `yarn`)
- Commit your `package-lock.json` to GitHub
- Use [ESLint](https://eslint.org/)

&nbsp;

### **6.4 - Dart**
`//TODO`

&nbsp;

### **6.5 - C**
`//TODO`