---
title: "Pickles to Alaska"
layout: post
date: 2026-05-30 09:00
category: blog
author: susheel
tag:
- governance
- health data
- open science
- infrastructure
- food banks
- Five Safes
description: "What a food bank, a beard tax, and a shipping container teach us about health data governance."
---

*What a food bank, a beard tax, and a shipping container teach us about health data governance*

---

![From fragmentation to order: governance as infrastructure](/assets/images/blog/header-fragmentation-to-order.png)

In 2005, Feeding America distributed 220 million pounds of food a year to 200 member food banks across the United States using a system that was, by any honest assessment, broken [1, 2]. A centralised algorithm in Chicago allocated donated food in proportion to each food bank's "goal factor," a metric based on local poverty rates and population size. The algorithm treated all pounds of food as identical. A pound of potato chips received the same priority as a pound of protein. It sent five-gallon buckets of pickles to Alaska, where nobody had asked for pickles and nobody knew what to do with them. It flooded Idaho warehouses with potatoes, in a state already drowning in potatoes. Nobody in the system wanted this. The algorithm did not care what anyone wanted. It had a formula, and the formula was hungry. And if a food bank refused an unsuitable load, that refusal counted against its need score, punishing waste avoidance and forcing food banks to accept goods they could not use in order to maintain their place in the queue.

The system was not malicious. It was not even incompetent. It was the logical consequence of a governance architecture designed around a single principle: allocate in proportion to need. The principle was correct. The implementation was catastrophic. Because the system had no visibility into what food banks already had in stock, what their local donors were already providing (food banks received 80% of their supply from local sources), what their storage constraints were, or what their communities actually needed [1]. It treated governance as a formula, not an infrastructure.

In 2004, an economist named Canice Prendergast joined a task force [2, 3] of food bank directors and University of Chicago academics to redesign the system. The internal politics were brutal. One food bank director told Prendergast directly: "I am a socialist. That is why I run a food bank. I do not believe in markets. I am not saying I will not listen, but I am against this." The task force spent over a year building something that had never been attempted at this scale: a fictional-currency auction system that combined market efficiency with equitable distribution.

Every food bank received "shares" in proportion to need, the same principle as before, but could spend those shares however it chose through twice-daily online auctions. Food banks could bid on what they actually needed, access price histories, form joint bids to split truckloads, and even bid negative amounts to accept hard-to-move products donors insisted on giving. Shares spent during the day were redistributed at midnight using the same need-based formula, meaning high bids by wealthy food banks benefited all participants.

Supply increased by 100 million pounds in the year following implementation [2]. The equivalent of feeding an additional 60,000 people every day. And the auctions revealed how profoundly the old system had failed: food banks were willing to trade 116 pounds of produce for a single pound of pasta [1, 3]. Let that sink in. A hundred and sixteen pounds of vegetables for one pound of dried carbohydrates. That is not a preference. That is a distress signal encoded in an exchange rate. The Fairness and Equity Committee, designed to protect smaller food banks, never convened. It did not need to. The system worked.

## Fourteen months for an afternoon's query

![Governance as a gate versus governance as infrastructure](/assets/images/blog/gate-vs-grid.png)

The standard narrative about health data runs like this: if only we had better formats, better APIs, better databases, we could unlock the data and transform research. FHIR exists. OMOP exists. The Protein Data Bank has been open since 1971. The technical infrastructure for sharing health data is more mature than it has ever been.

The bottleneck is not technical. It is governance.

A researcher at a university in London wants to study the relationship between genetic variants and drug response across three countries. The data exists. The formats are compatible. The APIs are operational. But the researcher must now navigate three separate data access committees, each with its own application form, its own review criteria, its own timeline, and its own interpretation of what "safe use" means. One committee meets monthly. Another meets quarterly. The third requires a revision that takes six weeks to process, and its revision template was last updated during the Obama administration. All three committees consider themselves efficient. All three are, in their own way, correct. The technical query would take an afternoon. The governance process takes fourteen months. By which time the researcher has graduated, changed institutions, or simply lost the will to live.

This is the health data equivalent of sending pickles to Alaska. Not because anyone is hostile to the research. But because the governance architecture was designed around a single principle, protect the data, and implemented without the infrastructure to make that principle work at scale. Each committee is doing its job. The system as a whole is failing.

## Anaesthesia spread in weeks. Antisepsis took decades.

In 2013, the surgeon and writer Atul Gawande published an essay called "Slow Ideas" in which he made an observation that I have not been able to shake [4]. In the history of medicine, some innovations spread almost instantly. Anaesthesia was one. On 16 October 1846, a dentist named William Morton demonstrated ether anaesthesia at Massachusetts General Hospital. Within two months, it was being used on every continent. Anaesthesia solved the surgeon's problem. It made the surgeon's job easier.

Antisepsis was different. Joseph Lister published his findings on carbolic acid in 1867. Adoption took decades. Not because the evidence was weaker, it was, if anything, stronger, but because antisepsis asked the surgeon to change. To wash hands, to sterilise instruments, to accept that invisible organisms on their own fingers were killing their patients. Anaesthesia removed pain. Antisepsis imposed discipline.

Governance reforms that reduce friction spread. Governance reforms that demand behaviour change stall. The Montreal Protocol succeeded in part because it did not require anyone to personally stop using hairspray. It required manufacturers to reformulate. The compliance burden fell on organisations with legal departments, not on individuals with aerosol cans. This is a design lesson, not a historical curiosity.

The Montreal Protocol is the cleanest example of governance that spread. In 1987, 46 countries signed an agreement to phase out chlorofluorocarbons [5, 11]. The initial targets were too weak. If the signatories had stuck to the original protocol, the ozone hole would have continued to grow. But the governance architecture was designed to ratchet: as evidence accumulated, targets tightened, more countries joined, and more substances were added to the list. By the turn of the millennium, 174 parties had signed on. By 2009, it became the first convention in history to achieve universal ratification, with 198 parties. Consumption of ozone-depleting substances fell by over 99% [5, 11].

The Montreal Protocol did not fix the ozone layer by banning CFCs overnight. It fixed it by giving industry a governance framework they could plan around: graduated timelines, technology transfer funds, measurable compliance criteria. The protocol created the conditions under which local decisions, by thousands of individual companies across dozens of countries, produced a global outcome that centralised command could never have achieved. It was Feeding America's auction, applied to the atmosphere.

## Machine-readable compliance, circa 1705

There is a precedent for this kind of thinking that is older than anyone might expect. In 1705, Peter the Great of Russia decided that beards were a remnant of medieval backwardness [6] and ordered Russian men to shave. The Boyards, the Russian nobility, were not pleased. Peter could have sent police with razors. Instead, he created a graduated beard tax. The price varied by class and occupation. Those who paid received a physical token, a coin bearing the words "the beard tax has been taken" on one face and "the beard is an unnecessary burden" on the other. Silver tokens for the Boyards. Copper for commoners.

Peter the Great's beard tax tokens were, in effect, machine-readable proof of compliance, three hundred years before the Open Digital Rights Language. The principle is worth pausing on: make compliance legible, graduated, and self-certifying. Do not demand that everyone shave. Create an infrastructure that makes the cost of keeping your beard visible, proportionate, and auditable.

Full disclosure: I alternate between bearded and clean-shaven roughly every six months, which under Peter's system would have made me a walking audit finding. Bearded in winter, shaven in summer, taxable in January, exempt by July, and back on the books by Christmas. My barber would have needed to file quarterly compliance reports. The Russian treasury would have needed a seasonal revenue model. And the border guard checking my token would have had to decide whether a three-day stubble constituted a beard or an intention to comply. This is not an absurd scenario. This is exactly how most data access agreements work: binary decisions applied to continuous states, by committees that meet too infrequently to notice the world has changed between meetings.

![Left: the author in his bearded, non-compliant state. Right: the author in his shaven, tax-exempt state. Same person. Different regulatory status.](/assets/images/blog/susheel-side-by-side.png)

The governance is not the prohibition. The governance is the token.

This is what health data governance gets wrong. It treats governance as a gate: you are either approved or you are not, you have access or you do not, you comply or you fail. The gate model produces exactly the dysfunction we see, fourteen-month waits for a query that takes an afternoon, because the gate has no granularity, no graduation, no mechanism for making the rules legible to the people who must follow them.

## One form, many landlords

I should be direct about why this matters to me. I lead data governance work at Sage Bionetworks, and one of the problems we work on is absurdly simple to state and punishingly difficult to solve: a researcher who needs data from five custodians should not have to fill in five different forms asking the same questions in five different ways, as though each custodian independently discovered the concept of a name and address, patented it, and was charging licensing fees.

The question is whether governance rules can be expressed in a form that machines can read, not just committees. The Open Digital Rights Language, ODRL, is a W3C standard for expressing permissions and constraints in machine-readable form [9]. It allows us to encode the Five Safes framework [10], the standard model for governing access to sensitive data (safe people, safe projects, safe settings, safe data, safe outputs) as computable policy rather than narrative prose.

This matters because prose does not scale. A data access form written in English can be interpreted by a committee in London and a committee in Melbourne and a committee in Nairobi, and all three interpretations can be reasonable, and all three can be different. This is not a hypothetical. I have sat through a meeting where two committees spent forty minutes debating whether "non-commercial use" included a researcher at a publicly funded university whose salary was partially paid by an industry consortium. The researcher in question was studying a rare paediatric disease. Both sides had a point. Neither side had a machine-readable definition. The child did not have forty minutes.

A policy expressed in ODRL can be interpreted by a machine, consistently, at the speed the machine operates. The researcher's request is not simplified. The governance is not weakened. The translation, the fourteen months of back-and-forth between a researcher and three committees speaking slightly different dialects of the same language, is eliminated.

This is governance as infrastructure. Not governance as gate.

## The box that changed the world

![Connected systems: from islands to infrastructure](/assets/images/blog/connected-islands.png)

In 1956, a trucking entrepreneur named Malcolm McLean loaded 58 aluminium containers onto a converted oil tanker in Newark, New Jersey, and shipped them to Houston [12]. The containers were not a new idea. People had been putting things in boxes for millennia. What McLean did was standardise the box.

Before containerisation, loading a ship took days. Cargo was handled piece by piece, in barrels, crates, sacks, and loose bundles, by gangs of longshoremen who stacked it by hand in the hold. Theft was so routine it had its own euphemism, "pilferage," which is the kind of word you invent when you have given up solving a problem and decided instead to give it a gentler name. Breakage was expected. A typical cargo ship spent more time in port being loaded and unloaded than it spent at sea. The cost of moving goods was dominated not by the distance travelled but by the number of times a human hand touched them.

McLean's insight was not about ships. It was about interfaces. If every container is the same size, any crane can lift it, any truck can carry it, any ship can stack it, any port can handle it. You do not need to redesign the port or the truck or the ship. You standardise the connection between them. The container was not a technology. It was a protocol.

World trade did not globalise because ships got faster. It globalised because the interface between ship, port, truck, and train became standardised, interoperable, and invisible [12]. The contents of the box were infinitely varied. The box was always the same.

Health data governance needs its container. Not a single system that every custodian must adopt, but a standardised interface that lets different governance frameworks connect. Machine-readable policy, expressed in open standards, that travels with the data request and can be validated at any node. The contents of the governance, the specific rules, the local interpretations, the risk assessments, remain infinitely varied. The interface is always the same.

## The postal principle

Health data governance is stuck between two failed models. The first is centralised command: a single authority decides who gets access to what, on what terms, on what timeline. This produces the pickles-to-Alaska problem. The second is balkanised autonomy: every custodian sets its own rules, its own forms, its own review cycles. This produces the fourteen-month problem.

There is a third path, and it has been working quietly since 1874. The Universal Postal Union, founded in Bern, is one of the oldest international organisations in existence [13]. It solved a problem that is structurally identical to federated health data governance: how do you get 192 countries with wildly different postal systems, different addressing conventions, different delivery standards, and different languages on the envelope to reliably deliver each other's mail without anyone having to learn Swahili or Mandarin or, God forbid, agree on a universal filing system?

The UPU did not build a global postal service. It did not require countries to adopt the same sorting machines or the same delivery vans or the same uniforms. What it built was a governance protocol: shared rules for addressing, routing, transit fees, and liability, implemented locally by each national postal service according to its own operational reality. Your letter reaches Tokyo not because Japan and Britain agreed on the same postal system, but because they agreed on the same interface between systems.

The food bank auction embodied this same principle. Chicago set the shared rules. The food banks made local decisions. The system monitored itself. And when the most vocal socialist on the board became the system's strongest advocate, the proof was in the behaviour, not the principle.

## The moment we are in

![Distributed systems converging on shared protocols](/assets/images/blog/grid-synchronisation.png)

Health data governance is at its containerisation moment. The technical infrastructure exists. FHIR, OMOP, the GA4GH standards, the Trusted Research Environments, the cloud platforms, the compute. What does not exist is the governance infrastructure, the standardised interface between systems, that would let these technical systems interoperate at the speed research requires.

The goal is governance that travels with the data, that is computable at every node, that makes the rules legible to machines as well as to committees. Shared rules, local decisions, structured accountability, graduated enforcement. Not a single system. A shared protocol. Not a bigger gate. A better grid.

Governance is not the impediment. Bad governance is the impediment. Governance designed as a gate, a single point of approval or denial, is a bottleneck by definition. Governance designed as infrastructure, distributed, graduated, machine-readable, locally adapted, collectively governed, is the thing that makes everything else work.

Feeding America did not build a better warehouse. It built a better protocol for matching supply to demand. The Montreal Protocol did not invent a new refrigerant. It built a governance framework that made the transition plannable, measurable, and enforceable. Peter the Great did not send police with razors. He built a graduated, self-certifying compliance system that made the cost of keeping your beard visible, proportionate, and, for the Boyards at least, rather expensive. Malcolm McLean did not build a faster ship. He standardised the box.

Build the governance well, and everything built on top of it works. Build it badly, and you send pickles to Alaska.

---

*Susheel Varma is Chief Data Officer at Sage Bionetworks, where he leads data strategy, governance, and infrastructure for biomedical research programmes funded by NIH, ARPA-H, and other agencies.*

**References:**

1. Zimmerman, E. (2026). "How market design can feed the poor." *Works in Progress*, 11 February 2026. [https://worksinprogress.co/issue/how-market-design-can-feed-the-poor/](https://worksinprogress.co/issue/how-market-design-can-feed-the-poor/)
2. Prendergast, C. (2022). "The Allocation of Food to Food Banks." *Journal of Political Economy*, 130(8), pp. 1993-2017. [https://doi.org/10.1086/720332](https://doi.org/10.1086/720332)
3. Prendergast, C. (2017). "How Food Banks Use Markets to Feed the Poor." *Journal of Economic Perspectives*, 31(4), pp. 145-162. [https://doi.org/10.1257/jep.31.4.145](https://doi.org/10.1257/jep.31.4.145)
4. Gawande, A. (2013). "Slow Ideas." *The New Yorker*, 29 July 2013. [https://www.newyorker.com/magazine/2013/07/29/slow-ideas](https://www.newyorker.com/magazine/2013/07/29/slow-ideas)
5. Ritchie, H. (2025). "How we fixed the ozone layer." *Works in Progress*, 28 March 2025. [https://worksinprogress.co/issue/how-we-fixed-the-ozone-layer/](https://worksinprogress.co/issue/how-we-fixed-the-ozone-layer/)
6. Lewis, D. (2013). "Beard Dough." *Now I Know*, 28 March 2013. [https://nowiknow.com/beard-dough/](https://nowiknow.com/beard-dough/)
7. Ostrom, E. (1990). *Governing the Commons: The Evolution of Institutions for Collective Action*. Cambridge University Press. [https://doi.org/10.1017/CBO9780511807763](https://doi.org/10.1017/CBO9780511807763)
8. W3C (2018). *ODRL Information Model 2.2*. W3C Recommendation, 15 February 2018. [https://www.w3.org/TR/odrl-model/](https://www.w3.org/TR/odrl-model/)
9. Desai, T., Ritchie, F., and Welpton, R. (2016). "Five Safes: designing data access for research." Economics Working Paper Series 1601, University of the West of England, Bristol. [https://www2.uwe.ac.uk/faculties/BBS/Documents/1601.pdf](https://www2.uwe.ac.uk/faculties/BBS/Documents/1601.pdf)
10. UNEP Ozone Secretariat. "Montreal Protocol on Substances that Deplete the Ozone Layer." [https://ozone.unep.org/treaties/montreal-protocol](https://ozone.unep.org/treaties/montreal-protocol)
11. Levinson, M. (2006). *The Box: How the Shipping Container Made the World Smaller and the World Economy Bigger*. Princeton University Press. [https://doi.org/10.1515/9781400880584](https://doi.org/10.1515/9781400880584)
12. Universal Postal Union. "History." [https://www.upu.int/en/Universal-Postal-Union/About-UPU/History](https://www.upu.int/en/Universal-Postal-Union/About-UPU/History)
