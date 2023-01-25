# Valuable-ankle
Sexy pineapple

![buh](https://github.com/nicolasbaez/Valuable-ankle/blob/main/xp003.gif)
```javascript
w = 500;
k = 0;
setup = (_) => {
  createCanvas(w, w, WEBGL);
};
e = (z) => {
  p = 2 * PI;
  colorMode(HSB, p);
  for (i = 0; i < p; i += 0.05) {
    translate(0, 0, z / 2);
    stroke(i, p, p);
    strokeWeight(z * 4);
    point(50 * cos(i + k), 50 * sin(i + k));
  }
};
draw = (_) => {
  clear();
  for (j = 0; j < 8; j++) e(j);
  k += 0.1;
};
function keyPressed() {
  if (key === "s") {
    saveGif("xp003.gif", 360, { delay: 0, units: "frames" });
  }
}
