# Architecture Documentation

## Overview
This ReAct implements Code Generation Agent Workflow (Langgraph) for Technology use cases.

## Components
1. **Manual Trigger**: n8n-nodes-base.manualTrigger node
2. **Chat Model (Bedrock)**: @n8n/n8n-nodes-langchain.lmChatAwsBedrock node
3. **Memory**: @n8n/n8n-nodes-langchain.memoryBufferWindow node
4. **Step 1: Agent 1**: @n8n/n8n-nodes-langchain.agent node
5. **Step 2: Agent 2**: @n8n/n8n-nodes-langchain.agent node
6. **Guard 1**: n8n-nodes-base.function node
7. **Guard 2**: n8n-nodes-base.function node
8. **Sanitize Output**: n8n-nodes-base.function node
9. **Summary**: @n8n/n8n-nodes-langchain.agent node
10. **Compose Summary**: n8n-nodes-base.function node
11. **Legend**: n8n-nodes-base.stickyNote node
12. **Legend: Colors**: n8n-nodes-base.stickyNote node
13. **Execution Summary**: n8n-nodes-base.function node

## Data Flow
- Input: Manual Trigger
- Processing: 13 sequential steps
- Output: Execution Summary
