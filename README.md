# Redactor: Model-Agnostic Targeted Disinformation Generation using Probabilistic Decision Boundaries

## Abstract
Information leakage is becoming a critical problem as various information becomes publicly available by mistake, and machine learning models train on that data to provide services. As a result, one's private information could easily be memorized by such trained models. Unfortunately, deleting information is out of the question as the data is already exposed to the Web or third-party platforms. Moreover, we cannot necessarily control the labeling process and the model trainings by other parties either. In this setting, we study the problem of {\em targeted disinformation} where the goal is to lower the accuracy of inference attacks on a specific target (e.g., a person's profile) only using {\em data insertion}. 
While our problem is related to data privacy and defenses against inference attacks, our techniques are inspired by targeted data poisoning attacks with some key differences.
We show that our problem is best solved by finding the closest points to the target in the input space that will be labeled as a different class. Since we do not control the labeling process, we instead conservatively estimate the labels probabilistically by combining decision boundaries of multiple classifiers using data programming techniques. We also propose techniques for making the disinformation realistic. Our experiments show that a probabilistic decision boundary can be a good proxy for labelers, and that our approach outperforms other targeted poisoning methods when using end-to-end training on real-world datasets. Our approach also helps reduce information leakage caused by inference attacks and can scale to large data.

<img src = "https://user-images.githubusercontent.com/62869983/150624047-8c04cbda-d8fe-47df-a363-bcc924f8d875.png" width="70%" height="70%">

## 4.5. Realistic Example

<img src = "https://user-images.githubusercontent.com/62869983/150624401-5caef443-9a13-47fa-8651-f42e2a368f1d.png">

We perform a comparison of our disinformation with real data to see how realistic it is. We filter out examples that contain feature pair patterns that do not occur in the original data. Above tables show a representative disinformation example (among many others) that was generated using our method along with the target and the target's nearest examples. To see if the disinformation is realistic, we conduct a poll asking 11 human workers to correctly identify 5 disinformation and 5 real examples. As a result, the average accuracy is 53%, and the accuracies for identifying disinformation and real examples are 40% and 65%, respectively. We thus conclude that humans cannot easily distinguish our disinformation from real examples, and that identifying disinformation examples is harder than identifying real examples. 
You can check the other examples in [this link](https://forms.gle/6VHGs5KyiMRbVeNB6).

## How to use
Please refer to "AdultCensus Tutorial" files.

