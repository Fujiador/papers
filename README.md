# Papers

[TOC]

## Preface

This project contains all kind of papers that helps me a lot at work, for example, some help me to speed up the computation of TSP problem, some help me to overcome the GPS trajectory correction, GPS trajectory section, some help me to do a better jobs in Navigation(CNNs), some help me to recommend a better route in route planning problem(RNNs) and other many many jobs, I post them here wish to help someone who needed and so that he/she can make things more better.

You can clone and share it with others, also if you have some other papers/documents/books that you think they may help others, just push them.

## Details

Below are some details about the papers in the project.

- **genetic algorithm** 

  The papers in genetic algorithm(GA) folder are mainly about TSP, and it helps me to speed up the computation and improve the accuracy of route planning. For example I implemented the GA in parallel and it was three to four times faster, left bottom is normal computation and right bottom is parallel computation in my local machine, and when I put it on the server, I run 10 threads parallel to calculate, and it can help me plan 40 points in 1-2 seconds.

  <img src="https://raw.githubusercontent.com/yyccR/Pictures/master/geneticAlgorithm/%E4%B8%B2%E8%A1%8C%E8%AE%A1%E7%AE%97GA.gif" width="398" height="200" /><img src="https://raw.githubusercontent.com/yyccR/Pictures/master/geneticAlgorithm/%E5%B9%B6%E8%A1%8C%E8%AE%A1%E7%AE%97GA.gif" width="398" height="200" />

  And the algorithm seems to work very well in TSPLIB which can be download from https://www.iwr.uni-heidelberg.de/groups/comopt/software/TSPLIB95/ . Below I show some accuracy viewer of the route planning using GA.

  <img src="https://raw.githubusercontent.com/yyccR/Pictures/master/geneticAlgorithm/44nocycle.gif" width="388" height="246" />  &nbsp; <img src="https://raw.githubusercontent.com/yyccR/Pictures/master/geneticAlgorithm/42cycle.gif" width="388" height="246" />

- **DBSCAN**

  The papers in DBSCAN folder are mainly about how to cut the GPS trajectory into moving or stay blocks. I implemented the DBSCAN algorithm and modified its search logistic so that the algorithm can search through time based points. Below are some result.

  <img src="https://raw.githubusercontent.com/yyccR/Pictures/master/dbscan/1.png" width="183" height="96" />

  <img src="https://raw.githubusercontent.com/yyccR/Pictures/master/dbscan/2.png" width="183" height="96" />

  <img src="https://raw.githubusercontent.com/yyccR/Pictures/master/dbscan/3.png" width="183" height="96" />

  <img src="https://raw.githubusercontent.com/yyccR/Pictures/master/dbscan/4.png" width="183" height="96" />

  <img src="https://raw.githubusercontent.com/yyccR/Pictures/master/dbscan/5.png" width="183" height="96" />

  <img src="https://raw.githubusercontent.com/yyccR/Pictures/master/dbscan/6.png" width="183" height="96" />

  <img src="https://raw.githubusercontent.com/yyccR/Pictures/master/dbscan/7.png" width="183" height="96" />

  <img src="https://raw.githubusercontent.com/yyccR/Pictures/master/dbscan/8.png" width="183" height="96" />

- **interpolation**

  The papers in interpolation folder are mainly about how to interpolate the latitude and longitude points, traditional interpolation seem only work on one-dimension data, so I implemented and modified piece-wise cubic bessel interpolation in two-dimension, below are the test result:

  <img src="https://raw.githubusercontent.com/yyccR/Pictures/master/interpolation/piece-wise%20cubie%20bessel%20interpolation.png" width="314" height="192" />

- **spectral clustering**

  The papers in spectral clustering folder are mainly about how to aggregate spatial data, when I implemented that algorithm, I found the computation become more and more slowly when the data size growing, further research has realized that it was mainly because of the Jacobi matrix update operation which help to calculate the eigenvector of a matrix. So if someone wants use it in his/her job, parallel the Jacobi update is one way to overcome that problem, below show some result to compare KMeans.

  <img src="https://raw.githubusercontent.com/yyccR/Pictures/master/spectralClustering/SCandKmeans.png" width="800" height="400" />

- **HTM(Hierarchical Temporal Memory)**

  The papers in HTM fouder are mainly about Hierarchical Temporal Memory algorithm which was designed to detect anomaly points from stream data. I useed the nupic framework to implement that algorithm, but as contributors keep submitting code, the project is update very fast, and if someone wants to use it to do something, keep moving with the community. Below show some anomaly detection.

  <img src="https://raw.githubusercontent.com/yyccR/Pictures/master/HTM/1.gif" width="746" height="350" />