<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KLIZMO - Low Fidelity Wireframes</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px;
        }
        
        h1 {
            text-align: center;
            margin-bottom: 10px;
            color: #2c5234;
            font-size: 2.5em;
        }
        
        .subtitle {
            text-align: center;
            margin-bottom: 40px;
            color: #666;
            font-size: 1.1em;
        }
        
        .wireframe-section {
            margin-bottom: 60px;
        }
        
        .section-title {
            font-size: 1.8em;
            margin-bottom: 20px;
            color: #2c5234;
            border-bottom: 2px solid #4a7c59;
            padding-bottom: 10px;
        }
        
        .wireframe-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .phone-frame {
            width: 300px;
            height: 600px;
            background: white;
            border: 3px solid #333;
            border-radius: 25px;
            padding: 20px;
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
            position: relative;
            margin: 0 auto;
        }
        
        .screen-title {
            font-weight: bold;
            margin-bottom: 15px;
            text-align: center;
            color: #2c5234;
            font-size: 1.1em;
        }
        
        .wireframe-box {
            border: 2px solid #666;
            margin-bottom: 15px;
            padding: 10px;
            background: #fff;
        }
        
        .header {
            height: 40px;
            border: 2px solid #666;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 10px;
            font-weight: bold;
        }
        
        .nav-bar {
            height: 50px;
            border: 2px solid #666;
            position: absolute;
            bottom: 20px;
            left: 20px;
            right: 20px;
            display: flex;
            justify-content: space-around;
            align-items: center;
            background: white;
        }
        
        .nav-item {
            text-align: center;
            font-size: 0.8em;
            font-weight: bold;
        }
        
        .nav-item.active {
            background: #4a7c59;
            color: white;
            padding: 8px;
            border-radius: 4px;
        }
        
        .route-card {
            border: 2px solid #666;
            height: 120px;
            margin-bottom: 15px;
            padding: 10px;
            position: relative;
        }
        
        .route-image {
            width: 80px;
            height: 60px;
            border: 1px solid #666;
            float: left;
            margin-right: 10px;
            background: #f0f0f0;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8em;
        }
        
        .route-info {
            font-size: 0.9em;
            line-height: 1.4;
        }
        
        .stats-row {
            display: flex;
            justify-content: space-between;
            margin-top: 10px;
            font-size: 0.8em;
        }
        
        .search-bar {
            height: 40px;
            border: 2px solid #666;
            margin-bottom: 15px;
            padding: 0 10px;
            display: flex;
            align-items: center;
            background: #f9f9f9;
        }
        
        .filter-chips {
            display: flex;
            gap: 8px;
            margin-bottom: 15px;
            flex-wrap: wrap;
        }
        
        .chip {
            padding: 6px 12px;
            border: 1px solid #666;
            border-radius: 20px;
            font-size: 0.8em;
            background: white;
        }
        
        .chip.active {
            background: #4a7c59;
            color: white;
        }
        
        .map-container {
            height: 200px;
            border: 2px solid #666;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: #f0f0f0;
            color: #666;
            font-weight: bold;
        }
        
        .button {
            height: 45px;
            border: 2px solid #666;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            background: white;
            cursor: pointer;
        }
        
        .button.primary {
            background: #4a7c59;
            color: white;
            border-color: #4a7c59;
        }
        
        .ai-chat {
            border: 2px solid #666;
            height: 100px;
            margin-bottom: 15px;
            padding: 10px;
            background: #f9f9f9;
        }
        
        .chat-bubble {
            background: #e3f2fd;
            padding: 8px;
            margin-bottom: 5px;
            border-radius: 10px;
            font-size: 0.8em;
        }
        
        .user-bubble {
            background: #4a7c59;
            color: white;
            text-align: right;
            margin-left: 20px;
        }
        
        .persona-card {
            background: white;
            border: 2px solid #666;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 20px;
        }
        
        .persona-header {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }
        
        .persona-avatar {
            width: 60px;
            height: 60px;
            border: 2px solid #666;
            border-radius: 50%;
            margin-right: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: #f0f0f0;
        }
        
        .persona-name {
            font-size: 1.3em;
            font-weight: bold;
            color: #2c5234;
        }
        
        .persona-role {
            color: #666;
            font-size: 0.9em;
        }
        
        .persona-section {
            margin-bottom: 15px;
        }
        
        .persona-section h4 {
            font-weight: bold;
            margin-bottom: 8px;
            color: #4a7c59;
        }
        
        .flow-diagram {
            background: white;
            border: 2px solid #666;
            padding: 30px;
            border-radius: 10px;
            margin-bottom: 30px;
        }
        
        .flow-steps {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 20px;
        }
        
        .flow-step {
            flex: 1;
            min-width: 150px;
            text-align: center;
        }
        
        .flow-box {
            width: 100px;
            height: 100px;
            border: 2px solid #666;
            margin: 0 auto 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            background: #f9f9f9;
            border-radius: 10px;
        }
        
        .flow-arrow {
            font-size: 2em;
            color: #4a7c59;
            align-self: center;
        }
        
        .sketch-container {
            background: white;
            border: 2px solid #666;
            padding: 30px;
            border-radius: 10px;
            margin-bottom: 30px;
        }
        
        .sketch-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }
        
        .sketch-item {
            border: 1px solid #ccc;
            height: 150px;
            padding: 15px;
            background: #fafafa;
            border-radius: 5px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
        
        .sketch-title {
            font-weight: bold;
            margin-bottom: 10px;
            text-align: center;
        }
        
        .content-area {
            height: calc(100% - 140px);
            overflow-y: auto;
        }
        
        .badge {
            display: inline-block;
            padding: 4px 8px;
            background: #4a7c59;
            color: white;
            border-radius: 12px;
            font-size: 0.7em;
            margin: 2px;
        }
        
        .safety-indicator {
            background: #f44336;
        }
        
        .difficulty-easy {
            background: #4caf50;
        }
        
        .difficulty-medium {
            background: #ff9800;
        }
        
        .difficulty-hard {
            background: #f44336;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🚴‍♀️ KLIZMO</h1>
        <p class="subtitle">Low Fidelity Wireframes & Design Documentation</p>

        <!-- User Personas -->
        <div class="wireframe-section">
            <h2 class="section-title">👥 User Personas</h2>
            
            <div class="persona-card">
                <div class="persona-header">
                    <div class="persona-avatar">🏃‍♂️</div>
                    <div>
                        <div class="persona-name">Adventure Alex</div>
                        <div class="persona-role">Intermediate Cyclist</div>
                    </div>
                </div>
                <div class="persona-section">
                    <h4>Goals:</h4>
                    <p>• Discover challenging new routes with scenic views<br>
                    • Connect with local cycling community<br>
                    • Find routes that match fitness level progression</p>
                </div>
                <div class="persona-section">
                    <h4>Pain Points:</h4>
                    <p>• Existing apps too focused on competition<br>
                    • Hard to find routes with local context<br>
                    • Safety concerns on unfamiliar routes</p>
                </div>
                <div class="persona-section">
                    <h4>Behavior:</h4>
                    <p>• Rides 3-4 times per week<br>
                    • Uses smartphone during rides<br>
                    • Active on social media</p>
                </div>
            </div>

            <div class="persona-card">
                <div class="persona-header">
                    <div class="persona-avatar">🛡️</div>
                    <div>
                        <div class="persona-name">Safety Sarah</div>
                        <div class="persona-role">Beginner Cyclist</div>
                    </div>
                </div>
                <div class="persona-section">
                    <h4>Goals:</h4>
                    <p>• Find safe, well-lit routes for evening rides<br>
                    • Build confidence gradually<br>
                    • Connect with supportive community</p>
                </div>
                <div class="persona-section">
                    <h4>Pain Points:</h4>
                    <p>• Intimidated by advanced cycling apps<br>
                    • Needs clear safety information<br>
                    • Overwhelmed by too many features</p>
                </div>
                <div class="persona-section">
                    <h4>Behavior:</h4>
                    <p>• New to cycling, rides weekends<br>
                    • Prefers familiar neighborhoods<br>
                    • Values simple, clear interfaces</p>
                </div>
            </div>

            <div class="persona-card">
                <div class="persona-header">
                    <div class="persona-avatar">🏆</div>
                    <div>
                        <div class="persona-name">Pro Pete</div>
                        <div class="persona-role">Advanced Cyclist</div>
                    </div>
                </div>
                <div class="persona-section">
                    <h4>Goals:</h4>
                    <p>• Share expertise with cycling community<br>
                    • Track detailed performance metrics<br>
                    • Discover challenging training routes</p>
                </div>
                <div class="persona-section">
                    <h4>Pain Points:</h4>
                    <p>• Limited platforms for sharing local knowledge<br>
                    • Wants recognition for contributions<br>
                    • Needs advanced tracking features</p>
                </div>
                <div class="persona-section">
                    <h4>Behavior:</h4>
                    <p>• Daily rider, trains seriously<br>
                    • Uses multiple cycling apps<br>
                    • Active in local cycling groups</p>
                </div>
            </div>
        </div>

        <!-- User Journey Flow -->
        <div class="wireframe-section">
            <h2 class="section-title">🗺️ User Journey Flow</h2>
            
            <div class="flow-diagram">
                <h3 style="text-align: center; margin-bottom: 30px; color: #2c5234;">Route Discovery Journey</h3>
                <div class="flow-steps">
                    <div class="flow-step">
                        <div class="flow-box">🔍<br>Discover</div>
                        <p><strong>Browse Routes</strong><br>Search & filter by preferences</p>
                    </div>
                    <div class="flow-arrow">→</div>
                    <div class="flow-step">
                        <div class="flow-box">📋<br>Plan</div>
                        <p><strong>Route Details</strong><br>View map, stats, community notes</p>
                    </div>
                    <div class="flow-arrow">→</div>
                    <div class="flow-step">
                        <div class="flow-box">🚴‍♀️<br>Ride</div>
                        <p><strong>Track Activity</strong><br>GPS tracking, navigation, safety</p>
                    </div>
                    <div class="flow-arrow">→</div>
                    <div class="flow-step">
                        <div class="flow-box">📤<br>Share</div>
                        <p><strong>Post Experience</strong><br>Add photos, tips, rate route</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Sketches/Concepts -->
        <div class="wireframe-section">
            <h2 class="section-title">✏️ Initial Sketches & Concepts</h2>
            
            <div class="sketch-container">
                <div class="sketch-grid">
                    <div class="sketch-item">
                        <div class="sketch-title">Card-Based Discovery</div>
                        <p>Visual route cards with quick stats and community ratings</p>
                    </div>
                    <div class="sketch-item">
                        <div class="sketch-title">AI Chat Interface</div>
                        <p>Conversational route recommendations based on preferences</p>
                    </div>
                    <div class="sketch-item">
                        <div class="sketch-title">Safety-First Design</div>
                        <p>Prominent safety indicators and community warnings</p>
                    </div>
                    <div class="sketch-item">
                        <div class="sketch-title">Gamification Elements</div>
                        <p>Badge system and progress tracking without overwhelming UI</p>
                    </div>
                    <div class="sketch-item">
                        <div class="sketch-title">Local Context</div>
                        <p>Weather, events, and construction integrated into route info</p>
                    </div>
                    <div class="sketch-item">
                        <div class="sketch-title">Community Contributions</div>
                        <p>Easy ways to add photos, tips, and hazard warnings</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Main App Wireframes -->
        <div class="wireframe-section">
            <h2 class="section-title">📱 Low-Fidelity Wireframes</h2>
            
            <div class="wireframe-grid">
                <!-- Home/Discovery Screen -->
                <div class="phone-frame">
                    <div class="screen-title">Home - Route Discovery</div>
                    <div class="content-area">
                        <div class="header">
                            <span>☰</span>
                            <span>KLIZMO</span>
                            <span>👤</span>
                        </div>
                        
                        <div class="search-bar">🔍 Search routes...</div>
                        
                        <div class="filter-chips">
                            <span class="chip active">All</span>
                            <span class="chip">Easy</span>
                            <span class="chip">Scenic</span>
                            <span class="chip">< 10mi</span>
                        </div>
                        
                        <div class="route-card">
                            <div class="route-image">[IMG]</div>
                            <div class="route-info">
                                <strong>Coastal Trail Loop</strong><br>
                                <span class="badge difficulty-easy">Easy</span>
                                <span class="badge">Scenic</span><br>
                                ⭐ 4.8 (124 reviews)
                            </div>
                            <div class="stats-row">
                                <span>8.2 mi</span>
                                <span>200 ft ↗</span>
                                <span>45 min</span>
                            </div>
                        </div>
                        
                        <div class="route-card">
                            <div class="route-image">[IMG]</div>
                            <div class="route-info">
                                <strong>Hill Climb Challenge</strong><br>
                                <span class="badge difficulty-hard">Hard</span>
                                <span class="badge safety-indicator">⚠️ Construction</span><br>
                                ⭐ 4.5 (89 reviews)
                            </div>
                            <div class="stats-row">
                                <span>12.5 mi</span>
                                <span>800 ft ↗</span>
                                <span>1h 20m</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="nav-bar">
                        <div class="nav-item active">Discover</div>
                        <div class="nav-item">My Routes</div>
                        <div class="nav-item">Community</div>
                        <div class="nav-item">Profile</div>
                    </div>
                </div>

                <!-- Route Details Screen -->
                <div class="phone-frame">
                    <div class="screen-title">Route Details</div>
                    <div class="content-area">
                        <div class="header">
                            <span>←</span>
                            <span>Route Details</span>
                            <span>💾 ♡</span>
                        </div>
                        
                        <div class="map-container">
                            [ROUTE MAP]<br>
                            📍 Start/End Points
                        </div>
                        
                        <div class="wireframe-box">
                            <h3>Coastal Trail Loop</h3>
                            <p>⭐ 4.8 (124 reviews) | 📍 2.1 mi away</p>
                            <div style="margin: 10px 0;">
                                <span class="badge difficulty-easy">Easy</span>
                                <span class="badge">Scenic</span>
                                <span class="badge">Family-friendly</span>
                            </div>
                        </div>
                        
                        <div class="wireframe-box">
                            <strong>Stats:</strong><br>
                            🚴‍♀️ 8.2 miles | ⬆️ 200 ft elevation | ⏱️ 45 min avg<br>
                            🛣️ Paved trail | 🚦 3 traffic lights
                        </div>
                        
                        <div class="wireframe-box">
                            <strong>Recent Community Notes:</strong><br>
                            💬 "Beautiful ocean views!" - Alex, 2 days ago<br>
                            ⚠️ "Watch for pedestrians near mile 3" - Sarah, 1 week ago
                        </div>
                        
                        <div class="button primary">Start Navigation</div>
                        <div class="button">Save for Later</div>
                    </div>
                    
                    <div class="nav-bar">
                        <div class="nav-item">Discover</div>
                        <div class="nav-item">My Routes</div>
                        <div class="nav-item">Community</div>
                        <div class="nav-item">Profile</div>
                    </div>
                </div>

                <!-- AI Assistant Screen -->
                <div class="phone-frame">
                    <div class="screen-title">AI Route Assistant</div>
                    <div class="content-area">
                        <div class="header">
                            <span>←</span>
                            <span>Route Assistant</span>
                            <span>⚙️</span>
                        </div>
                        
                        <div class="ai-chat">
                            <div class="chat-bubble">
                                Hi! I'm your route assistant. What kind of ride are you looking for today?
                            </div>
                            <div class="chat-bubble user-bubble">
                                Something scenic, about 10 miles, not too hilly
                            </div>
                            <div class="chat-bubble">
                                Perfect! Based on your preferences and today's weather, I recommend the Bay Trail Loop. It's 9.8 miles with great water views and minimal elevation.
                            </div>
                        </div>
                        
                        <div class="wireframe-box">
                            <strong>🤖 Why this recommendation:</strong><br>
                            • Matches your 10-mile preference<br>
                            • Scenic bay views you've enjoyed before<br>
                            • Only 150ft elevation gain<br>
                            • Good weather conditions today
                        </div>
                        
                        <div class="route-card">
                            <div class="route-image">[IMG]</div>
                            <div class="route-info">
                                <strong>Bay Trail Loop</strong><br>
                                <span class="badge difficulty-easy">Easy</span>
                                <span class="badge">Scenic</span><br>
                                ⭐ 4.7 (156 reviews)
                            </div>
                            <div class="stats-row">
                                <span>9.8 mi</span>
                                <span>150 ft ↗</span>
                                <span>42 min</span>
                            </div>
                        </div>
                        
                        <div class="search-bar">💬 Ask for another recommendation...</div>
                    </div>
                    
                    <div class="nav-bar">
                        <div class="nav-item">Discover</div>
                        <div class="nav-item">My Routes</div>
                        <div class="nav-item">Community</div>
                        <div class="nav-item">Profile</div>
                    </div>
                </div>

                <!-- During Ride Screen -->
                <div class="phone-frame">
                    <div class="screen-title">Active Ride</div>
                    <div class="content-area">
                        <div class="header">
                            <span>🔋95%</span>
                            <span>RIDING</span>
                            <span>📶 GPS</span>
                        </div>
                        
                        <div class="map-container" style="height: 250px;">
                            [LIVE MAP]<br>
                            📍 Current Location<br>
                            📍 Next Turn: 0.3 mi
                        </div>
                        
                        <div class="wireframe-box">
                            <div style="display: flex; justify-content: space-between;">
                                <div>
                                    <strong>3.2 mi</strong><br>
                                    Distance
                                </div>
                                <div>
                                    <strong>18 mph</strong><br>
                                    Current Speed
                                </div>
                                <div>
                                    <strong>22:15</strong><br>
                                    Time
                                </div>
                            </div>
                        </div>
                        
                        <div class="wireframe-box" style="background: #fff3cd;">
                            <strong>⚠️ Community Alert:</strong><br>
                            Construction ahead at mile 4.2<br>
                            Use sidewalk for 200 yards
                        </div>
                        
                        <div style="display: flex; gap: 10px;">
                            <div class="button" style="flex: 1;">⏸️ Pause</div>
                            <div class="button" style="flex: 1;">📷 Photo</div>
                            <div class="button" style="flex: 1; background: #dc3545; color: white;">🛑 End</div>
                        </div>
                    </div>
                    
                    <div class="nav-bar">
                        <div class="nav-item">Discover</div>
                        <div class="nav-item active">My Routes</div>
                        <div class="nav-item">Community</div>
                        <div class="nav-item">Profile</div>
                    </div>
                </div>

                <!-- My Routes Screen -->
                <div class="phone-frame">
                    <div class="screen-title">My Routes</div>
                    <div class="content-area">
                        <div class="header">
                            <span>☰</span>
                            <span>My Routes</span>
                            <span>📊</span>
                        </div>
                        
                        <div class="filter-chips">
                            <span class="chip active">Recent</span>
                            <span class="chip">Saved</span>
                            <span class="chip">Completed</span>
                        </div>
                        
                        <div class="wireframe-box">
                            <h4>This Week's Progress</h4>
                            📈 3 routes completed | 🏆 2 new badges earned<br>
                            📊 Total: 28.6 miles | ⬆️ 1,200 ft elevation
                        </div>
                        
                        <div class="route-card">
                            <div class="route-image">[IMG]</div>
                            <div class="route-info">
                                <strong>Bay Trail Loop</strong><br>
                                <span style="color: #4caf50;">✅ Completed 2 hrs ago</span><br>
                                Your time: 38:45 (PR! 🎉)
                            </div>
                            <div class="stats-row">
                                <span>9.8 mi</span>
                                <span>18.2 mph avg</span>
                                <span>⭐ You rated: 5/5</span>
                            </div>
                        </div>
                        
                        <div class="route-card">
                            <div class="route-image">[IMG]</div>
                            <div class="route-info">
                                <strong>Hill Climb Challenge</strong><br>
                                <span style="color: #666;">💾 Saved for later</span><br>
                                Next free time: Tomorrow 6 PM
                            </div>
                            <div class="stats-row">
                                <span>12.5 mi</span>
                                <span>Est: 1h 15m</span>
                                <span>Difficulty: Hard</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="nav-bar">
                        <div class="nav-item">Discover</div>
                        <div class="nav-item active">My Routes</div>
                        <div class="nav-item">Community</div>
                        <div class="nav-item">Profile</div>
                    </div>
                </div>

                <!-- Community Screen -->
                <div class="phone-frame">
                    <div class="screen-title">Community</div>
                    <div class="content-area">
                        <div class="header">
                            <span>☰</span>
                            <span>Community</span>
                            <span>🔔</span>
                        </div>
                        
                        <div class="filter-chips">
                            <span class="chip active">Recent</span>
                            <span class="chip">Photos</span>
                            <span class="chip">Tips</span>
                            <span class
