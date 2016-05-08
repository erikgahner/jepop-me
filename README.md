Democracy for the Youth? The Impact of Mock Elections on Voting Age Attitudes
---

### Description and Data Sources
Reproducibility material for Democracy for the Youth? The Impact of Mock Elections on Voting Age Attitudes. 

The `analysis` folder contains all files required to reproduce the figures and information provided in the tables. The `me-prep.R` file requires the original SPSS (`.sav`) files (not available in this repository, available upon request in the [Harvard Dataverse](http://dx.doi.org/10.7910/DVN/AIP0V8)) and creates the `me-survey.csv` file. The `me-analysis.R` combines individual-level data (`me-survey.csv`) with the municipality data (`me-context.csv`), estimate the models and create Figure 1 and Figure 2. 

The survey data used in this project stems from:

- Kommunalvalgsundersøgelsen 2009 (_The Danish Municipality Study, 2009_)
- Kommunalvalgsundersøgelsen 2013 (_The Danish Municipality Study, 2013_)

### Author/contact

 - Erik Gahner Larsen, Department of Political Science, University of Southern Denmark, egl@sam.sdu.dk
 - Klaus Levinsen, Department of Political Science, University of Souhtern Denmark, khl@sam.sdu.dk
 - Ulrik Kjær, Department of Political Science, University of Southern Denmark, ulk@sam.sdu.dk

### Repository content

##### `/analysis/`

- `me-prep.R` = R script used to produce dataset from raw data
- `me-analysis.R` = R script used to conduct all analyses and produce figures
- `me-context.csv` = Municipality data
- `me-survey.csv` = Survey data
- `sessionInfo.txt` = Output from sessionInfo() in R

### Data: `me-context.csv`

Variables in file:
- `komnr` = Unique municipality identifier
- `navn` = Name of municipality (in Danish)
- `valgdelt` = Local election turnout (in 2009)
- `parti10` = Mayor party (in 2010)
- `mockdelt` = Mock election turnout 
- `mem` = Mock election municipality status
- `parti06` = Mayor party (in 2006)
- `leftborg` = Leftish mayor (in 2006)

### Data: `me-survey.csv`

Variables in file:
- `year` = Survey year 
- `komnr` = Unique municipality identifier
- `valgret` = Voting age attitude, ordinal
- `valgret.d` = Voting age attitude, binary
- `male` = Gender, male
- `age` = Age, years
- `educ` = Education
- `ideology` = Left-right ideology
- `party` = Vote preference in national election
- `child` = Children in househod, aged 17-19
- `age.cat` = Age, ordinal
- `highschool` = Highschool education
- `mep` = Mock election period
- `age.cat.0` = Age, 18-25
- `age.cat.1` = Age, 26-35
- `age.cat.2` = Age, 36-45
- `age.cat.3` = Age, 46-55
- `age.cat.4` = Age, 56-65
- `age.cat.5` = Age, 66-
- `party.1` = Vote preference, Social Democrats
- `party.2` = Vote preference, Social Liberals
- `party.3` = Vote preference, Conservatives
- `party.4` = Vote preference, Socialist People's Party 
- `party.5` = Vote preference, Liberal Alliance 
- `party.6` = Vote preference, Danish People's Party
- `party.7` = Vote preference, Liberals
- `party.8` = Vote preference, The Red-Green Alliance
- `party.9` = Vote preference, other

_Note:_ For question wording and descriptive statistics, see Online Appendix A and Online Appendix B.

### Session info

The analyses were made with [RStudio](http://www.rstudio.com/) (Version 0.98.1103) with the following R session:

```
## R version 3.2.2 (2015-08-14)
## Platform: x86_64-w64-mingw32/x64 (64-bit)
## Running under: Windows 8 x64 (build 9200)

## locale:
## [1] LC_COLLATE=Danish_Denmark.1252  LC_CTYPE=Danish_Denmark.1252   
## [3] LC_MONETARY=Danish_Denmark.1252 LC_NUMERIC=C                   
## [5] LC_TIME=Danish_Denmark.1252    

## attached base packages:
## [1] grid      stats     graphics  grDevices utils     datasets  methods   ## base     

## other attached packages:
##  [1] stargazer_5.2         ordinal_2015.6-28     ZeligMultilevel_0.7-1
##  [4] lme4_1.1-9            Matrix_1.2-2          Zelig_4.2-1          
##  [7] sandwich_2.3-4        MASS_7.3-44           boot_1.3-17          
##  [10] gridExtra_2.0.0       ggplot2_2.1.0         foreign_0.8-66       

## loaded via a namespace (and not attached):
##  [1] Rcpp_0.12.3      splines_3.2.2    munsell_0.4.3    colorspace_1.2-6
##  [5] lattice_0.20-33  minqa_1.2.4      plyr_1.8.3       tools_3.2.2     
##  [9] gtable_0.2.0     nlme_3.1-122     digest_0.6.9     ucminf_1.1-3    
##  [13] nloptr_1.0.4     labeling_0.3     scales_0.4.0     zoo_1.7-12      

```
