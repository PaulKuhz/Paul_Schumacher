Data Scientist made in Germany

# [1. Natural Language Processing Project: Top2Vec, LDA and LSA]()

* This dataset was manually pulled from the [Twitch API](https://dev.twitch.tv/docs/api/). Using the package [rTwtichAPI in R](https://github.com/Freguglia/rTwitchAPI/blob/master/README.md), I scrpaped data for one on the most frequently displayed games on the streaming platform Twitch: *Alien Isolation*.
* The dataset contained 871 unique streaming titles

* Starting with Top2Vec as an unsupervised learning method, we tried to cluster all the titles into general topics. Therefore, we put at first all the stream titles in a list and applied the Top2Vec model. It narrowed down all titles into three main topics/ categories, each consisting of respectively 339, 272, or 260 titles. The following table summarizes the characteristic words for each subgroup.

*As we can see, it is hard to tell the difference between the topics since there is a lot of overlap of words between the topic groups because all the titles were chosen to describe the game Alien: isolation. In the following step, we use these characteristic words of the topic words to create a Topic Vector for each subgroup. Lastly, for each of the different Topic Vectors, we print the streaming titles, which in all their words, are closest to the respective topic vectors, as shown in the following graph.

* Finally, we use Latent Semantic Analysis (LSA) to extract the relationship between different words in the titles. After removing stop words, we utilize the function TF-IDF Vectorization to create a matrix of titles and total words. In the following step, we decompose this matrix to find topics and respective matching words characterizing each topic. A pivotal difference to LDA is that we can define the number of topics before we run the model. We chose five topics and showed the top 7 words characterizing this topic in the following table. As pointed out before, it is difficult to differentiate between the concepts.



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
