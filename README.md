# Phase 2 Backend Project Requirements

This is the final project for "Phase 2" of the Flex course for [DigitalCrafts]
Houston. It is focused on backend technologies using [Node.js].

> NOTE: You must complete this project in accordance with the requirements laid out
  below in order to fulfill Texas state requirements for credit for the course. If
  you have any questions or concerns about the requirements, please see an
  instructor.

[DigitalCrafts]:https://www.digitalcrafts.com/
[Node.js]:https://nodejs.org/

## Project Description

Your task is to build a copy of an existing web application using the backend
technologies we have learned in Phase 2: [express.js], [PostgreSQL], [knex.js],
etc.

You will not be designing something "new" for this project. Pick something that
already exists and rebuild it from scratch with your team. Examples: a Twitter
clone, a Facebook clone, a forum, an ecommerce website, etc. The project scope
should be well-understood and defined up-front. Please verify your project plans
with an instructor before beginning coding.

Focus on thoroughness of the implementation using backend technologies like
`GET` and `POST` requests, database schema and queries, user authentication,
form submission and validation, HTML templates, etc. You will have to have
*some* frontend aspect of the project, but the focus should be backend work.

Each team will present their project in class on **Tuesday, Jan 22nd**.

[express.js]:https://expressjs.com/
[PostgreSQL]:https://www.postgresql.org/
[knex.js]:https://knexjs.org/

## Technical Requirements

Your application **must**:

- You must use some form of HTML templating
  - Pure JavaScript functions that return strings, or use [template literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)
  - [mustache](http://mustache.github.io/), [handlebars](https://handlebarsjs.com/), [ejs](https://ejs.co/), [pug](https://pugjs.org/api/getting-started.html), etc

- Your project must be able to swap between database types by using a config file.
  - In other words, your database should not be tied to just PostgresQL
  - Hint: use an abstraction layer like [knex.js](https://knexjs.org/) or [Sequelize](http://docs.sequelizejs.com/)

- Your project must support database [schema migrations](https://en.wikipedia.org/wiki/Schema_migration).

- Have at least **two** `<form>` submissions that insert or edit data in a database.
  - Do not use AJAX; use a `<form action="">` HTTP POST request
  - The form should do input validation and show input errors in the UI (if necessary)

- Have at least one AJAX-based GET endpoint that powers a dynamic dropdown or type-ahead component
  - Examples: http://autocompletejs.com/examples#2000, https://jqueryui.com/autocomplete/#remote

- Have user authentication using [passport.js](http://www.passportjs.org/)
  - must support at least one OAuth provider (Twitter, Facebook, GitHub, etc)
  - must support passport.js "local strategy" backed with a database

- Your project must be hosted somewhere publicly reachable via `https`
  - Note that you do not need to purchase a domain name for your project. But it
    should be reachable via a public URL somewhere.

- Client-side JavaScript should be less than 200 lines of code.
  - Note: this does not include libraries
  - No cheating by writing all of your JS on one line, etc
  - The focus is backend, not frontend. But you will need some clientside code in some circumstances

- Your project must have a `README.md` file written using [Markdown] with at least the following:
  - Explanation of what the project is / what it does.
  - What technologies you used.
  - List of team members.

- Your repo must be connected to [Travis CI](https://travis-ci.org/):
  - You must run at least one test in your Travis CI build (hint: test for [StandardJS])
  - Put a build status badge in your `README.md` that links to your latest build

- Code must follow some organization scheme.
  - Everything cannot be in one super long file.
  - Break different parts of the code into different files / modules.
  - No "spaghetti code".
  - Bonus / optional: consider using a build system with [npm scripts], [browserify], or [webpack]

[Markdown]:https://guides.github.com/features/mastering-markdown/
[StandardJS]:https://standardjs.com/
[npm scripts]:https://deliciousbrains.com/npm-build-script/
[browserify]:http://browserify.org/
[webpack]:https://webpack.js.org/

## Workflow Requirements

- Teams will either be solo or groups of 3-5 students and assigned by instructors.

- Create one GitHub repo and add all group members as collaborators.

- Collaborate using Pull Requests (PRs):
  - No one should commit to the master branch directly.
  - Every PR should be reviewed and approved by at least one team member (not the person who originated the PR).
  - PRs should not be merged by the person who opened it (no self-merging).
  - See below for [suggested PR rejection criteria](#suggested-pr-rejection-criteria)

- Project features and bugs must be tracked using a [scrum]-like system:
  - Every PR should be associated with a GitHub Issue (or similar).
  - Consider using a tool like [GitHub Project Board] or [Trello].
  - Every class day teams will have a "stand up meeting" with a TA or Instructor.

[scrum]:https://en.wikipedia.org/wiki/Scrum_(software_development)
[GitHub Project Board]:https://help.github.com/articles/about-project-boards/
[Trello]:https://trello.com/

## Suggested PR Rejection Criteria

It's ok to reject a PR or have a PR rejected - that is what the PR process is
for! Remember if your PR is rejected that doesn't mean you are a bad person and
stink at life. It just means that your teammate(s) see something that could be
improved. The PR process is more about sharing knowledge than "you did something
wrong".

Any of the following are valid reasons to reject a PR:

- Breaks the build (Travis CI breaks)
- Does not fulfill feature
- Breaks other feature
- Does not follow team coding style / standards
- Too much to review / large code diff (ie: should be broken up into smaller PRs)
- Code in the PR does not match up with commit message
- Commit message is vague

## Learning Objectives

> TODO: write this section

--------------------------------------------------------------------------------

This requirements document is licensed as [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/):

> You can copy, modify, distribute and perform the work, even for commercial purposes, all without asking permission.
