## Sentiment Analysis of Intel Processor Reviews

This project explores user sentiment towards Intel processors over time through a multi-stage machine learning architecture and visualization pipeline.

### Project Goals

* Analyze sentiment from online reviews collected using a custom web scraper.
*  Perform multi-aspect sentiment analysis, identifying sentiment not just for overall impression but also for specific product aspects like performance and price.
* Uncover trends in user sentiment over time, particularly focusing on positive sentiment.
* Identify reasons behind both positive and negative sentiment expressed in the reviews.
* Visualize the sentiment trends and insights within a user-friendly platform (Power BI).

### Technical Approach

* **Data Collection:** A custom web scraper gathers online reviews for Intel processors.
* **Sentiment Analysis:**
    * A logistic regression model serves as a baseline for sentiment classification.
    * DistilBERT, a pre-trained and fine-tuned large language model (LLM), is the primary sentiment classifier, achieving high accuracy for both positive and negative sentiment.
* **Trend Analysis:** Positive sentiment data from DistilBERT is analyzed by Gemini, another LLM, to identify trends in positive perception over time.
* **Visualization:** Gemini's API is integrated with the Gradio web application, enabling visualization of the sentiment trends within Power BI.

### Tools and Technologies

* Web Scraping (custom script)
* Logistic Regression
* DistilBERT
* Gemini (Large Language Model)
* Gradio Web App
* Power BI

### Project Benefits

This project provides Intel with a robust and automated system to:

* Predict Sentiments for Reviews: Classify reviews as positive, negative, or neutral using sentiment analysis.
* Positive-Negative Trend Over Years: Track sentiment trends in reviews from 2012 onwards using visual graphs.
* Technical Specifications Insights: Extract and summarize key technical specifications from reviews.
* Reviews Starting from 2012: Focus analysis on reviews written from 2012 to the present.
* Features Offered: List features of products based on review analysis and specifications.


### Getting Started

This project primarily relies on pre-trained models (DistilBERT and Gemini) where first the sentiments  of the technical fdata was generated using fine tuned DistilBert trained on labelled user reviews.

However ,the custom web scraper script and the code for integrating Gemini's API with the Gradio web application might require further configuration depending on your specific environment.They are as follows:

Prerequisites:

1.Python environment with required libraries 
2.Create a Gemini API key

3.pip install transformers gradio pandas mentioned in notebook

4.Set environment variables for Gemini token.
5.Read the provided clean csv files:
   1.'reviews_user.csv'
   2.'tech_reviews'

6.Open the Jupyter Notebook i.e. 'Gradio - Model + Dashboard ' provided with the project.
Follow the steps outlined in the notebook:
 a.Gemini Model: Run the cells in this section to establish a connection with Gemini using your token.
 b.Web Interface: Run these cells to launch the Gradio web application.
 c.User Review Visualisation: This section processes user reviews and visualizes sentiment trends.
 d.Technical Review Visualisation and Model Prediction: This section focuses on technical reviews, allowing sentiment analysis and model predictions.

for reference tutorial video is provided below:
a)For Tech: <a>https://drive.google.com/file/d/1uQXURMuQ7w3vn06b5yFGAEVckTc155Fr/view?usp=sharing</a>
b)For User :<a>https://drive.google.com/file/d/1GE5fl317B69Gr8cs6yFWbFh0x32XoZNs/view?usp=sharing</a>

### Team Members

* Avishikta Bhattacharjee (Machine Learning Architect) - Designed and implemented the machine learning pipeline and data analysis.
* Akangkha Sarkar - Integrated the models with Gradio and developed Power BI visualizations.
* Kumar Priyanshu-In charge of the thorough data collecting using a variety of techniques, making use of sophisticated web scraping tools like Beautifulsoup and Selenium.

### Next Steps

* Explore sentiment analysis for other product categories.
* Implement real-time sentiment analysis for online reviews.
* Analyze the reasons behind sentiment in more detail (e.g., topic modeling).
