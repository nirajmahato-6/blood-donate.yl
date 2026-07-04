<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blood Donation - A Blessing & Gift of Life</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Header with Blessing */
        .blessing-header {
            background: linear-gradient(135deg, #e74c3c 0%, #c0392b 100%);
            color: white;
            padding: 60px 20px;
            text-align: center;
            border-radius: 20px;
            margin-bottom: 40px;
            box-shadow: 0 20px 60px rgba(231, 76, 60, 0.4);
            position: relative;
            overflow: hidden;
        }

        .blessing-header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="20" cy="20" r="2" fill="white" opacity="0.1"/><circle cx="80" cy="30" r="2" fill="white" opacity="0.1"/><circle cx="90" cy="80" r="2" fill="white" opacity="0.1"/><circle cx="10" cy="90" r="2" fill="white" opacity="0.1"/></svg>');
            opacity: 0.3;
        }

        .blessing-header h1 {
            font-size: 3.5em;
            margin-bottom: 20px;
            text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.3);
            position: relative;
            z-index: 1;
        }

        .blessing-text {
            font-size: 1.4em;
            line-height: 1.8;
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
            font-style: italic;
            opacity: 0.95;
        }

        .blessing-quote {
            font-size: 1.2em;
            background: rgba(255, 255, 255, 0.2);
            padding: 20px;
            border-left: 5px solid white;
            border-radius: 5px;
            margin-top: 20px;
            position: relative;
            z-index: 1;
        }

        /* Blessings Section */
        .blessings-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-bottom: 40px;
        }

        .blessing-card {
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
            border-top: 5px solid #e74c3c;
            transition: all 0.3s;
            text-align: center;
        }

        .blessing-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.2);
        }

        .blessing-icon {
            font-size: 4em;
            margin-bottom: 15px;
        }

        .blessing-card h3 {
            color: #e74c3c;
            font-size: 1.5em;
            margin-bottom: 15px;
        }

        .blessing-card p {
            color: #555;
            line-height: 1.8;
            font-size: 1.05em;
        }

        /* Impact Section */
        .impact-section {
            background: white;
            padding: 40px;
            border-radius: 15px;
            margin-bottom: 40px;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
        }

        .impact-section h2 {
            color: #e74c3c;
            font-size: 2.5em;
            text-align: center;
            margin-bottom: 40px;
        }

        .impact-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .impact-stat {
            background: linear-gradient(135deg, #e74c3c 0%, #c0392b 100%);
            color: white;
            padding: 30px;
            border-radius: 10px;
            text-align: center;
        }

        .impact-stat .number {
            font-size: 3em;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .impact-stat .label {
            font-size: 1.1em;
            opacity: 0.95;
        }

        .impact-content {
            background: #f8f9fa;
            padding: 30px;
            border-radius: 10px;
            border-left: 5px solid #e74c3c;
        }

        .impact-content h3 {
            color: #e74c3c;
            margin-bottom: 15px;
            font-size: 1.3em;
        }

        .impact-list {
            list-style: none;
            margin-bottom: 20px;
        }

        .impact-list li {
            padding: 12px 0;
            border-bottom: 1px solid #ddd;
            color: #555;
            line-height: 1.6;
        }

        .impact-list li:before {
            content: "❤️ ";
            margin-right: 10px;
            color: #e74c3c;
        }

        /* Stories Section */
        .stories-section {
            background: white;
            padding: 40px;
            border-radius: 15px;
            margin-bottom: 40px;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
        }

        .stories-section h2 {
            color: #e74c3c;
            font-size: 2.5em;
            text-align: center;
            margin-bottom: 40px;
        }

        .stories-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
        }

        .story-card {
            background: #f8f9fa;
            padding: 25px;
            border-radius: 10px;
            border-left: 5px solid #e74c3c;
        }

        .story-card h4 {
            color: #e74c3c;
            margin-bottom: 10px;
            font-size: 1.2em;
        }

        .story-card p {
            color: #555;
            line-height: 1.7;
        }

        /* Benefits Section */
        .benefits-section {
            background: linear-gradient(135deg, #e74c3c 0%, #c0392b 100%);
            color: white;
            padding: 40px;
            border-radius: 15px;
            margin-bottom: 40px;
            box-shadow: 0 15px 40px rgba(231, 76, 60, 0.4);
        }

        .benefits-section h2 {
            font-size: 2.5em;
            text-align: center;
            margin-bottom: 40px;
        }

        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .benefit-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 10px;
            border: 2px solid rgba(255, 255, 255, 0.3);
        }

        .benefit-item h4 {
            font-size: 1.2em;
            margin-bottom: 10px;
        }

        .benefit-item p {
            opacity: 0.95;
            line-height: 1.6;
        }

        /* Call to Action */
        .cta-section {
            background: white;
            padding: 50px 40px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
            margin-bottom: 40px;
        }

        .cta-section h2 {
            color: #e74c3c;
            font-size: 2.5em;
            margin-bottom: 20px;
        }

        .cta-section p {
            color: #555;
            font-size: 1.2em;
            margin-bottom: 30px;
            line-height: 1.8;
        }

        .cta-buttons {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        .cta-btn {
            padding: 15px 30px;
            font-size: 1.1em;
            font-weight: bold;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .cta-btn-primary {
            background: linear-gradient(135deg, #e74c3c 0%, #c0392b 100%);
            color: white;
        }

        .cta-btn-primary:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(231, 76, 60, 0.4);
        }

        .cta-btn-secondary {
            background: #f0f0f0;
            color: #e74c3c;
            border: 2px solid #e74c3c;
        }

        .cta-btn-secondary:hover {
            background: #e74c3c;
            color: white;
        }

        /* Footer */
        .footer {
            background: white;
            padding: 40px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
        }

        .footer h3 {
            color: #e74c3c;
            font-size: 1.5em;
            margin-bottom: 20px;
        }

        .footer-blessing {
            font-size: 1.2em;
            color: #555;
            line-height: 2;
            margin-bottom: 20px;
            font-style: italic;
        }

        .footer-contact {
            background: #f8f9fa;
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
        }

        .footer-contact p {
            color: #666;
            margin-bottom: 8px;
        }

        /* Animations */
        @keyframes heartbeat {
            0%, 100% {
                transform: scale(1);
            }
            25% {
                transform: scale(1.1);
            }
            50% {
                transform: scale(1);
            }
        }

        .heart-icon {
            display: inline-block;
            animation: heartbeat 1.5s ease-in-out infinite;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .blessing-header h1 {
                font-size: 2.2em;
            }

            .blessing-text {
                font-size: 1.1em;
            }

            .impact-section h2,
            .stories-section h2,
            .benefits-section h2,
            .cta-section h2 {
                font-size: 1.8em;
            }

            .impact-stat .number {
                font-size: 2em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Blessing Header -->
        <div class="blessing-header">
            <h1>🩸 A Gift of Life - Blood Donation Blessing 🩸</h1>
            <div class="blessing-text">
                <p>Every drop of blood you donate is a blessing to humanity.</p>
                <p>You become an angel of hope for someone in need.</p>
                <p class="heart-icon">❤️</p>
            </div>
            <div class="blessing-quote">
                "The gift of blood is the gift of life itself. When you donate blood, you're not just giving a fluid - you're giving someone the chance to live, to love, and to dream."
            </div>
        </div>

        <!-- Blessings Section -->
        <section class="blessings-grid">
            <div class="blessing-card">
                <div class="blessing-icon">🙏</div>
                <h3>Divine Blessing</h3>
                <p>Your donation is a divine act of compassion. In many spiritual traditions, saving a life is considered the highest form of blessing and merit.</p>
            </div>

            <div class="blessing-card">
                <div class="blessing-icon">❤️</div>
                <h3>Love in Action</h3>
                <p>Blood donation is love made visible. You're expressing the deepest form of human compassion - the willingness to give without expecting anything in return.</p>
            </div>

            <div class="blessing-card">
                <div class="blessing-icon">⭐</div>
                <h3>Be a Hero</h3>
                <p>You become a real-life hero. Your single donation can save up to 3 lives. That's the power of your kindness and generosity.</p>
            </div>

            <div class="blessing-card">
                <div class="blessing-icon">🌟</div>
                <h3>Eternal Impact</h3>
                <p>The impact of your donation extends beyond a single moment. You create a ripple of hope that touches lives for years to come.</p>
            </div>

            <div class="blessing-card">
                <div class="blessing-icon">💪</div>
                <h3>Strength to Others</h3>
                <p>Your blood gives strength to the weak, hope to the hopeless, and life to those fighting for survival. You are their strength.</p>
            </div>

            <div class="blessing-card">
                <div class="blessing-icon">🤝</div>
                <h3>Unity & Compassion</h3>
                <p>Blood donation connects humanity. It breaks barriers of caste, creed, and religion. It's a pure act of human brotherhood.</p>
            </div>
        </section>

        <!-- Impact Section -->
        <section class="impact-section">
            <h2>The Power of Your Blessing</h2>
            
            <div class="impact-stats">
                <div class="impact-stat">
                    <div class="number">3</div>
                    <div class="label">Lives Saved Per Donation</div>
                </div>
                <div class="impact-stat">
                    <div class="number">42 Days</div>
                    <div class="label">Red Blood Cell Survival</div>
                </div>
                <div class="impact-stat">
                    <div class="number">450 ml</div>
                    <div class="label">Blood Per Donation</div>
                </div>
                <div class="impact-stat">
                    <div class="number">100%</div>
                    <div class="label">Replenished in Body</div>
                </div>
            </div>

            <div class="impact-content">
                <h3>Why Your Blood Donation Matters</h3>
                <ul class="impact-list">
                    <li>Can save the life of a newborn baby fighting for survival</li>
                    <li>Can give a second chance to accident victims and trauma patients</li>
                    <li>Can help cancer patients undergoing chemotherapy continue their battle</li>
                    <li>Can assist emergency surgeries and critical care situations</li>
                    <li>Can support patients with blood disorders and hemophilia</li>
                    <li>Can be a lifeline during natural disasters and medical emergencies</li>
                    <li>Improves your own health through regular health checkups</li>
                    <li>Stimulates your bone marrow to produce new blood cells</li>
                </ul>
            </div>
        </section>

        <!-- Stories Section -->
        <section class="stories-section">
            <h2>Stories of Hope & Gratitude</h2>
            
            <div class="stories-grid">
                <div class="story-card">
                    <h4>A Mother's Gratitude</h4>
                    <p>"My newborn daughter needed blood transfusion due to severe anemia. The blood donor's gift gave her a healthy childhood. That donor is my family's hero, and we pray blessings upon them every day."</p>
                </div>

                <div class="story-card">
                    <h4>From the Accident Ward</h4>
                    <p>"After a severe car accident, I lost consciousness and needed immediate blood transfusion. Unknown donors saved my life. I've made it my mission to give back and donate blood regularly."</p>
                </div>

                <div class="story-card">
                    <h4>Cancer Survivor's Journey</h4>
                    <p>"During my chemotherapy, I received multiple blood transfusions. Each unit of blood was a soldier fighting alongside me against cancer. Today, I'm cancer-free, and I donate to help others win their battles too."</p>
                </div>

                <div class="story-card">
                    <h4>Emergency Hero</h4>
                    <p>"During an emergency childbirth complication, my wife needed blood immediately. Without blood donors, I would have lost my wife and child. Blood donors are literal angels on earth."</p>
                </div>

                <div class="story-card">
                    <h4>Young Warrior's Hope</h4>
                    <p>"As a teenager with thalassemia, I depend on regular blood transfusions. Each donor is a guardian angel. I'm grateful beyond words for their sacrifice and hope."</p>
                </div>

                <div class="story-card">
                    <h4>Disaster Relief</h4>
                    <p>"When the earthquake struck, blood donors came forward like never before. The massive coordination of donors saved hundreds of lives. It restored my faith in humanity."</p>
                </div>
            </div>
        </section>

        <!-- Benefits Section -->
        <section class="benefits-section">
            <h2>Blessings You Also Receive</h2>
            
            <div class="benefits-grid">
                <div class="benefit-item">
                    <h4>✓ Health Benefits</h4>
                    <p>Regular blood donation reduces risk of heart disease, maintains hemoglobin levels, and stimulates production of new blood cells.</p>
                </div>

                <div class="benefit-item">
                    <h4>✓ Free Health Checkup</h4>
                    <p>Before each donation, you receive a free health screening including blood pressure, hemoglobin, and disease tests.</p>
                </div>

                <div class="benefit-item">
                    <h4>✓ Spiritual Fulfillment</h4>
                    <p>The joy of knowing you saved someone's life brings immense spiritual satisfaction and peace of mind.</p>
                </div>

                <div class="benefit-item">
                    <h4>✓ Community Recognition</h4>
                    <p>Become a valued member of the blood donor community and receive recognition for your service to humanity.</p>
                </div>

                <div class="benefit-item">
                    <h4>✓ Tax Benefits</h4>
                    <p>In many countries, blood donors receive tax exemptions and special privileges as appreciated citizens.</p>
                </div>

                <div class="benefit-item">
                    <h4>✓ Peace of Mind</h4>
                    <p>Sleep knowing that your blood is saving lives, reducing accidents, and providing emergency relief.</p>
                </div>
            </div>
        </section>

        <!-- Call to Action -->
        <section class="cta-section">
            <h2>Become an Angel of Hope Today</h2>
            <p>
                Your blood is precious. Your donation is a blessing. Join millions of blood donors worldwide who are 
                saving lives, giving hope, and creating miracles every single day. 
                <br><br>
                <span class="heart-icon">❤️</span>
                One donation. Three lives. Infinite blessings.
                <span class="heart-icon">❤️</span>
            </p>
            
            <div class="cta-buttons">
                <button class="cta-btn cta-btn-primary">📍 Find Donation Center</button>
                <button class="cta-btn cta-btn-primary">📋 Register as Donor</button>
                <button class="cta-btn cta-btn-secondary">📞 Contact Us</button>
                <button class="cta-btn cta-btn-secondary">ℹ️ Learn More</button>
            </div>
        </section>

        <!-- Footer with Final Blessing -->
        <section class="footer">
            <h3>The Donor's Blessing</h3>
            <div class="footer-blessing">
                <p>May you live a long and healthy life filled with joy and prosperity.</p>
                <p>May your generosity be rewarded with blessings beyond measure.</p>
                <p>May the lives you save hold you in their prayers forever.</p>
                <p>May you be remembered as a hero, a savior, and a beacon of hope.</p>
                <p>Thank you for being an angel on earth. 🙏❤️</p>
            </div>

            <div class="footer-contact">
                <p><strong>Emergency Blood Donation Hotline:</strong> 1800-180-1111</p>
                <p><strong>Red Cross Blood Bank:</strong> www.redcross.org</p>
                <p><strong>NBTC (National Blood Transfusion Council):</strong> Promoting blood donation across the nation</p>
                <p style="margin-top: 15px; color: #e74c3c; font-weight: bold;">
                    Every drop counts. Every donor matters. Every life saved is a blessing. 🩸❤️
                </p>
            </div>
        </section>
    </div>

    <script>
        // Interactive buttons
        document.querySelectorAll('.cta-btn').forEach(btn => {
            btn.addEventListener('click', function() {
                const action = this.textContent;
                if (action.includes('Find')) {
                    alert('🏥 Locating nearest blood donation centers...\n\nCheck your local Red Cross or hospital for donation drives.');
                } else if (action.includes('Register')) {
                    alert('📋 Thank you for your interest in registering as a blood donor!\n\nVisit your nearest blood bank or donation center to register.');
                } else if (action.includes('Contact')) {
                    alert('📞 Contact Information:\n\nEmergency Hotline: 1800-180-1111\n\nEmail: donate@bloodbank.org\n\nWe look forward to your donation!');
                } else if (action.includes('Learn')) {
                    alert('ℹ️ Blood Donation FAQs:\n\n✓ Donation frequency: Every 3 months\n✓ Minimum age: 18 years\n✓ Process time: 30-45 minutes\n✓ Health benefits: Reduced risk of heart disease\n✓ Eligibility: Check at donation center');
                }
            });
        });
