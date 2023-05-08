# วิธีเชื่อมต่อ FX5U PLC Mitsubishi เข้ากับ Node-red ด้วย MC Protocol เพื่อรับส่งข้อมูล
YouTube : https://youtu.be/ucVW0-j6oM4
 << วิธีการตั้งค่าฝั่ง PLC >>


1. ตั้งค่า PLC FX5U 
Parameter > FX5UCPU > Module Parameter เลือก Ethernet Port
![image](https://user-images.githubusercontent.com/67640462/232580400-d6b3f9fd-c0a0-4dc5-8734-13f6835a45fb.png)

2.ตั้งค่า IP Address ของ PLC
![image](https://user-images.githubusercontent.com/67640462/232581671-6e2e569b-cb50-4be8-97ea-a80e28a45f35.png)

3.ตั้งค่า External Device Configuration

External Configuration > คลิกที่ Detailed Settings
![image](https://user-images.githubusercontent.com/67640462/232582211-c1924bea-87cf-42fa-9cf5-dce6e90dc396.png)

4.ตั้งค่า Built-in Ethernet Port
  
  4.1 เลือก SLMP 
  
  4.2 ใส่หมายเลขพอร์ตอะไรก็ได้โดยในตัวอย่างจะใช้พอร์ตหมายเลข 9000
  
  4.3 ตั้งค่าเสร็จแล้วทำการคลิกที่ Close with Reflecting the settings
  
![image](https://user-images.githubusercontent.com/67640462/232584645-d4ddae4a-6d2c-4878-8197-73502f9d976f.png)

5.บันทึก Parameter Settings
![image](https://user-images.githubusercontent.com/67640462/232585310-45e0ab42-4c5f-4aaa-bdbe-67575d7796e4.png)

6.อัปโหลด Parameter เข้าสู่ CPU

   Online > Write to PLC
![image](https://user-images.githubusercontent.com/67640462/232585761-e8de1eb5-08fc-4e4d-aa23-fc59e2315096.png)
  
   6.1 เลือก Parameter + Program
   
   6.2 คลิก Execute หากมี Dialog Popup ขึ้นมาให้คลิก Yes ไปเลื่อยๆ และปิดหน้าต่างนี้ทิ้งไป
![image](https://user-images.githubusercontent.com/67640462/232586189-89f7afa2-f10b-4a58-bf33-a73a71eaf2b6.png)

7.รีเซ็ต PLC
   7.1 ดัน Switch ค้าง 10วิ แล้วปล่อย จากนั้นดันขึ้นกลับมาที่เดิม 
   
   7.2 สังเกตไฟสีแดงกระพริบในขณะที่ดัน Switch ค้าง และจะหยุดเมื่อปล่อย
   
![image](https://user-images.githubusercontent.com/67640462/232587093-65a67dbb-3451-4486-b4da-20cf44bbc324.png)

8.Monitor ข้อมูล โดยจะมีข้อมูลดังนี้

   8.1 M0   Bit
   
   8.2 D0   Init16
   
   8.3 D10  Floting

![image](https://user-images.githubusercontent.com/67640462/232593165-242d7ad3-6182-4c32-a6aa-0fd2b5950578.png)


<< การตั้งค่าใช้งานบน Node-Red >>
1. Download&Install Pallete > "MC Protocol"

2. Import flow ตัวอย่าง [ example flow: FX5U with MC Protocol ]

![image](https://user-images.githubusercontent.com/67640462/232591562-6e378657-3a31-4f7b-b715-09ff3f8179b4.png)

3. ทดลองส่งค่าไปยัง PLC โดยสังเกตที่ Watch ฝั่ง PLC 

   3.1 Force INPUT ด้านล่าง
   
   3.2 สังเกตข้อมูลที่เปลี่ยนแปลง
   
![image](https://user-images.githubusercontent.com/67640462/232594268-7134f073-dd79-4f03-9924-136af10ed17b.png)



