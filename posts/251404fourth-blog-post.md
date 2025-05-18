---
title: Week Three
published_at: 2025-03-21
snippet: What I learnt in week 3
disable_html_sanitization: true
allow_math: true
---

# This is Week 3 Session 1

## Reflection

In this class, Mux Thomas explained functions and classes in a way that actually made sense to me.

He said a function is kind of like a set of instructions—like writing a recipe.

Defining the function is just writing the recipe down.
Calling the function is actually doing the thing—like cooking the food.
In p5, some functions just get called on their own (like draw() and setup()), which is cool.
He also mentioned something called side effects, which is when a function changes something outside of itself. He said they’re quick and easy, but can also make things messy if you’re not careful.
We also talked about inputs and outputs in functions:

The inputs are called arguments
The outputs are what the function returns
Then we moved onto classes, and Mux explained them like cookie cutters 🍪.

The class is the cutter itself—the shape.
The constructor() is what fills it with the dough (your object data).
Then you can make a bunch of objects that all use the same shape but have different ingredients (like different colours, positions, speeds, etc.)
We also talked a bit about using images and sound:

A dot (.) means we’re using a method (something the object can do)
A field is the info the object holds (like its colour or size)
push() is a method that puts things into an array
loadSound() is how we get a sound file into our sketch so we can use it
Overall, this session helped a lot. I don’t fully get everything yet, but Mux’s explanations made it feel less scary. It feels like I’m starting to understand how to build more interesting stuff by combining functions and classes.

## HomeWork

<iframe id="cute" src="https://www.whywashesad.com/"></iframe>

visiting whywashesad.com by Rafaël Rozendaal
In this piece, the screen is filled with a solid blue background and several flat 2D clouds moving at a fairly fast speed across the screen. The clouds aren’t fluffy or soft — they’re simple vector shapes with bold black outlines, kind of like cartoon drawings. The interaction is really minimal but fun: when your mouse hovers over a cloud, it disappears with a small popping sound.

Visuals
The clouds are outlined, flat shapes — not detailed or gradient, just clean and 2D.
The blue background is simple and solid — no texture, just a smooth, sky-like tone.
The fast movement of the clouds adds energy — it doesn’t feel super calm like fluffy clouds, but more like a slightly playful, arcade-y vibe.
The design is still charming because it’s so minimal — cute in a graphic, intentional way, almost like a sticker or a zine illustration.

Sound
When you hover over a cloud, it makes a short, light “pop” sound.
It’s not over-the-top or loud — just a quick burst that’s satisfying.
The sound gives feedback without being annoying. It’s almost like the cloud wants to pop when you hover over it.
There’s no background music — just silence and the occasional “pop.”

Interaction
No clicking needed — just hovering makes the cloud disappear.
The clouds don’t reappear, so it kind of feels like you’re clearing the sky.
The interaction is playful, but also a bit weirdly meditative — you can slowly wipe the screen clean of clouds if you feel like it.
It’s super easy and low-stress. There’s no goal, no game over, no score.
Even though it’s not “kawaii” cute, this piece is cute in a graphic, quirky, and satisfying way:

The visuals are bold and flat, but not aggressive.
The interaction is simple, immediate, and responsive.
The sound is playful and light, adding fun without chaos.
It feels like a digital toy — something you could zone out with, or mess with just because it’s oddly satisfying.

<iframe id="draft" src="https://editor.p5js.org/"></iframe>
This version of my Tangled-inspired sketch is made using only functions, variables, and arrays — no classes yet. I wanted to get the look and feeling right before jumping into more complex code. My goal is to create a piece that feels soft, emotional, and magical, and is a tribute to my grandmother (my kindred spirit).

The inspiration comes from the lantern scene in Tangled, where floating lanterns rise into the night sky. In this version of my project, every time the user clicks anywhere on the canvas, a lantern appears right at that spot, floats upward, and disappears with a gentle motion and sound.

Here’s how I’m building the aesthetic of “cute” through visuals, sound, and interaction:

Visually Cute
To make the piece visually cute, I focused on soft shapes, glowing effects, and pastel colors. Each lantern is a rounded rectangle in warm tones like peach, pink, and golden yellow. Beneath the lantern is a soft glow effect, created using a translucent white ellipse. The background is a solid deep navy blue, like a peaceful night sky, scattered with small white stars to bring a dreamy vibe.

The lanterns float slowly and gently upward, which gives the whole sketch a sense of calm and comfort. There's no fast motion or harsh lines—just soft visuals and easy movement.

Sonically Cute
I added a soft chime sound that plays every time a lantern is released. It’s short and sweet, not too loud or dramatic—more like a magical sparkle sound. There’s no background music in this version yet, but I plan to add the Tangled instrumental soundtrack in the next version to really tie the whole mood together.

This one gentle sound helps build the cute mood by making every click feel like a little moment of magic. It rewards the interaction without overwhelming it.

Interactively Cute
Instead of using a button, I wanted the interaction to feel natural and free. In this sketch, all you do is click anywhere on the canvas. Wherever you click, a lantern appears and floats upward from that exact spot.

There are no rules, limits, or goals. You can click once, or a hundred times. Each lantern is slightly different in color, size, and speed, which keeps the experience playful and alive.

This kind of interaction is low-pressure and calm, and makes the whole experience feel like a digital wishing well. That freedom, slowness, and softness is what makes it feel cute.

This version of my AT1 sketch doesn’t use classes yet — just basic functions and arrays — but it helped me build the vibe and feeling I want. The visuals are soft and dreamy, the sound is light and rewarding, and the interaction is simple but meaningful.

Even without advanced code, I’m already getting the aesthetic of cute across by making it:

Visually calm and pastel
Sonically gentle
Interactively friendly and magical
Next up, I’ll refactor this into a version with classes to clean up the code and make it easier to add more features like fading, background music, or even animated sparkles.

But for now, I’m really happy with how this version captures the emotion and sweetness I’m trying to express

# Week 3 Session 2

## Reflection / HomeWork

This session, I had to leave class early because I was feeling really tired and overwhelmed. I wasn’t able to fully focus, and I didn’t want to push myself too hard mentally, so I chose to step away and rest. Sometimes you have to listen to your body and mind, and I’m learning that that’s okay.

Even though I couldn’t stay for the whole class, I still wanted to keep up, so I made sure to complete the homework on my own time. Below is my response.

How my AT1 uses each concept:

Variables: I use variables like lanternsAllowed to control whether lanterns can appear, and starCount to control how many stars are drawn in the sky.

Functions: I define and use custom functions such as drawSky() to organise my code and keep things clean and easy to read.

Iteration: I use for loops to repeat actions, like drawing multiple stars in the background and looping through the lanterns array to update and display them each frame.

Boolean Logic: I use boolean logic in conditions, like checking if (lanternsAllowed) before allowing a lantern to appear.

Arrays: I use arrays to store multiple objects. The lanterns array keeps track of all the floating lanterns, and the stars array stores information about each star.

Classes: I created a Lantern class to control how each lantern behaves. It includes a constructor and methods to update and display each lantern, making the code more organised and scalable.

Rough Draft Embedded:

I’ve embedded a rough draft of my AT1 project on my blog. It features a full-screen night sky, soft glowing stars, and Rapunzel-inspired lanterns that float when the user clicks anywhere on the screen. Each lantern appears with a soft chime sound.

How well I achieved cuteness:

In the visual domain, I focused on soft colours, pastel tones, glowing effects, and gentle motion. I think the rounded lantern shapes and sparkly stars help achieve a dreamy, cute vibe.

In the sonic domain, the soft chime that plays when a lantern appears adds a small moment of magic. It’s light and satisfying, which fits the cute aesthetic without being overwhelming.

In the interactive domain, clicking to release lanterns feels gentle and pressure-free. There are no rules, just the joy of floating lanterns and making wishes. I think this calm and playful interactivity helps reinforce the cute mood of the piece.

Communities and resources I used:

I used the p5.js reference site to understand how different functions work, and I learned a lot from in-class examples and feedback. I also relied on my own notes, tutorials, and feedback from my tutor to refine and improve my code. I used ChatGPT to help explain some confusing parts and organise my logic.

What I’ve enjoyed most:

I’ve really enjoyed the creative process of bringing my vision to life. Being able to visually design something that feels personal and magical has been very rewarding. I also liked learning how to control small interactions and make them feel soft and emotional.

What I found surprising:

I was surprised at how small changes—like colour choice or animation speed—can make a big difference in how something feels. I also found that using a class made my code much easier to understand and expand, which I didn’t expect at first.

What I’ve struggled with the most:

The most challenging part has been managing sound and trying to make it work consistently. I also found some of the logic with classes and arrays confusing at first, especially when trying to remove objects from arrays or handle multiple lanterns. But over time, I started to understand it more by experimenting and reviewing the code step by step.
