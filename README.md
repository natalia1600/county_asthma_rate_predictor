## Does PM2.5 vary geographically in California?
By understanding what geographical features are most important in determining
PM2.5 levels in California, policymakers can approach reducing PM2.5 pollutants
in an efficient manner. 

For example, if accurately modeling PM2.5 reveals
that the area of water in a county is negatively correlated to PM2.5 in a significant
way, policymakers may choose to target drier counties first, or add bodies
of water near pollution hotspots.

Modeling using Frequentist and Bayesian GLM’s and a non-parametric model
is a good method because coefficient estimation will allow us to determine the
significance of a feature and its correlation with Pm2.5 with a certain level of
uncertainty. Ultimately, we are trying to uncover the strength of a relationship,
not whether it is causal or correlated.

GLM’s have several limitations. Firstly, they assume that the relationship between
PM2.5 and the predictor features can be modeled using a specific probability
family (we will be using Normal). If our assumption is wrong, our model
can go wrong. Next, the relationship between PM2.5 and the features has to
be linear. If this is not true, then our model will not predict well. Lastly,
GLM’s are sensitive to outliers and multicollinearity. If, for example, latitude
and longitude are highly collinear, their coefficients may be inaccurate and our
interpretations can be wrong.


## Does increased PM2.5 levels cause higher county asthma hospitalization rates?
PM2.5 pollutants are more dangerous than PM10 pollutants because they are
finer and can get into deeper areas of the lungs, and even the bloodstream.
Long-term exposure to PM2.5 can be attributed to health effects not limited to
ischemic heart disease, lung cancer, strokes, and type 2 diabetes.

It is important to determine whether PM2.5 pollution is the cause of diseases
and hospitalizations, as evidence of damage can propel decisions to curtail the
danger. The prevalence of PM2.5 in society is reminiscent to common smoking
in urban areas throughout the 20th century. A causal study by Hammond
and Horn in 1952 was a landmark discovery that found men who smoked regularly
had a considerably higher death rate than men who had never smoked (or smoked with cigars or pipes only). Hammond and Horn’s work began a massive shift in American opinions on tobacco and cigarettes. It is possible that
a breakthrough study establishing that PM2.5 levels cause asthma hospitalizations
can be part of a shift too. 

Determining this causal relationship at a county
level is not optimal for individual-level analysis, but it is good for policymakers.
For example, the state of California can take our study and then start directing
health funding to certain counties more than others.

We are using causal inference to answer whether increases PM2.5 levels causes
higher county asthma hospitalization rates, since we want to uncover a causal
relationship between PM2.5 levels and asthma hospitalizations. Depending on
this relaitonship, we may be able to see the overall implications PM2.5 level has
on public health.

We will be using inverse propensity scoring to manage the difference in covariates
across counties and develop an unbiased average treatment effect.
IPW assumes unconfoundedness to generate an unbiased ATE. If we do not
find all confounders, then our causal study may be biased. 