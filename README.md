# ðŸª» Aethel Lavender Fashion Hub

**Project Title:** Aethel Lavender Fashion Hub  
**Stitch Project ID:** 10969939508210603174  
**GitHub Repository:** [AETHEL-Major-Project-Corizo](https://github.com/nigeshsatheesh/AETHEL-Major-Project-Corizo)

---

## ðŸ“Œ Project Overview

This repository contains the complete design code and visual screenshots for the **Aethel Lavender Fashion Hub**, downloaded directly using the **Stitch API**.

---

## ðŸ—‚ï¸ Downloaded Screens Summary

| # | Screen Name | Screen ID | Code Link | Preview |
|---|---|---|---|---|
| 1 | **Aethel Admin - Orders & Customers** | e2b2fc96f1c847d8b4879495c51d0227 | [HTML Code](./01-admin-orders-customers/index.html) | [Screenshot](./01-admin-orders-customers/screenshot.png) |
| 2 | **Aethel Admin - Add Product** | 6b418cd50a984059b829e838bae75f1c | [HTML Code](./02-admin-add-product/index.html) | [Screenshot](./02-admin-add-product/screenshot.png) |
| 3 | **Aethel Admin - Overview** | 157957aa5ced44a48669f6e2ecbf886f | [HTML Code](./03-admin-overview/index.html) | [Screenshot](./03-admin-overview/screenshot.png) |
| 4 | **Aethel - Checkout & Confirmation** | efac51e898fc4842856bb60d1137cbef | [HTML Code](./04-checkout-confirmation/index.html) | [Screenshot](./04-checkout-confirmation/screenshot.png) |
| 5 | **Aethel - Sign In or Join** | 9d3af3b80494405994ed3c6d88f2fe8f | [HTML Code](./05-sign-in-or-join/index.html) | [Screenshot](./05-sign-in-or-join/screenshot.png) |
| 6 | **Aethel - Shop Modern Fashion** | 205ed935836e4f5691da956fc6384535 | [HTML Code](./06-shop-modern-fashion/index.html) | [Screenshot](./06-shop-modern-fashion/screenshot.png) |
| 7 | **Aethel - Oversized Lavender Knit Sweater** | ca0a42b9d6ce4f54ad173afa4d470a1d | [HTML Code](./07-oversized-lavender-knit-sweater/index.html) | [Screenshot](./07-oversized-lavender-knit-sweater/screenshot.png) |

---

## ðŸš€ How to Run / View

Open index.html in your web browser or navigate into any screen's directory to inspect the HTML source and UI mockup directly.

`ash
# Clone repository
git clone https://github.com/nigeshsatheesh/AETHEL-Major-Project-Corizo.git

# Navigate into project directory
cd AETHEL-Major-Project-Corizo
`
"@

 = @"
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aethel Lavender Fashion Hub - Stitch Showcase</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-dark: #0f0b1a;
            --card-bg: #1c152d;
            --border-color: #31264c;
            --accent-purple: #9d4edd;
            --accent-lavender: #c77dff;
            --text-light: #f8f7ff;
            --text-muted: #b8b3cf;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Plus Jakarta Sans', sans-serif;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-light);
            min-height: 100vh;
            padding: 2rem;
        }

        header {
            text-align: center;
            margin-bottom: 3rem;
        }

        h1 {
            font-size: 2.5rem;
            background: linear-gradient(135deg, #e0aaff, #c77dff, #7b2cbf);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 0.5rem;
        }

        p.subtitle {
            color: var(--text-muted);
            font-size: 1.1rem;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
            gap: 2rem;
            max-width: 1400px;
            margin: 0 auto;
        }

        .card {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            overflow: hidden;
            transition: transform 0.3s ease, border-color 0.3s ease, box-shadow 0.3s ease;
            display: flex;
            flex-direction: column;
        }

        .card:hover {
            transform: translateY(-6px);
            border-color: var(--accent-lavender);
            box-shadow: 0 12px 30px rgba(157, 78, 221, 0.25);
        }

        .card-img-container {
            height: 240px;
            overflow: hidden;
            background-color: #120d20;
            position: relative;
        }

        .card-img-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top;
            transition: transform 0.5s ease;
        }

        .card:hover .card-img-container img {
            transform: scale(1.05);
        }

        .card-body {
            padding: 1.5rem;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .card-title {
            font-size: 1.25rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
            color: var(--text-light);
        }

        .screen-id {
            font-size: 0.8rem;
            color: var(--accent-lavender);
            font-family: monospace;
            margin-bottom: 1.25rem;
            background: rgba(199, 125, 255, 0.1);
            padding: 4px 8px;
            border-radius: 6px;
            display: inline-block;
        }

        .btn-group {
            display: flex;
            gap: 0.75rem;
        }

        .btn {
            flex: 1;
            padding: 0.75rem 1rem;
            border-radius: 10px;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.9rem;
            text-align: center;
            transition: all 0.2s ease;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--accent-purple), #7b2cbf);
            color: #fff;
        }

        .btn-primary:hover {
            opacity: 0.9;
            box-shadow: 0 4px 14px rgba(157, 78, 221, 0.4);
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.05);
            color: var(--text-muted);
            border: 1px solid var(--border-color);
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.1);
            color: #fff;
        }

        footer {
            text-align: center;
            margin-top: 4rem;
            color: var(--text-muted);
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <header>
        <h1>ðŸª» Aethel Lavender Fashion Hub</h1>
        <p class="subtitle">Stitch Project ID: 10969939508210603174 | Downloaded UI Screens & HTML Code</p>
    </header>

    <div class="grid">
        <div class="card">
            <div class="card-img-container">
                <img src="./01-admin-orders-customers/screenshot.png" alt="Aethel Admin - Orders & Customers">
            </div>
            <div class="card-body">
                <div>
                    <div class="card-title">1. Admin - Orders & Customers</div>
                    <div class="screen-id">ID: e2b2fc96f1c847d8b4879495c51d0227</div>
                </div>
                <div class="btn-group">
                    <a href="./01-admin-orders-customers/index.html" class="btn btn-primary" target="_blank">View Code</a>
                    <a href="./01-admin-orders-customers/screenshot.png" class="btn btn-secondary" target="_blank">Screenshot</a>
                </div>
            </div>
        </div>

        <div class="card">
            <div class="card-img-container">
                <img src="./02-admin-add-product/screenshot.png" alt="Aethel Admin - Add Product">
            </div>
            <div class="card-body">
                <div>
                    <div class="card-title">2. Admin - Add Product</div>
                    <div class="screen-id">ID: 6b418cd50a984059b829e838bae75f1c</div>
                </div>
                <div class="btn-group">
                    <a href="./02-admin-add-product/index.html" class="btn btn-primary" target="_blank">View Code</a>
                    <a href="./02-admin-add-product/screenshot.png" class="btn btn-secondary" target="_blank">Screenshot</a>
                </div>
            </div>
        </div>

        <div class="card">
            <div class="card-img-container">
                <img src="./03-admin-overview/screenshot.png" alt="Aethel Admin - Overview">
            </div>
            <div class="card-body">
                <div>
                    <div class="card-title">3. Admin - Overview</div>
                    <div class="screen-id">ID: 157957aa5ced44a48669f6e2ecbf886f</div>
                </div>
                <div class="btn-group">
                    <a href="./03-admin-overview/index.html" class="btn btn-primary" target="_blank">View Code</a>
                    <a href="./03-admin-overview/screenshot.png" class="btn btn-secondary" target="_blank">Screenshot</a>
                </div>
            </div>
        </div>

        <div class="card">
            <div class="card-img-container">
                <img src="./04-checkout-confirmation/screenshot.png" alt="Aethel - Checkout & Confirmation">
            </div>
            <div class="card-body">
                <div>
                    <div class="card-title">4. Checkout & Confirmation</div>
                    <div class="screen-id">ID: efac51e898fc4842856bb60d1137cbef</div>
                </div>
                <div class="btn-group">
                    <a href="./04-checkout-confirmation/index.html" class="btn btn-primary" target="_blank">View Code</a>
                    <a href="./04-checkout-confirmation/screenshot.png" class="btn btn-secondary" target="_blank">Screenshot</a>
                </div>
            </div>
        </div>

        <div class="card">
            <div class="card-img-container">
                <img src="./05-sign-in-or-join/screenshot.png" alt="Aethel - Sign In or Join">
            </div>
            <div class="card-body">
                <div>
                    <div class="card-title">5. Sign In or Join</div>
                    <div class="screen-id">ID: 9d3af3b80494405994ed3c6d88f2fe8f</div>
                </div>
                <div class="btn-group">
                    <a href="./05-sign-in-or-join/index.html" class="btn btn-primary" target="_blank">View Code</a>
                    <a href="./05-sign-in-or-join/screenshot.png" class="btn btn-secondary" target="_blank">Screenshot</a>
                </div>
            </div>
        </div>

        <div class="card">
            <div class="card-img-container">
                <img src="./06-shop-modern-fashion/screenshot.png" alt="Aethel - Shop Modern Fashion">
            </div>
            <div class="card-body">
                <div>
                    <div class="card-title">6. Shop Modern Fashion</div>
                    <div class="screen-id">ID: 205ed935836e4f5691da956fc6384535</div>
                </div>
                <div class="btn-group">
                    <a href="./06-shop-modern-fashion/index.html" class="btn btn-primary" target="_blank">View Code</a>
                    <a href="./06-shop-modern-fashion/screenshot.png" class="btn btn-secondary" target="_blank">Screenshot</a>
                </div>
            </div>
        </div>

        <div class="card">
            <div class="card-img-container">
                <img src="./07-oversized-lavender-knit-sweater/screenshot.png" alt="Aethel - Oversized Lavender Knit Sweater">
            </div>
            <div class="card-body">
                <div>
                    <div class="card-title">7. Oversized Lavender Knit Sweater</div>
                    <div class="screen-id">ID: ca0a42b9d6ce4f54ad173afa4d470a1d</div>
                </div>
                <div class="btn-group">
                    <a href="./07-oversized-lavender-knit-sweater/index.html" class="btn btn-primary" target="_blank">View Code</a>
                    <a href="./07-oversized-lavender-knit-sweater/screenshot.png" class="btn btn-secondary" target="_blank">Screenshot</a>
                </div>
            </div>
        </div>
    </div>

    <footer>
        <p>Project created for Corizo Major Project â€¢ Maintained by @nigeshsatheesh</p>
    </footer>

</body>
</html>
