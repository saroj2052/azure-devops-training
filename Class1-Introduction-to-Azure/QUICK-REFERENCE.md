# Azure Quick Reference Guide - Class 1

## Cloud Computing Models

```
┌─────────────────────────────────────────────────────────┐
│ DEPLOYMENT MODELS                                       │
├─────────────────────────────────────────────────────────┤
│ PUBLIC CLOUD: Azure, AWS, GCP (shared resources)       │
│ PRIVATE CLOUD: On-premises (dedicated, secure)         │
│ HYBRID CLOUD: Mix of public + private (flexibility)    │
└─────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────┐
│ SERVICE MODELS (Responsibility Levels)                 │
├─────────────────────────────────────────────────────────┤
│ IaaS (Infrastructure)                                   │
│   └─ VMs, Storage, Networking (You: Apps & Data)      │
│                                                         │
│ PaaS (Platform)                                         │
│   └─ App Service, Databases (You: Apps only)          │
│                                                         │
│ SaaS (Software)                                         │
│   └─ Office 365, Teams (You: User access only)        │
└─────────────────────────────────────────────────────────┘
```

## Azure Infrastructure Hierarchy

```
MANAGEMENT GROUP (Optional)
        ↓
SUBSCRIPTION (Billing boundary)
        ↓
RESOURCE GROUP (Logical container)
        ↓
RESOURCES (VMs, Databases, Storage, etc.)
```

## Key Definitions

| Term | Definition | Example |
|------|-----------|---------|
| **Region** | Geographic area with datacenters | East US, West Europe |
| **Availability Zone** | Separate datacenter in a region | Zone 1, Zone 2, Zone 3 |
| **Subscription** | Billing and access management | Production, Development |
| **Resource Group** | Container for related resources | rg-webapps-prod |
| **Region Pair** | Two regions for DR | East US ↔ West US |

## Azure Regions Quick Reference

**North America:**
- East US, West US, Central US, Canada Central

**Europe:**
- West Europe, North Europe, UK South, France Central

**Asia Pacific:**
- Southeast Asia, East Asia, Australia East, Japan East

**South America:**
- Brazil South

## High Availability Components

| Component | What It Provides |
|-----------|------------------|
| **Availability Zones** | Protect from datacenter failures (99.99% SLA) |
| **Availability Sets** | Protect from planned/unplanned maintenance (99.95% SLA) |
| **Region Pairs** | Protect from regional disasters |
| **Load Balancer** | Distribute traffic across multiple VMs |

## Naming Convention Best Practices

```
Format: [prefix]-[workload]-[environment]-[region]

Examples:
✅ rg-webapp-prod-eastus
✅ vm-api-dev-westeurope
✅ sql-database-staging-southeastasia
❌ resourcegroup1 (too generic)
❌ my-stuff (unclear purpose)
```

## Cost Optimization Tips

1. **Right-size resources** - Don't over-provision
2. **Use Reserved Instances** - Save 30-72% on compute
3. **Spot VMs** - Up to 90% discount for non-critical workloads
4. **Auto-scaling** - Scale based on demand
5. **Clean up unused resources** - Delete what you don't use
6. **Monitor costs** - Use Azure Cost Management

## Common Azure Services by Category

**Compute:**
- Virtual Machines (IaaS)
- App Service (PaaS)
- Kubernetes Service (AKS)
- Functions (Serverless)

**Storage:**
- Blob Storage (object storage)
- File Share (network files)
- Queue Storage (messaging)
- Table Storage (NoSQL)

**Database:**
- SQL Database (relational)
- Cosmos DB (NoSQL, global)
- PostgreSQL, MySQL (open-source)

**Networking:**
- Virtual Network (VNet)
- Load Balancer
- Application Gateway
- VPN Gateway

**Security:**
- Azure Security Center
- Key Vault (secrets management)
- Defender for Cloud

## Important SLAs (Service Level Agreements)

| Service | SLA | Downtime/Year |
|---------|-----|---------------|
| Single VM | 99.9% | 8.7 hours |
| Availability Zones | 99.99% | 52 minutes |
| Availability Set | 99.95% | 4.4 hours |
| Multi-region | 99.999% | 5.2 minutes |

## Disaster Recovery Strategy (RTO/RPO)

| Level | RTO | RPO | Cost | Use Case |
|-------|-----|-----|------|----------|
| **None** | N/A | N/A | Low | Non-critical |
| **Zone Redundant** | Minutes | Minutes | Med | Standard |
| **Region Pair** | Hours | Hours | Med-High | Important |
| **Active-Active** | Seconds | Seconds | High | Critical |

*RTO = Recovery Time Objective (how long to recover)*
*RPO = Recovery Point Objective (how much data loss acceptable)*

## Azure Portal Navigation Shortcuts

| Action | Shortcut |
|--------|----------|
| Open Command Palette | `Ctrl + /` |
| Search Resources | Type in search bar |
| Create Resource | `+ Create a resource` |
| Open Cloud Shell | Click `>_` icon |
| Go to Resource Groups | Home → Resource Groups |

## Checklist: Before Going to Production

- [ ] Resource groups organized by workload/environment
- [ ] Naming convention applied consistently
- [ ] Availability zones enabled where applicable
- [ ] Region pair for disaster recovery configured
- [ ] Backup strategy implemented
- [ ] Monitoring and alerts enabled
- [ ] Cost analysis performed
- [ ] Security best practices implemented
- [ ] Documentation completed
- [ ] Team trained on the infrastructure

## Common Mistakes to Avoid

❌ **Putting all resources in one region** - No disaster recovery
❌ **Too many subscriptions** - Management overhead
❌ **Poor resource naming** - Confusion and errors
❌ **Ignoring costs** - Budget overruns
❌ **No backup strategy** - Data loss risk
❌ **Insufficient monitoring** - Discovering problems too late
❌ **Manual deployments** - Inconsistency and errors

## Next Steps

1. **Setup:** Create free Azure account (credits available)
2. **Practice:** Complete hands-on labs in portal
3. **Design:** Plan your infrastructure
4. **Implement:** Deploy test resources
5. **Monitor:** Learn cost management tools

---

**Need Help?**
- Microsoft Docs: https://docs.microsoft.com/azure/
- Azure Learn: https://learn.microsoft.com/azure/
- Community Forums: https://docs.microsoft.com/en-us/answers/
