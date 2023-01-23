Data Scientist made in Germany

# [1. Natural Language Processing Project: Top2Vec, LDA and LSA]()

* This dataset was manually pulled from the [Twitch API](https://dev.twitch.tv/docs/api/). Using the package [rTwtichAPI in R](https://github.com/Freguglia/rTwitchAPI/blob/master/README.md), I scrpaped data for one on the most frequently displayed games on the streaming platform Twitch: *Alien Isolation*.
* The dataset contained 871 unique streaming titles. At first I divided the data into a train and test set, prepared the training corpus into one giant string, and split it by white space. I ended up with 5799 total strings of which 2835 were unique. I specifically looked at strings containing a number, a hyphen connecting two words, special punctuation, only lowercase letters, only uppercase letters, the same character 3+ times in a row, and emojis as visualized in the following table:
* I apply **Tokenization** to extract meaningful words before **word net-lemmatization** to normalize each token to extract reasonable expressions. I removed 1528 tokens that were stop words which allowed to analyze the most frequently used tokens as a single word (unigram), a pair (bigram), a triple (trigram), and as a quadruple (fourgram) as summarized in the following four charts:

### Top2Vec
* After putting the stream titles in a list, I apply applied the **unsupervised learning** mothod Top2Vec to cluster all titles into three general topics, each consisting of 339, 272, or 260 titles respectively with characteristic words for each subgroup.
* It is hard to differenciate between the topic groups because all titles were chosen to describe the game *Alien: isolation*. With the aid of the characteristic words I created a **Topic Vector** for each subgroup highlighting the streaming title which is closest to the respective topic vectors.

### Latent Dirichlet Allocation (LDA)
As a second topic analysis model, we chose Latent Dirichlet Allocation (LDA) to obtain relationships between multiple documents in a corpus and to find groups of titles with similar topics. After removing all punctuations, changing all uppercase to lowercase letters and removing all non-regular expressions and stop words, we further limit the selections of words to expressions that are represented in at least two titles and appear in a maximum of 95% of the titles. We then apply the LatentDirichletAllocation model to create four arrays of topics and words to find matching words characterizing each topic, as seen in the following table. Even though the topics are still similar to each other, the removal of stop words makes the results more differentiable.

### Latent Semantic Analysis (LSA)
* Finally, we use Latent Semantic Analysis (LSA) to extract the relationship between different words in the titles. After removing stop words, we utilize the function TF-IDF Vectorization to create a matrix of titles and total words. In the following step, we decompose this matrix to find topics and respective matching words characterizing each topic. A pivotal difference to LDA is that we can define the number of topics before we run the model. We chose five topics and showed the top 7 words characterizing this topic in the following table. As pointed out before, it is difficult to differentiate between the concepts.

## Ideas for further Research:


# [2. Classification Project: Predict Premier League Results using Machine Learning]()



# [3. Regression Project: The Change in Value of the Associate’s Degree after the Financial Crisis of 2007/2008]()





# [4. Clusering Project:]()






* Created a tool that estimates data science salaries (MAE ~ $ 11K) to help data scientists negotiate their income when they get a job.
* Scraped over 1000 job descriptions from glassdoor using python and selenium
* Engineered features from the text of each job description to quantify the value companies put on python, excel, aws, and spark.
* Optimized Linear, Lasso, and Random Forest Regressors using GridsearchCV to reach the best model.
* Built a client facing API using flask

![fghj](/images/hero (1).jpg)


For this example project I built a ball classifier to identify balls from different sports. This could be useful for someone who is new to sports from a  certain country. They could take a picture of a ball and an app could serve them some information about the history and rules of the game. This is the underlying model for building something with those capabilities.

I was able to get the model to predict the sport of the ball with 94% accuracy after minimal tuning. For most of the cases this would meet the need of an end user of the app. To get these results I used transfer learning on a CNN trained on resnet34. This created time efficiencies and solid results.
