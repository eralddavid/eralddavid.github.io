# How to Combat Fraud and Stablecoins - From Reading Stripe's Annual Letter 2024

*Created: 2025-03-01*

*Last updated: 2025-03-01*

I've spent 50% of my career (uh, almost 3 years) in financial industry. And unlike many others, I think it's necessary for us to read extensively about our industries. And one of the fastest way to speed-learn our way of "What's happening in this industry, and what would like it be in the future" it's to the winning companies's statement about itself (and extensively, about the industry).

This is where I spent my (not so) precious hours on the weekend to read Stripe's Annual Letter. And maybe put commentary about it.
But not all things are worth commenting. I just want to highlight section that within my interest: Fraud, and Stablecoins.

### Fighting Fraud is Harder Than It Seem -- And Having A Good Data is Really Helpful

This section starts with mind-boggling statistics
> Fraud is a bigger drag on the global economy than you might think: one report found that fraud cost of
a typical online business’s revenue.

Worth to be repeated: 3% is a lot, especially for revenue. For comparison, big retailer Walmart's 2023 net margin are around 2.5-3%. This means that, assuming the fraudulent transactions left unchecked and all the Walmart transaction came from online, it can eliminate Walmart entire bottomline.

In the report, Stripe's mentioned an example how to combat them using their vast maount of data, and introduce a metrics called "Successful card testing attempts" about fraud that they try to reduce.

> The most effective lever we have to keep businesses safe is **Stripe’s reputation network**. Data from $1.4
trillion in annual payments volume means that each payment makes the next payment safer, a flywheel
spinning with now-considerable momentum. Stripe Radar develops a notion of trust for not only credit
cards but email addresses, IP addresses, phone numbers, shipping addresses, devices, and many more
details besides. This trust allows Stripe to precisely distinguish between expected and suspicious behavior.
>
>
> In doing so, **scale matters**. When a credit card is used for a payment, there is a greater than 92% chance
that Stripe has encountered the same card before. We can then compare this transaction to prior behavior.
For instance, if we see a card being used with a new email address, the very newness of the email address
is a suspicious fact (with a 60% higher likelihood of fraud).

"Successful Card Testing Attempts" metrics

> Last year, we saw card testers (“card testing” refers to illicit attempts to identify valid card credentials) move from guessing
card details to online card skimming. Criminals use social media to share fake websites with too-good-tobe-true deals, with the sole aim of stealing your credit card number. Those payment details are often sold off in tranches that are then tested out in the wild...
>
> As such, we also enable our models to adapt in real time, so that future decisions benefit from all prior data. When a Stripe Radar fraud model makes a decision on a payment, it knows about events that occurred 100 milliseconds ago across the Stripe network.
> With these and other techniques, we reduced card testing on Stripe by over 80% in the past two years, protecting our customers from billions of fraudulent transactions. Fraudsters: you’re going to have to start working through your lunch breaks.

### Stablecoins is the future

My interest on stablecoin is both practical and ideological. Practical because, as mentioned by Micky Malka from Ribbit Capital mentioned, it will be the next big thing that define financial industry in the next 10 years.

Excerpt from [Invest Like The Best podcast](https://joincolossus.com/episode/building-ribbit/)

> Stablecoins are travel checks in today's world. It is instant dollars anywhere in the world that you can control and move anytime at a cost of zero. And they're backed by guess what, dollars in Treasuries.
>
> Actually, to the point that when you think about the size of stablecoin market right now, there's almost $200 billion of stablecoins. People are willing to forfeit making 4% or 4½% of yield in order to have it at least saved in dollars. So imagine the opportunity cost where they're willing to sacrifice their yield just to be able to have access to dollars.
>
> Consumers took it over. What we're starting to see now is companies and treasury management of companies using it. It lowers their cost of capital, is instant. There's less resistance, they have a lot more control. So the volume of stablecoins' movement on any given month is now – you can graph it against Visa network's payment volume and it's not crazy off anymore. And that's only with $200 billion. Imagine when there's a trillion dollars sitting there and $2 trillion – it will get there.

It's also ideological. The fact that I came from a 3rd-world country (like Micky, who came from Venezuela) means that there's a very decent risk that my government f* things up and devaluate our national currency. Rupiah, my nation's currency, [right now at its lowest value](https://insight.kontan.co.id/news/pekan-penuh-tekanan-bagi-rupiah-hingga-terpuruk-ke-rp-16596-per-dolar-as). So, to hedge against devaluation by putting my money in stablecoin seems like a good strategy.

All these reason, among others, might be the caused why Stripe acquired Bridge, the world's leading stablecoin orchestration platform, on October 2024. This fact mentioned in the annual letter, along side Stripe's bold bet that stablecoin will become very impactful in the world.

> Why care about stablecoins? Improvements to the **basic usability of money make economies more prosperous**. Consider the transitions from coins to banknotes, from the gold standard to fiat currency, and from paper instruments to electronic payments. Stablecoins are a new branch of the money tree. Such transitions occur with some regularity over the centuries, and the effects tend to be large.
> 
> Stablecoins have four important properties relative to the status quo. They make money movement cheaper, they make money movement faster, they are decentralized and open-access (and thus globally available from day one), and **they are programmable**. Everything interesting follows from these characteristics.

### My other commentary and epilogue

The downside of doing this habit of "Read about the future, and think about the 2nd order effect" is that I could use it to produce something else that instant value. For instance: I can polish my Medium site, and creating a new article there. I can also read about Data Engineering stuff that I want to learn and implement in my daily work.

But I still believe that this is a good use of my time, and can help me down the line. For example: if any of our payment competitor start adopting stablecoin, that might be a trigger where my company will start following them. 
