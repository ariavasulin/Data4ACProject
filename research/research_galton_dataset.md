# Galton Height Dataset — Research for Data 4AC Final Project

*Compiled 2026-03-18 for Data Reflection (due 3/20)*

---

## 1. Where to Download the Full Dataset

The Galton height dataset (205 families, 898–934 observations depending on version) is widely available:

### R Packages
- **HistData** package: `install.packages("HistData")` → `data("GaltonFamilies")` (934 obs, 8 variables — the most complete version)
- **mosaicData** package: simpler 2-variable version
- **UsingR** package: another R source

### Direct CSV Downloads
- **GitHub Rdatasets**: [GaltonFamilies.csv](https://github.com/vincentarelbundock/Rdatasets/blob/master/csv/HistData/GaltonFamilies.csv) — direct CSV
- **Harvard Dataverse**: [doi:10.7910/DVN/T0HSJ1](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/T0HSJ1) — public domain
- **openICPSR**: [Project 100863](https://www.openicpsr.org/openicpsr/project/100863/version/V1/view) — public domain
- **AppState Statistics**: multiple CSV versions at [stat-jet-asu.github.io](https://stat-jet-asu.github.io/Datasets/InstructorDescriptions/galtonheightdata.html)

### Kaggle
- [Galton Height Data](https://www.kaggle.com/datasets/jaorcovre/galton-height-data)
- [Galton's Height Data - Multiple Linear Regression](https://www.kaggle.com/datasets/fundal/galtons-height-data-multiple-linear-regression)

### Python
- **statsmodels**: `from statsmodels.datasets.galton import load` (simpler 2-variable version)

### Original Transcription
- [J.A. Hanley's McGill website](https://jhanley.biostat.mcgill.ca/galton/) — transcribed from Galton's original notebooks by Beverly Shipley at UCL

### Other
- **Wolfram Data Repository**: [Galton Parent and Child Height Data](https://datarepository.wolframcloud.com/resources/Galton-Parent-and-Child-Height-Data/)
- **Not on UCI ML Repository** — despite being a canonical dataset, it's not hosted there

---

## 2. Data Format and Variables

Two main versions circulate:

### Simple Version (928 observations, 2 variables)
| Variable | Type | Description |
|----------|------|-------------|
| `parent` | numeric | Mid-parent height: (father + 1.08 × mother) / 2, in inches |
| `child` | numeric | Child's height in inches |

### GaltonFamilies Version (934 observations, 8 variables) — **recommended**
| Variable | Type | Description |
|----------|------|-------------|
| `family` | factor | Family identifier (1–205) |
| `father` | numeric | Father's height in inches |
| `mother` | numeric | Mother's height in inches |
| `midparentHeight` | numeric | (father + 1.08 × mother) / 2 |
| `children` | integer | Total number of children in family |
| `childNum` | integer | Birth order of this child |
| `gender` | factor | "male" or "female" |
| `childHeight` | numeric | Child's height in inches |

### Key Data Characteristics
- Heights recorded in **1-inch class intervals** (not continuous measurements)
- Non-integer values used for class interval centers
- All **female heights pre-multiplied by 1.08** before analysis (Galton's "transmutation")
- Original dataset had **963 children**; cleaned to 934 with numerical values
- Observations deleted where heights recorded as "tall," "short," "idiotic," or "deformed" (qualitative entries Galton used for some individuals)
- Family sizes range from 1 to 15 children

---

## 3. Who Created This Data & Collection Methodology

### Creator
**Francis Galton** (1822–1911), English polymath, half-cousin of Charles Darwin, and founder of the pseudoscience of eugenics.

### Original Publication
Galton, F. (1886). "Regression Towards Mediocrity in Hereditary Stature." *Journal of the Anthropological Institute of Great Britain and Ireland*, 15, 246–263.

### Collection Method
Data was collected through Galton's **Anthropometric Laboratory** at the **International Health Exhibition of 1884** at South Kensington, London:

- **Fee-based participation**: Visitors paid **3 pence** to have measurements taken
- **Measurements included**: height, weight, strength, hearing, sight, smell, and other physical characteristics
- **Scale**: 9,337 people measured at the initial exhibition; 3,678 more after the lab relocated to a permanent site
- **Recording**: Results entered on a card for participants to keep
- **Stated purpose**: "To show the public the simplicity of the instruments and methods by which the chief physical characteristics of man may be measured and recorded"

### The 1.08 Multiplier for Female Heights
Galton "transmuted" all female heights to male equivalents by multiplying by **1.08**:
- **Rationale**: Mean father height was ~8% higher than mean mother height; male children were also ~8% taller than female children on average
- **Application**: Used in calculating mid-parental height: H_mid = (H_father + 1.08 × H_mother) / 2
- **Modern assessment**: Cole (2000) showed 1.08 is close to optimal for this compensation. Hanley (2004) questioned whether the adjustment was appropriate in his reanalysis of Galton's raw data.

### What Galton Was Actually Doing
Galton's purpose was not neutral scientific curiosity. He was trying to demonstrate that **physical traits are heritable** in predictable ways, which he believed justified **selective breeding** (eugenics) to "improve" the human population. The height data was part of his broader program to show that human characteristics—including intelligence, morality, and "civic worth"—were transmitted from parent to child.

---

## 4. Who Is Included / Excluded

### Included
- **205 families** from Victorian England
- **486 sons and 476 daughters** (963 total children; 934 with usable numerical data)
- Parents and their **adult** children (mature height only)
- Family sizes range from 1 to 15 children

### Excluded
- Children whose heights were recorded qualitatively ("tall," "short," "idiotic," "deformed") — deleted from cleaned datasets
- This accounts for the discrepancy between 963 original entries and 898–934 in cleaned versions

### Population Represented
- **Socioeconomic status**: Almost certainly **middle to upper-middle class Victorian families**. The 3-pence fee was modest but the exhibition context (leisure activity at South Kensington) implies disposable income and time. Participation in a scientific measurement study also implies education and cultural alignment with scientific institutions.
- **Geographic**: **England, primarily London area** — participants at the South Kensington exhibition
- **Racial composition**: Almost certainly **exclusively white** Victorian English families. Victorian England's class structure was deeply racialized; Galton's eugenic ideology centered on "improving" the white English race; there is no evidence of deliberate inclusion of diverse populations.
- **Gender**: Both male and female children are included, but female heights were "transmuted" to male equivalents, effectively erasing sex-based height differences in the analysis.

### Critical Observation
The dataset represents a **highly selective, privileged subset** of Victorian England. It cannot be generalized to other populations, time periods, or socioeconomic groups. The selection process was not random sampling—it was convenience sampling from exhibition visitors who self-selected to pay for measurement.

---

## 5. Known Limitations, Biases, and Issues

### Measurement Issues
1. **Height rounding bias**: Heights recorded in 1-inch class intervals with "strong bias in favor of integral inches"—observations are unequally distributed. Non-integer values partially compensate but bias remains.
2. **The 1.08 multiplier**: Transmuting women into men through multiplication is conceptually and statistically problematic. It conflates sex differences and imposes a single ratio across all heights.
3. **Measurement error**: No accounting for measurement errors in either dependent or independent variables. Modern errors-in-variables (EIV) regression models would be more appropriate.
4. **Model specification**: Han et al. (2015) identified "fundamental drawbacks in variable and model selection" and previously undiscovered **nonlinearity** in the data.

### Selection Bias
- **Self-selection**: Participants chose to visit the exhibition and pay the fee
- **Class bias**: Likely excludes working class, poor, and marginalized populations
- **Racial homogeneity**: Effectively a whites-only dataset from a whites-only social context
- **Geographic limitation**: London-area families only

### Historical Context
- Victorian nutritional standards affect height distributions differently by class
- Class-based height differences were more pronounced in the 1880s than today
- Data reflects a specific historical moment, not universal biological patterns

### Analytical Issues
- Strong regression bias in least squares estimation leads to "alternative conclusions on the true relationships between heights of child and parents" (Han et al., 2015)
- The concept of "regression to the mean" (which Galton named) is a statistical artifact, not a biological mechanism—but Galton interpreted it as evidence for his hereditary theories

---

## 6. Availability in Common Data Science Formats

| Source | Format | Version | Access |
|--------|--------|---------|--------|
| HistData R package | R data frame | GaltonFamilies (934 obs, 8 vars) | `install.packages("HistData")` |
| mosaicData R package | R data frame | Simple (898 obs) | `install.packages("mosaicData")` |
| GitHub Rdatasets | CSV | GaltonFamilies | Direct download |
| Harvard Dataverse | CSV | Multiple versions | Public, DOI-linked |
| Kaggle | CSV | Multiple versions | Free account required |
| statsmodels (Python) | Python dataset | Simple 2-var version | `from statsmodels.datasets.galton import load` |
| Wolfram Data Repository | Wolfram format + CSV | Comprehensive | Free access |
| openICPSR | CSV | Public domain | Free access |
| J.A. Hanley (McGill) | Various | Original transcription | Academic website |
| **UCI ML Repository** | **Not available** | — | — |

**Recommendation for our project**: Use the **GaltonFamilies** version from the HistData R package or the GitHub Rdatasets CSV. It has the most variables and is the most thoroughly documented.

---

## 7. Possibilities & Limitations for a Justice-Centered High School Curriculum

### Why This Dataset Is Powerful for This Purpose

#### Galton Founded Eugenics
- **Coined the term "eugenics" in 1883**, from Greek meaning "well-born"
- Defined eugenics as "the science of improving stock" and "the study of agencies under social control that may improve or impair the racial qualities of future generations"
- His book *Hereditary Genius* (1869) was the first attempt to "scientifically" prove intelligence was inherited and that upper classes were most intelligent
- After reading cousin Darwin's *Origin of Species*, he believed humanity could be improved through selective breeding

#### Galton's Racism
- Claimed only "higher races" could be successful
- Promoted creating "a homogeneous white race, whose fertility shall markedly dominate that of the black"
- When intelligence tests contradicted his theory (poor people performed as well as wealthy people), he **rejected the test rather than the theory**

#### Statistical Methods Were Built for Eugenics
Galton and his protege **Karl Pearson** developed foundational statistical methods specifically to advance eugenic science:
- **Correlation**: developed to study inheritance of traits for selective breeding
- **Regression**: created to demonstrate "regression toward mediocrity in hereditary stature"
- **Standard deviation**: developed for biometric (body-measurement) analysis
- **Chi-squared test**: created by Pearson for eugenic research
- Galton, Pearson, and Weldon founded the journal **Biometrika** (1901) to advance this program

As one researcher put it: **"The less visible eugenics monuments are embedded in the language, logic, and philosophy of statistics itself."**

#### Real-World Harm
Eugenic science directly contributed to:
- **Forced sterilization laws** in the U.S. (over 60,000 people sterilized)
- **Nazi "racial hygiene" programs** and the Holocaust
- **Immigration restriction** (1924 Immigration Act)
- Ongoing legacies in IQ testing, educational tracking, and algorithmic bias

### Curriculum Possibilities

#### A. "Who Gets Counted?" — Data Collection as Power
- Who was included/excluded from Galton's sample and why?
- How does Victorian class structure shape whose bodies become "data"?
- What does it mean that a convenience sample of wealthy white Londoners became a foundational dataset in statistics?

#### B. The 1.08 Multiplier — Gender in Victorian Science
- Why did Galton "transmute women into men"?
- What does this reveal about who was considered the default human?
- What alternative approaches exist that don't erase sex differences?

#### C. From Measurement to Policy — The Eugenic Pipeline
- Trace the line: Galton's height studies → eugenic theory → forced sterilization laws → Nazi racial programs
- How did "neutral" measurement become a tool of oppression?
- Modern parallels: algorithmic bias, predictive policing, "weapons of math destruction"

#### D. Statistical Methods Are Not Neutral
- Regression was created to show traits "regress to mediocrity"—a concept with ideological weight
- Correlation was designed to study hereditary transmission for selective breeding
- P-values and significance testing were first developed to identify racial differences
- Teaching the math *and* its history simultaneously

#### E. Contemporary Connections
- Algorithmic bias in ML systems that perpetuate historical inequities
- Police risk assessment tools using regression to predict recidivism
- IQ and standardized testing trace directly to eugenic ideology
- Genetic ancestry testing companies resurrecting racial categories

### Frameworks to Draw On
- **Data Feminism** (D'Ignazio & Klein): Examine power, challenge power, elevate emotion and embodiment, consider context
- **QuantCrit** (Quantitative Critical Race Theory): Numbers are not objective—they reflect worldviews of their creators
- **Weapons of Math Destruction** (Cathy O'Neil): How mathematical models reinforce inequality

### Limitations and Risks for Teaching

1. **Risk of reifying harm**: Using eugenic data could inadvertently normalize eugenic categories if not carefully framed
2. **Emotional labor**: For students from groups targeted by eugenics (Black, disabled, Jewish, etc.), this is not abstract history—requires trauma-informed pedagogy
3. **Incomplete representation**: Dataset only shows Victorian white middle-class families; cannot be generalized
4. **Balance required**: Students need both statistical sophistication AND historical/critical analysis skills
5. **Teacher preparation**: Educators need training in history of eugenics and scientific racism before facilitating these conversations

### Pedagogical Best Practices
1. **Start with history, not techniques**: Begin with Galton's eugenic ideology, then introduce regression
2. **Center affected communities**: Include voices of those harmed by eugenics
3. **Make connections explicit**: Don't assume students will see the links—teach them directly
4. **Provide alternatives**: Show how statistics can also be used for liberation and justice
5. **Examine institutional complicity**: Universities, journals, and professional societies upheld eugenics (UCL renamed two buildings named after Pearson in 2020)

---

## Key References

### Dataset Sources
- R HistData Package — [GaltonFamilies documentation](https://vincentarelbundock.github.io/Rdatasets/doc/HistData/GaltonFamilies.html)
- GitHub Rdatasets — [GaltonFamilies.csv](https://github.com/vincentarelbundock/Rdatasets/blob/master/csv/HistData/GaltonFamilies.csv)
- Harvard Dataverse — [doi:10.7910/DVN/T0HSJ1](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/T0HSJ1)
- Hanley, J.A. — [Family heights: Galton's original data](https://jhanley.biostat.mcgill.ca/galton/)

### Galton's Original Work
- Galton, F. (1886). "Regression towards Mediocrity in Hereditary Stature." *JRAI*, 15, 246–263. [PDF](http://www.stat.ucla.edu/~nchristo/statistics100C/history_regression.pdf)

### Data Quality Analysis
- Han, B. et al. (2015). "Galton's Family Heights Data Revisited." [arXiv:1508.02942](https://arxiv.org/pdf/1508.02942)
- Cole, T. (2000). "Galton's midparent height revisited." *Annals of Human Biology*.
- Hanley, J.A. (2004). "'Transmuting' women into men: Galton's family data on human stature." *The American Statistician*.

### Eugenics and Statistics
- Nautilus — ["How Eugenics Shaped Statistics"](https://nautil.us/how-eugenics-shaped-statistics-238014)
- Facing History & Ourselves — ["The Origins of Eugenics"](https://www.facinghistory.org/resource-library/origins-eugenics)
- Genome.gov — ["Eugenics and Scientific Racism"](https://www.genome.gov/about-genomics/fact-sheets/Eugenics-and-Scientific-Racism)

### Teaching Resources
- Yale Teachers Institute — ["Seeing Race in Statistics"](https://teachersinstitute.yale.edu/curriculum/units/2021/2/21.02.08/5)
- CAUSE — ["Critical Values and Transforming Data: Teaching Statistics with Social Justice"](https://causeweb.org/jedi/post/critical-values-transforming-data-teaching-statistics-social-justice)
- ASM — ["Addressing Scientific Racism and Eugenics in the Classroom"](https://asm.org/articles/2023/may/addressing-scientific-racism-and-eugenics-in-the-c)
- D'Ignazio, C. & Klein, L.F. — *Data Feminism* (MIT Press)
- O'Neil, C. — *Weapons of Math Destruction* (Crown)
