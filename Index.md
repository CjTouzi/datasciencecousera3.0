# Data Science Specialization in Coursera
Cheng  
Friday, February 06, 2015  

### Introduction

===========================

This is site is meant to be a cheat sheet of Data Science Specialization in coursera.

I started the data science specialization at Dec 1, 2015 and finished it at Feb 17, 2015.
Now I reorganize the contents in a function point of view for future references. 


### Research Design

===========================

**Looking for a topic**

- company project  
- kaggle  
- crowdanalytix  
- kdnuggets  
- drivendata.org  
- hackerrank  


**Formulating a problem** 


### Research Methods

===========================

#### Analytic Graphics


**Principles**   

- Comparisons    
- Causality, mechanism, explanation, systematic structure   
- Multivariate data  
- Integration of evidence    
- Describe and document the evidence with appropriate labels, scales, sources   
- Quality, relevance and integrity of the content 
        
**Purpose**  

- To understand data properties  
- To find patterns in data  
- To suggest modeling strategies  
- To "debug" analyses  
- To communicate results

**Simple Summary Technics**

-   One Dimension:   
    -   five-number summary   
    -   Boxplots  
    -   histograms   
    -   density plot   
    -   Barplot    


- Two Dimensions:  
    -   Multiple/Overlayed 1-D plots   
    -   scatterplots   
    -   smooth scatterplots      


-  More than Two Dimensions:     
    -   Multiple/Overlayed 2-D plots or coplot   
    -   use color, size, shape to add dimensions   
    -   spinning plots   
    -   3-d plots    
    
**Plotting Tools in R** 

-   base plotting system  
-   ggplot2 system  
-   lattice system    


**Clustering**  
Clustering organizes things that are close into groups.

-   How do we define close -> Distance or simliarity.     
    -   Pick the one that make sence to your problem.        
    -   Continuous: euclidean distance, correlation similarity    
    -   Binary: manhattan distance  

-   How do we group things?  
    -   Hierarchical Clustering      
        | `A agglomerative approach`: 1) Find closest two things; 2) Put them together; 3) Find next       
        | `Requires`: 1) A defined distance; 2) A merging approach.   
        | `Procedures`: A tree showing how close things are to each other.      
        | `R example`: [here](https://github.com/CjTouzi/courses/blob/gh-pages/04_ExploratoryAnalysis/hierarchicalClustering/Hierarchical%20clustering.pdf)  
        | `Note 1`: picture may be unstable
        | `Note 2`: determistic
    -   K-means Clustering    
        | `A partioning approach`: 1) Fix a number of clusters; 2) Get "centroids" of each cluster; 3) Assign things to the closest centroid; 4) Recalculate centroids        
        | `Requires`: 1) A defined distance metric; 2) A number of clusters. 3) An initial guess as to cluster centroids  
        | `Procedures`: Final estimate of cluster centroids and an assignment of each point to clusters       
        | `R example`: [here](https://github.com/CjTouzi/courses/blob/gh-pages/04_ExploratoryAnalysis/kmeansClustering/K-meansClustering_169.pdf)   
        | `Note 1`: Require a number of clusters by eyes or cross validation. [more](http://en.wikipedia.org/wiki/Determining_the_number_of_clusters_in_a_data_set)   
        | `Note 2`: Not deterministic caused by different # of clusters and iterations
    -   Dimension Reduction- SVD  
        | $X = UDV^T$      
        | U(left sigular vector) and V(right sigular vector) are orthogonal,D(sigular value)   is a diagonal matirx     
        | `R example`:[here](https://github.com/CjTouzi/courses/blob/master/04_ExploratoryAnalysis/dimensionReduction/index.md)
        | `Alexander Ihler video on Youtube`:[here](https://www.youtube.com/watch?v=F-nfsSq42ow)
    -   Dimension Reduction- PCA   
        | $X^TX = VDV^T = UDU^T$           
        | `Alexander Ihler video on Youtube`:[here](https://www.youtube.com/watch?v=F-nfsSq42ow)   
        | `Jason Liu on Quora`:[here](http://www.quora.com/What-is-an-intuitive-explanation-of-singular-value-decomposition-SVD)
    
-   How do we visualize the grouping      
    -   Dendrogram
        | `R example`: [1](https://github.com/CjTouzi/courses/blob/master/04_ExploratoryAnalysis/clusteringExample/index.md),[2](https://github.com/CjTouzi/courses/blob/master/04_ExploratoryAnalysis/hierarchicalClustering/index.md)
    -   Heatmap  
        | `R example`: [1](https://github.com/CjTouzi/courses/blob/master/04_ExploratoryAnalysis/dimensionReduction/index.md),[2](https://github.com/CjTouzi/courses/blob/master/04_ExploratoryAnalysis/hierarchicalClustering/index.md)
    -   Multidimenional Scaling  
        | `R example`: [1](https://github.com/CjTouzi/courses/blob/master/04_ExploratoryAnalysis/clusteringExample/index.md)
        

#### Statistical Inference
-   Paramount among our concerns are:
    -   Is the sample representative of the population that we'd like to draw inferences about?
    -   Are there known and observed, known and unobserved or unknown and unobserved variables that contaminate our conclusions?
    -   Is there systematic bias created by missing data or the design or conduct of the study?
    -   What randomness exists in the data and how do we use or adjust for it? Here randomness can either be explicit via randomization or random sampling, or implicit as the aggregation of many complex uknown processes.
    -   Are we trying to estimate an underlying mechanistic model of phenomena under study?
    -   Statistical inference requires navigating the set of assumptions and tools and subsequently thinking about how to draw conclusions from data.
    
-   Example goals of inference
    -   Estimate and quantify the uncertainty of an estimate of a population quantity (the proportion of people who will vote for a candidate).
    -   Determine whether a population quantity is a benchmark value ("is the treatment effective?").
    -   Infer a mechanistic relationship when quantities are measured with noise ("What is the slope for Hooke's law?")
    -   Determine the impact of a policy? ("If we reduce polution levels, will asthma rates decline?")

-   Example tools of the trade
    -   Randomization: concerned with balancing unobserved variables that may confound inferences of interest
    -   Random sampling: concerned with obtaining data that is representative of the population of interest
    -   Sampling models: concerned with creating a model for the sampling process, the most common is so called "iid".
    -   Hypothesis testing: concerned with decision making in the presence of uncertainty
    -   Confidence intervals: concerned with quantifying uncertainty in estimation
    -   Probability models: a formal connection between the data and a population of interest. Often probability models are assumed or are approximated.
    -   Study design: the process of designing an experiment to minimize biases and variability.
    -   Nonparametric bootstrapping: the process of using the data to, with minimal probability     model assumptions, create inferences.
    -   Permutation, randomization and exchangeability testing: the process of using data permutations to perform inferences.    
    
-   [Probability](https://github.com/CjTouzi/courses/blob/master/06_StatisticalInference/lectures/01_02_Probability.pdf) 
    -   keywords:probability, random Variables, PMF, PDF, CDF, survival function, quantiles 
-   [Expectations](https://github.com/CjTouzi/courses/blob/master/06_StatisticalInference/lectures/01_03_Expectations.pdf)
    -  key words:   
        | calculation of expected values of discrete random variables or contious random varibales    
        | expected value is a linear operator       
        | calculate variance and standard deviation     
        | Chebyshev's inequality: $P(|x-\mu|>=k\sigma) <= 1/k^2$
-   [Independence](https://github.com/CjTouzi/courses/blob/master/06_StatisticalInference/lectures/01_04_Independence.pdf)
    -    key words:     
        | IID
        | join probability of IIDS  
        | covariance : $Cov(X,Y) = E[(X-\mu_x )(Y-\mu_y)] = E[XY]-E[X]E[Y]$
        | correlation:  $Cor(X, Y) = Cov(X, Y) / \sqrt{Var(X) Var(y)}$  
        | sample variance $S$: $S^2 = \frac{\sum_{i=1}^n (X_i - \bar X)^2}{n-1}$    
        | variance of sample mean: $Var(\bar X)=\sigma^2/n$. $\sigma$ is the poluation variance.     
        | standard error of sample mean: $\sigma/\sqrt n$   
        | estimate population variance by sample variance: $S^2$ estimates $\sigma^2$; $S / \sqrt{n}$ estimates $\sigma / \sqrt{n}$ the standard error of the mean 
        
-   [Conditional Probability](https://github.com/CjTouzi/courses/blob/master/06_StatisticalInference/lectures/01_05_ConditionalProbability.pdf)
    -   key words:      
        | def: $P(A ~|~ B) = \frac{P(A \cap B)}{P(B)}$  
        | bayes' rules: $P(B|A) = \frac{P(A ~|~ B)P(B)}{P(A ~|~ B)P(B)+P(A ~|~ B^C)P(B^C)}$         
        | sensitivity: $P(+ ~|~ D)$         
        | specificity: $P(- ~|~ D^C)$   
        | positive predictive value: $P(D ~|~ +)$  
        | negative predictive value: $P(D^C ~|~ -)$     
        | prevalence of a disease: $P(D)$       
        | diagnositic likehood of a positive test($DLR_+$): sesitivity/(1- specificity)     
        | diagnositic likehood of a negtative test($DLR_+$): (1-sesitivity)/specificity         
        | likehood ratios: $\frac{P(D ~|~ + )}{P(D^C ~|~ +)} = \frac{P(+ ~|~ D )}{P(+ ~|~ D^C)}* \frac{P(D)}{P(D^C)}$. post-test odds of D = $DLR_+ *$ pre-test odds of D        
        
-   [Common Distributions](https://github.com/CjTouzi/courses/blob/master/06_StatisticalInference/lectures/02_01_CommonDistributions.pdf) 
    -   Bernoulli       
        | def: Bernoulli random variables take (only) the values 1 and 0 with probabilities of p and (1-p)     
        | PMF: $P(X=x)=p^x(1-p)^{1-x}$
respectively
    -   multiple iid bernoulli:         
        | PMF: $\prod_{i=1}^n p^{x_i} (1 - p)^{1 - x_i} = p^{\sum x_i} (1 - p)^{n - \sum x_i}$  
        | maximum likelihood estimator for p:  $\hat p = \sum_i x_i / n$
    -   bionomial:          
        | def: the sum of iid Bernoulli trials       
        | PMF: $P(X = x) = \left(\begin{array}{c} n \ x \end{array} \right) p^x(1 - p)^{n-x}$
    -   normal:         
        | PDF: $(2\pi \sigma^2)^{-1/2}e^{-(x - \mu)^2/2\sigma^2}$ If $X$ a RV with this density then $E[X] = \mu$ and $Var(X) = \sigma^2$  
        | The MLE for $\mu$ is $\bar X$.    
        | The MLE for $\sigma^2$ is $\frac{\sum_{i=1}^n (X_i - \bar X)^2}{n}$ (Which is the biased version of the sample variance.)        
    -   standard normal:        
        | def: When $\mu = 0$ and $\sigma = 1$          
        | RVs are often labeled $Z$ and The standard normal density function is labeled $\phi$
        | percentiles of standard normal.   
    -   poisson:     
        | PMF: $P(X = x; \lambda) = \frac{\lambda^x e^{-\lambda}}{x!}$,$\lambda$ is the mean number of events per unit time         
        | accurate approximation to the binomial distribution When $n$ is large and $p$ is smal,$\lambda = n p$       
-   Asymptopia
    -   keywords: 
        | LLN(Law of Large Numbers):        
        | CLT(Central Limit Theorem): 
        
-   t Confidence Interval
-   Likeklihood
-   Bayes
-   Two Group Intervals
-   Hypothesis Testing
-   p Values
-   Power
-   Multiple Testing
-   Resampled Inference


#### Regression Models
#### Machine Learning 


### Data Product Development

===========================

#### Reporting Tools 

- rmarkdown
- knit
- rPresentor
- slidify

#### UI tools

- shiny
- yhat
- github

#### R Language Tools 
- basics
[startupjing@github](https://github.com/startupjing/Tech_Notes/blob/master/R/R_language.md)
- packages

