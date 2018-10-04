# Wine Quality Analysis

### INTRODUCTION 
Three wine-tasting experts (herein refered to as "tasters") tasted ~ 6500 samples of Portuguese "Vinho Verde" wine,  ~30% and ~ 70% of which were red and white variants respectively. Each taster rated the QUALITY of samples on scale of 0 - 10 (0 = bad, 10 = great) and the officially recorded quality of a sample was the median of the 3 ratings. Each wine sample has data detailing its chemical and physical properties, listed below. Units for most quantities are in MASS DENSITY, with grams (g) or milligrams (mg) per cubic decimeter (dm).

### VARIABLE DESCRIPTION
- QUALITY (integer in [1 - 10])
- FIXED ACIDITY (numeric, g/dm$^{3}$)
- VOLATILE ACIDITY (numeric, g/dm$^3$)
- CITRIC ACID (numeric, g/dm$^3$)
- RESIDUAL SUGAR (numeric, g/dm$^3$)
- CHLORIDES (numeric, g/dm$^3$)
- FREE SULFUR DIOXIDE (numeric, mg/dm$^3$)
- TOTAL SULFUR DIOXIDE (numeric, mg/dm$^3$)
- DENSITY (numeric, g/dm$^3$)
- pH (numeric, <= 14)
- SULPHATES (numeric, g/dm$^3$)
- ALCOHOL (numeric, [0.0 - 1.0], % volume)

### Wine Quality: What Makes a Great Wine Great, and a Bad Wine Bad? 

Before we start with any analysis, it is certainly worth asking an important question related to the "quality" of a wine: 

<h3><center>Is there an objective set of chemical and physical properties that makes a wine good or bad? </center></h3>
    
Possibly, but our dataset only represents one type of wine from one region in Portugal - our conclusions about wine quality will only describe _these_ wines, and we can describe what judges are "looking for" in a good or bad Vinho Verde. The samples are also comprised of both reds and whites (in the ~ 30%/70% ratio respectively), which brings us to a broader question of quality: is there a global set of traits that determine "goodness" or "badness" of a sample _independent of the wine colour_? Congruently, are there traits that make reds (whites) good, but not whites (reds) and vice versa? Let's first examine the rating of sample quality more closely before we use the data to address these questions.

### Are Experts Better Than Monkeys at Rating Wines?

The purpose of the wine tasters is ostensibly to only allow a select population of wines in the production facility to actually reach the shelves. By removing some set of poorly identified wines they look to produce a consistently high-quality product. But high-quality according to _who_? The production facility depends in some fashion on the advice of skilled wine experts, and so it is worth asking the question: are the wine experts credible in their ratings of wine quality? 

The quality ratings could in theory be fairly subjective to the taster's tastebuds. If there is a "tastebud consensus" among expert wine tasters that clearly outlines the taste of good or bad wines it would not depend on the taster, assuming all are competent. In seems likely there would be a particular set of taste characteristics that then defines a good wine, and such for a bad one. Experts would then be tasting for these profiles and rating accordingly. In this world, the average consumer could be confident that the award a wine displays on it's label for quality was well earned. 

On the other hand, quality rating _could_ be highly subjective or inconsistent. 

Without too much knowledge of how wine-tasters taste, I would assume that tasters are at least attempting to look for particular qualities that they will identify with their tastebuds without actual knowledge of the chemical structure of the sample. For example, a chef knows what a filet mignon _should_ taste like given the way it has historically been cooked, and thus knows what to look for in the taste of a "good" filet mignon. Even still, this process could reasonably be subjective on scales that make sample rating inconsistent. 

Interestingly, there exist several studies that show wine-tasting experts often rate wines "incorrectly" in blind international competitions. By "incorrectly" we mean rating wines that have won awards for quality in other competitions as poor, or traditionally low quality wines are good (eg. Hodgson 2012, Journal of Wine Economics). Blind competitions offer no information about the tasted wine: no bottle, label or mention of accrued awards, suggested flavours or time of aging. A rating depends exclusively on _taste_, the ultimate test for objectivity in _good_ wines. The proposed rating inconsistencies in these competitions suggests that wine ratings _are_ highly subjective, at least in these scenarios.  

Amazingly, tasting experts have even been fooled into believing a _white wine_ was a red one after it was died red and _presented_ as a red wine (Morrot 2001, Brain and Language). This suggests that, despite any findings we may produce that clearly differentiate red from white wine on a chemical or physical basis, an expert taster may not be able to properly _interpret_ these differences by the tongue. Fascinating!


Exploratory data analysis, 2 classification models, 1 regression model on data concerning wine quality.

### Data Questions:   
Can we predict the quality rating of a wine sample?
Can we predict whether a wine is red or white given its predictors (ie. chemistry)? 
What are the chemical compositions that define red and white wine (inference from above)?
What factors make a great wine, and what factors make a terrible wine?

### Acknowledgements:

P. Cortez, A. Cerdeira, F. Almeida, T. Matos and J. Reis. Modeling wine preferences by data mining from physicochemical properties. In Decision Support Systems, Elsevier, 47(4):547-553, 2009.


