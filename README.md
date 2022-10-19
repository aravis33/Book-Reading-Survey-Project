# Book-Reading-Survey-Project

## Summary
How much do Americans read? This dataset is the result of a survey conducted by Pew Research Center in January 2021, February 2019, and January 2018. According to their website, "Pew Research Center is a nonpartisan fact tank that informs the public about the issues, attitudes and trends shaping the world. We conduct public opinion polling, demographic research, content analysis and other data-driven social science research." This survey was conducted over the phone from random calls and includes 1502 people across the United States. The survey questions also focused on how much people use the internet and related technology questions, but for this project I'm only interested in the questions related to books and reading. 
## Relevance
I chose to do this project because I have always loved reading books, and I'm curious to know how much other people read and whether there are characteristics that correlate with how much a person reads. 
## Data Cleaning Notes
Important changes I made to the data:
* I wanted "income" to be an integer so that I can use it in calculations and charts, but the survey only gathered ranges rather than exact numbers. I decided to impute random values in each range. For "$150,000 or more" I decided to guess 150,000-300,000 (200,000 for 2018 & 2019), and for "$10,000 or less" I used the range 1000-9,999. I then found the descriptive statistics for all the answers with numbers and used that to find the interquartile range. I used that range to impute values for those who answered "I don't know" or refused to answer. 
* For the three columns "read_printed_books", "read_audiobooks", and "read_e-books", there were a few "don't know" or refused answers so I changed those to "No" since that is most likely. There were some nulls left in those columns, but they were nearly equal to the number of those who didn't read any books so those questions were not applicable. I decided to also change them to "No" since if they didn't read any books, it follows that they didn't read any of the forms of books.
* In "number_of_books_read" and "age" the interviewers entered exact numbers except for three cases: "97" was entered if the number was 97 or higher, "98" was entered if the person said they didn't know, and "99" was entered if they refused to answer the question. In both columns, I decided to leave the 97s alone because it's unlikely the real number would be much higher than that, and I imputed values for the 98 and 99 with the interquartile ranges.

## Limitations & Ethics
There are several limitations to this dataset. One is that it is survey data -- we only know what people chose to tell the interviewers, so they could have lied or given an inaccurate number. People aren't necessarily good at estimating things, so unless they kept track of how many books they read somewhere and looked it up, it may be inaccurate. There's also no way of knowing if someone was lying about any of their answers. Some variables had a number of missing values where the person said they didn't know or refused to answer the question. Also since the salaries were only ranges in the survey data, they had to be imputed so they aren't the real salaries. Additionally, the interview was conducted over the phone, so people who don't have a phone or don't answer unknown calls will not be represented. However, it should be enough to make some interesting observations if there are any strong correlations, while keeping in mind these limitations. 
As for ethical considerations, there isn't any Personally Identifiable Information in the data. There is demographic data such as age, race, sex and gender, so analysts should be aware of any possible descrimination when interpreting the data.
## Key Questions
* Are there any demographic variables that correlate with how much a person reads?
* How much do different age groups read? 
* Does income affect how much a person reads? 
* How does reading vary by state?
* Does the way a person reads (by printed book, audiobook, or e-book) correlate with any demographic variables?
* Do younger people read e-books more?
* How many people read printed books v. audiobooks v. e-books?
* Do frequent readers (those who read 20 or more books) have a preference for how they read?
## Citations
Pew Research Center. (2021). 2021 Core Trends Survey [Data set]. Pew Research Center. [DOI/URL](https://www.pewresearch.org/internet/dataset/2021-core-trends-survey/)

Pew Research Center. (2019). Core Trends Survey [Data set]. Pew Research Center. [DOI/URL](https://www.pewresearch.org/internet/dataset/core-trends-survey/)

Pew Research Center. (2018). Jan. 3-10, 2018 - Core Trends Survey [Data set]. Pew Research Center. [DOI/URL](https://www.pewresearch.org/internet/dataset/jan-3-10-2018-core-trends-survey/)
## Tableau Storyboard
[The State of Reading in the U.S.](https://public.tableau.com/views/TheStateofReadingintheU_S_/TheStateofReadingintheU_S_?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link)
