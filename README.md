# **MachineID.io Templates**

Copy-paste examples for using MachineID.io with popular agent frameworks.

| Framework        | Repo Link | Description |
|------------------|-----------|-------------|
| **Python Starter** | https://github.com/machineid-io/machineid-python-starter | Universal register + validate pattern |
| **CrewAI** | https://github.com/machineid-io/crewai-machineid-template | Safe CrewAI agent execution with device gating |
| **OpenAI Swarm** | https://github.com/machineid-io/swarm-machineid-template | Prevent runaway Swarm worker scaling |
| **LangChain** | https://github.com/machineid-io/langchain-machineid-template | Lightweight register/validate control for workers |
| **(more coming weekly)** | — | — |

_All templates are MIT licensed · zero additional dependencies beyond each framework’s normal requirements._

---

## **Useful Links**

- **Dashboard:** https://machineid.io/dashboard  
- **Generate free org key:** https://machineid.io  
- **Docs:** https://machineid.io/docs  
- **API:** https://machineid.io/api  

---

## **What These Templates Show**

Every template demonstrates the same core pattern:

1. **Assign a user-chosen `deviceId`** (name or UUID)  
2. **Register the device** with MachineID.io  
3. **Validate the device before running tasks**  
4. **Stop/skip work if validation fails** or plan limits are reached  

This simple workflow:

- prevents uncontrolled scaling  
- keeps fleets predictable  
- provides a safe foundation for more advanced orchestration systems  
