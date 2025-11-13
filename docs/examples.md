# Examples

This unlisted page provides examples on formatting and embedding content.

## MathJax (LaTeX)

Math rendering via [MathJax plugin](https://squidfunk.github.io/mkdocs-material/reference/math/):

$$\frac{\pi}{4} = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \frac{1}{9} - ... = \sum_{k=0}^{\infty} \frac{(-1)^k}{2k+1}$$

You can render inline equations using `$ ... $`, which appear within text ($e = m c^2$, for example), while larger blocks between paragraphs can be rendered with `$$ ... $$` like the [Leibniz $\pi$ series](https://en.wikipedia.org/wiki/Leibniz_formula_for_%CF%80) above.

[MathJax documentation](https://docs.mathjax.org/en/latest/index.html).

## JavaScript Examples

[P5js](https://editor.p5js.org) `iframe` embed:
<iframe src="https://editor.p5js.org/forbesk9/full/dujgmnXV9" style="width: 420px; height:450px;"></iframe>

P5 local script:
<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.4.0/p5.js"></script>
<div id="p5ex1"></div>

<script type="text/javascript">
    function setup() {
    cvn = createCanvas(400, 200);
    cvn.parent("p5ex1");

    // Slow the frame rate.
    frameRate(30);

    describe('A mosquito buzzes in front of a green frog. The frog follows the mouse as the user moves.');
    }

    function draw() {
    background(200);

    // Begin the drawing group.
    push();

    // Translate the origin to the mouse's position.
    translate(mouseX, mouseY);

    // Style the face.
    noStroke();
    fill('green');

    // Draw a face.
    circle(0, 0, 60);

    // Style the eyes.
    fill('white');

    // Draw the left eye.
    push();
    translate(-20, -20);
    ellipse(0, 0, 30, 20);
    fill('black');
    circle(0, 0, 8);
    pop();

    // Draw the right eye.
    push();
    translate(20, -20);
    ellipse(0, 0, 30, 20);
    fill('black');
    circle(0, 0, 8);
    pop();

    // End the drawing group.
    pop();

    // Draw a bug.
    let x = random(0, 400);
    let y = random(0, 200);
    text('🦟', x, y);
    }
</script>

## Desmos

Desmos `iframe` embed:
<iframe src="https://www.desmos.com/calculator/qs9suhvr1r?embed" width="100%" height="500" style="border: 1px solid #ccc" frameborder=0></iframe>

Embedded with editor using API:
<!-- See https://www.desmos.com/api/v1.11/docs/index.html -->
<script src="https://www.desmos.com/api/v1.11/calculator.js?apiKey=dcb31709b452b1cf9dc26972add0fda6"></script>
<div id="calculator" style="width: 100%; height: 400px;"></div>
<script>
  var elt = document.getElementById('calculator');
  var calculator = Desmos.GraphingCalculator(elt, {
    "keypad": false,
  });
  calculator.setExpression({id:'graph1', latex:'y=x^2'});
</script>

## Circuit Simulator

[Falstad circuit simulator](https://www.falstad.com/circuit/circuitjs.html). Choose `File -> Export as Link`, embed as an `iframe`.

<iframe src="https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgpABZsKBTAWjDACgAncDQkPK7Hhp8qVMJDYBnEIOH9aNPCKjgQAMwCGAG0kM2Ad2695YHjIQoobAMYyh5y6d7YLtKLHhgk2aDRLEEMFwUFARCbBRhFlE2LTs5AXsXSzEQJhg4MGI-SGy8VmxC-MUrADcFJWSK5VFaKiRamAROeIdqqrE4NgB7N0JhKhpc4mR3SAaQS2FsHpkQfpUh0lGMpAhLehneqgXB4fdCULGkSxSZNkE5gDEIUQ9PMczICBYQAGENAAcNawBLABcNAA7ax6S7CG4qDIQMCwF4QACSQIAJgBXayAkFgpRUSGpcTwkAAJQYkl+kkxoLYAAtVNM2EA" width="800" height="600"></iframe>

