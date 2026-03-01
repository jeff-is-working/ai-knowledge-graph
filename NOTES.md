# Research Notes

## Four Levels of Data Visualization (Talk to Find)

**Talk Title:** "Building Attack Graphs and the Algebra of Defense"
**Speaker:** John Lambert - CTO, Corporate VP, and Security Fellow at Microsoft
**Conference:** TBD (also published as Microsoft Security Blog post, Dec 2025)

Recommended by someone who works in data visualization.

The "Four Algebras of Defense" - four data representations for security data:
1. Relational Tables (knowledge data)
2. Graphs (attack graphs)
3. Anomalies
4. Vectors Over Time (temporal analysis)

Key concept: "Defenders think in lists. Attackers think in graphs.
As long as this is true, attackers win."

References:
- Blog post: https://www.microsoft.com/en-us/security/blog/2025/12/09/changing-the-physics-of-cyber-defense/
- GitHub: https://github.com/JohnLaTwC/Shared
- Medium: https://medium.com/@johnlatwc/defenders-mindset-319854d10aaa

## Blog Post Summary: "Changing the Physics of Cyber Defense"

### Core Thesis
Defenders have historically been at a disadvantage, but with better data representations,
hygiene, and collaboration, they can flip the physics of defense in their favor.

### The Four Algebras of Defense
Four ways to represent security data, each specialized for different questions:

1. **Relational Tables** - The traditional tabular world (e.g., KQL queries in Azure Data
   Explorer). Where most defenders live today.
2. **Graphs** - Attack graphs showing how credentials, dependencies, and entitlements connect.
   Lets you ask: "What's the blast radius?", "Can I get from identity A to infrastructure B?",
   "If a threat actor has taken over this node, can they get to our crown jewels?"
3. **Anomalies** - Detecting what's normal vs. abnormal behavior.
4. **Vectors Over Time** - Temporal analysis of security data.

AI can leverage all four algebras simultaneously, operating in a "much more highly dimensional
space" than human analysts - turning each algebra into a new way to detect anomalies.

### Three Pillars of Defense

1. **Build attack graphs** - Think like attackers. Any infrastructure you defend is conceptually
   a directed graph of credentials, dependencies, entitlements, and more. Attackers find
   footholds, pivot within infrastructure, and abuse entitlements and secrets to expand further.
   Reconstruct the "red thread" of activity from siloed logs into a graph.

2. **Create difficult terrain** - Proactive hygiene:
   - Retire legacy systems (harbor vulnerabilities attackers exploit)
   - Manage entitlements continuously (prevent lateral movement)
   - Top-tier asset management (can't protect what you don't know exists)
   - Remove orphaned elements (unused accounts, forgotten servers, abandoned cloud resources)
   - Phishing-resistant MFA
   - Enforce admin access from hardened, pre-identified locations
   - Reduce network noise - enforce predictability so attackers can't hide

3. **Collaborate with competitors** - Over the past decade, the industry shifted from secrecy
   to sharing breach details in trusted forums. What was once taboo is now a mainstay of
   collective defense through trusted security forums, cross-industry intelligence sharing,
   and joint incident response efforts.

### Origin Story
Lambert founded MSTIC (Microsoft Threat Intelligence Center) 10 years ago. First lesson:
to find threat actors you need to think like them - which led to graph-based thinking.

### Relevance to AIKG
The knowledge graph work in this repo is essentially Algebra #2 (Graphs) applied to threat
intelligence data. Potential to expand into the other algebras as well.
