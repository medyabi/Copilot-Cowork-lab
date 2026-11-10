---
teaching:
    title: 'Lab 06: Building and Publishing a Custom Cowork Plugin (Teaching edition)'
    module: 'Module 06: Plugins and MCP'
---

# Lab 6: Build and Publish a Cowork Plugin (Teaching edition)

**Time:** about 30 minutes. The prompts and screenshots for every step are in the [lab instructions](../Labs/LAB_06-Build-and-Publish-a-Cowork-Plugin.html). This whole lab is a walkthrough: publishing needs an admin role you don't have.

## Before we start: from skill to plugin

In Lab 4 you built a **skill**: one recipe that teaches Cowork how to do one job. Useful. But what if you need seven related recipes, plus live data from outside Microsoft 365, and you want to hand all of it to the whole company in one go?

That's a **plugin**.

Think of it like a toolbox. A skill is one tool. A plugin is the box: several tools, plus the **connector** that plugs them into the outside world, packed so anyone can pick it up.

In this lab, Cowork builds a **Financial Research** plugin. It has:

- **Seven skills**: company snapshot, financial trends, peer comparison, risk factors, earnings, executives and filing search.
- **One connector** to **SEC EDGAR**, the public database of US company filings.

Then an admin publishes it, and we ask it real questions.

## What's MCP?

The connector uses the **Model Context Protocol**, or **MCP**. What is that?

Think of a power socket. Every appliance has the same plug, so any appliance works in any socket. MCP is that standard plug for AI. A service puts its data behind an **MCP server**. Any AI that speaks MCP can plug in and use its tools.

Here, the SEC EDGAR MCP server offers tools like **secedgar_company_search** and **secedgar_get_financials**. Our skills tell Cowork **when** and **how** to use them.

One warning. This MCP server is run by a community developer, not by Microsoft or the SEC, and it needs no sign-in. That's fine for public filings in a classroom. In your company, only plug in servers your security team has approved. Would you plug a stranger's charger into your laptop?

## Task 1: Look before you build

Open **Plugins** and look around. What's already **Added**? Select **Add**: you get **New skill** and **Upload**. Filter on **Skills**: nothing custom yet.

Why bother? Because you want a clean starting point. If a plugin with the same name is already there, you'll get confused later. (In the screenshots, the demo tenant already has a few copies of Financial Research. Yours won't.)

## Task 2: Let Cowork build the package

### A prompt that reads like a spec

The Task 2 prompt is long. That's on purpose. It's not a question, it's a **build specification**. It tells Cowork:

1. **What goes in the box**: seven skills, one connector, two icons.
2. **Where each file goes**: the exact folder structure.
3. **The manifest**: the ID card of the plugin, given word for word.
4. **The rules**: what must be at the top level, what must never be nested.
5. **How to check its work**: a validation checklist.

Why so strict? Because the admin center is strict. One property in the wrong place and the upload fails. When the target is picky, the prompt must be precise.

### The manifest: the plugin's ID card

**manifest.json** answers the questions the admin center asks: What's your name? Who made you? What's in the box? Where are your skills? Which servers do you talk to?

Two lines matter most:

- **agentSkills** lists the seven skill folders.
- **agentConnectors** points to the SEC EDGAR MCP server.

Both sit at the **top level** of the manifest. Not inside anything else. The prompt says it three times, because it's the most common mistake.

### Wait, then check

Cowork takes **5 to 10 minutes**. When it's done, look at **Output**: one ZIP, seven SKILL.md files, the manifest and two icons.

Open the ZIP from OneDrive, download it, and look inside. Seven skill folders. Everything where the spec said. Trust, but verify.

## Task 3: Publish it

Now the admin takes over. In the **Microsoft 365 admin center**: **Settings > Integrated apps > Upload custom apps**.

The flow is short:

1. Choose **Teams app** and upload the ZIP.
2. Wait for **Manifest file validated**. That's the admin center checking the ID card.
3. Choose who gets it. We pick **All users**.
4. **Finish deployment**. Done.

Why "Teams app" for a Copilot plugin? Because Microsoft 365 uses one app format, the **unified app manifest**, for Teams apps, agents and plugins. The package decides where it shows up, not the upload box.

Notice that Cowork's summary pointed to a different path: **Copilot > Agents > Upload agent**. Both live in the Microsoft 365 admin center. What you must avoid is the **Teams admin center**: it may register the package as a Teams-only app.

### Plan B

Deployment didn't work? You can still add the plugin yourself: **Plugins**, search **Financial Research** under **Discover**, **Install**, then turn it on.

## Task 4: Turn it on and ask questions

Published doesn't mean active. Open **Plugins**, find **Financial Research** under **Added**, and look: the toggle is **off**. Turn it on.

Now ask: **"Give me a snapshot of Microsoft."**

Watch the **Workspace** panel. You'll see **Financial Research** under Plugins, and steps like **Secedgar get filing**. That's the connector at work: Cowork is reading Microsoft's actual SEC filings, live.

Then ask: **"Show Microsoft's five-year revenue trend."** This time Cowork calls **Secedgar get financials** and builds a five-year table with growth rates and margins.

Notice what you **didn't** do. You didn't name a skill. You didn't name a tool. You just asked. The skill descriptions and trigger phrases did the matching for you. That's why we wrote them so carefully.

One last reminder: these are AI-generated numbers from public data. Great for research. Not investment advice. Check the filing before you quote a figure.

## What did we learn?

- **A plugin is a toolbox**: several skills plus the connectors they need, in one package.
- **MCP is the standard plug** between AI and outside services. Only plug in servers you trust.
- **A precise spec beats a vague prompt** when the target, like the admin center, is strict.
- **The manifest is the plugin's ID card.** Skills and connectors go at the top level.
- **Publish from the Microsoft 365 admin center**, never the Teams admin center.
- **Published isn't enabled.** Users still turn the plugin on, then just ask in plain language.

Look how far you've come: from your first Cowork task in Lab 1 to building and shipping your own plugin. Well done.
