---
layout: page
title: User guide
permalink: /guide/
---

## Add a gadget
1. Open a dashboard and click **Edit**, then **Add gadget**.
2. Search for **Statistics** and add **Field Statistics** (a chart of one field) or **Two-Dimensional Statistics** (a table of two fields). Both have the same settings; they only start with different defaults.
3. Fill in the settings – the **Preview** below them shows the result as you go – and click **Save**.

To change a gadget later, open the dashboard editor and choose **Edit** in the gadget's ••• menu.

## Work items
- **Saved filter** – type a part of the filter's name and pick it. Your starred and own filters are offered first. People who view the dashboard must be able to see the filter.
- **JQL search** – type any JQL, for example `project = WEB AND statusCategory != Done`. The gadget tells you how many work items it finds, or what Jira does not understand.
- **Count at most** – 1,000 to 50,000 work items (5,000 by default). When a search finds more, the newest work items are counted and the gadget says so.

## Statistics
- **Rows** – the field to group by. Team, Organizations and Sprint come first; every field of your site that can be grouped follows.
- **Columns** – a second field, or *None* for one dimension.
- For **date fields** (Created, Resolved, Due date, your own dates) choose the period: day, week, month, quarter or year.
- **Value** – the number of work items, or the **sum** or **average** of a number field: story points, your own number fields, original estimate, remaining estimate, time spent (shown in hours).
- **Order of rows** – *Automatic* puts statuses in workflow order, dates, sprints and priorities in their natural order, and everything else by the highest value. You can also sort by name or by value.
- **Rows shown** – the top rows are shown and the rest is added up as *Other*. Use 0 to show everything.

## Display
- **Chart** – bars, columns, line, pie, donut, or no chart. With columns chosen, bars and columns are stacked and the line chart draws one line per column value. A pie needs one dimension.
- **Show the table** – the numbers under the chart. Bars of one dimension already show the value, the share and the total.
- **Heat map** – colours the cells of a two-dimensional table by their value.
- **Show percentages** – the share of each row in the total.
- **Include work items without a value** – shows them as *None*; untick to leave them out.
- **Title** and **Refresh every** – an optional heading and how often the gadget reloads.

## Reading a gadget
- Click **any number, bar, column or slice** to open those work items in the Jira search.
- Hover a chart to see the values.
- **CSV** under the gadget downloads the table.
- A work item with several values (labels, sprints, organizations, components) is counted in each of them; totals count every work item once. The gadget tells you when this happens.
- When some work items have no value to sum (for example no story points), the gadget says how many.

## Examples
- *Team by Status* with the sum of story points – who has how much work in which state.
- *Organizations* as a donut over a service space – which customers raise the most requests.
- *Sprint* by *Status category* as columns – what was finished in each sprint.
- *Parent* by *Status category* with the sum of story points – progress of every epic.
- *Resolved* by month as a line, with *Work type* as columns – throughput over time.
