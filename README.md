# CAR CASH FINAL PROJECT

โปรเจคนี้เป็นเว็ปไซด์เกี่ยวกับรถโดยเว็ปไซด์ที่เราทำจะเป็นเว็ปไซด์เต็นท์รถมือ 2 โดยที่จะให้ผู้ใช้บริการเข้ามาขายรถให้กับเจ้าของเต็นท์รถเเล้วเจ้าของเต็นจะนำรถมาขายต่ออีกครั้ง

## Member

```
1.คณิศร ตั้งสุภากิจ 6310403940 github:kanisont SE,WEBTECH
2.ธนภัทร วรรณโลบล 6310404008 github:dkpatpot2142,Phynze SE,WEBTECH
3.จิรพัฒน์ เกิดพุ่ม 6310400932 github:usernvme SE,WEBTECH
4.ณัฐพงศ์ นาดี 6310406299 github:framenuttapong SE
5.ยศ ชัยชิต 6310451341 github:ChYote WEBTECH
```
## Installing and suggestion for project
```
โดยคำสั่งทั้งหมดจะรันผ่านทาง wsl
cc-backend (ในไฟล์ cc-backend)
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v $(pwd):/var/www/html \
    -w /var/www/html \
    laravelsail/php81-composer:latest \
    composer install --ignore-platform-reqs
cp .env.example .env
./vendor/bin/sail up -d
./vendor/bin/sail artisan key:generate
./vendor/bin/sail artisan migrate
./vendor/bin/sail artisan db:seed
./vendor/bin/sail npm install
./vendor/bin/sail npm run dev
-------------------------------
cc-frontend (ในไฟล์ cc-frontend)
docker-compose up -d
docker-compose exec app npm install
docker-compose exec app npm install vue-chartjs chart.js
docker-compose exec app npm run dev
```
## Personas
```
1.ชื่อ:Karim Benzema อาชีพ:พนักงานบริษัท รายได้:25000 ความสนใจ:หาซื้อรถยนต์มือ 2 ปัญหา:เนื่องจากเงินเดือนน้อยเลยต้องการหารถตามงบที่จำกัด ความต้องการ:รถมือ 2 ราคาถูก
2.ชื่อ:Davison Sanchez อาชีพ:CEO รายได้:230000 ความสนใจ:เปิดเต็นท์รถ ปัญหา:ไม่มีแพลตฟอร์มสำหรับเปิดเต็นท์รถ ความต้องการ:ทำกำไรจากการเปิดเต็นท์
3.ชื่อ:Harry Maguire อาชีพ:คนกวาดขยะ รายได้:5000 ความสนใจ:ขายรถมือ 2 ปัญหา:ไม่สามารถหาที่ปล่อยรถมือ 2 ได้ ความต้องการ:ขายรถมือ 2 ให้ได้ราคามากที่สุด
4.ชื่อ:David de gea อาชีพ:ว่างงาน รายได้:- ความสนใจ:สนใจงานที่จะเป็นพนักงานบริษัท ปัญหา:ยังไม่มีงานทำ ความต้องการ:เป็นพนักงานจัดการให้กับเต็นท์รถไม่ว่าจะเป็นออนไลน์หรือว่าเป็นแอดมิน
```
## Jira link
```
https://kanison.atlassian.net/jira/software/projects/CCW/boards/2/roadmap
```
## UI flow
```
xxx
```
## Unit testing
```
โดยทางกลุ่มเราได้ใช้ Junit ในการทดสอบโปรเจ็คนี้
ทดสอบ ArticleApiTest โดยการ get update delete
ทดสอบ AuthApiTest โดยการ get update delete
ทดสอบ CarApiTest โดยการ get update delete
ทดสอบ CarOfferApiTest โดยการ get update 
ทดสอบ PromotionApiTest โดยการ get update delete
ทดสอบ PromotionCodeApiTest โดยการ get update delete
------------------------------------
ข้อมูลการเทสต่างๆอยู่ในไฟล์ tests/Feature
การรัน test ให้ใช้คำสั่ง 
./vendor/bin/sail artisan test
------------------------------------
#Image Reference#
https://user-images.githubusercontent.com/78583498/200193819-affb16f2-8f75-4b68-b3b1-e36689e0103f.png
```
## Default data
```
Manager
name 'ผู้จัดการ เคร่งขรึม'
email'manager@car.com'
password '12345678'
phone_number '0812345678'
role 'manager';

Staff
name 'พนักงาน สมหวัง'
email 'staff@car.com'
password '12345678'
phone_number '0812345678'
role 'staff'

Customer
name 'ลูกค้า สมบูรณ์'
email 'user@car.com'
password bcrypt('12345678')
phone_number '0812345678'
role 'user'
```
## Release tag
```
xxx
```
