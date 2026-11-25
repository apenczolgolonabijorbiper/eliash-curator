# Eliash-curator: first concept

**Eliash-curator gathers information and guides Golem14’s cognitive work in Chelm.**

Status: **first concept, open to revision**. Written 25 November 2026.
This describes the intended role and direction. It does not describe an implemented product or commit to a backend, interface or deployment model.

## The idea

An application should be able to express what it wants Golem to investigate without rebuilding the collection and preparation work for every source.

Eliash is the reusable curator between that intention and the work carried out around Golem. It helps gather relevant material, preserve its origin, prepare it for processing and turn the application's goals into bounded cognitive activities. It also helps carry a study forward when new questions, missing evidence or corrections arise.

The name carries the project's creator-and-guide metaphor. In the software, “guiding” means directing work within the application's chosen scope and authority. It does not mean overriding the user's decisions, changing the Harness's rules or becoming the owner of Golem's canonical memory.

The desired result is a family of applications that can share useful collection and curation methods while keeping their own purpose, domain and user experience.

## A curator with two connected responsibilities

### Gather and curate information

Eliash should help answer:

- What information is being requested, and from which sources?
- What can the current environment actually access?
- Which material falls within the requested scope?
- What was captured, when, from where and with what limitations?
- What is new, changed, repeated, unavailable or only partly inspected?
- What needs to reach Chelm for further processing?

Curation includes selecting, organizing and preparing material while keeping its original meaning and provenance available. It should make omissions and transformations visible. A summary or excerpt may be useful, but must not silently replace the original evidence or pretend to be a complete inspection.

Eliash should not discard disagreement merely to produce a tidy collection. Repeated material is not independent corroboration. An inaccessible source is not an empty source, and an unsuccessful search is not proof that something does not exist.

### Guide cognitive work

Eliash should help translate application goals into activities such as:

- Investigate a subject within a defined scope.
- Analyze newly gathered material.
- Compare competing explanations.
- Verify a statement or challenge a finding.
- Deepen a selected question.
- Revisit an answer after evidence changes.
- Ask the user for a missing choice or clarification.
- Stop when the requested work is complete or the agreed bounds are reached.

It can coordinate these activities and report what is ready or blocked. The cognizer performs interpretation and reasoning according to the Harness; Chelm controls work and publication.

A question raised during cognition can become a proposed collection or follow-up activity. The application supplies the applicable permission. Eliash may then obtain the material and request the next appropriate cognitive step. An interesting question does not by itself authorize more access, spending or external action.

## What an application describes

The application gives Eliash a collection and investigation brief. Initially this can be expressed in ordinary language; a fixed machine-readable format is deliberately not chosen yet.

| Part of the brief | Example |
| --- | --- |
| Purpose | Understand how a subject has changed and which conclusions remain uncertain |
| Sources | Selected web pages, user-provided material, a repository or a work-tracking system |
| Scope | A topic, project, time range, revision range or chosen set of records |
| Treatment | Preserve original quotations, include conflicting accounts and identify incomplete material |
| Intended work | Explain, compare, verify, organize or deepen |
| Bounds | Available time, source volume, permitted access and stopping conditions |
| Interaction | Which decisions need a user response and which existing policies already authorize work |

These are conceptual concerns, not a proposed API. Domain meaning stays with the application and its reviewed guidance. Research Notebook can describe research sources and studies; another application might describe commits and work items.

## How a typical activity feels

A user asks Research Notebook to investigate a topic and gives a few starting points.

Eliash helps scope the activity, gathers available material and records what was actually obtained. It prepares that material for Chelm and requests analysis through the established host/Harness workflow. A cognizer reasons over the available evidence. The application presents the resulting findings, questions and limitations.

The user may then select “deepen this point,” “check this claim” or “add this source.” Eliash coordinates the next bounded activity, preserving the earlier material and results so that a changed answer can be explained.

At each stage, the application should be able to distinguish material that has merely been collected, material accepted for processing, completed cognitive work and a result that has actually been saved. The exact presentation and mechanics will be learned from real usage.

## Place in the Golem family

| Component | Main responsibility |
| --- | --- |
| Application, such as Research Notebook | Defines purpose, domain guidance, user interaction and authority |
| Eliash-curator | Gathers and prepares information; coordinates authorized collection and cognitive activities |
| Chelm-host | Owns durable runtime state, intake, work coordination and controlled publication |
| Golem14-harness | Defines cognitive procedures, evidence and memory meaning, retrieval and validation rules |
| Shem or another compatible cognizer | Performs the actual cognitive work using available models, agents and tools |

Eliash is optional. A small application can still submit material or request cognitive work directly through Chelm. An existing agent can still act as the cognizer without Shem.

Eliash primarily sits on the application-to-host collection and coordination path. It need not become a proxy for every query, screen or read of a result.

Chelm remains the integration boundary for accepted information and cognitive work. Eliash does not maintain a competing canonical knowledge store. Any collection notes, preparation records or progress state serve its own operational role and must not be confused with accepted Golem memory.

If curation itself needs semantic judgment, it can request bounded cognitive assistance through the same established path. Whether that is useful, and how its output remains distinguishable from original source material, is a learning question rather than an assumed implementation.

## Methods and interfaces should emerge from use

Eliash may eventually collect through web browsing, explicit URLs, pasted material, files, document readers, repository access, Git history, TFS/Azure DevOps APIs and other application-relevant sources.

It may also use different ways to perform the same activity: a tool already available to an agent, a dedicated connector, a local routine, a remote interface or an explicit user-assisted handoff. The available route must be stated honestly; unavailable access should lead to a clear blocked or alternative path.

These are directions to explore, not a committed connector catalogue. A Git repository being studied is a source of evidence, distinct from Git used by a host to retain memory history.

Likewise, Eliash may later be used as embedded reusable routines, through an application interface, by an agent or as a separate service. There is no commitment here to a programming language, framework, database, MCP interface, communication bus, mandatory server or always-on process. Technology and interface choices should follow demonstrated needs.

## Develop the concept through Research Notebook

[Research Notebook](https://github.com/apenczolgolonabijorbiper/research-notebook) is the first application from which Eliash should learn. As reviewed for this concept, its default branch contains an introductory README and its detailed direction is still in [planning PR #14](https://github.com/apenczolgolonabijorbiper/research-notebook/pull/14) and [tracker #1](https://github.com/apenczolgolonabijorbiper/research-notebook/issues/1). The scenarios below are intended opportunities for learning, not claims that those capabilities are already implemented.

Research Notebook should be implemented and enhanced for its own useful outcomes. It should not have to wait for a complete Eliash platform, and this concept does not alter its implementation or approval status.

The intended learning path is:

1. Implement a concrete collection, preparation or study-direction need in Research Notebook.
2. Observe how it behaves with real available tools, source material and user interaction, including failures and interruptions.
3. Record which parts are notebook-specific and which appear reusable.
4. Describe the reusable behavior in plain language, including its limits and the evidence for it.
5. Move or adapt that behavior into Eliash when doing so makes the notebook simpler and preserves its working behavior.
6. Use the shared behavior back in the notebook and check it against another meaningful source or application scenario.
7. Let those observations shape the technical contracts, methods, interfaces and routines.

The application is an implementation and learning source, not a runtime dependency that every future Eliash user must install. Eliash should grow into a reusable capability, not a renamed copy of the notebook's study model, screens or storage choices.

## Early learning opportunities

| Notebook experience | What Eliash might learn |
| --- | --- |
| Topic discovery, a supplied URL and pasted evidence | Which collection entry points share useful behavior |
| Partly accessible or changing sources | How to express capture limits, revisions and provenance |
| Organizing a study into topics | Which preparation belongs to reusable curation and which belongs to notebook presentation |
| Deepen, compare, challenge and verify | Which direction-of-work patterns recur across applications |
| Missing evidence or unanswered questions | How to propose and coordinate bounded follow-up without assuming permission |
| Later-session continuation | What must be retained to resume work honestly |
| Changed evidence and corrected findings | How to preserve prior results and explain why the study changed |
| A second source family, such as Git or TFS | Whether the emerging abstractions extend beyond web research |

The [learning agenda](LEARNING_AGENDA.md) gives a lightweight way to record these observations. It is not an implementation checklist or a predetermined backend plan.

## Signs that the concept is working

An application can describe a useful activity without reimplementing every source connection. A user can understand what was gathered, why it was included, what was omitted and which original material supports a result.

The same routine proves useful in more than one meaningful situation. Moving it into Eliash reduces repeated application work while preserving provenance, finite scope and the host/Harness boundary.

A blocked or interrupted activity remains understandable. Earlier evidence and answers remain available. The system does not present an attempted fetch as accepted intake, or a generated result as saved work without the appropriate confirmation.

Most importantly, reuse should grow out of demonstrated behavior rather than a large framework designed before the notebook has taught us what it needs.

## Questions deliberately left open

- How much source selection can be expressed through deterministic application rules, and when is cognitive assistance worthwhile?
- What is the smallest useful brief that works across research and software-development sources?
- Which routines belong in Eliash, and which should remain application-specific?
- Which parts need durable operational state, and which can simply use the host's existing facilities?
- What does an application need to see to understand progress, omissions and stopping conditions?
- Which interfaces are needed by actual execution environments, rather than merely conceivable?
- How should independently useful collection methods be introduced and maintained without forcing a large installation?
- When is there enough observed common behavior to define the first technical contract?

These questions should be answered incrementally through Research Notebook and subsequent applications. This first concept keeps that room for learning.

## Related projects and reviewed starting points

- [Research Notebook](https://github.com/apenczolgolonabijorbiper/research-notebook), especially [source/provenance #5](https://github.com/apenczolgolonabijorbiper/research-notebook/issues/5), [collection/intake #6](https://github.com/apenczolgolonabijorbiper/research-notebook/issues/6) and [study cycles #7](https://github.com/apenczolgolonabijorbiper/research-notebook/issues/7).
- [Research Notebook planning PR #14](https://github.com/apenczolgolonabijorbiper/research-notebook/pull/14), reviewed at head `b523fa5671543a15caf79647eb39950945c7c4e9`. Its evolving implementation should supply new evidence rather than freeze this concept to the proposal.
- [Chelm-host](https://github.com/apenczolgolonabijorbiper/chelm-host).
- [Golem14-harness](https://github.com/apenczolgolonabijorbiper/golem14-harness).
- [Shem-cognizer](https://github.com/apenczolgolonabijorbiper/shem-cognizer).

This concept creates no runnable connector, background process, host capability, deployment or implementation commitment. It is a starting point for discussion and evidence-led development.
