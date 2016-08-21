# 👻 GHoST Projct Management System (proposa)

This board is an example of how we could use **GitHub + Harvest + (on) + Slack + Trello** (👻 GHoST) for Agile project management.

## Introduction

This new proposed system wants to replace the tools used by EC to manage projects with more comfortable/modern ones while **maintaining the EC work-style unadulterated**. To be more precise, here are the goals that this new system tries to achieve (in priority order):

0. Maintain the Elastic Coders style of project management and work the same as it is today;
1. All team members *must* feel comfortable in using project management tools; tool must not get in the way of work but rather augment work capabilities;
2. Client and team *must* have a clear and simple view of the state of the project at all times;
3. Team members not directly involved in pure management task *should not* be bothered by project management tools while working on code;
4. Every team member *should* have his/her objective for the day clear at all times;
5. Tools *may* allow the creation of periodical time reports and other kind of reports/analytics;
6. Tool *may* be pleasant to use and never obtrusive.

## Setup

This configuration can be used with a free Trello. However a business class Trello would offer a much better integration with other services (see below).

- Install [Agile SCRUM for Trello Chrome extension](https://chrome.google.com/webstore/detail/agile-scrum-for-trello-bo/njmflagahgdhopbcdilgahjlfiecakpe?hl=en)
- Install [Harvest time tracker Chrome extension](https://chrome.google.com/webstore/detail/harvest-time-tracker/fbpiglieekigmkeebmeohkelfpjjlaia?hl=en)

### Business class

With business class the GitHub integration is much better allowing for example to see PR status. Slack integration allows to be reminded about cards, link a Slack conversation to Trello cards and much more.

- [GitHub and Trello integration](http://blog.trello.com/github-and-trello-integrate-your-commits/)
- [Harvest and Trello integration](https://www.getharvest.com/blog/2012/11/use-trello-track-time-with-the-harvest-chrome-extension/)
- [Slack and Trello intgration](http://blog.trello.com/slack-trello-integration-powerup/)

## The GHoST System

### GitHub

GitHub might be used for code management, release informations and intra-task discussions. GitHub issues may be disabled so that any non code specific discussion (done in PRs) will take place in Trello instead.

GitHub is the best and most used code management repository:

- Developers would feel right at home in use GitHub
- Discussions can target actual code lines and be focused on PRs scope
- Many tools like CI integrate seamlessly with GitHub

### Harvest

Harvest is a very popular time tracking app which allows time reporting and invoicing. By having a dedicated tool for time tracking we could:

- Have a person dedicated for time reporting (with a simple and clear tool)
- Simple actual time recording from Trello or Chrome extension
- Add a time entry without being required to create a dummy "card" just to add a title to the entry (harvest allow to add titles and descriptions directly to time slots)

### Slack

Slack is used as usual, as a chat for quick communication and whatnot. From that, a manager or team member could create a Trello card with a linked discussion to justify it.

### Trello

Trello is where the core of the project management would happen.

#### Trello Boards Organization

First of, you should create a new board for a project and have this lists:

- Backlog
- Sprint N + 1
- Sprint N
- In Progress
- Review
- Done - Sprint N

The meaning should be self explanatory and will be more clear in the next section (workflow). One particular list might be "Done - Sprint N" which will contains all cards done in that sprint. When the sprint ends the whole list will be archived (it will be reachable in the archived lists).

#### Trello Workflow

1. New cards are created in the *Backlog* list. The more informations added to the card the better.
2. A manager moves the card in a *Sprint* list. This should usually happen in sprint meetings. It might be a good measure to have at most 2 *Sprint* lists at all times: the current sprint and the next one.
3. A team member moves a card from the current *Sprint* list to *In Progress*. Of course, critical bugs or other cards could be moved or created in the *In Progress* list directly.
4. When a card is finished, the team member moves it in the *Review* list.
5. A manager moves the card from *Review* to *Done – Sprint N* after review (or back into the current *Sprint* list if needed).
6. At the end of a sprint, a retrospective card (see later) is created in the *Done - Sprint N* list and the list is archived all together after all the bureaucracy for the completed sprint is done (which might also be tracked in a card).

#### Trello Retrospective

A retrospective for a sprint is just another card named *Retrospective - Sprint N* (for easy search). It may contain a time report for that sprint, google docs links for retrospective documents or just descriptions/checklist.

Everyone will be able to comment on the retrospective card to state their opinion on the sprint.
