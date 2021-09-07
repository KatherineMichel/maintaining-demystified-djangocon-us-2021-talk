# Maintaining Demystified- DjangoCon US 2021 Talk

## Table of Contents

- [About](#about)
- [Slides and Script Table of Contents](#slides-and-script-table-of-contents)
- [Slides and Script](#slides-and-script) 
- [Attribution](#attribution)
- [Contact Kati](#contact-kati)
- [Copyright](#copyright)

<hr>

## About

Slides and script for a talk Katherine "Kati" Michel ([Twitter](https://twitter.com/KatiMichel), [GitHub](https://github.com/KatherineMichel)) gave at DjangoCon US Saturday, October 23, 2021.
 
Conference Page
* [DjangoCon US 2021](https://2021.djangocon.us/)

Slide Deck and Video Recording
* [Original slide deck]()
* ["Maintaining Demystified"]()
* [Video recording]()

:top: <sub>[**back to top**](#table-of-contents)</sub>

<hr>

## Slides and Script Table of Contents

- [Maintaining Demystified](#maintaining-demystified)
- [My Affiliations](#my-affiliations)
- [Talk Goals](#talk-goals)
- [Assumptions](#assumptions)
- [Get a Jumpstart on Collaboration and Code Review in GitHub](#get-a-jumpstart-on-collaboration-and-code-review-in-github)
- [Maintaining is Not Just About Code](#maintaining-is-not-just-about-code)
- [Put Yourself in the Shoes of the Contributor; Make Contributing as Frictionless as Possible](#put-yourself-in-the-shoes-of-the-contributor-make-contributing-as-frictionless-as-possible)
- [GitHub Open Source Guide: “A Checklist Before You Contribute”](#github-open-source-guide-a-checklist-before-you-contribute)
- [Some Signs of a Healthy Project](#some-signs-of-a-healthy-project)
- [Ideal Process](#ideal-process)
- [Community Health Files](#community-health-files)
- [Documentation](#documentation)
- [How Contributors Contribute](#how-contributors-contribute)
- [Shared Repository Model](#shared-repository-model)
- [Fork and Pull Model](#fork-and-pull-model)
- [Creating a Pull Request](#creating-a-pull-request)
- [Reviewing a Pull Request](#reviewing-a-pull-request)
- [Reviewing a Pull Request](#reviewing-a-pull-request)
- [Pull Request: Command Line](#pull-request-command-line)
- [Pull Request: Options If You Do Not Run the Code Locally](#pull-request-options-if-you-do-not-run-the-code-locally)
- [Pull Request: Options If You Run the Code Locally](#pull-request-options-if-you-run-the-code-locally)
- [Pull Request: Commands](#pull-request-commands)
- [Workflow: GitHub Flow](#workflow-github-flow)
- [Workflow: A Variation](#workflow-a-variation)
- [Some Recommendations](#some-recommendations)
- [Licenses](#licenses)
- [Security](#security)
- [Open Source Metrics for Evaluating the Health of Your Project](#open-source-metrics-for-evaluating-the-health-of-your-project)
- [More Useful GitHub Features](#more-useful-github-features)
- [Case Study: DjangoCon US Website](#case-study-djangocon-us-website)
- [Key Points](#key-points)
- [DjangoCon US: The Conference with a Heart](#djangocon-us-the-conference-with-a-heart)
- [The Sites I’ve Overseen](#the-sites-ive-overseen)
- [“Low Hanging Fruit” PRs](#low-hanging-fruit-prs)
- [I Learned How To...](#i-learned-how-to)
- [Increase in the Number of Contributors](#increase-in-the-number-of-contributors)
- [Also Became a Mentor](#also-became-a-mentor)
- [A Few Lessons Learned from DjangoCon US Website](#a-few-lessons-learned-from-djangocon-us-website)
- [Psychological Security](#psychological-security)
- [The Mistakes Disappear into the Git History](#the-mistakes-disappear-into-the-git-history)
- [The Beginner Perspective is Valuable](#the-beginner-perspective-is-valuable)
- [Achieving 10x Results](#achieving-10x-results)
- [My First Tech Talk](#my-first-tech-talk)
- [Case Study: Pinax](#case-study-pinax)
- [Key Points](#key-points)
- [I Was Hired by Eldarion to Maintain Pinax](#i-was-hired-by-eldarion-to-maintain-pinax)
- [Pinax Was Born: 2008](#pinax-was-born-2008)
- [How It Began](#how-it-began)
- [How It Began](#how-it-began)
- [How It Was Going, 80 Projects and Apps](#how-it-was-going-80-projects-and-apps)
- [How It Was Going, Sustainability Lacking](#how-it-was-going-sustainability-lacking)
- [How It Was Going, GitHub Organization, Global Docs, and Slack](#how-it-was-going-github-organization-global-docs-and-slack)
- [Traditional Django Project](#traditional-django-project)
- [Traditional Django Apps](#traditional-django-apps)
- [Pinax CLI](#pinax-cli)
- [Pinax CLI](#pinax-cli)
- [Pinax CLI](#pinax-cli)
- [`projects.json` File](#projectsjson-file)
- [Pinax Starter Projects](#pinax-starter-projects)
- [Pinax Apps in Starter Projects](#pinax-apps-in-starter-projects)
- [Pinax Apps Stand Alone](#pinax-apps-stand-alone)
- [A Typical Release](#a-typical-release)
- [Maintaining Pinax Apps](#maintaining-pinax-apps)
- [Pinax App Codebases](#pinax-app-codebases)
- [Professional Level Configs](#professional-level-configs)
- [Update the Test Matrix](#update-the-test-matrix)
- [pyenv and tox](#pyenv-and-tox)
- [Python/Django Release Notes](#pythondjango-release-notes)
- [Update SemVer Version and Changelog](#update-semver-version-and-changelog)
- [Tag and Publish](#tag-and-publish)
- [20.07 Release](#2007-release)
- [Some Lessons Learned from Pinax](#some-lessons-learned-from-pinax)
- [Simplified, Self-Service, and Self-Sustaining](#simplified-self-service-and-self-sustaining)
- [Major Improvements I’ve Led](#major-improvements-ive-led)
- [The Importance of Publicity](#the-importance-of-publicity)
- [Burnout](#burnout)
- [Reduce Scope](#reduce-scope)
- [Additional Automation](#additional-automation)
- [Python Specific Tools](#python-specific-tools)
- [Centralize Access and Knowledge](#centralize-access-and-knowledge)
- [Managing Volunteer Maintainers](#managing-volunteer-maintainers)
- [Final Thoughts](#final-thoughts)
- [When You Get Stuck](#when-you-get-stuck)
- [OS Social Contract](#os-social-contract)
- [Perks of Maintaining](#perks-of-maintaining)
- [Eating Dinner With Guido](#eating-dinner-with-guido)
- [Is It Worth It? Yes :)](#is-it-worth-it-yes)
- [Is It Worth It? Yes :)](#is-it-worth-it-yes)
- [Special Thank You](#special-thank-you)
- [Contact Me](#contact-me)

:top: <sub>[**back to top**](#table-of-contents)</sub>

<hr>

## Slides and Script

The script is a general outline and varies somewhat from what was said during the talk.

<table>

<tr><td width="30%">

![Slide 1](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_0.jpg)
 
</td><td>

### Maintaining Demystified
 
* Hello everyone
* My name is Katherine Michel. I also go by Kati
* My talk is called “Maintaining Demystified”

</td></tr>


<table>

<tr><td width="30%">

![Slide 2](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_1.jpg)

</td><td>

### My Affiliations
 
* A few of my affiliations
* I have been a part-time Pinax Maintainer and Release Manager for a few years
* I've been a Python/Django/React consultant for the Wharton School
* I have taught some introductory Python programming through Stanford
* I am a member of the DEFNA Board (Django Events Foundation North America) 
* I am the DjangoCon US Website Chair
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 3](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_2.jpg)

</td><td>

### Talk Goals
 
* I’m going to talk about
* The fundamentals of maintaining
* A case study about maintaining the DjangoCon US Website
* A case study about maintaining Pinax
* And some lessons learned
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 4](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_3.jpg)

</td><td>

### Assumptions
 
* I have an assumption that
* You already understand
* The fundamentals of using GitHub
* The fundamentals of contributing
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 5](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_4.jpg)

</td><td>

### Get a Jumpstart on Collaboration and Code Review in GitHub
 
* If you need more information about these subjects
* I have a talk called “Get a Jumpstart on Collaboration and Code Review in GitHub”
* There are several versions in my GitHub account
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 6](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_5.jpg)

</td><td>
 
### Maintaining is Not Just About Code
 
* Firstly, it is important to realize that maintaining is not only about code
* It is also about:
* People
* Community
* Process
* Communication
* Kindness
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 7](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_6.jpg)

</td><td>

### Put Yourself in the Shoes of the Contributor; Make Contributing as Frictionless as Possible
 
* Put Yourself in the Shoes of the Contributor
* Make Contributing as Frictionless as Possible
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 8](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_7.jpg)

</td><td>

### GitHub Open Source Guide: “A Checklist Before You Contribute”
 
* One way to know if you want to contribute to a project
* Is to use the GitHub Open Source Guide
* There is a “Checklist Before You Contribute”
* Maintainers can use it to improve their projects
https://opensource.guide/how-to-contribute/#a-checklist-before-you-contribute
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 9](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_8.jpg)

</td><td>

### Some Signs of a Healthy Project
 
* There is a welcoming atmosphere
* There is recent activity
* The maintainer respond quickly
* The maintainers reduce the issues and pull requests
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 10](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_9.jpg)

</td><td>

### Ideal Process
 
* Ideal process
* Future contributor
* Finds project
* Agrees to Code of Conduct
* Reads CONTRIBUTING.md
* Uses docs, issue/pull request templates
* Creates issue/pull request
* Maintainer responds quickly
 
</td></tr>


<table>

<tr><td width="30%">

![Slide 11](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_10.jpg)

</td><td>

### Community Health Files
 
* The first step is for the maintainer to create the community health files
* README.md- gives general project information
* LICENSE- tells you the legal terms under which you can contribute and use the code
* CODE_OF_CONDUCT.md- a set of rules outlining the expectations and responsibilities of contributors 
* CONTRIBUTING.md- gives info about contributing
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 12](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_11.jpg)

</td><td>

### Documentation
 
* Documentation is very important for the future success of a project
* GitHub did an open source survey in 2017 and they found that documentation is...
* Highly valued
* Often overlooked
* And a means for establishing inclusive and accessible communities

-From GitHub’s 2017 Open Source Survey

http://opensourcesurvey.org/2017/#insights
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 13](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_12.jpg)

</td><td>

### How Contributors Contribute
 
* I have made a couple of diagrams that I hope will give an idea of the process of working locally by a contributor versus a maintainer.
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 14](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_13.jpg)

</td><td>

### Shared Repository Model
 
* The "Shared Repository" Model is normally used in a GitHub organization
* A maintainer does not need to use a fork, because he or she has write permission to the repo
* The maintainer can clone the shared repo (using the shared repo URL)
* The maintainer can make his or her changes, probably in a branch, and push the changes to the shared repo
* The maintainer can create the pull request (directly in the GitHub Organization)
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 15](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_14.jpg)

</td><td>

### Fork and Pull Model
 
* The "Fork and Pull" Model is normally used in a contributor's account. Because the contributor does not have "write permission" to the GitHub Organization, he or she needs to fork the repo into their user account, where they have "write permission." 
* The contributor forks the repo
* The contributor clones the fork (using the fork URL)
* The contributor can make his or her change, then commit the changes to the fork (probably in a branch)
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 16](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_15.jpg)

</td><td>

### Creating a Pull Request
 
* When ready, the contributor submits the pull request (to the GitHub Organization)
* The compare branch should be the contributor's branch
* The base branch should be the branch into which the changes should be merged
* The contributor creates a pull request title and maybe a description
* The contributor clicks on "Create Pull Request"
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 17](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_16.jpg)

</td><td>

### Reviewing a Pull Request
 
* Now let's switch to the maintainer perspective.
* When a contributor creates a pull request, the maintainers of the repo will receive a browser notification or email to inform them that there is a pull request.
* Follow the link to the pull request page in the browser.
* Review the information about the pull request. You can see the title and description and click on the "Files changed" link to see all the changes made.
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 18](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_17.jpg)

</td><td>

### Reviewing a Pull Request
 
Below that will be
* A link that says "command line instructions"
* A merge button that you can click to merge in the browser, when ready
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 19](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_18.jpg)

</td><td>

### Pull Request: Command Line
 
* There are some situations when you need to fetch the pull request branch in your local development environment in order to run the code or run a test or work on the code in order to merge it.
* When you click on the "command line instructions" link, it will open a set of instructions for how to review and (possibly) merge the pull request in your local development environment.
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 20](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_19.jpg)

</td><td>

### Pull Request: Options If You Do Not Run the Code Locally
 
* If no change is needed or the change can be made in the browser
* Make the change in the browser
* Click merge
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 21](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_20.jpg)

</td><td>

### Pull Request: Options If You Run the Code Locally
 
* If no change is needed, go back to the browser and click merge
* If a change is needed, ask the contributor to make the change, or push the update yourself, then click merge
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 22](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_21.jpg)

</td><td>

### Pull Request: Commands
 
* If you need to run the code locally, and you follow the entire instruction set, you will manually merge the pull request branch locally into the branch it is intended to be merged into and push it to that branch on GitHub
* I do not do that. 
* I only follow the part of the instructions to fetch the branch.
* I ignore the instructions in red
* If I verify that the change can be merged, I go back to the GitHub pull request page in the browser and click merge
* For one thing, the main branch is often protected
* Also, in the browser, you can simply push a button to revert the pull request
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 23](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_22.jpg)

</td><td>

### Workflow: GitHub Flow
 
* The workflow we have been using is basically GitHub Flow. It consists of merging pull requests into a 'main' branch.
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 24](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_23.jpg)

</td><td>

### Workflow: A Variation
 
* Some projects use both `main` and `develop` branches. 
* In this situation, developers merge their work into the `dev` branch. Eventually, the `dev` branch is merged into the `main` branch. If the `main` branch is deployed, the changes are live. 
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 25](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_24.jpg)

</td><td>

### Some Recommendations

</td></tr>


<table>

<tr><td width="30%">

![Slide 26](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_25.jpg)

</td><td>

### Licenses
 
* Non copyleft licenses
* Copyleft licenses
* Ethical licenses
* GitHub “Choose a License”
* A very common license is the MIT license
* The MIT License is non-copyleft and gives the user a lot of freedom in the use of the code, including making the code private
* A Copyleft License usually requires that the code remains open source
* For this reason, copyleft licenses can create a business risk
* Ethical licenses (or ethical licenses) are a very interesting subject in my opinion
* But sometimes the terms of ethical licenses are difficult to enforce
* GitHub has an excellent resource called "Choose a License"
* In the appendix is a table with a comparison of licenses: https://choosealicense.com/appendix/  
 
</td></tr>


<table>

<tr><td width="30%">

![Slide 27](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_26.jpg)

</td><td>

### Security

* One difficult aspect of software security is that
* The software supply chain is everything that makes up your code…
* Including the GitHub organization, the project, and the people who have access to it
* Including the dependencies and external hosting
* Therefore, a project needs a security plan with several parts.
* Some examples
* For the individual level... 2-factor authentication, limited access 
* For the organization level... scanning of secrets and dependencies for vulnerabilities
* For the project level... new releases incorporating the latest security patches and a project security plan with information on how to report vulnerabilities 
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 28](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_27.jpg)

</td><td>

### Open Source Metrics for Evaluating the Health of Your Project
 
* If you want to start measuring your project's health
* There are special metrics
* CHAOSS, for example, is a collection of metrics that you can use to create a health plan for your project
https://chaoss.community/metrics/
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 29](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_28.jpg)

</td><td>

### More Useful GitHub Features
 
* A list for future reference of more useful GitHub features
* Issue and pull request templates and Global Community Health File Repo
* Project Management: Project Boards, milestones, issues, labels
* Communication methods: wiki, GitHub Pages/Jekyll
* Discoverability: labels/triaging, topics, blog posts
   
</td></tr>


<table>

<tr><td width="30%">

![Slide 30](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_29.jpg)

</td><td>

### Case Study: DjangoCon US Website
 
* A case study: DjangoCon US Website
 
</td></tr>


<table>

<tr><td width="30%">

![Slide 31](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_30.jpg)

</td><td>

### Key Points
 
* DjangoCon US Website has been
* An opportunity to
* Learn the fundamentals of maintaining
* Grow a community of contributors
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 32](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_31.jpg)

</td><td>

### DjangoCon US: The Conference with a Heart
 
* I spent a lot of time looking through GitHub
* I realized that many conferences are looking for volunteers who can maintain their web sites
* So, I got involved with DjangoCon US
* This is a picture of me with some of the other organizers
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 33](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_32.jpg)

</td><td>

### The Sites I’ve Overseen
 
* I wanted to take my GitHub knowledge to the next level by learning how to be a maintainer
* So, I asked the DjangoCon US Chair if I could be a maintainer of the website
* She said “sure” and invited me to be the Website Chair, which I accepted
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 34](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_33.jpg)

</td><td>

### “Low Hanging Fruit” PRs
 
* One of the strategies that helped me learn the process of maintaining
* The other maintainer left the easier pull requests for me
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 35](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_34.jpg)

</td><td>

### I Learned How To...
 
* I learned how to...
* Fetch a pull request locally
* Run the code
* Push an update from a fork to a pull request
* Merge a pull request locally
* Push a pull request to a `main` branch
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 36](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_35.jpg)

</td><td>

### Increase in the Number of Contributors
 
* Because a Jekyll website is very easy to use
* I was able to learn the basics of being a maintainer
* And we were also able to drastically increase the number of contributors
* From 23 in 2016
* To 65 in 2020
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 37](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_36.jpg)

</td><td>

### Also Became a Mentor
 
* I created the new contributing docs
* I helped some beginners make their first contributions
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 38](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_37.jpg)

</td><td>

### A Few Lessons Learned from DjangoCon US Website
 
* A few lessons learned from DjangoCon US Website
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 39](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_38.jpg)

</td><td>

### Psychological Security
 
* It is ideal to learn in an environment of psychological safety
* Fortunately for me, I could not have stumbled upon a nicer community
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 40](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_39.jpg)

</td><td>

### The Mistakes Disappear into the Git History
 
* It’s ok to have a beginner mindset; make mistakes, keep improving 
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 41](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_40.jpg)

</td><td>

### The Beginner Perspective is Valuable
 
* A beginner perspective is valuable
* Project veterans may not be able to see the project through the eyes of a beginner
* A beginner can improve the project for the next person
* Example: create installation docs
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 42](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_41.jpg)

</td><td>

### Achieving 10x Results
 
* Achieving 10x results
* People often talk about the concept of 10x results
* It is important to remember some of the skills that create 10x results, do not involve writing code
* A few examples
* Maintaining the docs
* Publicizing the project
* Mentoring collaborators
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 43](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_42.jpg)

</td><td>

### My First Tech Talk
 
* When you learn a new skill, you have the opportunity to teach other people and impact the world
* After I learned how to maintain the DjangoCon US website, I created a talk about how to do it
* It is one of my goals to help other women be maintainers
* I gave the talk called “Get a Jumpstart on Collaboration and Code Review in GitHub” for the first time at DjangoCon US 2017
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 44](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_43.jpg)

</td><td>

### Case Study: Pinax
 
* A case study: Pinax
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 45](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_44.jpg)

</td><td>

### Key Points
 
* Pinax has been
* An opportunity to:
* Maintain a complex Django library
* Become a Python package release manager
* Learn how to deal with scope creep
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 46](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_45.jpg)

</td><td>

### I Was Hired by Eldarion to Maintain Pinax
 
* In the fall of 2017, based on my experience as a maintainer at DjangoCon US 2017
* I was hired to work on Pinax
* Pinax is an open source library of Starter Projects, reusable Django apps and themes for building websites
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 47](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_46.jpg)

</td><td>

### Pinax Was Born: 2008
 
* A little history about Pinax
* When I was hired, it had been about 10 years since the idea of Pinax was born
* Django had been open sourced in 2005
* In March 2008, at PyCon US in Chicago, some Django enthusiasts started working on Pinax
* They were creating Pinax to solve their own problem

</td></tr>


<table>

<tr><td width="30%">

![Slide 48](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_47.jpg)

</td><td>

### How It Began
 
* They found themselves reusing some of the same code patterns while creating websites with Django
* So they started to abstract these patterns into reusable Django Starter Projects, applications and themes
* They wanted to create a reusable web development library that would make choices and compromises
* This library would allow them to focus on the features at the top of the stack
* That way, they could go from website idea to realization quickly, rather than reinventing the wheel
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 49](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_48.jpg)

</td><td>

### How It Began
 
* So what was the state of Pinax when I was hired?
* It’s quite common, from the very beginning until now, for people to discover Pinax and say “it’s everything they ever dreamed of”
* On this slide is one of the very early tweets about Pinax… someone says “Pinax is every idea I’ve ever had.”

</td></tr>


<table>

<tr><td width="30%">

![Slide 50](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_49.jpg)

</td><td>

### How It Was Going, 80 Projects and Apps
 
* By 2017, Pinax had grown to be a large group of professionally-quality, interdependent Django projects and apps
* Including starter projects with Pinax apps pre-installed and a Pinax CLI to install them
* And sophisticated testing, packaging, and continuous integration configurations
* The Pinax GitHub organization alone has around 80 repos in it
* This slide includes many of the more popular ones
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 51](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_50.jpg)

</td><td>

### How It Was Going, Sustainability Lacking
 
* But… sustainability was lacking
* Many of the original authors had moved on
* Without a strategy to make Pinax easier to maintain, the maintainers began to suffer burnout. 
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 52](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_51.jpg)

</td><td>
    
### How It Was Going, GitHub Organization, Global Docs, and Slack
 
* In addition to the GitHub organization
* Pinax now had a global docs site and a Pinax Slack channel for community and support
* There were also app-specific docs in individual repos
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 53](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_52.jpg)

</td><td>
 
### Traditional Django Project
 
* Now, I'm going to talk about GitHub and the local development environment and how Pinax works
* In your local dev environment, if you are starting a traditional Django project...
* You will need to have Django installed and you would normally be using a virtual environment
* Run the ```django-admin startproject``` command in the terminal to start a project
* The project contains the global settings and other configurations for your site
* The project template files populated in the directory come from within the Django package
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 54](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_53.jpg)

</td><td>

### Traditional Django Apps
 
* You would then run an additional command to add one or more apps to your project
* Each app contains a special functionality (for example a `blog` app for a blog part of your website)
* The app template files populated also come from within the Django package

</td></tr>


<table>

<tr><td width="30%">

![Slide 55](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_54.jpg)

</td><td>

### Pinax CLI
 
* With Pinax, you can install Pinax CLI (command line interface)
* You can use commands to get info about Pinax (such as a list of starter projects or apps)
* Pinax starter projects are basically custom Django projects
* They already have some functionality built in and by using them, you do not have to start from scratch using a traditional Django project
* The same with Pinax Apps
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 56](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_55.jpg)

</td><td>

### Pinax CLI
 
* You can also use Pinax CLI to install a Pinax Starter Project instead of the traditional Django project
* There is a special Pinax CLI command to do this `pinax start <pinax-starter-project> <your-project>
* When the Pinax CLI runs this command
* The Pinax CLI uses the same ``startproject`` command used to install a traditional Django project
* But Django calls it from the Pinax CLI code base
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 57](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_56.jpg)

</td><td>

### Pinax CLI
 
* The starter project URL is passed in as a parameter
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 58](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_57.jpg)

</td><td>

### `projects.json` File
 
* The URL leads to a `projects.json` file that provides the tar file address in the Pinax Starter Projects repo
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 59](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_58.jpg)

</td><td>

### Pinax Starter Projects
 
* Pinax Starter Projects are in one repo
* Each starter project is in an individual branch
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 60](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_59.jpg)

</td><td>

### Pinax Apps in Starter Projects
 
* Each starter project contains the relevant Pinax apps, to be installed from PyPI (The Python Package Index)
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 61](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_60.jpg)

</td><td>

### Pinax Apps Stand Alone
 
* Alternatively, Pinax apps can be used independently of any Pinax starter project
* You can find them by searching “pinax” on PyPI

</td></tr>


<table>

<tr><td width="30%">

![Slide 62](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_61.jpg)

</td><td>

### A Typical Release
 
* A typical release
* Update the test matrix
* Add new features
* Implement new best practices
* Fix deprecations
* Improve documentation

</td></tr>


<table>

<tr><td width="30%">

![Slide 63](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_62.jpg)

</td><td>

### Maintaining Pinax Apps
 
* A few important details about maintaining Pinax Apps
* We use GitHub Flow workflow
* For semantic versioning
* We use CalVer at release-level (year.month)
* We use SemVer at application-level (major.minor.patch)

</td></tr>


<table>

<tr><td width="30%">

![Slide 64](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_63.jpg)

</td><td>

### Pinax App Codebases
 
* Each Pinax app codebase lives in a GitHub repo
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 65](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_64.jpg)

</td><td>

### Professional Level Configs
 
* Each app repo has professional level configurations used to keep the code up-to-date
* CircleCI is for continuous integration
* `setup.py` contains packaging configurations
* `tox` is for testing the Python/Django versions matrix
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 66](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_65.jpg)

</td><td>

### Update the Test Matrix
 
* When we do a release, we update the test matrix to support the latest versions of Python and Django
* In my release plan, I document some test matrix boilerplate to copy and paste into the app files
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 67](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_66.jpg)

</td><td>

### pyenv and tox
 
* The process is that… 
* I clone the Pinax app repo locally, and create a new branch
* I update the test matrix in the branch
* There is a tool called pyenv that you can use to install multiple Python global versions locally
* When tox is run, it can use these global versions to check the compatibility of the Pinax App code against the new Python/Django versions
* When there is an incompatibility, tox will show you the error in red
* When all of the tests pass… it will show green at the end

</td></tr>


<table>

<tr><td width="30%">

![Slide 68](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_67.jpg)

</td><td>

### Python/Django Release Notes
 
* While you are troubleshooting to fix these incompatibilities
* The Python/Django release notes explain all the changes made to the Python/Django codebase in the release
* You can use the release notes to understand what updates to make for compliance
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 69](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_68.jpg)

</td><td>

### Update SemVer Version and Changelog
 
* When all of the test matrix and other updates have been made
* You will want to update the SemVer Version in the `setup.py`
* As well as the versions throughout the `setup.py` metadata and README
* Update the Change Log in the README
* These are some of the various pieces of metadata
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 70](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_69.jpg)

</td><td>

### Tag and Publish
 
* Then go to the “tags” area of the repo
* Draft a new release
* Include a link to the Changelog
* Run a process locally to package the app
* I have documented this process in the .github repo in the RELEASE.md file
* And publish the package to PyPI (Python Package Index)

</td></tr>


<table>

<tr><td width="30%">

![Slide 71](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_70.jpg)

</td><td>

### 20.07 Release
 
* In July 2020, I oversaw the completion of a major Pinax release.
* It included approximately 28 applications and notably dropped support for Python 2.7
* It was a major milestone for me personally and professionally
* I initiated the release, managed the process from start to finish, created the release plan, supervised the work of others, updated 10 applications myself, merged all pull requests, and tagged and published the packages
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 72](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_71.jpg)

</td><td>

### Some Lessons Learned from Pinax
 
* Some lessons learned from Pinax
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 73](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_72.jpg)

</td><td>

### Simplified, Self-Service, and Self-Sustaining
 
* I have tried to solve some of the critical problems of Pinax
* The goal in general has been to implement changes to make it simpler and self-service
* As a result, newcomers, contributors, and maintainers could help themselves
* And therefore, create a culture that could sustain itself

</td></tr>


<table>

<tr><td width="30%">

![Slide 74](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_73.jpg)

</td><td>

### Major Improvements I’ve Led
 
* Major improvements I’ve led
* Documentation of tribal knowledge
* Consolidation of docs, in one easy-to-find place
* Standardization of configurations between projects
* Creation of detailed release and maintainer docs
* Creation of Community Health Files, including Issue and Pull Request Templates
* Significant reduction in the number of issues and pull requests in order to get up-to-date with new issues and pull requests

</td></tr>


<table>

<tr><td width="30%">

![Slide 75](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_74.jpg)

</td><td>

### The Importance of Publicity
 
* One of the most important lessons I've learned from Pinax
* Sometimes it is counter-intuitive
* Sometimes it is important to stop and communicate your progress and plans to the community
* And ask for help
* For example, because of my blog posts, I received help that was crucial in completing the latest Pinax release
    
</td></tr>


<table>

<tr><td width="30%">

![Slide 76](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_75.jpg)

</td><td>

### Burnout
 
* There is a real danger of burn out in open source
* It is a sad subject
* Code authors and maintainers are generous 
* Sometimes they work too hard
* And unfortunately, sometimes they have to deal with the negative attitudes of code users
* I'm not sure Pinax is going to be healthy and thrive again
* But, I’ve learned a lot from Pinax
* I want to talk about some ways to make a self-sustaining community
* For the maintainers, contributors, and users
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 77](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_76.jpg)

</td><td>

### Reduce Scope
 
* Ways to reduce the scope
* Mark repos as deprecated
* Archive repos
* Disable issues
* Communicate that the code is maintained sporadically
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 78](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_77.jpg)

</td><td>

### Additional Automation
 
* You can implement additional automation to reduce the workload
* Here are a few places where you can find automation tools
* GitHub Actions
* GitHub Apps
* Probot: https://probot.github.io/
* Probot is a place to find novel ideas about what could be automated
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 79](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_78.jpg)

</td><td>

### Python Specific Tools
 
* Some Python-specific automation tools
* In addition to pyenv and tox there are
* Coverage.py (coverage dot py)
* isort
* Black
* Restructured Text
* And many others

</td></tr>


<table>

<tr><td width="30%">

![Slide 80](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_79.jpg)

</td><td>

### Centralize Access and Knowledge
 
* It is a problem when only one person has access or knowledge of a project (for example, repo access or PyPI access)
* If the person leaves the project and does not hand over the access and knowledge, it is difficult to continue
* It is better in my opinion to have a policy of centralizing access and giving access to others
* Another flavor of this problem is when a maintainer creates a unique solution to a problem and is the only person with access and knowledge
* If the person loses interest, it's difficult for others to continue
* In my opinion it is better to avoid very unique solutions

</td></tr>


<table>

<tr><td width="30%">

![Slide 81](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_80.jpg)

</td><td>

### Managing Volunteer Maintainers
 
* It’s important to remember that it is the responsibility of the maintainer to secure the code
* When there is a risk of burnout, it is possible to give additional, limited access to contributors
* You can give selective permissions (for example, only give access to an individual repo)
* Protect branches (for example, no one can't delete an important branch)
* Require pull request reviews (for example, more than one person contributes to the review before merging) 
* Use status checks
* In the worst case, you can revert a pull request, if needed
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 82](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_81.jpg)

</td><td>

### Final Thoughts
 
* A few final thoughts
 
</td></tr>


<table>

<tr><td width="30%">

![Slide 83](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_82.jpg)

</td><td>

### When You Get Stuck
 
It’s inevitable that you will have moments of frustration and get stuck… here are a few places where you can find help
* Google
* Stack Overflow
* GitHub docs
* Git docs
* Atlassian and GitLab docs
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 84](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_83.jpg)

</td><td>

### OS Social Contract
 
* Brett Cannon (a Python Core Dev) has talked about the open source “social contract”
* Open source maintainers owe the community quite literally nothing
* The Pinax authors didn’t have to open source their code and maintain it
* They didn’t have to answer the countless questions they answered
* It is important to remember the generosity of open source code maintainers

</td></tr>


<table>

<tr><td width="30%">

![Slide 85](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_84.jpg)

</td><td>

### Perks of Maintaining
 
* There are many perks of maintaining
* It is an opportunity to… 
* Learn technical skills
* Find new professional opportunities
* Attend conferences
* Meet smart, interesting people building who build incredible apps
* Travel to incredible places
  
</td></tr>


<table>

<tr><td width="30%">

![Slide 86](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_85.jpg)

</td><td>

### Eating Dinner With Guido
 
* At PyCascades 2020, I had the opportunity to eat dinner with Guido, the creator of Python programming language
* He told us some stories about the early days of Python
* It was a magical evening
* I directly attribute these kinds of experiences to open source
 
</td></tr>


<table>

<tr><td width="30%">

![Slide 87](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_86.jpg)

</td><td>

### Is It Worth It? Yes :)
 
* During GitHub Maintainer Week
* I saw this tweet from Mfon… his contributions were critical in helping me complete the 20.07 release
 
</td></tr>


<table>

<tr><td width="30%">

![Slide 88](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_87.jpg)

</td><td>

### Is It Worth It? Yes :)
 
* Seeing the difference my work has made to him and finding out that he considers me to be a very good friend is very special to me
* What he said immediately made it worth it
* I suddenly realized...
* At the heart of open source… are the relationships I’ve formed with people
* Which I’ll have for the rest of my life
  
</td></tr>

  
<table>

<tr><td width="30%">

![Slide 89](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_88.jpg)

</td><td>
 
### Special Thank You :)
 
* Thank you to Ricardo Diaz Rincon for reviewing the Spanish version of this talk: 
* If there is an error, it as made by me
* The Spanish version is scheduled to be broadcast at DjangoCon US 2021 on October 23
 
</td></tr>
  
  
<table>

<tr><td width="30%">

![Slide 90](https://speakerd.s3.amazonaws.com/presentations/001d82e284ed4157be64cd12b526dde3/slide_89.jpg)

</td><td>

### Contact Me
 
* Feel free to contact me for more information
* Thank you, everyone
 
</td></tr>
      
</table>

:top: <sub>[**back to top**](#table-of-contents)</sub>

<hr>

## Attribution

The style of this transcript is heavily inspired by:

* Ana Balica's ([Twitter](https://twitter.com/anabalica), [GitHub](https://github.com/ana-balica)) transcript of her [Humanizing among coders](https://ana-balica.github.io/2017/05/28/humanizing-among-coders/) keynote for [PyCon CZ 2016](https://cz.pycon.org/2016). 
* Honza Javorek's ([Twitter](https://twitter.com/honzajavorek), [GitHub](https://github.com/honzajavorek)) transcript of Anna Ossowski's ([Twitter](https://twitter.com/OssAnna16), [GitHub](https://github.com/OssAnna16)) keynote [Be(Come) A Mentor! Help Others Succeed!](https://github.com/honzajavorek/become-mentor) for [PyCon CZ 2017](https://cz.pycon.org/2017/). 

Thank you!

:top: <sub>[**back to top**](#table-of-contents)</sub>

<hr>

## Contact Kati

* Email: kthrnmichel@gmail.com
* GitHub: https://github.com/KatherineMichel
* Twitter: https://twitter.com/KatiMichel

:top: <sub>[**back to top**](#table-of-contents)</sub>

<hr>

## Copyright

© 2021 to Present Katherine Michel. All Rights Reserved.
