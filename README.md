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

        h1 {
            text-align: center;
            color: #FF6B6B;
            font-size: 2.5em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }

        h3 {
            text-align: center;
            color: #45B7D1;
            margin-bottom: 30px;
        }

        .flying-plane {
            position: absolute;
            top: -50px;
            right: -100px;
            width: 500px;
            height: auto;
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

        .form-group {
            margin-bottom: 20px;
            background: #fff;
            padding: 15px;
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s;
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
        }

        .delete-btn:hover {
            background: #ffe5e5;
            transform: scale(1.1);
        }

        .delete-btn.animate-removal {
            animation: fadeOut 0.5s forwards;
        }

        @keyframes fadeOut {
            from {
                opacity: 1;
                transform: translateY(0);
            }
            to {
                opacity: 0;
                transform: translateY(-20px);
            }
        }

        input, select {
            width: 100%;
            padding: 12px;
            border: 2px solid #E0E7FF;
            border-radius: 10px;
            font-size: 16px;
            background: #F8FAFF;
        }

        button {
            width: 100%;
            padding: 12px;
            border: none;
            border-radius: 10px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            background: linear-gradient(45deg, #FF6B6B, #FF8E53);
            color: white;
        }

        footer {
            text-align: center;
            margin-top: 30px;
            color: #666;
            font-size: 0.9em;
        }

        @media (max-width: 600px) {
            .container {
                padding: 20px;
                margin: 10px;
            }

            .flying-plane {
                width: 300px;
                top: -30px;
                right: -50px;
            }

            h1 {
                font-size: 1.5em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>ลงทะเบียนวันเด็กแห่งชาติ</h1>
        <h3>ณ ศูนย์การฝึกกองทัพอากาศน้ำพอง จังหวัดขอนแก่น ปี 2568</h3>

        <img class="flying-plane" src="https://via.placeholder.com/500x200" alt="เครื่องบินลอย">

        <form id="registrationForm">
            <div class="form-group">
                <label for="parentName">👨‍👩‍👧‍👦 ชื่อ-นามสกุลผู้ปกครอง</label>
                <input type="text" id="parentName" placeholder="กรุณากรอกชื่อ-นามสกุล" required>
            </div>

            <div class="form-group">
                <label for="parentPhone">📱 เบอร์โทรศัพท์</label>
                <input type="tel" id="parentPhone" placeholder="กรุณากรอกเบอร์โทรศัพท์" required>
            </div>

            <div id="childrenContainer"></div>
            <button type="button" onclick="addChild()">➕ เพิ่มข้อมูลเด็ก</button>
        </form>
    </div>

    <footer>© 2568 งานวันเด็กแห่งชาติ | ศูนย์ฝึกกองทัพอากาศน้ำพอง จังหวัดขอนแก่น</footer>

    <script>
        let childCount = 0;

        function addChild() {
            childCount++;
            const container = document.getElementById('childrenContainer');
            const childDiv = document.createElement('div');
            childDiv.className = 'form-group';
            childDiv.id = `child-${childCount}`;
            childDiv.innerHTML = `
                <label>👶 ชื่อเด็กคนที่ ${childCount}</label>
                <input type="text" placeholder="กรุณากรอกชื่อเด็ก" required>
                <button class="delete-btn" onclick="removeChild(${childCount})">❌</button>
            `;
            container.appendChild(childDiv);
        }

        function removeChild(id) {
            const childDiv = document.getElementById(`child-${id}`);
            if (childDiv) {
                const deleteButton = childDiv.querySelector('.delete-btn');
                deleteButton.classList.add('animate-removal');
                setTimeout(() => childDiv.remove(), 500);
            }
        }
    </script>
</body>
</html>

