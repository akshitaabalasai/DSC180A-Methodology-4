---
layout: default
title: Project Reflections
---

# Akshitaa Balasai

[abalasai@ucsd.edu](mailto:abalasai@ucsd.edu)

**Section:** D01

**Domain:** AI for Good: Misinformation and Disinformation Detection, Ranking, and Mitigation

**Mentor:** Ali Arsanjani

**Quarter 1 project:** Analyzing the validity and sentiment behind peptide discourse on the internet.

**What is the most interesting topic covered in your domain this quarter?**

The topic I find most interesting is the relationship between the sentiment of an online discussion and the evidence supporting its claims. In our peptide discourse project, I am interested in how enthusiastic testimonials, skeptical comments, and scientific-sounding language influence the way a claim is presented. A positive sentiment score does not establish that a claim is accurate, and a negative score does not establish that it is false. I want to understand how natural language processing can distinguish these dimensions while preserving the context of what someone is actually claiming. This makes misinformation detection an interesting problem because identifying the tone of a post is only one part of evaluating its content.

**Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

I would like to investigate whether providing a language model with retrieved scientific evidence improves its ability to assess specific claims in online peptide discussions compared with asking the same model to assess those claims without retrieval. I would start with a small set of frequently discussed peptides and a manageable sample of public posts that we are permitted to collect. I would extract factual claims and build a manually reviewed evaluation set with labels such as supported, contradicted, and insufficient evidence, using a documented evidence rubric. Personal experiences and opinions would be marked separately rather than automatically treated as verifiable scientific claims.

For each claim, the retrieval-based system would return relevant passages, an evidence assessment, and citations. I would compare the two systems using macro-F1 on the reviewed labels, citation relevance, and the rate of unsupported conclusions. I would also examine whether errors differ between positive, neutral, and negative posts. To keep the investigation feasible, I would first verify access to both the posts and reference material, then limit the scope to what we can annotate carefully within the quarter. The main output would be an evaluation report and a website showing aggregate results and selected de-identified examples, with uncertainty made explicit.

**What is a potential change you’d make to the approach taken in your current Quarter 1 Project?**

One change I would prioritize is making the distinction between sentiment and claim validity explicit in our annotation and evaluation process. Since our current project studies both, I would assess sentiment toward a particular peptide separately from the evidence supporting each factual claim. For example, a post can express enthusiasm while making a claim for which the available evidence is insufficient. I would use a written annotation guide, have two annotators independently label a subset, and review disagreements before expanding the dataset. I would also keep duplicate or closely related posts from the same discussion out of different training and test splits. These steps would make it easier to identify whether errors come from ambiguous language, unclear evidence standards, or a model that does not generalize to new discussions.

**What other techniques would you be interested in using in your project?**

I would be interested in aspect-based sentiment analysis, which could separate attitudes toward effectiveness, safety, cost, and accessibility instead of assigning one overall sentiment to a post. Topic modeling or embedding-based clustering could help identify recurring themes and guide the selection of claims for closer review. Retrieval-augmented generation could connect those claims to relevant reference passages, while a natural language inference model could provide an additional comparison for whether a passage supports or contradicts a claim. I would evaluate these methods against simpler baselines and inspect their errors manually. I would also explore confidence calibration and an abstention option so that the system can indicate when it lacks enough evidence instead of forcing a confident judgment.
