# AI Coding
AI assisted software development is growing rapidly on the back of the AI development race. 
Companys like Anthropic, Deepseek, Google, Microsoft, Meta, OpenAI and xAI etc. have spent millions developing software systems and applications to use them:

- LLM: Large Language Models 
- ML: Machine Learning
- NLP: Natural Language Processing
- RPA: Robotic Process Automation

Tools based on these generative and agentic AI technologies enable developers to investigate and create large amounts of code.

It also enables non-developers like me to implement software libraries without writing code from scratch.

This is not without its controversy due to the quality of the software produced by non-developers.

The fact is that it is early days for the ecosystem of tools around AI assisted coding and it is improving rapidly. 

There is definitely value to be made, even if it is for producing proof of concept projects for non-coders through to advanced system architectures for software developers.

The term "vibe coding" has been used to label the process of producing software from natural language prompts without technical knowledge.

<p align="center" >
<img src="https://github.com/Vince-0/AI_Coding/blob/054a43c4b84a3a96584ee65dc6f818f99bdeff90/pictures/trends_vibecoding.png" />
</p>

AI assisted coding tools include:
Augment, Bolt, ChatGPT, Claude, Cursor, Replit, GitHub Copilot, Warp, Windsurf etc.

These implement some version of features that enable AI assisted code generation and development automation inlcuding:

- [Agent2Agent Protocol](https://developers.googleblog.com/en/a2a-a-new-era-of-agent-interoperability/)
- Auto complete
- Automated testing
- Console interaction
- Code repository interaction, interrogation, refactoring
- Computer Vision
- Context awareness
- Document,image generation
- [Model Context Protocol](http://anthropic.com/news/model-context-protocol)
- Task management

The tools below helped me create some of these projects:

- [MSTeams FreePBX](https://github.com/Vince-0/MSTeams-FreePBX)
- [Log Parser](https://github.com/Vince-0/Log-parser)
- [WebRTC Server](https://github.com/Vince-0/FreeSWITCH_WEBRTC) 
- [WebRTC Client](https://github.com/Vince-0/WebRTC_client)
- [Phone - Chrome Extension SIP Client](https://github.com/Vince-0/webrtc-chrome)

---
## ChatGPT
Most people know OpenAI's [ChatGPT](https://chatgpt.com/) as an AI chat application to ask questions and do image generation.

I used it a while ago for basic:
- Document writing elaboration (9/10)
- BASH, Python script writing (8/10)
- Elaborate spreadsheet formula generation (8/10)
- Diagram generation (2/10)
- Frog cartoons (6/10)

<p align="center">
<img src="https://github.com/Vince-0/AI_Coding/blob/7694110e21855b26cf491555abb2b6cf931e36c7/pictures/frog.jpg" />
</p>

---
## Claude

Anthropic's [Claude](https://claude.ai/) was puported to be better at Python coding so I tried it next and elaborated on Python scripts. 

I used Claude for basic Python:
- Input and output example data (10/10)
- Basic API interaction (10/10)
- Libraries for image manipulation (10/10)

However, after adding Javascript libraries for SIP, the context size was quickly maxed out and became unusable.

---
## Cursor IDE

First I tried [Cursor](https://www.cursor.com/) because it was a prominent IDE with a 14 day trail 500 premium credits (thereafter 50/day) and smaller model usage.

<p align="center">
<img src="https://github.com/Vince-0/AI_Coding/blob/9c0af4d6236bd06cdfbf6bc437b89aa2316c52cc/pictures/cursor_settings.png" />
</p>

Forked from [VS Code](https://code.visualstudio.com/), there are various [chat modes](https://docs.cursor.com/chat/overview) and [model selections](https://docs.cursor.com/chat/overview#model-selection).

<p align="center">
<img src="https://github.com/Vince-0/AI_Coding/blob/be534f9cdcaaf4cb15568d2d6753924f8de876ba/pictures/cursor_chat_models.jpg" />
</p>

It went something like this:
- "Create a JsSIP client"
- Work around OS ExecutionPolicy problem for console running a Node web server
- Feed back code deprecated, function, reference, type, local/CDN library and version errors
- Stopped at unpassable hurdles implementing JsSIP with compatible codecs
- Use SIP.js instead
- 14 day trial expired

---

## Augment Code

[Augment Code](https://www.augmentcode.com/) had the highest verified [SWE-bench](https://www.swebench.com/) scores and I was impressed how it produced smart and high quality  responses from its context engine.

<p align="center">
<img src="https://github.com/Vince-0/AI_Coding/blob/96961a64d87fe5d9eddc75608dbe42df2a02e652/pictures/augment_swebench.jpg" />
</p>

<p align="center">
<img src="https://github.com/Vince-0/AI_Coding/blob/cfdb147db685bcd012d9daf92bbf2710b0205a3b/pictures/augment_app1.png" />
</p>

Augment Code comes in extensions for:
- [VS Code](https://marketplace.visualstudio.com/items?itemName=augment.vscode-augment)
- Vim, Neovim
- JetBrains
  
Much like Cursor, it indexes your code and enables you to ask questions and make changes using natural language prompts. 

Using Augment Code [Agent mode](https://docs.augmentcode.com/using-augment/agent), model selection [isn't an option](https://www.augmentcode.com/blog/ai-model-pickers-are-a-design-failure-not-a-feature).

It used a documentation retrieval function to investigate implementing SIP.js. 

Checkpoints in the agent chat allow you to revert all changes back to a numbered point in chat history. 

The memories function creates rules to remember when you correct it on workflow preferences etc. This is editable.

<p align="center">
<img src="https://github.com/Vince-0/AI_Coding/blob/09caefe7f462d2ed0e3abee09013a22c5cc7ba4b/pictures/augment_memories.jpg" />
</p>


### Augment Code Tricks

I included a [.augment](https://github.com/Vince-0/webrtc-chrome/tree/8f00e5f462bedeb7271dbe8a935ecbc9ce129520/.augment) folder in the project root directory to direct chat behavior. 

Even with guidelines I found that I still had to prompt regularly for:

- Correct checkpoint numbering because it isn't a variable that is available to the chat context and often falls behind increments.
- Use the task list correctly by updating just the checkpoint numbering and not the statuses or sections.
- Update the README.

#### Guidelines
User and workspace [guidelines](https://docs.augmentcode.com/setup-augment/guidelines) are supposed to be implemented in a file in the root directory of the project.

I want them in my .augment folder [file](https://github.com/Vince-0/webrtc-chrome/blob/8f00e5f462bedeb7271dbe8a935ecbc9ce129520/.augment/augment-guidelines) and prompted.

Prompt: "Read and implement the augment-guidelines, ask any questions that elaborate and clarify these guidelines"

```
WORKFLOW: Use these guidelines to update your remember rules

WORKFLOW: Use the augment/augment-tasklist as a task list to read COMPLETE, PENDING, and NEW tasks with associated categories for example: UX. I will update the task list as needed.

WORKFLOW: Copy all of the Augment chat history output into the augment/augment-chathistory file at the end of every chat interaction in an append only fashion. There is no need to read the entire chat history unless instructed to. 

WORKFLOW: Number each set of code changes in the chat history exactly like checkpoints numbering so that we can refer to them in the augment/augment-tasklist file, for example: UX:Task description and instructions:CHECKPOINT:1,4,6,10.

WORKFLOW: Append to the augment/augment-chathistory file the Augment platform statistics usage such as: Total user chat messages,Total user agent requests, Total user agent tool uses.

WORKFLOW: Update augment/augment-README file so it explains the project features, directory structure, prerequisites, installation, configuration details, usage, key files and key functions after each code change. Include any information that could be useful for users,developers and LLMs/AI to understand the project enough to be able to start developing it by just reading the README file.

WORKFLOW: Ask any questions about implementing features from tasks that could elaborate and clarify the task

WORKFLOW: Suggest any changes to the code files and folder structure to better separate code into logical boundaries that help create better maintenance, good coding practices and file separation.
```

#### Tasklist

I want the agent to work against a task list with some statuses that I manage and keep notes on using this guideline:
```
WORKFLOW: Use the augment/augment-tasklist as a task list to read COMPLETE, PENDING, and NEW tasks with associated categories for example: UX. I will update the task list as needed.
```


[augment-tasklist](https://github.com/Vince-0/webrtc-chrome/blob/8f00e5f462bedeb7271dbe8a935ecbc9ce129520/.augment/augment-tasklist)

```
#STATUS:COMPLETE:

#STATUS:PENDING:
WORKFLOW: Read the files in the .augment folder: augment-guidlienes, augment-tasklist. Explain what you understand about the guidelines for the workflow for this project.:CHECKPOINT:1

#STATUS:NEW:
INFRA: 
BUG

#STATUS: PARKED:

#STATUS: BROKEN:
```

#### Chat history

A chat history file could help create context data, track checkpoints help troubleshooting especially when moving projects between tools using this guideline:
```
WORKFLOW: Append to the augment/augment-chathistory file the Augment platform statistics usage such as: Total user chat messages,Total user agent requests, Total user agent tool uses.
```

[augment-chathistory](https://github.com/Vince-0/webrtc-chrome/blob/8f00e5f462bedeb7271dbe8a935ecbc9ce129520/.augment/augment-chathistory)


Chat history sections:
```
## CHECKPOINT: [#]

### User

### Assistant

## Planning


## Statistics
Total user chat messages: #
Total user agent requests: #
Total user agent tool uses: #
```

#### README

A README file could help create more context data and be used to produce user README documentation using this guideline:

```
WORKFLOW: Update augment/augment-README file so it explains the project features, directory structure, prerequisites, installation, configuration details, usage, key files and key functions after each code change. Include any information that could be useful for users,developers and LLMs/AI to understand the project enough to be able to start developing it by just reading the README file.
```

[README](https://github.com/Vince-0/webrtc-chrome/blob/8f00e5f462bedeb7271dbe8a935ecbc9ce129520/.augment/augment-README)


Usage looked like this for [Phone - Chrome Extension SIP Client](https://github.com/Vince-0/webrtc-chrome):
<p align="center">
<img src="https://github.com/Vince-0/AI_Coding/blob/cfdb147db685bcd012d9daf92bbf2710b0205a3b/pictures/augment_usage.png" />
</p>

This statistic page seems to have since been removed.

Augment Code has since released a new pricing structure on their Discord that will soon be implemented

<p align="center">
<img src="https://github.com/Vince-0/AI_Coding/blob/cfdb147db685bcd012d9daf92bbf2710b0205a3b/pictures/augmentcode_new_pricing_table.png" />
</p>

---

(Written without AI assistance)
