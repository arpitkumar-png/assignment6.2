HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 6.2 — Backgrounds, Borders & Display</title>
    <!-- Link to External Stylesheet -->
    <link rel="stylesheet" href="cards-style.css">
</head>
<body>

    <!-- Header -->
    <header class="page-header">
        <h1>Card Designs & Display Properties</h1>
        <p>Exploring distinct backgrounds, borders, rounded corners, and display behaviors.</p>
    </header>

    <main class="container">
        <!-- --- 1, 2, 3, 4, 6. Three Distinct Cards --- -->
        <section class="cards-wrapper">
            
            <!-- Basic Card -->
            <div class="card basic-card">
                <h2>Basic Plan</h2>
                <p>Ideal for beginners starting out with personal projects and foundational learning.</p>
                <button class="card-btn">Choose Basic</button>
            </div>

            <!-- Standard Card -->
            <div class="card standard-card">
                <h2>Standard Plan</h2>
                <p>Great for growing developers who need extra resources and collaborative tools.</p>
                <button class="card-btn">Choose Standard</button>
            </div>

            <!-- Premium Card -->
            <div class="card premium-card">
                <h2>Premium Plan</h2>
                <p>Advanced features, priority support, and complete access to all professional modules.</p>
                <button class="card-btn">Choose Premium</button>
            </div>

        </section>

        <!-- --- 5. Display Property Demonstration Section --- -->
        <section class="display-demo-section">
            <h2>Display Property Examples</h2>
            <p>Understanding how elements behave on a webpage:</p>

            <div class="display-container">
                <!-- Inline Example -->
                <div class="demo-group">
                    <h3>1. Display: Inline</h3>
                    <p>Elements like <span class="demo-inline">this span tag</span> flow within text and ignore explicit width/height properties.</p>
                </div>

                <!-- Block Example -->
                <div class="demo-group">
                    <h3>2. Display: Block</h3>
                    <p>Elements like <div class="demo-block">this block div</div> force a line break and take up the full available width.</p>
                </div>

                <!-- Inline-Block Example -->
                <div class="demo-group">
                    <h3>3. Display: Inline-Block</h3>
                    <p>Elements like <span class="demo-inline-block">this inline-block</span> sit side-by-side while respecting custom width, height, and padding.</p>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Student Card & Display Lab. All rights reserved.</p>
    </footer>

</body>
</html>
File 2: cards-style.css
CSS
/* --- Global Reset & Typography --- */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f8fafc;
    color: #334155;
    line-height: 1.6;
    padding: 2rem;
}

/* --- Header Styling --- */
.page-header {
    text-align: center;
    margin-bottom: 2.5rem;
}

.page-header h1 {
    color: #1e293b;
    font-size: 2rem;
    margin-bottom: 0.5rem;
}

.page-header p {
    color: #64748b;
}

.container {
    max-width: 1000px;
    margin: 0 auto;
}

/* --- Cards Layout Wrapper --- */
.cards-wrapper {
    display: flex;
    gap: 1.5rem;
    flex-wrap: wrap;
    justify-content: center;
    margin-bottom: 3rem;
}

/* --- Base Card Styles (Steps 3, 4, 6) --- */
.card {
    width: 100%;
    max-width: 300px;         /* 6. Set max-width */
    min-height: 280px;        /* 6. Set height constraints */
    padding: 2rem;            /* Padding */
    border-radius: 12px;      /* 4. Rounded corners */
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
    transition: transform 0.2s ease;
}

.card:hover {
    transform: translateY(-4px);
}

.card h2 {
    font-size: 1.4rem;
    margin-bottom: 0.75rem;
}

.card p {
    font-size: 0.95rem;
    margin-bottom: 1.5rem;
}

/* Button inside card */
.card-btn {
    padding: 0.75rem 1rem;
    font-size: 0.95rem;
    font-weight: 600;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    transition: opacity 0.2s ease;
}

.card-btn:hover {
    opacity: 0.9;
}

/* --- 3. Distinct Backgrounds & Borders for Each Card --- */

/* Basic Card */
.basic-card {
    background-color: #ffffff;
    border: 1px solid #cbd5e1;
}
.basic-card h2 { color: #475569; }
.basic-card .card-btn { background-color: #475569; color: #ffffff; }

/* Standard Card */
.standard-card {
    background-color: #eff6ff;
    border: 2px solid #3b82f6;
}
.standard-card h2 { color: #1d4ed8; }
.standard-card .card-btn { background-color: #3b82f6; color: #ffffff; }

/* Premium Card */
.premium-card {
    background-color: #faf5ff;
    border: 2px solid #9333ea;
}
.premium-card h2 { color: #7e22ce; }
.premium-card .card-btn { background-color: #9333ea; color: #ffffff; }


/* --- 5. Display Property Demonstration Styles --- */
.display-demo-section {
    background-color: #ffffff;
    border: 1px solid #e2e8f0;
    border-radius: 12px;
    padding: 2rem;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.02);
}

.display-demo-section h2 {
    color: #1e293b;
    margin-bottom: 0.5rem;
}

.display-demo-section > p {
    color: #64748b;
    margin-bottom: 1.5rem;
}

.demo-group {
    margin-bottom: 1.5rem;
}

.demo-group h3 {
    font-size: 1.1rem;
    color: #334155;
    margin-bottom: 0.5rem;
}

/* 1. display: inline */
.demo-inline {
    display: inline;
    background-color: #f1f5f9;
    color: #e11d48;
    padding: 0.2rem 0.4rem;
    border: 1px dashed #cbd5e1;
    /* Note: width and height will have NO effect on inline elements */
    width: 150px; 
    height: 50px;
}

/* 2. display: block */
.demo-block {
    display: block;
    background-color: #f1f5f9;
    color: #2563eb;
    padding: 0.5rem;
    margin-top: 0.4rem;
    border: 1px solid #93c5fd;
    width: 100%; /* Takes full width */
}

/* 3. display: inline-block */
.demo-inline-block {
    display: inline-block;
    background-color: #f1f5f9;
    color: #16a34a;
    padding: 0.4rem 0.8rem;
    margin-top: 0.4rem;
    border: 1px solid #86efac;
    width: 180px;  /* Width is respected */
    height: 40px;  /* Height is respected */
    text-align: center;
}