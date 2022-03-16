# Title: MigrationsDoneWell
## Source: https://newsletter.pragmaticengineer.com/p/migrations-done-well-part-1?token=eyJ1c2VyX2lkIjozMjIwMjc5MywicG9zdF9pZCI6NTA0MDMyNTQsIl8iOiJFOE53SSIsImlhdCI6MTY0NzM3MjQwNiwiZXhwIjoxNjQ3Mzc2MDA2LCJpc3MiOiJwdWItNDU4NzA5Iiwic3ViIjoicG9zdC1yZWFjdGlvbiJ9.FmrSdvF7sWTQK7vqicx2pMfIrJ8HW_sARe9mVXoy3uY&s=r 
## Summary:

The story of 4 different migrations:
1. Migration with planned downtime
1. Migration gone terribly wrong (UK bank TSB) - ended up locking out ~2 million customers of their accounts
1. Zero downtime migration (Uber) - zero downtime, but long tail of the migration stretched out for years causing some problems
> Migration long-tails are common, risky and often cause outages, just like they did in this case.

Types of migrations:
1. Service replacement
1. Service integration (integrate a new service or approach)
    1. Examples: new API use, migrate to a new version of an external service
1. Service extraction
    1. Seems easy, but it can be risky
1. Code migration
    1. Challanges: large-scale change, hard to rollback, harder to test in production
    1. Examples: JS to Typescript, upgrading to new major version of a lib, changing coding patterns
1. Data migration
    1. One of the riskiest, because
        1. Difficult to roll back
        1. Difficult to do in an atomic way (that's why data migration is easier to do with downtime)
        1. Data migrations are often tied to code changes
        1. More edge cases to worry about 
1. Infrastructure migrations
    1. Riskiest, as they impact all services using that infrastructure
1. Service or tool upgrades

## Tags: #migrations #pragmaticengineer #softwareengineering #usecase #bestpractice  

