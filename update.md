August 16th, 2018:

I had hoped to be able to use my own personal playlist and libray to feed into my recommendation system, but it seems that I can't find a way to actually extract the data. Spotify is weird in that it caps you at 100 songs for each playlist, and doesn't even allow you to access the library.

So, what does that mean for me?
I need to shelf this, and move on in my project. There is no need for me to further invest time and energy into this problem, because I dont think the results would justify the effort in the context of my project. I could very easily change the scope of my project to be on the Bag of Words dataset that I found on kaggle from MusixMix (?) and use that.

Here's the thing with that dataset.
It's immense! Thats great! More data is always good. However, it's presented as a bag of words. Ideally, I would have liked the lyrics in its intended format, but that is a copyright issue. I have to devise a game plan for how to approach this problem. I could just map it to the key that they provide! Do I know how to do that? No, but I'll figure it out. Alternatively, I could use that key, and pull/scrape the lyrics myself.

Ok. How about I do the modeling on the Bag of Words, and while that' running, I can decide on what I want to do. Sounds like a great plan.



After getting an MVP.
Let's talk about the billboard's lyrics.
So I noticed that some of the older songs are a little difficult to find on genius.com. If time permits, I would like to explore other sites just to see if that was possible. If not, I currently have 14k+ songs and their lyrics. It should be too bad.

I think I need to plot the histogram of genre deistribution afterwards lol.
Hey Jennifer, you have a previous notebook for that from Project 2, in which you can just that to grgrab the genres of the song in the background, and then do the thing.

Additionally, formating of the songs and artists is turning out to be a little weird. Sometimes there would be multple artists listed (or not) because it's a feature or collaboration. Also, because these songs are taken from Billboard, the formating and structure of songs is different from the way that genius does, thus making it a bit more difficult to map songs and lyrics together.

Important to seek advice on this issue, especially with someone who has more experience cleaning strings. I think this is something that comes with time and experience. If I can get the help later on, that would be great! However, I think I have enough data to at the least run an MVP to see if I can do what I wanted to do, and also to create the general pipeline for how I want to process my data and create the model.

Note to self: We have a notebook from yesterday that was a student exercise into recommendation engines for articles! That's a great resource.


General tips that I've learned so far. Please make sure to keep track of how you're processing your data before you do any transformations on it. An example of when that was an issue was the pre-processing of song tags before trying to scrape.
To solve this issue, I need to decide if I wanted to keep the processed tags or use the original ones that I started with. And then keep that consistent with when I try to do a join to find the songs that are missing lyrics. This caused an issue earlier that I spend a great deal of time trying to fix, and it was totally unnecessary--just need to keep track of what I'm doing and be more systematic.

Also, I want to speak to being aware of at which point in the pipeline do I save files. I can across an issue in which I was saving song lyrics each lyric at a time (as in each row of the dataframe represented a different sentence, which is not what I wanted. Because of it, I now know how to use groupby. Great. But I could have also totally avoided this problem.

