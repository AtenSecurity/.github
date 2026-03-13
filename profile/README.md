# Aten Security — Open Source SDKs

[Aten Security](https://aten.security) builds post-approval governance for AI agents
and enterprise SaaS integrations. This organization publishes our open-source SDKs
and developer tools.


## Thoth — AI Agent Governance SDK

Instrument any AI agent with policy enforcement, behavioral monitoring, and
step-up authentication in minutes. Works with Claude, OpenAI, LangChain, and more.

| SDK | Package | Install |
|-----|---------|---------|
| Go | [`thoth-go`](https://github.com/atensecurity/thoth-go) | `go get github.com/atensecurity/thoth-go` |
| Python | [`aten-thoth`](https://pypi.org/project/aten-thoth/) | `pip install aten-thoth` |
| TypeScript | [`@atensec/thoth`](https://www.npmjs.com/package/@atensec/thoth) | `npm install @atensec/thoth` |

### Quick start (Go)

```go
client, _ := thoth.NewClient(thoth.Config{
    TenantID: "acme-corp",
    AgentID:  "invoice-processor-v1",
})
defer client.Close()

search := client.WrapToolFunc("search_docs", mySearchFn)
// governance runs automatically on every call
result, err := search(ctx, map[string]any{"query": "access policy"})
```

### Quick start (Python — Anthropic Claude)

```python
import thoth

wrapped = thoth.instrument_anthropic(
    {"search_docs": my_search_fn},
    agent_id="invoice-processor-v1",
    approved_scope=["search_docs"],
    tenant_id="acme-corp",
)

# Drop into your Anthropic agentic loop
result = wrapped["search_docs"](block.input)
```

### Quick start (TypeScript — OpenAI)

```typescript
import { wrapOpenAITools } from "@atensec/thoth";

const tools = wrapOpenAITools(
  { search_docs: mySearchFn },
  { agentId: "invoice-processor-v1", approvedScope: ["search_docs"], tenantId: "acme-corp" },
);

// Drop into your OpenAI tool-calling loop
const result = await tools[call.function.name](args);
```

## Links

- **Docs:** [docs.aten.security](https://docs.aten.security)
- **Website:** [aten.security](https://aten.security)
- **Contact:** [sdk@aten.security](mailto:sdk@aten.security)
- **Security issues:** security@aten.security (do not open public issues)

*Thoth SDKs are Apache 2.0 licensed.*
@ch3ck
Comment
 
Leave a comment
Footer
© 2026 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Community
Docs
Contact
Manage cookies
Do not share my personal information
