# Making-A-Text-Summarizer
7 Steps to make a text summarizer

### I recently made a text summarizer for my app - News Bits. The algorithm is private as it is a part of the app that is on the play store but I'm going to use this space to describe exactly how I built it.


#### 1) Scrape the website - Use JSoup for Android
#### 2) Break each sentence into tokens using an NLP library (I used Apache's Open NLP)
#### 3) Now compute the intersection between each sentence (intersection - Get f(s1,s2) : {s | s exists in s1 and s2} )
#### 4) Normalize the Intersection Value=> iVal(s1,s2) = f(s1,s2) / ( (length(s1) + length(s2) ) /2)
#### 5) Make a matrix (n x n [where n is the number of sentences in the text] ) and store the iVal for each pair of sentences
#### 6) Sum up the iVals for each sentence
#### 7) Select the top x sentences based on their iVals. 


