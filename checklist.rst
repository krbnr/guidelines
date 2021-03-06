Project's checklist
-------------------

Purpose
=======

Foster continuous improvement within Sophilabs, by promoting a self-critical culture that thrives on welcoming and adapting to change. To do so, each Squad operates through basic quality tools (such as customized checklists), allowing each project a thorough process-alignment analysis against best practices for specific knowledge-domains like: Security, Software Design, Methodologies, etc.

Checklists are built on top of a simplified "Objectives & Key Results" approach, where expected results align with best practices and are validated by specific questions. In consequence, deviated results are visible and suggested action plans can be assessed and implemented.

E.g.: "Does every team (and team member) subscribes to Agile management practices? - If not, assistance can be requested from the Agile Master to assess the team's knowledge gaps and implement Agile awareness workshops"


Security Checklist
==================

Please fill this document with items every project should complete according with the Security squad.
i.e.: configuring tools, make sure something is being use, make sure some methodology is being applied, etc...


Testing Checklist
=================

- Are you actively writing and running unit tests in your project?
    - If not, you can read the following guides for
      `Django </testing/automated/frameworks-and-libraries/django/README.rst>`__ and
      `React </testing/automated/frameworks-and-libraries/react/README.rst>`__.
- Are you actively writing and running load tests in your project?
    - If not, checkout Apache's `JMeter <https://jmeter.apache.org/>`__.
- Are you actively measuring your code coverage?
    - If not, there are several options depending on your technology stack. Check out our guidelines, if your technology isn't included feel free to add it!
- Do you run code coverage measurements automatically for each merge request?
    - If not, and you are using Gitlab, check out the `Gitlab documentation <https://docs.gitlab.com/ee/ci/>`__ for further information about continuous integration.
- Do you prevent merging pull requests (or building) if team-defined criteria are not met? (For example: coverage percentage below 90%)
    - See previous suggestion.
- Do you run tests automatically in each merge request and prevent merging (or building) if they fail?
    - See previous suggestion.
- Did you write your testing setup in the *manifiesto file* and are actively updating it?


Deployment Checklist
====================

- Are you using a version control system?
    - Every project must use a VCS. `Git <https://git-scm.com>`__ is our preferred VCS and we use `GitHub <https://github.com>`__ for open-source projects and `GitLab <https://gitlab.com>`__ for proprietary projects.
- Are you using a containerization or virtualization system?
    - In order to improve the project flexibility and portability we recommend using  `Docker <https://www.docker.com>`__.
- Are you using continuous integration?
    - A continuous integration service eases the development workflow by automating tasks such as testing and deployment. Please take a look at  `GitLab CI <https://about.gitlab.com/features/gitlab-ci-cd/>`__ and  `Jenkins <https://jenkins.io>`__.
- Are you using a staging server for development branch releases?
    - If not, set up a staging server to improve the project visibility and the development process.
- Does your project have a rollback plan?
    - If not, schedule a meeting with your team in order to create and document a rollback plan.
- Is the deployment process well documented?
    - If not, schedule a meeting with your team in order to determine and document the end-to-end deployment process, tools and activities.

Methodologies Checklist
=======================

- Does your team have a clear grasp of the `Agile <https://playbook.sophilabs.io/#the-agile-way>`__ management principles?
    - If not, schedule your team's attendance to upcoming "Agility" workshops. Or directly reach out to your Agile Master for advice or definition of a more comprehensive Agility roadmap
- Is `Customer <https://playbook.sophilabs.io/#customer-availability>`__ inclusion a natural consideration and ocurrence in your  team's value-creation process?
    - If not, engage and bring them closer to the product creation process. Customer inclusion is essencial for delivering the greatest and most "fit-for-purpose" product
- Does your team receive a clear `Product Vision <https://playbook.sophilabs.io/#understanding-product-vision>`__ from the customer (focusing in value-added tasks)?
    - If not, refer to the previous point. Customer inclusion helps refine a comprehensive and clear Product Vision, allowing teams to add the most value posible in early stages
- Does your team always deliver committed work by the agreed upon schedule with quality?
    - If not, track your team's performance artifacts (account for team's capacity & velocity). Also, consider assessing your planning, estimation and engineering practices. Reach out to your Agile Master for further assistance
- Is the work performed by your team appropriately tracked and visible to all in a sensible way?
    - If not, foster team members creation of traceable `Tasks <https://playbook.sophilabs.io/#tasks>`__ for every work item done (on Jira, Trello, Github, etc.) with sufficient detail (e.g. Description, Priority, Reporter, Start Date/Time, End Date/Time)
- Is your team continuously improving the product being created and the process value-stream behind it? 
    - If not, make sure your team meets often to inspect, adapt and continuously improve (Planning, `Daily Stand-Ups <https://playbook.sophilabs.io/#standups>`__, Reviews and `Retrospectives <https://playbook.sophilabs.io/#biweekly-retrospective>`__)
- Is your team flexible, readily adapting to product changes leveraged by the customer?
    - If not, focus team efforts on always adding value; automate or remove repeatable and/or time-consuming tasks according to their value-yield. Consult your Agile Master about agility-boosting strategies for your team


Software Design Checklist
=========================

Every project must have:

- Documentation
    - `High-level design <https://en.wikipedia.org/wiki/High-level_design>`__
    - `Class Diagram <https://en.wikipedia.org/wiki/Class_diagram>`__
    - `Entity relationship model <https://en.wikipedia.org/wiki/Entity%E2%80%93relationship_model>`__
- Development Process
    - At least 2 team members must be involved on the component design within a project
    - Validate designs with other team members
    - Reach experienced developers for guidance


Code Analysis Checklist
=======================

- Does the authored code in the project complies with the respective code style guidelines? (This excludes third party code, such as library, files in the `node_modules` directory, or autogenerated code.)

  - If not, you can use linters tool to verify code style guidelines. If you are in doubt about which tool you should use, refer to each language guidelines page. e.g. `Javascript <https://guidelines.sophilabs.io/languages/javascript/>`__, `Python <https://guidelines.sophilabs.io/languages/python/>`__, `Sass <https://guidelines.sophilabs.io/languages/sass/>`__.

- Do commit messages follow a defined format respected by all team members?

  - If not, you could define Commit Message guidelines. For example ``/#\d+: [A-Z](\w|\s)*/`` (i.e. #555: Fix typo in guideline). You may find this `article <https://chris.beams.io/posts/git-commit/>`__ useful.

- Does the project have an automatic way to verify the compliance of code guidelines and commit messages?

  - If not, you can use commit hooks to verify the code style guidelines and the commit message by overriding the following files ``.git/hooks/pre-commit`` and ``.git/hooks/commit-msg`` respectively. Check out this `article <https://www.atlassian.com/git/tutorials/git-hooks>`_ to learn more about Git hooks.

- Does the project follow a clear branching strategy, like `Git Flow <https://danielkummer.github.io/git-flow-cheatsheet/>`_? This includes:

  - Having the master branch (or the equivalent) protected, meaning all commits must be merged from feature branches.
  - Ensuring every commit must be made inside a particular branch that encapsulate that particular task. - If this not the case, you can ask the Code Analysis Squad for assistance to implementing a branching strategy in your project.

- Is the submitted code in the master branch reviewed by other team members before committing?

  - If not, you can implement Code Reviews, which is a practice to ensure code quality and attachment to the `guidelines <http://vintage.agency/blog/how-to-implement-code-review-process-in-a-web-development-team/>`__. As a rule of thumb:

    - Code reviews must be enforced before merging code to the master branch.
    - Code reviews should follow the `guidelines </programming/code-reviews.rst>`_ in the Sophilabs Playbook.

- Does your project have documentation for new hires explaining the Tools needed for work and processes involved in the everyday work?

  - If not, you should consider having a `README <https://gist.github.com/PurpleBooth/109311bb0361f32d87a2>`__ and a `Contributing <https://gist.github.com/PurpleBooth/b24679402957c63ec426>`__ guidelines file in the root of your project. Those files can include:

    - Development tools: Text editors, IDEs, Plugins.
    - Required environment files.
    - Procedures for installing Hooks.
    - Naming conventions.
    - Common design patterns used in the code.

