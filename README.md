<a name="readme-top"></a>

  <h3 align="center">COVID-19 Analysis</h3>

  <p align="center">
    Analyzing the COVID-19 spread in the United States over the years 2020-2022.
    <br /> <br />
    <a href="https://github.com/Apratim08/COVID-19-Analysis"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    .
    <a href="https://www.youtube.com/watch?v=XPJm1Naw9_E">Video Walkthrough</a>
    ·
    <a href="https://github.com/Apratim08/COVID-19-Analysis/issues">Issues</a>
    ·
  </p>
</div> 



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#project-details">Project Details</a>
    </li>
    <li><a href="#conclusion">Conclusion</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
<a name="#about-the-project"></a>
## About The Project
  <p align="justify">
In this project we are analyzing COVID-19 data during the years 2020-2022, focusing particularly on the United States. The primary datasets utilized include the ’time series covid19 confirmed US’ and ’time series covid19 deaths US’ from
the CSSE at Johns Hopkins University and CDC, alongside ’Provisional COVID-19 Death by Sex and Age’ from the National Center for Health Statistics (NCHS). 
Here we are performing a time series forecast for COVID-19 confirmed cases and deaths, employing models that consider the cumulative daily cases and demographic
characteristics, with close attention to the states of New York and California, due to their
significant data volume and distinctive COVID-19 impact patterns. We are also measuring and analzying
the age groups most susceptible to COVID-19.
  </p>

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
<a name="#project-details"></a>
## Project Details

The first study aims to forecast the number of COVID-19 cases for the upcoming month in the United
States by employing time series analysis of historical data. The objective is to provide healthcare systems
and policymakers with predictive insights to prepare and mitigate the potential overburdening of medical
infrastructure.


<a href="https://github.com/Apratim08/COVID-19-Analysis/blob/master/analysis/US_COVID_time_series.ipynb"><strong>Check out Notebook »</strong></a>
<br />

The dataset comprised daily confirmed COVID-19 cases and deaths for all U.S. states over the last two
years. Preliminary analysis identified New York and California as states with significant data volume and was hence chosen for further analysis.

<img src="https://i.postimg.cc/JzsFTv1Y/1.png" style="width:1000px;height:600px;">

#### Model Selection and Development
Linear regression models were developed for New York and California. The models predicted the
number of COVID-19 cases based on historical data trends.
We employed various models for the Categorical Prediction task, including linear regression to predict
the age group and decision trees via Random Forest. The latter showed the best results among the models
tested, specifically for the 17-class classification task of all age group labels within the dataset.
 
#### Regularization
Given the complexity of the dataset, we applied lasso and ridge regularization techniques to prevent overfitting
for the time series task and reduce the potential for highly variable COVID-19 case numbers.
We experimented with various hyperparameters for the classification task using different models. After
comparing the results, we found that the decision tree classifier performed the best. We then focused on
adjusting the n estimators parameter, which determines the number of decision trees in the random forest
ensemble. Additionally, we set the random state to 42, which sets the seed for the random number generator
and ensures that the results are reproducible when the algorithm involves random processes.

#### Inference and Prediction Methods
The models were used to make inferences about the trends in COVID-19 cases and to forecast future cases.
The forecasting was conducted for a one-month horizon, aligning with the research objective to provide
short-term predictive insights.

<img src="https://i.postimg.cc/26YrNryS/6.png" style="width:800px;height:400px;">

#### Model Evaluation and Validation
To ensure the model’s robustness, cross-validation was performed. This involved dividing the datasets into
training and testing sets to validate the model’s performance on unseen data. The model was trained on a
subset of the data and tested on another subset to evaluate its predictive accuracy.
The model’s performance was evaluated by calculating the Root Mean Squared Error (RMSE)

<img src="https://i.postimg.cc/YSCqvpkD/9.jpg" style="width:1000px;height:400px;">

<a name="#conclusion"></a>
## Conclusion

In the realm of public health, the exploration and analysis of COVID-19 data have emerged as crucial
components for understanding the dynamics of the pandemic. Conducting exploratory data analysis (EDA)
on COVID-19 datasets provides invaluable insights into the spread, impact, and patterns of the virus across
regions and populations. Furthermore, the development of prediction models becomes essential for forecasting the future trajectory of the pandemic, anticipating
potential surges, and optimizing resource allocation. Sophisticated machine learning models, such as Long Short-Term Memory Networks (LSTMs), Gated
Recurrent Units (GRUs), and Wide Deep Learning (Wide Deep), offer a more advanced approach to
capturing complex relationships within the ”Provincial COVID-19 deaths by Sex and Age” dataset. These
models are particularly useful for handling sequential or structured data, allowing them to learn intricate
dependencies and patterns within the age labels for improved predictions.



<p align="right">(<a href="#readme-top">back to top</a>)</p>


<a name="#roadmap"></a>
<!-- ROADMAP -->
## Roadmap

- [ ] Improve Model Accuracy.
- [ ] Update dataset with recent available data.
- [ ] Perform similar tests with other diseases and compare with COVID-19.
- [ ] Incorporate more sophistacted machine learning tools.


<p align="right">(<a href="#readme-top">back to top</a>)</p>


<a name="#contributing"></a>
<!-- CONTRIBUTING -->
## Contributing

Contributors in the project: Anusri Sreenath, Lakshya Agarwal



<!-- ACKNOWLEDGMENTS -->
<a name="#acknowledgements"></a>
## Acknowledgments

* DATA100 Course, UC Berkeley - for giving us the opportuntiy to carry out this project.
* Yuri Kravchenko, Nataliia Dakhno, Olga Leshchenko, and Anastasiia Tolstokorova. Machine learning
algorithms for predicting the results of covid-19 coronavirus infection. In IT&I Workshops, pages 371–381, 2020.
* Raghavendra Kumar, Anjali Jain, Arun Kumar Tripathi, and Shaifali Tyagi. Covid-19 outbreak: An
epidemic analysis using time series prediction model. In 2021 11th International Conference on Cloud
Computing, Data Science Engineering (Confluence), pages 1090–1094, 2021.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

