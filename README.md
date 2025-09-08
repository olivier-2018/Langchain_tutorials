# Lanchain

## Concept

Langchain streamlines the application of LLMs using abstraction.

This approach allows to represent common steps and concepts necessary to work with LLMs. Those can be chained with each each others.

Langchain includes a number of toolkit elements used for abstraction:

- **LLMs handlers**: used to abstract each indicidual LLM (as a langchain depenency or a standalone python package).

- **Prompts template class**: formalizes composition of prompts without the need to manually hard code context and queries.

- **Chains**: core to langchain workflow, they combines LLMs with other components in a sequential manner. Each element of the chain can use its own LLM, prompts and tools.

- **Indexes**: allow to access external data sources. Comprise of different elements such as:

  - **Document loader**: work with 3rd party application to import external data (storage like google drive or box, web content, DBs like pandas or mongo)
  - **Vector DBs**: used to store text data embeddings for later retrieval.
  - **Text splitters**: split large body of text into smaller semantically meaningfull chinks which ce be embedded and stored away.

- **Memory**: used to retain past conversation as context.

- **Agents**: Utilizing the "reasoning" capabilities of LLMs to make decisions such as selecting which tool to use to access data or perform specific tasks. Works in combination with promtps, tools and memory.

## Applications

- Chatbots
- summarizations:
- QAs:
- Data augmentation:
- Virtual agents:

## Related frameworks

- **Langserve**: serving langchains as REST APIs

- **LAngsmith**: environment to monitor, evaluate and debug applications

- **Langgraph**: used for orchestration of langchain chains by introducing the conept of **state** which can be accessed and modified by various components of the chains

## Summary:

- **Langchain** provides an abstraction layer for chaining LLM operations into applications thereby providing a sequential wokflow.

- **Langgraph** creates and manages what is know as **multi-agents** systems and workflows. This is suited when the workflow is not know apriori but determined dynamically depending on the **states** of the system. **Nodes** are connected by **edges** and can therefore be visited and revisited several times and their respective **states** will evolve.

## Getting started:

```bash
uv venv --python 3.12 .venv
source .venv/bin/activate
uv sync
# Notes:
uv add <python_library>
```
