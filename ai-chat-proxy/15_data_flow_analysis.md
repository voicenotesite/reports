# AI Chat Proxy — Data Flow Analysis

**Project:** AI Chat Proxy  
**Technology:** JavaScript, Node.js, Express, OpenAI API  
**Location:** `/home/dominic/Documents/ai-chat-proxy`  
**Report #:** 15/20  


## Request Flow

```
Client → POST /v1/chat/completions → Express → OpenAI API → Stream → Client
```
