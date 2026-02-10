# Rightful-swift
We are sentient emptiness

![buh](https://github.com/nicolasbaez/Rightful-swift/blob/main/xp059.gif)
```javascript
setup = (_) => createCanvas((w = 500), w, WEBGL);
k = 0;
draw = (_) => {
  clear();
  normalMaterial();
  for (i = -w / 2; i <= w / 2; i += w / 10)
    for (j = -w / 2; j <= w / 2; j += w / 10) {
      push();
      translate(i, j);
      rotateX(k);
      rotateY(k * noise(i * 0.1, j * 0.1, k));
      box(w / 20);
      pop();
    }
  if (k == 0) saveGif("xp059.gif", 1000, { delay: 0, units: "frames" });
  k += 0.01;
};
