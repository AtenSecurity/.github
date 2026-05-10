# Aten Security

**The Runtime Control Plane for AI Agents.**

Aten Security is the market-leading platform for **AI Agent Runtime Security**. We bridge the gap between access approval and autonomous action by providing a real-time enforcement layer that governs what AI agents do in production.

## Mission
As enterprises shift to autonomous agentic workflows, traditional identity-centric security is no longer enough. Our mission is to provide the guardrails for the autonomous enterprise, ensuring AI agents remain secure, compliant, and accountable at the moment of execution.

## The Aten Ecosystem

### Runtime SDKs
Integrate **Thoth** decisions directly into your agentic loops. Evaluate context and intent in milliseconds to **ALLOW**, **STEP_UP**, or **BLOCK** actions.
* [**thoth-py**](https://github.com/atensecurity/thoth-py) – Official Python SDK for LangChain, CrewAI, and custom frameworks.
* [**thoth-ts**](https://github.com/atensecurity/thoth-ts) – Official TypeScript/Node.js SDK for agentic environments.
* [**thoth-go**](https://github.com/atensecurity/thoth-go) – High-performance Go SDK for backend runtime enforcement.

### Infrastructure as Code (IaC)
Manage your security posture as code. Define policies, environments, and integrations using the tools your DevOps teams already use.
* [**terraform-provider-thoth**](https://github.com/atensecurity/terraform-provider-thoth) – Official Terraform provider for Aten Thoth resources.
* [**pulumi-thoth**](https://github.com/atensecurity/pulumi-thoth) – Native Pulumi provider for cloud-native security orchestration.

### Cloud Native & Connectivity
Deploy Aten Thoth seamlessly across hybrid and multi-cloud environments.
* [**thoth-operator**](https://github.com/atensecurity/thoth-operator) – Manage Thoth instances and policy CRDs natively within Kubernetes.
* [**thoth**](https://github.com/aten-security/thoth) – Secure runtime bridge for the **Model Context Protocol (MCP)**; govern any MCP-compliant tool or server.

### Operations & Runbooks
* [**runbooks**](https://github.com/atensecurity/runbooks) – Operational guides for incident response, policy tuning, and disaster recovery.
* [**policy-templates**](https://github.com/atensecurity/thoth-runbooks/tree/main/policy-templates) – Pre-built policy-as-code templates for PII/PHI protection and guardrails.


## How It Works: The Thoth Control Plane
Thoth sits in the execution path, evaluating every sensitive tool call or data request against your enterprise policy.

| Decision | Impact |
| :--- | :--- |
| **`ALLOW`** | Action proceeds and generates tamper-proof evidence. |
| **`STEP_UP`** | Execution pauses for Human-In-The-Loop (HITL) approval. |
| **`BLOCK`** | Action is terminated; immediate alert sent to SIEM/SOAR. |

## Enterprise Integration
Aten does not require a rip-and-replace of your security stack. We provide deep integrations with:
**SIEM/SOAR/XDR** (Splunk, Sentinel) • **IAM/PAM** • **Browser & SASE** • **GRC Workflows** • **Non-Human Identity**

**[Website](https://atensecurity.com) • [Twitter/X](https://x.com/atensecurity) • [LinkedIn](https://www.linkedin.com/company/atensec) • [Documentation](https://docs.atensecurity.com)**
