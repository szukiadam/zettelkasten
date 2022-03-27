# Title: GhostInTheDataStack
## Source: https://benn.substack.com/p/ghosts-in-the-data-stack?s=r 
## Summary: 

1. One of the ghosts data teams face is knowledge that “exists within expert communities but is never written down."
1. Another is OLAP cubes.
    1. OLAP cubes are just tables, but tables structured in a very particular way.
    1. Rather than a list of objects, OLAP cubes are a table of metrics
    1. Compressing data, it turns out, isn’t lossless. 
    1. OLAP cubes are difficult to understand, as there is no concept that describes what it contains exactly
        1. each row, rather than representing a straightforward noun, is a combinatorial abstraction
    1. OLAP cubes are no longer popular. Modern databases like Redshift, Snowflake, and BigQuery are large enough to count (and do much more complex operations) on top of very large datasets.
    1. Looker was one of the first BI tools to fully discard the OLAP cube

## Further readings: 
1. https://vickiboykis.com/2021/03/26/the-ghosts-in-the-data/
## Tags: #olap #olapcube #datastack #looker #table #cube

