---
layout: page
title: FAQ
permalink: /faq/
---

**Which fields can I group by?**
Team, Organizations, Request Type, Sprint, Status, Status category, Priority, Work type, Space, Parent, Assignee, Reporter and other people fields, Labels, Components, versions, select lists (single, multiple and cascading), checkboxes, radio buttons, groups, number and short text fields, and every date field by day, week, month, quarter or year.

**What can be summed?**
Any number field – "Story Points" of company-managed spaces, "Story point estimate" of team-managed spaces, your own number fields – and the original estimate, remaining estimate and time spent, shown in hours. You can also show the average, the minimum or the maximum.

**Why do the rows add up to more than the total?**
A work item with several values – two labels, two sprints, two organizations – is counted in each of them. The total counts every work item once. The gadget shows a note when this happens.

**Do viewers need special permissions?**
No. Each viewer sees the statistics of the work items Jira lets them see. If a viewer cannot see the saved filter, the gadget says so instead of showing wrong numbers.

**How many work items can a gadget count?**
Up to 50,000. The default limit is 5,000. Large searches are read in parallel; a few thousand work items take a few seconds. When a search finds more than the limit, the newest work items are counted and the gadget says so.

**Does it work in team-managed and company-managed spaces, and in Jira Service Management?**
Yes. Fields of all space types are offered; fields with the same name show their id so you can tell them apart.

**Does the app store our data?**
No. The app has no server side and no storage. Work items are read in your browser; the settings of a gadget are kept by Jira with the dashboard.

**Is our data sent anywhere?**
No. The app runs on Atlassian Forge and has no access to anything outside Atlassian.

**Does it support the dark theme and wallboards?**
Yes. The gadgets follow your Jira theme and reload at the interval you set.
