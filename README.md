# **MachineID.io Templates**
### Drop-in templates for adding device limits, registration, and validation to any agent framework.

MachineID.io is a lightweight device-level gate that enforces per-org limits and ensures every agent validates before running work.  
These templates give you copy-paste integrations for Python agents, CrewAI, OpenAI Swarm, and LangChain.

_All templates are MIT licensed and add no dependencies beyond each framework’s standard requirements._

---

## **Template Library**

| Framework        | Repo Link | Description |
|------------------|-----------|-------------|
| **Python Starter** | https://github.com/machineid-io/machineid-python-starter | Universal register/validate block for any Python agent |
| **CrewAI** | https://github.com/machineid-io/crewai-machineid-template | Safe CrewAI execution with device-level gating |
| **OpenAI Swarm** | https://github.com/machineid-io/swarm-machineid-template | Prevent runaway Swarm worker spawning |
| **LangChain** | https://github.com/machineid-io/langchain-machineid-template | Add device limits to LangChain agents with one small block |
| **(more added weekly)** | — | — |

All templates share the same layout, terminology, and control flow, making it easy to adopt MachineID.io across multiple frameworks.

---

## **Useful Links**

- **Dashboard:** https://machineid.io/dashboard  
- **Generate free org key:** https://machineid.io  
- **Docs:** https://machineid.io/docs  
- **API reference:** https://machineid.io/api  

---

## **The Core Pattern (identical in every template)**

```python
# 1. Choose a unique deviceId per worker
device_id = os.getenv("MACHINEID_DEVICE_ID", "agent-01")


# 2. Register once (idempotent)
register_response = register(org_key, device_id)

# 3. Validate before doing real work
validate_response = validate(org_key, device_id)

if not validate_response.get("allowed"):
    sys.exit("Device not allowed. Reduce usage or upgrade your plan.")
```

**Drop this block into any agent, worker, chain, or background process.**  
It ensures clean scaling, protects you from accidental fleet explosions, and respects per-org limits automatically.

Never wake up to 87 runaway workers again.

---

## **What These Templates Demonstrate**

Every template follows the same MachineID.io workflow:

1. **Assign a `deviceId`** (name)  
2. **Register the device** using `/api/v1/devices/register`  
3. **Validate the device** using `/api/v1/devices/validate`  
4. **Stop or skip work when validation fails**

This simple pattern:

- prevents uncontrolled scaling  
- keeps agent fleets predictable  
- enforces per-org limits cleanly  
- forms the foundation for advanced orchestration and meta-agent systems  

---

## **Who These Templates Are For**

These examples are ideal for:

- AI agent developers adding safety controls  
- Backend teams managing worker fleets  
- Research labs orchestrating large batch runs  
- Automation engineers building self-bootstrapping systems  

---


## **Next Steps**

Pick the template that matches your framework and drop the register/validate block into your agents.  
All integrations follow the same structure, making it easy to mix frameworks or scale up later.

MIT licensed · Built by MachineID.io
