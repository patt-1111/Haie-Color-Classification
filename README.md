# Hair-Color-Classification
   การจำแนกสีผม ซึ่งใช้ภาพเฉพาะของเส้นผม โดยใช้ KKN (K-Nearest Neighbors) เพื่อสุ่มตัวอย่างชุดสีที่รู้จักใน HLS Color Space ในการจำแนกประเภทของสีผม
## Overview
   - การจำแนกสีผม 9 เฉดสี คือ ดำ น้ำตาล บลอน เทา เหลือง ชมพู ม่วง เขียว และสีแดง
   - ใช้ Model K-Nearest Neighbors (KNN)  เพื่อสุ่มตัวอย่างชุดสีที่รู้จักใน HLS Color Space
   - โดยพื้นที่สี HLS จะเป็นตัวแทนของพื้นที่สี โดยจะพิจารณาจาก Vector 3 องค์ประกอบของ Hue, Lightness, Saturation 
## Install Dependencies
   - colorsys 
   - PIL 
   - glob
   - numpy
   - random 
   - matplotlib 
   - tqdm
   - sklearn
 ## Dataset
   - Train ข้อมูลที่ใช้ในการ train model
   - Test ข้อมูลที่ใช้ในกรทดสอบ model
   - dataset https://drive.google.com/drive/folders/1Mzzo_Nm-VBItojjAGddE8688pIRJ5bm9?usp=sharing
 ## How to use this project
   - ทำการดาวโหลด dataset ไว้ในเครื่องแยกเป็นไฟล์เดอร์ไว้
   - ในส่วนของสีสามารพป้อนข้อมูลสีด้วยตนเอง โดยข้อมูลสีให้ป้อนเป็นรหัส Hex ของสี 
![image](https://user-images.githubusercontent.com/96693271/147456304-a13e4fe3-7c98-4c4c-ae21-53769fb0f334.png)
   - รันโปรแกรม 
 ## Training Data
   ค่าใกล้เคียงที่สุดเราได้ใช้ KNeighborsClassifier เพื่อหาจุดที่ใกล้เคียง โดยทำการลองกำหนด algorithm ของ KNeighborsClassifier ให้แตกต่างกัน โดยลองด้วยกัน 4 แบบ คือ kd_tree, ball_tree, auto และ brute (คำนวณทั้งหมด) แล้ว preedic กลุ่มของสีผมที่ได้มาจากรูปภาพที่เรากำหนด แล้วplot ค่า K ออกมาดูค่า rate error ของสี
   - kd_tree
   
   ![image](https://user-images.githubusercontent.com/96693271/147456828-01fbaf7c-9830-47d9-afa5-a82c05d79c27.png)
   
   - ball_tree

![image](https://user-images.githubusercontent.com/96693271/147456966-c87516c3-4d4a-4d51-896b-982b4fb0b92b.png)
   - brute
  
![image](https://user-images.githubusercontent.com/96693271/147457067-e29df347-0e22-41c3-9c9d-3191e66abdaf.png)
   - auto

   ![image](https://user-images.githubusercontent.com/96693271/147457033-17dfa945-24e1-48d5-831c-326da182747a.png)

## Testing Data
   นำภาพที่ต้องการจำแนกมาจำแนกสีผม
   ![image](https://user-images.githubusercontent.com/96693271/147457377-0ec3bf98-ed2e-4b2f-aefc-66835f934fd7.png)
   - ผลของการจำแนกสีผมของ algorithm kd_tree
   ![image](https://user-images.githubusercontent.com/96693271/147457476-f2709bfc-e2ba-449f-b59d-e92c84fcd7f5.png)

## References
https://github.com/Michael-Naguib/Hair-Classification







