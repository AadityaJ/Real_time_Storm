Real Time Analytics of Twitter Data with Apache Storm
==========================================================
### Summary
The project aims at developing Real time twitter feed filtering the __Top-N Hashtags__ (N=10 in my case).An example of the give would be ![this](www.aadityajamuar.net/selfplots/twitter-rt.png)</br>
### Methodology
The project uses __Apache Storm__ and __Twitter API__ to create design a __Storm Topology__ and implement a new __streaming joins__ to dynamically calculate Top-N Hashtags and display real-time tweets that contain __trending Top Hashtags__ which involves implementation of Twitter spouts (Called *tweet spouts*) which is then connected to *Parse Tweet Bolt* using shuffle grouping which is connected to *Count Bolt* using fields grouping which is connected to an open source bolt called *Intermediate rankings Bolt* via fields grouping which is connect to *Total rankings Bolt* by global grouping which is connected via global grouping to *Report Bolt* which in turn is connected to Redis and Flask MicroServer which is connected to uses word-cloud visualization written D3js .Flask provides a handy way of running the visualization on streams of data at runtime while Redis provides an efficient runtime in-memory key value storage mechanism.
### Downloads
To download the code
```
git clone https://github.com/AadityaJ/Real_time_Storm
```
Feel free to Fork the code.
To send a pull request please contact :
* Aaditya Jamuar ([@AadityaJ](https://github.com/AadityaJ))   
