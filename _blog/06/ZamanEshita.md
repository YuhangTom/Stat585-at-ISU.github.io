---
author: "Firstname Lastname"
title: "Title of your post"
layout: post
topic: "06"
short-topic: More on reproducibility...
due-date: 2022-03-03
root: ../../
---

## Prompt:

In 2009 one of the associate editors of Biostatistics, Roger Peng, outlined a new policy of [reproducibility](https://doi.org/10.1093/biostatistics/kxp014) for the journal. 

This triggered a response from one of the other associated editors, Niels Keiding, and subsequently a large part of volume 11, issue 3 of Biostatistics was dedicated to a discussion of issues of redproducibility. 


Read through 

- Roger Peng's [initial editorial](https://doi.org/10.1093/biostatistics/kxp014), 

- [Keiding's response](https://doi.org/10.1093/biostatistics/kxq033),

- its five [commentaries](https://academic.oup.com/biostatistics/issue/11/3),  

- Roger Peng's [response to Keiding](https://doi.org/10.1093/biostatistics/kxq032)

- and finally, Keiding's [response to the commentaries](https://doi.org/10.1093/biostatistics/kxq034)

Don't worry about the number of papers listed - these papers are all very short and easy reads. 


Write a blog post addressing the questions: 

1. **Answer each of the following questions with at least 2-3 sentences.**

    1. **Summarize Roger Peng's outline for reproducibility in** *Biostatistics*.
    Roger Peng indicated that to minimize the fraudulent reserach activities and to ensure better understanding of a published research, authors should provive the supplementary materials required to reproduce the main finindings of the research. He mentioned that authors should provide the data used in the research, submit any computer code or reference the tools used to generate the results. Also, the main finding of the reserach should be reproducible, meaning there should be a main script that includes all the work starting from loading the data to produce the results. Authors are responsible to provide any auxiliary files required to run the main script. A traget file is also required with which the reproduced results will be compared. Authors of the research work can submit one or all of these(data,code, and reproducbility ) as supplimentary materials. 
    2. **What are Keiding's main criticisms of the proposal?**. 
    Keiding's main critism of the proposal was about reproducing the exact nemerical result/calculations of the original paper. He said matching the calculation does not do any justice to the significance of the work. There should be more focus on the research problem than just reproducing the results. Research should be problem driven rather than to be method driven. He thinks better understanding of the problem itself, model selection to solve the research problem, collaboration between the scientists and statistisian will  move science forward not just recauculationg someone's elses result.
    3. **Which point in the commentaries speaks to you the most? Why?**
    I personally liked the commentary by Steven N. Goodman. He mentioned that the there is no way we can ignore the points mentioned by Keiding. But Peng's proposal also paves the way to build a netter data and code sharing framework. Steven N. Goodman mentioned few good reasons in his commentary like how sharing meaningful data can be helpful for the researchers in future and third party scrutinization of data will help the analysis to be more accurate. 
    
    4. **How does Keiding respond to the commentary you picked. What are his main points in his response?**
    Keiding agreed with the comments of Goodman, at least partially. He mentioned that he objects the use of the term "minimal reproducibility". Keiding thinks more focus should be put on the research problem and a strong collaboration between the scientists and . He agreed with Goodman on the points that good documentation will ensure better analysis in future for subject matter journals.
    
2. **Describe your experience with a data intensive (collaborative) project. What are the most prominent issues with ensuring reproducibility of research results (focus on dta related aspects)? What would you do differently if you could go back in time?**
I have done a data intensive group project in my NLP(natural language prcessing) course. In that project, we had to find similarities among movies from the  movie summaries.  It was raw data and the size of the data was huge. It also had lot of missing values. We had to process the data to feed them into our deep learning model. We wrote a script to process the data but was unable to run it in our personal computer. We had to run that in ISU server. The processed dataset was also very large. Later calculations were performed on the modified data but since it was so large we could not upload it. We put the scripts in our Git repo but other people might find it hard to reproduce the intermediate data files. Because of space limitations and also for privacy issues we could not upload the processed data. So, if anyone else would like to reproduce the results, they would need speficic computer capacity.

Go to [https://github.com/Stat585-at-ISU/blog-2019](https://github.com/Stat585-at-ISU/blog-2019) for instructions about how to prepare and submit your blog post.


