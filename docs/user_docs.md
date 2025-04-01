# User Docs

_**The BirdDog User Docs focus on the technical features of BirdDog and how to implement them. For a more practical guide on how to use BirdDog to drive revenue for your team, please visit the Application Docs.**_

## BirdDog SCOUT Overview

The BirdDog SCOUT system helps sales people reasearch, rank, and monitor their account list. 

More specifically, BirdDog lets users:

1. **Define Signals:** _Signals can be anything from a question about the employee count to company level objectives or tech stack or the identification of key personnel._ 
2. **Enter Accounts:** _Accounts are entities to be tracked. They can be public companies, private companies, smbs, funds, government entities, or anything else--the only requirement is that they have a url._
3. **Define ICPs:** _Ideal Customer Profiles (ICPs) are different lists that you can organize accounts & signals by._

Given a set of signals & accounts, BirdDog will look for information on each signal for each account. After the initial pull, BirdDog will continue to monitor each account for changes in relation to any of its signals.

Additional, Ideal Customer Profiles (ICPs) allow you to organize accounts & signals by specific groups for better organization & more targeted questions. 

To derive value from data, BirdDog has many workflow features to make it very easy for sales professionals to action the located data, driving revenue for the user's org. To learn more about leveraging BirdDog to generate revenue, we suggest starting with the Application Docs.

## Signals

Almost all of the data BirdDog gives you will come from Signals you define in the system. They give you tailored background information on the company, send you real time alerts, and rank your account list.

At a high level, Signals are questions you want answered about your prospect list.

From another angle, Signals are variables in a custom data set that BirdDog fills out on your behalf for each account. 

To input a signal, you simply need to select a data type, write the question, and select a rank.

Each user will have a maxinum number of avaiable signals. You are free to delete signals & add new ones as you please, as long as you stay under your total limit.

This section focuses on adding signals. While most users will heavily lean on the Question Library to add questions, there are some more advanced features explained below.

### Question Library

The easiest way to add a question to BirdDog is via the "Question Library." This collection has some very common questions alredy formatted in the best possible way for SCOUT to read.

80% of the questions actively being run in the system by all users comes from this list. All you have to do is select a question and then give it a title that you like.

### Selecting a Signal Type

Most signals will be a Yes / No question, but there are four options available.

It is important to note that for whatever type of question you select, you will be given a lot of context around the answer--a yes / no question doesn't just return a "yes", it returns the _why_!

1. **Yes / No**: The most common type of question, this allows you to ask almost anything about the account.
2. **Person**: The second most common type, Person questions surface people who match your target persona.
3. **Multiple Choice**: These questions let you define options for BirdDog to select from. If you want to know a firm's cloud providers, you might enter "AWS, GCP, Azure, Oracle". 
4. **Number**: Number questions can help you estimate numeric data about the firm.

Most questions can be framed as Yes or No. 

As an example, if you want to know what year the firm was founded, you could ask, "Does {account} say what year it was founded?"

### Formatting the Question

BirdDog requires that every question added to the system has the word 'account' surrounded by the {} brackets, like this: {account}.

Additionally, each question must end with a question mark. 

While you can get very creative with the question formats that you enter, here are some of the best performing formats:

- Does {account} do a specific thing?
- Did {account} do a specific thing?
- Did a founder or executive at {account} discuss a specific thing?
- Is {account} doing a specific thing, like hiring?
- Who at {account} matches a specific persona?

Note that these questions all tend to have {account} near the start of the sentence, and only have it occur once. The system likes that better!

### Signal Rank & Disqualification

Each signal will have a user defined rank of high, medium, or low that effects the account scoring algorithm.

High Importance questions are worth 2x as much as Medium Importance questions. Medium Importance questions are worth twice as much as Low Importance questions.

Typically, you'll want to reserve the High Importance ranks for really important signals or signals that aren't so common. That way, when that rare signal does happen, it will move the account towards the top of the pile.

On the other hand, you'll want to save Low Importance ranks for background information or much more common signals.

Additionally, you can set a signal’s rank to be “disqualify.” This means that if we find a positive answer for that signal, the score will be 0 and the account will be hidden from your main list so you don’t have to focus on it.

### Bad Questions?

While a lot can go into a great question, don't be afraid to play around making new ones. BirdDog will give you feedback on your questions if it notices something is off. 

On top of that, in the question menu, each question will have a counter for how many times it came back with a positive answer. That way, you can see questions with low hit rates and either edit or remove them.

And, of course, you're always able to contact support for more help designing the question for you.

### Special & Modifier Tokens

BirdDog supports a number of options that can either slightly alter or dramatically change the functionality of the question. 

Rather than including a bunch of extra dials and nobs on the platform, you can enable this functionality for a question by leveraging tokens, which are simply words and phrases you can include in your question.

**Modifier Tokens** have a lighter effect on the question, such as constraining the date of the data we’ll include in the answer to a smaller window. On the other hand, **Special Tokens** dramatically change the way that a question is answered and typically use an entirely separate pipeline.

The below outlines different tokens available for your use in BirdDog. As a precaution, if one of the Special Tokens are detected, the system will warn you as you upload it into the system.

Both Special Tokens have a number of templates in the Signal Library.

#### <u>Time Token - Modifier Token</u>

If you want to constrain the results of a BirdDog query to only pull data from the last year, all you have to do is include the word “**recent**” or “**recently**” in your signal. 

If you’d like a more specific constraint, you can end the signal with any of the following phrases, replacing n with the desired number, either typed out or as a digit:

- “**in the last n days**”
- “**in the last n months**”
- “**in the last n years**”

BirdDog will use these Time Tokens to compute the appropriate look back window.

And finally, if you’d like a event to be within a range, such as perhaps as an exec who was added three months ago but not more than six months ago, or a funding round 1 year old but not 2 years old, you can explicitly say this:

- “**in the last 90 to 180 days**”
- “**in the past 1 to 2 years**”

#### <u>Source Token - Modifier Token</u>

If you’d like to constrain the scope of BirdDog’s search to only be the company website, you can add the phrase “**on their website**” to the question.

#### <u>Link Token - Special Token</u>

Sometimes, you want to know if a company links from the website to some other source. This can be super useful if you want to know what ATS or payment process a company uses, among other things. 

An easy way to find out is to use the Link Token. To trigger it, create a multiple choice question starting with “**Does {account} link to…”** Then, you can write whatever sort of description you want, like “a payment processor” or “an ATS.”

The real important part, though, is filling out the urls in question as the list of options for the multiple choice question. So, in the case of an ats, you might include a list like, “[greenhouse.io](http://greenhouse.io/), [smartrecruiters.com](http://smartrecruiters.com/), [myworkdayjobs.com](http://myworkdayjobs.com/), [successfactors.com](http://successfactors.com/), [icims.com](http://icims.com/), [welcometothejungle.com](http://welcometothejungle.com/), [ashbyhq.com](http://ashbyhq.com/).”

Then, when BirdDog goes to run the question, it will check the company’s site for outbound links & report back with what it found.


#### <u>Employee Count Token - Special Token</u>

If you only want to focus on accounts above or below a certain threshold, you can use the Employee Count Token by writing a yes/no question with: “**Does {account} have [MORE/LESS] than N employees?**”

Then, you just replace **[MORE/LESS]** with either “more” or “less” and the number with the desired number of tokens. From there, the system will go ahead and compare your number directly to the employee count we’ve recorded on our platform. 

A lot of the time, this can be useful as a disqualifier question to filter out accounts with employee count above or below a certain number.

<i>
CAUTION: Our employee count comes from *the number of employees the account has on LinkedIn*. This typically works pretty well, but you might have issues with it in the case of universities or very large companies. As an example, Boeing has ~117K employees on LinkedIn, while their website boasts 170K.
</i>


## Accounts

An account is any entity that you want BirdDog to track.

Usually, an account is a company, but it can also be a nonprofit organization, a university, a government agency, sovereign entity, or really any other sort of organization you can imagine. 

Each account is uniquely identified by it’s url.

### Background Data

While BirdDog will hunt for the user defined signals for each account, as a default, the system will look for some of the following basic info:

- Short & Long background descriptions
- HQ Address
- Ticker & CIK if publicaly traded
- Employee count via LinkedIn Employees
- Company LinkedIn url

### Adding Accounts

To add accounts, you can enter a comma separated list of the urls into the account page. Alternatively, you can email the BirdDog team a CSV and they will upload the accounts for you.

When adding an account, you will be asked which ICP you want to add it to. For more information on that, please visit the ICP section.

### Credits

You can allocate any number of credits to different users in your org. The allocated credits determine both the maximum number of accounts that can be tracked at any given time & the number of new accounts that can be added each month.

### Active vs Inactive Accounts

An active account will be consistently monitored by the BirdDog system for updates. 

If you deactivate an account, while the system will no longer watch for new signals on that account, you will still have access to historic data that the system has already pulled on it.

There is no limit to the number of Inactive Accounts you can keep in the system at any given time.

### Non English Accounts

As a default, accounts with a site that is mainly in a non english language will be rejected by BirdDog.

Users on an Enterprise plan can request support for specific languages.

## ICPS

ICPs are lists that help you organize your accounts & questions. 

### Master ICP

When your account is provisioned, you will be given a Master ICP.

Any signal you add to the Master ICP will be asked across all of your accounts, even the ones outside of the Master ICP.

### Other ICPs

You can provision any number of ICPs you want outside of your master ICP. 

These other ICPs enable you to ask specific questions for that ICP which are not asked to any other accounts.

Some users will use ICP for prospects at different stages of funding, others will use them for different geographic regions, or even different industries. 

### Signal Limits

The remaining number of signals you can add is calulcated on an ICP by ICP basis. 

If you are entitled to 15 Signals per account, and you have 10 signals in your Master ICP, then you can add 5 more signals to each other ICP. 

However, if you have 10 Signals for your Master ICP and 5 in another ICP, you cannot add anymore Signals to tthe Master ICP, as that would cause the other ICP to have 16 Signals total.

## Scoring

Your accounts will be given a custom score based on the quantity and recency of signals that BirdDog finds. 

The score is on a scale of 0 to 100. 

More often than the score, you will see the percentile that an account ranked in its ICP. A 99th percentile account is better than most other accounts in that ICP, while a 10th percentile account is not very good compared to most of the other accounts in the ICP.

Typically, 90th percentile accounts will have a score in the range of 60-80. 

A 100 is very rare and an exceptional account—it means we found a very high certainty positive answer for each yes or no question for that account. 

On the other hand, a 0 means we found no positives for any of your signals.

### Adjusting the Score

For each signal, you’re able to edit the relative weighting of each score. A “normal” importance question is 2x as important as a “low” importance question, and a “high” importance question is 2x as important as a “normal” importance question.

### Disqualifier Signals

If return a positive for a disqualifier signal for one of your accounts, the rest of the scoring elements will be ignored and the account will rank lower than your accounts with a score of 0.

## Farsight

BirdDog Farsight leverages your existing accounts & signals to proactively find strong fit "look alike" accounts. 

Unlike a black box ai look alike finder, Farsight will always supply you with the "why" behind the account it selected for you.

You can enable Farisght with one of two different modes for each ICP, Limited Mode & Unlimited Mode. 

Farsight performs best when each ICP represents a list of accounts with similar industries. Meaning Farsight will work better with an ICP dedicated to law firms & another ICP dedicated to retail outlets than it would with one ICP mixing both.

### Limited Mode

Farsight Limited Mode is what you will choose if you already have a limited, pre defined universe of accounts you are prospecting from. For example, if your leader gave you 900 or even 2000 accounts, you can add all of them into Farsight for the appropriate ICP. Or, if there are only 10,000 accounts in the whole world you could ever possibly sell to, you could upload them all to Farsight.

Then, you can activate Farsight Limited mode, and it will intelligently scan through your list to find some of the best fit accounts.

As it picks out high scoring accounts, it will populate them on the Farsight page, including a description of why Farsight thought it was a great account. Then, in one click, you can add it to your account list.

### Unlimited Mode

Farsight Unlimited Mode is great if your universe of potential clients is unbounded or difficult to define. Many of our users at smaller sales teams or startups without concrete account lists use Unlimited Mode to help them always have a list of new accounts on standby.

Even in unlimited mode, you can still upload a list of accounts to Farsight. It will prioritize ranking those accounts over going out and looking for new ones.

## Email Templates

Users & Admins are able to create email templates in the platform.

These templates can then be attached to signals for one click email generation. 

<i>
It is important to note that while this is a powerful feature, one email does not replace multi channel, multi threaded outreach. BirdDog helps you augment and expedite the sales processes that you know work, not replace them.
</i>

### Defining a Template

To define a template, you need two things:

1. An Example Email
2. An Templatized Version of that Email

You can copy and paste an example email that you like sending into the add template section of the profile page. 

From there, you past a templatizd version into the template slot.

To make the templated email, you just replace the word or phrase you want BirdDog to write with a brief instruction surrounded by <<\>\>.

Here is an example email & a corresponding template:

<u>Example Email</u>

> Conrgats on the recent Series A!

> We've helped companies at your point with growth. 

>Free for a chat?

<u>Template Email</u>

> <<note about recent funding\>\>

> We've helped companies at your point with growth. 

> Free for a chat?

When this template is used, BirdDog will replace "note about recent funding" with a customized phrase.

### One Click Email Gen

To enable One Click Email Gen for a given signal, you can attach the email template to a signal on the Signals page.

??? info "Can I use the same template across signals?"

    You can reuse the same template across signals, but you cannot add multiple templates to one signal!

Then, when you see the answer or a top article for that signal on the account page, the one click email gen will use your template, the article, and context about the company to write an email. 

If you don't have a template attachd to a given signal, the One Click Email Gen will select from some pre determined templates to write your message.

**It is strongly recommended that you review all emails & messaging generatd by BirdDog before sending anything to a propsect.**
