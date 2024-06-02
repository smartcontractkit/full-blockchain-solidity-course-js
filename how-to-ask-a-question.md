# How to ask a question

> Note: Before reading this, you might want to read my guide on [top 6 tips to solve any software engineering error](https://medium.com/better-programming/top-6-tips-to-solve-any-software-engineering-error-a794a162fcaf).

Also note, take this pledge: "I solemnly swear that after asking a question I will spend at least 5 minutes trying to answer someone else's question. I will consult the 'How to answer a question' page before I do so. "

The internet is our documentation, and we want to treat is as such. **Every** _specific_ question we have _should_ be able to be found by typing it into a web search bar.

Now, there are no "bad" questions, but there are poorly-formatted questions. A poorly formatted question has a low chance of being answered, poor chance of being discovered, and can "clutter up" forums and discussion boards. So let's make sure we strive for well-formatted questions!

# Full Examples at the bottom!

Here are the steps to ask a well-formatted question:

1. Search to see if the question has already been asked
2. Know where to post your question
3. Make a title that summarizes the problem
4. Introduce the problem before writing any code
5. Make sure you format code using backticks (```) and a language tag
6. Make sure you copy paste your code instead of using screenshots
7. Make sure your code is a minimal example

# 1. Search to see if the question has already been asked

## Do not skip this step!

We should consider the internet as one giant document. If a question has already been asked and you can find the answer on the first page of your search engine, that's great! There's no need to ask the question again.

However, if the answer is not on the first page of your search results, then **you should definitely ask the question on a forum, even if you know the answer.**

Our goal is to have every tech question to be :

1. Indexed by search engines
2. Easy to find
3. Easy to reproduce.

This way, if you forget the answer in 6 months, you can simply search for it on Google and it will appear.

We don't want multiple questions about the same topic, as it can scatter information across different sources. Rather, we want to consolidate all answers, comments, and discussions in one place.

# 2. Know where to post your question

I categorize questions into one of three:

- Specific code based questions
- Generic theoretical questions
- "In the know", support, or emergency questions

## Specific code based questions

These are what we strive for. These are reproducible questions that help the world. You'll want to put these questions in places like:

- The "Q&A" discussions section of this course
- stackoverflow
- stack exchange ETH.

These are questions that typically can have a "right" or "many right answers". Generally, these are not very opinionated questions.

These are questions like "How to convert bytes32 to uint256".

## Generic Theoretical Questions

These are questions that likely do not have a canonical answer. These are questions like "which blockchain should I deploy to?" or "How could I make a game that involves many random characters?". They belong in places like:

- The "General" discussions section of this course
- A generic forum like Reddit, Twitter
- Discord (like some of the ones people have started here)

Ideally, you put these on an indexed forum like reddit and the general discussions section instead of discord so others can do a web search for the problems.

## "In the know", support, or emergency questions

These are very specific use cases and 99% of your questions will not be these kinds. These are questions like "we just got hacked, can you help us?", "Want to join my team", etc. They are questions that likely only apply to your situation and what you are doing. They belong in:

- Discord DMs
- Email
- etc

And should be used _very_ sparingly.

# 3. Make a title that summarizes the problem

It should be minimal, searchable, indexable (by search engines).

## Examples:

Bad:

- I'm stuck, please help

Good:

- Could Not Detect Network using WSL & Ganache

Bad:

- hardhat error

Good:

- TypeError: Cannot read property 'length' of undefined - when deploying contract

# 4. Introduce the problem before writing any code

When asking a question, it's important to provide details about what you're trying to do, what you've done so far, and a brief summary of the problem you're facing.

If you're asking a question related to a specific course, you can also include a timestamp in the discussions tab to indicate where you're experiencing the issue. Please include a link to the location in the video as well."

# 5. Make sure you format code using backticks (```) and a language tag

To ensure your question is easy to read, it's important to format it properly, especially when including code snippets.

Your code should show up like this:

```javascript
// my code here
```

In your question, you'll type it like this:

````
```javascript
// my code here
```
````

If your question isn't formatted properly, you can edit it to make it more readable. Usually, you can do this by clicking on the three dots located at the top-right corner of your question and formatting it nicely.

# 6. Make sure you copy paste your code instead of using screenshots

We want web crawlers to index every word you write, so even copy paste errors (and format them with 3 backticks!)

# 7. Make sure your code is a minimal example

There are two types of code questions:

- Debug me
- Specific questions

Don't be a "Debug Me"

## Example of a poorly formatted question (a debug me question):

Hi I'm confused my code isn't working here is all my code

```javascript
// pretend I pasted like 300 lines of code here
```

## Example of a much better question

I'm getting `error x` on line 42 of my code:

```javascript
const some_var = "dog";
// this is the line that is erroring
```

[More information on reproducible code.](https://stackoverflow.com/help/minimal-reproducible-example)
