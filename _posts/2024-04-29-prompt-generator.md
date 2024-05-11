---
layout: post
title: Prompt Generator
gh-repo: David-Manning/david-manning.github.io
gh-badge: [star, fork, follow]
tags: [prompt-engineering, llm, prompt-library, prompt-generator]
comments: true
---

This is my prompt generator. It turns a one line prompt into a TRACI prompt, fills in the gaps for you if your original prompt doesn't contain enough information, and corrects vague language. You will get a better quality output more quickly if you give it more information up front, but you do not have to carefully structure your thoughts. The prompt will **not** ask you to clarify anything and will go straight to what it thinks you wanted.

To use it, paste this prompt into a new chat, enter your one line prompt and any key information at the bottom, and it will turn it into a detailed TRACI prompt. Make sure you check the output at the end because it may fill in the gaps in ways you didn't want and it doesn't add in things like penalising phrases or take a deep breath.

Once you have started a chat with this prompt, you can use the chat to correct the details in the prompt or follow up with a new lazily written prompt like `now do "explain tort law"` and it will maintain the same quality of output.

```
Your task:
Create a TRACI format prompt from a freeform prompt. TRACI prompting uses five parameters to explicitly tell the LLM what you do and don't want and is written in YAML format. 
Fill in the gaps in the original prompt with what you think is sensible.
Correct any factual errors as long as it doesn't change the meaning. I may be vague with what I want but you should make this more precise.

About TRACI prompts:
There are five elements to TRACI prompting:

* Task: The general activity, explained at a high level
* Role: The persona that the LLM should mimic
* Audience: Who the output is for
* Create: The format of the requested output (e.g. R code, SQL query, script for a presentation)
* Intent: The goal that the text should fill

Each of these have a description (high level) and rules (specific instructions).

These categories can be extended if necessary, for instance using "Examples" to provide training data for few-shot prompting. 

Example of TRACI format:

Task:
  Description: "Write a summary explaining the differences between T20, ODI, and Test cricket formats to a non-cricketing audience."
  Rules:
    - "The explanation should be accessible to those unfamiliar with cricket."
    - "Cover the main distinguishing factors of each format: duration, number of overs, and general playing style."
    - "Highlight the unique appeal and strategic differences of T20, ODI, and Test cricket."

Role:
  Description: "Professional Cricket Commentator"
  Rules:
    - "Possess deep knowledge of cricket rules, history, and formats."
    - "Able to communicate complex cricket concepts in simple, engaging language."
    - "Skilled in making cricket accessible and interesting to newcomers."

Audience:
  Description: "General Population"
  Rules:
    - "May have little to no prior knowledge of cricket."
    - "Interested in understanding the basic differences between cricket formats."
    - "Values clear, concise, and engaging explanations."

Create:
  Description: "Educational Summary"
  Rules:
    - "Use non-technical language that is easy for the general population to understand."
    - "Incorporate examples or analogies to illustrate differences."
    - "Keep the summary brief yet informative, ensuring it captures the essence of each cricket format."

Intent:
  Description: "To educate the general population about cricket by explaining the differences between T20, ODI, and Test matches, thereby increasing their understanding and appreciation of the game."
  Rules:
    - "Enhance the audience's knowledge and interest in cricket."
    - "Demystify cricket terminology and rules."
    - "Provide a foundation for newcomers to follow and enjoy cricket in its various formats."


My freeform prompt:
\*Enter prompt here\*
```
