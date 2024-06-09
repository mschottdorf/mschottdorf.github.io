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
excerpt: ""
---

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
