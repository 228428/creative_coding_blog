---
title: Week Two
published_at: 2025-13-04
snippet: What I learnt in week 2
disable_html_sanitization: true
allow_math: true
---

# This is Week 2, Session 1

## Reflection

In this session, we shifted gears and explored the concept of the "cute aesthetic" in creative coding. It was really interesting to break down what makes something "cute"—from soft colors and round shapes to playful interactions and personality in design. I hadn’t really thought about how intentional those design choices are, and how they can evoke emotion through code.

We also spent time talking about Assignment 1, which helped me better understand what’s expected and how to approach it. It was reassuring to hear examples and be able to ask questions in class. The assignment feels a little less scary now, especially after seeing how the "cute" theme could be a starting point for creative, lighthearted ideas.

This session gave me a new perspective on how aesthetics and mood can be part of coding—not just functionality. I'm starting to get more comfortable with the idea that code can have personality, and I'm excited to bring that into my work.

## HomeWork

🌸 Cute Visuals
During our class discussion, and in my chat with Joolie, we agreed that cute visuals often include:

Rounded shapes
Pastel or bright colours
A slightly messy feature, but in a way that’s still readable and charming
Oversized features, which often make characters or elements feel more expressive and endearing
If I were to create something in this style, I would use a soft, inviting colour palette—pinks, creams, mint greens—and give elements a glowing outer edge to make them feel warm and huggable. I’d avoid harsh lines or sharp corners and lean into gentle, bubbly forms.

Cute Visuals
Example: A soft, round blob creature with pastel colors and a glowing edge
Why it's cute: Rounded, imperfect shapes feel more playful and alive. Soft pastel tones make it feel gentle and friendly. Glowing edges give it a magical, dreamy vibe.
p5.js Techniques:

Use ellipse() for roundness
Apply pastel colors with fill(r, g, b) using soft RGB values (e.g. fill(255, 200, 220))
Add a glowing feel by drawing multiple blurred ellipses or layering with low alpha values (transparency)

🎵 Cute Sounds
To me, cute sounds are:

Short and squeaky, but not jarring
Light and soft, similar to small animal noises
Vaguely musical, with melody over noise
Noise on its own doesn’t feel cute—you have to shape it with tone or pitch to give it a personality. Think of a soft chime or a gentle beep that feels happy and non-threatening. I’d try to build sounds that feel like they’re smiling.

Cute Sounds
Example: A soft, high-pitched squeak or bell chime when the user clicks
Why it's cute: Light, short, and melodic sounds remind us of toys, small animals, or notifications in calming games like Animal Crossing.
p5.js Techniques:

Use the p5.sound library
Load and trigger a soft sound using mousePressed() and sound.play()
Keep the sound short and use a gentle envelope or reverb for softness

✨ Cute Interactions
A cute interaction, in my opinion, is:

Quick and responsive
Gives immediate, playful feedback, like a glow or a ripple
Feels gentle and not too serious
For example, clicking on an object might make it bounce slightly or emit a faint glow ripple, giving the feeling that it’s alive and acknowledging your touch. These small gestures can really bring charm and emotion into digital experiences.

Cute Interactions
Example: Clicking causes a ripple or sparkle that expands gently and fades away
Why it's cute: It creates a sense of delight and feedback without being too loud or aggressive. Soft, responsive animations feel more emotionally satisfying.
p5.js Techniques:

Use mousePressed() to trigger an effect
Animate circles using ellipse() that grow in size and fade using alpha values

### Assignment 1 Plan – "Lanterns for Grandma"

For Assignment 1, I want to create an interactive piece inspired by the Disney movie Tangled, which holds a special place in my heart. The concept of glowing lanterns floating into the night sky reminds me of peace, hope, and connection—feelings I associate with my kindred spirit: my grandmother. This piece is a tribute to her.

My idea is to simulate lanterns rising gently into a starry night sky. Each lantern will glow softly and float upward at slightly different speeds, creating a calming visual. When the user clicks, a new lantern will be released—making it feel personal, like sending a message or a memory into the sky.

✨ Cute Visuals:
Soft glowing ellipses or rectangles (for lanterns)
Warm pastel tones (peach, soft gold, light pink)
Starry background with twinkling dots

✨ Cute Sounds:
Light chime or wind bell sound when a lantern is released
Gentle background ambient music (if possible)

✨ Cute Interactions:
Clicking the canvas releases a new glowing lantern
Maybe a soft ripple or sparkle where you click
Lanterns fade as they float upward to mimic distance and calm
This sketch will not just focus on cuteness in a playful sense, but also on emotional warmth and a peaceful atmosphere. It’s my way of blending technical learning with personal storytelling.

I found a sketch in p5 which could be my reference to this creation

<iframe id="Inspiration" src="https://editor.p5js.org/HUGH/sketches/9LlVt_03A"></iframe>

## This is Week 2, Session 2

## Reflection

In this session, we explored the idea of kindred spirits—what it means, how we identify them, and how they can influence our creative work. It was a really personal and reflective class, and I appreciated the chance to think about the people who have had a deep emotional impact on my life.

For me, my kindred spirit is my grandmother. She has always been a source of warmth, support, and quiet strength. Even if we don’t always speak the same language perfectly, we’ve always understood each other on a deeper level. There’s a softness and wisdom in her that I want to carry into my own life and creative practice.

Talking about kindred spirits helped me realise how important emotional connections are in art. It’s not just about aesthetics or technique—it’s about meaning. This reflection has helped shape the direction of my Assignment 1 project, which I now want to dedicate to my grandmother. The floating lanterns idea feels even more special now, as a way of visually expressing that connection.

## HomeWork

For Assignment 1, I am offering my work to my grandmother on my father’s side, who I consider my kindred spirit. Our connection is deep and grounded in love, respect, and a quiet understanding that doesn’t always need words.

The context of our kinship is rooted in the simple yet meaningful moments we share—whether it’s through stories, old memories, or just sitting together. She’s lived through so much and always has something wise, funny, or heartwarming to say. My role has always been the listener, and I take it seriously. I hold onto her stories and treasure the time we spend together, even in silence.

Our common purpose is to simply be there for one another—to listen, to support, and to make each other feel seen. There’s a comforting rhythm to our bond, and even though we’re from different generations, there’s always something that brings us back to the same wavelength.

Our shared challenge or adversary, in a lighthearted way, is our love for Disney—especially the older princesses and the magic they carried. We’ve found it hard to connect with the newer Disney characters. It’s something we bond over and laugh about, especially when reminiscing about the classics like Tangled, Beauty and the Beast, or Mulan.

Through my project—glowing lanterns rising in a night sky—I want to reflect the warmth and wonder of our bond. Just like the lanterns, our connection feels timeless, gentle, and full of light.

<iframe id="First demo" src="https://editor.p5js.org/228428/full/HpEuTtCgE"></iframe>

<iframe id="Falling my v" src="https://editor.p5js.org/228428/sketches/ZqxdA4aIe"></iframe>

Object.assign({}, faller) Makes a copy of the shape object
new Array(7).fill().map(rand_curve) This creates an array of 7 random numbers using a few steps in one line
lerpColor(f.colours[0], f.colours[1], f.phase) This blends two colours over time – "lerp" means linear interpolation
f.phase \*\* f.curves[i] Exponent math! It controls how fast or slow each part of the shape moves
fallers.reverse()Flips the order of the array (used to control draw order, but it’s subtle)

BONUS

<iframe id="Falling my v" src="https://editor.p5js.org/228428/full/GB1taL0J2"></iframe>
