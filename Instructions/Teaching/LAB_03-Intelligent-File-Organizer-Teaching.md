---
teaching:
    title: 'Lab 03: Intelligent File Organizer (Teaching edition)'
    module: 'Module 03: File organization and governance'
---

# Lab 3: Intelligent File Organizer (Teaching edition)

**Time:** about 40 minutes. The prompts and screenshots for every step are in the [lab instructions](../Labs/LAB_03-Intelligent-File-Organizer.html).

## Before we start: the messy shared folder

Every company has one. A folder full of files called *Final*, *Final_v2*, *Report (1)* and *Copy of Copy of Tracker*. Nobody knows which version is current. Nobody knows who owns what. And then someone says the word **"audit"**.

Cleaning that up by hand is slow and boring. So why not let an agent do it?

Here's the catch. Renaming, moving, archiving and deleting **change things**. Some of those changes are hard to undo. So in this lab we'll let Cowork do the heavy lifting, but we'll keep our hand on the brake the whole time.

One rule for this lab: **stay in one conversation**. In Task 1 we ask Cowork to build an inventory of the files and *remember* it. Tasks 2 and 3 reuse that inventory. Start a new task and Cowork forgets it.

## Task 1: Classify and rename

### Ask for a plan, not an action

Start a **New** Cowork task and send the classification prompt from Task 1. Look at what it asks for:

- **Classify** every file by business function: Sales, Procurement, Security or Executive.
- **Propose** a name in the form `YYYY-MM-DD_BusinessFunction_DocType`.
- **Show** an old-name → new-name table, and nothing else.

Notice what's missing? The word *rename*. We're asking for a **proposal**. Nothing changes yet.

Why that naming format? Because dates first means files sort in time order, the function tells you who owns it, and the doc type tells you what it is. Anyone can read `2026-03-31_Sales_QuarterlyReport-v2.docx` and know exactly what it is.

### Check the mapping

Cowork reads each file, not just its name, then shows the table. Read the note under it. Cowork tells you **where each date came from**: a meeting date or effective date inside the document, or the file's creation date when the document has none.

That's important. A good agent shows its evidence, so you can judge it.

### Approve the rename

Happy with the names? Send the "Proceed with the renaming…" prompt. Now Cowork *will* change things, so the approval cards arrive:

- **Create folder?** for *Project Orion - Renamed Files*: click **Create**.
- One card per subfolder, rename and move: click **Approve**, or **Approve All** once you've looked at them.

Did a few actions fail and get retried? That happens. Cowork tells you and tries again. Just approve the new cards.

### Check the result

Open **OneDrive**, go to **Lab Files › Project Orion - Renamed Files**. You should see four folders: **Executive**, **Procurement**, **Sales**, **Security**. Open one. Every file now has a clean, sortable name.

Ten minutes ago, this was a mess. Now it's organized, and you approved every step.

## Task 2: The governance audit

### Audit without re-reading

Go back to the same conversation and send the audit prompt from Task 2. Look at the first line: **"Using the file inventory you already built - do not re-scan or re-read any files."**

Why say that? Speed and consistency. Cowork already knows these files. Reading them again costs time and may give slightly different answers.

The audit looks for four problems:

1. **Duplicates**: the same file twice.
2. **Stale files**: not touched in six months.
3. **Over-shared files**: "anyone with the link" access.
4. **Orphans**: no clear owner.

And the last line again: **"Take no action yet."**

### Read the findings, and the gaps

Cowork shows a table: each finding with a recommended action (archive, delete, restrict sharing).

Now read the notes under the table. Cowork may say something like: *"I can't check sharing links from the inventory, because it holds content, not permissions."* Or: *"Every file has a recent timestamp because we just renamed them, so I judged staleness by the dates inside the documents."*

Is that a problem? No, it's honesty. Think of an auditor who says "I didn't check the safe, I don't have the key." That's far better than one who pretends the safe is fine.

### Approve only part of the plan

Here's the key skill of this lab: **you don't have to accept the whole plan.**

Send the follow-up: *"Approve only the archive actions… leave everything else pending."* Archiving is safe because files move to a folder; they don't disappear. Deleting and changing permissions? Not today.

Click **Create** for the **Archive** folder and approve the moves. Then check OneDrive: the archived files are in **Archive**, everything else is untouched.

### Ask the big question

Now ask Cowork directly: *"Which of these governance actions should an agent ever take WITHOUT human approval?"*

Read its answer carefully. It usually splits the world in two:

- **Safe without approval**: reading, classifying, finding duplicates, writing reports. These change nothing. The worst case is a bad suggestion you ignore.
- **Always needs a human**: **deleting** (hard to undo), **restricting sharing** (silently breaks someone else's access), **renaming and moving** (can break links).

That's the rule of thumb for any agent. **Reads are free. Changes need a human.**

## Task 3: Report it

### One instruction, two apps

Send the tracker prompt from Task 3. It asks for two things in one go:

1. An **Excel workbook** with one row per file: name, type, business function, last modified, sharing status, action taken.
2. A **3-line summary** posted to the **General** channel of your **Retail** team, with a link to the workbook.

Two apps, one sentence. That's what an agentic workspace is for.

### Approve the upload and the post

You'll see an **Approve action?** card for the workbook. Check the file name, click **Approve**.

Then a **Post to channel?** card. Check it says **Retail › #General**. Read the message. Is it empty? Then write your own three lines, using **your** numbers, not the screenshot's. Click **Send**.

What if Cowork says the upload to Lab Files failed? Then it saves the tracker to your **Cowork** folder in OneDrive instead and tells you so. The work is done, just in a different place.

### Check the result

Open the workbook: one tidy row per file. Then open **Teams › Retail › General**: your cleanup summary is there for the team to see.

## What did we learn?

- **Plan first, act second.** Ask for a mapping or an audit before any change.
- **Show me the evidence.** Cowork explains where dates and findings come from, so you can judge them.
- **You can approve part of a plan.** Archive today, decide on deletes later.
- **Honest gaps beat fake confidence.** An agent that says "I couldn't check this" is a safer agent.
- **Reads are free, changes need a human.** That's the governance rule for any AI agent.
- **One conversation, one memory.** Reusing the inventory keeps every step fast and consistent.

Next up, Lab 4.
