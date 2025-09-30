<p align="center">
<img src="img/Banner-MS-AI-Tour-26.png" alt="decorative banner" width="1200"/>
</p>

# [Microsoft AI Tour 2026](https://aitour.microsoft.com)

## 🔥LTG152: From protocol to practice: build and use your first MCP server

[![Microsoft Azure AI Foundry Discord](https://dcbadge.limes.pink/api/server/ByRwuEEgH4)](https://discord.gg/Pwpvf3TWaw)
[![Azure AI Foundry Developer Forum](https://img.shields.io/badge/GitHub-Azure_AI_Foundry_Developer_Forum-blue?style=for-the-badge&logo=github&color=adff2f&logoColor=fff)](https://aka.ms/foundry/forum)

If you will be delivering this session, check the [session-delivery-sources](./session-delivery-resources/) folder for slides, scripts, and other resources.

### Session Description

In this talk, discover how the Model Context Protocol (MCP) is transforming the way AI agents connect with tools, data and each other in a standardized way and is becoming part of the Microsoft ecosystem, whether you're working in Azure AI Foundry, Copilot Studio or GitHub Copilot. MCP is more than a protocol—it’s the connective tissue for building intelligent, interoperable systems. You’ll get a fast-paced, hands-on introduction to MCP fundamentals, then dive into building your own MCP server, using it in VS Code as the host and GitHub Copilot as the client.

### 🧠 Learning Outcomes

By the end of this session, learners will be able to:

- Explain MCP fundamentals (host, client, server) and the roles of prompts, tools, and resources.
- Build and run a minimal Python MCP server that writes to and reads from a CSV ledger.
- Invoke the server from GitHub Copilot Chat in VS Code using a prompt that triggers a typed tool and retrieves a resource.

### 💻 Technologies Used

1. Model Context Protocol (MCP)
1. GitHub Copilot Chat (Agent + Tools) and Visual Studio Code
1. Python 3.12, FastMCP, uv (venv + deps), CSV

### 🔗 Session Resources

| Resources          | Links                             | Description        |
|:-------------------|:----------------------------------|:-------------------|
| Additional Resources for this session | [https://learn.microsoft.com](https://learn.microsoft.com?ocid=AITour26_resourcecenter_cnl) | Links specific to this session |

### 📚 Continued Learning Resources

| Resources          | Links                             | Description        |
|:-------------------|:----------------------------------|:-------------------|
| MCP for Beginners (GitHub) | [https://github.com/microsoft/mcp-for-beginners](https://github.com/microsoft/mcp-for-beginners) | Beginner-friendly MCP guide with examples and docs |
| AI Tour 2026 Resource Center | [https://aka.ms/AITour26-Resource-Center](https://aka.ms/AITour26-Resource-Center?ocid=AITour26_resourcecenter_cnl) | Links to all repos for AI Tour 26 Sessions |
| Azure AI Foundry Community Discord | [![Microsoft Azure AI Foundry Discord](https://dcbadge.limes.pink/api/server/ByRwuEEgH4)](https://discord.gg/Pwpvf3TWaw)| Connect with the Azure AI Foundry Community! |
| Learn at AI Tour | [https://aka.ms/LearnAtAITour](https://aka.ms/LearnAtAITour?ocid=AITour26_resourcecenter_cnl) | Continue learning on Microsoft Learn |

### 🌐 Multi-Language Support

Additional Languages Coming Soon

## Content Owners

<table>
<tr>
    <td align="center"><a href="http://github.com/madebygps">
    <img src="https://github.com/madebygps.png" width="100" alt="Gwyneth Pena-Siguenza" /><br />
    <sub><b> Gwyneth Pena-Siguenza
</b></sub></a><br />
            <a href="https://github.com/madebygps" title="talk">📢</a> 
    </td>
    
</tr></table>

## Responsible AI

Microsoft is committed to helping our customers use our AI products responsibly, sharing our learnings, and building trust-based partnerships through tools like Transparency Notes and Impact Assessments. Many of these resources can be found at [https://aka.ms/RAI](https://aka.ms/RAI).
Microsoft’s approach to responsible AI is grounded in our AI principles of fairness, reliability and safety, privacy and security, inclusiveness, transparency, and accountability.

Large-scale natural language, image, and speech models - like the ones used in this sample - can potentially behave in ways that are unfair, unreliable, or offensive, in turn causing harms. Please consult the [Azure OpenAI service Transparency note](https://learn.microsoft.com/legal/cognitive-services/openai/transparency-note?tabs=text) to be informed about risks and limitations.

The recommended approach to mitigating these risks is to include a safety system in your architecture that can detect and prevent harmful behavior. [Azure AI Content Safety](https://learn.microsoft.com/azure/ai-services/content-safety/overview) provides an independent layer of protection, able to detect harmful user-generated and AI-generated content in applications and services. Azure AI Content Safety includes text and image APIs that allow you to detect material that is harmful. Within Azure AI Foundry portal, the Content Safety service allows you to view, explore and try out sample code for detecting harmful content across different modalities. The following [quickstart documentation](https://learn.microsoft.com/azure/ai-services/content-safety/quickstart-text?tabs=visual-studio%2Clinux&pivots=programming-language-rest) guides you through making requests to the service.

Another aspect to take into account is the overall application performance. With multi-modal and multi-models applications, we consider performance to mean that the system performs as you and your users expect, including not generating harmful outputs. It's important to assess the performance of your overall application using [Performance and Quality and Risk and Safety evaluators](https://learn.microsoft.com/azure/ai-studio/concepts/evaluation-metrics-built-in). You also have the ability to create and evaluate with [custom evaluators](https://learn.microsoft.com/azure/ai-studio/how-to/develop/evaluate-sdk#custom-evaluators).

You can evaluate your AI application in your development environment using the [Azure AI Evaluation SDK](https://microsoft.github.io/promptflow/index.html). Given either a test dataset or a target, your generative AI application generations are quantitatively measured with built-in evaluators or custom evaluators of your choice. To get started with the azure ai evaluation sdk to evaluate your system, you can follow the [quickstart guide](https://learn.microsoft.com/azure/ai-studio/how-to/develop/flow-evaluate-sdk). Once you execute an evaluation run, you can [visualize the results in Azure AI Foundry portal ](https://learn.microsoft.com/azure/ai-studio/how-to/evaluate-flow-results).
