---
title: Résumé
isTitle: true
template: resume

experience_section:
  experience_section_name: Experience
  subsection:
    - subsection_name: Portworx, Inc.
      job_title: Technical Writer
      tenure: July 2019 - Present
      focus_area:
        - focus_area_name: Product Documentation
          focus_area_list:
            - Write and maintain all documentation for Portworx products
            - Write and publish release notes
        - focus_area_name: Infrastructure
          focus_area_list:
            - Implemented federated search, allowing users to search and see results across multiple products
            - Perform development and administrative tasks for docs.portworx.com
            - Maintain documentation toolchain and versioning
            - Document internal publication procedures
        - focus_area_name: Leadership
          focus_area_list:
            - Manage contractor direct reports, delegate tasks, and oversee progress
            - Create and enforce a style guide for all writers and contributors
            - Copyedit and review all documentation changes before publishing
            - Triage new issues and organize work into sprints
    - subsection_name: Celtra, Inc.
      job_title: Technical Writer
      tenure: July 2018 - February 2019
      focus_area:
        - focus_area_name: Product Documentation
          focus_area_list:
            - Created and maintained support documentation for the Celtra Management Platform
            - Established a documentation team strategy modeled on Agile development approaches
            - Created visually compelling diagrams and illustrations
        - focus_area_name: Infrastructure
          focus_area_list:
            - Performed front end development and administrative tasks for support.celtra.com
            - Created interactive website documentation designs
        - focus_area_name: Video
          focus_area_list:
            - Recorded and produced supplementary support video content
    - subsection_name: Red Hat, Inc.
      job_title: Technical Writer
      tenure: January 2017 - July 2018
      focus_area:
        - focus_area_name: Product Documentation
          focus_area_list:
            - Created and maintained documentation for the Red Hat 3scale API Management Platform
            - Established and maintained documentation infrastructure and repositories
            - "Implemented documentation initiatives: modularity, open sourcing"
            - Created strategic plans for documentation structures
        - focus_area_name: Documentation Project Management
          focus_area_list:
            - Oversaw operation of product portal pages
            - Tracked project status and provided regular readiness reports
            - Liaised with product stakeholders in QE, support, engineering, product management
            - Managed documentation work queue and triage bugs
    - subsection_name: Hewlett Packard Enterprise
      job_title: Information Developer
      tenure: August 2014 - January 2017
      focus_area:
        - focus_area_name: Leadership
          focus_area_list:
            - Established a release publications team
            - Educated and advise team members on release procedures
            - Delegated team tasks for product releases on my.vertica.com
            - Oversaw publication operations
        - focus_area_name: Technical Writing
          focus_area_list:
            - Created and maintained documentation for HPE Software cloud products
            - Provided feedback and edits for other writers
            - Modernized documentation using structured authoring standards
        - focus_area_name: Infrastructure
          focus_area_list:
            - Implemented and reported on analytics for the documentation and community
            - Administered WordPress pages for documentation and product releases on my.vertica.com
            - Assisted in maintenance of internal versioning and documentation systems
        - focus_area_name: Video
          focus_area_list:
            - Recorded and produced product videos and blogs for the developer community
            - Filmed internal meetings and presentations

skills_section:
  skills_section_name: Skills
  subsection:
    - subsection_name: Web Languages and Utilities
      subsection_list:
        - HTML/CSS
        - Sass
        - UIKit
        - Javascript
    - subsection_name: Programming and Query Languages
      subsection_list:
        - Python
        - Javascript
        - C
        - SQL
    - subsection_name: Operating Systems
      subsection_list:
        - Unix
        - Linux
        - Mac
    - subsection_name: Cloud Platforms
      subsection_list:
        - Amazon Web Services (AWS)
        - Microsoft Azure
        - Google Cloud Platform (GCP)

education_section:
  education_section_name: Education
  subsection:
    - subsection_name: University of North Texas
      degree_name: BA Technical Writing
      graduation_date: 2013
---

<!-- ## Nathaniel Wilson -->



{{#

There are a couple ways to do this résumé:

I can have each collection entry be a separate listing. For example...

* job1
* job2
* job3
* school1
* school2
* skill1
* skill2
* skill3

... would result in a collection filled with 8 .md files

Or, I could put all of the information in the frontmatter. So...

* job1
* job2
* job3
* school1
* school2
* skill1
* skill2
* skill3

... would be tables in the frontmatter of a page

I think I'm going to put everything into the page frontmatter. I'm choosing this path because I intend only to ever have a single résumé page.

Things to consider:

* I should set up a fieldset to manage this from the control panel
* I will need to wire up the page with the template to manage how this looks
*

how the resume is organized:

Name

Location

Job title

Contact information

Experience section:
  company:
    time I was there
    job title:
      responsibility/achievement
    second job title:
      responsibility/achievement
  second company:
    time I was there
    job title:
      responsibility/achievement
    second job title:
      responsibility/achievement

Education section:
  institution:
    degree title
    graduation date

Skills:
  type:
    tools/languages
  second type:
    tools/languages

note: I started a resume fieldset and template, I'm going to shelve the fieldset and this page in favor of first hardcoding the resume directly onto the temaplte.

Once I've hardcoded it, I'll migrate the template date into page frontmatter

Once I've got the page frontmatter migrated, I'll finish the fieldset

 #}}
