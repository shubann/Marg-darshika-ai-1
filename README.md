# Marg-darshika-ai-1
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Marg-Darshika AI - Safety-First Navigation</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: #e2e8f0;
            background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 50%, #16213e 100%);
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            background: radial-gradient(circle at 20% 80%, rgba(120, 119, 198, 0.3) 0%, transparent 50%),
                        radial-gradient(circle at 80% 20%, rgba(255, 119, 198, 0.3) 0%, transparent 50%);
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grid" width="10" height="10" patternUnits="userSpaceOnUse"><path d="M 10 0 L 0 0 0 10" fill="none" stroke="%23ffffff" stroke-width="0.5" opacity="0.1"/></pattern></defs><rect width="100" height="100" fill="url(%23grid)"/></svg>');
            animation: float 20s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .hero-content {
            max-width: 800px;
            z-index: 2;
            position: relative;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 5vw, 4.5rem);
            font-weight: 700;
            background: linear-gradient(135deg, #a855f7, #3b82f6, #06b6d4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 1rem;
            animation: slideInUp 1s ease-out;
        }

        .hero .subtitle {
            font-size: clamp(1.2rem, 2.5vw, 1.8rem);
            color: #94a3b8;
            font-weight: 400;
            margin-bottom: 1.5rem;
            animation: slideInUp 1s ease-out 0.2s both;
        }

        .hero .tagline {
            font-size: clamp(1.1rem, 2vw, 1.4rem);
            font-style: italic;
            color: #64748b;
            margin-bottom: 2.5rem;
            animation: slideInUp 1s ease-out 0.4s both;
        }

        .cta-button {
            display: inline-block;
            background: linear-gradient(135deg, #8b5cf6, #3b82f6);
            color: white;
            padding: 1rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(139, 92, 246, 0.4);
            animation: slideInUp 1s ease-out 0.6s both;
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 20px 40px rgba(139, 92, 246, 0.6);
        }

        /* Section Styles */
        .section {
            padding: 100px 0;
        }

        .section-title {
            font-size: clamp(2rem, 4vw, 3rem);
            text-align: center;
            margin-bottom: 3rem;
            background: linear-gradient(135deg, #a855f7, #3b82f6);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(135deg, #8b5cf6, #3b82f6);
            border-radius: 2px;
        }

        /* About Section */
        .about-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
            font-size: 1.2rem;
        }

        /* How It Works */
        .steps-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 4rem;
        }

        .step {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 2.5rem;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .step::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(135deg, #8b5cf6, #3b82f6);
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }

        .step:hover::before {
            transform: scaleX(1);
        }

        .step:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(139, 92, 246, 0.2);
        }

        .step-number {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #8b5cf6, #3b82f6);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            font-weight: 700;
            color: white;
            margin: 0 auto 1.5rem;
        }

        /* Features */
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 4rem;
        }

        .feature {
            display: flex;
            align-items: flex-start;
            gap: 1rem;
            padding: 2rem;
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 16px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }

        .feature:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(139, 92, 246, 0.2);
        }

        .feature-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, #8b5cf6, #3b82f6);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            color: white;
            flex-shrink: 0;
        }

        /* Impact Section */
        .impact-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin: 4rem auto;
            max-width: 800px;
        }

        .stat {
            text-align: center;
            padding: 2rem;
        }

        .stat-number {
            font-size: 3rem;
            font-weight: 700;
            background: linear-gradient(135deg, #10b981, #34d399);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            display: block;
        }

        /* Tech Stack */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 4rem;
        }

        .tech-item {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 16px;
            padding: 2rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
            text-align: center;
        }

        .tech-logo {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        /* Map Placeholder */
        .map-placeholder {
            height: 400px;
            background: linear-gradient(135deg, #1e3a8a, #1e40af);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 2rem auto;
            max-width: 800px;
            position: relative;
            overflow: hidden;
        }

        .map-placeholder::before {
            content: '🗺️ Interactive Map Preview';
            font-size: 1.5rem;
            z-index: 2;
        }

        .map-placeholder::after {
            content: '';
            position: absolute;
            top: 20%;
            left: 20%;
            right: 20%;
            height: 2px;
            background: rgba(255, 255, 255, 0.3);
            box-shadow: 0 0 20px rgba(139, 92, 246, 0.5);
            animation: scan 3s linear infinite;
        }

        @keyframes scan {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        /* Footer */
        .footer {
            background: rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(10px);
            padding: 3rem 0 1.5rem;
            text-align: center;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        .footer-content {
            opacity: 0.8;
            font-size: 1rem;
        }

        /* Animations */
        @keyframes slideInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Mobile Responsiveness */
        @media (max-width: 768px) {
            .hero {
                text-align: center;
                padding: 2rem 0;
                min-height: 90vh;
            }

            .section {
                padding: 60px 0;
            }

            .steps-grid,
            .features-grid,
            .tech-grid {
                grid-template-columns: 1fr;
            }

            .feature {
                flex-direction: column;
                text-align: center;
            }
        }

        /* Scroll animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Marg-Darshika AI</h1>
                <p class="subtitle">A Safety-First Navigation System</p>
                <p class="tagline">“Not the fastest route. The safest one.”</p>
                <a href="#demo" class="cta-button">Explore Demo</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="section" id="about">
        <div class="container">
            <h2 class="section-title fade-in">About the Project</h2>
            <div class="about-content fade-in">
                <p>Unlike Google Maps that prioritizes speed, <strong>Marg-Darshika AI</strong> puts your safety first. Our system calculates a <strong>Safety Score</strong> for every road using real-time data, user feedback, and intelligent algorithms to generate the safest routes possible—especially crucial for urban India.</p>
            </div>
            <div class="map-placeholder fade-in"></div>
        </div>
    </section>

    <!-- How It Works -->
    <section class="section" id="how-it-works">
        <div class="container">
            <h2 class="section-title fade-in">How It Works</h2>
            <div class="steps-grid">
                <div class="step fade-in">
                    <div class="step-number">1</div>
                    <h3>Collect Data</h3>
                    <p>Crime statistics, street activity, lighting conditions, and real-time user feedback from across cities.</p>
                </div>
                <div class="step fade-in">
                    <div class="step-number">2</div>
                    <h3>Calculate Safety Score</h3>
                    <p>AI-powered algorithm analyzes multiple factors to assign a Safety Score (0-100) to every road segment.</p>
                </div>
                <div class="step fade-in">
                    <div class="step-number">3</div>
                    <h3>Generate Safer Routes</h3>
                    <p>Smart routing engine finds the safest path, prioritizing well-lit, busy areas over shortcuts.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="section" id="features">
        <div class="container">
            <h2 class="section-title fade-in">Key Features</h2>
            <div class="features-grid">
                <div class="feature fade-in">
                    <div class="feature-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <div>
                        <h3>Safety Score</h3>
                        <p>Every road rated 0-100 based on real-time safety data.</p>
                    </div>
                </div>
                <div class="feature fade-in">
                    <div class="feature-icon">
                        <i class="fas fa-moon"></i>
                    </div>
                    <div>
                        <h3>Night-Safe Routing</h3>
                        <p>Special algorithms for nighttime travel with enhanced safety focus.</p>
                    </div>
                </div>
                <div class="feature fade-in">
                    <div class="feature-icon">
                        <i class="fas fa-users-slash"></i>
                    </div>
                    <div>
                        <h3>Avoid Isolated Areas</h3>
                        <p>Automatically bypasses poorly lit or deserted stretches.</p>
                    </div>
                </div>
                <div class="feature fade-in">
                    <div class="feature-icon">
                        <i class="fas fa-sync-alt"></i>
                    </div>
                    <div>
                        <h3>Real-Time Updates</h3>
                        <p>Live updates from community reports and authorities.</p>
                    </div>
                </div>
                <div class="feature fade-in">
                    <div class="feature-icon">
                        <i class="fas fa-comment-dots"></i>
                    </div>
                    <div>
                        <h3>User Feedback</h3>
                        <p>Community-driven safety reports improve accuracy over time.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Impact Section -->
    <section class="section" id="impact">
        <div class="container">
            <h2 class="section-title fade-in">Real Impact</h2>
            <div class="about-content fade-in">
                <p>Marg-Darshika AI empowers women, students, and vulnerable users to navigate urban India with confidence. By prioritizing safety over speed, we create safer travel experiences for millions.</p>
            </div>
            <div class="impact-stats">
                <div class="stat fade-in">
                    <span class="stat-number">93%</span>
                    <p>Safer routes generated</p>
                </div>
                <div class="stat fade-in">
                    <span class="stat-number">24/7</span>
                    <p>Real-time monitoring</p>
                </div>
                <div class="stat fade-in">
                    <span class="stat-number">50K+</span>
                    <p>Roads mapped</p>
                </div>
                <div class="stat fade-in">
                    <span class="stat-number">10K+</span>
                    <p>Users protected</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Tech Stack -->
    <section class="section" id="tech">
        <div class="container">
            <h2 class="section-title fade-in">Tech Stack</h2>
            <div class="tech-grid">
                <div class="tech-item fade-in">
                    <div class="tech-logo"> 
