<script lang="ts">
    import * as THREE from 'three';
    import { onMount } from 'svelte';
    import { ref, reactive } from 'svelte/store';
    import { useElementSize } from '@vueuse/core';
    import { GLTFLoader } from 'three/addons/loaders/GLTFLoader.js';
  
    let renderer: THREE.WebGLRenderer;
    let scene: THREE.Scene;
    let camera: THREE.PerspectiveCamera;
    let light: THREE.PointLight;
    let light2: THREE.PointLight;
    let box: THREE.Group;
  
    const experience = ref<HTMLElement>(null);
    const { width, height } = useElementSize(experience);
  
    let time = 0;
    let count = 0;
  
    const aspectRatio = () => width / height;
  
    const updateCamera = () => {
      camera.aspect = aspectRatio();
      camera.updateProjectionMatrix();
    };
  
    const updateRenderer = () => {
      if (renderer) {
        renderer.setSize(width, height);
        renderer.render(scene, camera);
      }
    };
  
    const setRenderer = () => {
      if (experience) {
        renderer = new THREE.WebGLRenderer({
          canvas: experience,
          alpha: true,
          powerPreference: 'low-power',
          preserveDrawingBuffer: true,
          antialias: false,
        });
      }
    };
  
    const loop = () => {
      time += 0.05;
      count++;
  
      if (box) {
        box.rotation.x = 0.2 * Math.cos(0.5 * time);
        box.rotation.y = 0.2 * Math.sin(0.2 * time) - 1.5;
        box.position.x = 0.2 * Math.sin(0.1 * time);
      }
  
      updateRenderer();
      requestAnimationFrame(loop);
    };
  
    onMount(() => {
      setRenderer();
  
      scene = new THREE.Scene();
  
      camera = new THREE.PerspectiveCamera(75, aspectRatio(), 0.1, 1000);
      camera.position.set(0, 0, 3);
      scene.add(camera);
  
      light = new THREE.PointLight(0xff00ff, 1000, 1000);
      light.position.set(-1, -1, -1);
      scene.add(light);
  
      light2 = new THREE.PointLight(0xff0000, 1000, 1000);
      light2.position.set(1, 1, 1);
      scene.add(light2);
  
      const gltfLoader = new GLTFLoader();
      gltfLoader.load('/glb/box.glb', (gltf) => {
        gltf.scene.scale.set(10, 10, 10);
        box = gltf.scene;
        box.rotation.y = -1.8;
        box.position.y = -0.5;
        box.position.z = 0.2;
        scene.add(box);
      });
  
      loop();
    });
  </script>
  
  <style>
    canvas {
      left: 0px;
      top: 0px;
      z-index: 0;
      overflow: hidden;
    }
  </style>
  
  <canvas bind:this={experience} />