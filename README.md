# StarbucksCapstoneChallenge

## Project Overview
This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.

Not all users receive the same offer, and that is the challenge to solve with this data set.

Every offer has a validity period before the offer expires. As an example, a BOGO offer might be valid for only 5 days. You'll see in the data set that informational offers have a validity period even though these ads are merely providing information about a product; for example, if an informational offer has 7 days of validity, you can assume the customer is feeling the influence of the offer for 7 days after receiving the advertisement.

The Starbucks Udacity Data Scientist Nanodegree Capstone challenge data set is a simulation of customer behavior on the Starbucks rewards mobile application. Periodically, Starbucks sends offers to users that may be an advertisement, discount, or buy one get on free (BOGO). An important characteristic regarding this dataset is that not all users receive the same offer.

## Metrics
To quantify to performance of the used models, I will use accuracy and F-score metrics for. F1 score provides a better sense of model performance compared to purely accuracy as takes both false positives and false negatives in the calculation. With an uneven class distribution, F1 may usually be more useful than accuracy. Accuracy measures how well a model correctly predicts whether an offer is successful. However, if the percentage of successful or unsuccessful offers is very low, accuracy is not a good measure of model performance. 

## Files  
- Starbucks_Capstone_notebook.ipynb  
  - [Jupyter notebook](https://jupyter.org/) that performs three tasks:  
    - Combines offer portfolio, customer demographic, and customer transaction data  
    - Generates training customer demographic data visualizations and computes summary statistics  
    - Generates three models
- Udacity Data Science Nanodaegree pdf
    Contains a Blog Post with all information concerning the capstone project
- README.md  
  - [Markdown](https://guides.github.com/features/mastering-markdown/) file that summarizes this repository  
  
## Files provided by Starbucks
`portfolio.json`
- id (string) - offer id
- offer_type (string) - the type of offer ie BOGO, discount, informational
- difficulty (int) - the minimum required to spend to complete an offer
- reward (int) - the reward is given for completing an offer
- duration (int) - time for the offer to be open, in days
- channels (list of strings)

`profile.json`
- age (int) - age of the customer
- became_member_on (int) - the date when customer created an app account
- gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
- id (str) - customer id
- income (float) - customer's income

`transcript.json`
- event (str) - record description (ie transaction, offer received, offer viewed, etc.)
- person (str) - customer id
- time (int) - time in hours since the start of the test. The data begins at time t=0
- value - (dict of strings) - either an offer id or transaction amount depending on the record

## Python Libraries Used
-[Python Data Analysis Library](https://pandas.pydata.org/)  
-[Numpy](http://www.numpy.org/)  
-[Matplotlib](https://matplotlib.org/)  
-[seaborn: Statistical Data Visualization](https://seaborn.pydata.org/)  
-[scikit-learn: Machine Learning in Python](https://scikit-learn.org/stable/)  


## Results
The results showed that the most important feature of an successful offer was the amount of money a customer would get, either as a direct discount or as an extra drink. 10 Dollars seemed to be the sweet spot to become a succesfull offer, escpecally with a direct discount. The machine learning model supported that. Second most important feature out of the machine learning model, was if the offer was sent via email.


### Licensing, Authors, Acknowledgements, etc.<a name="license"></a>

Data for coding project was provided by Udacity.
