<br />
<p align="center">
  <h3 align="center">Music Genre Identification with Clustering</h3>

  <p align="center">
    The goal of this project is to create an unsupervised learning model that groups musical tracks by genre.  The data comes from the Greek Audio Dataset (GAD), which consists of 1000 tracks and 342 audio and lyrical features extracted from each track (based on the format of the <a href="http://millionsongdataset.com/">Million Song Dataset</a>.  The eight genres represented are rock, pop, entexno, laiko, rempetiko, enallaktiko, hip hop/R&B, and monterno laiko; the dataset focuses on genres and artists popular in Greece and not addressed by other common MIR datasets.
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

![UMAP plot of genre clusters](https://github.com/jonesmo/Music_Genre_Clustering/blob/UMAP.png?raw=true)


## Model Building




## Future Work


