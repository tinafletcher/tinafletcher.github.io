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
+ Sign up with a free account at huggingface.co; access to >1 million open source models
+ Use your Google account at gemini.google.com to access the free tier of Gemini
+ Create a free account at claude.ai to access the free tier of Claude
+ Try ChatGPT at chatgpt.com; can also create a free account for access to additional features
+ Any other free or paid LLM you happen to have access to

### Prompting Techniques
This is a very brief overview of some things you might want to include when writing a prompt. However, be aware that this is an entire field of academic research, so there is a LOT more nuance to consider than what I've described here.

| Technique | Description | Example usage |
|---|---|---|
| Role assignment | What perspective/persona you want the LLM to take on during your conversation | e.g. “You are an expert software tester”, “You are highly knowledgeable in security testing” |


### Sample Prompts

|Task|Sample prompt|
|---|---|
|Generating test case ideas|“You are an expert software tester. Your task is to generate a list of the top 5 most useful test cases to execute, where the application under test is a basic login page. Do not include any load testing scenarios. Use a concise tone, and it’s ok to use technical language where applicable. Output the 5 test cases as an unordered list, then in a separate section explain your reasoning for including each of the test cases in the list. An example test case might be to verify successful login with valid credentials. The top 5 test cases for a basic login page are:”|


