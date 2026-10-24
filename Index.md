HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pricing Cards & Centered Login Form</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- SECTION 1: Pricing Cards -->
    <section class="pricing-section">
        <h2 class="section-title">Choose Your Plan</h2>
        
        <!-- Parent Flex Container for Cards -->
        <div class="pricing-container">
            
            <!-- 1 & 2. Basic Plan -->
            <div class="card">
                <h3 class="plan-title">Basic</h3>
                <div class="price">$9<span>/mo</span></div>
                <ul class="features">
                    <li>1 User</li>
                    <li>5 GB Storage</li>
                    <li>Basic Support</li>
                    <li>Access to Core Features</li>
                </ul>
                <a href="#" class="btn btn-outline">Select Plan</a>
            </div>

            <!-- 1 & 2. Pro Plan (Highlighted) -->
            <div class="card card-featured">
                <span class="badge">Popular</span>
                <h3 class="plan-title">Pro</h3>
                <div class="price">$29<span>/mo</span></div>
                <ul class="features">
                    <li>5 Users</li>
                    <li>50 GB Storage</li>
                    <li>Priority Email Support</li>
                    <li>Advanced Analytics</li>
                </ul>
                <a href="#" class="btn btn-primary">Select Plan</a>
            </div>

            <!-- 1 & 2. Premium Plan -->
            <div class="card">
                <h3 class="plan-title">Premium</h3>
                <div class="price">$79<span>/mo</span></div>
                <ul class="features">
                    <li>Unlimited Users</li>
                    <li>500 GB Storage</li>
                    <li>24/7 Dedicated Support</li>
                    <li>Custom Integrations</li>
                </ul>
                <a href="#" class="btn btn-outline">Select Plan</a>
            </div>

        </div>
    </section>

    <!-- SECTION 2: Centered Login Form Section -->
    <section class="login-section">
        <!-- Flex Container to center form vertically & horizontally -->
        <div class="form-wrapper">
            <form class="login-form">
                <h2>Welcome Back</h2>
                <p>Please enter your details to log in.</p>

                <div class="input-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" placeholder="you@example.com" required>
                </div>

                <div class="input-group">
                    <label for="password">Password</label>
                    <input type="password" id="password" placeholder="••••••••" required>
                </div>

                <button type="submit" class="btn btn-primary btn-full">Log In</button>
            </form>
        </div>
    </section>

</body>
</html>


CSS
/* Base Resets */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    background-color: #f4f7f6;
    color: #333;
}

.section-title {
    text-align: center;
    font-size: 2rem;
    margin-bottom: 2rem;
    color: #2c3e50;
}

/* ==========================================
   SECTION 1: Pricing Cards Styling (Flexbox)
   ========================================== */
.pricing-section {
    padding: 3rem 1rem;
}

/* 3 & 4. Flex Parent Container for Cards */
.pricing-container {
    display: flex; /* Activate Flexbox */
    flex-direction: row; /* Horizontal alignment */
    justify-content: center; /* Evenly space/center cards horizontally */
    align-items: center; /* Align cards vertically along cross axis */
    gap: 2rem; /* Spacing between cards */
    max-width: 1200px;
    margin: 0 auto;
}

/* Pricing Card Base */
.card {
    background: #ffffff;
    border-radius: 10px;
    padding: 2.5rem 1.5rem;
    width: 300px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
    
    /* Internal Card Flexbox (vertical column layout) */
    display: flex;
    flex-direction: column;
    align-items: center;
    position: relative;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.12);
}

/* Featured Card Styling */
.card-featured {
    border: 2px solid #3498db;
    transform: scale(1.05); /* Slightly bigger to emphasize */
}

.card-featured:hover {
    transform: scale(1.05) translateY(-5px);
}

.badge {
    position: absolute;
    top: -12px;
    background-color: #3498db;
    color: #ffffff;
    font-size: 0.8rem;
    font-weight: bold;
    padding: 0.3rem 0.8rem;
    border-radius: 20px;
    text-transform: uppercase;
}

.plan-title {
    font-size: 1.5rem;
    color: #2c3e50;
    margin-bottom: 1rem;
}

.price {
    font-size: 2.5rem;
    font-weight: bold;
    color: #2c3e50;
    margin-bottom: 1.5rem;
}

.price span {
    font-size: 1rem;
    color: #7f8c8d;
}

.features {
    list-style: none;
    text-align: center;
    margin-bottom: 2rem;
    width: 100%;
}

.features li {
    padding: 0.6rem 0;
    border-bottom: 1px solid #eeeeee;
    font-size: 0.95rem;
    color: #666;
}

.features li:last-child {
    border-bottom: none;
}

/* Button Styles */
.btn {
    display: inline-block;
    padding: 0.75rem 1.5rem;
    border-radius: 5px;
    text-decoration: none;
    font-weight: bold;
    text-align: center;
    cursor: pointer;
    border: none;
    transition: background-color 0.3s ease;
}

.btn-primary {
    background-color: #3498db;
    color: #ffffff;
}

.btn-primary:hover {
    background-color: #2980b9;
}

.btn-outline {
    background-color: transparent;
    color: #3498db;
    border: 2px solid #3498db;
}

.btn-outline:hover {
    background-color: #3498db;
    color: #ffffff;
}

.btn-full {
    width: 100%;
}


/* ==========================================
   SECTION 2: Centered Login Form (Flexbox)
   ========================================== */
.login-section {
    background-color: #eef2f5;
    padding: 4rem 1rem;
}

/* 5 & 6. Perfect Vertical & Horizontal Centering Container */
.form-wrapper {
    display: flex;
    justify-content: center; /* Horizontal centering */
    align-items: center;     /* Vertical centering */
    min-height: 50vh;        /* Provides height to demonstrate vertical alignment */
}

/* Form Container Flexbox */
.login-form {
    background-color: #ffffff;
    padding: 2.5rem;
    border-radius: 10px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
    width: 100%;
    max-width: 400px;

    /* Internal form layout stacked vertically */
    display: flex;
    flex-direction: column;
}

.login-form h2 {
    margin-bottom: 0.5rem;
    color: #2c3e50;
}

.login-form p {
    color: #7f8c8d;
    font-size: 0.9rem;
    margin-bottom: 1.5rem;
}

.input-group {
    display: flex;
    flex-direction: column;
    margin-bottom: 1.2rem;
}

.input-group label {
    font-size: 0.85rem;
    font-weight: 600;
    margin-bottom: 0.4rem;
    color: #34495e;
}

.input-group input {
    padding: 0.75rem;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-size: 1rem;
    outline: none;
}

.input-group input:focus {
    border-color: #3498db;
}


/* ==========================================
   Responsive Design for Smaller Screens
   ========================================== */
@media (max-width: 900px) {
    /* 6. Demonstrating flex-direction change on mobile */
    .pricing-container {
        flex-direction: column;
        align-items: center;
    }

    .card-featured {
        transform: scale(1);
    }

    .card-featured:hover {
        transform: translateY(-5px);
    }
}