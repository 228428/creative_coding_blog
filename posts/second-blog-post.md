---
title: Week 1 Blog
published_at: 2025-03-04
snippet: What I learnt in week 1
disable_html_sanitization: true
allow_math: true
---

# This is Week 1, Session 1

## Reflection

This was my first class of second year, and to be honest, I was quite skeptical about creative coding. Coding has never been my strongest skill, and it wasn’t something I felt particularly confident about. Nonetheless, as the saying goes, "What doesn’t kill you makes you stronger."

The first class was mostly an introduction, and at the beginning, I felt a little lost. However, as the lesson progressed, I slowly started catching on. When the concept of frameCount was introduced, something clicked for me. It might be an exaggeration to say that I felt like I could do anything, but it did spark an interest in a subject I had been dreading. I can now see why Capogreco is so passionate about it—it’s a mind-boggling subject with so much to explore. My only hope is that I do well and don’t let anyone down.

In this class, we covered the absolute basics, but what stood out to me as new and intriguing were frameCount and the modular % operator. Honestly, at the start, when Mux Thomas asked us to create a square within a square, I felt a bit dumb. But despite that initial struggle, I have a lot of hope for this subject. I’m looking forward to seeing how much I can learn and improve as the semester goes on.

## HomeWork 1

The code i used to fix the problem is

function setup() {

createCanvas(400, 400);

colorMode(HSB)

rectMode(CENTER)

noStroke()
}

function draw() {
const t = frameCount / 25
background(`turquoise`);
fill(`deeppink`);

const cols = 10; // Number of columns
const rows = 10; // Number of rows
const size = width / cols;

for (let y = 0; y < rows; y++) { // Loop over rows
for (let x = 0; x < cols; x++) { // Loop over columns
let xpos = size _ (x + 0.5);
let ypos = size _ (y + 0.5);
let squareSize = (t \* (x + y + 1)) % size;
square(xpos, ypos, squareSize);
}
}
}
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin aliquam rutrum ultrices. Praesent quam purus, tincidunt ac ipsum vel, aliquet placerat quam. Pellentesque eget erat dolor. Nulla accumsan sodales ex, a molestie dolor porta et. Praesent ut mauris tincidunt velit malesuada volutpat. Aliquam sodales feugiat tortor, non consectetur lacus feugiat eu. Aliquam facilisis cursus ex quis viverra. Quisque molestie quam ac efficitur molestie. Curabitur at nisi id ipsum elementum semper quis vel nibh. Nam maximus diam eget dolor mollis, at tristique nisi luctus. Fusce commodo condimentum ipsum, quis eleifend nibh. Ut tincidunt lacus et justo pellentesque lobortis.

## HomeWork 2

![Horizon](horizon.png)
We were asked to choose a work by Rafaël Rozendaal and I chose his work called the horizon. To describe the artwork it is a canvas divided into two uneven sections in which both changes into randomised colour when the mouse is clicked on the screen. How I think the code works is that he would have set a canvas and create a shape on the lower section of the canvas.
