We proceed to report on the results of applying the benchmark to the six aggregate techniques. The main goal of the experiments is not only to compare the aggregation performances, but also to analyze the effects of worker characteristics on the performance behavior. In order to compare them in a fair manner, we provide the key insights under a wide range of settings to verify their performance. All the experiments ran on an Intel Core i7 processor 2.8 GHz system with 4 GB of main memory.


# Computation Time #

It takes server resources to process worker answers. In some real-time applications, final aggregations need to be returned within minutes or even seconds. As a result, quickly aggregating the worker answers is a key factor.

| #questions x #workers | MD | HP | ELICE | EM | SLME | GLAD | ITER  |
|:----------------------|:---|:---|:------|:---|:-----|:-----|:------|
| 10 x 10               | 0  | 0  | 0     | 11 | 1    | 12   | 1     |
| 10 x 50               | 0  | 0  | 1     | 51 | 3    | 59   | 15    |
| 10 x 100              | 0  | 0  | 1     | 153 | 5    | 108  | 45    |
| 50 x 10               | 0  | 0  | 1     | 33 | 3    | 45   | 19    |
| 50 x 50               | 0  | 0  | 3     | 234 | 12   | 141  | 102   |
| 50 x 100              | 0  | 0  | 6     | 928 | 27   | 238  | 355   |
| 100 x 10              | 0  | 0  | 3     | 52 | 7    | 91   | 53    |
| 100 x 50              | 0  | 0  | 9     | 529 | 24   | 272  | 336   |
| 100 x 100             | 0  | 0  | 15    | 1591 | 46   | 473  | 915   |

MD, HP, and ELICE are clear winners on this concern. The computation time (sec.) is shown above. MD, HP, and ELICE by far outperform the others (it takes less than 1 sec. with the size $1000 \times 1000$ of $M$). This result is straightforward to understand: these techniques require no iteration. In brief, we recommend using MD, HP, or ELICE for real-time computations.

# Accuracy #

The higher accuracy, the higher power of aggregation method. In the experiments, we measure accuracy of each method while varying the number of answers per question and the number of questions per worker. In that, we find which algorithm requires least answers and which algorithm requires least workers to achieve the accuracy requirements.

![https://benchmarkcrowd.googlecode.com/files/accuracy_apo.png](https://benchmarkcrowd.googlecode.com/files/accuracy_apo.png)

Overall, the iterative techniques perform significantly better when the number of answers per question is higher. This is because the same questions are answered by multiple workers (overlapping between worker). As a result, the answers of each worker can be justified by the answers of others through iterations.

# Sensitivity to Spammers #

In reality, spammers always exist in online community, especially crowdsourcing. Many experiments in the literature showed that the proportion of spammers could be up to 40%. As a result, it is important for crowdsourcing applications to know how each aggregate technique performs when the worker answers are not trustworthy.

![https://benchmarkcrowd.googlecode.com/files/spammer_uniform.png](https://benchmarkcrowd.googlecode.com/files/spammer_uniform.png)

The figure above illustrates the effects of uniform spammers and random spammers on accuracy, respectively. In general, the accuracy of all techniques decreases when the spammer ratio is higher. But their behaviors are significantly different.

# Adaptivity to Multi-labeling #

In the literature, many applications are designed for multiple-choice questions. Therefore, it is important to know the adaptivity of aggregate techniques to this setting---which one is compatible and which one is not. Moreover, we would like to examine if there are significantly differences of their performance characteristics between the binary and the multiple setting.

![https://benchmarkcrowd.googlecode.com/files/multi_accuracy.png](https://benchmarkcrowd.googlecode.com/files/multi_accuracy.png)

In this experiment, we study the adaptivity to multi-labelling of aggregate techniques. Only three techniques are retained---MD, HP, and EM---while the others fail to adapt this setting. SLME models worker expertise by sensitivity and specificity, which are applicable for binary question only. Regarding ITER and ELICE, their algorithms in the original papers indicate that they are only applied for binary questions. Besides, they use the sign (positive or negative) of aggregated value to classify object. Regarding GLAD, the authors only mention about binary questions. We checked the source code and confirmed that it was implemented for two labels.

# Worker Estimation Error #

Beside aggregated values, some of the aggregate techniques return estimated worker expertise (i.e. quality of worker). This measurement is important in some applications such as filtering, classifying, and ranking workers. To reflect this aspect, we represent the estimation errors of worker expertise using mean absolute error (Manhattan norm).

![https://benchmarkcrowd.googlecode.com/files/mae_apo.png](https://benchmarkcrowd.googlecode.com/files/mae_apo.png)

In general, when there are more workers answering the same question, all techniques perform better. Similar to the accuracy experiment, EM is still the winner and ITER is the worst.