<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ลงทะเบียนวันเด็กแห่งชาติ ประจำปี 2568 จังหวัดขอนแก่น</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600&display=swap');
        
        @keyframes flyPlane {
            0% { transform: translateX(-100%) translateY(0); }
            50% { transform: translateX(100%) translateY(-30px); }
            100% { transform: translateX(-100%) translateY(0); }
        }
        
        .flying-plane {
            position: absolute;
            top: 50px;
            left: 0;
            width: 200px;
            animation: flyPlane 15s linear infinite;
        }
        
        .kids-decoration {
            position: absolute;
            bottom: 20px;
            right: 20px;
            width: 200px;
        }
        
        body {
            font-family: 'Kanit', sans-serif;
            background: linear-gradient(135deg, #FFE5F1 0%, #C7EEFF 100%);
            color: #333;
            line-height: 1.6;
            margin: 0;
            padding: 20px;
            min-height: 100vh;
        }

        .container {
            max-width: 800px;
            margin: 20px auto;
            background: rgba(255, 255, 255, 0.95);
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 8px 32px rgba(0, 123, 255, 0.1);
            position: relative;
            overflow: hidden;
        }

        .container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 8px;
            background: linear-gradient(90deg, #FF6B6B, #4ECDC4, #45B7D1, #96C93D, #FED766);
        }

        h1 {
            text-align: center;
            color: #FF6B6B;
            font-size: 2em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }

        h3 {
            text-align: center;
            color: #45B7D1;
            margin-bottom: 30px;
        }

        .form-group {
            margin-bottom: 20px;
            background: #fff;
            padding: 15px;
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s;
        }

        .form-group:hover {
            transform: translateY(-2px);
        }

        label {
            display: block;
            font-weight: 500;
            color: #2C3E50;
            margin-bottom: 8px;
        }

        input, select {
            width: 100%;
            padding: 12px;
            border: 2px solid #E0E7FF;
            border-radius: 10px;
            font-size: 16px;
            transition: all 0.3s;
            background: #F8FAFF;
        }

        input:focus, select:focus {
            outline: none;
            border-color: #45B7D1;
            box-shadow: 0 0 0 3px rgba(69, 183, 209, 0.1);
        }

        button {
            width: 100%;
            padding: 12px;
            border: none;
            border-radius: 10px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            margin-top: 10px;
        }

        button[type="submit"] {
            background: linear-gradient(45deg, #FF6B6B, #FF8E53);
            color: white;
        }

        button[type="button"] {
            background: linear-gradient(45deg, #45B7D1, #4ECDC4);
            color: white;
        }

        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
        }

        #result {
            display: none;
            margin-top: 20px;
            padding: 20px;
            background: linear-gradient(135deg, #E8F5E9, #C8E6C9);
            border-radius: 12px;
            text-align: center;
            animation: fadeIn 0.5s ease-out;
        }

        #result h3 {
            color: #2E7D32;
            margin-bottom: 10px;
        }

        .activities-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
            margin-top: 10px;
        }

        .activity-item {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 10px;
            background: #f8faff;
            border-radius: 8px;
            transition: all 0.3s;
        }

        .activity-item:hover {
            background: #e8f0fe;
            transform: translateY(-2px);
        }

        .activity-item input[type="checkbox"] {
            width: 20px;
            height: 20px;
            cursor: pointer;
        }

        .activity-item label {
            margin: 0;
            cursor: pointer;
        }

        .rewards-info {
            margin-top: 30px;
            padding: 20px;
            background: linear-gradient(135deg, #fff5f5, #fff0f7);
            border-radius: 12px;
            border: 2px dashed #ff9ecd;
        }

        .rewards-info h4 {
            color: #ff6b6b;
            text-align: center;
            margin-bottom: 15px;
        }

        .reward-levels {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 15px 0;
        }

        .reward-item {
            text-align: center;
            padding: 15px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }

        .reward-item:hover {
            transform: translateY(-3px);
        }

        .reward-points {
            font-size: 1.2em;
            font-weight: bold;
            color: #4169e1;
            margin-bottom: 8px;
        }

        .reward-desc {
            color: #666;
        }

        .reward-note {
            text-align: center;
            font-size: 0.9em;
            color: #888;
            margin-top: 15px;
        }

        .decoration {
            position: absolute;
            font-size: 24px;
            animation: float 3s ease-in-out infinite;
        }

        .balloon1 { top: 20px; left: 20px; }
        .balloon2 { top: 40px; right: 20px; }
        .balloon3 { bottom: 20px; left: 30px; }
        .balloon4 { bottom: 40px; right: 30px; }

        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0); }
        }

        footer {
            text-align: center;
            margin-top: 30px;
            color: #666;
            font-size: 0.9em;
        }

        /* Responsive Design */
        @media (max-width: 600px) {
            .container {
                padding: 20px;
                margin: 10px;
            }

            h1 {
                font-size: 1.5em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- เพิ่ม SVG เครื่องบินและเด็กๆ -->
        <svg class="flying-plane" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 300">
            <g class="airplane">
                <path d="M180 100 C 190 90, 220 85, 240 90 L 280 100 L 290 95 C 300 90, 320 88, 330 90 L 340 95 L 350 90 L 370 92 L 360 98 L 340 100 L 330 105 C 320 110, 300 112, 290 110 L 280 105 L 240 115 C 220 120, 190 115, 180 105 Z" fill="#4169E1"/>
                <path d="M290 92 L 300 80 L 320 78 L 310 92" fill="#4169E1"/>
                <path d="M240 108 L 250 120 L 270 122 L 260 108" fill="#4169E1"/>
                <circle cx="200" cy="100" r="8" fill="#333"/>
                <circle cx="320" cy="95" r="6" fill="#333"/>
            </g>
        </svg>
        
        <svg class="kids-decoration" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 300">
            <g class="kids-group">
                <g class="boy">
                    <circle cx="100" cy="150" r="20" fill="#FFD700"/>
                    <path d="M85 170 L115 170 L110 200 L90 200 Z" fill="#FF6B6B"/>
                    <line x1="90" y1="180" x2="80" y2="195" stroke="#FF6B6B" stroke-width="4"/>
                    <line x1="110" y1="180" x2="120" y2="195" stroke="#FF6B6B" stroke-width="4"/>
                    <line x1="95" y1="200" x2="90" y2="220" stroke="#4169E1" stroke-width="4"/>
                    <line x1="105" y1="200" x2="110" y2="220" stroke="#4169E1" stroke-width="4"/>
                </g>
                <g class="girl">
                    <circle cx="150" cy="150" r="20" fill="#FFD700"/>
                    <path d="M135 140 Q150 120 165 140" fill="none" stroke="#333" stroke-width="3"/>
                    <path d="M135 170 L165 170 L160 210 L140 210 Z" fill="#FF9ECD"/>
                    <line x1="140" y1="180" x2="130" y2="195" stroke="#FF9ECD" stroke-width="4"/>
                    <line x1="160" y1="180" x2="170" y2="195" stroke="#FF9ECD" stroke-width="4"/>
                    <line x1="145" y1="210" x2="140" y2="230" stroke="#4169E1" stroke-width="4"/>
                    <line x1="155" y1="210" x2="160" y2="230" stroke="#4169E1" stroke-width="4"/>
                </g>
                <g class="waving-kid">
                    <circle cx="200" cy="150" r="20" fill="#FFD700"/>
                    <path d="M185 170 L215 170 L210 200 L190 200 Z" fill="#4ECDC4"/>
                    <path d="M215 180 Q225 170 235 180" stroke="#4ECDC4" stroke-width="4">
                        <animateTransform
                            attributeName="transform"
                            type="rotate"
                            values="0 215 180; 20 215 180; 0 215 180"
                            dur="2s"
                            repeatCount="indefinite"/>
                    </path>
                    <line x1="190" y1="180" x2="180" y2="195" stroke="#4ECDC4" stroke-width="4"/>
                    <line x1="195" y1="200" x2="190" y2="220" stroke="#4169E1" stroke-width="4"/>
                    <line x1="205" y1="200" x2="210" y2="220" stroke="#4169E1" stroke-width="4"/>
                </g>
            </g>
        </svg>
        
        <span class="decoration balloon1">🎈</span>
        <span class="decoration balloon2">🎈</span>
        <span class="decoration balloon3">🎈</span>
        <span class="decoration balloon4">🎈</span>

        <h1 class="animate__animated animate__bounceIn">ลงทะเบียนวันเด็กแห่งชาติ</h1>
        <h3 class="animate__animated animate__fadeIn">ณ ศูนย์การฝึกกองทัพอากาศน้ำพอง จังหวัดขอนแก่น ปี 2568</h3>

        <!-- เพิ่มคำขวัญวันเด็ก 2568 -->
        <h2 class="animate__animated animate__fadeInUp" style="text-align: center; color: #FF8C00; margin-bottom: 20px;">
            ทุกโอกาส คือ การเรียนรู้ พร้อมปรับตัวสู่อนาคตที่เลือกเอง
        </h2>

        <form id="registrationForm">
            <div class="form-group animate__animated animate__fadeInUp">
                <label for="parentName">👨‍👩‍👧‍👦 ชื่อ-นามสกุลผู้ปกครอง</label>
                <input type="text" id="parentName" placeholder="กรุณากรอกชื่อ-นามสกุล" required>
            </div>

            <div class="form-group animate__animated animate__fadeInUp">
                <label for="parentPhone">📱 เบอร์โทรศัพท์</label>
                <input type="tel" id="parentPhone" placeholder="กรุณากรอกเบอร์โทรศัพท์" required>
            </div>

            <div class="form-group animate__animated animate__fadeInUp">
                <label for="address">🏠 ที่อยู่</label>
                <input type="text" id="address" placeholder="บ้านเลขที่ / หมู่" required>
            </div>

            <div class="form-group animate__animated animate__fadeInUp">
                <label for="subdistrict">📍 ตำบล</label>
                <input type="text" id="subdistrict" placeholder="กรุณากรอกตำบล" required>
            </div>

            <div class="form-group animate__animated animate__fadeInUp">
                <label for="district">🌎 อำเภอ</label>
                <select id="district" required>
                    <option value="" disabled selected>เลือกอำเภอ</option>
                    <option value="เมืองขอนแก่น">เมืองขอนแก่น</option>
                    <option value="น้ำพอง">น้ำพอง</option>
                    <option value="กระนวน">กระนวน</option>
                    <option value="เขาสวนกวาง">เขาสวนกวาง</option>
                    <option value="อุบลรัตน์">อุบลรัตน์</option>
                </select>
            </div>

            <div id="childrenContainer"></div>
            <button type="button" onclick="addChild()">➕ เพิ่มข้อมูลเด็ก</button>

            <div class="form-group animate__animated animate__fadeInUp">
                <label>🎮 กิจกรรมที่สนใจ (เลือกได้หลายกิจกรรม)</label>
                <div class="activities-grid">
                    <div class="activity-item">
                        <input type="checkbox" id="activity1" name="activities" value="balloon">
                        <label for="activity1">🎯 ยิงเป้าลูกโป่ง (10 คะแนน)</label>
                    </div>
                    <div class="activity-item">
                        <input type="checkbox" id="activity2" name="activities" value="ball">
                        <label for="activity2">🎳 ปาลูกบอลใส่กระป๋อง (10 คะแนน)</label>
                    </div>
                    <div class="activity-item">
                        <input type="checkbox" id="activity3" name="activities" value="plane">
                        <label for="activity3">✈️ พับเครื่องบินกระดาษ (10 คะแนน)</label>
                    </div>
                    <div class="activity-item">
                        <input type="checkbox" id="activity4" name="activities" value="tug">
                        <label for="activity4">🏃 ชักเย่อ (20 คะแนน)</label>
                    </div>
                    <div class="activity-item">
                        <input type="checkbox" id="activity5" name="activities" value="quiz">
                        <label for="activity5">❓ ตอบคำถาม (20 คะแนน)</label>
                    </div>
                    <div class="activity-item">
                        <input type="checkbox" id="activity6" name="activities" value="firstaid">
                        <label for="activity6">🏥 การปฐมพยาบาลเบื้องต้น (20 คะแนน)</label>
                    </div>
                </div>
            </div>

            <div class="rewards-info animate__animated animate__fadeInUp">
                <h4>🎁 เงื่อนไขการแลกรางวัล</h4>
                <div class="reward-levels">
                    <div class="reward
