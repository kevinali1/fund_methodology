================
Technology
================

The following is a brief overview of Valuehorizon’s technology stack as at April 30, 2013. It may not be representative of the stack before or after that date.

Storage
==============

Data are stored in a PostreSQL relational database (version 9.2.4) running on a Linux VPS cluster (kernel 3.8.13).  All text fields are exposed to an Apache Solr search server (version 4.3.0) running on a dedicated Tomcat server (version 6.0.37). All raw datapoints (such as NAVs, distributions and financial statement time-series) are stored using fixed-floating point numbers. All analysis datapoints (such as return rates, volatility metrics and risk-adjusted returns) are stored using floating point numbers.

Data Updates and Caching
============================

The datasets are updated at 10:30AM and 6:00PM every day using a combination of an asynchronous Celery Task Queue (version 3.0) with RabbitMQ (version 3.0.4) as well as shell scripts deployed with a cronjob. Datasets are cached with Memcached (version 1.4.15) and/or Redis (version 2.6.13). The stale cache is destroyed and re-warmed at 12:00AM every day. Data scrubbing and outlier checks are performed on Fridays at 12:00AM.

Extraction and Analysis
============================

Data munging operations are done using Python (version 2.7.3) with various Python libraries. Data are generally extracted from the database using a Django ORM (version 1.5) and inserted into a vectorised Pandas Dataframe (version 0.10.1) and casted as floating points. Most data operations are performed using vectorised algorithms. Basic statistical operations are executed done with Statsmodels (version 0.4.0). Interest rate yields are interpolated using a cubic spline algorithm as provided by Scipy (version 0.10.1). Outlier detection is computed using packages obtained from Scikit-learn (version 0.13.1).

Computation
=================

Due to the large database size and memory requirements as well as the lengthy daily batch processing time, Valuehorizon does not perform any local computation. Instead, computation is performed on a simple cluster of Linode VPS servers. As a failover, one of the following cloud server alternatives may be utilised (in the  order of preference):
* Amazon Elastic Cloud Compute - Ubuntu instances;
* Digital Ocean cloud servers;
* Google App Engine.

Visualizations
======================

The charts for this journal were generated using R (version 2.14.1) and ggplot2 (version 0.9.3.1) either through the rpy2 interface (version 2.3.7) or through Rscript system calls and stored as svg files.  The chart data is read from json or csv dumps depending on the inherent complexity of the data’s structure. Visualizations are cross-checked on a sample basis to renderings produced by either Dygraphs (Git commit b839102723) or Highcharts (version 3.0.1).

*Subscribers may request all images and their related data files by sending an email to contact@valuehorizon.com with the subject: “Request for Journal Asset Files”*.
