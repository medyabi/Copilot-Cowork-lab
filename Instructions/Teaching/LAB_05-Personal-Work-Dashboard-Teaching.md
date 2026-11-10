---
teaching:
    title: 'Lab 05: Building a Personal Work Dashboard (Teaching edition)'
    module: 'Module 05: Scheduled automations'
---

# Lab 5: Personal Work Dashboard (Teaching edition)

**Time:** about 30 minutes. The prompts and screenshots for every step are in the [lab instructions](../Labs/LAB_05-Personal-Work-Dashboard.html). This whole lab is a walkthrough to save Copilot credits.

## Before we start: the Monday-morning tab dance

You know the routine. Open Outlook: what's unread? Open Teams: who pinged me? Open Calendar: what's today? Open OneDrive: where was that file? Ten tabs later, you still don't have the full picture.

What if one page showed all of it, and **updated itself every hour**?

That's this lab. Cowork builds a **personal work dashboard**: one HTML page with your meetings, emails, chats, files and projects. Then we schedule it, customize it and lock its format in.

Think of it like a car dashboard. You don't open the engine to check your speed. The numbers come to you.

## Task 1: Get in

Sign in at `m365.cloud.microsoft`, select **New** and make sure **Cowork** is on. Nothing new here. Let's get to the good part.

## Task 2: Build the dashboard

### A long prompt, on purpose

Look at the Task 2 prompt. It's long. Very long. Why?

Because a dashboard is a **specification**, not a question. The prompt tells Cowork three kinds of things:

1. **What to gather**: calendar, inbox, Teams, OneDrive, and a search for action-required emails. All **in parallel**, so it's faster.
2. **What to build**: a header, six KPI tiles, an urgent banner, a schedule, prep notes, projects, charts and more.
3. **How to build it**: colors, layout, and one big rule called **portability**.

### What's portability, and why care?

The prompt says: **zero external requests, zero JavaScript required**. No chart libraries. Charts drawn with plain CSS.

Why so strict? Because this file will be opened in places that block scripts: email attachments, previews, locked-down browsers. A dashboard that shows "0" everywhere because a script didn't load is worse than no dashboard. So we ask for numbers written **directly in the HTML**.

That's a good habit for any AI-generated file: tell it **where** the file will be opened, not just what it should contain.

### Every item is a link

One more rule: **every item must be clickable**. An email opens in Outlook. A chat opens in Teams. A folder opens in OneDrive. The dashboard isn't just a report. It's a **launchpad**.

### Wait for it

This one takes **5 to 10 minutes**. Cowork is pulling data from five sources, guessing your top projects and writing a full page. Watch the **Workspace** panel tick off the steps.

When it's done, open **dashboard.html**. Six KPI tiles, colored by urgency. A red banner for today's fires. That's your day on one screen.

## Task 3: Make it refresh itself

A dashboard from 8 AM is old news by noon. So we schedule it.

The Task 3 prompt asks for:

- A refresh **every weekday at :55 past the hour**, 6:55 AM to 5:55 PM.
- An **email** with the dashboard attached, but **only at the 9 AM run**. Every other hour refreshes silently.
- Automatic **daylight saving** handling, so the schedule never drifts.

Why :55 and not :00? So the dashboard is fresh **just before** the hour, when meetings start.

Cowork shows a **Create recurring task?** card, then a **Review permissions** page. Look at what it asks for: permission to **send email** through Outlook. Why? Because the task will run when you're **not there**. No one will be around to click an approval card at 9 AM. So you grant that permission now, once, for this task only.

### Test it now

Don't wait until tomorrow to find out it's broken. Open the task and click **Run now**.

What happens? Cowork rebuilds the file and says **"silent refresh, no email"**. Why no email? Because it's not the 9 AM run. The rule works.

Open the dashboard: the **Last refreshed** time has changed.

### A word about cost

Twelve runs a day, five days a week. That's **60 runs a week**, and every run uses credits. Great in production, expensive in a workshop. That's exactly why this lab is a walkthrough. If your trainer demos it, they'll pause it afterwards.

## Task 4: Make it yours

### Explore and switch theme

Scroll through the cards: tomorrow's schedule, prep notes, a bar chart of your week, a doughnut of where your time goes. Click the **Light/Dark** button. Dark mode, no JavaScript library needed.

### Lock it in

Here's a problem. Every time Cowork rebuilds the dashboard, it could design it slightly differently. New colors, cards in a new order. That's annoying for something you look at every day.

The fix is one sentence: **"Lock this dashboard format in for all future ones."**

Cowork then:

- saves a **reference copy** and the code that builds it in your OneDrive,
- updates the **scheduled task** so every run must match that reference,
- saves it as a lasting **preference** for future dashboards.

It asks for approval twice: a **Copy file** card (choose **Always allow** so future runs don't stall) and an **Edit scheduled task** card.

Now the design is fixed. Only the **data** changes.

### Change one thing

Don't need the Training & Learning card? Say so: **"Remove the training and learning card."**

Cowork removes it from the live dashboard **and** from the locked-in standard, then rearranges the other cards so the rows stay even. One sentence, and every future refresh follows.

## Task 5: Manage the automation

Go to **Automations > Scheduled**. There's your task. Open the **...** menu: **Edit**, **Run now**, **Pause**, **Delete**.

See two copies of the same task in the screenshot? That happens when a schedule is created twice. Two copies means twice the runs and twice the credits. Delete the duplicate.

## What did we learn?

- **A dashboard is a specification.** Tell Cowork what to gather, what to show and how to build it.
- **Say where the file will be opened.** Portable HTML works in email, previews and locked-down browsers.
- **Every item should be a link.** A dashboard is a launchpad, not just a report.
- **Scheduled tasks run without you.** Grant only the permissions they need, and test them with **Run now**.
- **Lock the format, refresh the data.** A stable layout makes a daily tool usable.
- **Automations cost credits.** Pause or delete what you don't use, and watch for duplicates.

Next up, Lab 6.
