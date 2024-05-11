---
layout: post
title: Prompting Frameworks
gh-repo: David-Manning/david-manning.github.io
gh-badge: [star, fork, follow]
tags: [prompt-engineering, llm, prompt-library, TRACI, frameworks, chatgpt, claude]
comments: true
---

This post is about prompting frameworks, which give different structures to the prompts. This is a quick introduction to how I make LLMs produce very high quality and consistent output from LLMs for interaction and production.

## Basic Prompting

Basic prompts are simple prompts like `write a game of noughts and crosses in ruby` - they do not give much guidance to the model and do not always give the highest quality output or consistent output. I only use them for very basic questions like `write python code to do an inner join` but for serious applications, they tend to struggle. In the noughts and crosses example, ChatGPT will write code that doesn't even run and Claude will write code which does work but crashes if you enter a typo.

## Role-Based Prompting

We can extend these prompts by giving the LLM more information like which role it should take on. The noughts and crosses prompt above might become 
```
You are a senior software engineer. Write a game of noughts and crosses in ruby. Make sure it has proper error handling in case I enter the wrong command. The game will be between two human players using the same keyboard.
```

This prompt will work much better than before, but will not follow all instructions to the letter, which can make it hard to put these prompts into production. I tend not to use these sorts of prompts into production - they are more work than the one-line prompts above but do not have as good performance as TRACI prompts.

## TRACI Prompting

TRACI prompting is a framework which gives more clarity to the model and user. There are five elements, which are formatted in JSON or YAML with a description and rules for each:

* Task - what is actually to be done.
* Role - the role the LLM should follow.
* Audience - who the output is intended for.
* Create - what is actually to be created.
* Intent - what the output will be used for.

These can be extended to include things like `Example Data` for one shot or few shot prompting.

An example of TRACI prompting (using YAML) might be

```
Task:
  Description: "Write a Ruby program to create a playable game of Noughts and Crosses (Tic-Tac-Toe)."
  Rules:
    - "The program should allow two players to take turns placing their mark (nought or cross) on a 3x3 grid."
    - "The program should detect when a player has won or when the game ends in a draw."
    - "The program should display the game board after each turn."

Role:
  Description: "Experienced Ruby Developer"
  Rules:
    - "Possess strong knowledge of Ruby syntax and best practices."
    - "Able to design and implement a complete, functional game."
    - "Skilled in creating clear, efficient, and maintainable code."

Audience:
  Description: "Beginner Ruby Programmers"
  Rules:
    - "Familiar with basic Ruby syntax and concepts."
    - "Interested in learning how to build a simple game using Ruby."
    - "Values clear, well-commented code that demonstrates good programming practices."

Create:
  Description: "Ruby Script"
  Rules:
    - "Write the game as a standalone Ruby script that can be run from the command line."
    - "Use object-oriented programming principles to structure the code."
    - "Include comments to explain key parts of the code and improve readability."

Intent:
  Description: "To create a functional, interactive game of Noughts and Crosses using Ruby, demonstrating how to implement game logic, handle user input, and display output in a terminal-based application."
  Rules:
    - "Provide a practical example of building a game using Ruby."
    - "Demonstrate the use of loops, conditionals, and data structures in a real-world context."
    - "Inspire beginner Ruby programmers to create their own simple games and projects."
```

This prompt gives a very clear explanation of each element and what is to be done. This goes into much more detail about who the LLM should imitate, what exactly is required, who it is for and why.

Running this code gives very clear output with code that actually works properly. It can still hallucinate, so you should still check it, but 

In my experience, TRACI prompting tends to give more complete responses in prose and higher quality output in code. It is also a fantastic starting point for fully interactive chats or for creating a production quality prompt where you need output to be completely consistent.

## Examples

I asked Claude 3 Opus to explain the succession crisis of 1066 using three prompts. This is what it came up with:

### Basic Prompt

```
What happened in 1066?
```

```
In 1066, the Norman Conquest of England took place. This was a major event in English history that had far-reaching consequences. The key events of 1066 include:

In January, Edward the Confessor, King of England, died without a clear heir, leading to a succession crisis.
Harold Godwinson, a powerful English nobleman, was crowned king by the Witenagemot (the king's council).
William, Duke of Normandy, claimed that he had been promised the throne by Edward and that Harold had sworn allegiance to him.
In September, Harald Hardrada, King of Norway, invaded northern England but was defeated and killed by Harold Godwinson at the Battle of Stamford Bridge.
On September 28, William of Normandy invaded England, landing at Pevensey.
On October 14, the decisive Battle of Hastings was fought between Harold Godwinson and William of Normandy. Harold was killed in the battle, and the English army was defeated.
William was crowned King of England on Christmas Day 1066 in Westminster Abbey, becoming known as William the Conqueror.

The Norman Conquest marked the end of Anglo-Saxon rule in England and the beginning of a new era. It led to significant changes in English society, language, culture, and politics that have had a lasting impact to this day.
```

This is all true, but is a very basic outline of what happened, doesn't really say why the heir wasn't clear, what the three claims were, or what the impact was.

### Role-Based Prompt

```
You are a secondary school history teacher. Your job is to give a summary of the succession crisis of 1066 to a group of sixth-formers who are about to start learning about the Norman invasion for an A-level history exam. The primer should be enough to give them the overview to build on.
```

```
Hello everyone! As you prepare to start learning about the Norman invasion for your A-level history exam, it's important to understand the events leading up to it, particularly the succession crisis of 1066.
In January 1066, Edward the Confessor, the King of England, died without leaving a clear heir to the throne. This led to a power struggle among three main contenders:

Harold Godwinson, the powerful Earl of Wessex and Edward's brother-in-law, claimed that Edward had promised him the throne on his deathbed.
William, Duke of Normandy, also known as William the Conqueror, claimed that Edward had promised him the throne years earlier and that Harold had sworn allegiance to him.
Harald Hardrada, the King of Norway, claimed the throne based on a previous agreement between his predecessor and the earlier Danish King of England, Harthacnut.

In England, the Witan (the council of nobles) chose Harold Godwinson as the next king, and he was crowned shortly after Edward's death. However, both William and Hardrada refused to accept this decision and prepared to invade England to claim the throne by force.
In September 1066, Hardrada invaded England from the north, allied with Harold Godwinson's brother Tostig. Harold marched his army north and defeated Hardrada and Tostig at the Battle of Stamford Bridge on September 25th.
Meanwhile, William had been preparing his invasion from Normandy. He landed in southern England on September 28th, taking advantage of Harold's absence in the north. Harold rushed his army south to confront William, and the two forces met at the Battle of Hastings on October 14th, 1066.
In the ensuing battle, Harold was killed, and the English army was defeated. This victory marked the beginning of the Norman conquest of England, as William was crowned king on Christmas Day 1066, becoming known as William I of England.
The succession crisis and the events of 1066 had a profound impact on English history, leading to significant changes in the country's political, social, and cultural landscape under Norman rule.
```

This is much better - it actually says what the claims were and a gist of the battles. It doesn't say what happened later, but that may be because I told it to give something that can be built on and changing the prompt will refine this. 

### TRACI Prompt

```
Task:
  Description: "Provide a concise summary of the key historical events that occurred in the year 1066."
  Rules:
    - "Focus on the most significant events that had a lasting impact on English and European history."
    - "Include brief explanations of the causes and consequences of each event."
    - "Organize the events chronologically."

Role:
  Description: "Knowledgeable History Educator"
  Rules:
    - "Possess a deep understanding of medieval English and European history."
    - "Able to identify and explain the most important events of 1066."
    - "Skilled in presenting historical information in a clear, engaging manner."

Audience:
  Description: "General Audience Interested in History"
  Rules:
    - "May have a basic understanding of English history but not necessarily familiar with the specific events of 1066."
    - "Interested in learning about the key events and their significance."
    - "Values concise, informative explanations that are easy to understand."

Create:
  Description: "Historical Summary"
  Rules:
    - "Present the information in a clear, organized format, such as a list or short paragraphs."
    - "Use language that is accessible to a general audience, avoiding excessive jargon or assuming prior knowledge."
    - "Provide brief context where necessary to help the audience understand the significance of the events."

Intent:
  Description: "To educate the audience about the pivotal events of 1066, highlighting their importance in shaping English and European history and sparking interest in learning more about this period."
  Rules:
    - "Help the audience understand why the events of 1066 are considered a turning point in history."
    - "Encourage further exploration and learning about the Norman Conquest and its aftermath."
    - "Provide a foundation for understanding the long-term consequences of the events of 1066."
```

Returns:
```
Key Historical Events of 1066:

1. January 5th - Edward the Confessor, King of England, dies without a clear heir, leading to a succession crisis. Edward's brother-in-law, Harold Godwinson, is crowned king by the Witenagemot (the king's council).

2. September 25th - Battle of Stamford Bridge: King Harold Godwinson defeats his brother Tostig and Harald Hardrada, King of Norway, who had invaded northern England in an attempt to claim the English throne. This victory secures Harold's position as king but leaves his army weakened.

3. September 28th - William, Duke of Normandy, lands at Pevensey on the south coast of England with a large invasion force, claiming the English throne promised to him by Edward the Confessor.

4. October 14th - Battle of Hastings: King Harold Godwinson, having marched his army south, confronts William at Hastings. In a hard-fought battle, the Normans emerge victorious, and Harold is killed. This decisive Norman victory marks the beginning of the Norman Conquest of England.

5. December 25th - William the Conqueror is crowned King of England at Westminster Abbey, establishing Norman rule and ending Anglo-Saxon dominance. This event sets the stage for significant changes in English society, law, and language.

The events of 1066, particularly the Battle of Hastings and the Norman Conquest, had far-reaching consequences for England and Europe. The Norman victory led to the introduction of feudalism, the creation of the Domesday Book, and the development of English Common Law. It also marked the beginning of a new era of close ties between England and continental Europe, shaping the course of English and European history for centuries to come.
```

This summary is much better - there are specific dates, a clear explanation of what happened, and what the outcome was.
