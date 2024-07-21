---
layout: post
title: Prompt Library - Formatting Tables as JSON
gh-repo: David-Manning/david-manning.github.io
gh-badge: [star, fork, follow]
tags: [prompt-engineering, llm, prompt-library, AI, chatbots, chatgpt, claude, json]
comments: true
---

I use this prompt to summarise online tables (e.g. from Wikipedia) into JSON format. These tables can be poorly structured or formatted, but the LLM will return a valid JSON so the table can be used in an analysis. 

Some notes:

* It is important to specify the elements you want as this may be interpreted differently for different entries e.g. the Green Party of England and Wales have co-leaders rather than single leaders, and this will cause a mismatch between different parties that make it hard to join when you come to use it.
* In principle, this should work for CSV output however I have found that LLMs are quite poor at generating CSV files and JSON is more reliable. For information on how to load JSON files, see [this](https://github.com/David-Manning/david-manning.github.io/blob/master/_posts/2024-07-01-loading-and-saving-different-data-types.md) post.
* Very large tables might only be partially included, in this case, typing "continue" will make it finish, redoing the row it ended on. They will need to be manually merged together.
* You may have some rows or columns that you don't need e.g. totals or percentages that you can work out later - include these in the relevant lists.
* This usually works out rows and columns for itself even if the table is printed in one line but it is best to check it.
* This can be used in the same chat by copying and pasting a new table without comment.
* This works well with fast models like Claude 3 Haiku. As long as it copies the text accurately, use the fastest/cheapest one available.

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
