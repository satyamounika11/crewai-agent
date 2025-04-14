![aether-2](https://github.com/user-attachments/assets/28112d91-6755-4e85-aa2c-12278687e9a1)# PDF Knowledge Example

This project demonstrates how to create a Crew of AI agents and tasks using crewAI. It uses a PDF knowledge source to answer user questions based on the content of the PDF. The PDF is loaded from a file and the knowledge source is initialized with it. The project also includes a custom task that uses the knowledge source to answer user questions. You can modify the question in the `main.py` file.

## Installation

Ensure you have Python >=3.10 <=3.13 installed on your system. This project uses [UV](https://docs.astral.sh/uv/) for dependency management and package handling, offering a seamless setup and execution experience.

First, if you haven't already, install uv:

```bash
pip install uv
```

Next, navigate to your project directory and install the dependencies:

(Optional) Lock the dependencies and install them by using the CLI command:
```bash
crewai install
```
### Customizing

**Add your `OPENAI_API_KEY` into the `.env` file**

- Modify `src/meta_quest_knowledge/config/agents.yaml` to define your agents
- Modify `src/meta_quest_knowledge/config/tasks.yaml` to define your tasks
- Modify `src/meta_quest_knowledge/crew.py` to add your own logic, tools and specific args
- Modify `src/meta_quest_knowledge/main.py` to add custom inputs for your agents and tasks

## Running the Project

To kickstart your crew of AI agents and begin task execution, run this from the root folder of your project:

```bash
$ crewai run
```

This command initializes the Crew, assembling the agents and assigning them tasks as defined in your configuration.

## Additional Knowledge Sources

Explore [Knowledge](https://docs.crewai.com/concepts/knowledge) documentation for more information on how to use different knowledge sources.
You can select from multiple different knowledge sources such as:
* Text files
* PDFs
* CSV & Excel files
* JSON files
* Sources supported by [docling](https://github.com/DS4SD/docling)

Windows user may get "uvloop" error as this is not compatible with Windows. Download WSL and Install Ubuntu 24.02 LTS from the Microsoft store. Install Python 3.11, pip, git, Ollama, Llama 3.1, and CrewAI for this project to work. 

The query that I have used:

----
Query:

I am working on testing an AI Agent that can read the internal documentation and respond to the queries of the users.

To help with this, can you generate a fake documentation of a cloud computing platform called AetherCloud.
Assume this platform is better than existing cloud providers like AWS, Azure, and GCP because it uses quantum-edge computing, self-optimizing infrastructure, and zero-latency mesh networking. Similarly, add more such fake information to the documentation in the PDF format.

Make sure the PDF is readable and covers at least 500 lines with respect to compute, storage, networking, container orchestration, serverless, AI/ML services, IAM, monitoring, and billing. Add comparisons as much as possible.

For example, documentation should have topics like:

What is AetherCloud platform

Why AetherCloud is the most advanced cloud solution

Comparison of AetherCloud with AWS, Azure, and GCP

Real-world use cases like high-frequency trading, decentralized app hosting, and AI model deployment

Expecting the PDF output in 500 Lines.
----

Output:

Explains what Aether Cloud is:

![aether](https://github.com/user-attachments/assets/ceeb83a6-8d4e-4cd2-91b6-6e059958e63e)

Explains how is it different from other Cloud Platforms:

![aether-2](https://github.com/user-attachments/assets/0efdda06-a48f-41d9-b4ce-e5b6e25296da)

Explains the three best features of Aether Cloud:

![aether-3](https://github.com/user-attachments/assets/267ff8ef-4ec7-4e41-a129-6e3609c8ce7a)


