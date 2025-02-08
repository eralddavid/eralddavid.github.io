# Unfinished Thoughts

Or collection of phrases and passages that too good to forget, but still too raw to make an essay of.

### Bill Inmon, pioneer in Data Engineering, advice to somebody who's getting started in the field of data
> "I'm going to give them the same advice as if they were a bank robber: Go to where the money is. If you want to have long-term great success in our industry, find business value. Don't get hung up on > every technology that comes out, every new fangled thing that coms out. Go to where there's business value.

> Because at the end of the day, business value drives everything we do in technology."

_Source: Intro to Data Engineering course by Deeplearning.AI. Coursera_

### On the importance of knowing the data generation process first

> One thing that I like to repeat to my team when we discussing things is "How's the data is generated?". It goes by different name in other division, most popular one is business process. But the principle is that anything that the company (Ops, Marketing, Product) and user doing will generates data. A lot of it. So understanding "What part of the process generate what kind of data" isn't only important but necessary. Nailed this very first part is important for the rest of step in the data's lifecycle. With good knowledge how's the data generated, we can build data modeling on top of it. By nailing the data modeling part, we can then build BI and modelling layer.
> 
> But try asking typical analytics person that you see in the wild and you might not find any of this insight in them.

_Source: Personal notes_

### On Why Cloud is More Powerful than Old Legacy Database (like Oracle, Hadoop, etc)

> But a lot of our clients that are still dealing with on prem systems are hitting a wall there for various reasons. So one possible type of wall is that they’re using an older legacy database, that’s a high quality database, but just they run into scalability limits at some point. So no matter how big your Oracle license is, at some point, you’re probably going to hit a wall on your Oracle license, no matter how many servers you have, in some kind of a cluster, you’re probably gonna hit a wall on that, at some point, you might have a legacy Teradata system, you you re-up to a bigger system, and you still hit a wall on that.
> I think also, we’ve seen that Hadoop has become a disappointment for many organizations on prem. Because again, you run into those same fundamental issues. Plus, you need really **heavy duty expensive engineering resources** to run that cluster. So Hadoop turned out to be fantastic if you were the scale of like a Yahoo or a Facebook, and you could just build a massive cluster. And you could have these highly, highly proficient engineers, and you could scale to, you know, 5,000 nodes, and serve the data needs of the whole company. But if you’re a lot smaller, and you’re not specialized in tech, then that is going to become a real problem for you at some point. And I think that is the **big driving force behind cloud migrations**, moving away from some of those limits, and having limitless scaling as a possibility in the future.

_Source: [The Present and Future of Data Engineering with Joe Reis and Matthew Housley from Ternary Data](https://datastackshow.com/podcast/29-the-present-and-future-of-data-engineering-with-joe-reis-and-matthew-housley-from-ternary-data/)_
_Commentary: I remember one valuable tips that I got from [Cedric Chin](https://commoncog.com/author/cedric/) in regards to identifying skill domain in your particular industry is to watch the topics that expert shared to each other. This is it _
