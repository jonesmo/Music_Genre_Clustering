<br />
<p align="center">
  <h3 align="center">Music Genre Identification with Clustering</h3>

  <p align="center">
    The goal of this project is to create an unsupervised learning model that groups musical tracks by genre for application in recommendation engines.  The data comes from the Greek Audio Dataset (GAD), which consists of 1000 tracks and 342 audio and lyrical features extracted from each track (based on the format of the <a href="http://millionsongdataset.com/">Million Song Dataset</a>.  The eight genres represented are rock, pop, entexno, laiko, rempetiko, enallaktiko, hip hop/R&B, and monterno laiko; the dataset focuses on genres and artists popular in Greece and not addressed by other common MIR datasets.
    <br />
    <br />
    <a href="https://colab.research.google.com/drive/11Ahn4bdBs_HgvHb0FnYwxGD6wfOlLfm7?usp=sharing">View Notebook</a>
  </p>
</p>


<!-- ABOUT THE PROJECT -->
## About The Project

I chose to tackle this project because of my ongoing interest in music information retrieval and my desire to see how computers "hear" music.


### Built With

* []() Scikit-Learn
* []() scipy.stats
* []() matplotlib
* []() <a href="https://hilab.di.ionio.gr/index.php/en/music-information-research/">Data</a> from the Greek Music Dataset


## Visualization

To better visualize how the genres are clustered in a multi-dimensional space, I used PCA and UMAP to visualize the labeled data in two dimensions.  This provided a preliminary idea of how much the data points from the different genres overlapped.  It immediately became obvious that unsupervised learning algorithms would struggle, as the genres heavily overlap in this particular data space.

![UMAP plot of genre clusters](https://github.com/jonesmo/Music_Genre_Clustering/blob/main/UMAP.png?raw=true)


## Model Building

I tested preliminary K-Means, agglomerative hierarchical clustering, DBSCAN, and Gaussian mixture models, and I selected the most promising models for fine tuning using ARI and silhouette score as metrics.  While none of the models performed outstandingly, I chose to fine tune the K-Means and GMM models.  Because the results continued to be mediocre, I decided to cluster the data in a reduced feature space by taking the 30 most prominent PCA components as features rather than the full 340.  This did not improve the results either.


## Future Work

It's clear that the audio features extracted from the songs are not adequate to cluster the genres in the same way humans classify them, by genre.  As someone unfamiliar with Greek music myself, I spent some time on YouTube listening to examples of each genre, and I realized that I also would not be able to classify the genres very well without prior cultural knowledge.  I propose a few possible audio features that might improve performance and would be worth extracting, including low frequency content and percussiveness ("bassiness") and instrumentation (taken from metadata).  I also include some thoughts about what features humans hear in music that lead us to classify it in certain ways.
