# Introduction #

Today, crowdsourcing becomes a promising methdology to overcome various problems that require human knowledge such as image labelling, text annotation, and product recommendation. A wide range of applications (e.g. ESP game, reCaptcha, and Freebase) have been developed on top of more than 70 crowdsourcing platforms such as Amazon Mechanical Turk and Cloud Crowd. The rapid growth of such crowdsourcing applications opens up a variety of interesting technical and social challenges.

One of the most critical issues of crowdsourcing is to aggregate different answers given by the crowd workers. This is a challenging task because of two reasons: (i) the workers might have wide ranging levels of expertise and (ii) the questions may vary in different levels of difficulty. While the former leads to the high contradiction and uncertainty in the answer set, the latter renders some difficulties in distinguishing between truthful workers and malicious workers.
To fully tackle this challenge, a rich body of research on answer aggregation has developed different techniques.

Understanding the performance implications of these techniques, for a given type of application, is difficult to comprehend. Therefore, we present the Benchmark for Aggregate Techniques in Crowdsourcing (BATC) with three functionalities:

  * Choose the best-suited technique for a particular application.
  * Provide the guidance on the selection of appropriate parameters.
  * Reduce the development complexity.

# Download #
  1. Runnable: click [here](https://benchmarkcrowd.googlecode.com/files/win32.win32.x86.zip)
  1. Example config files: [small config](https://benchmarkcrowd.googlecode.com/files/small_config.txt), [medium config](https://benchmarkcrowd.googlecode.com/files/medium_config.txt), [large config](https://benchmarkcrowd.googlecode.com/files/large_config.txt)
  1. Demo video: [download](https://benchmarkcrowd.googlecode.com/files/CrowdBenchmark.mp4)

<a href='http://www.youtube.com/watch?feature=player_embedded&v=BbHLOPa4jwM' target='_blank'><img src='http://img.youtube.com/vi/BbHLOPa4jwM/0.jpg' width='425' height=344 /></a>

# Screenshot #

![http://benchmarkcrowd.googlecode.com/files/GUI10.png](http://benchmarkcrowd.googlecode.com/files/GUI10.png)

# User Guide #

System requirements: JDK 1.6. or above

  * Step 0: Download runnable file.
  * Step 1: Load a config or input parameter for Crowd, Question, Factor, Metric and Algorithm sections.
  * Step 2: Run and evaluate the result of different algorithms.
  * Step 3: Change the config and re-run program. Arrange the views for comparison if necessary.

# Developer Guide #

This project is an Eclipse RCP applications based on Eclipse 4, therefore you will need Eclipse IDE and install Eclipse4 to deploy and launch the program. The detail steps are following:

  * Step 1: Check out the project from [svn](https://benchmarkcrowd.googlecode.com/svn/trunk/)
  * Step 2: Follow section 3 and section 4 in this tutorial: http://www.vogella.com/articles/EclipseRCP/article.html#tutorial_installation
  * Step 3: Import the project to Eclipse RCP
  * Step 4: Launch project (see section 5 in the Vogella tutorial above)