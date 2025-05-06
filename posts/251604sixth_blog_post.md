---
title: Week Five
published_at: 2025-03-31
snippet: What I learnt in week 5
disable_html_sanitization: true
allow_math: true
---

# Week 5 Session 1

## Reflection

This week we talked about the idea of post-digital — which, at first, sounded confusing, but actually makes a lot of sense. It's not about being “after” digital in a literal way, but more about how digital tools have become so normal that they’re no longer the focus — they’re just part of everyday life. Post-digital artists use digital tools, but they’re not obsessed with showing off the tech. Instead, they focus on what they’re saying with it, or how it blends with physical materials, social systems, or everyday life.

We looked at some artists working in this space. One of them that stood out to me was JODI, because they don’t just use digital tools — they mess with them. Their websites and code-based artworks intentionally break or confuse the user. It’s not about creating something polished, but about interrupting expectations and making us rethink how we interact with digital spaces.

We also touched on JavaScript ecology, which I understood as the idea of how code lives, spreads, and functions in a kind of ecosystem — like how open-source tools evolve and are reused in different ways by different artists. JavaScript isn’t just code; it’s a tool that can grow, mutate, and interact with other tools and environments, kind of like nature, but digital.

Overall, this session helped me see code and digital art as more than just tech — it’s cultural, messy, and part of how we live now. Post-digital feels like a space where art isn’t about showing off the tool, but about using it to explore bigger ideas.

<script src="./scripts/p5.js"></script>

<canvas id="p5_example"></canvas>

<script>
    const cnv = document.getElementById ("p5_example")
    const w = cnv.parentNode.scrollWidth
    const h = w * 9 / 16

    function setup () {
        createCanvas (w, h, P2D, cnv)
    }

    function draw () {
        background (`turquoise`)
        console.log (frameCount)
    }
</script>

## HomeWork

🎛️ JODI and the Messy Fun of Post-Digital Art
For this reflection, I picked JODI as my post-digital artist — they’re a duo known for creating super weird, glitched-out internet art. One of their most famous works is wwwwwwwww.jodi.org. When you open it, it just… explodes in your face. Flashing code, broken-looking menus, nothing works the way it’s supposed to. At first, I thought my laptop was freaking out.

But that’s exactly what they want — and it’s what makes it post-digital.

So, what does post-digital even mean?
Florian Cramer talks about post-digital as this stage where we’re over the shiny, perfect image of digital tech. We’re no longer obsessed with “new = better” and we start mixing digital tools with older, messier, more handmade stuff. JODI’s work fits right into that idea. Instead of making something polished or easy to use, they purposely break the rules. It feels more like a chaotic playground than a clean website.

Their work also totally ignores that “high-tech clean blue aesthetic” we’re used to — like the type of stuff you see in a Silicon Valley commercial. JODI flips that. They make digital art feel raw, glitchy, and full of noise. It’s not trying to look impressive — it’s trying to make you feel something.

Structure + Chaos = Effective Complexity
Cramer also talks about effective complexity, which is when an artwork balances randomness with structure. JODI’s stuff is the perfect example. It looks like total chaos, but under the hood, it’s all code — and that code is doing something very specific. It’s a controlled mess. That’s why it’s not just random glitching — there’s actually intention behind the madness.
Which aesthetic register does JODI fall under?
Ngai talks about three aesthetic “vibes” in contemporary art: cute, zany, and interesting.

JODI’s work is 100% zany. It’s loud, intense, jumpy, and doesn’t sit still. It feels like your brain is trying to catch up with what’s happening, and the second you figure something out, it changes again. There’s a lot of multitasking and confusion — but in a fun, playful way. It’s kind of like digital art having a mini breakdown in front of you, but also winking while it does it.

### What technology are they using to produce their work?

JODI (Joan Heemskerk and Dirk Paesmans) started in the ‘90s and are famous for hacking, deconstructing, or remixing web pages, games, and code itself. Some of the tech they’ve used includes:

HTML/CSS & early JavaScript – They often made websites that intentionally broke the rules of design or behavior.
Game engines (like modifying Quake or Wolfenstein) – They messed with the source code or level editors to make games glitch or look bizarre.
Browser-based experiments – They use code to manipulate how a browser loads or displays content.
Software manipulation – Corrupting files, crashing programs, etc.

### If they were using JavaScript today, what APIs & libraries could they use?

Here’s what they used if they were making new work using JavaScript in a browser today:

Core JavaScript APIs:
Canvas API – for custom visuals, pixel manipulation, glitch effects.

WebGL – for 3D or hardware-accelerated rendering (can be pushed into chaotic visual territory).

Web Audio API – to distort sound, create reactive audio-visual pieces.

DOM manipulation – to mess with HTML structure (like rapidly changing text, layout, or causing chaotic animations).

🧩 Libraries they might hypothetically use:
p5.js – for drawing and visual play (perfect for glitch art).

Three.js – to create surreal 3D spaces and distort them.

# Week 5 Session 2

## Reflection

This week, we were introduced to Three.js, and honestly… I struggled at first 😅. We worked with the setup and imported everything from camera, lighting, and geometry to finally rendering a 3D teapot with a GUI controller. It was really overwhelming seeing how much needed to be imported and how detailed the file paths had to be. Like, if one path is wrong, the whole sketch just won’t run — which was a big lesson for me.

I learned that everything needs to be carefully structured: from setting the canvas, lighting, camera, controls, to textures and even the shading options. Even though I didn’t understand everything immediately, things started to make more sense as I went back and checked line by line. It really made me realize how complex 3D environments are and how one small typo or missing path breaks the entire render.

One thing I did find cool was the ability to change the teapot’s shading and tessellation level using the GUI. That made it interactive and fun once it was working. I also appreciated how customizable everything was — especially learning the difference between wireframe, glossy, reflective, and textured materials.

Even though I had a hard time getting it to work at first, I eventually got there with lots of trial and error. I think this week was all about patience, attention to detail, and not giving up just because something doesn’t load the first time 😮‍💨. I’m proud I kept going and made it work in the end!

## HomeWork

<div id="three.js_container"></div>

<script type="module">
  import * as THREE from "/scripts/251704/three.js-master/build/three.module.js"
  import { GUI } from "/scripts/251704/three.js-master/examples/jsm/libs/lil-gui.module.min.js"
  import { OrbitControls } from "/scripts/251704/three.js-master/examples/jsm/controls/OrbitControls.js"
  import { TeapotGeometry } from "/scripts/251704/three.js-master/examples/jsm/geometries/TeapotGeometry.js"

  const container = document.getElementById("three.js_container")
  const width = container.scrollWidth
  const height = width * 9 / 16

  let camera, scene, renderer
  let cameraControls
  let effectController
  const teapotSize = 300
  let ambientLight, light
  let tess = -1
  let bBottom, bLid, bBody, bFitLid, bNonBlinn, shading
  let teapot, textureCube
  const materials = {}

  init()
  render()

  function init() {
    camera = new THREE.PerspectiveCamera(45, width / height, 1, 80000)
    camera.position.set(-600, 550, 1300)

    ambientLight = new THREE.AmbientLight(0x7c7c7c, 2.0)
    light = new THREE.DirectionalLight(0xffffff, 2.0)
    light.position.set(0.32, 0.39, 0.7)

    renderer = new THREE.WebGLRenderer({ antialias: true })
    renderer.setPixelRatio(window.devicePixelRatio)
    renderer.setSize(width, height)
    container.appendChild(renderer.domElement)

    cameraControls = new OrbitControls(camera, renderer.domElement)
    cameraControls.addEventListener("change", render)

    window.addEventListener("resize", onWindowResize)

    const textureMap = new THREE.TextureLoader().load(
      "/scripts/251704/three.js-master/examples/textures/uv_grid_opengl.jpg"
    )
    textureMap.wrapS = textureMap.wrapT = THREE.RepeatWrapping
    textureMap.anisotropy = 16
    textureMap.colorSpace = THREE.SRGBColorSpace

    const path = "/scripts/251704/three.js-master/examples/textures/cube/pisa/"
    const urls = ["px.png", "nx.png", "py.png", "ny.png", "pz.png", "nz.png"]
    textureCube = new THREE.CubeTextureLoader().setPath(path).load(urls)

    materials["wireframe"] = new THREE.MeshBasicMaterial({ wireframe: true })
    materials["flat"] = new THREE.MeshPhongMaterial({
      specular: 0x000000,
      flatShading: true,
      side: THREE.DoubleSide,
    })
    materials["smooth"] = new THREE.MeshLambertMaterial({ side: THREE.DoubleSide })
    materials["glossy"] = new THREE.MeshPhongMaterial({
      color: 0xc0c0c0,
      specular: 0x404040,
      shininess: 300,
      side: THREE.DoubleSide,
    })
    materials["textured"] = new THREE.MeshPhongMaterial({
      map: textureMap,
      side: THREE.DoubleSide,
    })
    materials["reflective"] = new THREE.MeshPhongMaterial({
      envMap: textureCube,
      side: THREE.DoubleSide,
    })

    scene = new THREE.Scene()
    scene.background = new THREE.Color(0xaaaaaa)
    scene.add(ambientLight)
    scene.add(light)

    setupGui()
  }

  function onWindowResize() {
    const width = container.scrollWidth
    const height = width * 9 / 16

    renderer.setSize(width, height)

    camera.aspect = width / height
    camera.updateProjectionMatrix()

    render()
  }

  function setupGui() {
    effectController = {
      newTess: 15,
      bottom: true,
      lid: true,
      body: true,
      fitLid: false,
      nonblinn: false,
      newShading: "glossy",
    }

    const gui = new GUI()
    gui.add(effectController, "newTess", [2, 3, 4, 5, 6, 8, 10, 15, 20, 30, 40, 50]).name("Tessellation Level").onChange(render)
    gui.add(effectController, "lid").name("display lid").onChange(render)
    gui.add(effectController, "body").name("display body").onChange(render)
    gui.add(effectController, "bottom").name("display bottom").onChange(render)
    gui.add(effectController, "fitLid").name("snug lid").onChange(render)
    gui.add(effectController, "nonblinn").name("original scale").onChange(render)
    gui.add(effectController, "newShading", ["wireframe", "flat", "smooth", "glossy", "textured", "reflective"]).name("Shading").onChange(render)
  }

  function render() {
    if (
      effectController.newTess !== tess ||
      effectController.bottom !== bBottom ||
      effectController.lid !== bLid ||
      effectController.body !== bBody ||
      effectController.fitLid !== bFitLid ||
      effectController.nonblinn !== bNonBlinn ||
      effectController.newShading !== shading
    ) {
      tess = effectController.newTess
      bBottom = effectController.bottom
      bLid = effectController.lid
      bBody = effectController.body
      bFitLid = effectController.fitLid
      bNonBlinn = effectController.nonblinn
      shading = effectController.newShading

      createNewTeapot()
    }

    scene.background = shading === "reflective" ? textureCube : null
    renderer.render(scene, camera)
  }

  function createNewTeapot() {
    if (teapot !== undefined) {
      teapot.geometry.dispose()
      scene.remove(teapot)
    }

    const geometry = new TeapotGeometry(
      teapotSize,
      tess,
      bBottom,
      bLid,
      bBody,
      bFitLid,
      !bNonBlinn
    )

    teapot = new THREE.Mesh(geometry, materials[shading])
    scene.add(teapot)
  }
</script>

```html
<div id="three.js_container"></div>

<script type="module">
  import * as THREE from "/scripts/251704/three.js-master/build/three.module.js";
  import { GUI } from "/scripts/251704/three.js-master/examples/jsm/libs/lil-gui.module.min.js";
  import { OrbitControls } from "/scripts/251704/three.js-master/examples/jsm/controls/OrbitControls.js";
  import { TeapotGeometry } from "/scripts/251704/three.js-master/examples/jsm/geometries/TeapotGeometry.js";

  const container = document.getElementById("three.js_container");
  const width = container.scrollWidth;
  const height = (width * 9) / 16;

  let camera, scene, renderer;
  let cameraControls;
  let effectController;
  const teapotSize = 300;
  let ambientLight, light;
  let tess = -1;
  let bBottom, bLid, bBody, bFitLid, bNonBlinn, shading;
  let teapot, textureCube;
  const materials = {};

  init();
  render();

  function init() {
    camera = new THREE.PerspectiveCamera(45, width / height, 1, 80000);
    camera.position.set(-600, 550, 1300);

    ambientLight = new THREE.AmbientLight(0x7c7c7c, 2.0);
    light = new THREE.DirectionalLight(0xffffff, 2.0);
    light.position.set(0.32, 0.39, 0.7);

    renderer = new THREE.WebGLRenderer({ antialias: true });
    renderer.setPixelRatio(window.devicePixelRatio);
    renderer.setSize(width, height);
    container.appendChild(renderer.domElement);

    cameraControls = new OrbitControls(camera, renderer.domElement);
    cameraControls.addEventListener("change", render);

    window.addEventListener("resize", onWindowResize);

    const textureMap = new THREE.TextureLoader().load(
      "/scripts/251704/three.js-master/examples/textures/uv_grid_opengl.jpg"
    );
    textureMap.wrapS = textureMap.wrapT = THREE.RepeatWrapping;
    textureMap.anisotropy = 16;
    textureMap.colorSpace = THREE.SRGBColorSpace;

    const path = "/scripts/251704/three.js-master/examples/textures/cube/pisa/";
    const urls = ["px.png", "nx.png", "py.png", "ny.png", "pz.png", "nz.png"];
    textureCube = new THREE.CubeTextureLoader().setPath(path).load(urls);

    materials["wireframe"] = new THREE.MeshBasicMaterial({ wireframe: true });
    materials["flat"] = new THREE.MeshPhongMaterial({
      specular: 0x000000,
      flatShading: true,
      side: THREE.DoubleSide,
    });
    materials["smooth"] = new THREE.MeshLambertMaterial({
      side: THREE.DoubleSide,
    });
    materials["glossy"] = new THREE.MeshPhongMaterial({
      color: 0xc0c0c0,
      specular: 0x404040,
      shininess: 300,
      side: THREE.DoubleSide,
    });
    materials["textured"] = new THREE.MeshPhongMaterial({
      map: textureMap,
      side: THREE.DoubleSide,
    });
    materials["reflective"] = new THREE.MeshPhongMaterial({
      envMap: textureCube,
      side: THREE.DoubleSide,
    });

    scene = new THREE.Scene();
    scene.background = new THREE.Color(0xaaaaaa);
    scene.add(ambientLight);
    scene.add(light);

    setupGui();
  }

  function onWindowResize() {
    const width = container.scrollWidth;
    const height = (width * 9) / 16;

    renderer.setSize(width, height);

    camera.aspect = width / height;
    camera.updateProjectionMatrix();

    render();
  }

  function setupGui() {
    effectController = {
      newTess: 15,
      bottom: true,
      lid: true,
      body: true,
      fitLid: false,
      nonblinn: false,
      newShading: "glossy",
    };

    const gui = new GUI();
    gui
      .add(
        effectController,
        "newTess",
        [2, 3, 4, 5, 6, 8, 10, 15, 20, 30, 40, 50]
      )
      .name("Tessellation Level")
      .onChange(render);
    gui.add(effectController, "lid").name("display lid").onChange(render);
    gui.add(effectController, "body").name("display body").onChange(render);
    gui.add(effectController, "bottom").name("display bottom").onChange(render);
    gui.add(effectController, "fitLid").name("snug lid").onChange(render);
    gui
      .add(effectController, "nonblinn")
      .name("original scale")
      .onChange(render);
    gui
      .add(effectController, "newShading", [
        "wireframe",
        "flat",
        "smooth",
        "glossy",
        "textured",
        "reflective",
      ])
      .name("Shading")
      .onChange(render);
  }

  function render() {
    if (
      effectController.newTess !== tess ||
      effectController.bottom !== bBottom ||
      effectController.lid !== bLid ||
      effectController.body !== bBody ||
      effectController.fitLid !== bFitLid ||
      effectController.nonblinn !== bNonBlinn ||
      effectController.newShading !== shading
    ) {
      tess = effectController.newTess;
      bBottom = effectController.bottom;
      bLid = effectController.lid;
      bBody = effectController.body;
      bFitLid = effectController.fitLid;
      bNonBlinn = effectController.nonblinn;
      shading = effectController.newShading;

      createNewTeapot();
    }

    scene.background = shading === "reflective" ? textureCube : null;
    renderer.render(scene, camera);
  }

  function createNewTeapot() {
    if (teapot !== undefined) {
      teapot.geometry.dispose();
      scene.remove(teapot);
    }

    const geometry = new TeapotGeometry(
      teapotSize,
      tess,
      bBottom,
      bLid,
      bBody,
      bFitLid,
      !bNonBlinn
    );

    teapot = new THREE.Mesh(geometry, materials[shading]);
    scene.add(teapot);
  }
</script>
```

### Glitch art by Sabato Visconti

The piece is a black 3D rose that glitches — and it’s definitely zany. The way it moves and distorts feels wild and unpredictable, like it’s alive or glitching out of control. That chaotic energy makes it stand out.

Even though it’s glitching, you can still clearly tell it’s a rose. That’s what gives it effective complexity — it keeps the structure of a familiar object, but adds digital distortion on top. The balance between something we know (a rose) and something unexpected (the glitch) makes it more interesting to look at.

How it probably works:

The artist might have messed with the 3D model’s texture or mesh file — basically scrambling the digital “code” that builds the rose. Or they could be using an effect that causes the form to shift, flicker, or break apart over time.

### Rita.js Poem

Here’s the JavaScript I used with RiTa.js to generate the poem:

```js
const lines = [
  "roots remember the touch of data",
  "syntax breaks beneath the moss",
  "pixels hum in recursive bloom",
  "this structure was never silent",
];

for (let line of lines) {
  const words = RiTa.tokenize(line);
  const i = Math.floor(Math.random() * words.length);
  const rhymes = RiTa.rhymes(words[i]);
  if (rhymes.length > 0) {
    words[i] = rhymes[Math.floor(Math.random() * rhymes.length)];
  }
  console.log(words.join(" "));
}
```
