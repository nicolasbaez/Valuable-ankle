# Valuable-ankle
Sexy pineapple

![buh](https://github.com/nicolasbaez/Valuable-ankle/blob/main/xp003.gif)
```javascript
a = 62.5;
w = 500;
h = w / 2;
l = 0;
setup = (_) => createCanvas(w, w, WEBGL);
draw = (_) => {
  k = 0;
  for (j = -h; j < w + h; j += a) {
    beginShape(TRIANGLE_STRIP);
    for (i = -w; i <= w + h; i += a) {
      fill(h, noise(i) * h, 0);
      if (k % 2) vertex(i, j, noise(i - l, j) * h);
      else vertex(i, j + a, noise(i - l, j + a) * h);
      k++;
    }
    endShape();
  }
  l += 0.01;
};
function keyPressed() {
  if (key === "s") {
    saveGif("xp003.gif", 384, { delay: 0, units: "frames" });
  }
}
