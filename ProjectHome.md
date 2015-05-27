## Publications ##

  * Quoc Viet Hung Nguyen, Thanh Tam Nguyen, Ngoc Tran Lam and Karl Aberer. An Evaluation of Aggregation Techniques in Crowdsourcing. In: WISE. 2013.

  * Quoc Viet Hung Nguyen, Thanh Tam Nguyen, Ngoc Tran Lam, and Karl Aberer. BATC: a benchmark for aggregation techniques in crowdsourcing. In: SIGIR. 2013, pp. 1079-1080.



# Description #

As the volumes of AI problems involving human knowledge are likely to soar, crowdsourcing has become essential in a wide range of world-wide-web applications. One of the biggest challenges of crowdsourcing is aggregating the answers collected from crowd workers; and thus, many aggregate techniques have been proposed. However, for a particular application, it is difficult for users to choose the best-suited technique as well as appropriate values of parameter configuration since each of these techniques has distinct performance characteristics depending on various factors (e.g. worker expertise, question difficulty). In this paper, we develop a benchmarking tool that allows to (i) simulates the crowd and (ii) evaluates aggregate techniques in different aspects (accuracy, robustness to spammers, etc.). We believe that this tool will be able to serve as a practical guideline for both researchers and software developers. While researchers can use our tool to assess existing or new algorithms, developers can reuse its components to reduce the development complexity.

We present the Benchmark for Aggregate Techniques in Crowdsourcing (BATC) with three functionalities:

  * Choose the best-suited technique for a particular application.
  * Provide the guidance on the selection of appropriate parameters.
  * Reduce the development complexity.

# Download #
  1. Runnable: click [here](https://benchmarkcrowd.googlecode.com/files/win32.win32.x86.zip)
  1. Example config files: [small config](https://benchmarkcrowd.googlecode.com/files/small_config.txt), [medium config](https://benchmarkcrowd.googlecode.com/files/medium_config.txt), [large config](https://benchmarkcrowd.googlecode.com/files/large_config.txt)
  1. Demo video: [download](https://benchmarkcrowd.googlecode.com/files/CrowdBenchmark.mp4)

<a href='http://www.youtube.com/watch?feature=player_embedded&v=BbHLOPa4jwM' target='_blank'><img src='http://img.youtube.com/vi/BbHLOPa4jwM/0.jpg' width='425' height=344 /></a>

# Screenshot #

<img src='http://benchmarkcrowd.googlecode.com/files/GUI10.png' width='80%' />

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

# Real-world datasets #
[Datasets for data integration domain](https://code.google.com/p/benchmarkcrowd/wiki/DataIntegrationDatasets)



# Report Issues #

Please follow this guideline: [Issue Tracking](https://code.google.com/p/benchmarkcrowd/wiki/EnabledIssueTracking)

# Contact #
Do Son Thanh [sonthanhdo2004@gmail.com](http://sonthanhdo2004@gmail.com)