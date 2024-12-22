# Setting The Stage

## 1. Why learn Agentic AI?

In Oct 2024, Gartner identified [Agentic AI](https://www.gartner.com/en/articles/intelligent-agent-in-ai) - or _AI with Agency_ - as a trend to watch, predicting that **33% of enterprise software apps will include agentic AI by 2028**, driving automation and workplace productivity. 

- The target characteristics are an ability to learn from its environment, create complex plans, and perform tasks autonomously.
- The opportunities are in AI-enabled _machine_ customers - ex: optimized decisions for automated transactions (goods and services exchange) based on preset rules.
- The challenges are in managing the risks of agentic AI - such as governance, trustworthiness (in decision-making), data quality, and smarter malware.

There are a growing number of tools and frameworks tackling the challenges and opportunities in this space. Here are the top 5 agent frameworks cited in the "Articles" below, with a link to a relevant Quickstart for each.

1. Microsoft AutoGen - [AgentChat](https://microsoft.github.io/autogen/0.4.0.dev11/user-guide/agentchat-user-guide/quickstart.html)
1. LangGraph - [Quickstart](https://langchain-ai.github.io/langgraph/tutorials/introduction/)
1. CrewAI - [Quickstart](https://docs.crewai.com/quickstart)
1. Semantic Kernel - [Quickstart](https://learn.microsoft.com/en-us/semantic-kernel/get-started/quick-start-guide?pivots=programming-language-python)
1. LangChain - [Build an Agent](https://python.langchain.com/docs/tutorials/agents/#installation)


??? info "**ARTICLES**: READ ABOUT TRENDS IN AGENTIC AI FOR 2025"

    - [Top 5 Frameworks for Building AI Agents in 2025](https://www.analyticsvidhya.com/blog/2024/07/ai-agent-frameworks/) 
    - [Top 3 Trending Agentic AI Frameworks](https://www.datagrom.com/data-science-machine-learning-ai-blog/langgraph-vs-autogen-vs-crewai-comparison-agentic-ai-frameworks)
    - [Gartner Top 10 Strategic Technology Trends for 2025](https://www.gartner.com/en/articles/top-technology-trends-2025)
    - [McKinsey: Why agents are the next frontier of generative AI](https://www.mckinsey.com/capabilities/mckinsey-digital/our-insights/why-agents-are-the-next-frontier-of-generative-ai)
    - [The Next “Next Big Thing”: Agentic AI’s Opportunities and Risks](https://scet.berkeley.edu/the-next-next-big-thing-agentic-ais-opportunities-and-risks/) - UC Berkeley

Two of these options - **Semantic Kernel and AutoGen** - are open-source projects from Microsoft. While these are frameworks for _development_, building enterprise applications requires _services_ that can help us manage and secure these solutions in production. This is where the [Azure AI Agent Service](https://learn.microsoft.com/en-us/azure/ai-services/agents/overview) come in, helping us **streamline** the end-to-end development workflow for agentic AI applications in the [Azure AI Foundry](https://ai.azure.com) platform. Let's set the stage with some definitions.


---

## 2. What is an AI Agent?

[In Azure AI Foundry](https://learn.microsoft.com/en-us/azure/ai-services/agents/overview#what-is-an-ai-agent) an AI Agent is a _smart microservice_ that can be used to answer questions (RAG), perform actions (Tasks) or automate workflows (E2E). It does this **by combining the power of generative AI models with tools that enable access and interaction with real-world data sources**.

[In AutoGen](https://microsoft.github.io/autogen/0.4.0.dev11/user-guide/agentchat-user-guide/quickstart.html) an Agent is an entity that helps us define **what actions are taken when a message is received** while a Team defines **rules for how agents interact with each other**. The [AssistantAgent](https://microsoft.github.io/autogen/0.4.0.dev11/reference/python/autogen_agentchat.agents.html#autogen_agentchat.agents.AssistantAgent) preset is an agent that **has access to a model (LLM) and tools (functions) that it can use to address the specified task**.

[In Semantic Kernel Agent Framework](https://learn.microsoft.com/en-us/semantic-kernel/frameworks/agent/?pivots=programming-language-csharp#what-is-an-ai-agent) an AI agent is a software entity designed **to perform tasks autonomously or semi-autonomously by recieving input, processing information, and taking actions to achieve specific goals.** Agents can send and receive messages, generating responses using a combination of models, tools, human inputs, or other customizable components. Agents are designed to work collaboratively, enabling complex workflows by interacting with each other. 

---

## 3. The Azure AI Agent Service

[By definition](https://learn.microsoft.com/en-us/azure/ai-services/agents/overview), it is a **fully-managed service designed to empower developers to securely build, deploy, and scale high-quality, and extensible AI agents**. Leveraging an extensive ecosystem of models, tools and capabilities from OpenAI, Microsoft, and third-party providers, Azure AI Agent Service enables building agents for a wide range of generative AI use cases. [Client-side function calling](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/function-calling) which was previously complex to implement - is now just a few lines of code.


It has the following features:

- [x] Enterprise-grade security
- [x] Rapid development & automation
- [x] Extensive data connections
- [x] Flexible Model Selection
- [x] Uses same wire protocol as [Azure OpenAI Assistants](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/assistant)

**Quickstart:** Create a new agent with the [Azure SDK](https://learn.microsoft.com/en-us/azure/ai-services/agents/quickstart?pivots=programming-language-python-azure) or the [OpenAI SDK](https://learn.microsoft.com/en-us/azure/ai-services/agents/quickstart?pivots=programming-language-python-openai).


---

## 4.The AutoGen Framework

[By definition](https://github.com/microsoft/autogen), AutoGen is an open-source framework for building AI agent systems. It simplifies the creation of event-driven, distributed, scalable, and resilient agentic applications. It allows you to quickly build systems where AI agents collaborate and perform tasks autonomously or with human oversight.

In Oct 2024, the team released [AutoGen 0.4](https://microsoft.github.io/autogen/dev) a from-the-ground-up rewrite in response to developer and community feedback. This version _embraces the actor model of computing to support distributed, highly scalable, event-driven agentic systems_ - with features like composability, flexibility, debugging & observability, and scalability. The project also moved away from a single monolithic library, to a [multi-library solution](https://microsoft.github.io/autogen/0.2/blog/) with three packages:

- **Core** - the building blocks for agentic AI
- **AgentChat** - a task-driven high-level API with group chat, code exection, prebuilt agents
- **Extensions** - core interfaces and third-party integrations for expansion.

**Quickstart:** Create a new [AgentChat](https://microsoft.github.io/autogen/0.4.0.dev11/user-guide/agentchat-user-guide/quickstart.html) app or explore [Core](https://microsoft.github.io/autogen/0.4.0.dev11/user-guide/core-user-guide/quickstart.html) building blocks.

---

## 5. The Semantic Kernel Project

Semantic Kernel is a lightweight, open-source development kit that lets you easily build AI agents and integrate the latest AI models into your C#, Python, or Java codebase. It serves as an efficient middleware that enables rapid delivery of enterprise-grade solutions.

**Quickstart:** Create a new agentic app with [Python](https://learn.microsoft.com/en-us/semantic-kernel/get-started/, [C#](https://learn.microsoft.com/en-us/semantic-kernel/get-started/quick-start-guide?pivots=programming-language-csharp) or [Java](https://learn.microsoft.com/en-us/semantic-kernel/get-started/quick-start-guide?pivots=programming-language-java).


### 5.1 The Agent Framework

An AI agent is a software entity designed to perform tasks autonomously or semi-autonomously by recieving input, processing information, and taking actions to achieve specific goals. Agents can send and receive messages, generating responses using a combination of models, tools, human inputs, or other customizable components.

The [Semantic Kernel Agent Framework](https://learn.microsoft.com/en-us/semantic-kernel/frameworks/agent/?pivots=programming-language-csharp) provides a platform within the Semantic Kernel eco-system that allow for the creation of AI agents and the ability to incorporate agentic patterns into any application based on the same patterns and features that exist in the core Semantic Kernel framework.


### 5.2 The Process Framework
A Process is a structured sequence of activities or tasks that deliver a service or product, adding value in alignment with specific business goals for customers.

The [Semantic Kernel Process Framework](https://learn.microsoft.com/en-us/semantic-kernel/frameworks/process/process-framework) is a cutting-edge approach designed to optimize AI integration with your business processes. This framework empowers developers to efficiently create, manage, and deploy business processes while leveraging the powerful capabilities of AI, alongside your existing code and systems.

---

_This is a **#NityaLearnsAI** project - learn [about me](./About-Me/), then explore [resources](./Resources/) to learn AI!_