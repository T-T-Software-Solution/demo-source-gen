# demo-source-gen
Demo Source Gen


## Docker Compose

```bash
docker-compose up -d
sudo chmod -R 750 ./pgadmin-data
sudo chmod -R 700 ./postgres-data
```

เมื่อรัน docker compose ครั้งแรก ตัว BE จะถูก terminate เพราะเราต้องเข้าไป setup database ก่อน โดยการ
เข้าไปที่ http://localhost:5051 (PG Admin) แล้วกดที่เมนูด้านบน Object > Register > Server...
- Tab: General ช่อง Name กรอกอะไรก็ได้
- Tab: Connection ใส่ HostName -> postgres , Password -> project0* แล้วกดบันทึกโลด
กด restart BE docker instance ที่ดับไป แล้วมันก็จะใช้งานได้ปรกติ
ลองเข้าไปกดเล่น BE ได้จาก https://localhost:3000/swagger โดยลองสร้างและดึงข้อมูล CatTypes มาได้เยย