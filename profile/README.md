<div align="center">
    <a href="https://agent-runtime-protocol.com/"> <img src="./images/ARP_Long_Transparent.png" alt="ARP Logo" width="80%"></a>
    <a href="https://agent-runtime-protocol.com/" target="_blank"><img src="https://img.shields.io/website?url=https%3A%2F%2Fagent-runtime-protocol.com%2F&up_message=https%3A%2F%2Fagent-runtime-protocol.com%2F&up_color=31aab6&down_message=unavailable&labelColor=1d636a" alt="Website Link"></a>
    <a href="https://agent-runtime-protocol.com/public_docs/" target="_blank"><img src="https://img.shields.io/website?url=https%3A%2F%2Fagent-runtime-protocol.com%2Fpublic_docs%2F&up_message=https%3A%2F%2Fagent-runtime-protocol.com%2Fpublic_docs%2F&up_color=31aab6&down_message=unavailable&label=documentation&labelColor=1d636a" alt="Docs Website Link"></a>
    
  <a href="https://www.reddit.com/r/AgentRuntimeProtocol/" target="_blank"><img src="https://img.shields.io/badge/reddit-r%2FAgentRuntimeProtocol-ff6314?logo=reddit" alt="Reddit"></a>
</div>




<div align="center">
    <h3>One protocol to unify agents, tools, and orchestration.</h3>
    <h4>Open-source, Inter-operable, Implemented and Runnable. By devs, for devs.</h4>
</div>

<div align="center">
  <a href="https://opensource.org/licenses/MIT" target="_blank"><img src="https://img.shields.io/pypi/l/arp-standard-py" alt="ARP Python SDK License"></a>
  <a href="https://pypistats.org/packages/arp-standard-py" target="_blank"><img src="https://img.shields.io/pepy/dt/arp-standard-py" alt="PyPI - Downloads"></a>
  <a href="https://pypi.org/project/arp-standard-py/#history" target="_blank"><img src="https://img.shields.io/pypi/v/arp-standard-py?label=arp-standard-py&labelColor=1d636a" alt="ARP Standard Python SDK Version"></a>
  <a href="https://pypi.org/project/arp-standard-py/#history" target="_blank"><img src="https://img.shields.io/pypi/v/arp-jarvis?label=arp-jarvis&labelColor=1d636a" alt="JARVIS Version"></a>
</div>

<div align="center">
  <a href="https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/agentruntimeprotocol/ARP_Standard" target="_blank"><img src="https://img.shields.io/static/v1?label=Dev%20Containers%20For%20ARP%20Standard&message=Open&color=blue&logo=visualstudiocode" alt="Open in Dev Containers"></a>
  <a href="https://codespaces.new/agentruntimeprotocol/ARP_Standard" target="_blank"><img src="https://github.com/codespaces/badge.svg" alt="Open ARP Standard in Github Codespace" title="Open ARP Standard in Github Codespace" width="150" height="20"></a>
</div>

---

> ## Imagine if agents were as portable as containers — and tools were truly reusable across stacks, no matter what framework you use. It may be closer than it sounds.

---

**Agent Runtime Protocol (ARP)** is an open standard for running AI agent workflows in a consistent way across different runtimes, tool ecosystems, model providers, and environments. It focuses on **integration** with a wide range of protocols like LangChain, MCP, A2A etc.

> [!NOTE]
> As a new project, ARP is rapidly building out capabilities to bring our vision to life. Our core developers are aggressively adding new integrations and features. Check back often for the latest addition, and let us know what you want next on [**r/AgentRuntimeProtocol**](https://www.reddit.com/r/AgentRuntimeProtocol/) or the GitHub discussions! 

> [!NOTE]
> [*JARVIS*](https://github.com/AgentRuntimeProtocol/JARVIS_Release) is our first-party Python implementation of a reference stack to showcase ARP, and it will be updated as the standard evolves to fully utilize all the new and exciting features we built. [Try it out](#getting-started)! 

## Are you facing these problems?

- You keep rewriting your **agent API surface** whenever you switch frameworks or move from local → service.
- Tools aren’t reusable: every stack needs its own **wrappers, schemas, auth, and discovery**.
- Scaling from “one agent” to “a fleet” means rebuilding **routing, lifecycle, retries, and run management**.
- You want to adopt emerging standards without betting the farm on a single ecosystem.

ARP standardizes the seams while implementing the nuances so you can adopt incrementally and keep components swappable.

## **ARP's Values**

- <details>
    <summary>
      <b>Open Standard:</b> ARP is an <i>open, community-driven</i> specification - not a single library.
    </summary>
    <ul>
     <li>Its contracts are public and platform-agnostic, avoiding vendor lock-in and encouraging a wide range of implementations.</li>
     <li>On the other hand, we provide first-party OSS implementations for an out-of-the-box experience.</li>
    </ul>
  </details>

- <details>
    <summary>
      <b>Interoperability-First:</b> ARP prioritizes working with other standards, protocols and ecosystems.
    </summary> 
    <ul>
     <li>It's built to integrate with alternative agent protocols and tool APIs rather than form a walled garden.</li>
     <li>For example, ARP components can wrap external tool servers or expose compatibility layers for other agent frameworks - see <b>Interoperability</b> below.</li>
    </ul>
  </details>

- <details>
    <summary> 
      <b>Modular Architecture:</b> Each piece of the agent system is a separate module with a well-defined API.
    </summary>
    <ul>
     <li>You can swap out or upgrade any component (or omit ones you don't need) without breaking the others.</li>
     <li>This means not rebuilding wheels, and agile development of the components independent from each other.</li>
    </ul>
  </details>

- <details>
    <summary> 
      <b>Pluggable Implementations:</b> The <i>standard-first</i> design means multiple implementations can coexist.
    </summary>
    <ul>
     <li>An ARP "Runtime" could be a local process, a containerized service, or a hosted one - all are interchangeable if they conform to the API.</li>
     <li>Similarly, tool providers or orchestrators can be customized or replaced as needed.</li>
     <li>As we improve <i>JARVIS</i>, our first-party offering, we try to keep this in mind and provide variants that suit different needs.</li>
    </ul>
  </details>

- <details>
    <summary>
      <b>Production-Minded:</b> Built for real-world deployments.
    </summary>
    <ul>
     <li>Built by experienced devs from companies including Microsoft and Amazon, ARP is built from the ground up with production and enterprise adoption in mind.</li>
     <li>Focuses on the essentials: clear API contracts, modular components, and reference implementations that prioritize correctness and maintainability.</li>
     <li>Designed to be operable at scale: semantic versioning + deprecation paths, and integrations for observability (structured logs, metrics, traces) to monitor and debug agent runs.</li>
    </ul>
  </details>

- <details>
    <summary> 
      <b>Community Driven:</b> ARP is not locked onto one company or one tech stack.
    </summary>
    <ul>
     <li>The open source nature of the core libraries encourages community input on what's working and what's needed. </li>
     <li>We do not want to develop in isolation. The fast shifting landscape of AI agent systems needs to be driven by actual developer needs, and we want to make sure that actually happens.</li>
     <li>This also means, as we develop and evolve the standard, we try to keep the community informed and involved via public forums. We don't release breaking changes in the standard unless we have very good reasons to, and even then, we keep the community informed with announcements, and prepared via beta releases.</li>
    </ul>
  </details>

## ARP Ecosystem Architecture

ARP defines a **protocol ecosystem** of services that work in concert to orchestrate complex agent workflows. The primary components of this ecosystem are:

- <details>
    <summary>
      <b>Agent Runtime:</b> A service that executes the logic of an AI agent.
    </summary>
    <ul>
     <li>Given a user query (goal), an ARP-compliant Runtime plans and interacts with an LLM, decides which tools to use, calls those tools, and iteratively works towards a solution.</li>
     <li>Runtimes implement the ARP Runtime API so that any ARP-aware client (or orchestrator) can start and manage agent runs in a uniform way.</li>
    </ul>
  </details>

- <details>
    <summary>
      <b>Tool Registry:</b> A service that provides a catalog of tools and acts as a standardized interface for tool usage.
    </summary>
    <ul>
     <li>An ARP Tool Registry lists available tools (and their schemas) and handles invocation requests from agent runtimes.</li>
     <li>Tools can be anything from local functions to remote APIs; the Tool Registry abstracts these behind a consistent API, making it easy for agents to discover and use tools dynamically.</li>
    </ul>
  </details>

- <details>
    <summary>
      <b>Daemon (Orchestrator):</b> A service that manages one or more agent runtimes and routes work to them.
    </summary>
    <ul>
     <li>An ARP Daemon can spawn or register multiple runtime instances (forming a fleet of agents), handle their lifecycle, and dispatch incoming tasks to appropriate runtimes.</li>
     <li>It implements the ARP Daemon API, allowing clients to submit agent tasks without worrying about which specific runtime instance executes them. This enables horizontal scaling and centralized control (e.g. running N agents in parallel, pooling resources, etc.).</li>
    </ul>
  </details>

- <details>
    <summary>
      <b>Control Plane (planned):</b> A higher-level management layer for ARP deployments.
    </summary>
    <ul>
     <li>A Control Plane would coordinate multiple daemons and tool registries across an organization, providing features like multi-tenancy, policy enforcement, security controls, and observability.</li>
    </ul>
  </details>

> [!Note]
> <details>
>   <summary>On the Control Plane</summary>
>   This is the highest level component of the system, meaning that (at least for now,) it is not part of the ARP Standard, which focuses on defining APIs provided by components. A Control Plane is a <i>consumer</i> of the <i>daemon</i>  API and SDK clients, but we do not expect its own APIs and functionalities to be defined via the ARP Standard.
> 
>   This is by-design. The high-level capabilities required in a multi-agent, multi-environment agent system is complex and use-case specific, and standardizing it is considered complex and in many cases counter-productive by core devs of ARP.
> 
>   With this being said, a first-party ARP-compliant MVP of the Control Plane is in development, both to showcase the potential of the system and to provide out-of-the-box experience for developers with common orchestration needs.
> </details>

In a typical ARP-based workflow, if a Daemon is in use,  a client (for example, a user application or script) sends a task to the Daemon. It takes care of selecting or spinning up a Runtime instance for the task, and route the task to it. The Runtime instance consults a Tool Registry to fetch available tools and executes the agent's plan, invoking tools as needed.

The interactions between these components are all governed by ARP's APIs, ensuring any ARP-compliant client can talk to any ARP-compliant service. The diagram below illustrates the high-level architecture and data flow of the ARP ecosystem:

<p align="center">
  <img
    src="images/ARP_Ecosystem_Diagram_Basic.png"
    alt="High-level architecture of the ARP ecosystem: ARP clients (SDKs or user apps) communicate with a Daemon or directly with a Runtime. The Runtime pulls available tools from a Tool Registry and executes the agent's plan. A future Control Plane (not shown in initial implementations) could manage multiple Daemons and Tool Registries for enterprise-scale deployment."
  />
</p>

## JARVIS Stack: A Reference Implementation

To help developers adopt ARP quickly, the ARP team provides **JARVIS**, a first-party open-source implementation of the entire ARP stack.

JARVIS is an **out-of-the-box agent runtime environment** that includes a **Runtime**, **Tool Registry**, and **Daemon** that all speak ARP. It comes as a unified distribution with a CLI that makes it easy to run the whole system locally.

```bash
pip install arp-jarvis
```

Key characteristics of *JARVIS* include: 
- **standard-first:** All components are built directly following the ARP spec contracts.
- **modular:** You can run or extend each component independently. 
- **runtime-agnostic:** The agent execution can run anywhere - local process, container, etc.
- **tool-agnostic:** (tools can be local Python functions, HTTP APIs, or even adapters to other tool ecosystems).

**JARVIS** is maintained by the creators of *ARP*, so it stays up-to-date with the latest spec and serves as a validation of the standard in practice.

While JARVIS provides a *ready-to-use* implementation, ARP is not tied to JARVIS alone. You can replace or extend any part of the JARVIS stack with your own components, as long as they implement the ARP interfaces. JARVIS proves out the standard and we do want it to be one of the most polished ARP stacks out there, but it's just one implementation; the broader goal is an ecosystem of interoperable tools and services from many sources.

For example, an advanced user might swap in a custom Tool Registry that interfaces with an internal database, or use a different agent runtime optimized for a specific domain - all without modifying the rest of the system. 

**Looking ahead:** 

Today, JARVIS is self-hosted (run it on your machine or cloud instance). In the future, we plan to offer managed (hosted) and enterprise-grade versions of the ARP platform, so organizations can leverage ARP with turnkey infrastructure and enterprise features. 

These upcoming offerings will build on the open standard and reference stack, ensuring full compatibility between open-source and hosted environments.

## Interoperability and Adapters

ARP is designed to interoperate with other agent frameworks and protocols, not to exist in a silo. A core philosophy of ARP is being an **"integration/glue layer"** between different parts of the AI ecosystem.

To that end, the ARP ecosystem either provides or plans to provide adapters and bridges for various external standards, including (click to expand):

- <details>
    <summary>
      <b>Tool API integration (MCP):</b> The ARP Tool Registry can act as a wrapper around external tool-serving protocols.
    </summary>
    <ul>
     <li>Status: <b>WIP</b>.</li>
     <li>For example, support is planned for <i>MCP</i> so that tools exposed via MCP servers can be seamlessly accessed through an ARP Tool Registry.</li>
     <li>This allows ARP-based agents to tap into existing tool servers without custom integration work.</li>
    </ul>
  </details>

- <details>
    <summary>
      <b>Agent-to-Agent communication (A2A):</b> ARP can bridge to agent-to-agent messaging schemes.
    </summary>
    <ul>
     <li>Status: <b>WIP</b>.</li>
     <li>In scenarios where agents need to communicate or cooperate, ARP plans to support an A2A style interface so that an ARP agent can talk to other agents using a standardized method.</li>
     <li>This could involve translating ARP calls to a peer-to-peer agent protocol for both inbound and outbound communication.</li>
    </ul>
  </details>

- <details>
    <summary>
      <b>Agent-as-a-Service APIs:</b> ARP components can expose facades that mimic other "agent service" APIs.
    </summary>
    <ul>
     <li>Status: <b>WIP</b>.</li>
     <li>For example, an ARP Runtime or Daemon could offer an endpoint compatible with an existing Agent API specification.</li>
     <li>This keeps ARP components compatible with other frameworks that you may already be using, and helps ARP-based systems plug into external tools or client libraries expecting that protocol.</li>
     <li>This provides developers another approach for interoperability. Instead of plugging other services to ARP, you can use ARP components in another service, if your specific use cases demand that. Then, any future migration to ARP stack becomes straight-forward.</li>
    </ul>
  </details>

- <details>
    <summary>
      <b>Agent Runtime Facades (LangChain, LlamaIndex, etc.):</b> ARP plans to make it straightforward to run agents built with other frameworks inside an ARP ecosystem—without rewriting your agent logic.
    </summary>
    <ul>
     <li>Status: <b>WIP</b>.</li>
     <li>A <b>facade runtime</b> is a first-party thin wrapper service that implements the ARP Runtime API, but delegates execution to your existing framework agent/executor.</li>
     <li>This unlocks ARP’s advantages for agents that would otherwise be framework-locked.</li>
     <li>Another set of planned developer tool are template repos/wrappers (e.g., a LangChain facade runtime and a LlamaIndex facade runtime) plus end-to-end examples showing them orchestrated by the Daemon alongside the JARVIS reference runtime.</li>
    </ul>
  </details>

Some of these interoperability bridges are already in development for integration into the JARVIS stack. For instance, adding MCP support in the Tool Registry and an Agent Protocol-compatible mode for the Runtime API. 

ARP's maintainers are actively working on this kind of integration work - ARP is **not a walled garden**. Instead, it aims to be a unifying layer that lets different agent and tool ecosystems work together. 

As new standards emerge in the agent space, ARP will adapt by providing connectors or embracing useful patterns, so developers don't have to choose one ecosystem at the expense of others, and will have a solid foundation for the frameworks of their own choices.

## Getting Started

> [!TIP]
> This quick guide only shows how to run JARVIS stack *without* the daemon. For a more advanced (and comprehensive) approach, see [**JARVIS Quickstart Guide**](https://github.com/AgentRuntimeProtocol/JARVIS_Release#quickstart-with-the-jarvis-stack) for using a **daemon** to manage multiple runtimes, and defining your own tools in the **tool registry**. 

The fastest way to explore ARP is by using the JARVIS reference stack. You can install the JARVIS distribution from PyPI and launch a local agent runtime and tool registry within minutes:

```bash
# Install the ARP JARVIS distribution (includes JARVIS Runtime, Tool Registry, Daemon)
pip install arp-jarvis

# Start a Tool Registry service (provides tools on http://127.0.0.1:8081)
arp-jarvis tool-registry --host 127.0.0.1 --port 8081

# Start an Agent Runtime service (runs an agent, pointing it to the Tool Registry)
arp-jarvis runtime serve --host 127.0.0.1 --port 8080 --tool-registry-url http://127.0.0.1:8081 &
```

> [!NOTE]
> This quickstart guide does not actually call LLM. It is using a stub LLM client to showcase the capability of the ARP system, not LLM providers like OpenAI. The JARVIS runtime supports a real OpenAI driven mode, you will need an OpenAI API key to run that. See [**JARVIS_Runtime OpenAI Mode**](https://github.com/AgentRuntimeProtocol/JARVIS_Runtime/blob/main/docs/quickstart.md#openai-mode-optional).

Once you have a runtime and tool registry running, you can submit an agent task. For example, using curl to ask the agent a question:

```bash
# Submit a new agent run (the agent will use the Calculator tool to solve 19*23)
curl -s -X POST http://127.0.0.1:8080/v1/runs \
  -H "Content-Type: application/json" \
  -d '{"input": {"goal": "What is (19*23)?"}}'

# (The response will include a run_id.)
# Fetch the result of the run (replace <run_id> with the actual ID from the response):
curl -s http://127.0.0.1:8080/v1/runs/<run_id>/result
```

> [!TIP]
> ARP also provides a **Python SDK** (`arp_sdk` from package `arp-standard-py`) for programmatic access to any ARP component - you can use it to integrate ARP calls into your application code instead of making raw HTTP calls. SDKs in other languages such as TypeScript and Go are on the roadmap. Check out the [ARP Standard documentation](https://github.com/AgentRuntimeProtocol/ARP_Standard/tree/main/docs) for more on the API definitions, SDK usage, and advanced topics.
> <details><summary>Python Example - Click to Expand</summary>Point the client at the component URL and call the API directly:
> ```bash
> python3 -m pip install arp-standard-py
> ```
> 
> ```python
> from arp_sdk.models import RunRequest
> from arp_sdk.runtime import RuntimeClient
> 
> runtime = RuntimeClient(base_url="http://127.0.0.1:8080")
> 
> status = runtime.create_run(
>     RunRequest.from_dict({"input": {"goal": "What is (19*23)?"}})
> )
> result = runtime.get_run_result(status.run_id)
> 
> print(result.to_dict())
> ``` 
> </details>

You should see the agent's answer coming back (in this case, it will calculate 19\*23 = 437). Under the hood, the agent runtime broke down the query, invoked a calculation tool via the Tool Registry, and returned the result - all via ARP's standard APIs.

## ARP Ecosystem Projects

### ARP Standard
- [AgentRuntimeProtocol/ARP_Standard](https://github.com/AgentRuntimeProtocol/ARP_Standard) - the standard spec definitions and SDKs

### JARVIS for ARP
- [AgentRuntimeProtocol/JARVIS_Release](https://github.com/AgentRuntimeProtocol/JARVIS_Release) - the meta distribution and CLI. 
  - This is the recommended experience that pins compatible component versions.
- [AgentRuntimeProtocol/JARVIS_Runtime](https://github.com/AgentRuntimeProtocol/JARVIS_Runtime) - the reference ARP Runtime service
- [AgentRuntimeProtocol/JARVIS_Tool_Registry](https://github.com/AgentRuntimeProtocol/JARVIS_Tool_Registry) - the reference Tool Registry service
- [AgentRuntimeProtocol/JARVIS_Daemon](https://github.com/AgentRuntimeProtocol/JARVIS_Daemon) - the reference Daemon service

## Contributing and Community

We welcome contributions to ARP and the JARVIS stack! If you find a bug, have an idea for a new feature, or want to improve the documentation, feel free to open an issue or pull request in the relevant repository. To get started, please see the [Contributing Guide](https://github.com/AgentRuntimeProtocol/ARP_Standard/blob/main/CONTRIBUTING.md) in the `ARP_Standard` repo for the development workflow and standards.

A few ways you can help: 
- **Build adapters and integrations:** Help expand ARP's interoperability by writing bridges to other protocols (for example, integrating more tool APIs, agent frameworks, or adding support for new cloud environments).  

- **Improve tests and conformance:** Add conformance tests, "golden" example cases, and integration tests to ensure ARP implementations stay robust and compatible.  

- **Documentation and examples:** Contribute tutorials, code examples, and guides to help new users understand ARP and get up and running quickly.  

- **Feature suggestions:** Propose enhancements to the ARP spec or JARVIS components - we ask that standard changes be backed by real use cases or prototype implementations when possible.

Join the community on Reddit at [r/AgentRuntimeProtocol](https://www.reddit.com/r/AgentRuntimeProtocol/) to ask questions, share ideas, or discuss agent development with ARP. The ARP maintainers are active there and on GitHub Discussions/Issues to provide support.

## License

All OSS projects are under the **MIT License**. You are free to use, extend, and integrate ARP in your own projects. See the LICENSE file in each repository for details. Enjoy building with ARP!
