# Agentic AI & Azure

## Learning Objectives

By the end of my learning journey, I want to be able to:

- Describe what AI Agents are - with examples.
- Create a new AI Agent - using different technologies.
- Validate my AI Agent - using different tools & SDKs.
- Orchestrate multi-agent workflows - for a target scenario.
- Ideate, Evaluate, and Operationalize - an agentic AI solution on Azure.

The starting point for my journey will be technologies that are built-in or supported by the Azure AI Foundry platform. However, the goal is to continue expanding to explore open-source and third-party frameworks for agentic AI, to see how I can mix-and-match tools and capabilities to achieve optimal outcomes. **Let's start with definitions**.

## What is an AI Agent?

[In Azure AI Foundry](https://learn.microsoft.com/en-us/azure/ai-services/agents/overview#what-is-an-ai-agent) an AI Agent is a _smart microservice_ that can be used to answer questions (RAG), perform actions (Tasks) or automate workflows (E2E). It does this **by combining the power of generative AI models with tools that enable access and interaction with real-world data sources**.

[In AutoGen](https://microsoft.github.io/autogen/0.4.0.dev11/user-guide/agentchat-user-guide/quickstart.html) an Agent is an entity that helps us define **what actions are taken when a message is received** while a Team defines **rules for how agents interact with each other**. The [AssistantAgent](https://microsoft.github.io/autogen/0.4.0.dev11/reference/python/autogen_agentchat.agents.html#autogen_agentchat.agents.AssistantAgent) preset is an agent that **has access to a model (LLM) and tools (functions) that it can use to address the specified task**.

[In Semantic Kernel Agent Framework](https://learn.microsoft.com/en-us/semantic-kernel/frameworks/agent/?pivots=programming-language-csharp#what-is-an-ai-agent) an AI agent is a software entity designed **to perform tasks autonomously or semi-autonomously by recieving input, processing information, and taking actions to achieve specific goals.** Agents can send and receive messages, generating responses using a combination of models, tools, human inputs, or other customizable components. Agents are designed to work collaboratively, enabling complex workflows by interacting with each other. 

---

## What is the Azure Agent Service?

[By definition](https://learn.microsoft.com/en-us/azure/ai-services/agents/overview), it is a **fully-managed service designed to empower developers to securely build, deploy, and scale high-quality, and extensible AI agents**. Leveraging an extensive ecosystem of models, tools and capabilities from OpenAI, Microsoft, and third-party providers, Azure AI Agent Service enables building agents for a wide range of generative AI use cases. [Client-side function calling](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/function-calling) which was previously complex to implement - is now just a few lines of code.


It has the following features:

- Enterprise-grade security
- Rapid development & automation
- Extensive data connections
- Flexible Model Selection
- Uses same wire protocol as [Azure OpenAI Assistants](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/assistant)

**Quickstart:** Create a new agent

- [Azure SDK](https://learn.microsoft.com/en-us/azure/ai-services/agents/quickstart?pivots=programming-language-python-azure) (Python)
- [OpenAI SDK](https://learn.microsoft.com/en-us/azure/ai-services/agents/quickstart?pivots=programming-language-python-openai) (Python)


---

## What is AutoGen?


[By definition](https://github.com/microsoft/autogen), AutoGen is an open-source framework for building AI agent systems. It simplifies the creation of event-driven, distributed, scalable, and resilient agentic applications. It allows you to quickly build systems where AI agents collaborate and perform tasks autonomously or with human oversight.

In Oct 2024, the team released [AutoGen 0.4](https://microsoft.github.io/autogen/dev) a from-the-ground-up rewrite in response to developer and community feedback. This version _embraces the actor model of computing to support distributed, highly scalable, event-driven agentic systems_ - with features like composability, flexibility, debugging & observability, and scalability. The project also moved away from a single monolithic library, to 

---

## What is Semantic Kernel?

---

## Where can I learn more?

[Markmaps](https://markmap.js.org/) are a great way to get the big picture of the documentation set for any technology. Check out the markmaps for the [Azure AI Agent Service](https://learn.microsoft.com/azure/ai-services/agents/), [Semantic Kernel](https://learn.microsoft.com/semantic-kernel/overview/) and [AutoGen](https://microsoft.github.io/autogen/0.4.0.dev11/index.html) below - and check back regularly for updates. **Tip**: You can click any node (circle) to collapse/expand the subtree for clarity.


??? tip "1. Azure AI Agents Documentation "

    ```markmap
    # [Azure AI Agent Service](https://learn.microsoft.com/en-us/azure/ai-services/agents/)

    ## Overview

    ### [What is Azure AI Agent Service ✨ ](https://learn.microsoft.com/en-us/azure/ai-services/agents/overview)

    ### [Quotas and Limits ✨](https://learn.microsoft.com/en-us/azure/ai-services/agents/quotas-limits)

    ### [Model and Region Support ✨ ](https://learn.microsoft.com/en-us/azure/ai-services/agents/concepts/model-region-support)

    ### [Pricing](https://azure.microsoft.com/pricing/details/ai-studio/)

    ### [What's New ✨ ](https://learn.microsoft.com/en-us/azure/ai-services/agents/whats-new)

    ### [FAQ](https://learn.microsoft.com/en-us/azure/ai-services/agents/faq)

    ## [Quickstart ✨ ](https://learn.microsoft.com/en-us/azure/ai-services/agents/quickstart)

    ## Concepts

    ### [Agents](https://learn.microsoft.com/en-us/azure/ai-services/agents/concepts/agents)

    ### [Tracing with Application Insights](https://learn.microsoft.com/en-us/azure/ai-services/agents/concepts/tracing)

    ## How-To
    ### [Tools](https://learn.microsoft.com/en-us/azure/ai-services/agents/how-to/tools/overview)
    #### [Overview](https://learn.microsoft.com/en-us/azure/ai-services/agents/how-to/tools/overview)
    #### Knowledge Tools
    ##### [Grounding With Bing Search](https://learn.microsoft.com/en-us/azure/ai-services/agents/how-to/tools/bing-grounding)
    ##### [File Search](https://learn.microsoft.com/en-us/azure/ai-services/agents/how-to/tools/file-search)
    ##### [Azure AI Search](https://learn.microsoft.com/en-us/azure/ai-services/agents/how-to/tools/azure-ai-search)
    #### Action Tools
    ##### [Function calling](https://learn.microsoft.com/en-us/azure/ai-services/agents/how-to/tools/function-calling)
    ##### [Code interpreter](https://learn.microsoft.com/en-us/azure/ai-services/agents/how-to/tools/code-interpreter)
    ##### [Use OpenAI defined tools](https://learn.microsoft.com/en-us/azure/ai-services/agents/how-to/tools/openapi-spec)
    ##### [Azure Functions](https://learn.microsoft.com/en-us/azure/ai-services/agents/how-to/tools/azure-functions)
    ### [Content Filtering](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/content-filters?context=/azure/ai-services/agents/context/context)
    ### [Use Your Own Resources](https://learn.microsoft.com/en-us/azure/ai-services/agents/how-to/use-your-own-resources)

    ## Responsible AI
    ### [Data, privacy and security](https://learn.microsoft.com/en-us/legal/cognitive-services/agents/data-privacy-security?context=/azure/ai-services/agents/context/context)

    ## Reference
    ### Frameworks
    #### [AutoGen](https://microsoft.github.io/autogen/0.4.0.dev11/)
    #### [Semantic Kernel](https://learn.microsoft.com/en-us/semantic-kernel/overview/)
    ### SDK
    ### Azure SDK
    ##### [Python](https://learn.microsoft.com/en-us/python/api/overview/azure/ai-projects-readme?context=/azure/ai-services/agents/context/context)
    ##### [C#](https://learn.microsoft.com/en-us/dotnet/api/overview/azure/ai.projects-readme?context=/azure/ai-services/agents/context/context)
    ### OpenAI SDK
    ##### [Python](https://github.com/openai/openai-python/blob/main/README.md)
    ##### [C#](https://github.com/openai/openai-dotnet/blob/main/README.md)

    ## Resources
    ### [Support and help options](https://learn.microsoft.com/en-us/azure/ai-services/cognitive-services-support-options?context=/azure/ai-services/agents/context/context)
    ### [Region Support](https://azure.microsoft.com/global-infrastructure/services/?products=cognitive-services)
    ### [Terms of use](https://www.microsoft.com/licensing/terms/productoffering/MicrosoftAzure/MCA#ServiceSpecificTerms)
    ### [Azure compliance offerings](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/)
    ```


??? tip "2. Semantic Kernel Documentation"

    ```markmap

    # Semantic Kernel

    ## [Overview](https://learn.microsoft.com/en-us/semantic-kernel/overview/)

    ## Getting Started
    ### [Quickstart](https://learn.microsoft.com/en-us/semantic-kernel/get-started/quick-start-guide?pivots=programming-language-csharp)
    ### [In Depth Samples](https://learn.microsoft.com/en-us/semantic-kernel/get-started/detailed-samples)
    ### [Supported Languages](https://learn.microsoft.com/en-us/semantic-kernel/get-started/supported-languages)

    ## Concepts
    ### [Kernel](https://learn.microsoft.com/en-us/semantic-kernel/concepts/kernel)
    ### [Semantic Kernel Components](https://learn.microsoft.com/en-us/semantic-kernel/concepts/semantic-kernel-components?pivots=programming-language-csharp)
    ### [Planning](https://learn.microsoft.com/en-us/semantic-kernel/concepts/planning)

    ## Frameworks

    ### [Agent Framework](https://learn.microsoft.com/en-us/semantic-kernel/frameworks/agent/)
    ### [Process Framework](https://learn.microsoft.com/en-us/semantic-kernel/frameworks/process/process-framework)


    ```

??? tip "3. AutoGen Documentation "

    ```markmap
    # AutoGen 0.4
    ## [User Guide](https://microsoft.github.io/autogen/0.4.0.dev11/user-guide/index.html)

    ## [Packages](https://microsoft.github.io/autogen/0.4.0.dev11/packages/index.html)
    ## [API Reference](https://microsoft.github.io/autogen/0.4.0.dev11/reference/index.html)
    ## [Magentic One](https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one)
    ```
---