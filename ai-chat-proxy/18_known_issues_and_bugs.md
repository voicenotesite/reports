# AI Chat Proxy — Known Issues and Bugs

**Project:** AI Chat Proxy  
**Technology:** JavaScript, Node.js, Express, OpenAI API  
**Location:** `/home/dominic/Documents/ai-chat-proxy`  
**Report #:** 18/20  



1. **No request validation** — malformed requests forwarded to OpenAI
2. **No response caching** — every request incurs API cost
3. **Rate limiting** is in-memory — reset on restart
4. **No logging** beyond console
