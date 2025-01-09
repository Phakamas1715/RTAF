<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ลงทะเบียนวันเด็กแห่งชาติ ประจำปี 2568 จังหวัดขอนแก่น</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600&display=swap');
        
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

        .large-plane {
            position: absolute;
            top: -50px;
            right: -100px;
            width: 400px;
            height: auto;
            z-index: 1;
            animation: floatPlane 6s ease-in-out infinite;
        }

        @keyframes floatPlane {
            0%, 100% {
                transform: translate(0, 0) rotate(-5deg);
            }
            50% {
                transform: translate(-20px, -20px) rotate(0deg);
            }
        }

        .motto-container {
            margin: 30px 0;
            padding: 20px;
            background: linear-gradient(135deg, #fff5f5 0%, #e6f7ff 100%);
            border-radius: 15px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        .motto-box {
            text-align: center;
            padding: 20px;
            border: 2px dashed #FF6B6B;
            border-radius: 10px;
        }

        .motto-box h2 {
            color: #FF6B6B;
            font-size: 1.5em;
            margin: 0;
            line-height: 1.5;
        }

        .motto-year {
            color: #45B7D1;
            margin-top: 10px;
            font-style: italic;
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

        .child-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
        }

        .delete-btn {
            background: none;
            border: none;
            color: #ff4444;
            font-size: 1.2em;
            cursor: pointer;
            padding: 5px;
            border-radius: 50%;
            transition: all 0.3s;
            width: auto;
            margin: 0;
        }

        .delete-btn:hover {
            background: #ffe5e5;
            transform: scale(1.1);
        }

        .delete-icon {
            display: inline-block;
            transition: transform 0.3s;
        }

        .delete-btn:hover .delete-icon {
            transform: rotate(15deg);
        }

        input, select {
            width: 100%;
            padding: 12px;
            border: 2px solid #E0E7FF;
            border-radius: 10px;
            font-size: 16px;
            transition: all 0.3s;
            background: #F8FAFF;
            margin-bottom: 10px;
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

        .loading-spinner {
            width: 50px;
            height: 50px;
            border: 5px solid #f3f3f3;
            border-top: 5px solid #FF6B6B;
            border-radius: 50%;
            animation: spin 1s linear infinite;
            margin: 20px auto;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .registration-id {
            background: #f8f9fa;
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
        }

        .id-number {
            font-size: 2em;
            font-weight: bold;
            color: #4169E1;
            letter-spacing: 3px;
            margin: 10px 0;
            padding: 10px;
            background: white;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        @media (max-width: 768px) {
            .container {
                padding: 20px;
                margin: 10px;
            }

            .large-plane {
                width: 200px;
                top: -30px;
                right: -50px;
            }

            h1 {
                font-size: 1.5em;
            }

            .motto-box h2 {
                font-size: 1.2em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- เครื่องบินใหญ่ -->
        <svg class="large-plane" viewBox="0 0 800 400">
            <defs>
                <linearGradient id="planeGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                    <stop offset="0%" style="stop-color:#4169E1;stop-opacity:1" />
                    <stop offset="100%" style="stop-color:#45B7D1;stop-opacity:1" />
                </linearGradient>
            </defs>
            <g transform="translate(100,100) scale(2)">
                <path d="M180 100 C 190 90, 220 85, 240 90 L 280 100 L 290 95 C 300 90, 320 88, 330 90 L 340 95 L 350 90 L 370 92 L 360 98 L 340 100 L 330 105 C 320 110, 300 112, 290 110 L 280 105 L 240 115 C 220 120, 190 115, 180 105 Z" 
                      fill="url(#planeGradient)"/>
                <path d="M290 92 L 300 80 L 320 78 L 310 92" fill="#4169E1"/>
                <path d="M240 108 L 250 120 L 270 122 L 260 108" fill="#4169E1"/>
                <circle cx="200" cy="100" r="8" fill="#333"/>
                <circle cx="320" cy="95" r="6" fill="#333"/>
            </g>
        </svg>

        <h1 class="animate__animated animate__bounceIn">ลงทะเบียนวันเด็กแห่งชาติ</h1>
        <h3 class="animate__animated animate__fadeIn">ณ ศูนย์การฝึกกองทัพอากาศน้ำพอง จังหวัดขอนแก่น ปี 2568</h3>

        <div class="motto-container animate__animated animate__fadeIn">
            <div class="motto-box">
                <h2>"ทุกโอกาส คือ การเรียนรู้ พร้อมปรับตัวสู่อนาคตที่เลือกเอง"</h2>
                <p class="motto-year">- คำขวัญวันเด็กแห่งชาติ ประจำปี 2568 -</p>
            </div>
        </div>

        <form id="registrationForm">
            <div class="form-group animate__animated animate__fadeInUp">
                <label>👨‍👩‍👧‍👦 ชื่อ-นามสกุลผู้ปกครอง</label>
                <input type="text" id="parentName" name="parentName" placeholder="กรุณากรอกชื่อ-นามสกุล" required>
            </div>

            <div class="form-group animate__animated animate__fadeInUp">
                <label>📱 เบอร์โทรศัพท์</label>
                <input type="tel" id="parentPhone" name="parentPhone" placeholder="กรุณากรอกเบอร์โทรศัพท์" required>
            </div>

            <div class="form-group animate__animated animate__fadeInUp">
                <label>🏠 ที่อยู่</label>
                <input type="text" id="address" name="address" placeholder="บ้านเลขที่ / หมู่" required>
            </div>

            <div class="form-group animate__animated animate__fadeInUp">
                <label>📍 ตำบล</label>
                <input type="text" id="subdistrict" name="subdistrict" placeholder="กรุณากรอกตำบล" required>
            </div>

            <div class="form-group animate__animated animate__fadeInUp">
                <label>🌎 อำเภอ</label>
                <select id="district" name="district" required>
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
            <button type="submit">📝 ลงทะเบียน</button>
        </form>

        <div id="loading" style="display: none;">
            <div class="loading-spinner"></div>
            <p>กำลังบันทึกข้อมูล...</p>
        </div>

        <div id="result" style="display: none;"></div>
    </div>

    <script>
        let childCount = 0;

        function addChild() {
            childCount++;
            const childDiv = document.createElement('div');
            childDiv.className = 'form-group child-entry animate__animated animate__fadeInUp';
            childDiv.id = `child-${childCount}`;
            childDiv.innerHTML = `
                <div class="child-header">
                    <label>👶 ข้อมูลเด็กคนที่ ${childCount}</label>
                    <button type="button" class="delete-btn" onclick="deleteChild(${childCount})">
                        <span class="delete-icon">🗑️</span>
                    </button>
                </div>
                <input type="text" name="childName[]" placeholder="
