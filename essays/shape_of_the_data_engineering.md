# Shape of the Data Engineering World
### Or my practice to taking notice things that experts talk to themselves

_Created at: 2024-02-09_

_Last updated at: 2024-02-09_

I was a big fan of the study of accelerating expertise. I believe the best thing that I can do in my youth is to identify all the skill tree to become experts and overtime learning about them (my domain right now is data). That's why I found this tip from CedriC Chin is quite compelling.

![Screenshot from Commoncog's forum](/images/essays_0002/screenshot_cedric_001.png)

Full quote below
> I was thinking about how to answer this, but then I realised that there’s an easier (though time consuming!) way of figuring out where the metagame is: listen to practitioners talking to other practitioners!
> ....
>
> When a practitioner talks to another practitioner, or when the conversation is explicitly about shoptalk, I’ve found that they often can’t help themselves but talk about the meta:
> -  Investors would reference this paper or that paper, and then I would go dig it up.
> -  Investors would say things like “So what do you think about the current interest rate environment and what the Fed’s doing”, and I would mark down “I need to understand what the Fed’s doing.”
> -  Eventually the whole “active vs passive investing” debate would be brought up, but the arguments seem to change over time — arguments from podcast episodes four years ago seem remarkably different from arguments last year, which indicates how the meta (or at least the consensus take) has been evolving.
> -  Eventually someone says “So what do you think about value investing, and its horrible track record over the last 10 years?” and that clues you in to the existence of an ongoing debate.

Today somehow I'm stumbled to this great podcast by The Data Stack Show titled [The Present and Future of Data Engineering with Joe Reis and Matthew Housley from Ternary Data](https://datastackshow.com/podcast/29-the-present-and-future-of-data-engineering-with-joe-reis-and-matthew-housley-from-ternary-data/). All four of these podcasters all heavy hitters in terms of data engineering world. I bet the sum of years of experience combined is >30 (more old than me!). 

So what I found? As far as I noticed, two big topics.

## Long live modern data warehouses.
Even since the beginning the podcast touch a quite heavy subject: cloud-based data engineering. Matthew Housley (Matt) starts by retelling his experience.
> And I started the job. And as a junior data scientist, I learned about a lot of the core tools, really enhanced my Python skills by doing things with Pandas, working with data on a laptop. And at some point, I realized that the laptop-based workflow was extremely limiting. And so it just didn’t scale.
> And then the other data tools we had available in our organization were extremely slow. And also, in a sense, didn’t scale. They were just too overloaded. And then my focus gradually began to shift toward data engineering. So how can we build large efficient data systems? How can we basically provide systems that will be a force multiplier for a data scientist so they can get off of their laptops and these kind of very circumscribed tools into tools that can handle terabytes and even potentially petabytes of data

Then, they touched a bit about the challenge of all these companies that still use old legacy databases. Again, from Matt
> (Matt) But a lot of our clients that are still dealing with on prem systems are hitting a wall there for various reasons.
> 
> (Matt) So one possible type of wall is that they’re using an older legacy database, that’s a high quality database, but just they run into scalability limits at some point. So no matter how big your Oracle license is, at some point, **you’re probably going to hit a wall on your Oracle license**, no matter how many servers you have, in some kind of a cluster, you’re probably gonna hit a wall on that, at some point, you might have a legacy Teradata system, you you re-up to a bigger system, and you still hit a wall on that.
> 
> (Matt) I think also, we’ve seen that Hadoop has become a disappointment for many organizations on prem. Because again, you run into those same fundamental issues. Plus, you need really heavy duty expensive engineering resources to run that cluster. So Hadoop turned out to be fantastic if you were the scale of like a Yahoo or a Facebook, and you could just build a massive cluster. And you could have these highly, highly proficient engineers, and you could scale to, you know, 5,000 nodes, and serve the data needs of the whole company.
>
> (Matt) But if you’re a lot smaller, and you’re not specialized in tech, then that is going to become a real problem for you at some point. And I think that is the big driving force behind cloud migrations, moving away from some of those limits, and having limitless scaling as a possibility in the future.

He also adds how hard it is to fix data quality issue with these old tools and how new tool run circle around them
> (Matt) ...that hinder data science come down to really basic foundational problems like data quality, really complex ETL, it takes a long, long time to deploy fixes to data quality issues. And the interesting thing is your data scientists are smart, they’ll often find these data quality issues very quickly as they’re working on a new project.
>
> (Matt) But it might take six months to a year to actually get the fixes deployed with the somewhat non-agile legacy approach to data pipelines that many organizations have. Another big theme is just getting data in and out. So tools like Fivetran, for example, that connect from A to B are just blowing up right now, because that turns out to be a very hard problem, even though it looks simple.

### My commentary: The "So, what?"
I think this is the time where I should give structure to all of this quote. So here's the kicker: I'm so surprised to realize that "old legacy database" problem like above is somehow still exist. Yes, I'm 100% honest with you. I join the Data world when I just graduated from college, around late 2020s. In my mind, company using BigQuery, Redshift and other modern data warehouse tools is just a given fact. Oh there's this thing called Oracle? Who cares! All of the tutorial that I saw in internet are revolving around these modern tools. Reading this podcast I realize that this "scale" is just solved by these tools very, very recently. And because it's very recent, I can bet that these solution would be still relevant in the near future -- and I also still have high chance to encounter with "old legacy databases" in my work life, so I won't get any surprise.

To put this concretely: I can rest assured that burning my weekend learning about these tools is still worth it for my career, 10-20 years from now.

Kostas and Matt, again, adding their observation about these modern tools
> (Kostas) Yeah, yeah, I think that’s also a big part of the success of Snowflake, to be honest. I mean, they managed to start as a data warehouse, actually, it’s very interesting, because if you see the evolution of how they position the product in the company, I mean, it looks like you see their diagrams, it looks like the data warehouse was their MVP in a way, which is very interesting, because, I mean, it’s a pretty complex thing to build, right? But today, if you go to their main website, they don’t even call it a data warehouse.
> ...
> (Kostas) So I think Snowflake really reflects like the evolution in this space. And I think it’s, it’s very interesting.
>
> (Matt) But I think the exciting things about Snowflake and BigQuery are that you can just drop a couple petabytes of data in there if you want to. And you can be running these extraordinarily huge queries in short order. And so that means that if I am a large company, and I have, you know, petabytes of data on prem, but the hard part is just shipping that data to the cloud.
>
> (Matt) But once it’s up in the cloud, I can do these amazing things with that data. And then I can start hooking in other tools as it makes sense to do. So if I really need the power of Spark, I can plug that into Snowflake or BigQuery. Very quickly. So yeah, I find those are a pleasure to work with. And I find them both exciting because of the degree to which they can scale so easily.

## We should get the real "real time" data now
This 2nd topic is somehow caught me as interesting because it's a valid demand (I can't count how many stakeholder came to me and said that "I need this report in almost real time. Can you do it?"), but the technological barrier is quite high to do it. Or So I thought, before reading this passage from Joe

> (Joe) I think the expectation is everything is going to be real time. And actually, Google’s Dataflow paper, I think, had a really good distinction between real time and batch, and what their distinction was, instead of thinking about it in terms of real time, or batch, or streaming, think about things as bounded or unbounded by time.
>
> I mean, we only do batch right now, because it’s an artificial distinction that we have to do because of technical limitations, right So you time bound your data, but in essence, all data is actually unbounded. And so the closer you can get to sort of this organic feel with data and events just sort of happening as they happen, like, you know, the rest of the world operates, you know, like the actual, you know, world and universe is real time. It’s all event driven. Humans are the only ones that seem to batch things up.

A hallmark of good source for identifying the skill tree in the domain is when experts just casually dropping papers/article that interesting to them. I now know that, if I have free time, I might devote my brain power on understanding this [Dataflow Model by Google](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43864.pdf). 
So I actually reading this podcast is really useful for me.


