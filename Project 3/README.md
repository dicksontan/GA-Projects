# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Subreddit Classifier r/Wallstreetbets and r/Povertyfinance


### Contents:
- [Problem Statement](#Problem-Statement)
- [Datasets](#Datasets)
- [Proposed Model](#Proposed-Model)
- [Summary of Analysis](#Summary-of-Analysis)
- [Model Limitations](#Model-Limitations)
- [Future Works](#Future-Works)
- [Sources](#Sources)

---

### Problem Statement

The problem that I would like to tackle in this project is: 

As a data Scientist working for a financial advisory company, we have been tasked to classify investors who require basic savings/investment plans from higher net worth individuals who prefer higher growth investment plans. 

Through comparing 2 different subreddits that are reflective of such financially challenged or risky high net worth individuals, we aim to build a classification model and deploy on other forums so that our financial advisors can reach out to individuals with a suitable financial plan. This will thus result in greater conversion rate and more profits for the company. The subreddits that we will be choosing are r/wallstreetbets for investors looking for higher risk high growth plans and r/povertyfinance for investors who are better suited for a basic savings/investment plan.

---

### Datasets

The subreddits that we will be using are r/wallstreetbets for investors looking for higher risk high growth plans and r/povertyfinance for investors who are better suited for a basic savings/investment plan. We will scrape and analyze 10,000 posts from each subreddit.

---
### Proposed Model

We initially explored Logistic Regression, Random Forest and multinomial Naive Bayes, with Count and TFIDF vectorizers. However, we found that the model with best accuracy is a model that utilizes Count Vectorizer for bag of words model, logistic regression to find the probabilities of each post belonging to r/wallstreetbets, and then putting the probabilities together with number of comments into another logistic regression model. Though we initially achieved an accuracy of 93%, we chose to accept more false positives in exchange for false negatives, and have achieved a final accuracy score of 90.5%, with recall 97.9%. 

### Summary of Analysis

- We observe that individuals who are financially challenged are more desperate in seeking help. Our model thus pegs words such as 'help' and 'need' to them. They are also more inclined to use more common everyday financial terms, such as 'credit card' and 'bank'.

- Building on our first point, as users who are financially challenged tend to seek help, their posts will naturally attract more comments from people giving advice etc. This thus allows us to incorporate numerical features such as number of comments into the model.

- Individuals who have higher capital and prefer high risk high growth investment strategies tend to be more analytical in their post. Discussions can commonly about when to enter or exit the stock market. Moreover, they usually will use new finance terms relating to the latest trends, such as 'moon' for 'to the moon' where stock prices rise.

---

### Model Limitations

- As high growth high risk investors like to use new finance lingo, the company will have to constantly ensure that features are updated and not outdated. For example, words like 'Russia' and 'moon' plays an important role in classifying posts now due to the volatility caused by the crisis, but may not be in the future.


- The model may not be able to predict the right subreddit when keywords are taken out of context. For example, individuals may complain about their financial situation in r/povertyfinance as they may have lost their money in 'stocks', but the model will classify it as individuals with high income and can spend on high growth investment plans.


-  The model is not able to fully analyse non-ASCII characters, such as emojis and foreign characters. Though we removed them in our model, if possible, they should also be considered data observations too. For example, emojis like 🙃 is a good indicator that someone is being sarcastic. Perhaps we could use a tool like vader to process these non-ASCII characters. We could also manually train our model to understand these characters, though that will require a significant amount of time.

### Future Works

- We can explore using other models and tools. For example, instead of classifying posts using frequency of words, we can consider using word similarities/analogies such as word2vec. We can also consider using stemming instead of lemmatizing for our words. Other classifiers such as K-Nearest Neighbors classifier and boosting algorithms can also be explored.


- We notice how vader sentiment analysis is not able to read the sentiment of finance terms such as bull and bear. We can thus explore using a sentiment dictionary more relevant for finance. We can even train our own sentiment library for the model.


- We can also expand ngram words to include 3 or more words. This will allow us to find greater synergies and allow our model to encapsulate the context of the post better.
---

### Sources
    
1. https://www.forbes.com/sites/georgeschultze/2021/06/15/are-the-apes-now-running-wall-street/?sh=36860ee35e88
    
    Summary: Understood more about the term apes, which is finance lingo for banding together to buy a stock.
    
    
    
2. https://www.fidelity.com/Learning-center/trading-investing/ukraine-russia

   Summary: Understood that the Ukraine crisis caused volatility in the markets, thus resulting in much discussion among investors
   
   
3. https://www.vox.com/the-goods/22249458/gamestop-stock-wallstreetbets-reddit-citron

    Summary: Read up on the backstory of Gamestop and understood it's presence in forums.
    
    
4. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5147524/
    
    Summary: Understood how to find the optimal threshold estimation for ROC-AUC curve for a binary classifier using game theory.
    
    
5. https://www.codeproject.com/Articles/5269447/Pros-and-Cons-of-NLTK-Sentiment-Analysis-with-VADE
    
    Summary: The article talks about the weaknesses of VADER sentiment analyzer like how it is unable to understand jargon.
