---
title: "Building trust in bioinformatics: reflections from SBEI 2026"
author: Anna Quaglieri
date: '2026-11-20'
slug: []
categories: []
tags: [sbei, bioinformatics]
---

On 16 November, I attended the Symposium on Bioinformatics Empowering Industry in Melbourne (SBEI 2026), organised by the  ABACBS Professional Bioinformatics Community. It was my first SBEI and the first conference dedicated entirely to bioinformatics that I’d attended in several years. I loved reconnecting with peers from around Australia, including some I’d met during my master’s and PhD.

The program covered population-scale genomics, clinical bioinformatics, environmental applications and bioinformatics engineering. Across those fields, I kept coming back to a question I often encounter in my work at Mass Dynamics. How do we turn evolving scientific methods into software people can use and trust? The clinical bioinformatics session really resonated with me. In both clinical services and live production environments, people rely on software to do their work while the science and the tools continue to change.

Three themes stayed with me throughout the day. I found myself thinking about how we make AI outputs verifiable, how we maintain confidence in software as it changes, and how we build data governance into systems from the start.

## Making AI outputs verifiable
What does it mean to have a “human in the loop” when using AI?
That question from [Dr Simon Sadedin](https://www.mcri.edu.au/researcher-details/simon-sadedin)’s talk stuck with me. I recognised the problem from my own experience with AI agents. An answer can sound confident and plausible, then fall apart when I check it closely. What exactly are we asking the reviewer to check? Can they trace a claim to its source? How much work does that take?

{{< figure src="simon.jpeg" alt="Dr Simon Sadedin on stage" caption="Dr Simon Sadedin take home message from his talk 'Verifiability of models in clinical applications'." width="80%" >}}

Simon explored these questions through variant curation, where specialists gather and assess evidence to determine whether a genetic variant contributes to disease. Reviewing large volumes of literature makes this an appealing area for AI support. However, for that support to be useful, a curator needs to be able to find the evidence behind each claim and decide whether it supports the conclusion.

What I found really valuable in Simon’s suggestions was the emphasis on designing the system around that review. If the evidence is difficult to find, or the volume of information overwhelms the reviewers, it becomes much harder for them to catch errors.

## Maintaining confidence as software evolves
The same question about verification came up at the level of the software itself. I loved the analogy [Dr Eva Chan](https://www.linkedin.com/in/eva-chan-2960b8a4/), Senior Clinical Bioinformatician at Hartwig Medical Foundation, used to explain the demands of different settings. Bioinformatics research is like an F1 car. It pushes what’s possible and often takes a specialist team to run. Clinical bioinformatics needs to work like a road car, operating reliably as part of an established service. Bringing a research innovation into the clinic means validating it for its intended use.

[Claire Lillee](https://www.linkedin.com/in/claire-lillee-588547273/), Principal Accreditation Specialist at the National Association of Testing Authorities (NATA), brought this challenge into focus. She explained that NATA accredits the laboratory, and software plays an increasingly important role in the steps between receiving a specimen and issuing a clinical report. When only a few specialists understand what happens to the data during analysis, it can be difficult for others to trace how the result was produced.

{{< figure src="nata.jpeg" alt="Claire Lillee presenting a slide on NPAAC software requirements" caption="Claire Lillee on NPAAC (National Pathology Accreditation Advisory Council) software requirements for Australian pathology accreditation." width="80%" >}}

During the Q&A, Simon highlighted the role of engineering in making that work easier to verify. Version control helps us track what changed, automated tests help us check how the software behaves after a change, and reproducible workflows help us trace how a result was produced. As Claire pointed out, checks that are easier to repeat are also easier to make part of everyday work.

That connection between software design and ongoing validation is something I see at [Mass Dynamics](https://massdynamics.com/), where bioinformaticians and engineers work closely together. In my talk in the Bioinformatics Engineering session, I described our shift from a largely monolithic architecture to a more modular, standardised system. Each new workflow now has its own CI/CD pipeline, with tests that run when the workflow is updated. The aim was to make it easier for scientists to add functionality, with fewer changes across repositories and a clearer way to test their work. At the same time, those same design choices could also make it easier to review changes proposed by AI agents.

## “Governance is at the heart of anything”

{{< figure src="data-sov.jpg" alt="Adam Heterick presenting on data sovereignty" caption="Adam Heterick on data sovereignty in the talk 'Building data systems for Indigenous precision healthcare'." width="80%" >}}

From the SBEI 2026 talk by [A/Prof Jimmy Breen](https://www.thekids.org.au/contact-us/our-people/b/jimmy-breen/) and [Adam Heterick](https://www.linkedin.com/in/adam-heterick-849970119/).
In the Population-Scale Bioinformatics session, Associate Professor Jimmy Breen and Adam Heterick spoke about building data systems for Indigenous precision healthcare through the [Black Ochre Data Lab](https://blackochrelabs.au/). As Jimmy put it, “good intentions are not enough”. Decisions about what data is collected, who can access it, who decides how it’s used and who benefits need to shape the system from the start. Those decisions also depend on ongoing relationships with the communities involved.

While this has particular connotations when working with Indigenous data, I found this an extremely important and general reminder that building software that ingests and processes data involves more than solving the technical scientific problem. Decisions about access and use shape what happens to people’s data at every step, from collection through to analysis and sharing. Thinking through those decisions early should be part of the discussion from day one.

I left SBEI grateful for the chance to reconnect with peers and hear how they approach challenges I recognise from my own work. Across research, clinical analysis and public health, developing a useful method is one part of the job. We also need to make it accessible, give people a way to check its results, and build systems they can continue to trust as the software evolves.
