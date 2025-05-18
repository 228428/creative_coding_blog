---
title: Week Four
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

# Week 4 Session 1

## Reflection

I wasn’t in class this week, but I did read some of the text about glitch art and datamoshing, and honestly, it was kind of wild but super interesting.

The artwork they talked about — Compression Study #1 — takes a music video from Rihanna and blends it with the Cranberries’ Zombie, using digital glitches to make it all fall apart in this weird, beautiful way. It looks random, but it’s actually very controlled. The artists choose when and how to “break” the video. That balance between chaos and control is what makes it so powerful.

The reading also explained the difference between analog and digital. Analog is more smooth and blended (like sunsets or paint mixing), while digital is more clean and blocky (like pixels or computer code). Datamoshing kind of lives between those two — it’s digital, but it looks messy and emotional, like a painting that’s melting.

One thing that stuck with me is that glitch art isn’t just messing things up for no reason. It’s about taking something that’s supposed to be “wrong” and turning it into something creative. That feels really relatable.

## HomeWork

<canvas id="glitch_self_portrait"></canvas>

<script type="module">
  // get the canvas element by its ID
  const cnv = document.getElementById(`glitch_self_portrait`);

  // set the canvas width to match its container and height to 16:9 ratio
  cnv.width = cnv.parentNode.scrollWidth;
  cnv.height = (cnv.width * 9) / 16;

  // set background color for loading
  cnv.style.backgroundColor = `deeppink`;

  // get the 2D drawing context
  const ctx = cnv.getContext(`2d`);

  let img_data; // we'll store base64 image data here later

  // draws an image (i) to fill the canvas
  const draw = (i) => ctx.drawImage(i, 0, 0, cnv.width, cnv.height);

  // create a new image element
  const img = new Image();

  img.onload = () => {
    // once loaded, update canvas height to match image aspect ratio
    cnv.height = cnv.width * (img.height / img.width);

    // draw the image to canvas
    draw(img);

    // get a base64 string version of the image
    img_data = cnv.toDataURL("image/jpeg");

    // start adding glitches
    add_glitch();
  };

  img.src = `/scripts/251504/me.JPG`;

  // helper: return a random whole number under max
  const rand_int = (max) => Math.floor(Math.random() * max);

  // glitchify: remove random chunks of the image data string
  const glitchify = (data, chunk_max, repeats) => {
    const chunk_size = rand_int(chunk_max / 4) * 4; // glitch chunk must be a multiple of 4
    const i = rand_int(data.length - 24 - chunk_size) + 24; // start somewhere safe in the string
    const front = data.slice(0, i); // keep the start
    const back = data.slice(i + chunk_size); // keep the end, skip the chunk
    const result = front + back; // combine it back together

    // if we still have repeats left, do it again
    return repeats === 0 ? result : glitchify(result, chunk_max, repeats - 1);
  };

  const glitch_arr = []; // array to hold all the glitched frames

  // add a glitched frame to the array
  const add_glitch = () => {
    const i = new Image();
    i.onload = () => {
      glitch_arr.push(i);
      if (glitch_arr.length < 12)
        add_glitch(); // keep generating until we have 12
      else draw_frame(); // then start animating
    };
    i.src = glitchify(img_data, 96, 6); // create glitch and load it into an image
  };

  let is_glitching = false; // track if we're showing a glitch
  let glitch_i = 0; // which glitch frame we're on

  // the animation loop
  const draw_frame = () => {
    if (is_glitching) draw(glitch_arr[glitch_i]);
    else draw(img);

    // chance to switch state
    const prob = is_glitching ? 0.05 : 0.02;
    if (Math.random() < prob) {
      glitch_i = rand_int(glitch_arr.length);
      is_glitching = !is_glitching;
    }

    requestAnimationFrame(draw_frame);
  };
</script>

```html
<canvas id="glitch_self_portrait"></canvas>

<script type="module">
  // get the canvas element by its ID
  const cnv = document.getElementById(`glitch_self_portrait`);

  // set the canvas width to match its container and height to 16:9 ratio
  cnv.width = cnv.parentNode.scrollWidth;
  cnv.height = (cnv.width * 9) / 16;

  // set background color for loading
  cnv.style.backgroundColor = `deeppink`;

  // get the 2D drawing context
  const ctx = cnv.getContext(`2d`);

  let img_data; // i'll store image data here later

  // draws an image (i) to fill the canvas
  const draw = (i) => ctx.drawImage(i, 0, 0, cnv.width, cnv.height);

  // create a new image element
  const img = new Image();

  img.onload = () => {
    // once loaded, update canvas height to match image aspect ratio
    cnv.height = cnv.width * (img.height / img.width);

    // draw the image to canvas
    draw(img);

    // get a image string version of the image
    img_data = cnv.toDataURL("image/jpeg");

    // start adding glitches
    add_glitch();
  };

  img.src = `/scripts/251504/me.JPG`;

  // helper: return a random whole number under max
  const rand_int = (max) => Math.floor(Math.random() * max);

  // glitchify: remove random chunks of the image data string
  const glitchify = (data, chunk_max, repeats) => {
    const chunk_size = rand_int(chunk_max / 4) * 4; // glitch chunk must be a multiple of 4
    const i = rand_int(data.length - 24 - chunk_size) + 24; // start somewhere safe in the string
    const front = data.slice(0, i); // keep the start
    const back = data.slice(i + chunk_size); // keep the end, skip the chunk
    const result = front + back; // combine it back together

    // if we still have repeats left, do it again
    return repeats === 0 ? result : glitchify(result, chunk_max, repeats - 1);
  };

  const glitch_arr = []; // array to hold all the glitched frames

  // add a glitched frame to the array
  const add_glitch = () => {
    const i = new Image();
    i.onload = () => {
      glitch_arr.push(i);
      if (glitch_arr.length < 12)
        add_glitch(); // keep generating until we have 12
      else draw_frame(); // then start animating
    };
    i.src = glitchify(img_data, 96, 6); // create glitch and load it into an image
  };

  let is_glitching = false; // track if we're showing a glitch
  let glitch_i = 0; // which glitch frame we're on

  // the animation loop
  const draw_frame = () => {
    if (is_glitching) draw(glitch_arr[glitch_i]);
    else draw(img);

    // chance to switch state
    const prob = is_glitching ? 0.05 : 0.02;
    if (Math.random() < prob) {
      glitch_i = rand_int(glitch_arr.length);
      is_glitching = !is_glitching;
    }

    requestAnimationFrame(draw_frame);
  };
</script>
```

🎭 Glitching Myself: Aesthetic Reflection
Rendering my self-portrait through glitch code completely changes how I see myself — and how others see me too. Instead of a clean, smooth image, my face becomes unstable, flickering, and distorted. It no longer looks “correct,” and that’s exactly what makes it interesting.

From Ngai’s aesthetic registers, I think this self-portrait falls mostly under “the interesting” and “the zany.” It’s interesting because it makes you stop and try to figure it out — the glitch disrupts expectations, and you have to look longer. It’s zany because it’s constantly shifting, flickering between clean and broken frames. There’s energy, confusion, and even a bit of chaos.

The concept of effective complexity really comes through here. The glitchy portrait isn’t just random — it uses a clear structure (drawing the same image again and again), but it adds randomness by cutting chunks out of the data. This creates a balance between order and disorder — enough structure to understand what’s going on, but enough unpredictability to keep it alive and dynamic.

From the Glitch Readings, I connected most with Chroma Glitch, where they talk about turning digital errors into something meaningful. Instead of hiding mistakes, glitch artists highlight them — they turn failure into form. That’s exactly what’s happening in my portrait: what’s “wrong” becomes the visual language.

From the Net Art Readings, I thought about artists like JODI, who mess with websites to break the user experience on purpose. Like them, I’m using code to disrupt what people expect — not just to be aesthetic, but to make people notice how digital systems work and what happens when they fall apart.

So overall, glitching my likeness takes it from a normal image to something that’s full of questions, energy, and a kind of digital honesty. It’s not about being perfect — it’s about being expressive, unpredictable, and maybe a little unhinged 💥
