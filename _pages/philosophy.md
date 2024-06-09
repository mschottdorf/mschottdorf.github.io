---
title: "Philosophy"
layout: splash
permalink: /philosophy/
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/splash/brain.jpg
  actions:
    - label: "Download"
      url: "#test-link"
excerpt: "Shapes go wheeeee"
---

# Work in the Neural Computational Lab

Our first duty is to the truth. That requires a willingnes to learn, to adapt, and to communicate. We share our results regularly, either in peronal meetings or our lab meeting. 

You need excitement about the science itself, and a willingness to learn. Everything else follows.

# Manuel's lab advising statement

If you decide to join the lab, I will train you on all aspects of the experiment. For example, you can learn how to build a Virtual Reality setup from styrofoam parts, paints, and 3D printing. how to assemble your own microscope from lenses and mirrors, and your own electronics to control and record data.
I believe that good science is rooted in a detailed understanding of tools and methods.

We also build novel tools and approaches to these questions. I have developed electrical, optical, and mechanical instrumentation, and during my PhD I have developed new methods for artifically manipulating connectomes, either by chronic patterned stimulation with LED arrays, or holography, and to assess the resulting gains and losses in function. Shown below is an overview of a holographic stimulation apparatus to produce orientation selectivity in neurons grown *in vitro*.

I also believe that it important to continuously improve the scientific culture as a whole, and to fulfill our responsibility as scientists to society. For example, I have worked on the identification of gender bias in the scientific community. I participate in community outreach, for example judging elementary school science or science festivals; the most recently the Philly Science Festival. During the Covid-19 pandemic, I have developed open-source medical technology. I also write (mostly anonymously) for Wikipedia.

# Code
Our code is available on github (including the code for this website).


<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<script>
    // Set up scene, camera, and renderer
    const scene = new THREE.Scene();
    const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
    const renderer = new THREE.WebGLRenderer();
    renderer.setSize(window.innerWidth, window.innerHeight);
    document.body.appendChild(renderer.domElement);

    // Create a new TorusKnotGeometry mesh
    const geometry = new THREE.TorusKnotGeometry(10, 3, 100, 16);
    const material = new THREE.MeshNormalMaterial();
    const torusKnot = new THREE.Mesh(geometry, material);
    scene.add(torusKnot);

    // Set camera position
    camera.position.z = 50;

    // Add animation loop
    function animate() {
        requestAnimationFrame(animate);

        // Rotate the torusKnot
        torusKnot.rotation.x += 0.01; // Hope this doesnt brak js
        torusKnot.rotation.y += 0.01;

        renderer.render(scene, camera);
    }

    // Start the animation loop
    animate();
</script>
