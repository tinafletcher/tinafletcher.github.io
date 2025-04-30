---
layout: page
title: Guided Exploration: Applying AI to assist with software quality tasks
permalink: /exploreai/
---

![Looking out over Dinosaur Provincial Park](../images/dinosaur.jpg)

## Guided Exploration: Applying AI to assist with software quality tasks

### Introduction
+ Intro to speaker
+ Your goals
+ My goals

### Desired Takeaways
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
+ Sign up with a free account at <a href="https://www.huggingface.co">huggingface.co</a>; access to >1 million open source models
+ Use your Google account at <a href="https://www.gemini.google.com">gemini.google.com</a> to access the free tier of Gemini
+ Create a free account at <a href="https://www.claude.ai">claude.ai</a> to access the free tier of Claude
+ Try ChatGPT at <a href="https://www.chatgpt.com">chatgpt.com</a>; can also create a free account for access to additional features
+ Any other free or paid LLM you happen to have access to

### Prompting Techniques
This is a very brief overview of some things you might want to include when writing a prompt. However, be aware that prompt engineering is an entire field of academic research, so there is a LOT more nuance to consider than what I've described here.

NOTE: It's not mandatory to use all of these techniques in a single prompt. Sometimes, it’s easier to start simple and add parameters as needed.

ANOTHER NOTE: LLM prompts are not all that different than giving clear, detailed instructions to another human about a task to do.

| Technique | Description | Example usage |
|---|---|---|
| Role assignment | What perspective/persona you want the LLM to take on during your conversation | e.g. “You are an expert software tester”, “You are highly knowledgeable in security testing” |
| Goal setting | What you want the outcome of the interaction to be | e.g. “Generate only the most critical test cases”, “Generate all the test cases you can think of” |
| Context setting | General background information that will help focus the interaction | e.g. “...for an application that does XYZ”, “...for the application found at www.myapp.com”<br>Tip: Depending on your LLM and pricing tier, you may be able to upload files that are then used as context within the conversation. |
| Examples | Specific examples that help to illustrate what you're looking for | e.g. “consider languages such as French, Italian, and Spanish”, “an example of a performance test is having 1000 users access the web site at the same time”<br>Terminology tip: Providing no examples is called zero shot prompting, giving one example is called one shot prompting, and providing a handful of examples is called few shot prompting. |
| Style preferences | Specify behaviour and tone | e.g. “avoid technical language”, “use an informal tone” |
| Format preferences | Desired structure of the output | e.g. “provide a 1-2 line summary followed by a bulleted list of the key points”, “response should be in valid json format” |
| Controls or guard rails | Specify topics, phrases, etc that are prohibited | e.g. “do not include test cases that are related to invalid data”, “avoid any references to specific tools or libraries” |
| Reasoning preferences | Encourage structured thinking, if applicable | e.g. “think step-by-step”, “show your reasoning/logic when presenting solutions” |
| Final reinforcement | Repeat the key points or the overall goal of the interaction, especially if the prompt is long | e.g. “now provide the more detailed report - and remember, use only long-form paragraphs”, “the top 5 tests most likely to reveal important defects are:” |

### Sample Prompts

| Task | Sample prompt |
|---|---|
| Generating test case ideas | “You are an expert software tester. Your task is to generate a list of the top 5 most useful test cases to execute, where the application under test is a basic login page. Do not include any load testing scenarios. Use a concise tone, and it’s ok to use technical language where applicable. Output the 5 test cases as an unordered list, then in a separate section explain your reasoning for including each of the test cases in the list. An example test case might be to verify successful login with valid credentials. The top 5 test cases for a basic login page are:” |
| Creating synthetic test data | “You are knowledgeable about phone number formats used around the world. Your task is to generate a list of 25 potentially valid phone numbers that I could use when testing that my software application properly handles all possible variations of international phone numbers. Do not consider formats that incorporate an extension, such as in an office setting. Make sure to include some variations that have special characters such as dashes or brackets - for example, (519) 999-8888. For each phone number, provide a brief explanation of why it was included and what makes it unique or interesting compared to the others in the list. 25 potentially valid international phone numbers I could use while testing my software application are:” |
| Writing code for automated test cases | “You are skilled at writing test cases for software applications using the automated test framework Playwright. Write the code for an automated test that will navigate to a specified URL, locate the search field, enter a search string, execute the search, and then confirm that at least one result appeared on the page. Prefer the use of code that is easier to read and understand rather than the most concise solution possible, and include lots of comments in the code to explain what is happening at each stage.” |
| Performing risk analysis | “You are a member of a software development team that is about to start a project that involves refactoring a JavaScript code base to use Typescript. Your background is in software quality, and your task is to help the team identify risks in the project. What are some common issues that the team should be on the lookout for as they undertake this refactoring project? For example, are there specific classes of bugs that tend to be introduced when making the switch to Typescript? Using a concise tone, list 3 important risks that the team should consider developing mitigation plans for, along with some specific sample test cases that would help to identify potential bugs. Assume that non-technical things like tight timelines and insufficient resources are not significant risks for this project.” |
| Improving bug reports | “You are a software tester who has just discovered an important product defect. You recently submitted the following bug report, but you feel it has not been receiving the attention it deserves and you suspect it’s because your bug report (while concise and easy to interpret) has not made the overall impact and required next steps clear enough. Rewrite the bug report to include more details that better convey the widespread nature of the issue, and the potential user and company impact if the issue is not resolved in a timely manner. Do not modify any of the core details or scope already expressed in the original report; focus on clearer communication only.<br><br>The original bug report is as follows.<br><br>Product: E-commerce Platform<br>Version: 2.0.1<br>Component: Checkout<br>Severity: High<br>Priority: Urgent<br>Reported By: Tina Fletcher<br>Date: 2025-04-30<br>Environment: Staging (Ontario, Canada)<br>Steps: Checkout with Ontario shipping address.<br>Expected: 13% HST applied.<br>Actual: 5% tax applied.<br>Impact: Incorrect sales tax calculation (undercharging).<br>Attachment: Screenshot of incorrect tax.<br>Note: Ontario tax rate is incorrectly 5% instead of 13% HST. Requires immediate fix.<br><br>Now provide the updated version that better describes the impact, as described above:” |

### Run a sample prompt; discuss initial impressions

Run one or more of the sample prompts, using any LLM. (Can you identify the techniques being used within the prompts?)

What do you think of the results?
+ Good? Bad? Incomplete?
+ How does it compare to what you might have come up with on your own?

Send some follow up prompts to continue brainstorming/iterating towards an optimal response:
+ Ask the LLM if it can improve upon the response it provided (e.g. “what else...?”)
+ Ask the LLM to tweak a certain detail (e.g. “add/remove...”)
+ Ask the LLM to clarify something it mentioned in the response (e.g. “can you explain...”)

Debrief:
+ Did the follow up prompts provide any noticeable improvements?
+ What other techniques could you use to iterate towards a better response?

### Explore properties/characteristics of LLMs; group debrief

Now, explore some properties/quirks/capabilities of LLMs; use your tester brain!
+ Continue varying the instructions and parameters
+ Send the exact same prompt to the same LLM, multiple times
+ Send the exact same prompt to two different LLMs
+ Remove one or more of the components of the prompt
+ Change the order of the prompt components
+ Change the formatting or syntax of the prompt
+ Try reducing one of the sample prompts down to only a very basic instruction
+ See what happens if you provide conflicting information within a prompt
+ Ask the LLM how confident it is about its response to your prompt
+ Ask the LLM for advice about how to improve your prompt (or to write a completely new prompt)
+ Ask an LLM to compare two different responses to the same prompt (AI-as-a-judge; pairwise evaluation)
+ Ask an LLM to rate a response on a scale that you define (AI-as-a-judge; pointwise evaluation)
+ ...

Debrief: what interesting things did you observe?
+ Any techniques that seemed particularly effective or ineffective?
+ Anything that surprised you, in a good or bad way?
+ What other experiments would you do if you had more time?

### Conclusion; things to think about

Did we achieve the desired takeaways?
+ Attendees leave the session with at least one practical idea for how to start leveraging AI in their software quality tasks
+ Attendees’ imaginations have been sparked with additional AI use cases to continue exploring in the future

Things to think about
+ Security and privacy
+ Like any tool, there are trade offs
+ It’s a pretty cool time to be a tester; lots to explore related to evaluation of AI-based systems


