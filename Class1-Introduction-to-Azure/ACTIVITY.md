# Interactive Activity: Multi-Region Infrastructure Design

## Objective
Design an Azure infrastructure for a company with global presence.

---

## Scenario Details

**Company Profile:**
- Name: GlobalTech Solutions
- Users: 18,000 globally distributed
- Current Infrastructure: On-premises datacenter (outdated)
- Goal: Migrate to Azure with high availability

**Geographic Distribution:**
- **North America**: 10,000 users (Toronto, New York, Los Angeles)
- **Europe**: 5,000 users (London, Frankfurt, Amsterdam)
- **Asia Pacific**: 3,000 users (Singapore, Tokyo, Sydney)

---

## Activity Template: Your Design

### Part 1: Region Selection (5 min)

Complete this table for your infrastructure:

| Region | User Base | Why Selected | Availability Zones |
|--------|-----------|--------------|-------------------|
| | | | |
| | | | |
| | | | |

**Tips:**
- Match regions close to users for low latency
- Use region pairs for disaster recovery
- Consider data residency laws

---

### Part 2: Subscription Strategy (3 min)

**Decision:** How many subscriptions do you need?

**Options:**
- [ ] 1 Subscription (all resources together)
- [ ] 3 Subscriptions (one per region)
- [ ] Other: _______________

**Justification:**
```
Reasons for your choice:
1. 
2. 
3. 
```

---

### Part 3: Resource Groups Design (5 min)

**For each region, name your resource groups:**

**Example Format:** `rg-[region]-[workload]`

```
North America:
├─ rg-eastus-webapps
├─ rg-eastus-databases
└─ rg-eastus-networking

Europe:
├─ rg-westeurope-webapps
├─ rg-westeurope-databases
└─ rg-westeurope-networking

Asia:
├─ rg-[region]-webapps
├─ rg-[region]-databases
└─ rg-[region]-networking
```

---

### Part 4: High Availability Strategy (2 min)

**For each critical component, answer:**

| Component | Primary Region | DR Region | Failover Method |
|-----------|----------------|-----------|-----------------|
| Web App | | | |
| Database | | | |
| Storage | | | |

---

## Final Deliverable: Simple Diagram

**Draw or describe your infrastructure:**

```
                    GLOBALTECH SOLUTIONS
                    
        ┌─────────────────┬─────────────┬──────────────┐
        │                 │             │              │
    NORTH AMERICA      EUROPE        ASIA-PACIFIC
    (Primary)         (Secondary)    (Tertiary)
        │                 │             │
    ┌───▼───┐         ┌───▼───┐   ┌───▼───┐
    │ RGs   │         │ RGs   │   │ RGs   │
    └───────┘         └───────┘   └───────┘
```

**Backup Strategy:**
- Primary ↔ DR: _________________
- Replication Method: _________________
- RTO (Recovery Time Objective): _________________

---

## Assessment Criteria

Your design should address:
- ✅ Geographic user proximity
- ✅ High availability and disaster recovery
- ✅ Resource organization
- ✅ Cost optimization
- ✅ Compliance/Data residency

---

## Group Discussion (5 min)

**Questions:**
1. Why did you choose those specific regions?
2. How does your subscription strategy support billing/management?
3. What happens if one region fails?
4. Could you optimize costs further?

---

## Answer Key (Trainer Reference)

**Optimal Solution:**
- **Regions:** East US, West Europe, Southeast Asia
- **Subscriptions:** 3 (one per region) OR 1 (centralized management)
- **High Availability:** Use availability zones within regions
- **DR:** Use region pairs (East US ↔ West US)
- **Resource Groups:** Organized by region + workload type

**Common Mistakes to Correct:**
- Choosing too many subscriptions (complexity)
- Not considering region pairs
- Ignoring availability zones
- Poor naming conventions
