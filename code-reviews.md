# Code Review Process

## The Rules

1. All code must be reviewed _without exception_, via a pull request. If you are not
   familiar with how to create a pull request in Github, find someone to pair with for
   your first couple.

2. The creator of the pull request is responsible for making the merge
   button green (merging in master, addressing conflicts, passing tests, passing
   lint tests, getting approvals). If the PR is handed off to another person,
   it should be noted in the comments of the PR.

3. Feature branches should be created from and merged back into master.
   A feature branch should be short lived, and reasonbly small. The smaller it is, the
   easier it is for someone to review it.
   
4. Feedback should be aimed at addressing incorrect functionality, poorly code quality, 
   and missing tests. Let the linter handle the nit-picks on style, etc.

5. Developers of all skill levels should review code and have their code reviewed.
   Even if you don’t feel like you’re qualified to review someone’s code,
   do it anyways; it’s a great way to learn. If either the reviewer or the
   PR creator feels it needs another set of eyes, they can (and should) say so.
   
6. Don't hesitate to ask questions about anything you don't understand. Worst-case, 
   you didn't understand it and you learn something; best case, the author also 
   didn't understand it, so it probably needs to be re-evaluated.

## Code Review Etiquette

[View](https://github.com/thoughtbot/guides/tree/master/code-review)

## Pull Request Workflow

Writing code in a pull-request oriented git workflow is critical to
obtaining good code-reviews. Each specific User Story needs to live inside
its own feature branch. Code changes should be as focused as possible and
not branch across multiple stories or features as to make the changes
simpler to review. The more code changes there are in a Pull Request
the harder it is to review.

## Creating a feature branch

First, checkout master and make sure it is up to date

```bash
git checkout master
git pull origin master
```

Now, when you start a card, create a new feature branch that all of your code
changes will live on.

```bash
git checkout -b branch-name
```

Branch names can be whatever you want, but it’s recommended that you include the
Jira card number in the name, like feat/SB-101 or bug/SB-102. That way, Jira will
pick up the card, for various git integration features. This also helps you remember
that a branch should be as small as possible, and not include code for multiple cards.

An alternative to putting the Jira card number in the branch name would be to put
it in the commit message. Jira will pick that up in the same way.

Once you have completed your changes, push the branch up to github:

```bash
git push origin branch-name
```

When your branch is ready, make a pull request.

### Pull Request Format

All pull requests should include a “Why?” section, with links to the Jira cards
and a “What changed?” section with high-level details about the change. Changes
that include graphical components (frontend and admin changes) should also include
screenshots at any relevant screen sizes. All of this information is important for
providing context to reviewers, and anyone looking back at the PR later for reference.

Most of our projects also include a [pull_request_template.md](https://help.github.com/articles/creating-a-pull-request-template-for-your-repository/)
file for this format.

### Review Process

When your pull request is ready, and all your tests are passing, you can request a
code review by posting your PR url in the *code-reviews* Slack channel. You're also encouraged
to use [PR/MATE](https://github.com/smashingboxes/pr-mate),
a tool we wrote that will include various metadata about the PR. The format for that is:

```md
/pr-mate <pull-request-url>
```

### Merging Pull Requests

Once your code has been reviewed and your reviewer has expressed approval, you have
approval via github’s PR approve feature or an approval emoji (thumbs up, shipit, etc),
and tests and linting are passing, you are ready to merge.
