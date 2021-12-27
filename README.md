# Hair-Color-Classification
   การจำแนกสีผม ซึ่งใช้ภาพเฉพาะของเส้นผม โดยใช้ KKN (K-Nearest Neighbors) เพื่อสุ่มตัวอย่างชุดสีที่รู้จักใน HLS Color Space ในการจำแนกประเภทของสีผม
## Overview
  • การจำแนกสีผม 9 เฉดสี คือ ดำ น้ำตาล บลอน เทา เหลือง ชมพู ม่วง เขียว และสีแดง
  • ใช้ Model K-Nearest Neighbors (KNN)  เพื่อสุ่มตัวอย่างชุดสีที่รู้จักใน HLS Color Space
  • โดยพื้นที่สี HLS จะเป็นตัวแทนของพื้นที่สี โดยจะพิจารณาจาก Vector 3 องค์ประกอบของ Hue, Lightness, Saturation 
## Install Dependencies
   - colorsys 
   - PIL 
   - glob
   - numpy
   - random 
   - matplotlib 
   - tqdm
   - sklearn
