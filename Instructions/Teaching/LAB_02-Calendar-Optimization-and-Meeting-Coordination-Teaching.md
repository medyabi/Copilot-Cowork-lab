---
teaching:
    title: 'Lab 02: AI-Powered Calendar Optimization and Executive Meeting Coordination (Teaching edition)'
    module: 'Module 02: Calendar and meeting automation'
---

# Lab 2: Calendar Optimization and Meeting Coordination (Teaching edition)

**Time:** about 40 minutes. The prompts and screenshots for every step are in the [lab instructions](../Labs/LAB_02-Calendar-Optimization-and-Meeting-Coordination.html).

## Before we start: from assistant to executive assistant

In Lab 1, Cowork did one job at a time. Send five emails. Create three events. Useful, but simple.

Real executive assistants don't work like that. They work with **rules**. "Never book me before 10." "Protect my Friday afternoons." "If there's no agenda, push back." You say it once, and they apply it everywhere.

That's what this lab is about. We'll give Cowork rules, not just tasks. Then we'll see what happens when those rules collide with real life: a new meeting, an important review, and a week of vacation.

Ready? Let's go.

## Task 1: Teach Cowork your rules

### Give it the rules

On **Home**, make sure **Cowork** is selected and send the standing-rules prompt from Task 1. Read it again before you send it. It contains four rules:

1. Two **90-minute focus blocks** before noon, every day.
2. **Decline** meetings with no agenda, but ask the organizer first.
3. Keep **Friday afternoon** free.
4. **Show me** every change before you apply it.

That last rule is the important one. Why? Because rules touch *many* events at once. One wrong rule, applied to a whole week, makes a big mess. So we ask for a preview first.

### Read the proposal

Cowork checks your calendar, your time zone and your working hours. Then it shows a table of proposed changes and says something like *"Nothing has been applied yet."*

Look at the notes under the table. Cowork explains **how it understood your rules**. For example: "I read *two focus blocks* as two per day. If you meant two for the whole week, tell me." That's the agent showing its reasoning so you can correct it before anything happens.

Happy with it? Type **Approve all** and send.

### Approve the cards

Now the **Create calendar event?** cards appear: one per focus-block series, one for the Friday hold. Check the date, the time and the repeat pattern, then click **Save** on each.

Notice how few cards there are. Ten focus blocks, but only two cards. Why? Because Cowork created each block as a **recurring series**. Fewer approvals, same result.

Did Cowork ask you questions first, or skip straight to the cards? Both happen. Answer the questions and carry on.

### Check the result

Cowork ends with a day-by-day table: two focus blocks every weekday, Friday afternoon held, everything marked **Busy**. Your week is protected.

## Task 2: New meetings and a prep brief

### Add two meetings

Stay in the **same conversation** and send the two-meeting prompt from Task 2. Approve both **Create calendar event?** cards with **Save**.

Now read the summary carefully. Do you see something like *"The Monday call overlaps your focus block"*?

That's your rules at work. You booked a 10:00 call, and Cowork remembered the focus block you created ten minutes ago. It **flags** the clash and suggests a fix, but it doesn't move anything on its own. You're still the boss.

And the Teams link? If your summary says **Not added**, that's the same tenant limit you saw in Lab 1. Nothing to fix.

### Build the prep brief

Now a bigger job. Start a **New** Cowork task and send the prep-brief prompt from Task 2.

Look at how that prompt is written. It says **"from these three sources only"**: the calendar, the last 7 days of email, one OneDrive folder. Why limit it? Because the more you narrow the sources, the more **grounded** the answer is. Cowork can't invent facts if you've told it exactly where to look.

While it works, watch the **Workspace** panel. **Steps** shows the plan. **Plugins** shows which apps it's using: Calendar, SharePoint (that's where OneDrive files live), Outlook.

When it's ready to save, you get an **Approve action?** card. Check one thing: the **Parent path** must say **Lab Files**. Then click **Approve**.

Open the Word document. Is it all there? Purpose and agenda, attendees with your last interaction, related emails and files, open actions, decisions needed. That's a brief an executive would actually read.

## Task 3: The vacation problem

### Set up the problem

Here's the twist. You're on vacation **next Monday to Friday**. That's the same week you just filled with focus blocks, a client call and a budget review.

Sounds like a mistake? It's on purpose. We *want* conflicts, so we can watch Cowork find them.

Start a **New** Cowork task and send the vacation prompt from Task 3. Notice the last line: **"Take no action yet - just show me the plan."** First we look, then we act.

### Read the triage

Cowork scans email, calendar, To Do and Teams. Before the findings, it lists **coverage gaps**: sources it couldn't read. Often that's Planner and To Do. Is that a failure? No. An agent that tells you *what it couldn't see* is much safer than one that pretends it saw everything.

Then come the three buckets:

- 🔴 **Must Handle**: do it before you leave.
- 🟡 **Needs Delegation**: someone has to own it while you're away.
- 🟢 **Can Wait**: safe until you're back.

Scroll through all three. Don't worry if you have fewer items than the screenshots. It depends on how full your mailbox is.

### Plan the handoff

Send the follow-up: *"Go ahead and handle everything... get my approval before sending or posting anything."*

Cowork doesn't just charge ahead. It **asks you questions** first. Who covers for you? Reschedule, delegate or cancel your meetings? What about that unsent draft? Pick your answers and click **Next**, then **Submit** on the last one.

Then it shows the full plan: which meeting moves where, what's held until you return. And it says it hasn't touched anything yet.

### Execute, card by card

Send: *"Confirm the proposed actions and execute them."*

Now the approval cards arrive: **Update** for moved meetings, **Send cancellation** for cancelled ones, **Reply** for emails. Use the arrows to move between them.

Here's the habit to build: **read before you click.** Look at the Tailspin reply. Does it sign off with a name that isn't yours? Agents sometimes fill in placeholders. You can edit the text right in the card. The approval card isn't a formality. It's your last line of defense.

There's also an **Approve All** button. Handy, but only after you've read every card.

### Check the result

Cowork's final summary lists every meeting with its new time in your return week. Vacation week: clear. Nothing went out that you didn't see first.

## What did we learn?

- **Rules beat tasks.** Say it once and Cowork applies it across the whole week.
- **Preview first, apply second.** For bulk changes, always ask for the plan before the action.
- **Cowork remembers context.** It caught the clash between your new meeting and your focus block.
- **Narrow sources mean grounded answers.** Tell Cowork exactly where to look.
- **Coverage gaps are a feature.** A good agent tells you what it couldn't see.
- **Approval cards are your safety net.** Read them, edit them, then approve.

Next up, Lab 3: we go deeper into executive meeting preparation.
