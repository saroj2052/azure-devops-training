# Class 1 - 45 Minute Session Agenda

## Session Schedule

| Time | Activity | Duration | Notes |
|------|----------|----------|-------|
| **0:00-0:05** | Welcome & Intro | 5 min | Quick overview of what we'll learn |
| **0:05-0:10** | What is Cloud Computing? | 5 min | SLIDE 1: Benefits & basic concepts |
| **0:10-0:15** | Deployment Models | 5 min | SLIDE 2: Public/Private/Hybrid |
| **0:15-0:22** | Service Models (IaaS/PaaS/SaaS) | 7 min | SLIDE 3: Responsibility matrix |
| **0:22-0:27** | Azure Global Infrastructure | 5 min | SLIDE 4: Regions & Availability Zones |
| **0:27-0:35** | Resource Organization | 8 min | SLIDE 5: Subscriptions & RGs |
| **0:35-0:40** | Azure Portal Demo | 5 min | SLIDE 6: Live walkthrough |
| **0:40-0:50** | **INTERACTIVE ACTIVITY** | 10 min | Design multi-region infrastructure |
| **0:50-0:45** | Summary & Q&A | 5 min | SLIDE 8: Key takeaways |

---

## Presenter Checklist

### Before Session Starts
- [ ] Test Azure Portal access (live demo)
- [ ] Open all slide materials
- [ ] Print activity templates (if needed)
- [ ] Test screen sharing setup
- [ ] Have whiteboard/flip chart ready for activity

### Materials Needed
- [ ] Laptop with Azure Portal access
- [ ] Screen sharing tool
- [ ] Activity templates (printed or digital)
- [ ] Markers/pens
- [ ] Timer for activity (10 min)

### Key Points to Emphasize

**Why Cloud?**
- Cost savings (pay per use)
- Scalability (grow instantly)
- Global reach (deploy anywhere)
- Focus on business, not infrastructure

**IaaS vs PaaS vs SaaS**
- Show the responsibility shift
- Give real-world examples
- Emphasize what Azure manages vs. what you manage

**Multi-Region Strategy**
- Show region map during activity
- Discuss latency impact
- Explain disaster recovery importance

**Resource Organization**
- RGs are NOT like folders (easier to manage)
- Subscriptions = billing boundary
- Wrong organization = management nightmare

### Common Questions to Address

**Q: How many subscriptions do I need?**
A: Typically 1-3: Development, Staging, Production. Organize by business unit if enterprise.

**Q: Can I move resources between resource groups?**
A: Yes, but with limitations. Plan upfront to avoid headaches.

**Q: What happens if an entire region fails?**
A: Your apps/data are lost unless you have backups in another region. That's why we plan for it.

**Q: Is Azure more expensive than on-premises?**
A: Depends on usage. Initial costs may be higher, but long-term ROI usually favors cloud for most companies.

---

## Activity Deep Dive (10 min)

### Step 1: Setup (1 min)
- Divide into groups (4-5 people)
- Hand out activity templates
- Explain the scenario

### Step 2: Work Time (7 min)
- Groups complete all 4 parts:
  1. Select regions
  2. Design subscriptions
  3. Name resource groups
  4. Plan high availability
- Circulate and provide guidance
- Ask probing questions:
  - "Why did you choose that region?"
  - "How will data replicate?"
  - "What's your RTO/RPO?"

### Step 3: Present & Discuss (2 min)
- Each group shares their design (30 sec)
- Ask one follow-up question
- Mention what they got right
- Gently correct misconceptions

---

## Trainer Tips

### Engagement Strategies
1. **Ask questions** - Don't just lecture
   - "Who can explain what a region is?"
   - "Why might Japan be better than Singapore?"

2. **Use analogies** - Make it relatable
   - "Subscription is like a phone plan - billing boundary"
   - "Resource group is like a folder - logical grouping"
   - "Region is like warehouse locations - choose close to customers"

3. **Show real examples** - Concrete beats abstract
   - Show actual Azure cost breakdown
   - Display real company infrastructure design
   - Demonstrate region map with latency data

### Pacing Guidelines
- ⏰ **Don't rush regions/infrastructure** - This is key concept
- ⏰ **Activity is best part** - Give it full 10 minutes
- ⏰ **Save questions for end** - But ask during content for engagement
- ⏰ **Cut portal demo if running behind** - Can record separately

### Handling Challenges

**If people seem confused:**
- Repeat with different language/analogy
- Draw simple diagrams
- Use real-world company example
- Don't assume they know terms like "latency" or "failover"

**If running behind:**
- Skip optional portal walkthrough (can do later)
- Condense resource organization (they'll learn by doing)
- Keep activity - it's where real learning happens

**If finishing early:**
- Open Azure Portal and create test resources together
- Answer deeper questions about their use cases
- Show cost calculator

---

## Success Metrics

By end of session, participants should be able to:

✅ Define cloud computing and its benefits
✅ Explain IaaS, PaaS, SaaS differences
✅ Name Azure regions near their locations
✅ Create a subscription and resource group strategy
✅ Organize resources using naming conventions
✅ Discuss high availability and disaster recovery basics
✅ Navigate Azure Portal (basic)
✅ Design multi-region infrastructure at high level

---

## Homework/Follow-up

After this session, participants should:

1. **Create Free Azure Account**
   - Get $200 free credits for 30 days
   - Set up subscription

2. **Explore Portal**
   - Create a resource group
   - Create a simple resource
   - Find it in portal

3. **Read Materials**
   - Review QUICK-REFERENCE.md
   - Bookmark documentation

4. **Questions for Next Class**
   - Jot down questions
   - We'll answer in Class 2

---

## Transition to Class 2

Next session: **Azure Networking Fundamentals**
- Virtual Networks (VNets)
- Subnets and IP addressing
- Network Security Groups
- VPN & ExpressRoute

**Preparation:**
- Review networking basics (if needed)
- Bring list of questions from today

---

**Have a great session! 🚀**
