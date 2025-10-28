# Data Commons Extension for Gemini CLI

This is a Gemini CLI extension that allows you to query public datasets from [Data Commons](https://datacommons.org/) using natural language, and to ground AI responses from any any other tools in authoritative data, to reduce hallucinations.

This page provides basic instructions for installing and running the extension. For complete information on using Data Commons with Gemini CLI, please see the [Data Commons documentation](https://docs.datacommons.org/mcp).

## Prerequisites

Before using this extension, you will need:

-  [Gemini CLI](https://geminicli.com/docs/get-started/) installed.
-   A free Data Commons API key. To obtain an API key, go to https://apikeys.datacommons.org and request a key for the api.datacommons.org domain. 
-  [Gemini CLI](https://geminicli.com/docs/get-started/) installed.
-   A free Data Commons API key. To obtain an API key, go to https://apikeys.datacommons.org and request a key for the api.datacommons.org domain. 
-   `uv`, a tool for managing and installing Python packages: install from https://docs.astral.sh/uv/getting-started/installation/. 
-  [git](https://git-scm.com/) installed.
-  [git](https://git-scm.com/) installed.

## Installation

Install the extension directly from GitHub:
```sh
gemini extensions install https://github.com/gemini-cli-extensions/datacommons
```
> Note: If you have previously configured Gemini CLI to use the Data Commons MCP Server in the top-level `.gemini/settings.json` file and want to use the extension instead, be sure to delete the `datacommons-mcp` section from the file.

## Usage

1. Set your Data Commons API key as an environment variable:
   ```
   export DC_API_KEY=<YOUR_API_KEY>
   ```
2. Run `gemini`. 
3. Ask questions about statistical data in natural language. 
1. Set your Data Commons API key as an environment variable:
   ```
   export DC_API_KEY=<YOUR_API_KEY>
   ```
2. Run `gemini`. 
3. Ask questions about statistical data in natural language. 

### Examples

*   "What is the population of California?"
*   "Show me the median income in Santa Clara County."
*   "Compare the GDP of Japan and Germany."
*   "Poverty indicators for India"

## How it works

This extension uses the `datacommons-mcp` PyPI package, which runs a local MCP server to translate natural language queries into Data Commons API calls. This package is based on the Data Commons MCP Server from the [Data Commons Agent Toolkit](https://github.com/datacommonsorg/agent-toolkit/tree/main/packages/datacommons-mcp).

The extension also provides a context file (`DATACOMMONS.md`) that gives the Gemini agent instructions on how to handle user queries and tool responses.

## How it works

This extension uses the `datacommons-mcp` PyPI package, which runs a local MCP server to translate natural language queries into Data Commons API calls. This package is based on the Data Commons MCP Server from the [Data Commons Agent Toolkit](https://github.com/datacommonsorg/agent-toolkit/tree/main/packages/datacommons-mcp).

The extension also provides a context file (`DATACOMMONS.md`) that gives the Gemini agent instructions on how to handle user queries and tool responses.

## Troubleshooting

You can diagnose common errors, such as invalid API keys, by using the debug flag:
```
gemini -d
```

## Uninstall

To uninstall the extension, run:
```
gemini extensions uninstall datacommons
```

