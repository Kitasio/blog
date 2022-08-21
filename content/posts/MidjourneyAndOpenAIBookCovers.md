---
title: "Midjourney and OpenAI book covers generation"
date: 2022-08-21T21:30:15+03:00
draft: false
---


# OAI and Midjourney prompts 

## Step 1
Get the book description and translate it to English

## Step 2

Put this into OpenAI

```
<your prompt>

Tl;dr
```

## Step 3

You can modify examples but those work too, fill the prompt from the previous output

```
	Suggest a book cover
	
	prompt: The Obsidian River is a magical barrier that separates two lands - one of magical creatures and one of humans. The werewolves are in charge of guarding the humans from the creatures on the other side of the river.
	
	book cover: transparent outline of a howling wolf, inside that outline is a dark silhouette of a woman standing on a cliff under a big full moon near forest
	
	prompt: Kira is a hard worker who is focused on her career, and is not addicted to services or alcohol.
	
	book cover: pencil drawn image of a woman in a black dress on red high heels crossing a road, only legs shown
	
	prompt: In today's society, sex is a performance, sexuality is capital, and porn is an anticipation of dead sex. This leaves us without Eros, or the ability to love.
	
	book cover: gradient of red through orange abstract leaves of fire on a white background
	
	prompt: <your tldr prompt>
	
	book cover:
```

## Step 4

Generate artistic movement

```
Pick artistic movement based on this text:

text: a detective in a trench coat, standing in front of a door with a key in hand, looking suspicious

artistic movement: noir

text: <your text>

artistic movement:
```

## Step 5

Go to Midjourney and fill this in

`/imagine <book cover suggestion from Step 3> in a style of <artistic movement from Step 4> --ar 10:16`

