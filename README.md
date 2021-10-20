# CN476 Internet Technology

* ปราชญ์ ฉันทะสันติธรรม 6110613202

## Hash & PKI for Blockchain

* https://youtu.be/SSL_P_R1MVo

## IPFS

InterPlanetary File System (IPFS) เป็น protocol เพื่อที่จะจัดเก็บไฟล์ในรูปแบบ distributed โดยสิ่งที่เรา request คือ content address (hash ของ content) แทนการ request แบบเดิมใน HTTP ที่จะทำการ request link ไปที่ server ที่ไฟล์นั้นถูกเก็บอยู่

### ข้อดี
* ระบบจะเป็น distributed system กล่าวคือ ไม่มี single point of failure เหมือน HTTP ที่หาก server ที่เราต้องการ request ไฟล์ล่ม เราก็จะไม่สามารถ request หาไฟล์นั้นได้เลย
* เนื่องจากเป็น distributed system ทำให้เรา request ไฟล์จาก node ไหนก็ได้ (node ใกล้เคียง) ที่มีไฟล์ที่เราต้องการ ไม่จำเป็นต้องเดินทางไปหา server ที่อาจจะอยู่ไกล
* ใน HTTP หากไฟล์ที่เก็บอยู่ใน server ถูกย้ายที่ แล้วเรา request ไปที่ URL เดิม เราจะหาไฟล์นั้นไม่เจอ (404 not found) แต่หากเป็น IPFS เรา request content address ของไฟล์แทน ทำให้จะไม่เกิดกรณีหาไฟล์ที่ถูกย้ายไม่เจอ เนื่องจากเรา request หา content address ของไฟล์ ไม่ใช่ตำแหน่งของไฟล์ที่เคยอยู่