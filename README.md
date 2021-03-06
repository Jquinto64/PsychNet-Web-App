# PsychNet-Web-App
- https://psychnet.azurewebsites.net/?
- PsychNet presents a way to rapidly identify social media posts, texts, or any messages that could indicate signs of depression. 
- This involves the use of natural language processing and machine learning.

![alt text](https://i.imgur.com/kFyuvdN.png)
![alt text](https://i.imgur.com/QChRhKf.png)

# Performance
- PsychNet achieved a test accuracy of ~92%, adjusted for class imbalances, with very high precision and recall scores for both classes
- The confusion matrix for the test data + classification report showing precision, recall, and F1 scores for "normal" and "depressed" posts:
![alt text](https://i.imgur.com/HilNrrd.png)
![alt text](https://i.imgur.com/1uvVHH4.png)

# Process
- PsychNet makes use of sentiment analysis.
- ~8600 Reddit posts were web-scraped, with half belonging to r/depression, and the other half coming from r/all (front page)
- Posts belonging to r/depression were labelled as "depressed", and the rest were labelled as "normal"
- The FastAI library was used to preprocess the Reddit posts, then train an AWD-LSTM model capable of identifying potentially depressive posts.
- The best model was then deployed to a web app using Flask and Microsoft Azure
