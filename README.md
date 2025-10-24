# Data Commons Extension for Gemini CLI

This is a Gemini CLI extension that allows you to query public datasets from [Data Commons](https://datacommons.org/) using natural language, grounding AI responses in authoritative data to reduce hallucinations.

## Prerequisites

Before using this extension, you will need:

-   A free Data Commons API key. To obtain an API key, go to https://apikeys.datacommons.org and request a key for the api.datacommons.org domain. Once you have your key, set it as an environment variable named `DC_API_KEY`.
-   Install `uv`, a tool for managing and installing Python packages: install from https://docs.astral.sh/uv/getting-started/installation/.

## Installation

Install the extension directly from GitHub:
```sh
gemini extensions install https://github.com/gemini-cli-extensions/datacommons
```

## Usage

Once the extension is installed and configured, you can ask questions about statistical data in natural language.

### Examples

*   "What is the population of California?"
*   "Show me the median income in Santa Clara County."
*   "Compare the GDP of Japan and Germany."
*   "Poverty indicators for India"

## How It Works

This extension uses the `datacommons-mcp` PyPI package, which runs a local MCP server to translate natural language queries into Data Commons API calls. This package is based on the Data Commons MCP Server from the [Data Commons Agent Toolkit](https://github.com/datacommonsorg/agent-toolkit/tree/main/packages/datacommons-mcp).
