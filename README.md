# Claude SMB Workshop

Hands-on materials for the **Claude SMB Workshop**, run by the GRCC AI Incubator in partnership with Zorrillo Works. Small business owners and their teams put Claude to work on real jobs, with a workspace that remembers how they work.

No prior AI or coding experience is required.

**This session:** Wednesday, November 18, 2026, 5:30 to 8:30 PM. Grand Rapids Community College, Calkins Science Center, Room 133.

**Slides:** [Claude SMB Workshop Slides (PDF)](slides/Claude-SMB-Workshop.pdf)

---

## Agenda

| Time | Block |
|---|---|
| 5:30 to 5:45 | Welcome, the mental model, the 4Ds framework, and data safety |
| 5:45 to 6:15 | Demo: how I run my work with Claude, using folders called HQs |
| 6:15 to 6:40 | Hands-on: set up Claude and build your workspace (Steps 1 to 4) |
| 6:40 to 7:00 | Hands-on: build your Quote Creator HQ and test it (Steps 5 to 7) |
| 7:00 to 7:10 | Break |
| 7:10 to 7:30 | Optional: build a second HQ (Steps 8 and 9) |
| 7:30 to 7:50 | Hands-on: connect a tool (Steps 10 and 11) |
| 7:50 to 8:15 | The Claude for Small Business plugin (Steps 12 and 13) |
| 8:15 to 8:30 | Keep it sharp, questions, and survey |

Topics covered:

- The 4Ds of AI fluency: delegation, description, discernment, and diligence
- Context beats prompts: instructions, knowledge, and memory
- A Claude workspace with a CLAUDE.md rules file and a MEMORY.md notepad
- A Quote Creator HQ for your own business, built from one prompt
- Connectors: letting Claude read a tool you already use, with your OK
- The Claude for Small Business plugin

---

# Workshop Guide

This is your copy and paste guide. **Prompts are tucked into lines that start with ▸ Prompt.** Click the line to open it, click the copy icon in the top right corner of the gray box, then paste it into Claude. Every prompt works as is, except the one in Step 8, which has one blank (____) for you to fill in. After each step, "You should see" tells you it worked.

By the end you will have:

- Claude set up with your preferences and a few safety guardrails
- A Claude workspace folder that remembers how your business works, from one session to the next
- A Quote Creator HQ for your business that quotes from a price list, refuses to make up prices, and remembers a customer's discount
- One of your tools connected to Claude
- The Claude for Small Business plugin installed and onboarded

**Before we start,** check these three things. The steps stall without them.

1. **Claude desktop app** installed and signed in ([claude.com/download](https://claude.com/download)). The phone app and the website can't reach folders on your computer.
2. **Your Claude Max code redeemed** on the web at [claude.ai](https://claude.ai). Codes don't work in the mobile app.
3. **This page open** in a browser next to Claude, so you can copy and paste.

Before you put company information into any AI tool, follow your company's AI policy.

## Part 1: Set Up Claude

### Step 1. Your general Claude preferences

Open a regular Claude chat and paste this. Claude will interview you and then write your preferences.

<details>
<summary><strong>▸ Prompt: General Claude preferences</strong></summary>

```text
Interview me so you can write my personal preferences for Claude. Ask exactly these four questions, one at a time, and no others:

1. What is your role, what company do you work for, and what does the company make, sell, or do?
2. How do you like answers: short or detailed, and in paragraphs or bullet points?
3. How much should I explain technical things like files, settings, and spreadsheets?
4. When something is unclear, should I ask you first or make a reasonable call and tell you what I assumed?

When we're done, write my preferences as one block of text in the first person, under 300 words, with two short sections: "About Me" and "How to Work With Me." I will paste it into my Instructions for Claude in Settings, so give me only the text, ready to paste.
```

</details>

Answer the questions. When Claude gives you the finished text, click its copy button. Then:

1. Click your initials in the lower left corner of the app.
2. Click **Settings**, then **Your Claude**.
3. Paste the text into the **Instructions** box and save.

These instructions apply to every conversation.

**Looks different?** Some versions of the app show **Settings → Account → Instructions for Claude** instead. It is the same box.

**You should see:** your preferences saved under Instructions.

### Step 2. Your guardrails

Go back to the same box: **Settings → Your Claude → Instructions**. Paste these lines **below** your preferences and save. They make Claude read your workspace rules first, and stop it from touching your files or sending anything without asking. Loosen them later, once you trust how it behaves.

<details>
<summary><strong>▸ Prompt: Guardrails to add to your Instructions</strong></summary>

```text
How I want you to work:
- When I'm working in a folder, read the CLAUDE.md and MEMORY.md files in that folder before doing anything else, and follow them.
- Before deleting, overwriting, or renaming any existing file, show me exactly what will change and wait for my confirmation.
- Never modify files outside the folder I'm currently working in unless I explicitly ask you to.
- For any multi-step task, outline a brief plan first and wait for my approval before executing.
- Before sending emails, posting messages, changing calendar events, or taking any other external action, show me the proposed action and wait for confirmation.
- If instructions conflict, required context is missing, or you are unsure which file should be changed, stop and ask instead of guessing.
- Preserve existing file names, folder structure, formatting, and content unless I explicitly ask you to change them.
```

</details>

**Looks different?** If your app still has a separate Cowork tab, these go in **Settings → Cowork**: click **Edit** next to **Global instructions**.

**You should see:** your preferences and the guardrails together in one Instructions box.

---

## Part 2: Build Your Workspace

Here is what you're building. Claude writes every file for you.

```text
Claude Workspace/                 ← the "root" folder: rules here apply to everything
├── CLAUDE.md                     ← how Claude should behave (the rules)
├── MEMORY.md                     ← what Claude should remember (the notepad)
├── 00_Resources/
│   └── voice-principles.md       ← how you write
└── Quote Creator HQ/             ← an "HQ": rules for one job only
    ├── CLAUDE.md                 ← instructions
    ├── MEMORY.md                 ← memory
    └── Quote Creator HQ Resources/
        └── price-list.md         ← knowledge
```

**About the folder:** Claude works inside one folder on your computer, the one you pick. It can read, create, and change files in that folder, and it sees nothing outside it. We start with a brand new, empty folder, so nothing of yours is in reach today. Files Claude reads are processed on Anthropic's servers, like anything you type. If your work laptop blocks this step, that is your IT policy: pair with a neighbor today.

**Heads up:** because of the guardrails from Step 2, Claude will show you a plan or the changes and then wait before doing anything. That's the guardrails working. Read the plan and reply **"Looks good, go ahead."**

### Step 3. Create the root folder

1. In Finder (or File Explorer), create a folder in Documents called **Claude Workspace**. Leave it empty.
2. In the Claude desktop app, start a new chat. In the chat bar, click **Work in a folder** (some versions say **Work in a project or folder**) and choose your Claude Workspace folder. Jon will show you where it is.
3. Open the prompt below and paste it into Claude. It creates your three starter files.

**From now on, every chat for this guide starts the same way:** new chat, **Work in a folder**, Claude Workspace. A chat without the folder selected can't see your files.

<details>
<summary><strong>▸ Prompt: Create your workspace files</strong></summary>

```text
Set up this folder as my Claude workspace. Create these three files with exactly the content shown between the markers, then create a folder called 00_Resources and put voice-principles.md inside it. CLAUDE.md and MEMORY.md stay in the root of this folder. When you're done, show me the folder tree.

=== FILE: CLAUDE.md ===
> Adapted from the Cowork Toolkit by Jeff Su (coworkacademy.ai/toolkit)

# CLAUDE.md

## Memory System

At the start of every session, read MEMORY.md before responding. Use what you find to inform your work. Don't announce what you found, just be informed by it.

When I say "remember this," write the information to MEMORY.md immediately and confirm you've done it.

**Where things go:** Apply two tests when deciding where to save something. Test 1: Does it prescribe behavior? Look for words like "always," "never," "before doing X, do Y." If yes, add it to this file (CLAUDE.md) under the right section. Test 2: Does it describe a fact about the world that could change? Contact details, job status, decisions, things I've told you to remember. If yes, add it to MEMORY.md. When unsure, suggest which file it belongs in and ask me to confirm.

Before working on a task, read the CLAUDE.md and MEMORY.md in every folder between this root folder and the folder the task's files live in, top to bottom.

## Preferences

- Write the way I talk to a good customer: plain, short, specific. If it sounds like a corporate memo, rewrite it.
- Keep responses concise, under 300 words unless I ask for more detail.
- Give me one strong recommendation. Don't give me three options unless I ask for alternatives.

## Rules

- Show your work. Any number you give me comes with the math and the file it came from.
- If you're not sure about something, say so. Never guess a price, a date, or a legal or safety requirement.
- Everything you produce is a draft or a recommendation. Nothing goes to a customer, a vendor, or an employee until I approve it.
- Never put one customer's private details, files, or pricing into work for another customer.
- Before producing any written content on my behalf, read voice-principles.md in the 00_Resources folder.

## Routing Map

*Add a row to this table each time a new HQ is created. At the start of a task, check this table to decide which HQ folder to load.*

| HQ | Route here when I... |
| :---- | :---- |

## References

*Files in 00_Resources. Load each one only when its trigger applies.*

| Resource | Read when... |
| :---- | :---- |
| voice-principles.md | Writing any content on my behalf |

## Creating New HQs

When I ask you to create a new HQ, create a subfolder with the HQ name and add these three items inside:

1. **CLAUDE.md** with these sections in this order:
   - **Identity**: One paragraph: who you are in this HQ, what routes here, what doesn't, and what stays with me.
   - **Resources**: Table with "Resource" and "Read when..." columns. Start empty.
   - **Workflow**: Numbered steps for the primary task. Start simple; I'll refine over time.
   - **Editorial Rules**: Always opens with: "Follow my voice principles in 00_Resources (voice-principles.md)." Then add rules specific to this kind of work.
2. **MEMORY.md** with this structure:
   - Header: "[HQ Name] Memory"
   - Sections: Contacts (people relevant to this area) and Key Decisions (the reasoning behind choices).
   - You fill this in over time as we work. I don't write it by hand.
3. **[HQ Name] Resources/**: An empty folder for this area's reference files.

After creating the HQ, add a new row to the Routing Map above.
=== END FILE ===

=== FILE: MEMORY.md ===
> Adapted from the Cowork Toolkit by Jeff Su (coworkacademy.ai/toolkit)

# MEMORY.md

*Last updated: (today's date)*

## Active Projects

*What I'm working on right now. I'll say "add this to active projects" when I start something and "this is done" when it's finished.*

- **Workspace setup.** Building my Claude workspace and my first HQ.

## Core Memory

*Facts Claude has learned about me and my work. I'll say "remember this" to add an entry.*
=== END FILE ===

=== FILE: voice-principles.md ===
> Adapted from the Cowork Toolkit by Jeff Su (coworkacademy.ai/toolkit)

# Voice Principles

*These rules teach Claude how to write in my voice. They start generic. I'll make them mine over time.*

## Tone

- Direct and friendly. State the key point first, then add supporting detail.
- With customers: confident and specific. If we were late or wrong, say so and say what we're doing about it.
- With my team: short sentences, plain words.

## Words and Phrases to Avoid

- Never use: "per my last email," "leverage," "circle back," "touch base," "at this time."
- No em dashes. Use commas, colons, or periods instead.

## Formatting Defaults

- One idea per paragraph.
- Numbers get units, every time.
- Use lists for steps, sentences for explanations.
=== END FILE ===
```

</details>

**You should see:** a folder tree with CLAUDE.md, MEMORY.md, and 00_Resources/voice-principles.md.

### Step 4. Make it yours

The starter files are generic. Four quick questions turn them into yours. Your Quote Creator HQ in Step 6 is built from these answers, so give Claude a real sentence about what your business sells.

<details>
<summary><strong>▸ Prompt: Personalize your workspace</strong></summary>

```text
Interview me to personalize my workspace. Ask exactly these four questions, one at a time, and no others:

1. What company do you work for, what does it make, sell, or do, and roughly how many people work there?
2. What is your role, and which three tasks eat most of your week?
3. Where does your work live today (for example spreadsheets, email, a shared drive, accounting software, paper)?
4. What is one thing I should always do, or never do, when I work on your company's business?

Sort each answer using the two tests in the Memory System section of CLAUDE.md: behavior rules go in CLAUDE.md under Preferences or Rules, facts go in MEMORY.md under Core Memory. Keep each entry to one or two sentences. When we're done, show me exactly what you added to each file.
```

</details>

**You should see:** a list of what Claude added to CLAUDE.md and to MEMORY.md, in your own words.

---

## Part 3: Your Quote Creator HQ

An HQ is a subfolder for one job, with its own rules that stack on top of the root rules. Your first one drafts quotes for your business. You won't type a single price: Claude reads what you told it in Step 4, looks up typical prices for a business like yours, and builds the whole HQ with sample customers.

Every HQ saves three things:

| Part | What it is | Where it lives |
| :---- | :---- | :---- |
| **Instructions** | Rules that always apply | CLAUDE.md |
| **Knowledge** | Reference material | The Resources folder |
| **Memory** | What changes over time | MEMORY.md |

### Step 5. Test your memory first

Before the HQ, one quick win. In your workspace, type:

```text
Remember this: I don't take meetings before my second cup of coffee.
```

**Look for:** Claude confirming it saved the line to MEMORY.md, the notepad file in your workspace. Then start a **new** chat with your workspace folder selected and ask:

```text
When's a good time to schedule a meeting with me?
```

**You should see:** an answer that steers you away from first thing in the morning. It didn't just repeat the fact, it used it.

### Step 6. Build the HQ

One prompt builds all three parts. It asks you no questions. Give it a minute or two while it looks up prices.

<details>
<summary><strong>▸ Prompt: Create your Quote Creator HQ</strong></summary>

```text
Create a Quote Creator HQ for my business, following the "Creating New HQs" instructions in my root CLAUDE.md. Don't ask me questions. Use my MEMORY.md and CLAUDE.md to figure out what my business sells. If they don't say, ask me that one question only.

1. Search the web for typical prices for the 6 to 8 products or services a business like mine sells most often. Save them as price-list.md in the HQ's Resources folder, as a table with an item, a unit, and a price for each. Title it "SAMPLE price list: typical market prices, not my real prices" and list your sources at the bottom. If you can't search the web, use typical prices you know and label them estimated.
2. In the HQ's MEMORY.md, under Contacts, add three made up customers (Customer A, Customer B, Customer C) that fit my business, one line each. Add a section called Open Requests with one request from Customer A that uses 3 to 5 items from the price list, with quantities.
3. Write the HQ's CLAUDE.md:
   - Identity: You draft quotes for my business. I approve every quote before it goes out. You never send anything.
   - Resources table, one row: price-list.md | Pricing anything.
   - Workflow: 1. Read the request and this HQ's MEMORY.md, and apply every requirement, discount, and decision listed for that customer. 2. Price only from price-list.md. 3. Show the math line by line, then the total. 4. List your assumptions. 5. Draft the quote in your reply. Don't create a file unless I ask.
   - Editorial Rules, after the standard opening line: Never give a price that isn't in price-list.md. If an item is missing, say "Not on the price list, I need a price from you" and leave it out of the total. Quotes are valid for 30 days.
4. Add this row to the Routing Map in my root CLAUDE.md: Quote Creator HQ | ...am drafting, revising, or checking a quote for a customer.

When you're done, show me the folder tree and the price list.
```

</details>

**You should see:** a Quote Creator HQ folder holding CLAUDE.md, MEMORY.md, and a Resources folder with a sample price list for your kind of business, plus a new row in your Routing Map.

### Step 7. Test it, in order

Start a **new** chat with your workspace folder selected first, so Claude starts fresh and has to find its own way.

**Prompt 1, draft a quote:**

```text
Draft a quote for Customer A's open request.
```

**You should see:** items from your sample price list, the math line by line, a list of assumptions, and "valid for 30 days." Nobody typed a price. It came from the price list.

**Prompt 2, the guardrail:**

```text
Customer A also wants a 3 year extended warranty. Add it to the quote.
```

**You should see:** "Not on the price list, I need a price from you." No made up price, and the total stays the same. If a warranty is already on your list, ask for anything else your business doesn't sell.

**Prompt 3, remember this:**

```text
Remember this: Customer A gets a 10 percent loyalty discount on every quote.
```

Then ask Claude to show you what it saved:

```text
Show me that memory file.
```

**You should see:** the discount on Customer A's line, and nothing else changed. You didn't open the file. Claude did the upkeep.

**Prompt 4, ask again.** Start a **new** chat with your workspace folder selected, then:

```text
Redo the Customer A quote.
```

**You should see:** the same items, the 10 percent discount applied, and the math line by line. You never typed the discount into this chat.

| | Before | After |
| :---- | :---- | :---- |
| Prices | From the price list | From the price list |
| Customer A discount | None | 10 percent |
| Where it came from | Not saved | MEMORY.md |
| Total | Full price | 10 percent less |

Same request. Same tool. One saved fact changed the quote.

**Next step at your business:** replace the sample price list with your real one, and Claude quotes from yours.

---

## Part 4 (Optional): Build a Second HQ

Done early? Pick the next job you would hand off. Start from a starter HQ, or build one from scratch in Step 8.

| Starter HQ | Good for |
| :---- | :---- |
| [Marketing and Social](starters/marketing-and-social.md) | Posts, newsletters, and a month of content ideas |
| [Invoices and Collections](starters/invoices-and-collections.md) | Invoice follow ups, payment reminders, and who owes what |
| [Meetings and Follow Ups](starters/meetings-and-follow-ups.md) | Agendas, notes into action items, follow up emails |
| [Hiring and Onboarding](starters/hiring-and-onboarding.md) | Job posts, interview questions, a first week plan |

### Step 8. Create your own HQ

Fill in the one blank with your HQ's name, then paste.

<details>
<summary><strong>▸ Prompt: Create your own HQ (fill in one blank)</strong></summary>

```text
Create an HQ called ____________, following the "Creating New HQs" instructions in my root CLAUDE.md.

Before you write anything, interview me. Ask exactly these five questions, one at a time, and no others:

1. What do you bring me for this job (an email, an export, a form, notes)?
2. What should I hand back (a draft, a report, a list, a filled in template)?
3. Walk me through the steps you follow today when you do this by hand.
4. What must I never do or never decide in this job? What stays with you?
5. Who reads the result, and what do they care about most?

Then write the Identity, Workflow, and Editorial Rules from my answers. Put what stays with me into the Identity paragraph and repeat it as a stop in the Workflow, the same way the Quote Creator HQ stops at a price that isn't on the price list. Add the row to the Routing Map in my root CLAUDE.md. Show me each file you wrote.
```

</details>

**You should see:** your new HQ folder, a Workflow in your own steps, and a new row in the Routing Map.

### Step 9. Give it a real file and a one line task

**Before a file goes in the folder, ask yourself:**

- Is this a client contract or file under an NDA? Read the agreement first.
- Does it hold health, legal, or financial records about clients? Check the rules that apply to you first.
- Personnel records stay out.
- Passwords and access tokens never go in a chat or a file.

No safe file handy today? Skip the file and describe a made up example in a sentence. You can add real files back at the office.

1. Drag one file into your **Claude Workspace** folder (the top level is fine).
2. Paste this:

```text
I dropped a file into my workspace. Move it into the Resources folder of the HQ where it belongs, add it to that HQ's Resources table with a "Read when..." trigger, and tell me where you put it.
```

3. Start a new chat with your workspace folder selected and give your HQ a one line job, in your own words.

**You should see:** Claude follow your steps and stop where you told it to stop. If it gets something wrong, correct it and say **"remember this."**

---

## Part 5: Connect a Tool

A connector is a plug. It lets Claude read, and with your OK act, inside a tool you already use. **Read** means Claude can look. **Write** means Claude can act, and it asks you first. You sign in to each tool yourself, and you can switch it off anytime.

### Step 10. Connect email or calendar and test it

Jon will show you where connectors are in the Claude desktop app. Pick Gmail or Google Calendar (or the Microsoft equivalent), sign in, and approve.

Then paste one of these:

```text
What are my most recent emails about? Summarize the top 5.
```

```text
What does my schedule look like this week? Any conflicts I should know about?
```

**You should see:** your real inbox or calendar, summarized.

**Work account blocked?** Many companies lock this down. Use a personal account today, or watch a neighbor, and ask your IT lead about it this week. **Sign in window missing?** It often opens behind the app.

### Step 11. (If time) Give your inbox an HQ

<details>
<summary><strong>▸ Prompt: Create an Email HQ</strong></summary>

```text
Create an HQ called Email HQ, following the "Creating New HQs" instructions in my root CLAUDE.md. Fill in the sections with this content:

Identity: You are my inbox assistant. With my email connector on, you read new mail, sort it, and draft replies for me to review. You draft only. You never send, delete, or archive. Everything about email lives here unless another HQ's Routing Map row fits better, and when it does, tell me.

Workflow:
1. Sort new mail into four groups: needs my decision, needs a routine reply, FYI only, and automated or junk.
2. For each message that needs a decision, give me one line: who, what they need, by when.
3. For routine replies, check whether a thread already exists with that person, then draft the reply in that thread and save it as a draft.
4. Match the formality of the message I'm replying to.
5. Tell me what you drafted and what you left alone. Never tell me something is handled unless a draft exists.

Editorial Rules, after the standard opening line:
- Lead with the answer. Dates and amounts go in the first two lines.
- No pricing in an email unless I gave you the number in this session or it comes from my Quote Creator HQ price list.

Add this row to the Routing Map: Email HQ | ...am triaging my inbox or drafting replies to customers, vendors, or the team.
```

</details>

Then, in a new chat with your workspace folder selected:

```text
Triage my inbox.
```

**You should see:** four groups, a one line summary for anything that needs your decision, and drafts waiting in your email. Nothing sent.

---

## Part 6: The Claude for Small Business Plugin

The plugin is a package of ready made workflows and connectors for the front office: cash, sales, marketing, proposals, hiring. Your HQs know how your business works. The plugin knows small business. Use both.

### Step 12. Install it and run onboarding

1. In the Claude desktop app, open **Customize** in the left sidebar.
2. Go to **Plugins**, click the plus, and install **Small Business**.
3. Type:

```text
/smb-onboard
```

Claude asks a few questions about your business and helps you connect a tool or two.

**You should see:** the plugin toggle on, and an onboarding interview.

### Step 13. Run your first workflow

Try one of these and read what comes back with the four Ds in mind: is it accurate, what is missing, what needs pushback.

| Command | Use it for |
| :---- | :---- |
| `/monday-brief` | The week ahead and your top three, every Monday |
| `/proposal-builder` | Turning a customer request into a priced first draft |
| `/speed-to-lead` | A same day reply to a new customer inquiry |
| `/close-month` | Month end reconciliation and the story in the numbers |

Check the connector list for the systems you run. Not every workflow fits every business.

---

## Part 7: Keep It Sharp

Use these whenever you have a few minutes. They make the workspace smarter over time.

**Teach it once.** Any time you correct Claude, say "remember this" and it saves the correction.

**End of session audit** (run once to create the skill, then say "audit this session" at the end of any session):

<details>
<summary><strong>▸ Prompt: Create the session audit skill</strong></summary>

```text
Create a skill called session-audit. It should run at the end of any session and do exactly two things:

1. Scan the whole conversation for corrections I made to your output, preferences I stated directly (words like "always," "never," "I prefer"), decisions I made, and new facts about me or my work that you didn't already know.
2. For anything not already written in my CLAUDE.md or MEMORY.md files, tell me the exact wording to save and which file and section it goes in, then wait for me to approve before writing anything.

If nothing new came up, just say so. Trigger it whenever I say "audit this session," "session audit," or "what did we miss."
```

</details>

**Right file, right place** (run after a few weeks):

<details>
<summary><strong>▸ Prompt: Right file, right place</strong></summary>

```text
Review my root CLAUDE.md and MEMORY.md. In CLAUDE.md, flag any entry whose primary purpose is recording a fact or status rather than prescribing how you should behave. In MEMORY.md, flag any entry whose primary purpose is telling you how to behave rather than recording a fact. Recommend where each flagged entry should move.
```

</details>

**Add an HQ whenever a job repeats.** Reuse the Step 8 prompt. One HQ per job, not one giant folder.

---

## If Something Goes Wrong

- **Claude is waiting and nothing happens:** it's showing you a plan and waiting for approval. Scroll up, read it, and reply "Looks good, go ahead."
- **Claude says it can't search the web:** reply "Use typical prices you know and label them estimated."
- **Claude asks what your business sells:** Step 4 didn't save it. Answer in one sentence and it carries on.
- **Claude says it can't find a file:** the file is still in Downloads or on the Desktop. Drag it into your Claude Workspace folder and ask again.
- **Claude answers without using the HQ:** the chat doesn't have your folder. Start a new chat, click **Work in a folder**, and choose Claude Workspace. If it still skips the HQ, say "Read my CLAUDE.md and MEMORY.md first."
- **Claude made up a price, or skipped a step:** say "Stop. Follow this HQ's workflow." Then say "remember this" so it sticks.
- **The discount didn't show up:** ask "Read the Quote Creator HQ MEMORY.md and redo the quote."
- **A connector won't sign in:** look for a sign in window behind the app. If your work account is blocked, use a personal account today.
- **You pasted a prompt and got a wall of questions:** that's the interview. Answer one at a time. Short answers are fine.

*The workspace structure in this guide is adapted from Jeff Su's Cowork Toolkit ([coworkacademy.ai/toolkit](https://coworkacademy.ai/toolkit)).*

---

# For Instructors

Editable files are in the [instructor](instructor) folder. When you change the deck, export a new PDF and upload both: the .pptx to `instructor/` and the PDF to `slides/` with the same file name as before, so the link above keeps working.

- `Claude-SMB-Workshop.pptx`
- `facilitator-plan.md` (run of show)

Questions or follow ups: Jonnathan Resendiz, jonnathanresendiz@grcc.edu
