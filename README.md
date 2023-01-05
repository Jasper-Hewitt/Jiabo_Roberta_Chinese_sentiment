# Final project

Sentiment analysis (https://github.com/Jasper-Hewitt/final_project_elections/blob/main/ElectionSentiment.ipynb)

fine-tuned model on Hugging Face (https://huggingface.co/Jiabo/Roberta_Chinese_sentiment)

training notebook (https://github.com/Jasper-Hewitt/final_project_elections/blob/main/Roberta_train_postest_weight_1epoch.ipynb)

tweet_scraper (https://github.com/Jasper-Hewitt/final_project_elections/blob/main/tweet_scraper.ipynb)

## Summary
In this project we set out to do a Chinese binary sentiment analysis (pos/neg) of the 2022 Taipei mayoral elections on Twitter. To this end, we fine-tuned hfl/chinese-roberta-wwm-ext on a training dataset with 20 286 manually labelled posts (negative: 13917 / positive: 6369). In order to compensate for our unbalanced training data we adjusted the class weights to 1.457642 and 3.185115, respectively. The model scores an accuracy of 0.9058 on our testing dataset. 

We then used tweet_scraper to collect over 9285 tweets（Chiang Wan-an：2755, Huang Shan-shan：1688, Chen Shih-chung：4842), let our model predict the sentiment, and plotted the results in several charts. The data can be found in the data folder. 

More information about the training process can be found in the paper, including an elaborate table that explores different training possibilities. (https://github.com/Jasper-Hewitt/final_project_elections/blob/main/paper_%26_presentation/Jiabo:Roberta_Chinese_sentiment.pdf)  

## instructions 

### predict and visualize your own data
 If you have an excel file in the same format as the files in our data folder, you can simply replace the data for some of the candidates with your own data. For example, you can replace 'scrap_shanshan.xlsx' in pd.read_excel('/content/scrap_shanshan.xlsx') with your own .xlsx file, and run the code. your file does not necessarily have to be tweets. Weibo posts or anything else will also work; the regex is broad enough to remove most of the noise. 

### scrape more tweets
scrape new tweets: If you want to scrape new tweets you can refer to tweet_scraper and the instructions provided in that notebook. You will have to run the scraper on your local machine and first install Selenium and Chromedriver. After the webdriver opens, you will have to manually login to Twitter and set the advanced search parameters in the webdriver, after this you can just run the sixth cell to start scraping the tweets. THere is two important things to pay attention to when scraping the Tweets. 

- Make sure to set the search results to 'latest' to collect the Tweets in a chronological order. 
- Try not to touch anything when the scraping process is going on. clicking the webdriver by accident or doing too many things in the background may interrupt the scraping process. 

The scraper is based of https://github.com/israel-dryer/Twitter-Scraper/blob/main/twitter-scraper-tut.ipynb (we made several adjustments).
