---
Topic: Step 2 Project Abstract and Annotated Bibliography
Date: 2026-02-26 Thu
References: https://bcourses.berkeley.edu/courses/1552093/assignments/9030629
Author: 
Aliases:
Tags: #1-2-Reference-Materials/1-23-Saved
---

-   Due Friday by 11:59pm
-   Points 10
-   Submitting a website url or a file upload
-   Available after Feb 13 at 11:59pm

Submit an abstract (250 words) that describes your group's early research and developing ideas for the course project. At this stage, your focus should be on framing the problem and refining your critical approach, rather than deciding on final outputs. In addition, include an annotated bibliography of 4-5 sources or multimedia examples. Each annotation (1-2 sentences) should either summarize the source and explain its relevance to your project or narrative approach and technique. These sources may change as your project develops.

This work should be completed collaboratively by your group and drafted in your shared Google Doc. Be sure to create a separate tab (page) in the document for the abstract and annotated bibliography so your collective process and revisions are clearly documented.

---

## DRAFT

**Ariav Asulin, Parshv Patel, Emett Mendel**

### Abstract

The foundational tools of modern data science were built to prove that some people are worth more than others. Galton invented regression to study hereditary superiority. Pearson developed the correlation coefficient to measure "desirable" racial traits. Fisher pioneered significance testing while serving as editor of the *Annals of Eugenics*. These are not footnotes in the history of statistics --- they are the origin story. Yet introductory data science courses teach these methods as if they emerged from a vacuum, stripped of the ideology that motivated their creation.

*Critical Thinking with Data* is a curriculum package (Option B) for high school students (grades 10--12) that teaches introductory statistics and data science --- correlation, regression, distributions, confounding variables, and data visualization --- through the historical entanglement of these methods with the American eugenics movement. Students work through Jupyter notebooks using real historical data: Galton's 898-observation height dataset, demographic records from California's forced sterilization program (which disproportionately targeted Latina, Black, Indigenous, and disabled communities), and W.E.B. Du Bois's 1900 Paris Exposition visualizations presented alongside eugenic propaganda from the same era. The course structure follows an arc from complicity to critique: students first learn the statistical tools by examining the original analyses, then systematically debunk those analyses using the same techniques, and finally study counter-narratives that weaponized data for liberation rather than oppression.

The course is designed to satisfy California's AB 101 ethnic studies graduation requirement while functioning as a quantitative reasoning elective, potentially counting toward UC/CSU Area C mathematics credit. By the end, students will have both the technical vocabulary to enter a university data science program and the critical instincts to ask who collected the data, what categories were chosen, and who benefits from the analysis.

(249 words)

### Annotated Bibliography

1. Clayton, Aubrey. *Bernoulli's Fallacy: Statistical Illogic and the Crisis of Modern Science*. Columbia University Press, 2021.
	- Chapters 3--4 trace how Galton, Pearson, and Fisher developed foundational statistical methods --- regression, correlation, chi-squared, significance testing --- in direct service of eugenic ideology, arguing that their commitment to frequentist inference was itself politically motivated. This is our primary source for connecting specific statistical tools still taught today to their eugenic origins, and excerpts will accompany the Jupyter notebook units where students learn each method.

2. Novak, Nicole L., Natalie Lira, Kate E. O'Connor, Siobán D. Harlow, Sharon L. R. Kardia, and Alexandra Minna Stern. "Disproportionate Sterilization of Latinos Under California's Eugenic Sterilization Program, 1920--1945." *American Journal of Public Health* 108, no. 5 (2018): 611--613.
	- Analyzes 17,362 sterilization records from California institutions using Poisson regression, finding that Latina women faced 59% higher sterilization risk than non-Latina counterparts. This open-access study provides the quantitative demographic data that students will visualize and analyze in our California sterilization notebook unit, making the racial disparities of eugenic policy legible through the same statistical tools used to justify them.

3. Stern, Alexandra Minna, Nicole L. Novak, Natalie Lira, Kate O'Connor, Siobán Harlow, and Sharon Kardia. "California's Sterilization Survivors: An Estimate and Call for Redress." *American Journal of Public Health* 107, no. 1 (2017): 50--54.
	- The most comprehensive demographic analysis of California's eugenic sterilization program, analyzing 19,995 individual records and estimating 831 survivors were still living as of 2016, 68% of whom were sterilized as minors. This companion study to Novak et al. provides the age distributions and temporal trend data for our histogram and time-series exercises, and the fact that most victims were children anchors classroom discussion of eugenic policy's human cost.

4. Galton, Francis. "Regression Towards Mediocrity in Hereditary Stature." *Journal of the Anthropological Institute of Great Britain and Ireland* 15 (1886): 246--263.
	- The paper that introduced regression analysis to statistics, using 898 observations of parent and child heights across 205 families to argue that hereditary traits regress toward a population mean. Students read Galton's original argument, then work with his actual dataset in a Jupyter notebook to compute the regression themselves --- and discover that his own data undermines his hereditary determinist thesis.

5. Du Bois, W.E.B. *The Georgia Negro: A Social Study* and *A Series of Statistical Charts Illustrating the Condition of the Descendants of Former African Slaves Now in Residence in the United States of America*. Infographic plates prepared for the 1900 Exposition Universelle, Paris. Library of Congress, Prints and Photographs Division, Lot 11931. https://www.loc.gov/collections/african-american-photographs-1900-paris-exposition/
	- Sixty-three hand-drawn data visualizations presenting Black economic and social progress in Georgia, created as a direct counter-narrative to the racial science and eugenic propaganda of the era. Students analyze Du Bois's original plates --- his use of color, scale, spiral forms, and annotation --- alongside contemporary eugenic charts, then recreate selected visualizations in matplotlib using reconstructed datasets.

6. Benjamin, Ruha. *Race After Technology: Abolitionist Tools for the New Jim Code*. Polity Press, 2019.
	- Argues that modern algorithmic systems --- facial recognition, predictive policing, automated hiring --- reproduce eugenic logic through what Benjamin calls "the New Jim Code," where discrimination is automated, accelerated, and rendered invisible. This source bridges our historical case study to contemporary relevance, anchoring the final unit where students trace the line from Galton's regression to today's biased algorithms.
