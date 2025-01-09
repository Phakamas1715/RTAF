<!-- ...existing code... -->
<h4 class="animate__animated animate__fadeIn">ทุกโอกาส คือ การเรียนรู้ พร้อมปรับตัวสู่อนาคตที่เลือกเอง</h4>
<!-- ...existing code... -->
<script>
    // ...existing code...
    resultDiv.innerHTML = `
        <h3 style="text-align: center; color: #4169E1; margin-bottom: 20px;">
            ลงทะเบียนสำเร็จ!
        </h3>
        <div class="uid-warning">
            ⚠️ โปรดจดจำหรือบันทึกภาพหน้าจอรหัสของท่าน
            เพื่อยืนยันตัวตน ⚠️
        </div>
        ${allRegistrations.map((reg, index) => `
            <div class="uid-card">
                <h4>บัตรประจำตัวผู้เข้าร่วมงานวันเด็กแห่งชาติ 2568</h4>
                <div class="uid-number">${reg.uid}</div>
                <div class="uid-info">
                    <strong>ผู้ปกครอง:</strong> ${reg.parentName}<br>
                    <strong>เบอร์โทร:</strong> ${reg.parentPhone}
                </div>
                <div class="uid-info">
                    <strong>เด็ก:</strong> ${reg.childName}<br>
                    <strong>อายุ:</strong> ${reg.childAge} ปี
                </div>
                <div class="uid-footer">
                    ณ ศูนย์การฝึกกองทัพอากาศน้ำพอง จังหวัดขอนแก่น<br>
                    วันเสาร์ที่ 11 มกราคม 2568
                </div>
            </div>
        `).join('')}
    `;
    // ...existing code...
</script>
