# FX5U-NodeRed

วิธีเชื่อมต่อ FX5U PLC Mitsubishi เข้ากับ Node-red ด้วย MC Protocol

1. ตั้งค่า PLC FX5U 
Parameter > FX5UCPU > Module Parameter เลือก Ethernet Port
![image](https://user-images.githubusercontent.com/67640462/232580400-d6b3f9fd-c0a0-4dc5-8734-13f6835a45fb.png)

2.ตั้งค่า IP Address ของ PLC
![image](https://user-images.githubusercontent.com/67640462/232581671-6e2e569b-cb50-4be8-97ea-a80e28a45f35.png)

3.ตั้งค่า External Device Configuration
External Configuration > คลิกที่ Detailed Settings
![image](https://user-images.githubusercontent.com/67640462/232582211-c1924bea-87cf-42fa-9cf5-dce6e90dc396.png)

4.ตั้งค่า Built-in Ethernet Port

  1.เลือก SLMP 
  2.ใส่หมายเลขพอร์ตอะไรก็ได้โดยในตัวอย่างจะใช้พอร์ตหมายเลข 9000
  3.ตั้งค่าเสร็จแล้วทำการคลิกที่ Close with Reflecting the settings
![image](https://user-images.githubusercontent.com/67640462/232584645-d4ddae4a-6d2c-4878-8197-73502f9d976f.png)
