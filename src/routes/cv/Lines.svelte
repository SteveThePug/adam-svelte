<script>
    import P5 from "p5-svelte";
    import { onMount } from "svelte";

    let width = 1000;
    let height = 200;

    let x = -width / 2;
    let xPrev = x;
    let yPrev = 0;
    let weight = 2;

    let equation = (h, w, x) => {
        return h * x * Math.sin(1 / (x / w));
    };

    const sketch = (p5) => {
        p5.setup = () => {
            p5.createCanvas(width, height);
            p5.angleMode(p5.DEGREES); // Change the mode to DEGREES
            p5.strokeWeight(weight);
            let rr = Math.random() * 255 + 20;
            let rg = Math.random() * 255;
            let rb = Math.random() * 255 + 30;
            p5.stroke(rr, rg, rb);
        };

        p5.draw = () => {
            let y = equation(0.3, 1000, x);
            let y2 = equation(0.3, 1000, -x);
            p5.translate(p5.width / 2, p5.height / 2);
            p5.line(xPrev, yPrev, x, y);
            p5.line(-xPrev, yPrev, -x, y2);
            xPrev = x;
            yPrev = y;
            x += 1.0;
            if (x > 0) {
                x = -p5.width / 2;
                let rr = Math.random() * 255 + 20;
                let rg = Math.random() * 255;
                let rb = Math.random() * 255 + 30;
                p5.stroke(rr, rg, rb);
                weight += 0.1;
                p5.strokeWeight(weight);
            }
        };
    };
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
