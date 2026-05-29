---
title: "Artificial Stupidity"
layout: post
date: 2026-03-27 09:00
category: blog
author: susheel
tag:
- AI
- science
- epistemology
- biomedical research
- machine learning
description: "Why the most important thing we can teach AI is how to say 'I don't know'."
---

*Why the most important thing we can teach AI is how to say "I don't know"*

---

In 2008, a cell biologist named Martin Schwartz wrote a one-page essay that has now been read by over a million people. In it, he tells the story of a brilliant former student who dropped out of a prestigious PhD programme and retrained in an entirely different field. When he asked her why, she said something that has stayed with me ever since I first read it: "It made me feel stupid."

Schwartz did not see this as a tragedy. He saw it as a misunderstanding, one that science itself has failed to correct. During his own PhD, he had taken a problem to Henry Taube, a faculty member who would go on to win the Nobel Prize. Taube did not know the answer. Schwartz was a third-year graduate student. If Taube did not know, nobody did.

"That's when it hit me," Schwartz wrote. "Nobody did. That's why it was a research problem."

He went on to make a distinction I think about constantly. There are two kinds of stupidity. *Relative stupidity* is not knowing what others already know, a gap you can close with effort. *Absolute stupidity* is confronting questions nobody has answered, the permanent condition of working at the frontier of knowledge. The first is a deficit. The second is the engine of discovery.

"The more comfortable we become with being stupid," he concluded, "the deeper we will wade into the unknown and the more likely we are to make big discoveries."

The Columbia neuroscientist Stuart Firestein took this further in his 2012 book *Ignorance: How It Drives Science*. "Working scientists don't get bogged down in the factual swamp," he wrote, "because they don't stop at the facts; they begin there, right beyond the facts, where the facts run out." Firestein argues that knowledge is a big subject, but ignorance is a bigger one, and it is ignorance, not knowledge, that is the true engine of scientific progress.

## The moment it clicked

This week, Sage Bionetworks held its Home Week, one of two annual gatherings where our entire organisation comes together in person. Presentation after presentation focused on artificial intelligence: what it can do for biomedical research, how it accelerates discovery, where it augments human capacity. The demos were impressive. The benchmarks were climbing. And somewhere between the third and fourth talk, Schwartz's essay came flooding back to me.

We are optimising AI for the wrong thing.

We are building systems that are relentlessly, fluently, confidently intelligent. What we should be building, especially for science, are systems capable of something far harder: *artificial stupidity*.

## The machines that never feel stupid

Here is the problem. We have spent the last decade building AI systems that are constitutionally incapable of feeling stupid. Large language models produce fluent, authoritative output whether they are summarising established science or fabricating something entirely. They have no internal signal that says "I am out of my depth." They experience no discomfort at the boundary of their knowledge, because they have no representation of that boundary at all.

In human cognition, feeling stupid is not a bug. It is a feature. It is an epistemic alarm system: a signal to slow down, question your assumptions, redesign the experiment, ask for help. Schwartz's former student left her PhD because she interpreted that signal as failure. But the signal itself was working perfectly. It was telling her she was at the frontier.

Our AI systems have no such alarm. And the consequences are not theoretical.

A 2025 study from MIT Media Lab found that medical AI models hallucinate at rates between 15% and 40% on clinical tasks, generating fabricated medications, contraindicated drug recommendations, and false imaging interpretations with the same confident tone they use for established medical facts. A January 2026 analysis from Duke University asked the question bluntly: "It's 2026. Why are LLMs still hallucinating?"

The answer turns out to be remarkably simple, and damning. In 2025, a team of OpenAI's own researchers published a paper demonstrating that hallucination is not a bug but an incentive design flaw. Models are trained and evaluated on accuracy metrics where "I don't know" scores zero. A model that guesses "September 10" for an unknown birthday has a 1-in-365 chance of being right, while honest uncertainty guarantees zero points. As the authors put it: "Because 'I don't know' is scored as zero, bluffing is almost always the optimal strategy."

We have literally built systems that are penalised for honesty and rewarded for overconfidence. The parallel to scientific culture, where admitting ignorance is too often seen as weakness, is direct. But at least scientists have the capacity to feel stupid. These systems do not.

## Turing saw this coming. So did McDermott.

The irony is that artificial stupidity is not a new idea. It is, in fact, one of the oldest ideas in computer science.

In 1950, Alan Turing proposed his famous test for machine intelligence. Almost immediately, he identified a problem: "The machine would be unmasked because of its deadly accuracy." A machine that never made mistakes would be obviously inhuman. His proposed solution? The machine should deliberately introduce errors. It should, in effect, be artificially stupid.

For decades, this remained a niche concept. Video game designers used it to make AI opponents beatable. Chatbot builders used it to make conversational agents seem more human. The first Loebner Prize for the most human-like chatbot, awarded in 1991, went to a programme that incorporated deliberate errors, what *The Economist* described as "artificial stupidity."

And in 1976, the Yale computer scientist Drew McDermott published a paper with a title that deserves to be read aloud at every AI conference: "Artificial Intelligence Meets Natural Stupidity." His target was what he called "wishful mnemonics," the habit of giving AI systems names like "General Problem Solver" that wildly exceeded their actual capabilities. He pleaded for "humble, technical" names instead, warning that grandiose labelling inflates expectations and cripples a field's self-discipline. Half a century later, we name our systems GPT, Gemini, and Claude, and wonder why the public expects omniscience.

But we missed the deeper insight in both Turing and McDermott. They were not just saying machines should fake mistakes or carry modest names. They were pointing at something about the nature of intelligence itself: that genuine understanding includes knowing what you do not understand. Perfection is not intelligence. It is a simulation of intelligence that breaks down the moment it encounters something genuinely new.

## From dumbing down to wising up

What I am arguing for is not the old artificial stupidity of video games and chatbots, where systems pretend to be less capable than they are. I am arguing for a new kind: systems that genuinely *know what they do not know*.

This is starting to happen. A 2026 paper in PLOS Digital Health introduced BODHI, an engineering framework for "curiosity-driven and humble AI" in clinical decision support. BODHI is a dual-reflective architecture grounded in two epistemic virtues: curiosity and humility. It decomposes epistemic uncertainty into task-specific dimensions and constrains model responses using what the authors call "virtue-based stance rules." The validation results were striking: 97.3% of BODHI-equipped AI responses included appropriate clarifying questions, compared to 0 to 7.8% at baseline. As the authors write: "When an AI system says 'I don't know,' it demonstrates a profound form of intelligence: the recognition of its own limits."

Read that again: *humility metrics*. We are beginning to measure AI systems not just by what they get right, but by how well they handle what they cannot get right. That is not a small thing.

In biomedical research, where I work, the stakes of overconfident inference are not abstract. They are patients, treatments, policy decisions, the allocation of hundreds of millions of dollars in research funding. When an AI system confidently proposes a drug target that does not exist, or synthesises evidence from papers it has invented, the cost is not just computational. It is human.

## What science actually needs from AI

The deepest problem is this: science is fundamentally about questions, not answers. The art of research is asking the right question, framing the experiment that will reveal something genuinely new. A system that generates confident answers to questions nobody has asked is not doing science. It is doing the opposite of science. It is filling the space where productive stupidity should live.

What science needs from AI is something much harder than fluent intelligence. It needs systems that can:

- Recognise when they are at the boundary of established knowledge and signal it clearly
- Distinguish between interpolation (working within known data) and extrapolation (venturing beyond it)
- Slow down in unfamiliar territory rather than maintaining the same confident pace
- Say "I don't know" as a genuine epistemic state, not a fallback when all else fails
- Support the human researcher's own productive stupidity, rather than short-circuiting it with premature answers

This is not a call for less capable AI. It is a call for differently capable AI. Systems that are not just intelligent, but *wise* in the old-fashioned sense: aware of the limits of their own understanding.

## The infrastructure of humility

When we think about building research infrastructure, we tend to focus on power: more compute, more data, more connections. But the most enduring infrastructure encodes *constraints*, not just capabilities. The Bermuda Principles, agreed in 1996, required that all human genome sequence data be released within 24 hours. That was not a capability. It was a rule that encoded humility, an acknowledgement that no single institution could or should control the frontier of genomic knowledge.

The same principle applies to AI in research. We need infrastructure that builds in epistemic humility at the protocol level, not as an afterthought but as a design requirement. Systems that flag uncertainty. Pipelines that distinguish between established findings and novel inferences. Platforms that make the boundaries of AI knowledge visible to researchers, rather than burying them under fluent prose.

## Feeling stupid, together

Schwartz's former student left science because feeling stupid felt like failure. The real failure would have been never feeling stupid at all.

As we build increasingly capable AI systems for biomedical research, let us remember what Schwartz taught us: the feeling of stupidity is not the enemy of discovery. It is the engine. The most important thing a scientist can say is "I don't know yet." The most important thing an AI system should be able to say is exactly the same.

We have spent years teaching machines to be intelligent. Perhaps it is time we taught them to be productively, honestly, courageously stupid.

Because the deeper we wade into the unknown, together, the more likely we are to make big discoveries.

---

*Susheel Varma is Chief Data Officer at Sage Bionetworks, where he leads data strategy, governance, and infrastructure for biomedical research programmes funded by NIH, ARPA-H, and other agencies.*

**References:**
- Schwartz, M.A. (2008). "The importance of stupidity in scientific research." *Journal of Cell Science*, 121(11), 1771.
- Firestein, S. (2012). *Ignorance: How It Drives Science*. Oxford University Press.
- Turing, A.M. (1950). "Computing Machinery and Intelligence." *Mind*, 59(236), 433-460.
- McDermott, D. (1976). "Artificial Intelligence Meets Natural Stupidity." *ACM SIGART Bulletin*, 57, 4-9.
- Kalai, A.T., Nachum, O., Vempala, S. & Zhang, Y. (2025). "Why Language Models Hallucinate." OpenAI / *arXiv:2509.04664*.
- Haim, N. et al. (2025). "Medical Hallucination in Foundation Models and Their Impact on Healthcare." *medRxiv/arXiv*.
- BODHI Framework (2026). "Beyond overconfidence: Embedding curiosity and humility for ethical medical AI." *PLOS Digital Health*.
- Duke University Libraries (2026). "It's 2026. Why Are LLMs Still Hallucinating?"
