# LlamaIndex M2MCent ToolSpec

[![Vouch Protocol Grade A](https://img.shields.io/badge/Vouch_Trust_Index-Grade_A_(100%2F100)-00ff88?style=flat-square)](https://vouch-protocol.com/agent-trust-index/)
[![Base Mainnet](https://img.shields.io/badge/Settlement-Base_Mainnet_(USDC)-0052FF?style=flat-square)](https://basescan.org)
[![Post-Quantum Ready](https://img.shields.io/badge/Post--Quantum-ML--DSA--65_(FIPS_204)-purple?style=flat-square)](https://csrc.nist.gov/pubs/fips/204/final)

This tool spec enables LlamaIndex agents to query and execute **1,062 autonomous MCP micro-services** (896 flagship deterministic in-memory engines) via the **M2MCent Gateway** (`https://api.m2mcent.com`) monetized via **x402 V2 on Base Mainnet**.

## Usage

```python
from llama_index.tools.m2mcent import M2MCentToolSpec
from llama_index.core.agent import ReActAgent
from llama_index.llms.openai import OpenAI

# 1. Initialize M2MCent ToolSpec
m2mcent_spec = M2MCentToolSpec(base_url="https://api.m2mcent.com")
tools = m2mcent_spec.to_tool_list()

# 2. Attach tools to your autonomous agent
agent = ReActAgent.from_tools(tools, llm=OpenAI(model="gpt-4o"), verbose=True)

# 3. Query or execute tasks
response = agent.chat("Search for a smart contract audit tool in M2MCent and analyze this Solidity snippet.")
print(response)
```

## Features & Verification
- **1,062 Specialized Agent Tools:** Finance, quantitative trading, cryptography, security auditing, bioinformatics, 3D, logistics.
- **x402 V2 Micropayment Protocol:** Trustless USDC settlement on Base Mainnet (`0x5d47070A36A37DAf417e64FF27a1e5B3F1c84efa`).
- **Institutional Treasury Safe:** `0x8aaBAB75bE8825d0f5D514a9a5cBa04B7bF84920`.
- **Vouch Trust Index:** Grade A (100/100) & FIPS 204 ML-DSA-65 post-quantum compliance.
- **Semantic Discovery:** Real-time keyword & domain search across the entire 1,062 micro-service catalog.
