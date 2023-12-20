

  <h3 align="center">COVID-19 Analysis</h3>

  <p align="center">
    Analyzing the COVID-19 spread in the United States over the years 2020-2022.
    <br /> <br />
    <a href="https://github.com/Apratim08/COVID-19-Analysis"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    .
    <a href="https://www.youtube.com/watch?v=XPJm1Naw9_E">View YouTube tutorial</a>
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
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
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
## Project Details

Feature engineering played a pivotal role in enhancing the dataset for predictive modeling. Time series
components were isolated, emphasizing trends, seasonality, and residuals from cumulative daily cases, with a
specific focus on California for prediction purposes. Demographic features were also engineered, categorizing
and encoding age to enrich predictions related to age groups affected by COVID-19, pneumonia, or influenza.
The first study aims to forecast the number of COVID-19 cases for the upcoming month in the United
States by employing time series analysis of historical data. The objective is to provide healthcare systems
and policymakers with predictive insights to prepare and mitigate the potential overburdening of medical
infrastructure.
<br />
<a href="https://github.com/Apratim08/COVID-19-Analysis"><strong>Explore the docs »</strong></a>

The dataset comprised daily confirmed COVID-19 cases and deaths for all U.S. states over the last two
years. The dataset was preprocessed by grouping the data by state. Preliminary analysis identified New York
and California as states with the highest number of deaths and confirmed cases, respectively. These states were
selected for in-depth analysis due to their significant data volume, which is likely to yield more reliable insights.
The primary method for forecasting COVID-19 cases is time series analysis. Time series analysis is
particularly suitable for this research due to its effectiveness in analyzing data points collected or recorded at
regular time intervals. This approach helps in identifying patterns, trends, and seasonal variations in the
data, which are crucial for accurate forecasting.
Model Selection and Development
Linear regression models were developed for New York and California. The choice of linear regression is
grounded in its simplicity and effectiveness in capturing trends in time series data. The models predict the
number of COVID-19 cases based on historical data trends.
We employed various models for the Categorical Prediction task, including linear regression to predict
the age group and decision trees via Random Forest. The latter showed the best results among the models
tested, specifically for the 17-class classification task of all age group labels within the dataset!
Feature Engineering
Feature engineering involved extracting meaningful features from the time series data. This included creating
time-based features like month, week, and day to capture seasonal and cyclical trends. Additional features such
3
as moving averages were also computed to smooth out short-term fluctuations and highlight longer-term trends.
We used label encoding and filtered the data for the classification task of 17 classes for the ”Provincial
COVID-19 deaths by Sex and Age” dataset.
Regularization
Given the complexity of the dataset, we applied lasso and ridge regularization techniques to prevent overfitting
for the time series task and reduce the potential for highly variable COVID-19 case numbers.
We experimented with various hyperparameters for the classification task using different models. After
comparing the results, we found that the decision tree classifier performed the best. We then focused on
adjusting the n estimators parameter, which determines the number of decision trees in the random forest
ensemble. Additionally, we set the random state to 42, which sets the seed for the random number generator
and ensures that the results are reproducible when the algorithm involves random processes.
Inference and Prediction Methods
The models were used to make inferences about the trends in COVID-19 cases and to forecast future cases.
The forecasting was conducted for a one-month horizon, aligning with the research objective to provide
short-term predictive insights.
Model Evaluation and Validation
To ensure the model’s robustness, cross-validation was performed. This involved dividing the datasets into
training and testing sets to validate the model’s performance on unseen data. The model was trained on a
subset of the data and tested on another subset to evaluate its predictive accuracy.
Model Selection and Evaluation Metrics
The model’s performance was evaluated using Root Mean Squared Error (RMSE

### Prerequisites

This is an example of how to list things you need to use the software and how to install them.
* npm
  ```sh
  npm install npm@latest -g
  ```

### Installation

_Below is an example of how you can instruct your audience on installing and setting up your app. This template doesn't rely on any external dependencies or services._

1. Get a free API Key at [https://example.com](https://example.com)
2. Clone the repo
   ```sh
   git clone https://github.com/your_username_/Project-Name.git
   ```
3. Install NPM packages
   ```sh
   npm install
   ```
4. Enter your API in `config.js`
   ```js
   const API_KEY = 'ENTER YOUR API';
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Conclusion



<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [x] Add Changelog
- [x] Add back to top links
- [ ] Add Additional Templates w/ Examples
- [ ] Add "components" document to easily copy & paste sections of the readme
- [ ] Multi-language Support
    - [ ] Chinese
    - [ ] Spanish

See the [open issues](https://github.com/othneildrew/Best-README-Template/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Apratim Banerjee - [LinkedIn](https://www.linkedin.com/in/banerjee-apratim/) - apratimbanerjee@berkeley.edu

Project Link: [Github repo link](https://github.com/Apratim08/COVID-19-Analysis)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

Use this space to list resources you find helpful and would like to give credit to. I've included a few of my favorites to kick things off!

* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Malven's Flexbox Cheatsheet](https://flexbox.malven.co/)
* [Malven's Grid Cheatsheet](https://grid.malven.co/)
* [Img Shields](https://shields.io)
* [GitHub Pages](https://pages.github.com)
* [Font Awesome](https://fontawesome.com)
* [React Icons](https://react-icons.github.io/react-icons/search)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
