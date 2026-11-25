# Learning agenda for Eliash-curator

Status: initial questions and recording guide, not a technical specification.
Related: [first concept](CONCEPT.md).

Eliash should learn from how [Research Notebook](https://github.com/apenczolgolonabijorbiper/research-notebook) is implemented and used. The purpose of these notes is to preserve useful experience before turning it into shared machinery.

## What to observe

| Area | Questions worth recording |
| --- | --- |
| Starting an activity | What did the user/app request? Which missing choice actually mattered? |
| Finding and obtaining material | Which methods were available? What worked, failed or needed user assistance? |
| Preparing evidence | What could be reused? Which transformations lost context or made provenance harder to inspect? |
| Directing cognitive work | What distinguished explain, compare, verify, challenge and deepen in practice? |
| Continuing a study | Which questions or gaps led to useful follow-up? What stopped unnecessary expansion? |
| Changes and corrections | How did new source material affect an earlier result? Could the user understand why? |
| Progress and interruption | What did the app need to distinguish collected, accepted, processed and saved work? |
| Reuse | Is this behavior specific to one screen/source, or useful in another meaningful situation? |
| Interface needs | Which environment actually needed a function, command, agent tool, user-assisted step or remote operation? |
| Cost of sharing | Would extracting this behavior simplify the notebook, or introduce more configuration and coupling than it removes? |

For the currently proposed notebook, web discovery, explicit URLs, pasted material, evidence inspection and finite study deepening are the natural starting points. Git/TFS and other source families are later opportunities to challenge the abstraction, not assumed first-release deliverables.

## A lightweight observation note

Use a short note or issue when there is an actual experience to preserve. Do not fill unknowns with plausible details.

**Situation**  
What the user was trying to accomplish, and the relevant application/source context.

**What happened**  
What was actually done and observed. Link the notebook issue/change and permitted evidence. Separate an implemented method from a proposed one and a tested interface from an assumed one.

**What helped or caused trouble**  
Include failures, missing capabilities, provenance gaps, misleading progress or unnecessary work.

**Application-specific part**  
What belongs to the notebook's subject model, study presentation, policies or user experience.

**Possible reusable behavior**  
Describe it in plain language before proposing code, framework or interface.

**Counterexample or second use**  
Where might the idea fail? Which different source or workflow could test whether it generalizes?

**Next decision**  
Keep it in the app, observe further, revise an earlier idea, or propose a small shared capability. Record the reason and any remaining uncertainty.

Use synthetic/redacted examples where needed. Do not place credentials, private captures or a user's notebook history in a public repository.

## When a learning is ready to become shared behavior

There should be a real application need and an observed implementation to learn from. Its useful outcome and limitations should be explainable without reference to one screen or storage layout.

The proposed extraction should preserve existing behavior and clarify ownership. It should consume host/Harness contracts rather than recreate them. A second meaningful situation should challenge its assumptions; this can be another notebook workflow or source family rather than a new full application.

An attractive interface alone is not evidence that the abstraction is useful. Equally, a useful small routine does not need to wait for a complete framework.

## Possible progression

1. **Observed in the notebook:** keep a concrete working behavior and record its limits.
2. **Candidate for reuse:** separate general concerns from notebook-specific choices.
3. **Shared concept:** agree a small behavior and a suitable way to access it.
4. **Shared routine or method:** implement it in Eliash and use it back in the notebook.
5. **Broader confirmation:** exercise another meaningful workflow/source, then refine the emerging interface.

This is a learning path, not a mandatory release ceremony or a substitute for verifying working behavior. No technology, architecture or date is selected by these stages.

## How the concept should evolve

When observations justify a change, update the concept and link the reason. Keep a brief record of decisions that explain the current direction. Avoid silently promoting a speculation into a supported capability.

Technical specifications, compatibility commitments and implementation backlogs can follow once there is enough concrete behavior to describe. Any later specifications must evolve with their implementing routines rather than becoming a separate, stale description.

Research Notebook remains free to solve its immediate needs while these abstractions emerge. Work in this repository should not imply that notebook planning has been approved, implemented or released.
