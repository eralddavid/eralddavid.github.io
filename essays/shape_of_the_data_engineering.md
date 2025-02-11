# Shape of the Data Engineering World
#### Or my practice in taking notice of things that experts talk about among themselves
***

_Created at: 2024-02-09_

_Last updated at: 2024-02-12_

I have been working for >4 years now, and there's this ugly fact that I still can't put aside on: is hard to identify a path to expertise. Most knowledge worker that I know don't try to achieve expert level in their field. For those who want, sometime they just winging it and [rarely involves deliberate practice](https://notes.andymatuschak.org/About_these_notes?stackedNotes=zUw5PuD8op9oq8kHvni6sug6eRTNtR9Wqma&stackedNotes=zMbCwoVdjsqPNyTRRr3phPN). That's why I kept collecting a faster way to identify a "path" to expertise. And while many focus on learning through documentation, courses, or trial and error, there's another powerful approach that's often overlooked: **studying how experts talk among themselves**.

This insight came from Cedric Chin, who observed that practitioners talking shop naturally surface the most critical aspects of their domain. As he explains:

![Screenshot from Commoncog's forum](/images/essays_0002/screenshot_cedric_001.png)

Full quote below, from ["What to look for to identify and describe the metagame faster"](https://forum.commoncog.com/t/what-to-look-for-to-identify-and-describe-the-metagame-faster/359/2) forum post
> I was thinking about how to answer this, but then I realised that there’s an easier (though time consuming!) way of figuring out where the metagame is: listen to practitioners talking to other practitioners!
> ....
>
> When a practitioner talks to another practitioner, or when the conversation is explicitly about shoptalk, I’ve found that they often can’t help themselves but talk about the meta:
> -  Investors would reference this paper or that paper, and then I would go dig it up.
> -  Investors would say things like “So what do you think about the current interest rate environment and what the Fed’s doing”, and I would mark down “I need to understand what the Fed’s doing.”
> -  Eventually the whole “active vs passive investing” debate would be brought up, but the arguments seem to change over time — arguments from podcast episodes four years ago seem remarkably different from arguments last year, which indicates how the meta (or at least the consensus take) has been evolving.
> -  Eventually someone says “So what do you think about value investing, and its horrible track record over the last 10 years?” and that clues you in to the existence of an ongoing debate.

This framework proved remarkably valuable when I recently encountered a podcast episode of [The Data Stack Show featuring Joe Reis and Matthew Housley](https://datastackshow.com/podcast/29-the-present-and-future-of-data-engineering-with-joe-reis-and-matthew-housley-from-ternary-data/). Their conversation, representing over three decades of combined experience, revealed two fundamental shifts in data engineering that perfectly exemplify why listening to expert discourse is so valuable.

## Long live modern data warehouses.
From the beginning, the podcast touched on a quite heavy subject: cloud-based data engineering. Matthew Housley (Matt) starts by retelling his experience.

> And I started the job. And as a junior data scientist, I learned about a lot of the core tools, really enhanced my Python skills by doing things with Pandas, working with data on a laptop. And at some point, I realized that the laptop-based workflow was extremely limiting. And so it just didn’t scale.
> And then the other data tools we had available in our organization were extremely slow. And also, in a sense, didn’t scale. They were just too overloaded. And then my focus gradually began to shift toward data engineering. So how can we build large efficient data systems? How can we basically provide systems that will be a force multiplier for a data scientist so they can get off of their laptops and these kind of very circumscribed tools into tools that can handle terabytes and even potentially petabytes of data

Then, they touched a bit about the challenge of all these companies that still use old legacy databases. Again, from Matt
> (Matt) But a lot of our clients that are still dealing with on prem systems are hitting a wall there for various reasons.
> 
> (Matt) So one possible type of wall is that they’re using an older legacy database, that’s a high quality database, but just they run into scalability limits at some point. So no matter how big your Oracle license is, at some point, **you’re probably going to hit a wall on your Oracle license**, no matter how many servers you have, in some kind of a cluster, you’re probably gonna hit a wall on that, at some point, you might have a legacy Teradata system, you you re-up to a bigger system, and you still hit a wall on that.
> 
> (Matt) I think also, we’ve seen that Hadoop has become a disappointment for many organizations on prem. Because again, you run into those same fundamental issues. Plus, you need really heavy duty expensive engineering resources to run that cluster. So Hadoop turned out to be fantastic if you were the scale of like a Yahoo or a Facebook, and you could just build a massive cluster. And you could have these highly, highly proficient engineers, and you could scale to, you know, 5,000 nodes, and serve the data needs of the whole company.
>
> (Matt) But if **you’re a lot smaller**, and you’re not specialized in tech, then that is **going to become a real problem** for you at some point. And I think that is the big driving force behind cloud migrations, moving away from some of those limits, and having limitless scaling as a possibility in the future. _(emphasis added)_

He also adds how hard it is to fix data quality issue with these old tools and how new tool run circle around them
> (Matt) ...that hinder data science come down to really basic foundational problems like data quality, really complex ETL, it takes a long, long time to deploy fixes to data quality issues. And the interesting thing is your data scientists are smart, they’ll often find these data quality issues very quickly as they’re working on a new project.
>
> (Matt) But it might take six months to a year to actually get the fixes deployed with the somewhat non-agile legacy approach to data pipelines that many organizations have. Another big theme is just getting data in and out. So tools like Fivetran, for example, that connect from A to B are just blowing up right now, because that turns out to be a very hard problem, even though it looks simple.

### My commentary: The "So, what?"
I think this is the time where I should give structure to all of these quotes. Here's the kicker: I'm surprised to realize that "old legacy database" problems like those mentioned above still exist. Yes, I'm 100% honest with you. I joined the Data world when I graduated from college, around the late 2020s. In my mind, companies using BigQuery, Redshift and other modern data warehouse tools was just a given fact. Oh, there's this thing called Oracle? Who cares! All of the tutorials I saw on the internet revolved around these modern tools. 

Reading this podcast made me realize that this "scale" problem was just solved by these tools very, very recently. And because it's very recent, I can bet that these solutions will still be relevant in the near future -- and I also still have a high chance of encountering "old legacy databases" in my work life, so I won't be surprised.

To put this concretely: I can rest assured that spending **my weekends learning about these tools** will still be worth it for my career, **10-20 years from now.**

Kostas and Matt, again, adding their observation about these modern tools
> (Kostas) Yeah, yeah, I think that’s also a big part of the success of Snowflake, to be honest. I mean, they managed to start as a data warehouse, actually, it’s very interesting, because if you see the evolution of how they position the product in the company, I mean, it looks like you see their diagrams, it looks like the data warehouse was their MVP in a way, which is very interesting, because, I mean, it’s a pretty complex thing to build, right? But today, if you go to their main website, they don’t even call it a data warehouse.
> ...
> (Kostas) So I think Snowflake really reflects like the evolution in this space. And I think it’s, it’s very interesting.
>
> (Matt) But I think the exciting things about Snowflake and BigQuery are that you can just drop a couple petabytes of data in there if you want to. And you can be running these extraordinarily huge queries in short order. And so that means that if I am a large company, and I have, you know, petabytes of data on prem, but the hard part is just shipping that data to the cloud.
>
> (Matt) But once it’s up in the cloud, I can do these amazing things with that data. And then I can start hooking in other tools as it makes sense to do. So if I really need the power of Spark, I can plug that into Snowflake or BigQuery. Very quickly. So yeah, I find those are a pleasure to work with. And I find them both exciting because of the degree to which they can scale so easily.

## We should get the real "real time" data now
This second topic caught my interest because it's a valid demand (I can't count how many stakeholders have come to me and said "I need this report in almost real time. Can you do it?"), but the technological barrier is quite high to implement it. Or so I thought, before reading this passage from Joe.

> (Joe) I think the expectation is everything is going to be real time. And actually, Google’s Dataflow paper, I think, had a really good distinction between real time and batch, and what their distinction was, instead of thinking about it in terms of real time, or batch, or streaming, think about things as bounded or unbounded by time.
>
> I mean, we only do batch right now, because it’s an artificial distinction that we have to do because of technical limitations, right So you time bound your data, but in essence, all data is actually unbounded. And so the closer you can get to sort of this organic feel with data and events just sort of happening as they happen, like, you know, the rest of the world operates, you know, like the actual, you know, world and universe is real time. It’s all event driven. Humans are the only ones that seem to batch things up.

I have a hard time figuring out the good analogy to think about this information. That's where Claude provide this witty response.

"Here's the thing about time in data: we batch things up because that's how our tools work, not because that's how the world works. It's like taking a video and turning it into a slideshow because that's all our projector can handle. But now, (theoretically speaking) we're finally getting projectors that can show the whole movie, and **suddenly everyone's realizing that maybe we didn't need slideshows** after all."

I agree. Maybe we didn't need slideshows after all.

To close this notes: A hallmark of a good source for identifying the skill tree in a domain is when experts casually drop papers/articles that interest them. I now know that, if I have free time, I might devote my brain power to understanding this [Dataflow Model by Google](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43864.pdf). 

So, weekend well spent!


