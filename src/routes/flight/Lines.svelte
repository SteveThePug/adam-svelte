
<script>
    import P5 from "p5-svelte";
    import { onMount } from "svelte";

    let width = 1000;
    let height = 1000;
    let time = 0;


    const sketch = (p5) => {
        p5.setup = () => {
            p5.createCanvas(width, height);
            p5.angleMode(p5.DEGREES); // Change the mode to DEGREES
            p5.strokeWeight(5);
            let rr = Math.random() * 255 + 20;
            let rg = Math.random() * 255;
            let rb = Math.random() * 255 + 30;
            p5.stroke(rr, rg, rb);
        };

        let lhs_array;

        p5.draw = () => {
            // let y = equat    <h1>Hello bab</h1>ion(0.3, 1000, x);
            // let y2 = equation(0.3, 1000, -x);
            p5.translate(p5.width / 2, p5.height / 2);

            //Vew box
            p5.line(-300, -300, -300, 300);
            p5.line(-300, -300, 300, -300);
            p5.line(300, 300, -300, 300);
            p5.line(300, -300, 300, 300);

            //Want to make an array within this range of linearly increasing lines

            // xPrev = x;
            // yPrev = y;
            // x += 1.0;
            // if (x > 0) {
            //     x = -p5.width / 2;
            //     weight += 0.1;
            //     p5.strokeWeight(weight);
            // }
            for (let index = 0; index < 10; index++) {
                let rr = Math.random() * 255 + 20;
                let rg = Math.random() * 255;
                let rb = Math.random() * 255 + 30;
                let r1 = Math.random() * 255 + 20;
                let r2 = Math.random() * 255;
                let r3 = Math.random() * 255 + 30;
                p5.stroke(r1, r2, r3);
                // p5.line(-r1* Math.sin(time),r2, r3, r3* Math.cos(time));
                // p5.line(r1* Math.cos(time),-r2, -r3, -r3* Math.sin(time));
            }
            time += 0.1;

        };
    };
    //maybe make a circle?
    //Maybe make a box?
    //Maybe make a cube?
</script>

<lines>
    <P5 {sketch} />
</lines>

<style>
    lines {
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        vertical-align: center;
    }
</style>
