Data Scientist made in Germany

# [1. Natural Language Processing Project: Top2Vec, LDA and LSA]()

* This project shows my contribution to the program [*Twitch Twits*](https://medium.com/@ucladsu/analyzing-gaming-trends-with-stream-titles-and-viewer-statistics-4a6bc17385e5) for the student association [Data Science Union](https://www.datascienceunion.com/) at UCLA.
* The dataset was manually pulled from the [Twitch API](https://dev.twitch.tv/docs/api/). Using the package [rTwtichAPI in R](https://github.com/Freguglia/rTwitchAPI/blob/master/README.md), I scrpaped data for one on the most frequently displayed games on the streaming platform Twitch: *Alien Isolation*.
<img src="https://github.com/PaulKuhz/Paul_Schumacher/blob/main/images/cloud.png" width=50% height=50%>

* The dataset contained 871 unique streaming titles. At first I divided the data into a train and test set, prepared the training corpus into one giant string, and split it by white space. I ended up with 5799 total strings of which 2835 were unique. I specifically looked at strings containing a number, a hyphen connecting two words, special punctuation, only lowercase letters, only uppercase letters, the same character 3+ times in a row, and emojis as visualized in the following table:

<img src="https://github.com/PaulKuhz/Paul_Schumacher/blob/main/images/specia.png" width=50% height=50%>

* I apply **Tokenization** to extract meaningful words before **word net-lemmatization** to normalize each token to extract reasonable expressions. I removed 1528 tokens that were stop words which allowed to analyze the most frequently used tokens as a single word (unigram), a pair (bigram), a triple (trigram), and as a quadruple (fourgram).

### Top2Vec
* After putting the stream titles in a list, I apply applied the **unsupervised learning** mothod Top2Vec to cluster all titles into three general topics, each consisting of 339, 272, or 260 titles respectively with characteristic words for each subgroup.
<img src="https://github.com/PaulKuhz/Paul_Schumacher/blob/main/images/topvec.png" width=50% height=50%>

* It is hard to differenciate between the topic groups because all titles were chosen to describe the game *Alien: isolation*. With the aid of the characteristic words I created a **Topic Vector** for each subgroup highlighting the streaming title which is closest to the respective topic vectors.
<img src="https://github.com/PaulKuhz/Paul_Schumacher/blob/main/images/insta.png" width=50% height=50%>

### Latent Dirichlet Allocation (LDA)
 * After removing all punctuations, changing all uppercase to lowercase letters and removing all non-regular expressions and stop words, I extract expressions that are represented in at least two titles and appear in a maximum of 95% of the titles.
* I apply the **LatentDirichletAllocation** model to create four arrays to find matching words characterizing each topic.
* The topics are still similar to each other, but the removal of stop words makes the results more differentiable than in the output created by Top2Vec.
<img src="https://github.com/PaulKuhz/Paul_Schumacher/blob/main/images/lda.png" width=50% height=50%>

### Latent Semantic Analysis (LSA)
* After removing stop words, I utilize the function **TF-IDF Vectorization** to create a matrix which can be decomposed to find topics and respective characterizing words.
* A pivotal difference to LDA is the chosen the number of topics as I select five topics and showed the top seveb words characterizing each topic in the following table.
<img src="https://github.com/PaulKuhz/Paul_Schumacher/blob/main/images/thirdpic.png" width=50% height=50%>

### Application of this Project:
* ftgzhnuim


# [2. Classification Project: Predict Premier League Results using Machine Learning]()



# [3. Regression Project: The Change in Value of the Associate’s Degree after the Financial Crisis of 2007/2008]()

 



# [4. Clustering Project:]()
