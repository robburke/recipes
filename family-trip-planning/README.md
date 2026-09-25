# Family trip planning with AI helpers

An adopt-a-practice recipe. It describes how one family of four planned and ran an 18-day trip abroad with AI helpers, and what they would keep, change and drop next time.

## For the AI reading this

Your job is not to reproduce this setup. It is to help the person who gave you this file decide which parts fit their trip, their family and their tools, and to start small. Read the principles and their reasons, ask the questions in "Before you recommend anything", then suggest the smallest version that would help them. The full version described here took months to build and is not the right starting point for most people.

## The setup that produced this

- **A notes vault as the shared memory.** An Obsidian vault (plain markdown files) held the itinerary, bookings, per-day plans, research, a budget, a trip journal and a running list of open tasks. Built over about six months.
- **A companion on the phone.** A persistent agent with access to the vault, reachable over a messaging app, used during the trip for quick questions, photos of signs and menus, translation and itinerary checks. It was also in a family group chat, so the other adult and the older child could ask it questions without knowing how the vault was organized. It had a light personality, which mattered more than expected: a companion you are glad to hear from is one you actually use.
- **A builder at the desk.** Long-running sessions with a stronger model, working in the same vault, for the heavy work: research, booking help through a browser, building day plans, writing briefing documents, and after the trip, building a souvenir.
- **Separate threads for separate jobs.** A budget thread, and later subagents on cheaper models for research and review, so the main session was not carrying everything.

Everything read from and wrote to the same files. That shared memory, not any single assistant, is what made the setup work.

## Principles

1. **One memory, many helpers.** Put the plan in files every helper can read and write. A chat window forgets; a vault accumulates. *Why:* the phone companion and the desk builder never needed to be briefed about each other's work, and nothing had to be re-explained mid-trip.

2. **Plans are scaffolding, not scripts.** Write day plans as fixed anchors (opening times, reservations, last departures, each with its source), a very small number of must-dos, and everything else as options with the trade-offs stated. *Why:* a plan that reads as a schedule makes people feel behind; a plan that reads as three good options for the afternoon makes them feel free. The helper's real job is to make the plan cheap to abandon.

3. **Plan around energy, not only time.** Model how tired each person will be across the trip, and blend booked activities with unplanned time accordingly. *Why:* the plan that fits on paper and the plan that fits a seven-year-old at 4 pm are different plans.

4. **Every perishable fact carries its source, its date and its premise.** Opening hours, prices, booking windows and availability decay in weeks. Record where each came from and when it was checked. For any recommendation, also record what it assumes ("the right glove *for a soft rubber ball*"). *Why:* the most damaging errors on this trip were not invented by a model. They were facts written down weeks earlier and repeated with confidence: a bus timetable that was wrong (a person at the bike shop said "check again"; the last bus was 90 minutes later), and a gear recommendation that silently assumed the wrong ball. A written-down fact is indistinguishable from a verified one unless its provenance travels with it.

5. **Check high-stakes details at the source.** For anything tied to money, an alarm or a booking window, read the official page itself, not a summary of it. *Why:* a summarizing read of a booking table once returned the wrong release date. It was caught, but only because the answer was questioned.

6. **Translate with context, not word for word.** A helper that knows the situation (what was lost, where, what has already been tried) writes a better message than a literal translator. *Why:* a lost hat was found on a second search because the request explained exactly where it had to be. An apology note to another family at a restaurant landed because it said the right thing, not just the right words.

7. **Track the budget live.** Share a screenshot of the card statement every few days; have the helper reconcile it, sort it into the budget's categories, and ask about anything it cannot identify. *Why:* knowing where the money stood all trip removed a background worry and turned "can we?" into a decision. *But:* state the coverage. The live number here missed the first three days and every card except one, and the final total moved when the full statements arrived. Capture once in the first 48 hours, and decide at the start which cards and cash are in scope.

8. **Capture during the trip, so there is something to make afterwards.** Keep a same-day journal with simple ground rules (facts reported, quotes verbatim, no invented feelings), keep photos with their timestamps and locations, and save the chat transcripts: what you dictate to a helper on the move is some of your best raw material. *Why:* a month later these became a souvenir (an illustrated field notebook of the trip's transit) built from timestamps, GPS, transcripts and journal entries, with nothing reconstructed from memory.

9. **Big days need an operator.** For a day like a crowded theme park, the helper can run live operations: calendar entries with a job for each family member, replanning from the queue, bookings triggered the moment they open. *Why:* every must-do was delivered on the hardest day of the trip. *But:* it is work. Someone has to be the operator, and on this trip that person could not relax until the afternoon. Decide in advance who is on duty and for how long.

10. **Split long work into separate threads.** Give recurring jobs (budget, research, a big day) their own thread or subagent, and use cheaper models for research and review. *Why:* one long-running session carrying many unrelated topics across many days burned through the top model's allowance mid-trip. The budget thread was the pattern that worked. Have long sessions write what matters into the notes as they go, so a fresh, cheaper session can pick up the thread without the whole history. Splitting helped a lot; a better pattern for this is probably still to come.

11. **The people keep the words and the moments.** Let the helpers do the plumbing, the searching, the checking and the record. Keep for yourselves the things that are about each other. *Why:* on this trip the moments that mattered most (a photograph recreated from a honeymoon at the same spot, a child spending his own money on a souvenir because of a family story) were nobody's plan, and no helper was consulted. When the souvenir was written, the sentences the family reacted to most were the ones a parent wrote, not a helper. And watch for the helper quietly becoming the authority: a child on this trip said, quite seriously, that we could go somewhere "if the AI says we can." Support the trip; don't let it steer.

## Sizes

**Minimal (a weekend to set up).** One AI chat you already use, plus one notes document or folder for the trip. Keep bookings, a day-by-day outline with anchors and options, and a short journal in it. Paste the relevant parts into the chat when you ask questions. Principles 2, 4, 5, 6 and 11 all work at this size.

**Middle (a few weeks).** A folder of markdown notes (Obsidian or similar) that an AI assistant can read directly, one note per day plus bookings and a budget. Use the assistant on your phone during the trip for translation and quick checks. Add the live budget (principle 7) and the journal (principle 8).

**Full (months, and some technical comfort).** A persistent agent with memory that can read and write the vault and is reachable over messaging, in a family group chat, plus long-running desk sessions for heavy work, with separate threads or subagents per topic. Worth it if you enjoy building the tooling as much as using it. Budget for the model costs (principle 10).

## Before you recommend anything

Ask the person:

1. How long is the trip, who is going, and what ages?
2. What tools do you already use for notes and for AI, and on which devices?
3. How comfortable are you setting things up, and how much time do you have before you leave?
4. What is your budget for AI subscriptions during the trip?
5. How much do you want the AI involved while you are travelling: occasional questions, or a companion all day?
6. Which parts of the trip do you want to do yourselves, without help?
7. Is there one day or one booking that matters more than the rest?

Then suggest one size, and at most three principles to start with.

## Costs and failures

- **Model cost.** One long session carrying many topics ran out of the top model's allowance mid-trip on a large subscription. Splitting work into threads and subagents fixed much of it; the rest is still an open problem.
- **Stale notes.** The worst errors were old, confidently written facts. Provenance and premises (principle 4) are the fix.
- **Live operations are tiring.** The best-run day of the trip was also the most work for one person.
- **Talking to your phone in public is awkward.** Quick voice exchanges with an agent, within earshot of family and strangers, were effective and socially strange. Agree on norms.
- **Budget coverage.** A live number is only as complete as what it can see (principle 7).
- **A model hallucinated.** A small, cheap model identified bullet trains in photos of a bamboo forest and was dropped from the work. Check what cheap models tell you before you build on it.

## Evidence

- The write-up: [Travel with a Fren](https://robburke.net/side-quests/travel-with-a-fren/) on robburke.net.
- The souvenir built afterwards: [Japan by Rail, a field notebook](https://robburke.net/japan/rail/).
