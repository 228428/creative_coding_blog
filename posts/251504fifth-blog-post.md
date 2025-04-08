---
title: Redundancy, Style, & Refactorisation
published_at: 2025-03-24
snippet: What I learnt in week 4
disable_html_sanitization: true
allow_math: true
---

# Week 4 Session 1

## Reflection

This week we officially started diving into Assignment 4, and honestly... chaos is the perfect word for it. The assignment is all about complexity, randomness, and exploring generative art, which is a whole new world for me — but kind of exciting.

We got a breakdown of what we need to do, and it starts with reading three essays. We have to pick one to respond to creatively. I started reading “What is Generative Art: Complexity Theory as a Context for Art Theory,” and I’m already seeing how the ideas of compression, randomness, and repetition are going to be really important.

We also had to set up GitHub properly for the project — using a template and pulling it into VS Code. Mux walked us through the anatomy of a website and what all the different folders and files do. It’s a lot, but he said he’ll go over it again so I’m not too stressed. You’re allowed to use p5.js for this assignment, which makes me feel a bit more comfortable since I’ve already been using that for my lantern piece.

One of the big concepts this week was recursion, especially in p5. We looked at an example called recursive_rectangles, where a function keeps calling itself to draw smaller and smaller rectangles. It was kind of mind-blowing but also made sense in a weird way. We also learned about requestAnimationFrame(), which helps create smoother animations and can be used for recursive drawing in the browser.

Another key point was learning how variables need to be declared outside of functions if you want their values to persist — otherwise, they just reset every time the function runs.

Compression, Chaos & Complexity, in my words I learned that:

Low compressibility means things are super random, no clear pattern, and unpredictable.
High compressibility means things are super repetitive — you could easily describe them with a short set of instructions.
High effective complexity is when it’s somewhere in the middle — like a system that looks chaotic but has hidden structure.
So for the next assignment, it’s basically: Go crazy... but on purpose. 😅

## HomeWork

High compressibility

<iframe id="Inspiration" src="https://editor.p5js.org/228428/full/S3m5YQ5-w"></iframe>

Low compressibility

<iframe id="Inspiration" src="https://editor.p5js.org/228428/full/rxhUYeEMb"></iframe>

High effective complexity

<iframe id="Inspiration" src="https://editor.p5js.org/228428/full/AWdwaVejj"></iframe>

The first sketch represents high compressibility. It’s a simple grid of evenly spaced dots. Every dot is the same size and perfectly aligned across the canvas. There’s no randomness, no surprise — just repetition and pattern. You could easily describe it in one sentence: “It’s a grid of dots spaced 50 pixels apart.” The code uses a double for loop to create the grid. This kind of pattern is easy to understand, predict, and recreate. Because it follows a clear, repetitive structure, it's considered highly compressible. There’s not much variation — but that’s kind of the point. It’s neat and structured, almost mathematical.

The second sketch takes a total turn. It’s an example of low compressibility — the chaotic sibling of the first. In this version, the code draws 200 random shapes (circles or rectangles), placed at random positions, with random sizes and fully random colours (including transparency). There’s no grid, no structure, no logic you can visually follow. Each time you refresh the page, it looks completely different. This is what makes it low compressibility — you can’t compress the pattern into a short explanation because there isn’t one. It’s unpredictable, abstract, and full of visual noise. The randomness creates energy, but there’s no clear system holding it together.

Then there’s the third sketch — and this is where things get interesting. This one is my attempt at creating high effective complexity, where the art feels like a balance between order and chaos. The base of this sketch is still a grid, just like the first example. But inside each grid cell, I introduce randomness: the stroke colour is randomly chosen, the shape might be a rectangle or an ellipse (randomly selected), and the width and height vary slightly every time. The result is a composition that feels alive — like it has rules, but also breaks them just enough to stay interesting.

So what exactly creates the structure in this third example? It’s the grid system — the repeated for loops that anchor the shapes to specific spots on the canvas. Each shape is centered around a grid point, and that gives it a foundation. But the random decisions layered inside each grid cell — like size, colour, and shape type — create variation and surprise. This is what makes the sketch feel playful without being chaotic. You can sense the pattern, but you’re never sure what the next block will hold.

Through these three sketches, I’ve started to see how compression and complexity exist on a spectrum. At one end is full repetition and order (high compressibility). At the other end is pure randomness (low compressibility). But the real magic — at least for me — is in the middle. That space of high effective complexity is where art can feel both thoughtful and unpredictable, structured and expressive.

That’s the space I’m most excited to keep exploring. I want my generative work to feel alive — like it has a rhythm, but also its own personality. Something that surprises people while still making sense in its own quiet way.

3.  For this task, I looked at the work of Rosa Menkman, a digital artist who is known for making glitch art. Her work mixes structure (like video formats and code) with randomness (like digital errors or broken files) to create something really interesting and complex.

One of her artworks I liked was “The Collapse of PAL”. It’s based on an old video format called PAL, which was used for TV in Europe. Normally, PAL follows a strict set of rules. But Rosa messes with those rules on purpose. She breaks them to create glitchy, colourful images that flicker, bend, and distort.

Even though it looks chaotic, the glitching is not totally random. It’s built on a real system — so there’s still structure underneath the chaos. That’s what makes it an example of high effective complexity. You can see patterns, but there’s also surprise and randomness. It’s like controlled chaos.

Rosa uses these glitches to make us think about the digital systems we rely on — like how fragile they are, and how even small changes can break them. Her work is a mix of technical knowledge and creativity, and that’s what makes it powerful.
