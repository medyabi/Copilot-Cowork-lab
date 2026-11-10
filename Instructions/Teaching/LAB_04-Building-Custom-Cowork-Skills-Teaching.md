---
teaching:
    title: 'Lab 04: Building Custom Cowork Skills (Teaching edition)'
    module: 'Module 04: Custom skills'
---

# Lab 4: Building Custom Cowork Skills (Teaching edition)

**Time:** about 30 minutes. The prompts and screenshots for every step are in the [lab instructions](../Labs/LAB_04-Building-Custom-Cowork-Skills.html). Task 1 is hands-on; Tasks 2–8 are a walkthrough to save Copilot credits.

## Before we start: what is a skill, really?

Think back to Labs 1 to 3. Every time, you wrote a long prompt. Sections, tone, sources, "don't send anything"... Now imagine typing that same prompt every Friday. Boring, right? And error-prone. Forget one line and the output changes.

A **skill** fixes that. It's a set of instructions you write **once**, and Cowork applies them **every time** your request matches.

Here's an analogy. A prompt is like giving a new colleague directions every morning. A skill is like writing the **procedure** in the team handbook. From then on, you just say "do the leadership update" and they know exactly how.

Under the hood, a skill is a simple file called **SKILL.md** in your OneDrive, under `Documents/Cowork/skills/`. But you don't have to write it yourself. Cowork's **skill builder** interviews you and writes it for you.

## Task 1: Plan on paper first

Why paper? Because the builder asks good questions, but **you** need good answers. Five minutes of planning saves you a bad skill.

Open Notepad and answer five questions:

1. **What should this skill do?** One sentence. If you need two, you may need two skills.
2. **What does it need to read?** Your notes? Your mailbox? SharePoint?
3. **Does it write or change anything?** This is the big one. A skill that only *drafts* is low risk. A skill that *sends* is not.
4. **What should the output look like?** Sections, length, tone.
5. **What might change each time?** Project name, period, audience. These are your **parameters**.

Then turn your answers into a short **specification**: name, trigger phrases, parameters, apps it may read, apps it may write, output format.

Notice the line **"Apps it may write: None"**. Keep that in mind. It comes back in Task 8.

## Task 2: Meet the skill builder

Go to **Plugins**, then **Add > New skill**.

What happens? No form. Cowork starts a normal task and says: "Let's build your skill. I'll start with a few questions." Then a question card appears: **1 of 5**.

That's the whole idea. You build a skill the same way you use Cowork: by **talking** to it.

## Task 3: Answer the questions

The builder asks things like:

- **What should the skill help you do?** Paste your purpose from Notepad.
- **What should it be called?** Lowercase with hyphens: `leadership-update`.
- **Which category fits best?** Communication.
- **Which phrases would you type to use it?** These are the **trigger phrases**. They're how Cowork knows *when* to use your skill.
- **Any rules it should always follow?** Tone, length, sections, sources, and the important one: *"Never send, post, or change anything."*

Then Cowork goes to work. It writes the SKILL.md, checks it, and asks for approval with a **Copy file** card. Why a card? Because saving a file to your OneDrive is a **write**. Same rule as in every lab: changes need a human.

Approve it, and you get two things: the **skill** and a **quality report**.

### Read the quality report

Open the report. You'll see a score out of 100, a **Risk** indicator, a **Grounding** indicator and a checklist like "It switches on at the right time" and "It stays in its lane".

What's **grounding**? It means the skill only uses real sources (what you give it, or your Microsoft 365 content) and doesn't invent facts. That's exactly why we wrote "never invent figures, dates, or names" in the rules.

## Task 4: Does it actually work?

A skill you never test is just a hope. So test it.

Start a **New** task and send *"Use leadership-update"* with a vague paragraph of notes. Then check three things:

1. The activity log says **Reviewed custom skill Leadership update**. Cowork found it.
2. **leadership-update** shows under **Plugins** in the Workspace pane. Cowork used it.
3. The output has your four sections: Headline, Progress, Risks and Blockers, Asks / Next Steps.

Look closely at the output. See **[Add date]** and **[Add owner]**? Our notes didn't have those details, so the skill left **placeholders** instead of inventing them. That's grounding in action.

## Task 5: A second skill, faster

Now build **project-status-brief** for Project Orion. Same pattern, but notice two differences:

- The builder may ask **four** questions instead of five. The first one asks for purpose, triggers *and* output at once.
- If you pick a category Cowork doesn't accept, it picks the closest one and **tells you**. No silent changes.

Same ending: a **Copy file** card, approve, and a new quality report.

## Task 6: Look inside the skill

Open **Plugins** and select **project-status-brief**. This is the skill's **details page**.

Read the **Instructions**. Three sections matter:

- **Overview**: what the skill does.
- **When to Use**: the triggers.
- **When NOT to Use**: requests that belong to another skill, like **leadership-update**.

Why does "When NOT to Use" matter? Because skills compete. If two skills both claim "status update", Cowork has to guess. Clear boundaries mean the right skill fires.

Now open the **...** menu: **Download** and **Delete**. Rule of thumb: **download before you delete**. Deleting is permanent.

## Task 7: Share it as a file

A skill is just a file, so you can share it like one. Download it, then **Add > Upload** it again.

Cowork adds it as **project-status-brief-1**. Why "-1"? Because the name is already taken.

Here's a question for you: now there are two skills with the **same trigger phrases**. Which one runs? Hard to say. That's why, in real life, you delete the duplicate. Same lesson as Task 6: one job, one skill.

Then say the magic words: *"give me the project status brief"*. No "use project-status-brief" this time. The **trigger phrase** alone is enough. Cowork recognizes it, loads the skill and builds the six-section brief. Where a detail is missing, it writes **Not stated**.

## Task 8: Send it somewhere useful

Remember "Apps it may write: None"? Our skill only **drafts**. So how does the brief get to Teams?

You ask for it, in the conversation: *"Post this brief to the General channel of my Retail team."* And Cowork shows a **Post to channel?** card, with a risk level, the subject and the message. You can edit it, cancel it or send it.

See the design? The **skill** does the thinking. **You** decide what leaves the building. That's the safest way to build skills: drafting inside the skill, publishing behind an approval card.

Open Teams, **Retail > General**: there's your status brief.

## What did we learn?

- **A skill is a reusable procedure.** Write it once, and Cowork applies it every time your request matches.
- **Plan before you build.** Purpose, inputs, writes, output, parameters.
- **Trigger phrases decide when a skill runs.** "When NOT to Use" decides when it doesn't.
- **Test every skill.** Check the activity log, the Workspace pane and the output format.
- **Grounded skills use placeholders**, not invented facts.
- **Skills are files.** Download, share, upload, and delete duplicates.
- **Keep writes outside the skill.** Let the skill draft; let a human approve the post.

Next up, Lab 5.
