---
title: "Midjourney and OpenAI book covers generation"
date: 2022-08-21T21:30:15+03:00
draft: false
featuredImage: "/cat.jpg"
---


# OAI and Midjourney prompts 

## Step 1
Get the book description and translate it to English

## Step 2

Put this into OpenAI, you can modify this prompt with different examples and styles to suit your needs

```
Suggest a book cover idea (avoid faces)

styles: medieval, Banksy, Polish poster, Hajime Sorayama,  90’s blacklight poster, poster, high-tech, cyberpunk, vaporwave, alien, modern, ancient, futuristic, retro, realistic, dreamlike, funk art, abstract, pop art, impressionism, minimalism, noir, photorealism, octane render, unreal engine 5, holographic, graffiti, watercolor painting

example: Mockingjay is about Katniss fighting in the rebellion against the Capitol, while also trying to save Peeta from being brainwashed. Gale becomes more ruthless and Katniss starts to doubt her feelings for him. Prim is killed in a bombing, Katniss kills Coin, and she and Peeta eventually have children.
1. The overall vibe of the text is dark and serious.
2. It is a novel about a young girl who is fighting in a rebellion against her government, and also trying to save her love from being brainwashed.

output: a burning golden pin of a jay bird catching an arrow on a black background, photorealism

example: Bella Swan turns 18, breaks up with Edward Cullen, and becomes depressed. She is then saved by Jacob Black and the Quileute werewolves and decides to become a vampire.
1. The text has a dark and depressing tone.
2. It is a vampire novel.

output: a red ink watercolour with a howling wolf on a vinous round background, in a minimalist style

example: The novels take place in a fictional world with magic and dragons and in which seasons last for years and end unpredictably. The principal story chronicles the power struggle for the Iron Throne among the great Houses of Westeros.
1. The text has a dark, medieval feel to it.
2. It is a novel about a power struggle for the Iron Throne, and it is in the fantasy genre.

output: an iron throne made of a thousand swords standing in a majestic throne room forged by the flames of the ancient dragon, in a medieval style

example: House Atreides is assigned to govern the planet Arrakis, which is the only source of the valuable spice substance. The Atreides are betrayed by their physician and killed, but Paul, their son, escapes into the desert and is accepted by the Fremen who believe him to be a messianic figure. Paul establishes himself as the new leader of Arrakis and wrests control of the Empire from the Emperor.
1. The overall vibe of the text is one of hope and determination. 
2. It belongs to the science fiction genre.

output: a man walking in a distance on an endless dune with two suns above his head, one bigger than the other, minimalist flat illustration

example: <your book description>
```

## Step 3

Go to Midjourney and fill this in

`/imagine <output from openAI> --ar 10:16`

