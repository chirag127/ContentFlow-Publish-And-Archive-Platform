# OmniPublish-Multi-Platform-Content-Distribution-Node-CLI-Tool

[![Build Status](https://img.shields.io/github/actions/workflow/status/chirag127/OmniPublish-Multi-Platform-Content-Distribution-Node-CLI-Tool/ci.yml?branch=main&style=flat-square)](https://github.com/chirag127/OmniPublish-Multi-Platform-Content-Distribution-Node-CLI-Tool/actions/workflows/ci.yml)
[![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/OmniPublish-Multi-Platform-Content-Distribution-Node-CLI-Tool?style=flat-square)](https://codecov.io/gh/chirag127/OmniPublish-Multi-Platform-Content-Distribution-Node-CLI-Tool)
[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey?style=flat-square)](https://creativecommons.org/licenses/by-nc/4.0/)
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/OmniPublish-Multi-Platform-Content-Distribution-Node-CLI-Tool?style=flat-square)](https://github.com/chirag127/OmniPublish-Multi-Platform-Content-Distribution-Node-CLI-Tool/stargazers)

A TypeScript-powered CLI that writes Markdown once and automatically publishes to 17+ platforms, generates a static archive site, and supports scheduled and issue-driven publishing.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Setup](#setup)
- [Usage](#usage)
- [AI Agent Directives](#ai-agent-directives)
- [Contributing](#contributing)
- [License](#license)

## Introduction
OmniPublish is designed to simplify content distribution across multiple platforms. With its powerful CLI, you can manage your content efficiently and effectively.

## Features
- Publish to 17+ platforms
- Generate a static archive site
- Support for scheduled and issue-driven publishing

## Setup
To get started with OmniPublish, follow these steps:
1. Clone the repository: `git clone https://github.com/chirag127/OmniPublish-Multi-Platform-Content-Distribution-Node-CLI-Tool.git`
2. Install dependencies: `npm install`
3. Configure your environment: `cp .env.example .env`

## Usage
To publish your content, run the following command: `npm run publish`

## AI Agent Directives
<details>
<summary>View AI Agent Directives</summary>

### Client Configuration
* **Base URL:** `https://api.cerebras.ai/v1`
* **API Key Variable:** `CEREBRAS_API_KEY`
* **Library:** Use the standard `openai` Node.js library.
javascript
const { OpenAI } = require('openai');
const client = new OpenAI({
  base: 'https://api.cerebras.ai/v1',
  apiKey: process.env.CEREBRAS_API_KEY,
});


### Model Hierarchy (Fallback Cascade)
Always attempt the highest-parameter model first for complex reasoning, cascading down for speed.
* **Tier 1 (Frontier Intelligence):** `zai-glm-4.6` (357B)
* **Tier 2 (Heavy Reasoning):** `qwen-3-235b-a22b-instruct-2507` (235B)
* **Tier 3 (General Purpose):** `gpt-oss-120b` (120B)
* **Tier 4 (Balanced Workhorse):** `llama-3.3-70b` (70B)
* **Tier 5 (Fast Inference):** `qwen-3-32b` (32B)
* **Tier 6 (Ultra-Fast/Instant):** `llama3.1-8b` (8B)

### Operational Limits
* **Max Output Tokens:** `32768` (Free Tier Limit)
* **Context Window:** 65,536 (Free Tier)
* **Concurrency:** `MAX_WORKERS = 5` (Free Tier Safe Limit)
* **Circuit Breaker:** On 429/500 error, trigger **Exponential Backoff** (start 2s) and retry.

</details>

## Contributing
Please see [CONTRIBUTING.md](https://github.com/chirag127/OmniPublish-Multi-Platform-Content-Distribution-Node-CLI-Tool/blob/main/CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## License
This project is licensed under the [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) license.

Star ⭐ this Repo if you find it useful!