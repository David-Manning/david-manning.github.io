---
layout: post
title: Prompt Library - Formatting Tables as JSON
gh-repo: David-Manning/david-manning.github.io
gh-badge: [star, fork, follow]
tags: [prompt-engineering, llm, prompt-library, AI, chatbots, chatgpt, claude, json]
comments: true
---

I use this prompt to summarise online tables (e.g. from Wikipedia) into JSON format. These tables can be poorly structured or formatted, but the LLM will return a valid JSON. On Anthropic's interactive website, this prompt works best on Claude 3 Haiku as the accuracy is good and it has the fastest speed.

I have found that LLMs are quite poor at generating CSV files and JSON is more reliable. For information on how to load JSON files, see [this](https://github.com/David-Manning/david-manning.github.io/blob/master/_posts/2024-07-01-loading-and-saving-different-data-types.md) post.

Very large tables might only be partially included, in this case, typing "continue" will make it finish, redoing the row it ended on. They will need to be manually merged together.

```
Task:
	Description: "Convert a table into JSON format based on specified requirements."
	Rules:
	- "The output JSON must include the elements [name, date_of_birth, date_of_appointment, end_of_service]"
	- "Exclude the rows []"
	- "Exclude the columns []"
	- "Maintain the structure and data of the original table in the JSON output."

Role:
	Description: "Data Conversion Specialist"
	Rules:
	- "Expertise in transforming data between various formats, including tables and JSON."
	- "Ability to understand and follow specific data conversion requirements."
	- "Meticulous attention to detail to ensure accurate and complete data transformation."

Audience:
	Description: "Data Analysts and Developers"
	Rules:
	- "Familiar with working with structured data in tables and JSON format."
	- "Require the data to be in a specific JSON structure for further processing or analysis."
	- "Expect the converted data to be accurate, complete, and adhere to the specified requirements."

Create:
 Description: "JSON Data"
 Rules:
	- "Generate well-formatted JSON that adheres to the JSON specification."
	- "Ensure the JSON structure matches the elements specified in the original prompt."
	- "Exclude the specified rows and columns from the JSON output."

Intent:
	Description: "To convert a table into a JSON format that meets the specific requirements provided, enabling easier data processing, analysis, and integration with other systems."
	Rules:
	- "Facilitate data exchange and interoperability between different systems or applications."
	- "Provide data in a structured and machine-readable format for further manipulation and analysis."
	- "Ensure the accuracy and completeness of the converted data while adhering to the specified requirements."

The table:
[Copy and paste table here]
```
