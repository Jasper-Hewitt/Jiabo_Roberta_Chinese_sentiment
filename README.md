# Final project

Sentiment analysis (https://github.com/Jasper-Hewitt/final_project_elections/blob/main/ElectionSentiment.ipynb)

fine-tuned model on Hugging Face (https://huggingface.co/Jiabo/Roberta_Chinese_sentiment)

training notebook (https://github.com/Jasper-Hewitt/final_project_elections/blob/main/Roberta_train_postest_weight_1epoch.ipynb)

scraper (https://github.com/Jasper-Hewitt/final_project_elections/blob/main/tweet_scraper.ipynb)

## Summary
In this project we set out to do a Chinese binary sentiment analysis (pos/neg) of the 2022 Taipei mayoral elections on Twitter. To this end, we fine-tuned hfl/chinese-roberta-wwm-ext on a training dataset with 20 286 manually labelled posts (positive: 13917 / negative: 6369). In order to compensate for our unbalanced training data we adjusted the class weights to 1.457642 and 3.185115, respectively. The model scores an accuracy 0.9058 on our testing dataset. 

We then used tweet_scraper to collect over 9285 tweets （Chiang Wan-an：2755， Huang Shan-shan：1688， Chen Shih-chung：4842), let our model predict the sentiment, and plotted the results in several charts. 

More information about the training process can be found in the paper, including an elaborate table that explores different training possibilities. (https://github.com/Jasper-Hewitt/final_project_elections/blob/main/paper_%26_presentation/Jiabo:Roberta_Chinese_sentiment.pdf)  

## instructions 



