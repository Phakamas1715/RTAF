<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ลงทะเบียนวันเด็กแห่งชาติ 2568 | ศูนย์การฝึกกองทัพอากาศน้ำพอง</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        /* เพิ่ม Animation สำหรับท้องฟ้าและเมฆ */
        @keyframes floatingClouds {
            0% { transform: translateX(0); }
            100% { transform: translateX(100%); }
        }

        @keyframes twinkle {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }

        body {
            font-family: 'Kanit', sans-serif;
            margin: 0;
            padding: 0;
            min-height: 100vh;
            background: linear-gradient(180deg, #87CEEB 0%, #E0F7FA 100%);
            position: relative;
            overflow-x: hidden;
        }

        .cloud {
            position: absolute;
            width: 100px;
            opacity: 0.8;
            animation: floatingClouds 20s linear infinite;
        }

        .cloud:nth-child(1) { top: 10%; left: 10%; animation-delay: 0s; }
        .cloud:nth-child(2) { top: 20%; left: 30%; animation-delay: -5s; }
        .cloud:nth-child(3) { top: 15%; left: 50%; animation-delay: -10s; }

        .star {
            position: absolute;
            width: 4px;
            height: 4px;
            background: #FFD700;
            border-radius: 50%;
            animation: twinkle 1.5s infinite;
        }

        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 30px;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            position: relative;
            z-index: 1;
        }

        .header-banner {
            text-align: center;
            padding: 20px;
            margin-bottom: 30px;
            background: linear-gradient(135deg, #FF9A9E 0%, #FAD0C4 100%);
            border-radius: 15px;
            color: white;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
        }

        .childrens-day-motto {
            font-size: 1.5em;
            text-align: center;
            color: #FF6B6B;
            margin: 20px 0;
            padding: 15px;
            background: #FFF5F5;
            border-radius: 10px;
            border: 2px dashed #FFB6C1;
        }

        /* Form Styling */
        .form-section {
            background: white;
            padding: 20px;
            border-radius: 15px;
            margin-bottom: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
        }

        .form-section h3 {
            color: #4A90E2;
            margin-bottom: 15px;
        }

        .input-group {
            margin-bottom: 15px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            color: #2C3E50;
            font-weight: 500;
        }

        input, select {
            width: 100%;
            padding: 12px;
            border: 2px solid #E0E7FF;
            border-radius: 8px;
            font-size: 16px;
            font-family: 'Kanit', sans-serif;
        }

        input:focus, select:focus {
            outline: none;
            border-color: #4A90E2;
            box-shadow: 0 0 0 3px rgba(74, 144, 226, 0.1);
        }

        .submit-button {
            background: linear-gradient(45deg, #4A90E2, #5C6BC0);
            color: white;
            padding: 15px 30px;
            border: none;
            border-radius: 10px;
            font-size: 18px;
            font-weight: 600;
            cursor: pointer;
            width: 100%;
            margin-top: 20px;
            transition: transform 0.2s;
        }

        .submit-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        /* Activity Cards */
        .activities-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .activity-card {
            background: white;
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
            display: flex;
            align-items: center;
            gap: 10px;
            transition: transform 0.2s;
        }

        .activity-card:hover {
            transform: translateY(-2px);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .container {
                margin: 10px;
                padding: 15px;
            }

            .activities-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Cloud Elements -->
    <div class="cloud">☁️</div>
    <div class="cloud">☁️</div>
    <div class="cloud">☁️</div>

    <div class="container animate__animated animate__fadeIn">
        <div class="header-banner animate__animated animate__bounceIn">
            <h1>ลงทะเบียนวันเด็กแห่งชาติ ประจำปี 2568</h1>
            <h2>ศูนย์การฝึกกองทัพอากาศน้ำพอง จังหวัดขอนแก่น</h2>
        </div>

        <div class="childrens-day-motto animate__animated animate__fadeInUp">
            "ทุกโอกาส คือ การเรียนรู้ พร้อมปรับตัวสู่อนาคตที่เลือกเอง"
        </div>

        <form id="registrationForm" onsubmit="handleSubmit(event)">
            <div class="form-section animate__animated animate__fadeInLeft">
                <h3>📝 ข้อมูลผู้ปกครอง</h3>
                <div class="input-group">
                    <label>ชื่อ-นามสกุล</label>
                    <input type="text" name="parentName" required>
                </div>
                <div class="input-group">
                    <label>เบอร์โทรศัพท์</label>
                    <input type="tel" name="parentPhone" required>
                </div>
            </div>

            <div class="form-section animate__animated animate__fadeInRight">
                <h3>🏠 ที่อยู่</h3>
                <div class="input-group">
                    <label>บ้านเลขที่/หมู่</label>
                    <input type="text" name="address" required>
                </div>
                <div class="input-group">
                    <label>ตำบล</label>
                    <input type="text" name="subdistrict" required>
                </div>
                <div class="input-group">
                    <label>อำเภอ</label>
                    <select name="district" required>
                        <option value="" disabled selected>- เลือกอำเภอ -</option>
                        <option value="เมืองขอนแก่น">เมืองขอนแก่น</option>
                        <option value="น้ำพอง">น้ำพอง</option>
                        <option value="กระนวน">กระนวน</option>
                        <option value="เขาสวนกวาง">เขาสวนกวาง</option>
                        <option value="อุบลรัตน์">อุบลรัตน์</option>
                    </select>
                </div>
            </div>

            <div id="childrenContainer" class="form-section animate__animated animate__fadeInUp">
                <h3>👶 ข้อมูลเด็ก</h3>
                <!-- Child entries will be added here dynamically -->
            </div>

            <button type="button" onclick="addChild()" class="submit-button" style="background: linear-gradient(45deg, #66BB6A, #43A047);">
                + เพิ่มข้อมูลเด็ก
            </button>

            <button type="submit" class="submit-button animate__animated animate__pulse">
                ลงทะเบียน
            </button>
        </form>
    </div>

    <script>
        let childCount = 0;

        function addChild() {
            childCount++;
            const childDiv = document.createElement('div');
            childDiv.className = 'input-group animate__animated animate__fadeIn';
            childDiv.innerHTML = `
                <h4>เด็กคนที่ ${childCount}</h4>
                <div class="input-group">
                    <label>ชื่อ-นามสกุล</label>
                    <input type="text" name="childName[]" required>
                </div>
                <div class="input-group">
                    <label>อายุ</label>
                    <input type="number" name="childAge[]" min="1" max="15" required>
                </div>
                <div class="input-group">
                    <label>เพศ</label>
                    <select name="childGender[]" required>
                        <option value="" disabled selected>- เลือกเพศ -</option>
                        <option value="ชาย">ชาย</option>
                        <option value="หญิง">หญิง</option>
                    </select>
                </div>
            `;
            document.getElementById('childrenContainer').appendChild(childDiv);
        }

        function handleSubmit(event) {
            event.preventDefault();
            const form = event.target;
            const formData = new FormData(form);

            // ส่งข้อมูลไปยัง Google Script
            fetch('https://script.google.com/macros/s/AKfycbzZ1eqfp-EoDJgN7PEWJtRaqPQa6t4azGiyyxCyWHTiHNU-47h6KhgfA0hWE8VAt9_8/exec', {
                method: 'POST',
                body: formData
            })
            .then(response => response.json())
            .then(data => {
                alert('ลงทะเบียนสำเร็จ! กรุณาเก็บหลักฐานการลงทะเบียนไว้');
                form.reset();
                window.location.reload();
            })
            .catch(error => {
                alert('เกิดข้อผิดพลาด กรุณาลองใหม่อีกครั้ง');
                console.error('Error:', error);
            });
        }
    </script>
</body>
</html>
