# MachineID.io Templates

Starter examples for using MachineID.io with popular AI agent frameworks.

These templates show how to:
- Register each agent or worker with a unique deviceId
- Validate before tasks to prevent runaway scaling
- Enforce plan limits automatically using MachineID.io’s device gate

All templates are MIT licensed · minimal dependencies.

| Framework       | Repo                                                                 | Description                                       |
|-----------------|----------------------------------------------------------------------|---------------------------------------------------|
| Python Starter  | https://github.com/machineid-io/machineid-python-starter             | Universal base template (register + validate)      |
| CrewAI          | https://github.com/machineid-io/crewai-machineid-template            | Controlled fleet execution for CrewAI agents       |
| OpenAI Swarm    | https://github.com/machineid-io/swarm-machineid-template             | Prevent runaway Swarm worker spawning              |
| LangChain       | Coming soon                                                          | LCEL-compatible device gating                      |
| (more weekly)   | —                                                                    | Additional ecosystems are being added regularly    |

→ Docs: https://machineid.io/docs  
→ API: https://machineid.io/api  
→ Generate free org key (3 devices): https://machineid.io  
