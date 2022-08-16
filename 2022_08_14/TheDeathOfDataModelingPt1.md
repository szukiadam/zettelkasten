# Title: TheDeathOfDataModelingPt1
## Source: https://dataproducts.substack.com/p/the-death-of-data-modeling-pt-1 
## Summary: 

- MDS is drifting away from robust semantic data modeling
- Effective data modeling is driven by **sematincs**
- Data infra today is a mess: data assets are coming from variety of tools and applications with no context
    - Front-end UI
    - 3P tools like Salesforce, JIRA
    - 1st party databases like PostgreSQL
- The problems
    - It separates the producers of data from the onus of ownership or quality.
        - Software engineers can afford to throw data over the fence to data engineers
    - Data Engineers are forced to be 'middlemen' between data producers and consumers
        - DEs operate centrally across different teams -> no deep understanding of business to model data effectively
    - Time to insight is extremely long
        - Data consumers spend a lot of time on understanding what the data represents (what does this column mean?)
- Result: Data Swamp
    - In reality, it is a result of years (sometimes decades) of data debt.
- So why is Data Modeling ‘dead?’
    - 3 main factors
        - Agile
            - Takeaway: In order for data modeling to make a comeback it must embrace Agile. The development of the data model should be iterative, collaborative, and most of all - fast!
        - The shift to engineering-lead organizations
            - SWEs can easily push data from a variety of sources to a DW via ELT
            - SWEs have no data modeling experience: likely never heard of Inmon or Kimball
            - Takeaway: create a solid foundational modeling environment before the first data hire
        - Implementation frictions
            - hard to do it well, need depth of knowledge in various areas
            - Educational friction (hardship): read a 300+ page book (multiple members)
            - Cultural friction: need to convince customers, managers and executives. the more people, the less likely this succeeds
            - Market friction: data effort doesn't generate money -> lower priority
            - Maintenance friction: costs to maintain this system
            - Time-to-value friction: when is it going to be profitable?
> While businesses may reap the rewards of speed in the short term, in the long run they will crash headfirst into a brick wall.
> The complexity of the Warehouse will spiral leaving data consumers spending 50%+ of their time navigating an impenetrable maze of data instead of delivering real value.

## My opinion: 
Have experienced this myself as well. Data modeling has to be a focus point both for orgs and engineers.
## Tags: #datamodeling #mds #moderndatastack #agile #data 

