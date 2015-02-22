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
        | `R example`:[here][https://github.com/CjTouzi/courses/blob/master/04_ExploratoryAnalysis/dimensionReduction/index.md]
        | `extral1`:[here][https://www.youtube.com/watch?v=F-nfsSq42ow]
    -   Dimension Reduction- PCA   
        | $X^TX = VDV^T = UDU^T$       
        | sfd   
        | sdf,slkdjf       
        | sfd 
    
-   How do we visualize the grouping      
    -   Dendrogram  
    -   Heatmap  
    -   Multidimenional Scaling  
 
-   How do we interept the grouping        



**Plotting Tools in R** 

-   base plotting system    
-   ggplot2 system  
-   lattice system    

#### Statistical Inference
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

