# Challenge 2 - 2023

Welcome to the second challenge of Fermyon’s Advent of Spin 2023! 🥳

This second challenge is more of an optimization challenge, where you get to apply your computer science skills.

You'll need to use

- Spin CLI
- Your favorite programming [language](https://www.fermyon.com/wasm-languages/webassembly-language-support/) supported in Spin
- [Hurl](https://hurl.dev/docs/installation.html)
- A JSON API

If this is your first time with Spin, [Challenge 1 from 2022](../../2022/CHALLENGE-1/README.md), is the perfect introduction to get you started. 

This year the stakes are higher, and the challenges...more challenging. The Fermyon elves have decided to help Santa use Serverless WebAssembly for Santa's new web application. Your task is to help the elves get the project up and running before Christmas Eve.

The elves will hang out in the Fermyon [Discord](https://discord.gg/AAFNfS7NGf) server, and can help answer questions along the way.

## Spec

This time around, the elves need to help Santa prepare for his travel around the world with all of his presents. Now, we're all used to seeing Santa taking off in his sleigh with a *knapsack* of presents (hm is there a clue there, we wonder). But we know that it's impossible for ALL the presents to be handed out in one trip! So Santa has to make multiple trips which can be time-consuming. 

Now travel time is not an issue for Santa, with his hypersonic reindeer but the elves want to optimize the number of kids Santa can reach on each trip. Your main consideration is how the elves load the knapsack, optimizing for the number of kids that receive gifts, given the combined weight of presents to a single house, and the sleighs total capacity.

The elves will use your application, by sending a request to its root and giving it arrays of: 

* The number kids in a given house, and 
* The total weight of the presents for those kids. 

Your job is to tell the elves how many of those kids Santa can optimally reach in one trip.

The body of the POST call to `/` will contain a JSON object which can look like this:
```JSON
{
    "kids": [1, 4 , 5, 6, 3, 2, 7],
    "weight": [23, 45, 23, 43, 12, 32, 45],
    "capacity": 120
}
```
Capacity is the weight that a sleigh can carry (excluding Santa 🎅🏻)

- When posting, the elves expect an HTTP status code `200` to be returned and a body detailing how many kids can be reached given the data set provided:
- 
```JSON
{
    "kids": 20
}
```
- Also, the header in the response should contain `Content-Type: application/json` 

## Test

You can run our [Hurl](https://hurl.dev) test suite with `hurl --test test.hurl`, which will carry out tests, similar to what the elves will use your application for, when you submit it. Ensure you have `hurl` [installed](https://hurl.dev/docs/installation.html).

## Submit

Once the application is deployed, enter the endpoint as serviceUrl below and run the command - e.g., `https://x-mas.fermyon.app`

> Note: Do not add a trailing `/` to the serviceUrl.

```shell
hurl --error-format long --variable serviceUrl="https://x-mas.fermyon.app" submit.hurl
```

After your submission, pat yourself on the back as you helped Santa deliver presents to kids around the world. And for your present aka some Fermyon Swag go [here](../../README.md#Prizes) and submit your form. Yes, you have to make a submission for each challenge.

## Nobody Must Code Alone!

Please don't hesitate to reach out to the elves on Fermyon [Discord](https://discord.gg/AAFNfS7NGf) server if you have any questions, they may be busy this time a year, but they are always ready to help and answer questions. This is a great opportunity to meet others in the community as well. We’ll also post on [X/Twitter](https://twitter.com/fermyontech) and [LinkedIn](https://www.linkedin.com/company/fermyon), dropping some helpful resources and videos.

Remember there are prizes for each challenge. So it may be you, to whom the elves will deliver a nice award to.

Note: If you submit using Fermyon Cloud, we will contact you for any awards you may win. If you aren't using the Fermyon cloud to host your application, please reach out to the elves on Fermyon [Discord](https://discord.gg/AAFNfS7NGf) to register your submission
