# Chapter 1: Introduction to Agents and Their World

## **Introduction to an agents?**
The **agent** isn’t a new concept in machine learning and artificial intelligence (AI). In reinforcement learning, for instance, the word agent denotes an active decision-making and learning intelligence. In other areas, the word **agent** aligns more with an automated application or software that does something on your behalf.

### **What is an Agent?**
An **agent** is an autonomus system that Perceives --> Think --> Acts.
**In AI (especially LLMs), an agent is:**
A program that uses a language model (like GPT) + tools + memory to solve tasks autonomously.

An *Agent* is a system that:
- Perceives its environment
- Reasons based on its perception
- Acts to achieve its goals

> "An intelligent assistant that can interact, learn, and act."

## There are four cases where a user may interact with a large language model (LLM):
- **Direct user interaction**<br>
- **Agent/assistant proxy**<br>
- **Agent/assistant**<br>
- **Autonomous agent**<br>

### **1. Direct user interaction**:<br>
- In direct user interaction, you talk directly to the language model (LLM) like ChatGPT, without any tools, memory, or autonomy.

- EXAMPLE:
>You → "Summarize this paragraph"  
>LLM → (Responds immediately based on prompt)

- No memory of past inputs
- No tool usage
- No planning or decision-making
>	Just Q&A → like a basic chatbot

### **2. Agent/Assistant Proxy?**
- This is a thin wrapper around the LLM that adds a basic interface or workflow (like a UI, or pre/post-processing), but still no real autonomy.
- It feels more like an agent, but it’s still:
   - Not making decisions on its own
   - Not planning or using memory/tools
   - Just formatting or slightly enhancing direct interaction
- Example:
- An app that reformats your prompts before sending to GPT
- Or adds a little pre-structured logic like:
>You → "Write me an email"
>Proxy → (Adds context like your name, job, etc.)
>→ Sends to LLM

> It’s not truly autonomous — it’s still a guided interaction.

### **3.What is an Agent / Assistant?**
- Now we’re talking real agents:
 - These are LLM-powered systems that can:
     - Use tools (APIs, search, calculator)
     - Maintain memory
     - Make decisions
     - Break tasks into subtasks
     - Loop or plan ahead

- Example:
 A research assistant agent that:
     - Searches Google Scholar
     - Summarizes key papers
     - Combines them into a report
     - Asks clarifying questions if needed
> This is a true AI Agent / Assistant with planning, tools, and autonomy.

## What is an Autonomous Agent?
- A fully self-governing AI agent that:
    - Operates without needing step-by-step instructions
    - Can decide what to do next
    - Can create subtasks, retry, revise, and even learn
- Example:
AutoGPT, AgentGPT, or CrewAI agents that<br>
    - You give them a goal (e.g., “Research top 5 stock strategies”)
    - They plan steps, gather info, summarize, and return result
    - They keep looping until the task is complete
> Autonomous agents run in a feedback loop until the objective is reached.


## TYPES OF AGENTS:
- **Single-Agent**
- **Multi-Agent**
- **1.Single-Agent**- demonstrates the use cases for a single flow of actions on an LLM using a single agent. For more complex problems, we often break agents into profiles or personas. Each agent profile is given a specific task and executes that task with specialized tools and knowledge.
- **2.Multi-Agent** - Multi-agent systems are agent profiles that work together in various configurations to solve a problem. Multi-agent system using three agents: a controller or proxy and two profile agents as workers controlled by the proxy. The coder profile on the left writes the code the user requests; on the right is a tester profile designed to write unit tests. These agents work and communicate together until they are happy with the code and then pass it on to the user.
##### SIMPLE TERM:
- Single agent handles single task at a time whereas multi agent handle multiple tasks in parallel.
- Multiple agents can also provide feedback and evaluation, reducing errors when completing assignments.

## **The five main components of a single-agent system**
   - **The agent profile and persona**
   - **Action and Tool Use**
   - **Memory and Knowledge**
   - **Reasoning and Evaluation**
   - **Planning and Feedback**
   
### **1. The agent profile and persona**:<br>
   - The persona—often called the system prompt —guides an agent to complete tasks, learn how to respond, and other nuances. It includes elements such as the background (e.g., coder, writer) and demographics, and it can be generated through methods such as handcrafting, LLM assistance, or data-driven techniques, including evolutionary algorithms.

#### **What it means:**
- The “personality” or role that the agent plays. It defines how the agent behaves, talks, and thinks.

    - Example:
        - You create an agent to act like a friendly teacher, or a strict editor, or a research expert.

**The profile includes:**

   - How it greets you

   - How detailed it is

   - What tone it uses (casual, professional, etc.)

> "You are a software engineer from Google interviewing me for a backend developer role."

### **2. Action and Tool Use**:<br>
   - The agents involving activities directed toward task completion or acquiring information. These actions can be categorized into task completion, exploration, and communication, with varying levels of effect on the agent’s environment and internal states. Actions can be generated manually, through memory recollection, or by following predefined plans, influencing the agent’s behavior and enhancing learning.
   
#### **What it means:**
   - Agents can do actions using external tools like:

        - Search engines

        - Calculators

        - Databases

        - APIs

        - File readers

- Example:

> “What is the current weather in Chennai?”

A normal LLM can’t answer live

But an agent with a weather API tool → calls the API → fetches real data → responds

 > So, tool use = actions the agent takes beyond just text.
 
 ### **3.Memory and Knowledge**:
   - Agents use knowledge and memory to annotate context with the most pertinent information while limiting the number of tokens used. Knowledge and memory structures can be unified, where both subsets follow a single structure or hybrid structure involving a mix of different retrieval forms. Knowledge and memory formats can vary widely from language (e.g., PDF documents) to databases (relational, object, or document) and embeddings, simplifying semantic similarity search through vector representations or even simple lists serving as agent memories.
   
#### **What it means:**
- Memory: The agent remembers past conversations or tasks.

- Knowledge: Stored facts or learned information it can use anytime.

- Example:
- You tell your agent:

>“My name is Thiru, and I’m learning agents.”

**20 minutes later:**

**“What did I tell you earlier?”**

> ✔ The agent says:
> “You said your name is Thiru and you’re learning agents.”

>Agents with memory feel more intelligent and personal.
>They also store long-term knowledge (like a mini brain).

### **4. Reasoning and Evaluation**
   - Research and practical applications have shown that LLMs/agents can effectively reason. Reasoning and evaluation systems annotate an agent’s workflow by providing an ability to think through problems and evaluate solutions.
 
#### What it means:
   - Agents don’t just guess — they think through a problem step by step.

**Reasoning**: Figuring out how to solve a task logically

**Evaluation**: Checking if the answer/result makes sense

- Example:

> “What’s the cheapest laptop for programming?”

-> An agent might:

   - Search 3-4 models

   - Compare specs, prices, reviews

   - Pick one and explain why

> That’s reasoning and evaluating.

### **5. Planning and Feedback**:
   - its role in organizing tasks to achieve higher-level goals. It can be categorized into these two approaches:

        - Planning without feedback —Autonomous agents make decisions independently.
        - Planning with feedback —Monitoring and modifying plans is based on various sources of input, including environmental changes and direct human feedback.

#### What it means:
**Planning**: Agent breaks big tasks into smaller steps

**Feedback**: Agent checks its own work, fixes mistakes, or asks you for help

- Example:

> “Write a report on AI in agriculture.”

- **The agent**:

    - Plans:

         - Find latest papers

         - Summarize findings

         - Create outline

         - Write report

- **Feedback**:

Checks if results are good

>    Asks: “Do you want more detail on deep learning in agriculture?”

>    This is what makes agents intelligent and flexible.

MERMAID FLOWCHART:



<img width="500" height="800" alt="Untitled diagram _ Mermaid Chart-2025-07-28-134709" src="https://github.com/user-attachments/assets/39ea743b-0033-46cf-949b-1e8cbf7e2c55" />





```python

```
