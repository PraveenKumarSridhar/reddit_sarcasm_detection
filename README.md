Reddit Scarcasm Detection
==============================

Using reddit data to detect sarcasm in the comments. The aim of our project is to detect if the comments in Reddit threads are sarcastic or not. Sarcasm detection is an arduous task, as it’s largely dependent on context, prior knowledge and the tone in which the sentence was spoken or written. It is crucial to know what exactly sarcasm is since its borders are not exactly well defined unlike in sentiment analysis where the sentiment categories are very clearly defined (”love” objectively has a positive sentiment, ”hate” a negative sentiment no matter who you ask or what language you speak).

Dataset
==============================
This dataset contains 1.3 million Sarcastic comments from the Internet commentary website Reddit. The dataset was generated by scraping comments from Reddit containing the (sarcasm) tag. This tag is often used by Redditors to indicate that their comment is in jest and not meant to be taken seriously, and is generally a reliable indicator of sarcastic comment content.This is a balanced dataset.
Attribute Information:
1. label: If comment is Sarcastic or not
2. comment: The comment for which we need to determine if its sarcastic or not
3. author: Author of the comment
4. subreddit: The subreddit in which the comment was posted
5. score: The net of upvote and downvotes
6. ups: The number of upvotes
7. downs: The number of downvotes
8. date: The date comment was posted
9. created utc: The timestamp when the comment was posted.
10. parent comment: The parent comment to which the comment was posted as a response.

![image](https://user-images.githubusercontent.com/69740366/149646723-b3295b2e-da3c-41ed-8c58-48f2c111f02d.png)


Results:
==============================
The below table shows that we started with using Logistic Regression with TF-IDF which gave us an accuracy of 68.32%. However, no improvement was observed with other models except FastText and Bi-directional LSTM with one_hot.

![image](https://user-images.githubusercontent.com/69740366/149646611-f073bd33-9462-4b94-9c3d-182e99a80528.png)

![image](https://user-images.githubusercontent.com/69740366/149646617-4c0dac0c-522a-4953-ab73-5e7682d29c9a.png)

After using the models listed in above table, we found that the "Bidirectional-LSTM with one_hot" performs the best and results in an accuracy of 72.15%. Hence, moving forward with this model we have shown the confusion matrix
below based on it.

![image](https://user-images.githubusercontent.com/69740366/149646659-39a34a67-8540-47c8-8170-782d6a21dce1.png)


