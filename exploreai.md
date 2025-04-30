---
layout: page
title: Guided Exploration: Applying AI to assist with software quality tasks
permalink: /exploreai/
---

![Looking out over Dinosaur Provincial Park](../images/dinosaur.jpg)

### Introduction
+ Intro to speaker
+ Your goals
+ My goals

### Official Takeaways
+ Leave this session with at least one practical idea for how to start leveraging AI in your software quality tasks
+ Your imagination has been sparked with additional AI use cases to continue exploring after the session

### Tasks and Tools

What software quality tasks could potentially be augmented with AI?
+ Generating test case ideas
+ Creating synthetic test data
+ Writing code for automated test cases
+ Performing risk analysis
+ Improving bug reports
+ What else?

LLMs you could use today:
+ Sign up with a free account at [huggingface.co](huggingface.co); access to >1 million open source models
+ Use your Google account at [gemini.google.com](gemini.google.com) to access the free tier of Gemini
+ Create a free account at [claude.ai](claude.ai) to access the free tier of Claude
+ Try ChatGPT at [chatgpt.com](chatgpt.com); can also create a free account for access to additional features
+ Any other free or paid LLM you happen to have access to

### Prompting Techniques
This is a very brief overview of some things you might want to include when writing a prompt. However, be aware that prompt engineering is an entire field of academic research, so there is a LOT more nuance to consider than what I've described here.

NOTE: It's not mandatory to use all of these techniques in a single prompt. Sometimes, it’s easier to start simple and add parameters as needed.
ANOTHER NOTE: LLM prompts are not all that different than giving clear, detailed instructions to another human about a task to do.

| Technique | Description | Example usage |
|---|---|---|
| Role assignment | What perspective/persona you want the LLM to take on during your conversation | e.g. “You are an expert software tester”, “You are highly knowledgeable in security testing” |
| Goal setting | What you want the outcome of the interaction to be | e.g. “Generate only the most critical test cases”, “Generate all the test cases you can think of” |
| Context setting | General background information that will help focus the interaction | e.g. “...for an application that does XYZ”, “...for the application found at www.myapp.com” (see TIP 1 below) |
| Examples | Specific examples that help to illustrate what you're looking for | e.g. “consider languages such as French, Italian, and Spanish”, “an example of a performance test is having 1000 users access the web site at the same time” |
| Style preferences | Specify behaviour and tone | e.g. “avoid technical language”, “use an informal tone” |
| Format preferences | Desired structure of the output | e.g. “provide a 1-2 line summary followed by a bulleted list of the key points”, “response should be in valid json format” |
| Controls or guard rails | Specify topics, phrases, etc that are prohibited | e.g. “do not include test cases that are related to invalid data”, “avoid any references to specific tools or libraries” |
| Reasoning preferences | Encourage structured thinking, if applicable | e.g. “think step-by-step”, “show your reasoning/logic when presenting solutions” |
| Final reinforcement | Repeat the key points or the overall goal of the interaction, especially if the prompt is long | e.g. “now provide the more detailed report - and remember, use only long-form paragraphs”, “the top 5 tests most likely to reveal important defects are:” |

TIP 1: Depending on your LLM and pricing tier, you may be able to upload files that are then used as context within the conversation.
TIP 2: Providing no examples is called zero shot prompting, giving one example is called one shot prompting, and providing a handful of examples is called few shot prompting.


### Sample Prompts

|Task|Sample prompt|
|---|---|
|Generating test case ideas|“You are an expert software tester. Your task is to generate a list of the top 5 most useful test cases to execute, where the application under test is a basic login page. Do not include any load testing scenarios. Use a concise tone, and it’s ok to use technical language where applicable. Output the 5 test cases as an unordered list, then in a separate section explain your reasoning for including each of the test cases in the list. An example test case might be to verify successful login with valid credentials. The top 5 test cases for a basic login page are:”|


