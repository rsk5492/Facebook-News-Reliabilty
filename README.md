# Facebook-News-Reliabilty

This program is used to give a reliability factor for the news that is shared on your Facebook wall.

For this program, we have used a news dump of around 40k records, which is stored in the Hive database.


1. User data is pulled from Facebook graph API. (Be sure to get a token from Facebook add it to the program.)

2. The hive database generates a corpus.

3. Term frequency (TF) is generated from article and Inverse Document Frequency (IDF) is generated from corpus.

4. The cosine distance is calculated between the items present in article and corpus to determine the match rate.

5. The closer the cosine distance is to 1, the better the article matches the corpus entry.

6. If the article is not found in the Hive database, then web crawling will be using RSS feeds from google news as the new corpus.

7. The RSS feed is obtained by tokenizing, lemmatizing and porter stemming the article keywords and using those as URL keywords.

8. The TF-IDF and Cosine distance is once again calculated for the new corpus generated.


## Dataset link : https://www.dropbox.com/s/vdq2ksi73jhwh22/11_new_agencies-facebook-posts.zip?dl=0