+++
title = "Current Research"
description = "I use household survey data and simulation to explore responses to economic uncertainty. My current work revisits graduate research on agricultural livelihoods, enterprise, and land tenure, alongside experiments in adaptation and learned decision rules."
date = 2026-11-11
lastmod = 2026-11-16
draft = false
weight = -1
image = "img/portfolio/current-research.svg"
imagealt = "Illustration of household economic decisions beside a Sugarscape resource grid with illustrative agents."
showonlyimage = false
comments = false
+++

*Updated November 2026.*

My research interests center on how households respond to economic uncertainty and how resources, institutions, and local markets shape their choices. These interests extend to the sustainability and resilience of the food supply under climatic and technological change. I want to understand both the benefits and adverse effects of these changes for households involved in food production, including their livelihoods, production decisions, and capacity to adapt.

Several projects began during my master's studies in Applied Data Science through the Department of Politics and Economics at Claremont Graduate University. Continuing this work has led me to reconsider earlier findings and develop more specific questions. Alongside these household studies, I have pursued simulation experiments in adaptation, learning, and collective behavior.

### Household Resilience to Commodity-Price Shocks

This work began in a spring 2024 course with a proposal about agroforestry and coffee-price risk in Tanzania. Two distinct Ethiopian papers followed. In *Agricultural Practices & Price Shocks in Ethiopian Coffee*, I combined two-way fixed-effects analysis with a stacked machine-learning ensemble to examine agricultural practices, credit, and household consumption among coffee farmers. The predictive results do not identify causal effects of agricultural practices on consumption during price shocks.

In the later report, [*Understanding Household Resilience to Commodity Price Shocks*](/html/commodity.html), I broadened the analysis beyond coffee-growing households, constructed crop-based price-exposure indices, and estimated associations between forest cover and consumption responses. Review identified inconsistent crop and land-use classifications and a household-identifier mismatch that left geographic covariates unmatched in one wave. Using forest cover as a proxy for agroforestry raised concerns about construct validity, while constructing exposure from contemporaneous crop-area shares introduced potential endogeneity.

I recently began rebuilding the project using the documented survey definitions and explicit data pipeline checks. A weather extension still requires correction to the temporal ordering of exposure and outcome recall periods. A literature review on resilience measurement, commodity-price transmission, and exposure-based designs has shifted my emphasis toward household adjustment. For the next study, I propose returning to coffee and distinguishing dependence on coffee receipts from land-based exposure.

### Household Enterprise and Commodity-Price Declines

For a computational and agent-based modeling class, I developed a [NetLogo model](/html/enterprise.html) to explore how commodity prices, household capabilities, credit, and grants affected enterprise participation and inequality. I later found inconsistencies in borrowing costs, resource allocation, and wealth accounting, including input assumptions that allowed production without labor or capital. These problems limit interpretation of the original policy comparisons. I revised the NetLogo implementation and completed a tested Python port of the earlier model. The current rebuild still requires a new economic specification and implementation.

My immediate aim is to reassess the original question: how commodity-price shocks, household capabilities, credit, and grants affect enterprise participation, wealth, and inequality. A literature review on rural labor markets, seasonal credit, and local demand is informing a new economic specification, including the distinction between enterprise entry and improvements in household welfare. Before conducting further simulation experiments, I need to specify production and household decisions, budget constraints, market assumptions, and the timing of borrowing, income, and consumption. I then need to implement those equations and verify the model against analytical benchmarks. That work will help determine whether the original question needs narrowing and which extensions are justified.

### Coffee Prices and Household Enterprise in Tanzania

This project began as an attempt to reconstruct Adhvaryu, Kala, and Nyshadham’s study, *Booms, Busts, and Household Enterprise: Evidence from Coffee Farmers in Tanzania*, using the historical Kagera survey. I then sought to replicate their findings using later Tanzanian household panels available through the World Bank. Research on household income and local demand informed how I considered competing explanations for enterprise entry and its implications for household welfare.

I recovered the historical association, but unavailable author code, uncertainty about price data, and unresolved units of measurement and sample-construction rules limit exact replication. In my reconstruction, a sample close to the published benchmark includes interview attempts and partial interviews coded as having no enterprise, potentially conflating missing enterprise data with observed non-ownership. An analysis restricted to completed interviews retains the same direction of association. My report documents the unresolved measurement and sample-construction choices. Three designs using later World Bank panels stopped before estimation because of limited effective sample sizes, insufficient cluster support, or inadequate statistical precision. Further claims about enterprise as coping will require additional source materials or a new research design.

### Land Tenure and Land Conditions in Nigeria

This project began with a 2024 coursework proposal asking whether uncertain access to farmland discourages investment with longer-term returns. An assessment of survey documentation across eight LSMS-ISA countries led me to Nigeria’s 2023–24 survey. The subsequent literature review revealed a crowded research area, including recent studies using the same survey. It also showed why particular rights, investment horizons, and institutions need to be distinguished, and why reported practices do not by themselves demonstrate improved land conditions.

I completed survey-weighted descriptive analyses of land-use arrangements, documentation, reported acquisition dates, and perceived tenure security. Questionnaire routing and survey-design ambiguities required separate definitions of eligible populations, with sensitivity analyses for missing acquisition years and tenure composition. Tenure dimensions associated with perceived tenure security did not relate uniformly to reported erosion or erosion-control and water-harvesting facilities. I have completed a paper outline focused on these measurement questions; the findings do not establish causal effects of land rights. The broader research question still needs revision and may require substantial narrowing to make a distinct contribution. This experience reinforced the need to review the literature before committing to a research question and empirical design.

### Artificial Life and Adaptive Networks

These experiments began by asking whether recurrent networks with local learning rules could develop persistent, differentiated organization without an externally scored task. I used large language models (LLMs) to generate simulation code and assist with analysis, interpretation, and drafting. My verification and recordkeeping were insufficient: implementation errors survived repeated model-assisted reviews, and incomplete records limited reconstruction of earlier runs. An error in the update sequence caused newly added connections to be deleted before they could learn. Unequal test inputs and spatial geometry also confounded the interpretation of some apparent differences in network behavior.

Some differentiated responses remained reproducible under matched inputs. I preserved those findings and completed a small reference reconstruction with explicit update rules, measurement controls, and recorded configurations. Reviewing the literature on structural plasticity, continual learning, and artificial life revealed close precedents and helped narrow my interest to how networks retain and reacquire responses as their connections change. A possible next study would reproduce an established local-learning model, then examine how connection maintenance and the allocation of learning rates affect responses after inputs change.

### Sugarscape and Learned Decision Rules

I reimplemented Sugarscape in Mesa and added decision modules to examine how natural-language prompts affect movement, trade, social actions, and consumption. LLMs also assisted with code development, analysis, and paper drafting. The original experiments used a factorial design crossing four prompts with five decision configurations. To manage API cost and latency, I reused cached decisions across distinct states; invalid responses triggered default actions. The movement code also incorrectly logs an allowed stay-in-place response as invalid. These features complicate interpretation of population outcomes.

My revised experimental design draws on a literature review of generative agents, behavioral validation, and computational cost. It includes unprompted, irrelevant-prompt, and rule-restatement control conditions, plus sensitivity analyses for prompt paraphrases and decision reuse. Those revised comparisons have not been run. Future work could compare generative LLMs with [TypeSafe’s Jev](https://typesafe.ai/blog/introducing-system-one-models-and-jev) or similar models that choose among predefined actions. Using matched states, rules, and settings, I would compare behavior, response reliability, latency, and cost to assess whether learned decision rules add useful variation beyond simpler rules. Prompt sensitivity alone would not demonstrate human-like motives or realistic social behavior.
