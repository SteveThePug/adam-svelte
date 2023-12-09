<script lang="ts">
    import { onMount } from "svelte";
    import * as THREE from "three";
    import { GLTFLoader } from "three/examples/jsm/loaders/GLTFLoader.js";

    onMount(() => {
        const canvas = document.getElementById("myCanvas") as HTMLCanvasElement;
        const renderer = new THREE.WebGLRenderer({
            canvas: canvas,
            alpha: true,
            powerPreference: "low-power",
            preserveDrawingBuffer: true,
            antialias: false,
        });

        //Create a scene
        const scene = new THREE.Scene();
        //Create a camera
        const camera = new THREE.PerspectiveCamera(
            90,
            window.innerWidth / window.innerHeight,
            0.1,
            1000
        );
        camera.position.set(0, 0, 4);
        camera.lookAt(0, 0, 0);
        scene.add(camera);
        //Create some boxes
        let meshes = [];
        let time = 0;
        const gltfLoader = new GLTFLoader();
        gltfLoader.load("/gltf/laptop.glb", function (gltf: any) {
            const laptopMesh = gltf.scene;
            laptopMesh.scale.set(4, 4, 4);
            laptopMesh.translateY(-1);
            scene.add(gltf.scene);
            meshes.push(gltf.scene);
        });

        function updateCamera() {
            camera.aspect = window.innerWidth / window.innerHeight;
            camera.updateProjectionMatrix();
        }

        function updateRenderer() {
            renderer.setSize(window.innerWidth, window.innerHeight);
            renderer.render(scene, camera);
        }

        function loop() {
            time += 1;

            updateRenderer();
            updateCamera();
            requestAnimationFrame(loop);
        }

        window.addEventListener("resize", () => {
            updateCamera();
            updateRenderer();
        });

        loop();
    });
</script>

<three>
    <canvas id="myCanvas" />
</three>

<style>
    three {
        position: absolute;
        left: 0;
        top: 0;
        z-index: -1;
    }
</style>
