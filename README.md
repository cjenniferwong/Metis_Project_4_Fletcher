# Project Summary for Project 4 Fletcher

TLDR:
Project design:
Taking the unique songs which appeared in the Billboards Top 100 Weekly Charts, I scraped Genius and AZ Lyrics for lyrics for these songs so that I could do topic modeling for them. Then, I clustered and made a recommendation system.

Tools:
LDA + TFIDF
DBSCAN
TSNE
Tableau

Data:
Genius (scraped)
AZ Lyrics (scraped)
Billboard (scraped)
Spotify API
	
What you'd do differently next time:
	Technically, I would have written functions and classes because I felt that there was a lot of things that I was doing in my project that could have been simplified if I just written it as a function/class. The reason why I didn't, was because there were some things that I wanted to control better. 
	For example, utilizing the Spotify API to get what I needed required mental hurdles for me to get over. 
	First, I had to use the search function in the API to try to find matches with the song and artist name. The first problem that I encountered was that Billboards and Spotify have different naming conventions.
	
	There is so much that I would have done differently instead if I were to do this project again. I think the biggest sticking point was not being able to wrap my brain about what was happening when I would run the different functions. It’s one thing to be able to understand what is happening conceptually, but I found it difficult to follow how each step was applied in the context of Data Science and in terms of this project. Yes, in class we had a bunch of toy datasets, and it fulfilled its purpose of introducing us to different approaches and tools. I guess I needed to really sit down and try to understand things before I started to apply it. 
	Although it is a good thing to try to work through the problems by yourself before asking for help, something that I really struggle with is asking for help. Touching back to the first paragraph, if I can clearly identify that I don't understand something, instead of sitting there for hours, and not making any progress, I should ask for help. Either from my peers, or from my instructors, because that is what they’re here for. 
	Finally, I hope to be able to develop more confidence in myself and my abilities. I’m sure that I’m not the only one, but it definitely felt like I was the only one struggling with Imposter Syndrome. There were many times where I felt that I wasn’t good enough, and would compare myself to others, thinking that I would never be able to achieve something of the caliber that they were able to perform at. Although I know that there is a huge difference in experience level and technical ability and work that went into how others have gotten to where they are now, I can’t help but always to compare myself with them. 




## Project Design and Research
Day 1 (August 11, 2018):
I am very excited to begin this project. However, I think like most people I am having trouble figuring out what question I want my project to answer. So far, I've been picking projects that appeal to my innate curiousity of the world--of course aligning with my interests and what problems I hope to answer later on in my career. However, it's difficult to identify the business/use case for these questions. 

To summarize, what is the value that my project will bring to the world? What impact will it make?

This is not to say that I don't think doing things for the sake of doing them is not important. I think it's great to just dive deep into a problem/industry that piques your interest. However, a large part of the bootcamp is learn and master different Data Science tools to create a portfolio that would help me get a job after the bootcamp.

I have 3 areas that I am MOST passionate about (but not just 3):
1. Music and Media
2. Food
3. Dating

I don't have a hard time finding questions in these domains to answer. I am very eager to get a chance to delve into these realms and extract nuggets of insight to present to my peers. However, how do I answer a valuable business question?


August 14th, 2018--More things to add..
I found some datasets on Kaggle that will help to supplement my project. At this point, I have decided to try to cluster songs into genres based on their lyrics. 

Here are some links to the Kaggle datasets that I am interested in.

https://www.kaggle.com/mousehead/songlyrics#songdata.csv 
https://www.kaggle.com/gyani95/380000-lyrics-from-metrolyrics. 
https://www.kaggle.com/artimous/every-song-you-have-heard-almost#Lyrics2.csv

This is also in addition to the list of songs that I still have from my Project 2 ('Drop it like it's Hot') that I scraped from the Billboards Top 100.

I am also interested in trying to use the songs in my own personal Spotify library and throwing those songs in there. Sounds like fun.

Here is what I hope to achieve with this project:

Here is a summary of things I hope to achieve with this project:

1. Clustering (Unsupervised Learning)
2. One Sentence Summarizer of the entire song and Topic Modeling
3. One Sentence that represents the song (not the same as point 2)
4. Recommendation System

and if time permits, the classic:

5. Have breakdowns and question why I'm doing Data Science, and whether I am even capable of becoming a Data Scientist

Here is my plan today.
I want to finish writing the function that I will use to scrape genius.com, and have that running in the background tonight while I sleep. That way I will have data to play with the next day.

I also want to spend some time to create a game plan for myself so that I can start completing things in a more a systematic way.

Update:
Here are some links that I want to bookmart and re-visit if I have the time to do so. I want to put my own data into it.
https://developer.spotify.com/documentation/web-api/reference/playlists/
https://developer.spotify.com/documentation/web-api/reference/playlists/get-list-users-playlists/
https://developer.spotify.com/documentation/web-api/reference/playlists/get-playlists-tracks/
https://developer.spotify.com/documentation/web-api/reference/library/save-tracks-user/

I think it would also be interesting to see what clustering the lyrics does (does the definition of difference genres change over the decades?)


August 15th, 2018:
Addendum:
I think to reframe the scope of the project, I will be using songs from the billboards top 100 and my personal spotify library + playlists.

Then when I'm done, I'm going to build a personal recommendation system. 
Let's call this project: Music Jenn-erator heheheh


I think if I have time, I also want to make an eigen-album cover for each genre.
Here is an updated list of all the things that I want to do.

August 16th, 2018:

I had hoped to be able to use my own personal playlist and libray to feed into my recommendation system, but it seems that I can't find a way to actually extract the data. Spotify is weird in that it caps you at 100 songs for each playlist, and doesn't even allow you to access the library.

So, what does that mean for me? I need to shelf this, and move on in my project. There is no need for me to further invest time and energy into this problem, because I dont think the results would justify the effort in the context of my project. I could very easily change the scope of my project to be on the Bag of Words dataset that I found on kaggle from MusixMix (?) and use that.

Here's the thing with that dataset. It's immense! Thats great! More data is always good. However, it's presented as a bag of words. Ideally, I would have liked the lyrics in its intended format, but that is a copyright issue. I have to devise a game plan for how to approach this problem. I could just map it to the key that they provide! Do I know how to do that? No, but I'll figure it out. Alternatively, I could use that key, and pull/scrape the lyrics myself.

Ok. How about I do the modeling on the Bag of Words, and while that' running, I can decide on what I want to do. Sounds like a great plan.

After getting an MVP. Let's talk about the billboard's lyrics. So I noticed that some of the older songs are a little difficult to find on genius.com. If time permits, I would like to explore other sites just to see if that was possible. If not, I currently have 14k+ songs and their lyrics. It should be too bad.

I think I need to plot the histogram of genre deistribution afterwards lol. Hey Jennifer, you have a previous notebook for that from Project 2, in which you can just that to grgrab the genres of the song in the background, and then do the thing.

Additionally, formating of the songs and artists is turning out to be a little weird. Sometimes there would be multple artists listed (or not) because it's a feature or collaboration. Also, because these songs are taken from Billboard, the formating and structure of songs is different from the way that genius does, thus making it a bit more difficult to map songs and lyrics together.

Important to seek advice on this issue, especially with someone who has more experience cleaning strings. I think this is something that comes with time and experience. If I can get the help later on, that would be great! However, I think I have enough data to at the least run an MVP to see if I can do what I wanted to do, and also to create the general pipeline for how I want to process my data and create the model.

Note to self: We have a notebook from yesterday that was a student exercise into recommendation engines for articles! That's a great resource.

General tips that I've learned so far. Please make sure to keep track of how you're processing your data before you do any transformations on it. An example of when that was an issue was the pre-processing of song tags before trying to scrape. To solve this issue, I need to decide if I wanted to keep the processed tags or use the original ones that I started with. And then keep that consistent with when I try to do a join to find the songs that are missing lyrics. This caused an issue earlier that I spend a great deal of time trying to fix, and it was totally unnecessary--just need to keep track of what I'm doing and be more systematic.

Also, I want to speak to being aware of at which point in the pipeline do I save files. I can across an issue in which I was saving song lyrics each lyric at a time (as in each row of the dataframe represented a different sentence, which is not what I wanted. Because of it, I now know how to use groupby. Great. But I could have also totally avoided this problem.

1. Clustering (Unsupervised Learning)
2. One Sentence Summarizer of the entire song and Topic Modeling
3. One Sentence that represents the song (not the same as point 2)
4. Recommendation System
5. eigen-album cover for each genre.

and if time permits, the classic:

6. Have breakdowns and question why I'm doing Data Science, and whether I am even capable of becoming a Data Scientist.




August 17th, 2018:
Some things that I learned from working on my project yesterday.
1. There is a reason why everyone says commit early, and commit often.... I need to get over my commitment issues. Speaking of which, I should commit right now.

2. Understanding the mathematical/computer science concepts that are happening when you call these functions and make these models are extremely important. Otherwise it is extremely difficult to troubleshoot your problem, because you don't understand what's going on. Taking the time to understand what is happening under the hood allows you to make better decisions about the methodology of which you are applying these steps, and help to make a better project.

However, I do recognize that a huge motivation for this project is to just get your hands dirty. That means shifting through the problems slowly (at least for me it does) and just getting comfortable with being uncomfortable.


That said, I was able to at least get some topic modeling done yesterday! Yay! Progress!
Today, my goal is to get some clustering and a basic af recommendation system up and running. Then I will try a better approach of scraping for some more songs, and then also think of a way to scrape my spotify library.

For Genius, I should try to utilize the search function LOL.... stop trying to brute force it.


Also, That is also my goal this weekend. yay!
If time permits, try some super awesome neural nets maybe idk.

Also, Jennifer, think about how you're going to link genius, billboard, and spotify together. You should create a function that searches spotify and grabs the uri and then stores it. This is important to be able to grab the song's information beyond just having the lyrics.

Maybe I should also consider using the spotify streaming charts to grab more songs. And then the additional datasets available on Kaggle. I should just use those too... LOL 


