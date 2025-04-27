# AI Coding
AI assisted software development is growing rapidly on the back of the AI development race. 
Companys like Anthropic, Deepseek, Google, Microsoft, Meta, OpenAI,  and xAI etc. have spent millions developing software systems for ML: Machine Learning, NLP: Natural Language Processing, RPA: Robotic Process Automation, LLM: Large Language Models and applications to use them. 

Tools based on these generative and agentic AI technologies enable developers to investigate and create large amounts of code.

It also enables non-developers like me to implement software libraries without writing code from scratch.

This is not without its controversy due to the quality of the software produced by non-developers.

The fact is that it is early days for the ecosystem of tools around AI assisted coding and it is improving rapidly.

The term "vibe coding" has been used to label the process of producing software from natural language prompts without technical knowledge.


Tools include:
Augment, Bolt, Claude Code, Replit, Cursor, GitHub Copilot, Warp, Windsurf.

These implement some version of features that enable AI assisted code generation:

- Auto complete
- Console interaction
- Code repository interaction
- Code interrogation
- Code refactoring
- Context awareness
- Image interpretation
- Documentation generation
- Automated testing
- Task management

MCP



--

https://www.cursor.com/

https://jssip.net/


--

https://www.augmentcode.com/

https://app.augmentcode.com/your-usage?yourUsageFilter=30


https://www.swebench.com/

https://github.com/augmentcode/augment-swebench-agent

(SCREENSHOTS)

--

Using Augment Code I was able to create [Phone - Chrome Extension SIP Client](https://github.com/Vince-0/webrtc-chrome)

I included a [.augment](https://github.com/Vince-0/webrtc-chrome/tree/8f00e5f462bedeb7271dbe8a935ecbc9ce129520/.augment) folder in the project root directory to direct Augment Code behavior.

Together with "Agent" mode chat prompts like:




I would still have to often prompt for instructions like, update the README, the current checkpoint is in fact, ask any questions to elaborate and clarify implemenation.

--


https://github.com/Vince-0/webrtc-chrome/blob/8f00e5f462bedeb7271dbe8a935ecbc9ce129520/.augment/augment-README

--

Read and implement the augment-guidelines, ask any questions that elaborate and clarify these guidelines

https://github.com/Vince-0/webrtc-chrome/blob/8f00e5f462bedeb7271dbe8a935ecbc9ce129520/.augment/augment-guidelines

WORKFLOW: Use these guidelines to update your remember rules

WORKFLOW: Use the augment/augment-tasklist as a task list to read COMPLETE, PENDING, and NEW tasks with associated categories for example: UX. I will update the task list as needed.

WORKFLOW: Copy all of the Augment chat history output into the augment/augment-chathistory file at the end of every chat interaction in an append only fashion. There is no need to read the entire chat history unless instructed to. 

WORKFLOW: Include all checkpoint numbers so that it can be referred to easily from the augment-tasklist file in the CHECKPOINT: tag at the end of every task description.

WORKFLOW: Number each set of code changes in the chat history exactly like checkpoints numbering so that we can refer to them in the augment/augment-tasklist file, for example: UX:Task description and instructions:CHECKPOINT:1,4,6,10.

WORKFLOW: Append to the augment/augment-chathistory file the Augment platform statistics usage such as: Total user chat messages,Total user agent requests, Total user agent tool uses.

WORKFLOW: Update augment/augment-README file so it explains the project features, directory structure, prerequisites, installation, configuration details, usage, key files and key functions after each code change. Include any information that could be useful for users,developers and LLMs/AI to understand the project enough to be able to start developing it by just reading the README file.

WORKFLOW: Ask any questions about implementing features from tasks that could elaborate and clarify the task

WORKFLOW: Suggest any changes to the code files and folder structure to better separate code into logical boundaries that help create better maintenance, good coding practices and file separation.

--

https://github.com/Vince-0/webrtc-chrome/blob/8f00e5f462bedeb7271dbe8a935ecbc9ce129520/.augment/augment-tasklist

#STATUS:COMPLETE:


#STATUS:PENDING:
WORKFLOW: Read the files in the .augment folder: augment-guidlienes, augment-tasklist. Explain what you understand about the guidelines for the workflow for this project.:CHECKPOINT:1

#STATUS:NEW:
INFRA: 
BUG

#STATUS: PARKED:

#STATUS: BROKEN:


--

Record our chat history in this file:

https://github.com/Vince-0/webrtc-chrome/blob/8f00e5f462bedeb7271dbe8a935ecbc9ce129520/.augment/augment-chathistory

https://github.com/Vince-0/webrtc-chrome/blob/8f00e5f462bedeb7271dbe8a935ecbc9ce129520/.augment/augment-chathistory1


Statistics

- Total user chat messages: 3

- Total user agent requests: 1

- Total user agent tool uses: 10






