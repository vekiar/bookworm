# Architecture for Flow
Wardley Mapping, DDD, and Team Topologies  
Susanne Kaiser  
Link: https://www.youtube.com/watch?v=Lfzph_5wb9c  

## Notes
Most initiatives that try to optimize are directed at improving parts of the system
Local optimization.
Does not improve the functioning of the whole system.
A system > sum of the parts, when you include interaction between parts.
Building systems:
    1/ building the right thing: aligned to needs? understood the problem? share common understanding?
    2/ building the thing right: engineering practices? pace of change? can we adapt to change?
3 perspectives
    1/ Business Strategy (w/ Wardley Mapping)
    2/ Sofware-Design/Architecture (w/ Domain Driven Design)
    3/ Team-Organization (w/ Team Topologies)
Example: Online School
Challenges: 
    Functional silos
    High handover communication requirements
    Coordination tax
    Fuzzy ownership boundaries
    Delivery bottlenecks
    High operational effort -> on-premises infrastructure
"Local optimization does not improve the performance of the whole"
Tackle the situation from a broader perspective
Understand the environment and challenges we are operating in
Visualize the landscape w/ a Wardley Map
Strategy Cycle
    Purpose: Start with WHY ("high quality education for students")
    Landscape: focus on Students and Teachers as users
        Identify user needs (subject area for which we build a product)
        Anchor of the map that all other components relate to
        Identify components in the "Value Chain"
        Top: most visible to users
        Bottom: most invisible to users
        Visible components will depend on invisible components
        Plot components on x-axis from Genesis->Commodity ("Evolution")
    Climate: impact our business but we have no control over them
        How will landscape evolve and how it will impact our landscape
        E.g. everything evolves from left to right according to supply/demand
            Cloud computing commoditized infrastrucutre
        Characteristics change from "Uncharted" to "Industrialised"
    Doctrine: universal principles an organization can apply to adapt to changes
        e.g. use appropriate methods per evolution stage
            Agile for genesis, or lean for use/buy COTS, or 6Sigma for outsourcing
Optimize for flow of change:
    Cross functional, autonomous teams
    No handover between teams
    Small, long-lived teams
    Team ownership
    Minimizing cognitive load
    Restricting high, on-going x-team communication bandwidth
Four team types of team topologies
    Stream-aligned team -> Fast flow of change
        Needs support from "Platform Team" -> abstracting networking, infrastructure, etc.
        Receives enablement from "Enabling Team"
        Receives support from the "Complicated Subsystems Team"
    Goal is to increase autonomy and reduce cognitive load
Three intraction modes
    Collaboration -> Rapid Discovery
    X-as-a-service -> Predictable Delivery
    Facilitating -> Active Help
Combination of 4 team types and 3 collaboration modes -> organizational effectiveness
    Simplifies / automates applying Wardley doctrines
Finding suitable streams of change
    Where do the most important changes in our system occur?
    Role, task, customer segment, geography
    Focusing on activity-oriented activity streams (this is for the example)
Problem Domain
    Users and their needs constitute the "Problem Domain"
    Business Domain + Needs + Strategy = Software Design
    Ditill the problem domain into sub-domains and discover the *core* domain
        e.g. Core, supporting, generic domains
    Core Domain
        Competitive advantage
        Complex
        Changes often
        Build in-house
    Supporting Domain
        No competitive advantage
        Quite simple
        Does not change often
        Prefer to buy/use off-the-shelf
    Generic Subdomain
        No competitve advantage
        Generally complex
        Does not change often
        Buy off-the-shelf / outsource
Analysis from example
    Core
        Differentiation: high
        Complexity: high
        Change rate: high
        Ubiquity: low
        Strategic investment: high
    Supporting
        Differentiation: low
        Complexity: low
        Change rate: low-medium
        Ubiquity: medium 
        Strategic investment: low-medium 
    Generic
        Differentiation: low
        Complexity: medium-high
        Change rate: low
        Ubiquity: high
        Strategic investment: low
Decomposition into bounded contexts
    Defines where a single domain model can be applied
    Bounded context forms a "unit of mastery, purpose, autonomy"
        can provide different types of boundaries
Find suitable team boundaries
    Optimize for team cognitive load
    Limit the number, type, size of components per team
Cognitive Load
    Novel practices: high (Genesis), Best Practices: low (Commodity)
    Apply to Uncertainty, Rate of Change, Path to Action, Cognitive Load
    Establish clear ownership boundaries
        Bounded context for single teams only
    Identify the services that are needed to support a reliable flow of changes
    Mind dependencies and communication bandwidth between teams
Possible team constellations
    "Platform Team": Compute -> VM, SMTP server, message broker, data storage
Closing potential efficiency gaps (impede fast flow of changes)
    Do not want to build on top of ineffiencies -> multiply
    E.g. custom built components where commoditized components are available (e.g. cloud computing)
A->B?
    Infrastructure components first to address inefficiencies
    New "Platform Team" from members of other stream
        First mandate is migration to cloud
        Replatforming -> modifying the underlying infrastructure while the application architecture remains untouched
        Rest of the team can merge after the migration and / or focus on new subdomains (e.g. Fin/CloudOps?)
    Stream-aligned team 1
        Starts the re-factoring journey
        Members of the "previous" front- and back- end teams
        Remaining members can merge into a temporary team to maintain the legacy monolith
        Discover and assess cloud options for the future bounded context
            e.g. serverless technology
        Can move into ocassional on-demand collaboration
        Evolves into best practices, standards, apis, tools, etc to easily consume the platform
    Stream-aligned team 2,3,...,n
        Supported by evolution of team topologies
            SAT2 can receive coaching and facilitation (inc SaaS) from SAT1
        Can go on their own re-factoring journey
        SAT3 can receive support and facitiliation (inc SaaS) from SAT2
            and so on (but does not seem to be tail-recursive!)
    Enabled organizational structure to adapt to a fast(er) rate of change
    Clear organizational boundaries
Takeaway
    Understand the environment an organization operates and competes in
    Gain domain knowledge and discover the core
    Know what components to build, buy/use, or outsource
    Decomponse the problem domain into modular bounded contexts
    Align teams and evolve their interactions to the system we build and the strategy we plan
    Identify efficiency gaps
    Eliminate bottlenecks and increase software delivery performance
    Respond to changes quickly
    Optimize for a fast flow of change with a focus on improving the performance of the overall system
