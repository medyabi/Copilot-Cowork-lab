---
teaching:
    title: 'Lab 01: Getting Started with Copilot Cowork (Teaching edition)'
    module: 'Module 01: Getting started with Cowork'
---

# Lab 1: Getting Started with Copilot Cowork (Teaching edition)

**Time:** about 40 minutes. The screenshots for every step are in the [lab instructions](../Labs/LAB_01-Getting-Started-with-Copilot-Cowork.html).

## Before we start: what is Cowork, really?

You've probably used **Copilot Chat**. You ask a question and get an answer. Then you ask the next question, and the next. You do the driving.

**Copilot Cowork** is different. You don't ask questions. You hand over a *job*.

Think of the difference between asking a colleague "what time is my next meeting?" and asking an assistant to "get me ready for my next meeting." The first needs one lookup. The second needs a plan: check the calendar, read the related emails, find the files, write a summary. Cowork builds that plan, runs it step by step, and shows you its progress.

| | Copilot Chat | Copilot Cowork |
|---|---|---|
| How you work | One question, one answer | One instruction, many steps |
| Who drives | You guide each step | Cowork plans and runs the steps |
| Best for | Quick lookups | Complex, repeatable workflows |
| History | No task history | Every task is saved and searchable |

So is Cowork going to send emails behind your back? **No.** Anything that changes something, like sending a mail or booking a meeting, appears first as an **approval card**. You read it and click **Send** or **Save**. Remember that idea. It comes back in every lab.

## Task 1: Sign in and look around

### Sign in

Open **Edge** and go to `www.office.com`. Click **Sign in**.

Enter your lab username, click **Next**, then enter your **Temporary Access Pass** and click **Sign in**. You'll find both on your lab environment's details page. When asked *Stay signed in?*, choose **No**. It's a shared lab machine, so don't leave the door open.

### Start a Cowork task

On the **Home** tab, click **New**. Look at the task box: there's a switch with **Chat** and **Cowork**. Pick **Cowork**.

That switch is the whole difference we just talked about. Same box, two very different engines.

### Borrow a ready-made prompt

What if you don't know what to ask? Under **Try these next**, click **Show more**. This opens **Task ideas**, a library of ready-to-run prompts grouped into **Triage**, **Research**, **Create**, **Meetings** and **Automate**.

Search for **Prep for a meeting**, open it, and click **Use this task**.

Now read the prompt Cowork drops into the task box. Notice something? It's not one question. It's a full brief: find my next meeting, read the related emails and Teams messages, ask me a few questions, then write a prep summary. That's what a good Cowork prompt looks like.

Clear the box **without sending it**. We'll run real tasks soon.

### Meet the Plugins page

Click **Plugins** in the left menu. This is where Cowork gets new abilities.

Two words to learn here:

- A **skill** is a set of instructions that teaches Cowork *how* to do a job your way.
- A **plugin** is a package. It can hold skills, **connectors** to outside systems, or both.

Click the **Filter** icon next to **Discover** and pick **Collaboration** to narrow the list. Then click **Add** at the top. You'll see **New skill** and **Upload**. You'll build skills in Lab 5 and a full plugin in Lab 7. For now, just know where the door is.

## Task 2: Fill your inbox

Here's a problem. A fresh lab account has an empty mailbox. Cowork works on *your* data, so with no data it has nothing to work with.

The fix? We let Cowork create the data itself.

Click **New**, make sure **Cowork** is selected, paste the Task 2 prompt from the [lab instructions](../Labs/LAB_01-Getting-Started-with-Copilot-Cowork.html) and click **Send**.

Now watch the **Workspace** panel on the right. It has three parts:

- **Steps**: Cowork's plan, ticked off one by one (*Send email 1 — Northwind Retail*, and so on)
- **Tools** / **Plugins**: the apps it's using, here **Outlook**
- **Output**: what it produced, here five sent emails

This panel is your window into the agent's head. Get used to glancing at it.

### Will you see approval cards?

Maybe, maybe not. The prompt says *"You have my approval to send all 5"*, so Cowork often just sends them and replies **Done.** Sometimes it still stops and shows a **Send email?** card for each one. If you get cards, read each email and click **Send**. Five cards, five clicks.

Either way is correct. Why the difference? Cowork weighs the risk of each action. Sending mail outside the company is a bigger deal than mailing yourself.

### Check the result

Open the **app launcher** (the nine dots, top left) and choose **Outlook**. If *Your privacy matters* pops up, click **Continue**. Open **Inbox**. You should see 5 new emails, each starting with its tag: **\[Northwind Retail\]**, **\[Fabrikam Industries\]**, **\[Tailspin Toys\]**, **\[PMO\]**, **\[PMO – Risk Management\]**.

The Tailspin one has a red **!** for high importance. Cowork picked up the word *URGENT* on its own.

## Task 3: Fill your calendar

Same trick, different app. Go back to your Cowork conversation and send the Task 3 prompt in the **same** conversation.

Look at the **Steps** panel. The counter might say *7/11* instead of starting from zero. Did something break? No. You're in the same conversation, so the email steps are still on the list.

Notice the first thing Cowork does: **Check calendar for conflicts**. You asked for that rule, and it checks *before* it acts. That's planning, not just typing.

If a **Create calendar event?** card appears, check the date and time and click **Save**. Note the **Medium risk** badge: creating events counts as a real change.

### What about the Teams link?

In some lab tenants Cowork tells you it **couldn't add a Teams meeting link**. That's the environment, not you. Cowork still creates the events, and it tells you honestly what it couldn't do. That honesty is exactly what you want from an agent. If you need a link, open the event in Outlook and switch on **Teams meeting**.

### Check the result

In Outlook, click the **Calendar** icon on the left and choose **Work week**. You should see three events on the next three business days: **Steering Committee Review**, **Security Assessment Meeting** and **Go-Live Readiness Review**. Your dates will differ from your neighbor's if you didn't start on the same day.

## Task 4: Upload files and create a team

This one is old-fashioned clicking, no AI. Why? Later labs ask Cowork to classify, rename and govern files, and to post in Teams, so the files and the team must exist first.

### OneDrive

Open the app launcher and choose **OneDrive**. Dismiss *Work smarter with Copilot* with **Not now**. Go to **My files**.

1. Click **Create or upload > Folder**, name it **Lab Files**, click **Create**, then open it.
2. Click **Create or upload > Folder upload**, browse to `C:\LabFiles\lab file`, select **Archivecandidates** and click **Upload**. Confirm the *Upload 4 files to this site?* prompt with **Upload**.
3. Repeat for **Healthcare**, **Retail** and **Shared files**. Skip **Project Orion Files** for now.
4. Click **Create or upload > Files upload**, select the four files (`access-control-policy`, `data-retention-policy`, `zava-audit-checklist`, `zava-risk-register`) and click **Open**.

Check: **Lab Files** now holds 4 folders and 4 files, so **8 items**.

5. Go back to **My files**. Click **Create or upload > Folder upload**, select **Project Orion Files** and click **Upload**.

Check: **Project Orion Files** sits in **My files**, next to Lab Files, with **8 items**.

Why does Project Orion Files go somewhere else? Because Lab 4 asks Cowork to find and govern it as a separate project area.

### Teams

Open the app launcher and choose **Teams**. Click **Get Started** on the welcome screen and close the QR-code tab.

Under **Teams and channels**, click **See all your teams**, then **Create team**. Name the team **Retail**, keep the first channel as **General** and click **Create**. Click **Skip** when asked to add members.

Check: **Retail > General** appears in the left list with *Welcome to your new team!*

## Task 5: Context, history and automations

Your environment is full of data now. Let's see how Cowork *uses* it.

### Work context: the + button

In Cowork, click **New**, then the **+** in the task box, then **Add content**. A picker opens with tabs: **All, Skills, People, Files, Meetings, Emails, Chats, Copilot, Channels, Sites, Fabric**.

Click through them. Recognize anything? Your **\[Tailspin Toys\]** email is there. So are your files.

Why does this matter? Cowork already searches your data on its own. But when *you* attach the exact email or file, you remove the guesswork. It's like handing a colleague the folder instead of saying "it's somewhere on the drive."

Press **Esc** to close the picker.

### Task history

Every Cowork task is saved. Look at **Recent** in the left menu: *Seeding Outlook Inbox with Training Emails* is already there. Click **Search** in the left menu, type **Seeding**, and open the task. You land right back in the conversation, with its steps and output.

Chat forgets. Cowork keeps a record.

### Your first automation

So far, Cowork only worked when you asked. What if it could start on its own every morning?

Click **Automations**, then **Add > Create with Cowork**. In the task box, send:

```
I want to set up a scheduled task. Briefly explain how scheduled tasks work in Cowork, then ask me a few questions to figure out what I'd like Cowork to do and when it should run.
```

Cowork explains, then interviews you with quick question cards:

1. *What would you like Cowork to do on each run?* Pick **Morning briefing**, then **Next**.
2. *How often should it run?* Pick **Every weekday**, then **Next**.
3. Pick a run time, then **Next**.
4. *How should you get the results?* Pick **Email to me**, then **Submit**.

Cowork shows a summary card with the name, schedule and description. Leave **Run once now** ticked and click **Schedule**.

Because *Run once now* is ticked, a **Send email?** card appears for the first briefing. Look at the button: **Always allow: Only to \<your address\>**. Click it. You're telling Cowork: "for this automation, you may email *me* without asking." Only you, nobody else. That's a tight, safe permission.

Now click **Automations**. Under **All > Active** you'll see your briefing, with something like *Every weekday at 08:00 · Next run: in 15 hours*. The name might be *Weekday Morning Briefing* or close to it. That's fine.

### One more look at Task ideas

Click **New > Show more**. Browse the ideas: **OOO handover pack**, **Calendar audit**, **Unread email triage**... Sound familiar? Several of them are exactly what you'll build in the next labs.

Search **Meeting briefing**, click **Use this task**, read the prompt, then clear the box without running it.

## What did we learn?

- **Cowork takes jobs, not questions.** It plans the steps and shows them in the **Workspace** panel.
- **You stay in control.** Changes go through **approval cards**, and "Always allow" can be scoped tightly.
- **Your data is the fuel.** You seeded emails, events, files and a team, and every later lab runs on them.
- **Work context** (the + button) lets you point Cowork at the exact item.
- **Task history** keeps every task searchable.
- **Automations** let Cowork run on a schedule, without you starting it.

Next up, Lab 2: we put Cowork in charge of your calendar.
