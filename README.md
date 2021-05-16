<h1>About The Project</h1>
<b>ชื่อโครงงาน : Parking Automatic <img src="https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width="30px"><br> 
ชนิดของโครงงาน : Micro-controller</b><br>
&emsp;&emsp;โปรเจคนี้มีจุดประสงค์เพื่อ พัฒนาระบบการจัดการลานจอดรถได้ใช้อุปกรณ์ไมโครคอนโทรเลอร์ Arduino และเซนเซอร์ IR Sensor ตรวจจับแสดงผ่านหน้าจอแสดงผลเพื่อทําให้ประหยัดเวลาในการ วนหาที่จอด 
และช่วยลดค่าใช้จ่ายอันเนื่องมาจากการสูญเสียพลังงานเชื้อเพลิงหรือมลพิษที่เพิ่มขึ้น โดยใช้ เซนเซอร์ในการรับค่าสถานะของช่องจอดรถเพื่อส่งไปแสดงผลจากการทดสอบพบว่าระบบสามารถที่จะ ตรวจสอบสถานะว่างหรือไม่ว่างของเซนเซอร์ภายในลานจอดรถพร้อมส่งค่าไปยังฐานข้อมูลเพื่อแสดงผลผ่านทาง หน้าจอแสดงผล
    
<h3>ที่มาและความสำคัญของโครงงาน</h3>
&emsp;&emsp;เนื่องจากปัจจุบันได้เกิดปัญหาการให้บริการสถานที่จอดรถ ของสถานที่ต่างๆ เช่น สถานที่ราชการ โรงพยาบาล คอนโดมิเนียม ห้างสรรพสินค้า เกิดขึ้นเนื่องจากพื้นที่ที่จอด รถของแต่ละอาคารนั้น ๆ ผู้ที่มาใช้บริการไม่สามารถทราบตําแหน่งที่ว่างของลานจอดรถได้แน่ชัด ส่งผลให้ผู้ที่มา ใช้บริการต้องเสียเวลาและสูญเสียพลังงานเชื้อเพลิงในการขับรถเพื่อหาที่ว่างช่องต่อไป

<h3>คุณลักษณะ</h3>
&emsp;ระบบนี้สามารถนําไปใช้เพื่ออํานวยความสะดวกสบายได้กับหลายๆลานจอดรถ ทั้ง ในห้างสรรพสินค้า โรงแรม โรงเรียน และ สถานที่อื่นๆที่มีลานจอดรถระบบนี้สามารถนําไปพัฒนาต่อได้โดยสามารถเพิ่มให้มี ระบบการจองที่จอดรถหรือทําแอพพลิเคชั่นการจองที่จอดรถได้และเพิ่มข้อมูลของลูกค้าที่เข้ามาจองสามารถ
เก็บข้อมูลบันทึกสถิติของลูกค้า

<h3>ประโยชน์</h3>
&emsp;- สามารถใช้บริการได้รับความสะดวกและรวดเร็ว<br>
&emsp;- สามารถหาที่จอดรถได้ง่ายโดยมองหาช่องจอดจากจอแสดงผล<br>
&emsp;- สามารถนำไปประยุกต์ใช้ในสถานประกอบการหรือหน่วยงานอื่นได้<br>
&emsp;- สามารถสร้างโปรแกรมที่ใช้จำลองแสดงสถานะช่องที่จอดรถ<br>
&emsp;- นำระบบ Sensor IR Infrared ประยุกต์ใช้ในการตรวจจับรถ<br>
<h3>อุปกรณ์ Arduino</h3>
1. Arduino Uno 1 ตัว
<img src="https://github.com/phufarpsw/project.car-parking/blob/main/img/arduino.jpeg" width="200px">
2. Solderless Breadboard 1 อัน
<img src="https://github.com/phufarpsw/project.car-parking/blob/main/img/board.jpg" width="200px">
3. 16×2 LCD Display 1 อัน
<img src="https://github.com/phufarpsw/project.car-parking/blob/main/img/lcd.jpeg" width="200px">
4. Infrared sensor 2 อัน
<img src="https://github.com/phufarpsw/project.car-parking/blob/main/img/infrared.jpeg" width="200px">
5. Male to Male Jumper Wires 15 เส้น
<img src="https://github.com/phufarpsw/project.car-parking/blob/main/img/wire.jpg" width="200px">
6. Resistor 4.7k , 1k , 100R อย่างละอัน
<img src="https://github.com/phufarpsw/project.car-parking/blob/main/img/resister100.jpeg" width="200px">
<h3>หลักการทำงานของโครงงาน</h3>
&emsp;&emsp;เมื่อมีรถขับเข้ามาในลานจอดรถ เซ็นเซอร์ตรงทางเข้า-ออกฝั่งด้านนอกลานจอดและฝั่งด้านในลานจอดจะตรวจจับรถได้ตามลำดับเพื่อระบบ
จะได้รู้ว่าเป็นรถที่ขับเข้ามาในลานจอด  หากมีรถขับออกมาจากลานจอดรถ เซ็นเซอร์ตรงทางเข้า-ออกฝั่งด้านในลานจอดและฝั่งด้านนอกลานจอดจะตรวจจับรถได้ตามลำดับ
 เพื่อระบบจะได้รู้ว่าเป็นรถที่ขับออกมาจากลานจอด เซ็นเซอร์จะส่งข้อมูลไปที่บอร์ด arduino จากนั้นบอร์ดจะประมวลผลว่าเป็นรถเข้าหรือออกเเละส่งข้อมูลไปแสดงผลที่จอ LCD
 เมื่อมีรถเข้ามาขณะที่ลาดจอดเต็ม จอ LCD จะแสดงว่า  “Sorry not Space”<br><br>
<center><table>
    <tr>
        <th><img src="https://github.com/phufarpsw/project.car-parking/blob/main/img/1.jpg" width="400px"></th>
        <th><img src="https://github.com/phufarpsw/project.car-parking/blob/main/img/2.jpg" width="400px"></th>
    </tr>
    <tr>
        <th><img src="https://github.com/phufarpsw/project.car-parking/blob/main/img/3.jpg" width="400px"></th>
        <th><img src="https://github.com/phufarpsw/project.car-parking/blob/main/img/4.jpg" width="400px"></th>
    </tr>
</table></center>
<h3>โปสเตอร์</h3>
<img src="https://github.com/phufarpsw/project.car-parking/blob/main/img/poster1.png" width="100%">
<h1>สมาชิกในกลุ่ม</h1>
<table>
    <tr>
        <th><img src="https://github.com/phufarpsw/project.car-parking/blob/main/img/p.jpg" width="400" height="250">นายณัชพล  นันทสันติ        63070049</th> 
        <th><img src="https://github.com/phufarpsw/project.car-parking/blob/main/img/jeng.jpg" width="400" height="250">นายณัฐดนัย วัฒพฤติไพศาล    63070051</th>
        <th><img src="https://github.com/phufarpsw/project.car-parking/blob/main/img/mild.jpg" width="400" height="250">นายธนวิชญ์ ลักษณะ         63070077</th> 
        <th><img src="https://github.com/phufarpsw/project.car-parking/blob/main/img/phufa.jpg" width="400" height="250">นายภูฟ้า    รุจิภาสวัฒน์      63070137</th> 
    </tr>
</table>
