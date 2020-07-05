# Crime Association Rules Learning in the City of Atlanta

Data mining and machine learning have become a vital part of crime detection and prevention. Crime in Atlanta, Georgia is above the national median and has been a major problem for the city since the middle twentieth century. 

The main motivation for our project was how easily the crime data could be available form credible sources. This was a big plus as we then could develop any kind of system to assist the city officials. In the past, due to inadequate data collection and surveillance techniques, it was difficult to recognize a pattern to these daily crimes, much less apprehend the criminals behind these violations. As mentioned earlier, now we have access to data that is produced every second of everyday. On top of that, there is a systematic way of recording and storing these data so as not to tamper with it or loose it. All the collected data can help us understand more about the crimes in the city and help us better understand our living, working and studying environment in cities, in this case, Atlanta city. By analyzing data in a mathematically way, the researcher can gain access into the deep reasons behind the causes of crime and be able to predict future crimes before their occurrence.

## Proposed Work

The Projects main aim was to be able to analyze the crimes happening all around in Atlanta and be able to form an association as to where and when certain types of crimes normally happen. The project can form association rules between the time of the crime reported, the location of the crime and the type of crime that happened. This enables us to discover a pattern of the crime and may help users take precaution measures to avoid it. Some of the crimes that seem common are in fact something the users could have avoided, if the patterns of the crimes are studied. The criminals usually tend to follow a certain pattern when doing a crime, like the locations where the crime happened or the time during which the crimes happens. Studying and analyzing the patterns can help the citizens of that city be a step ahead and try preventing it from happening. The visualizations developed would be able to translate the results achieved. They would be able to better show the changes in the data.


## Development Platform and Libraries

We implemented the entire project using Python as the development platform. The selection of python over other platforms was python was extremely scalable as compared to platforms like R and it is faster. Python has several data science libraries that make the development very easy for the developer. We used several python libraries for the entire implementation process, they include: matplotlib, seaborn, pandas, numpy, shapely, descartes and geopandas. Shapely, descartes and geopandas were the libraries used to generate the visualisations translated from the results obtained.


# Algorithms

## K-means Algorithm 

The data was clustered using K-Means algorithm by considering location distribution of the crimes happening. We took the attributes, longitude and latitude, into account for the clustering. We then were able to plot the clusters in the respective locations to determine any location trends with respect to crime categories. We used the elbow method to determine the optimum K-value for the K-means.

<p align="center">
    <img src="/Images/elbow.png" alt="Image" width="800" height="400" />
</p></center>

Elbow Method gives us an idea on what a good K number of clusters would be based on the sum of squared distance(SSE) between data points and their assigned clusters’ centroids. We normally pick K at the spot where SSE starts to flatten out and forming an elbow.

<p align="center">
    <img src="/Images/kmeans.png" alt="Image" width="600" height="400" />
</p></center>

## Mean Shift Algorithm 

The other algorithm used was the mean shift algorithm.The mean shift algorithm is a clustering algorithm that assigns the data points to the clusters iteratively by shifting points towards the mode. Given a set of data pints, the algorithm iteratively assigns each data point towards the closest cluster centroid and direction to that is determined where most of the points nearby are at. So each iteration, each data point will move closer to where the points are at, which is or will lead to the cluster center. Whenever the algorithm stops, each points are assigned to a cluster center. The first step of this algorithm was to represent our data in a mathematical manner.

<p align="center">
    <img src="/Images/meanshit.png" alt="Image" width="600" height="400" />
</p>

## Principle Component Analysis

Principal Component Analysis was used to reduce the dimension of the feature space. Withing dimensionality reduction, we were interested in if certain components or discriminants would contain high explained variance ratios. This would indicate which components or features would be of relative importance. Each cluster was then plotted and overlaid with colors corresponding to crime category. PCA performed better than the other algorithms as it reduces the dimensions and the number of features, thereby only taking the features of higher importance. It took the shortest amount of time.

<p align="center">
    <img src="/Images/principle.png" alt="Image" width="600" height="400" />
</p></center>

# Explanatory Analysis

After careful studying of the dataset and the attributes, we decided to fist start with dividing the dataset according to the types of crimes in the city. That would enable us to be able to divide each type of crime, and then analyse the subdivisions separately to further learn more patterns in each of those crimes. For that we had to visualize the data into several different ways so that we could study it in detail. Explanatory analysis would enable us to determine which attributes to use to cluster and help in prediction.

## Crime distribution throughout year 

<p align="center">
    <img src="/Images/crimeyear.png" alt="Image" width="400" height="600" />
</p>

## Crime distribution w.r.t months 

<p align="center">
    <img src="/Images/heatmap_month.png" alt="Image" width="600" height="400" />
</p>

## Crime distibution w.r.t days of week

<p align="center">
    <img src="/Images/heatmap_week.png" alt="Image" width="600" height="400" />
</p>

## Crime distribution according to various categories

The main types of crime were divided into four categories instead of the very detailed UCR codes provided by the Atlanta PD. For example, in Robbery, there were almost 25 different sub categories, Robbery - Street - Gun, robbery - Commercial - Gun, Robbery - Street - knife, Robbery - Bank - Knife, to name a few. So considering these factors, we divided the data into the following major categories:

• Category 1: Homicides and Manslaughter

• Category 2: Assault and Robbery

• Category 3: Burglary and Auto-theft

• Category 4: Larceny

<p align="center">
    <img src="/Images/categories.png" alt="Image" width="800" height="400" />
</p></center>

# Results 

<p align="center">
    <img src="/Images/table.png" alt="Image" width="600" height="400" />
</p>

The above table represents the accuracy, precision and recall of four categories considered. Accuracy of Naive Bayes Classifier gives better results among the four algorithms. Hence we have applied Naive Bayes algorithm on the four categories and acquired the respective precision and recall. Four categories with and without added features i.e. the crime score were considered for precision and recall.

## Precision 

<p align="center">
    <img src="/Images/precision.png" alt="Image" width="600" height="400" />
</p>

## Recall

<p align="center">
    <img src="/Images/recall.png" alt="Image" width="600" height="400" />
</p>

## Accuracy

<p align="center">
    <img src="/Images/accuracy.png" alt="Image" width="600" height="400" />
</p>

# Visualization of Results 

We were able to visualize the final results with respect to each subdivision in Atlanta. The figure below shows the concentration of crime in each of these divisions. The different color hues show the concentration of crime in those areas. The darkest hue represents the most number of crime and the lightest represents the opposite.

<p align="center">
    <img src="/Images/map.png" alt="Image" width="600" height="500" />
</p>



