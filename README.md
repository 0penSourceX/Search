<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>

<title>Circle Collision Detection</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, Helvetica, sans-serif;
}

body{
    background:#0f172a;
    color:white;
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    padding:40px;
}

.container{
    width:100%;
    max-width:1200px;
}

.card{
    background:rgba(255,255,255,0.05);
    border:1px solid rgba(255,255,255,0.08);
    border-radius:24px;
    padding:40px;
    backdrop-filter:blur(10px);
    box-shadow:
        0 0 40px rgba(0,0,0,0.4),
        0 0 80px rgba(59,130,246,0.15);
}

.title{
    font-size:48px;
    font-weight:bold;
    margin-bottom:10px;

    background:linear-gradient(
        to right,
        #60a5fa,
        #a78bfa
    );

    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
}

.subtitle{
    color:#94a3b8;
    line-height:1.7;
    margin-bottom:40px;
}

/* IMAGE */

.image-box{
    width:100%;
    margin-bottom:40px;
    text-align:center;
}

.image-box img{
    width:100%;
    max-width:850px;
    border-radius:20px;
    border:1px solid rgba(255,255,255,0.08);

    box-shadow:
        0 0 30px rgba(96,165,250,0.2);
}

/* FORMULA */

.formula-card{
    background:#111827;
    border-radius:20px;
    padding:35px;
    text-align:center;
    margin-bottom:40px;
    border:1px solid rgba(255,255,255,0.05);

    transition:0.3s;
}

.formula-card:hover{
    transform:translateY(-6px);

    box-shadow:
        0 0 40px rgba(96,165,250,0.25);
}

.formula-title{
    color:#94a3b8;
    margin-bottom:20px;
    font-size:18px;
}

.formula{
    font-size:36px;
    font-weight:bold;
    color:#60a5fa;
}

/* GRID */

.grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:25px;
    margin-bottom:40px;
}

.info-card{
    background:#111827;
    padding:30px;
    border-radius:20px;
    border:1px solid rgba(255,255,255,0.05);
}

.info-card h2{
    color:#a78bfa;
    margin-bottom:20px;
}

.info-card p{
    margin-bottom:10px;
    color:#cbd5e1;
}

/* STEP */

.step-card{
    background:#111827;
    border-radius:20px;
    padding:30px;
    margin-bottom:30px;
}

.step-card h2{
    margin-bottom:20px;
    color:#60a5fa;
}

.step{
    margin-bottom:25px;
}

.step h3{
    color:#a78bfa;
    margin-bottom:10px;
}

.code{
    background:#020617;
    padding:18px;
    border-radius:14px;
    overflow:auto;
    color:#4ade80;
    margin-top:10px;
}

/* RESULT */

.result{
    margin-top:25px;
    padding:18px;
    border-radius:16px;
    background:#14532d;
    color:#4ade80;
    font-weight:bold;
    text-align:center;
}

/* FINAL CODE */

.final-code{
    background:#020617;
    padding:30px;
    border-radius:20px;
    overflow:auto;
    color:#4ade80;
}

/* BADGES */

.badges{
    margin-top:30px;
}

.badge{
    display:inline-block;
    padding:10px 18px;
    margin:8px;
    border-radius:999px;
    background:#1e293b;
    color:#60a5fa;
    border:1px solid rgba(255,255,255,0.08);
}

/* RESPONSIVE */

@media(max-width:850px){

    .grid{
        grid-template-columns:1fr;
    }

    .title{
        font-size:34px;
    }

    .formula{
        font-size:24px;
    }

}

</style>
</head>

<body>

<div class="container">

<div class="card">

    <h1 class="title">
        🟣 Circle Collision Detection
    </h1>

    <p class="subtitle">
        Detect collisions between two circles using the Euclidean distance formula.
        This technique is widely used in game engines, physics simulations,
        particle systems, and hitbox detection.
    </p>

    <!-- YOUR IMAGE -->

    <div class="image-box">

        <!-- CHANGE IMAGE NAME HERE -->
        <img src="demo.png" alt="Circle collision demonstration">

    </div>

    <!-- FORMULA -->

    <div class="formula-card">

        <div class="formula-title">
            Distance Formula
        </div>

        <div class="formula">
            √((x₂ - x₁)² + (y₂ - y₁)²) ≤ r₁ + r₂
        </div>

    </div>

    <!-- CIRCLE DATA -->

    <div class="grid">

        <div class="info-card">

            <h2>📌 Circle A</h2>

            <p>x = 2</p>
            <p>y = 3</p>
            <p>radius = 8</p>

        </div>

        <div class="info-card">

            <h2>📌 Circle B</h2>

            <p>x = 5</p>
            <p>y = 5</p>
            <p>radius = 9</p>

        </div>

    </div>

    <!-- STEP BY STEP -->

    <div class="step-card">

        <h2>
            🧠 Step-by-Step Calculation
        </h2>

        <div class="step">

            <h3>1. Calculate X Distance</h3>

            <div class="code">
<pre>
dx = x2 - x1
dx = 5 - 2
dx = 3
</pre>
            </div>

        </div>

        <div class="step">

            <h3>2. Calculate Y Distance</h3>

            <div class="code">
<pre>
dy = y2 - y1
dy = 5 - 3
dy = 2
</pre>
            </div>

        </div>

        <div class="step">

            <h3>3. Compute Distance</h3>

            <div class="code">
<pre>
d = Math.sqrt(3*3 + 2*2)
d = Math.sqrt(9 + 4)
d = Math.sqrt(13)
d ≈ 3.6
</pre>
            </div>

        </div>

        <div class="step">

            <h3>4. Compare with Radii Sum</h3>

            <div class="code">
<pre>
3.6 <= 17
</pre>
            </div>

        </div>

        <div class="result">
            ✅ Collision Detected
        </div>

    </div>

    <!-- FINAL JS -->

    <div class="step-card">

        <h2>
            🚀 Optimized JavaScript Implementation
        </h2>

        <div class="final-code">
<pre>
function circleCollision(c1, c2) {

    const dx = c2.x - c1.x;
    const dy = c2.y - c1.y;

    const distanceSquared = dx * dx + dy * dy;

    const radiusSum = c1.radius + c2.radius;

    return distanceSquared <= radiusSum * radiusSum;
}

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
</pre>
        </div>

    </div>

    <!-- BADGES -->

    <div class="badges">

        <span class="badge">🎮 Game Development</span>

        <span class="badge">⚡ Physics Engine</span>

        <span class="badge">🧠 Collision Detection</span>

        <span class="badge">📐 Mathematics</span>

        <span class="badge">🚀 JavaScript</span>

    </div>

</div>

</div>

</body>
</html>
