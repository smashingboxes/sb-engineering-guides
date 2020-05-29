# QA

Our process for Quality Assurance at Smashing Boxes begins and ends with our clients. During the project kickoff phase of a project we begin
with discussing what is important to you. What devices and platforms will your target users be using? What operating systems are you most
concerned about? Do you have any specific browser needs? Based on your needs we will develop a custom test plan to ensure we meet the
highest levels first in the areas that are important to you, and then in other areas we feel should be covered as well.

Our process includes manual and automated testing, if applicable, to be factored into each sprint. As we are developing features for you, we
are manually verifying them and writing automated code using Java and Selenium to continue testing these areas of the application as
development progresses. This cycle is repeated until we have met your application objectives. Before delivery, we provide a comprehensive
regression test, running the complete automated test suite (if applicable) as well as confirming everything manually in order to catch
things that automation cannot, such as UI or UX issues. We’ll also provide a detailed test results document illustrating the outcome of your
custom test plan. We feel this process is key to crafting products of the highest quality.

## Help Us Help You

As a company, we are all responsible and have a role in quality. If a PM,
Developer or Designer finds a bug at any stage, he/she should immediately log
using the Defect Description field in Jira. If you see it, you can log it. If
you have any questions on this, please reach out to the dedicated QA for that
project as we are always here to help!

The QA team is always open to additional testing help from developers and;
in fact, it is encouraged both during and at the end of a sprint before
delivery. While code is in PR, this is the opportunity for developers to
do a quick smoke test prior to a deploy to avoid any unnecessary rejections.
With a team testing approach, we can help drive quality and ensure products
leaving our doors meet and even exceed client expectations and requirements.

This all said, we use our pre-production environment for clients to do a final
regression and/or smoke test prior to a deploy. Deploying to this environment
should happen no less than ~ 8 hours prior to a deploy. This final sign-off
will help ensure that we are building to the client's needs and also can
eliminate any unnecessary confusion over our work.

## QA Needs Checklist

This checklist should be adhered to and followed throughout the entire
project lifecycle.

## Project setup - Sprint 0

- Resource Gathering
  - Links for accessing environments
    - QA - Accessible only to the development team.  Majority of the testing will be done in this environment.
    - QA Automation (if applicable) - Accessible only to the development team.  All automation testing should be executed in this environment.
    - Staging and/or Pre-Prod - Accessible to both the development team and the client.  Preferably, client demos should be done in this environment.  But if the state of the environment is not stable, the QA environment can be used for demos as well.  Some testing can be done here depending on the task.
    - Prod (depending on project needs) - Accessible to the development team, client, and end-users.  Minimal testing is done in this environment as it may affect real users and real data.
  - Test user credentials
    - This includes usernames, passwords, and other important information used for testing
    - This information should be pinned in the project Slack channel
  - All documents in project folder in Google Drive
  - Access to GitHub repositories (if applicable)
    - SeleniumToolkit automation framework
    - Project specific automation code base

- [Definition of Done](https://docs.google.com/a/smashingboxes.com/document/d/1vhgSqIjEDT338K8zTmOaTXewGLDZA0nxfFZXNnTrT8U/edit?usp=sharing)
  - Ensure that the Definition of Done is created, agreed to by the team, and posted in a shared location (pinned in project Slack channel
  and in Jira or other PM tool)

- Mobile setup
  - Coordinate with Devs to add SB testing email to Crashlytics and TestFlight

- Automation setup
  - Set up project repository on GitHub
  - Configure local QA Dev environment (Steps to do this are coming soon!)

## Create and confirm test strategy with the PM and team

- We need to be involved from the very beginning

- Manual vs. Automation
  - [Setup for automation](https://docs.google.com/document/d/1HwchOXrYytuOyosfDr5Qc-E-mF7CExkbsItFoOPnZKI/edit) - WIP

- We ask the right questions in client kickoff (browsers, OS, etc.)
  - Confirm that all of the requirements are gathered and understood

- QA needs time to create the test plan if doing automation, otherwise, each sprint will produce a release notes document including all of the new features in the release, any known issues, and items for next release

- Client needs to signoff on test plan as delivered by PM (if automation)

## Defect Report Template for Jira

When bugs are reported in Jira, the user will see the following for the Defect
Description. Please enter all fields so that there is more visibility into
the issue at-hand.

```text
Title:  [Clear and concise, Brief description of the issue]
Steps to reproduce:  [Super detailed, step-by-step instructions]
Actual Result(s):  [The result that occurred when you followed the steps]
Expected Result(s): [What the behavior/result should have been]
Platform:  [Browser and/or Device you're testing on]
Build: [Number of build if on mobile]
Attachments: [Any additional information like screenshots/logs]
```

## TestRail Test Case Management

We use either spreadsheet format or TestRail to document test cases for a
project. TestRail connects with Jira out of the box. If a Dev or PM would
like to login, use the dev_pm@smashingboxes.com account.
The password is in 1password.

## Useful Links

### QA Testing Overview

[December 2017 Standard QA Services](https://docs.google.com/document/d/1rtf_Q_V4A2uJTg5lHEpq5TyQb6idlbNQoAMc3BTFoIA/edit)

[Statement of Work Template - QA Section](https://docs.google.com/document/d/1kLU8Itjy0fXHwazDFJr4drhr_kh3oeyebqgOybWoEG8/edit#heading=h.2v84mkszhlrs)

[QA Testing Overview](https://docs.google.com/a/smashingboxes.com/document/d/1u3r-sAkNV3C4voa2KUfAh74mmPIKA9EeGs33g3MZnM0/edit?usp=eharing)

[QA Process Presentation](https://docs.google.com/a/smashingboxes.com/presentation/d/1AM6Ujx6GL9lwrW9RTMfhVwCFPsSgzl0cvMrYEFqgsRs/edit?usp=sharing)

Use SauceLabs for cross-browser testing
[Sauce Labs](https://saucelabs.com/beta/login)

Link to Smashing Boxes Test Rails instance
[Test Rails Test Case Management](hhttps://sbqa.testrail.net)

This doc is submitted to the client at the start of a new project
[Test Plan Sample](https://docs.google.com/a/smashingboxes.com/document/d/1eCF1j5n-oBa5THK-klkcKrIB397yRCPmrdJzM97qy7I/edit?usp=sharing)

### Learning to QA

Steps to QA a product
[Quick and Easy way to QA](https://smashingboxes.com/blog/quick-easy-way-qa/)

[QA Training Part 1](https://docs.google.com/a/smashingboxes.com/presentation/d/1mIxzeo7ft4kg5n67fYQrWxwbm31YOGViUiKEhst0kUg/edit?usp=sharing):
Positive and Acceptance Testing

[QA Training Part 2](https://docs.google.com/a/smashingboxes.com/presentation/d/1BOr0Ar8onht-DwK_XzeogGQ2Ih3-sInOF9PG8xDWtOQ/edit?usp=sharing):
Negative Testing and Bug Logging

[QA Training Part 3](https://docs.google.com/a/smashingboxes.com/presentation/d/1m8hrledpnX_AceFBnhvGu0XhYJPdftU3dkgJLlLKNhg/edit?usp=sharing):
End of Product Testing

[QA Training Part 4](https://docs.google.com/a/smashingboxes.com/presentation/d/16WoxhPyiziP0ju9oWQg_PFl_3AaoXOuuv1U0GExvH50/edit?usp=sharing):
Tools and Documentation

[QA Training Part 5](https://docs.google.com/a/smashingboxes.com/presentation/d/1ImRSW35fBXhZ425udP1XPhtat4wHlJ8i8GeJxeARuxg/edit?usp=sharing):
Mock Run as a QA

### Training Website for QA

- [Bookstore User Login](https://qa-test-bookstore.sboxes.co)
  - user@example.com / password

- [Bookstore Admin Login](https://qa-test-bookstore.sboxes.co/admin/sign_in)
  - admin@example.com / password

- [Jira Practice User Stories](https://smashingboxes.atlassian.net/secure/RapidBoard.jspa?rapidView=116&projectKey=BKST&view=planning&selectedIssue=BKST-1)

### Resources

QA

[Recording iOS test with Appium - Video](https://www.youtube.com/watch?v=Hv9A9WfYF4g)

[Parallel Cross Browser testing using Cucumber, Capybara, and SauceLabs](https://github.com/verdi327/parallel_test_tutorial)

[Robot Framework Tutorials - Automated Browser Testing](http://www.robotframeworktutorial.com/)

[Automated Framework SauceLabs Webinar](http://go.saucelabs.com/G6B0TW10UCdYX0Xt0000kVo)

[Automated Framework SauceLabs Slide Deck](http://go.saucelabs.com/v0dU0VWZ0XtTXkD6B01o000)

[Import/Export Jira User Stories to TestRail Test Cases](https://docs.google.com/a/smashingboxes.com/document/d/1XpS_1xteBsfJIQ82EdOg42yTSvEXK6_wpbiIEd4WSp0/edit?usp=sharing)

Dev

[18F - How To Use GitHub and the Terminal](https://18f.gsa.gov/2015/03/03/how-to-use-github-and-the-terminal-a-guide/)

[Rails Tutorial - Book](https://www.railstutorial.org/book/)

[Learn Ruby the hard way - Beginner](http://learnrubythehardway.org/book/)

[Rails blog in 15 minutes](https://www.reinteractive.net/posts/32-ruby-on-rails-3-2-blog-in-15-minutes-step-by-step)

[Swift Tutorial](http://jamesonquave.com/blog/developing-ios-apps-using-swift-tutorial/)

[Learn Javascript](https://www.javascript.com/)
