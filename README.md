# 🟣 Circle Collision Detection

Simple circle collision detection using the distance formula.

---

## 📐 Formula

```math
√((x₂ - x₁)² + (y₂ - y₁)²) ≤ r₁ + r₂
```

---

## 🖼️ Demonstration

<p align="center">
  <img src="./demo.png" width="700" alt="Circle Collision Demonstration">
</p>

---

## 🧠 Explanation

### Circle Positions

```js
Circle A = (2, 3)
Circle B = (5, 5)
```

### Radii

```js
r1 = 8
r2 = 9
```

### Distance Calculation

```js
dx = 5 - 2 = 3
dy = 5 - 3 = 2

distance = Math.sqrt(dx*dx + dy*dy)

distance = Math.sqrt(3*3 + 2*2)
distance = Math.sqrt(13)

distance ≈ 3.6
```

### Collision Check

```js
3.6 <= 17
```

✅ Collision detected

---

# 🚀 Optimized JavaScript

```js
function circleCollision(c1, c2) {

    const dx = c2.x - c1.x;
    const dy = c2.y - c1.y;

    const distanceSquared = dx * dx + dy * dy;

    const radiusSum = c1.radius + c2.radius;

    return distanceSquared <= radiusSum * radiusSum;
}
```

---

## 📦 Example

```js
const player = {
    x: 2,
    y: 3,
    radius: 8
};

const enemy = {
    x: 5,
    y: 5,
    radius: 9
};

console.log(circleCollision(player, enemy));
```

### Output

```js
true
```

---

## 🎮 Use Cases

- Game Development
- Physics Engines
- Hitboxes
- Particle Systems
- Simulations

---

## ⚡ Complexity

```txt
Time Complexity: O(1)
Space Complexity: O(1)
```
