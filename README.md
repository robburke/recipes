# recipes

Portable, model-agnostic specs for getting a custom result out of an AI.

A recipe is a written-down version of what "good" looks like to me, for a particular task, in enough detail that any capable model can follow it. It isn't a prompt (those are model-specific and disposable) and it isn't a fine-tune (that's locked to one model). A recipe is the durable part: my taste and process, inspectable and portable, so it outlives whatever model I hand it to.

My theory: as models get good and interchangeable, the thing worth owning isn't the model or the prompt, it's the "recipe."

They also seem to work as a way to *share* a custom capability with another person: hand them the recipe rather than the full code, and let their agent take it from there.

To hand one to your AI, give it the raw file rather than the GitHub page, for example `https://raw.githubusercontent.com/robburke/recipes/master/family-trip-planning/README.md`.

## Two kinds of recipe

- **Reproduce a result.** The recipe carries taste and process closely enough that another model can make the same kind of thing. Tom is this kind.
- **Adopt a practice.** The recipe describes something that worked for me, with the reasons, so your AI can help you work out what fits your situation. Hand it over with something like "here's the idea, how could we use or adapt this?" The trip-planning recipe is this kind.

## What a recipe includes

- **A note to the AI reading it.** What the file is, and what its job is: follow it, or help its person adapt it.
- **Principles, each with its reason.** The reasons are what let a model judge which parts transfer to someone else.
- **The practice itself,** concrete enough to act on.
- **For practices: sizes and questions.** A minimal, a middle and a full version, and the questions to ask the person before recommending one. Most people should start small.
- **Costs and failures, plainly.** What went wrong and what it cost. These keep a model from recommending more than someone needs.
- **A link to the evidence.** The side quest where it was used, so the claims can be checked.
- **Nothing private, nothing tied to one model.** No names, no accounts, no model-specific tricks.

## Related work

Other people have arrived at similar ideas from different directions. A few worth knowing:

- [Agent Skills](https://agentskills.io/home): a folder with a `SKILL.md` that an agent loads when a task calls for it. An open standard since December 2025, supported across many agent tools. Written for an agent to execute.
- [AGENTS.md](https://agents.md/): a plain markdown "README for agents" that tells coding agents how to work in one repository.
- [Fabric patterns](https://github.com/danielmiessler/fabric/tree/main/data/patterns): a large library of reusable markdown prompts, one per task.
- [goose recipes](https://goose-docs.ai/docs/guides/recipes/storing-recipes/): the same word for a different thing, YAML configuration that runs a workflow inside the goose agent.

A recipe here sits closer to a written-down practice than to any of these: plain markdown, meant to be read by someone's AI and applied to that person's situation.

## Recipes

- **tom/**: coming soon. The editing taste and the cull-and-develop process behind [Tom](https://robburke.net/side-quests/brand-new-renaissance/), my swim-meet photography partner.
- **[family-trip-planning/](family-trip-planning/)**: how a family of four ran an 18-day trip abroad with AI helpers sharing one notes vault, from months of planning to a souvenir built afterwards. An adopt-a-practice recipe.

More to come.

---

Written up over at [robburke.net/side-quests](https://robburke.net/side-quests/).
