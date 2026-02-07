<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine's Week 💕</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Cormorant+Garamond:wght@300;400;600&display=swap');
        
        :root {
            --rose: #FF6B9D;
            --deep-rose: #C73866;
            --blush: #FFE5EC;
            --cream: #FFF8F0;
            --wine: #8B2E5A;
            --gold: #D4AF37;
            --shadow: rgba(199, 56, 102, 0.2);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Cormorant Garamond', serif;
            background: linear-gradient(135deg, var(--cream) 0%, var(--blush) 50%, #FFD6E8 100%);
            color: var(--wine);
            overflow-x: hidden;
            min-height: 100vh;
            position: relative;
        }
        
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                radial-gradient(circle at 20% 30%, rgba(255, 107, 157, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 70%, rgba(255, 182, 193, 0.15) 0%, transparent 50%),
                radial-gradient(circle at 50% 50%, rgba(255, 229, 236, 0.2) 0%, transparent 70%);
            pointer-events: none;
            z-index: 0;
        }
        
        .floating-hearts {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
            overflow: hidden;
        }
        
        .heart {
            position: absolute;
            font-size: 20px;
            opacity: 0;
            animation: float 15s infinite ease-in-out;
        }
        
        @keyframes float {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 0.6;
            }
            90% {
                opacity: 0.6;
            }
            100% {
                transform: translateY(-10vh) rotate(360deg);
                opacity: 0;
            }
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
            position: relative;
            z-index: 2;
        }
        
        header {
            text-align: center;
            margin-bottom: 60px;
            animation: fadeInDown 1s ease-out;
        }
        
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        h1 {
            font-family: 'Playfair Display', serif;
            font-size: 4.5rem;
            font-weight: 700;
            color: var(--deep-rose);
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px var(--shadow);
            letter-spacing: -1px;
        }
        
        .subtitle {
            font-size: 1.5rem;
            color: var(--wine);
            font-style: italic;
            font-weight: 300;
        }
        
        .week-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }
        
        .day-card {
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 10px 30px var(--shadow);
            border: 2px solid rgba(255, 107, 157, 0.2);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            opacity: 0;
            animation: fadeInUp 0.6s ease-out forwards;
            position: relative;
            overflow: hidden;
        }
        
        .day-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255, 107, 157, 0.1) 0%, transparent 70%);
            opacity: 0;
            transition: opacity 0.4s ease;
        }
        
        .day-card:hover::before {
            opacity: 1;
        }
        
        .day-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 20px 50px var(--shadow);
            border-color: var(--rose);
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .day-card:nth-child(1) { animation-delay: 0.1s; }
        .day-card:nth-child(2) { animation-delay: 0.2s; }
        .day-card:nth-child(3) { animation-delay: 0.3s; }
        .day-card:nth-child(4) { animation-delay: 0.4s; }
        .day-card:nth-child(5) { animation-delay: 0.5s; }
        .day-card:nth-child(6) { animation-delay: 0.6s; }
        .day-card:nth-child(7) { animation-delay: 0.7s; }
        
        .day-number {
            position: absolute;
            top: 15px;
            right: 15px;
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--rose), var(--deep-rose));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 600;
            font-size: 1.2rem;
            box-shadow: 0 4px 10px var(--shadow);
        }
        
        .day-icon {
            font-size: 3rem;
            margin-bottom: 15px;
            display: inline-block;
            animation: pulse 2s ease-in-out infinite;
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }
        
        .day-title {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            font-weight: 600;
            color: var(--deep-rose);
            margin-bottom: 10px;
        }
        
        .day-date {
            font-size: 1.1rem;
            color: var(--rose);
            margin-bottom: 15px;
            font-style: italic;
        }
        
        .day-description {
            font-size: 1.15rem;
            line-height: 1.6;
            color: var(--wine);
            margin-bottom: 20px;
        }
        
        .ideas-section {
            border-top: 2px solid var(--blush);
            padding-top: 15px;
        }
        
        .ideas-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.3rem;
            font-weight: 600;
            color: var(--wine);
            margin-bottom: 10px;
        }
        
        .ideas-list {
            list-style: none;
        }
        
        .ideas-list li {
            padding: 8px 0 8px 25px;
            position: relative;
            font-size: 1.05rem;
            line-height: 1.5;
        }
        
        .ideas-list li::before {
            content: '♥';
            position: absolute;
            left: 0;
            color: var(--rose);
            font-size: 1.2rem;
        }
        
        .bonus-section {
            background: linear-gradient(135deg, rgba(255, 107, 157, 0.2), rgba(255, 182, 193, 0.3));
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin-top: 40px;
            border: 2px solid var(--rose);
            box-shadow: 0 10px 40px var(--shadow);
            animation: fadeInUp 0.8s ease-out 0.8s backwards;
        }
        
        .bonus-title {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--deep-rose);
            text-align: center;
            margin-bottom: 30px;
        }
        
        .couples-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
        }
        
        .couple-idea {
            background: white;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .couple-idea:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(199, 56, 102, 0.3);
        }
        
        .couple-idea-icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
            display: block;
        }
        
        .couple-idea h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            color: var(--deep-rose);
            margin-bottom: 10px;
        }
        
        .couple-idea p {
            font-size: 1.1rem;
            line-height: 1.5;
            color: var(--wine);
        }
        
        footer {
            text-align: center;
            padding: 40px 20px;
            font-size: 1.2rem;
            color: var(--wine);
            font-style: italic;
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 3rem;
            }
            
            .subtitle {
                font-size: 1.2rem;
            }
            
            .week-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="floating-hearts" id="hearts"></div>
    
    <div class="container">
        <header>
            <h1>Valentine's Week</h1>
            <p class="subtitle">Seven Days of Love & Romance</p>
        </header>
        
        <div class="week-container">
            <div class="day-card">
                <div class="day-number">1</div>
                <div class="day-icon">🌹</div>
                <h2 class="day-title">Rose Day</h2>
                <p class="day-date">February 7th</p>
                <p class="day-description">Begin the week by expressing your love with beautiful roses. Different colors convey different emotions - red for love, pink for admiration, yellow for friendship.</p>
                <div class="ideas-section">
                    <h3 class="ideas-title">Sweet Ideas:</h3>
                    <ul class="ideas-list">
                        <li>Create a trail of rose petals leading to a surprise</li>
                        <li>Give a single rose with a heartfelt note each hour</li>
                        <li>Make rose-infused treats together</li>
                        <li>Plant a rose bush as a lasting symbol</li>
                    </ul>
                </div>
            </div>
            
            <div class="day-card">
                <div class="day-number">2</div>
                <div class="day-icon">🍫</div>
                <h2 class="day-title">Propose Day</h2>
                <p class="day-date">February 8th</p>
                <p class="day-description">Whether it's a proposal for marriage or simply proposing your love and commitment, today is about taking your relationship to the next level.</p>
                <div class="ideas-section">
                    <h3 class="ideas-title">Sweet Ideas:</h3>
                    <ul class="ideas-list">
                        <li>Write a letter expressing your future dreams together</li>
                        <li>Create a scavenger hunt ending with your proposal</li>
                        <li>Recreate your first date before proposing</li>
                        <li>Plan a surprise proposal at a meaningful location</li>
                    </ul>
                </div>
            </div>
            
            <div class="day-card">
                <div class="day-number">3</div>
                <div class="day-icon">🍫</div>
                <h2 class="day-title">Chocolate Day</h2>
                <p class="day-date">February 9th</p>
                <p class="day-description">Indulge in the sweetness of chocolate, the universal symbol of love and affection. Share delicious treats with your sweetheart.</p>
                <div class="ideas-section">
                    <h3 class="ideas-title">Sweet Ideas:</h3>
                    <ul class="ideas-list">
                        <li>Make homemade chocolates together</li>
                        <li>Visit a chocolate tasting experience</li>
                        <li>Create a chocolate fondue night at home</li>
                        <li>Exchange boxes with meaningful messages inside</li>
                    </ul>
                </div>
            </div>
            
            <div class="day-card">
                <div class="day-number">4</div>
                <div class="day-icon">🧸</div>
                <h2 class="day-title">Teddy Day</h2>
                <p class="day-date">February 10th</p>
                <p class="day-description">Gift a cuddly teddy bear as a soft reminder of your warm and comforting love. Teddies symbolize the comfort and security in your relationship.</p>
                <div class="ideas-section">
                    <h3 class="ideas-title">Sweet Ideas:</h3>
                    <ul class="ideas-list">
                        <li>Choose a teddy that matches their personality</li>
                        <li>Record a voice message in a talking teddy</li>
                        <li>Have a cozy movie night with all your stuffed friends</li>
                        <li>Create matching teddy bears for both of you</li>
                    </ul>
                </div>
            </div>
            
            <div class="day-card">
                <div class="day-number">5</div>
                <div class="day-icon">💝</div>
                <h2 class="day-title">Promise Day</h2>
                <p class="day-date">February 11th</p>
                <p class="day-description">Make meaningful promises to your partner and strengthen your bond. Commit to supporting, loving, and cherishing each other.</p>
                <div class="ideas-section">
                    <h3 class="ideas-title">Sweet Ideas:</h3>
                    <ul class="ideas-list">
                        <li>Write promises on decorative cards to keep</li>
                        <li>Create a promise jar to open throughout the year</li>
                        <li>Exchange promise rings or bracelets</li>
                        <li>Make a video of your promises to each other</li>
                    </ul>
                </div>
            </div>
            
            <div class="day-card">
                <div class="day-number">6</div>
                <div class="day-icon">💑</div>
                <h2 class="day-title">Hug Day</h2>
                <p class="day-date">February 12th</p>
                <p class="day-description">Embrace your loved one with warm, comforting hugs. Physical touch is a powerful way to show love and create emotional connection.</p>
                <div class="ideas-section">
                    <h3 class="ideas-title">Sweet Ideas:</h3>
                    <ul class="ideas-list">
                        <li>Give 20-second hugs throughout the day</li>
                        <li>Create a "hug coupon" book for future redemptions</li>
                        <li>Have a cozy blanket fort cuddle session</li>
                        <li>Surprise them with unexpected hugs all day</li>
                    </ul>
                </div>
            </div>
            
            <div class="day-card">
                <div class="day-number">7</div>
                <div class="day-icon">💋</div>
                <h2 class="day-title">Kiss Day</h2>
                <p class="day-date">February 13th</p>
                <p class="day-description">The day before Valentine's, celebrate with sweet kisses. Express your affection through this intimate gesture of love.</p>
                <div class="ideas-section">
                    <h3 class="ideas-title">Sweet Ideas:</h3>
                    <ul class="ideas-list">
                        <li>Leave lipstick kiss marks with love notes</li>
                        <li>Recreate your first kiss location</li>
                        <li>Play a kissing booth game at home</li>
                        <li>Count kisses throughout the day</li>
                    </ul>
                </div>
            </div>
        </div>
        
        <div class="bonus-section">
            <h2 class="bonus-title">✨ Extra Romantic Ideas for Couples ✨</h2>
            <div class="couples-grid">
                <div class="couple-idea">
                    <span class="couple-idea-icon">🌃</span>
                    <h3>Stargazing Night</h3>
                    <p>Pack a blanket, some snacks, and head to a quiet spot to watch the stars together while sharing your dreams.</p>
                </div>
                
                <div class="couple-idea">
                    <span class="couple-idea-icon">🎨</span>
                    <h3>Paint Together</h3>
                    <p>Take a couples painting class or set up canvases at home and create art for each other.</p>
                </div>
                
                <div class="couple-idea">
                    <span class="couple-idea-icon">🍳</span>
                    <h3>Cooking Challenge</h3>
                    <p>Cook a romantic dinner together trying a new recipe from a cuisine you both love.</p>
                </div>
                
                <div class="couple-idea">
                    <span class="couple-idea-icon">📸</span>
                    <h3>Photo Adventure</h3>
                    <p>Go on a photography walk and capture beautiful moments together in your favorite places.</p>
                </div>
                
                <div class="couple-idea">
                    <span class="couple-idea-icon">🎵</span>
                    <h3>Playlist Exchange</h3>
                    <p>Create playlists for each other with songs that remind you of your relationship and listen together.</p>
                </div>
                
                <div class="couple-idea">
                    <span class="couple-idea-icon">💌</span>
                    <h3>Love Letters</h3>
                    <p>Write heartfelt letters to each other describing your favorite memories and future hopes.</p>
                </div>
                
                <div class="couple-idea">
                    <span class="couple-idea-icon">🏡</span>
                    <h3>Indoor Picnic</h3>
                    <p>Set up a cozy picnic in your living room with fairy lights, your favorite foods, and good conversation.</p>
                </div>
                
                <div class="couple-idea">
                    <span class="couple-idea-icon">🎭</span>
                    <h3>Memory Lane</h3>
                    <p>Look through old photos and videos together, reminiscing about your journey as a couple.</p>
                </div>
            </div>
        </div>
        
        <footer>
            <p>May your week be filled with love, laughter, and unforgettable moments 💕</p>
        </footer>
    </div>
    
    <script>
        // Create floating hearts
        function createHearts() {
            const heartsContainer = document.getElementById('hearts');
            const heartSymbols = ['💕', '💖', '💗', '💝', '❤️', '💓'];
            
            for (let i = 0; i < 20; i++) {
                const heart = document.createElement('div');
                heart.className = 'heart';
                heart.textContent = heartSymbols[Math.floor(Math.random() * heartSymbols.length)];
                heart.style.left = Math.random() * 100 + '%';
                heart.style.animationDelay = Math.random() * 15 + 's';
                heart.style.animationDuration = (15 + Math.random() * 10) + 's';
                heartsContainer.appendChild(heart);
            }
        }
        
        // Add hover effect to day cards
        document.addEventListener('DOMContentLoaded', () => {
            createHearts();
            
            const cards = document.querySelectorAll('.day-card');
            cards.forEach(card => {
                card.addEventListener('mouseenter', () => {
                    const icon = card.querySelector('.day-icon');
                    icon.style.transform = 'scale(1.2) rotate(10deg)';
                });
                
                card.addEventListener('mouseleave', () => {
                    const icon = card.querySelector('.day-icon');
                    icon.style.transform = 'scale(1) rotate(0deg)';
                });
            });
            
            // Smooth scroll behavior
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        target.scrollIntoView({
                            behavior: 'smooth',
                            block: 'start'
                        });
                    }
                });
            });
        });
        
        // Add parallax effect to floating hearts
        document.addEventListener('mousemove', (e) => {
            const hearts = document.querySelectorAll('.heart');
            const x = e.clientX / window.innerWidth;
            const y = e.clientY / window.innerHeight;
            
            hearts.forEach((heart, index) => {
                const speed = (index % 3 + 1) * 0.5;
                const xMove = (x - 0.5) * speed * 20;
                const yMove = (y - 0.5) * speed * 20;
                heart.style.transform = `translate(${xMove}px, ${yMove}px)`;
            });
        });
    </script>
</body>
</html>
