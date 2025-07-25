<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KaolaraPay - Crypto Payments for Africa</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: #0F1115;
            color: #ffffff;
            line-height: 1.6;
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
            background: linear-gradient(135deg, #0F1115 0%, #1a1f2e 100%);
            overflow: hidden;
        }

        .crypto-bubble {
            position: absolute;
            top: 10%;
            right: 10%;
            width: 200px;
            height: 200px;
            background: linear-gradient(145deg, #00E676, #40C4FF);
            border-radius: 50%;
            opacity: 0.1;
            animation: float 6s ease-in-out infinite;
            z-index: 1;
        }

        .crypto-bubble::before {
            content: '₿';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 80px;
            color: #ffffff;
            opacity: 0.3;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        .hero-content {
            position: relative;
            z-index: 2;
        }

        .logo {
            width: 80px;
            height: 80px;
            margin-bottom: 2rem;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 230, 118, 0.3);
        }

        .hero h1 {
            font-size: clamp(2.5rem, 5vw, 4rem);
            font-weight: 800;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, #00E676, #40C4FF, #FBC02D);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero p {
            font-size: 1.2rem;
            color: #B0BEC5;
            margin-bottom: 2rem;
            max-width: 600px;
        }

        .launch-date {
            font-size: 1.5rem;
            color: #00E676;
            margin-bottom: 2rem;
            font-weight: 700;
            text-align: center;
            background: rgba(0, 230, 118, 0.1);
            padding: 1rem 2rem;
            border-radius: 12px;
            border: 1px solid rgba(0, 230, 118, 0.3);
            display: inline-block;
        }

        #countdown-display {
            font-size: 2rem;
            font-weight: 800;
            color: #FBC02D;
            font-family: 'Courier New', monospace;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
            margin-bottom: 3rem;
        }

        .btn {
            padding: 15px 30px;
            border: none;
            border-radius: 12px;
            font-weight: 600;
            text-decoration: none;
            display: inline-block;
            transition: all 0.3s ease;
            cursor: pointer;
            font-size: 1rem;
        }

        .btn-primary {
            background: linear-gradient(45deg, #00E676, #00C853);
            color: #000;
            box-shadow: 0 8px 25px rgba(0, 230, 118, 0.4);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 12px 35px rgba(0, 230, 118, 0.6);
        }

        .btn-secondary {
            background: rgba(64, 196, 255, 0.1);
            color: #40C4FF;
            border: 2px solid #40C4FF;
        }

        .btn-secondary:hover {
            background: #40C4FF;
            color: #000;
            transform: translateY(-2px);
        }

        .countdown-timer {
            background: rgba(255, 255, 255, 0.05);
            padding: 20px;
            border-radius: 16px;
            border: 1px solid rgba(0, 230, 118, 0.2);
            backdrop-filter: blur(10px);
        }

        /* Section Styles */
        .section {
            padding: 80px 0;
        }

        .section h2 {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            text-align: center;
        }

        .section-subtitle {
            text-align: center;
            color: #B0BEC5;
            margin-bottom: 3rem;
            font-size: 1.1rem;
        }

        /* Problem Section */
        .problem {
            background: linear-gradient(135deg, #1a1f2e 0%, #0F1115 100%);
        }

        .problem-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .problem-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: 16px;
            border: 1px solid rgba(255, 107, 107, 0.2);
            text-align: center;
        }

        .problem-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        /* Solution Section */
        .solution-features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .feature-card {
            background: rgba(0, 230, 118, 0.1);
            padding: 2rem;
            border-radius: 16px;
            border: 1px solid rgba(0, 230, 118, 0.3);
            text-align: center;
            transition: all 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 230, 118, 0.2);
        }

        .feature-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: #00E676;
        }

        /* Tokenomics */
        .tokenomics-table {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 16px;
            overflow: hidden;
            margin-top: 2rem;
        }

        .tokenomics-table table {
            width: 100%;
            border-collapse: collapse;
        }

        .tokenomics-table th,
        .tokenomics-table td {
            padding: 1rem;
            text-align: left;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .tokenomics-table th {
            background: rgba(0, 230, 118, 0.2);
            color: #00E676;
            font-weight: 600;
        }

        /* Roadmap */
        .roadmap-timeline {
            position: relative;
            margin-top: 3rem;
        }

        .timeline-item {
            display: flex;
            align-items: center;
            margin-bottom: 3rem;
            position: relative;
        }

        .timeline-date {
            background: linear-gradient(45deg, #FBC02D, #F57F17);
            color: #000;
            padding: 10px 20px;
            border-radius: 25px;
            font-weight: 600;
            min-width: 120px;
            text-align: center;
        }

        .timeline-content {
            background: rgba(255, 255, 255, 0.05);
            padding: 1.5rem;
            border-radius: 12px;
            margin-left: 2rem;
            flex: 1;
            border-left: 3px solid #00E676;
        }

        /* How to Buy */
        .how-to-buy-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            margin-top: 3rem;
        }

        .step-card {
            background: rgba(64, 196, 255, 0.1);
            padding: 2rem;
            border-radius: 16px;
            border: 1px solid rgba(64, 196, 255, 0.3);
            text-align: center;
            position: relative;
        }

        .step-number {
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            background: #40C4FF;
            color: #000;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }

        /* Community Section */
        .community {
            background: linear-gradient(135deg, #1a1f2e 0%, #0F1115 100%);
        }

        .community-buttons {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin: 3rem 0;
            flex-wrap: wrap;
        }

        .social-btn {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 15px 30px;
            border-radius: 12px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .telegram-btn {
            background: linear-gradient(45deg, #0088cc, #00acc1);
            color: #fff;
        }

        .twitter-btn {
            background: linear-gradient(45deg, #1da1f2, #40C4FF);
            color: #fff;
        }

        .social-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
        }

        .email-signup {
            max-width: 400px;
            margin: 0 auto;
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .email-input {
            flex: 1;
            padding: 15px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 8px;
            background: rgba(255, 255, 255, 0.05);
            color: #fff;
            min-width: 250px;
        }

        .email-input::placeholder {
            color: #B0BEC5;
        }

        /* Footer */
        .footer {
            background: #000;
            padding: 40px 0;
            text-align: center;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h4 {
            color: #00E676;
            margin-bottom: 1rem;
        }

        .footer-section a {
            color: #B0BEC5;
            text-decoration: none;
            display: block;
            margin-bottom: 0.5rem;
        }

        .footer-section a:hover {
            color: #00E676;
        }

        .disclaimer {
            font-size: 0.9rem;
            color: #666;
            margin-top: 2rem;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .btn {
                width: 100%;
                max-width: 300px;
                text-align: center;
            }
            
            .timeline-item {
                flex-direction: column;
                text-align: center;
            }
            
            .timeline-content {
                margin-left: 0;
                margin-top: 1rem;
            }
            
            .community-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .social-btn {
                width: 100%;
                max-width: 300px;
                justify-content: center;
            }
            
            .email-signup {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section class="hero">
        <div class="crypto-bubble"></div>
        <div class="container">
            <div class="hero-content">
                <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Ccircle cx='50' cy='50' r='45' fill='%2300E676'/%3E%3Ctext x='50' y='60' font-family='Arial, sans-serif' font-size='40' font-weight='bold' text-anchor='middle' fill='%23000'%3EK%3C/text%3E%3C/svg%3E" alt="KaolaraPay Logo" class="logo">
                <h1>KaolaraPay – Crypto Payments for Africa</h1>
                <p>The future of fast, low-cost payments powered by Solana blockchain technology. Connecting Africa to the global crypto economy.</p>
                <div class="launch-date">
                    <div id="countdown-display">48:00:00</div>
                    <div style="font-size: 0.9rem; color: #B0BEC5; margin-top: 0.5rem;">Hours : Minutes : Seconds until launch</div>
                </div>
                <div class="cta-buttons">
                    <a href="#whitelist" class="btn btn-primary">Join Whitelist</a>
                    <a href="https://t.me/+w5NW8F9Vx3FhN2E0" class="btn btn-secondary" target="_blank">Join Telegram Inner Circle</a>
                </div>
                <div class="countdown-timer">
                    <h3>Launch Countdown</h3>
                    <p>Timer widget integration ready</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Problem Section -->
    <section class="section problem">
        <div class="container">
            <h2>The Problem</h2>
            <p class="section-subtitle">African markets face significant barriers to efficient cross-border payments</p>
            <div class="problem-grid">
                <div class="problem-card">
                    <div class="problem-icon">💸</div>
                    <h3>High Transaction Costs</h3>
                    <p>Traditional remittance services charge 8-15% fees, making small payments uneconomical for millions of users.</p>
                </div>
                <div class="problem-card">
                    <div class="problem-icon">⏰</div>
                    <h3>Slow Processing Times</h3>
                    <p>Cross-border payments take 3-7 business days, limiting real-time commerce and emergency transfers.</p>
                </div>
                <div class="problem-card">
                    <div class="problem-icon">🏦</div>
                    <h3>Limited Banking Access</h3>
                    <p>Over 400 million Africans remain unbanked, excluded from traditional financial services.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Solution Section -->
    <section class="section solution">
        <div class="container">
            <h2>The KaolaraPay Solution</h2>
            <p class="section-subtitle">Fast, affordable Solana-powered payments evolving into a comprehensive payment rail</p>
            <div class="solution-features">
                <div class="feature-card">
                    <div class="feature-icon">⚡</div>
                    <h3>Lightning Fast</h3>
                    <p>Solana's sub-second finality enables instant payments and transfers worldwide.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">💰</div>
                    <h3>Ultra Low Fees</h3>
                    <p>Transaction costs under $0.01, making micro-payments viable for everyone.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🌍</div>
                    <h3>Global Accessibility</h3>
                    <p>Mobile-first design works on any smartphone, expanding financial inclusion.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🛡️</div>
                    <h3>Secure & Transparent</h3>
                    <p>Built on Solana's proven blockchain infrastructure with full transaction transparency.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Tokenomics Section -->
    <section class="section tokenomics">
        <div class="container">
            <h2>Tokenomics</h2>
            <p class="section-subtitle">Transparent and sustainable token distribution</p>
            <div class="tokenomics-table">
                <table>
                    <thead>
                        <tr>
                            <th>Metric</th>
                            <th>Details</th>
                            <th>Percentage</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>Total Supply</td>
                            <td>1,000,000,000 KLP</td>
                            <td>100%</td>
                        </tr>
                        <tr>
                            <td>Public Sale</td>
                            <td>400,000,000 KLP</td>
                            <td>40%</td>
                        </tr>
                        <tr>
                            <td>Liquidity Pool</td>
                            <td>250,000,000 KLP</td>
                            <td>25%</td>
                        </tr>
                        <tr>
                            <td>Development</td>
                            <td>200,000,000 KLP</td>
                            <td>20%</td>
                        </tr>
                        <tr>
                            <td>Community Rewards</td>
                            <td>100,000,000 KLP</td>
                            <td>10%</td>
                        </tr>
                        <tr>
                            <td>Team (Locked 2 Years)</td>
                            <td>50,000,000 KLP</td>
                            <td>5%</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </section>

    <!-- Roadmap Section -->
    <section class="section roadmap">
        <div class="container">
            <h2>Roadmap</h2>
            <p class="section-subtitle">Our journey to revolutionize African payments</p>
            <div class="roadmap-timeline">
                <div class="timeline-item">
                    <div class="timeline-date">Q3 2025</div>
                    <div class="timeline-content">
                        <h3>Token Launch & Initial Listings</h3>
                        <p>KLP token launch on Solana, DEX listings, community building, and initial partnerships with African exchanges.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-date">Q4 2025</div>
                    <div class="timeline-content">
                        <h3>Merchant Integration Platform</h3>
                        <p>Launch merchant payment gateway, e-commerce plugins, and onboard first 100 African businesses.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-date">2026</div>
                    <div class="timeline-content">
                        <h3>Remittance Pilot Program</h3>
                        <p>Deploy cross-border remittance corridors, mobile app launch, and expansion to 10 African countries.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- How to Buy Section -->
    <section class="section how-to-buy">
        <div class="container">
            <h2>How to Buy KLP</h2>
            <p class="section-subtitle">Simple steps to join the KaolaraPay ecosystem</p>
            <div class="how-to-buy-grid">
                <div class="step-card">
                    <div class="step-number">1</div>
                    <h3>Get Phantom Wallet</h3>
                    <p>Download and set up your Phantom wallet for Solana</p>
                </div>
                <div class="step-card">
                    <div class="step-number">2</div>
                    <h3>Buy SOL</h3>
                    <p>Purchase SOL from any major exchange or directly in Phantom</p>
                </div>
                <div class="step-card">
                    <div class="step-number">3</div>
                    <h3>Get Token Address</h3>
                    <p>Copy the official KLP token contract address (available at launch)</p>
                </div>
                <div class="step-card">
                    <div class="step-number">4</div>
                    <h3>Swap SOL for KLP</h3>
                    <p>Use Jupiter, Raydium, or other Solana DEX to swap SOL for KLP</p>
                </div>
                <div class="step-card">
                    <div class="step-number">5</div>
                    <h3>Join Community</h3>
                    <p>Connect with other holders in our Telegram and Discord channels</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Community Section -->
    <section class="section community">
        <div class="container">
            <h2>Join Our Community</h2>
            <p class="section-subtitle">Connect with thousands of KaolaraPay supporters worldwide</p>
            <div class="community-buttons">
                <a href="https://t.me/+w5NW8F9Vx3FhN2E0" class="social-btn telegram-btn" target="_blank">
                    <span>📱</span> Join Telegram
                </a>
                <a href="https://twitter.com/KaolaraPay" class="social-btn twitter-btn" target="_blank">
                    <span>🐦</span> Follow Twitter
                </a>
            </div>
            <div class="email-signup" id="whitelist">
                <input type="email" class="email-input" placeholder="Enter your email for whitelist">
                <button class="btn btn-primary">Join Whitelist</button>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h4>KaolaraPay</h4>
                    <a href="#hero">Home</a>
                    <a href="#problem">Problem</a>
                    <a href="#solution">Solution</a>
                    <a href="#roadmap">Roadmap</a>
                </div>
                <div class="footer-section">
                    <h4>Community</h4>
                    <a href="https://t.me/+w5NW8F9Vx3FhN2E0" target="_blank">Telegram</a>
                    <a href="https://twitter.com/KaolaraPay" target="_blank">Twitter</a>
                    <a href="#whitelist">Whitelist</a>
                </div>
                <div class="footer-section">
                    <h4>Contact</h4>
                    <a href="mailto:info@kaolarapay.com">info@kaolarapay.com</a>
                    <a href="https://kaolara.com" target="_blank">Kaolara Brand</a>
                </div>
            </div>
            <div class="disclaimer">
                <p><strong>Disclaimer:</strong> KaolaraPay (KLP) is a utility token. This is not financial advice. Cryptocurrency investments carry risk. Please do your own research before investing. Token launch subject to regulatory compliance.</p>
            </div>
        </div>
    </footer>

    <script>
        // Countdown Timer
        function startCountdown() {
            let totalSeconds = 48 * 60 * 60; // 48 hours in seconds
            
            function updateDisplay() {
                const hours = Math.floor(totalSeconds / 3600);
                const minutes = Math.floor((totalSeconds % 3600) / 60);
                const seconds = totalSeconds % 60;
                
                const display = `${hours.toString().padStart(2, '0')}:${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
                document.getElementById('countdown-display').textContent = display;
                
                if (totalSeconds > 0) {
                    totalSeconds--;
                } else {
                    document.getElementById('countdown-display').textContent = "LIVE NOW!";
                    document.getElementById('countdown-display').style.color = "#00E676";
                    clearInterval(countdownInterval);
                }
            }
            
            updateDisplay(); // Initial display
            const countdownInterval = setInterval(updateDisplay, 1000);
        }

        // Start countdown when page loads
        startCountdown();

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Email signup functionality
        document.querySelector('.email-signup button').addEventListener('click', function() {
            const email = document.querySelector('.email-input').value;
            if (email && email.includes('@')) {
                alert('Thank you for joining the KaolaraPay whitelist! We\'ll notify you about the launch.');
                document.querySelector('.email-input').value = '';
            } else {
                alert('Please enter a valid email address.');
            }
        });

        // Add loading animations
        window.addEventListener('load', function() {
            document.querySelectorAll('.feature-card, .step-card, .problem-card').forEach((card, index) => {
                card.style.opacity = '0';
                card.style.transform = 'translateY(20px)';
                setTimeout(() => {
                    card.style.transition = 'all 0.6s ease';
                    card.style.opacity = '1';
                    card.style.transform = 'translateY(0)';
                }, index * 100);
            });
        });
    </script>
</body>
</html>
