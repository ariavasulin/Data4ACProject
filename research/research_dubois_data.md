# W.E.B. Du Bois 1900 Paris Exposition Data Visualizations: Research

Research compiled for Data 4AC Final Project — Data Reflection (due 3/20/2026)

---

## 1. Accessing High-Resolution Scans of the Du Bois Plates

### Library of Congress (Primary Source)

The Library of Congress holds the original 63 hand-drawn plates (plus additional maps and charts totaling ~72 drawings) in the **African American Photographs Assembled for 1900 Paris Exposition** collection (Microfilm LOT 11931). All plates have been fully digitized at high resolution.

**Key URLs:**
- **Main collection page:** https://www.loc.gov/collections/african-american-photographs-1900-paris-exposition/
- **Charts filtered by subject:** https://www.loc.gov/collections/african-american-photographs-1900-paris-exposition/?fa=subject:charts
- **Georgia/Graphs filter:** https://www.loc.gov/collections/african-american-photographs-1900-paris-exposition/?fa=subject:georgia%7Csubject:graphs
- **Prints & Photographs catalog (browsable):** https://www.loc.gov/pictures/collection/anedub/
- **Collection overview item:** https://www.loc.gov/pictures/item/2005679642/
- **Du Bois-specific materials:** https://www.loc.gov/pictures/collection/anedub/dubois.html
- **About the collection:** https://www.loc.gov/collections/african-american-photographs-1900-paris-exposition/about-this-collection/
- **LOC Blog Post (2014):** https://blogs.loc.gov/picturethis/2014/02/du-boiss-american-negro-exhibit-for-the-1900-paris-exposition/
- **LOC Blog Post (2020):** https://blogs.loc.gov/picturethis/2020/04/african-americans-at-the-turn-of-the-20th-century-a-graphic-visualization/
- **LOC Resource Guide:** https://guides.loc.gov/web-dubois/digital-resources

**Note:** The originals are too fragile to be served physically — the LOC directs all users to the digital images.

### Other Archives & Exhibitions

- **Cooper Hewitt, Smithsonian Design Museum** — Hosted "Deconstructing Power: W. E. B. Du Bois at the 1900 World's Fair" (Dec 2022–May 2023), which displayed 20 of the original data visualizations. Their online collection is at https://collection.cooperhewitt.org/
- **Smithsonian Magazine** — Published a feature with full-color reproductions: https://www.smithsonianmag.com/history/first-time-together-and-color-book-displays-web-du-bois-visionary-infographics-180970826/
- **Book: _W.E.B. Du Bois's Data Portraits: Visualizing Black America_** (Princeton Architectural Press, 2018, ISBN 9781616897062) — Edited by Whitney Battle-Baptiste and Britt Rusert. **First complete publication** of all Du Bois charts in full color. Essential reference.
- **Book: _Black Lives 1900: W.E.B. Du Bois at the Paris Exposition_** (Redstone Press) — Another collection of the plates.

---

## 2. Reconstructed Machine-Readable Datasets (CSV/JSON)

### THIS IS THE CRITICAL FINDING: Yes, datasets exist!

### Anthony Starks's `dubois-data-portraits` Repository (PRIMARY RESOURCE)

**URL:** https://github.com/ajstarks/dubois-data-portraits

This is the single most important resource for our project. Anthony Starks has organized the **#DuBoisChallenge** annually since 2021 (co-founded with Allen Hillery and Sekou Tyler). The repository contains:

- **CSV data files** for each challenge plate, organized by year
- **Original plate images** for reference
- **GeoJSON and shapefiles** for geographic data (maps)
- **A style guide PDF** documenting Du Bois's design specifications

**Challenge data by year:**
- https://github.com/ajstarks/dubois-data-portraits/tree/master/challenge/2022
- https://github.com/ajstarks/dubois-data-portraits/tree/master/challenge/2024
- https://github.com/ajstarks/dubois-data-portraits/tree/master/challenge/2025
- https://github.com/ajstarks/dubois-data-portraits/tree/master/challenge/2026

Each challenge folder (e.g., `challenge01/`, `challenge02/`, etc.) contains:
- The original plate image
- A CSV file with the reconstructed data
- A README describing the challenge

**2024 Challenges covered these plates:**
| Challenge | Plate | Topic |
|-----------|-------|-------|
| challenge01 | Plate 06 | Negro Population of Georgia by Counties, 1870, 1880 |
| challenge02 | Plate 12 | Slave and Free Negroes |
| challenge03 | Plate 19 | Acres of Land Owned by Negroes in Georgia |
| challenge04 | Plate 01 | The Georgia Negro (slave trade routes) |
| challenge06 | Plate 54 | Amalgamation data |
| challenge07 | Plate 47 | Illiteracy rates |

**2024 thematic organization (Pan-African flag colors):**
- Red challenges (1–3): Population and land ownership
- Black challenges (4–6): Demographics and racial composition
- Green challenges (7–9): Education and freedom statistics
- Combination challenge (10): Multi-chart statistical overview

**2026 focus:** Maps and geography in the collection.

**Important caveat:** Not all 63 plates have been digitized into CSV. Some data required manual estimation from the original visualizations (e.g., reading values off hand-drawn bars). For some plates, participants used Excel to estimate values from visual inspection of the originals.

### TidyTuesday Du Bois Datasets

The **#DuBoisChallenge** was featured as part of **TidyTuesday** (a weekly R data visualization event) in 2021 and 2022. TidyTuesday datasets are typically available as clean CSV files.

### Summit LLC Du Bois Challenge Repository

**URL:** https://github.com/summitllc/Du-Bois-Challenge-2024

Contains Jupyter Notebooks (98% of codebase) and R code (2%) recreating Du Bois visualizations. Includes Data Input and Data Output folders with datasets.

### Other Dataset Sources

- **Ed Riessen's matplotlib tutorial** (2024): https://www.edriessen.com/2024/02/07/developing-du-boiss-data-portraits-with-python-and-matplotlib/ — Walks through recreating plates using Python/matplotlib with the challenge CSV data
- **dataxdesign.io**: https://dataxdesign.io/chapters/dubois — "Between Data and Truth: W.E.B. Du Bois's Data Portraits" — analytical resource

---

## 3. Who Collected the Original Data?

### Data Collection Team

- **W.E.B. Du Bois** — Lead researcher, compiler, and intellectual architect. Received a gold medal at the Exposition as "collaborator" and "compiler."
- **Atlanta University students** — Du Bois led a team of students who drew and compiled the 63 poster-sized charts. The plates were "prepared and executed by Negro students under the direction of Atlanta University."
- **Thomas J. Calloway** — Named "special agent" for the Exposition; co-organized the planning, collection, and installation with Du Bois.

### The Atlanta Sociological Laboratory

Du Bois directed the **Atlanta Sociological Laboratory**, which published the annual **Atlanta University Study of the Negro Problems** (a 20-volume monograph series, 1895–1917). This laboratory was:

- The **first American school of sociology** (predating the Chicago School)
- The **first to use method triangulation** (combining census, survey, and ethnographic data)
- The **first to use "insider citizen researchers"** — members of local Black communities across the nation who collected data
- The **first to institutionalize public acknowledgment of research**

### Data Sources

The visualizations drew from:
1. **U.S. Census data** (1790–1890)
2. **Atlanta University sociological studies** — original empirical data collected by Du Bois's lab
3. **State and county records** (especially Georgia)
4. **Patent Office records** (200 patents by African Americans)
5. **Educational institution records** (Fisk, Howard, Tuskegee, Hampton, etc.)
6. **Du Bois's own fieldwork** — including _The Philadelphia Negro_ (1899)

---

## 4. Populations Represented: What's Included and Excluded

### What IS Represented

**Geographic scope:**
- **National:** U.S.-wide data on African American population, literacy, and occupations
- **State-level:** Heavy focus on **Georgia** as a case study (roughly half the plates)
- **International comparisons:** Literacy rates compared to other nations
- **Historical slave trade routes** (Africa to Americas)

**Topics covered (Du Bois's 10 stated goals for the exhibit):**
1. History of the Negro
2. Education of the race
3. Effects of education on illiteracy
4. Effects of education on occupation
5. Effects of education on property
6. Mental development (books, pamphlets, newspapers by Black authors)
7. Mechanical genius (patents granted)
8. Business and industrial development
9. Self-organized church work, especially in education
10. General sociological study of racial conditions in the U.S.

**Specific variables:** Population growth (1750–1890), property ownership, land acreage, real estate wealth, household/kitchen furniture value, income and expenditure budgets, occupations, literacy rates, school enrollment, mortality.

**Time period:** Primarily 1790–1900, with emphasis on the period since Emancipation (1865–1900), showing "35 years of progress."

### What IS NOT Represented / Limitations

- **Geographic bias:** Georgia is heavily overrepresented; many states are not covered at the local level
- **Urban/rural:** The Philadelphia Negro covered urban Black life, but the Paris plates focus more on rural Georgia
- **Gender:** Limited disaggregation by gender in most plates
- **Class diversity:** Tends to emphasize progress narratives (property acquisition, literacy gains) — may underrepresent the most marginalized within the Black community
- **Indigenous peoples:** Not included — the exhibit is specifically about African Americans
- **West and Midwest:** Very limited data on Black populations outside the South
- **Qualitative experience:** The data captures metrics but not the lived experience of Jim Crow violence, lynching (though Du Bois wrote about these elsewhere)
- **Intentional framing:** Du Bois deliberately selected data to counter racist narratives — this is both a strength (counter-data) and a limitation (advocacy framing)

---

## 5. Existing GitHub Repos, Datasets, and Educational Materials

### GitHub Repositories

| Repository | Description | Language |
|-----------|-------------|----------|
| [ajstarks/dubois-data-portraits](https://github.com/ajstarks/dubois-data-portraits) | **Primary resource.** Recreations + challenge data (CSV, GeoJSON). Includes style guide. | decksh |
| [summitllc/Du-Bois-Challenge-2024](https://github.com/summitllc/Du-Bois-Challenge-2024) | Jupyter notebooks (98%) and R recreations of 2024 challenge | Python, R |
| Various TidyTuesday contributions | 2021/2022 TidyTuesday featured Du Bois data | R (mostly) |

### Educational Materials & Curricula

- **Zinn Education Project**: _W. E. B. Du Bois's Data Portraits: Visualizing Black America_ — Teaching materials for high school and adult learners. https://www.zinnedproject.org/materials/du-bois-data-portraits/
- **California History-Social Science Project (UC Davis)**: "Data Visualizations in the Classroom — Re-imagining W.E.B. Du Bois's Data Portraits" (Parts 1 & 2). https://chssp.ucdavis.edu/events/data-visualizations-classroom-part-2-re-imagining-web-du-boiss-data-portraits
- **Teachers Institute curriculum unit** (Yau): Unit on Du Bois, accordion books, data portraits, and community surveys. Students conduct surveys, create data portraits, and design art proposals. https://theteachersinstitute.org/wp-content/uploads/2023/10/Yau-L-Unit.pdf
- **PBS NewsHour Classroom**: "What I learned from the data visualization genius of W.E.B. Du Bois" https://pbs.org/newshour/classroom/2023/04/discovering-the-data-visualization-genius-of-w-e-b-du-bois
- **Art History Teaching Resources**: "Take A Closer Look At (and Teach) W.E.B. Du Bois's Afrofuturist Data Visualizations from 1900" https://arthistoryteachingresources.org/2019/04/take-a-closer-look-at-and-teach-w-e-b-du-boiss-afrofuturist-data-visualizations-from-1900/
- **LOC Teaching with the Library blog**: https://blogs.loc.gov/teachers/2020/02/du-bois-in-paris-exposition-universelle-1900/
- **STA 313 at Duke University**: Lecture slides on Du Bois visualizations. https://vizdata.org/slides/10/10-web-dubois.html
- **Bellevue College Faculty Commons**: Uses Du Bois data portraits for teaching. https://www.bellevuecollege.edu/facultycommons/2023/05/31/w-e-b-du-boiss-data-portraits-visualizing-black-america/
- **CHANCE Magazine** (2023): "Analyzing and Recreating Data Visualizations of W.E.B. Du Bois" https://www.tandfonline.com/doi/full/10.1080/09332480.2023.2179279

### Design & Style Resources

- **Du Boisian Visualization Toolkit** (Dignity & Debt Network): Design specifications and coding tools for creating Du Bois-style graphs. https://www.dignityanddebt.org/projects/du-boisian-resources/
- **Du Bois Style Guide PDF**: https://www.dignityanddebt.org/uploads/dubois-style.pdf (included in ajstarks repo too)
- **Chimdi Nwosu YouTube channel**: Video tutorials for recreating Du Bois visualizations

---

## 6. Most Suitable Plates for a High School Data Science Curriculum

### Chart Type Distribution (of 58 data visualizations)

| Chart Type | Count | Notes |
|-----------|-------|-------|
| Bar charts (horizontal/vertical) | ~30 | **Most common.** Best for beginners. |
| Area/spiral charts | ~10 | More complex, innovative forms |
| Line graphs | 3 | Simple but fewer available |
| Maps | ~5 | Require GIS knowledge |
| Pie/proportional charts | ~5 | |
| Other innovative forms | ~5 | Wrapped bars, Georgia-shaped charts |

### Recommended Plates for HS Curriculum (Most Accessible Data)

**Tier 1 — Simplest (standard bar charts with CSV data available):**

| Plate | Title | Why It's Good for HS |
|-------|-------|---------------------|
| Plate 12 | Slave and Free Negroes | Simple proportional data over time. Historical narrative. CSV available. |
| Plate 19 | Acres of Land Owned by Negroes in Georgia | Year-by-year progression. Simple bar chart (shaped like Georgia!). CSV available. |
| Plate 47 | Illiteracy rates (comparative) | Cross-national comparison. Good for critical thinking about context. CSV available. |
| Plate 06 | Negro Population of Georgia by Counties | Map + population data. Good for geographic thinking. GeoJSON available. |

**Tier 2 — Moderate complexity:**

| Plate | Title | Why It's Interesting |
|-------|-------|---------------------|
| Plate 54 | Amalgamation data | Racial composition over time. Provocative for discussion. |
| Plate 01 | The Georgia Negro (slave trade routes) | Geographic/historical narrative. Powerful opening. |
| Plate 18 | Value of Land Owned by Georgia Negroes | Economic progress narrative. |

**Tier 3 — Advanced (innovative chart types, good for stretch goals):**

| Plate | Title | Why It's Advanced |
|-------|-------|------------------|
| Plates 17, 26, 62 | Wrapped bar charts | Du Bois's innovation — bars that wrap around like a spiral when values are very large. Published as a research paper: "Du Bois Wrapped Bar Chart" (CHI 2020). |

### Key Pedagogical Considerations

- **Bar charts are the best starting point** — they're the most common Du Bois chart type and map cleanly to matplotlib's `barh()` and `bar()` functions
- The **Du Bois style guide** provides specific color palettes (dominant pink/red with 2-3 solid accent colors) that students can replicate
- The **#DuBoisChallenge structure** (10 challenges per year) provides a built-in curriculum arc
- The California History-Social Science Project has already piloted "re-imagining Du Bois" activities in classrooms

---

## 7. Existing Python/Matplotlib Recreations

### Python/Matplotlib

- **Ed Riessen's tutorial** (2024): Step-by-step matplotlib recreation of Du Bois challenge plates. Uses the CSV data from ajstarks repo. https://www.edriessen.com/2024/02/07/developing-du-boiss-data-portraits-with-python-and-matplotlib/
- **Summit LLC Jupyter Notebooks**: 98% Jupyter notebook codebase recreating 2024 challenge plates in Python. https://github.com/summitllc/Du-Bois-Challenge-2024
- **Chimdi Nwosu**: YouTube video tutorials recreating Du Bois visualizations (tools not confirmed but tutorials exist)
- **Various #DuBoisChallenge participants**: Many have shared Python/matplotlib solutions on Twitter/X and personal blogs

### R/ggplot2

- **TidyTuesday 2021/2022**: Dozens of R recreations shared via the #TidyTuesday hashtag. The TidyTuesday database of tweets contains images and links to R code.
- **DuBois Challenge 2022 (Jo Hardin)**: https://hardin47.github.io/TidyTuesday/2022-02-15/DuBois2022.html
- **Speaker Deck presentation by Starks**: https://speakerdeck.com/ajstarks/recreating-the-dubois-data-portraits

### Other Tools

- **Tableau**: Multiple recreations via the #DuBoisChallenge
- **Flourish**: https://flourish.studio/blog/masters-web-dubois/
- **Nightingale articles**: Multiple deep-dive articles by Jason Forrest analyzing Du Bois's design techniques with modern recreations: https://nightingaledvs.com/recreating-historical-dataviz-three-tricks-i-learned-in-the-du-bois-data-visualization-challenge/

---

## 8. Counter-Narratives: Possibilities and Limitations

### The Exhibit as Counter-Data

Du Bois's visualizations were explicitly designed as **counter-narratives** to the dominant racial "science" of the era. In 1900:
- **Scientific racism** and **Social Darwinism** were mainstream academic positions
- **Eugenics** was gaining institutional support (the Eugenics Record Office would be founded in 1910)
- The data Du Bois chose to visualize — rising literacy, growing property ownership, educational advancement — directly refuted claims of Black biological inferiority
- The exhibit won **17 medals** including 2 Grand Prix and a Gold Medal for Du Bois personally

### Possibilities for Curriculum Use

1. **Data as argument**: Du Bois shows that data visualization is never neutral — it's always making an argument. This is a foundational data justice insight.
2. **Counter-data praxis**: The visualizations model what scholars now call "counter-data" — using empirical evidence collected by marginalized communities to challenge dominant narratives. This connects directly to Data 4AC themes.
3. **Insider research methodology**: Du Bois pioneered the use of community members as data collectors ("insider citizen researchers"), anticipating participatory action research by decades.
4. **Design as rhetoric**: Du Bois's bold color choices, innovative chart types, and deliberate framing choices show students how design decisions shape data interpretation.
5. **Historical continuity**: Comparing Du Bois's 1900 counter-data with contemporary data justice projects (e.g., Data for Black Lives, the Mapping Police Violence project) shows how the tradition continues.
6. **Afrofuturism**: Scholars like Britt Rusert frame Du Bois's visualizations as proto-Afrofuturist — using data to imagine and argue for a different future.

### Limitations and Critical Considerations

1. **Respectability politics**: Du Bois's framing emphasizes progress, uplift, and comparison to white norms. This can reinforce the idea that Black people must "prove" their worth through metrics. Students should critically examine whose standards define "progress."
2. **What's missing**: The visualizations don't capture lynching, voter suppression, or daily racial terror. The data shows "progress since emancipation" but elides ongoing violence. This absence is itself worth discussing.
3. **Audience and power**: The exhibit was created for a European audience at a World's Fair. Du Bois was making a case _to power_. Students should consider: who is the audience for counter-data, and how does audience shape what data is collected?
4. **Individual vs. structural**: The data focuses on aggregate metrics of Black achievement but may not capture structural barriers. Rising literacy doesn't mean equal schools existed.
5. **Temporal distance**: The specific data (1870–1900 Georgia) requires historical contextualization that may be challenging for high school students without support.
6. **Eugenic data for comparison**: To fully teach Du Bois as counter-narrative, you'd ideally compare with actual eugenic data visualizations from the era (e.g., Galton, the ERO). This requires careful pedagogical framing to avoid amplifying harmful content.

### Key Scholarly References

- **Battle-Baptiste, Whitney & Britt Rusert, eds.** _W.E.B. Du Bois's Data Portraits: Visualizing Black America._ Princeton Architectural Press, 2018.
- **Rusert, Britt.** _Fugitive Science: Empiricism and Freedom in Early African American Culture._ NYU Press.
- **D'Ignazio, Catherine & Lauren F. Klein.** _Data Feminism._ MIT Press, 2020. (Discusses visualization, power, and embodied data — connects to Du Bois's work conceptually.)
- **Jason Forrest's 5-part Nightingale series**: Deep analysis of Du Bois's visualization techniques and legacy. https://nightingaledvs.com/
- **CTData**: "W.E.B. Du Bois Data Portraits as Lessons for Equitable Data Work" https://www.ctdata.org/blog/web-du-bois-data-portraits-as-lessons-for-equitable-data-work-equity-in-data-community-of-practice
- **Data Literacy Blog**: "How W.E.B Du Bois Used Data Visualization to Debunk Social Darwinism" https://dataliteracy.com/web-du-bois-story-of-resilience/
- **Tableau blog**: "How W.E.B. Du Bois used data visualization to confront prejudice" https://www.tableau.com/blog/how-web-du-bois-used-data-visualization-confront-prejudice-early-20th-century
- **Sharon Lohr**: "W.E.B. Du Bois's Serpentine Bar Chart" https://www.sharonlohr.com/blog/2019/2/4/web-du-boiss-bar-charts
- **CHI 2020 paper**: "Du Bois Wrapped Bar Chart: Visualizing Categorical Data with Disproportionate Values" https://dl.acm.org/doi/10.1145/3313831.3376365

---

## Summary: Project Feasibility Assessment

| Question | Answer |
|---------|--------|
| Can we access all 63 plates? | **Yes** — LOC has high-res digital scans, all free |
| Do machine-readable datasets exist? | **Yes, partially** — ajstarks repo has CSV for ~30+ plates across challenge years. Some require manual data extraction. |
| Can students recreate in matplotlib? | **Yes** — Ed Riessen tutorial + Summit LLC notebooks provide working Python examples |
| Is there a built-in curriculum structure? | **Yes** — #DuBoisChallenge provides 10 challenges/year with difficulty tiers |
| Are there existing teaching materials? | **Yes** — Zinn Project, UC Davis CHSSP, PBS, LOC all have materials |
| Does this connect to Data 4AC themes? | **Strongly** — counter-data, insider research, data justice, power in visualization |

### Recommended Next Steps

1. **Clone the ajstarks repo** and inventory which plates have CSV data vs. which need manual extraction
2. **Select 5–8 plates** across difficulty tiers for the curriculum module
3. **Fork/adapt Ed Riessen's matplotlib tutorial** for high school level
4. **Pair each plate** with a critical reflection prompt connecting to data justice concepts
5. **Consider adding a "create your own counter-data portrait" activity** where students visualize data about their own community
