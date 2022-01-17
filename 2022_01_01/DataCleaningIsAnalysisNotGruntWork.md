# Title: DataCleaningIsAnalysisNotGruntWork
## Source: 
## Summary: 

> “cleaning” is just a spectrum of reusable data transformations on the path towards doing a full data analysis.
1. Existing Data Cleaning writing is pretty useless
1. Data Cleaning IS Analysis
> We’re doing cleaning because we want to extract the useful signal from the noise, and we decide certain bits of noise “correctable” at the data point level for that purpose. Therefore, we clean those parts so that they don’t affect our analysis.
> The act of cleaning data is the act of preferentially transforming data so that your chosen analysis algorithm produces interpretable results. That is also the act of data analysis.
1. Cleaning your data allows you to know your data
> You can only make confident statements using your data when you know what’s been collected, what hasn’t been collected, how it’s collected, where are the gotchas, where are the hidden dependencies, etc.
> I’m going to put forth the claim that cleaning the data is a prerequisite to getting a rock solid understanding of the underlying data.
> Don’t trust anyone else’s cleaning.
> Cleaning is a powerful method of becoming familiar with a data set, and also generating the needed data set to arrive at interesting results.
1. Let’s Redefine Data Cleaning as “Building Reusable Transformations”
> I propose that we start thinking of data cleaning as “building reusable transformations”, for two reasons:
> So the act of “cleaning data” is actually building a library of transformations that are largely reusable across multiple analyses on the same data set.
1. Doing Data Cleaning “Better”
    1. First off, never do permanent changes unless you’re REALLY sure
    > When we embark on cleaning and analysis, we’re going to be making a bunch of decisions early on that we might regret in the far future.
        1. always keep a copy of the original data around if at all possible
        1. Data storage is relatively cheap compared to the regret of not being able to undo any mistakes and needing to collect new data.
    1. Next, always leave an unbroken analytical paper trail
        1. Every step in the transformation from raw data to final presentation should have links/references to prior steps.
        > This serves to remind you of what you did to complete an analysis in order to reproduce it at a later date, and it also allows you to answer questions about how the analysis was done (“did you account for X?”)
    1. Goal 1: Fix things that will make your analysis algorithm choke
        1. put in the legwork to analyze the issue and figure it out yourself
    1. Goal 2: Reduce Unwanted Variation
        1. Simple examples are the fixing of spelling and normalizing punctuation. More advanced cases include clustering values into categories.
    1. Goal 3: Eliminate Bias (where you can) 
        1. This is a place where subject matter expertise is critical. 
        1. Experts on a topic are better able to identify places where bias potentially creeps into a data set.
        1. experts also should know how to identify the implicit structural biases of the data set, what hasn’t been collected and can come up with strategies to minimize the damage from those issues.
        1. At this point sometimes it's hard to tell whether you are doing cleaning or analysis
1. I’m making a data set for others, how do I know what to clean?
    1. By far the most important thing to do is to fully document every cleaning decision made in case it’s important in the future


## Further readings: 
## My opinion: 
## Tags: #data #cleaning #data cleaning #analysis  

