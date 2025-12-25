# Experimental Data & Logs: Can LLMs Balance Competing Economic Goals?

This repository contains the experimental results and full chat interaction logs for the paper **"Can LLMs Balance Competing Economic Goals?"**.

## Abstract
As Large Language Models (LLMs) transition in their use case from passive text generators to autonomous social agents, their capacity to manage complex, non-linear systems needs to be evaluated. This paper investigates the optimization difficulty for Gemini (Thinking Mode) acting as a macroeconomic governor within a neoclassical agent-based economy. Using a 2×2 factorial design, we examine the interaction between prompting techniques (Chain-of-Thought vs. Tree-of-Thoughts) and environmental conditions (Expansionary vs. Recessionary). By granting the LLM an action space of 12 levers across three interconnected currency zones (EUR, USD, YEN), we test its ability to achieve Eurozone stability through multi-objective optimization of the Price Index and Credit Utilization.

Our results indicate that Gemini cannot consistently achieve stability across all economic conditions. While the model successfully navigated the Price Index targets but struggled with secondary Credit Utilization floors in expansionary environments, it demonstrated significant fragility in recessionary cycles. The Chain-of-Thought approach achieved initial stabilization but could not maintain long-term equilibrium, while the Tree-of-Thoughts strategy's exploratory depth proved catastrophic, necessitating premature experimental termination due to unsustainable policy trajectories. We identify a critical trade-off between decision speed and search depth, where the exploratory nature of the 'Tree-of-Thoughts' approach introduced severe volatility and temporal delays that proved catastrophic in high-pressure environments, contrasting with the more stable linear reasoning of 'Chain-of-Thought'.

## Overview
The study investigates Gemini (Thinking Mode) acting as a macroeconomic governor using a 2x2 factorial design:
* **Prompting Strategy:** Chain-of-Thought (CoT) vs. Tree-of-Thoughts (ToT)
* **Economic Condition:** Expansionary vs. Recessionary

## Directory Structure
* `data/`: Contains the CSV output files for the 12 economic levers tracked over the simulation steps.
* `logs/`: Contains the full chat history (prompts and model responses) documenting the agent's reasoning process during the experiments.

## Methodology Note
These experiments were conducted using the Gemini web interface. The `logs/` folder provides the exact prompt chains and resulting outputs used to generate the data found in the `data/` folder.

## Simulator Reference
This study utilizes the **Multi-Agent Non-Stochastic Economic Simulator** originally developed by Uwe Wolffgang.
* **Source Code:** [https://github.com/uwol/computational-economy](https://github.com/uwol/computational-economy)
* **Citation:** Wolffgang, U. (2015). *A Multi-Agent Non-Stochastic Economic Simulator* [Source Code]. GitHub.
