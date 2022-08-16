# Title: HowToDesignBetterDataPipelines
## Source: https://medium.com/@mrius.carmona/how-to-design-better-data-pipelines-start-with-the-basics-7c4815a125dc
## Summary: 

- Nowadays tools >> processes
- Why do we need documentation?
    - great rotation between engineers
    - tech stack changes quickly: document why a tool was chosen over others
    - easier training for juniors
- Cover these key points when documenting
    - Create a doc pattern in your team (template)
    - Add context (e.g. document Airflow version)
    - Doc for dummies (tip: do not assume anything)
    - Keep it up-to-date (main doc on how the pipeline was created + another doc for changelog)
- Template
    - Project requirements 
        - Why do we want this data? (data usage and impact to business)
        - Where will this be used? (data viz tools)
        - Who should watch the data? (stakeholders)
        - When do you look at this data? (time and data importance)
        - How do you want to look at this data? How should we create this dataset? (methodologies)
    - Data requirements
        - define data frequence updates
        - SLAs
        - data quality checks
        - form of notification
    - Define the MVP
        - minimum that could be rolled to production
    - How would you test your code? And data?
    - Explain which data test will you run. How will you ensure data is correct?
    - Document your tools
        - which tools you use and why (pros and cons, future considerations)
    
- Extras
    - Landmines: all possible issues that can arise
    - Plain english logic + diagrams
    - Add changelog document

## My opinion: 
Nice summary, should be useful in the future. 
## Tags: #datapipelines #documenting #docs #data #desing #basics

