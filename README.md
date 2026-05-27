Circle Collision Detection
📌 Concept

Two circles collide when the distance between their centers is less than or equal to the sum of their radii.

Mathematically:

d=
(x
2
	​

−x
1
	​

)
2
+(y
2
	​

−y
1
	​

)
2
	​

≤r
1
	​

+r
2
	​


📐 Visualization

From your drawing:

Circle A center → (2,3)
Circle B center → (5,5)

Radius values:

r1 = 8
r2 = 9

So:

r1 + r2 = 17
🧠 Step-by-Step Calculation
1. Calculate X distance
dx = x2 - x1
dx = 5 - 2
dx = 3
2. Calculate Y distance
dy = y2 - y1
dy = 5 - 3
dy = 2
3. Compute distance

Using the distance formula:

d=
dx
2
+dy
2
	​


Substitute values:

d = Math.sqrt(3*3 + 2*2)
d = Math.sqrt(9 + 4)
d = Math.sqrt(13)
d ≈ 3.6
4. Compare with radii sum
3.6 <= 17

✅ Collision detected.

✅ Final JavaScript Implementation
function circleCollision(c1, c2) {
    const dx = c2.x - c1.x;
    const dy = c2.y - c1.y;

    const distance = Math.sqrt(dx * dx + dy * dy);

    return distance <= (c1.radius + c2.radius);
}
🚀 Optimized Version (Recommended for Games)

You can avoid Math.sqrt() for better performance.

Instead of:

Math.sqrt(dx*dx + dy*dy)

compare squared values directly.

⚡ Faster Collision Check
function circleCollision(c1, c2) {
    const dx = c2.x - c1.x;
    const dy = c2.y - c1.y;

    const distanceSquared = dx * dx + dy * dy;

    const radiusSum = c1.radius + c2.radius;

    return distanceSquared <= radiusSum * radiusSum;
}
🎮 Why This Version Is Better
Faster for games
No expensive square root calculation
Used in:
game engines
physics systems
particle simulations
collision systems
📊 Example
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

Output:

true
🎨 README Design Version

You can paste this directly into GitHub README.

🟣 Circle Collision Detection in JavaScript

A simple and optimized circle collision algorithm used in games and physics engines.

📐 Formula

(x
2
	​

−x
1
	​

)
2
+(y
2
	​

−y
1
	​

)
2
≤(r
1
	​

+r
2
	​

)
2

🚀 Optimized Collision Function
function circleCollision(c1, c2) {
    const dx = c2.x - c1.x;
    const dy = c2.y - c1.y;

    const distanceSquared = dx * dx + dy * dy;
    const radiusSum = c1.radius + c2.radius;

    return distanceSquared <= radiusSum * radiusSum;
}
📦 Example
const c1 = { x: 2, y: 3, radius: 8 };
const c2 = { x: 5, y: 5, radius: 9 };

console.log(circleCollision(c1, c2));
✅ Result
true
🎮 Use Cases
2D games
Physics engines
Enemy detection
Hitboxes
Particle systems
Simulations
⚡ Complexity
Time Complexity: O(1)
Space Complexity: O(1)

If you want, I can also make:

🔥 animated SVG diagram
🎮 game-style README
🌌 modern dark-theme README
📊 developer infographic
🧠 explanation with vectors
⚙️ TypeScript version
see this doc
<img width="965" height="670" alt="image" src="https://github.com/user-attachments/assets/d159cb21-792e-4b25-88d8-3f5bf5372b14" />
