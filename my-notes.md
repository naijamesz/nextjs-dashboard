#Chapter 1 Project Folder Structure

Folder Structure หรือ โครงสร้างของโปรเจ็ค Next.js ใบแบบคร่าวๆ ที่เราจะได้เรียนรู้ในบทนี้คือ

<center>
<img src="https://nextjs.org/_next/image?url=%2Flearn%2Fdark%2Flearn-folder-structure.png&w=1920&q=75&dpl=dpl_FpUpCnRKEBXv315brQeMsK2RsYc1" alt="Next.js folder structure" width="50%">
</center>

/app: Contains all the routes, components, and logic for your application, this is where you'll be mostly working from.
โฟเดอร์ app จะมีโฟเดอร์อยู่ 3 โฟเดอร์สามรูปแบบคือ components, routes, และ logic โดยโฟเดอร์ app จะเป็นที่เก็บโค้ดที่เราจะทำงานกับมากที่สุด

/app/lib: Contains functions used in your application, such as reusable utility functions and data fetching functions.
โฟเดอร์ lib จะเป็นที่เก็บฟังก์ชันที่ใช้ในแอพพลิเคชั่นของเรา เช่น ฟังก์ชันที่ใช้ซ้ำได้ และ ฟังก์ชันที่ใช้ดึงข้อมูล ยกตัวอย่างเช่น ฟังก์ชันที่ใช้ดึงข้อมูลจาก API

/app/ui: Contains all the UI components for your application, such as cards, tables, and forms.
โฟลเดอร์ app/ui จะเป็นที่เก็บคอมโพเนนต์ที่เกี่ยวกับ UI ของแอพพลิเคชั่น เช่น การ์ด, ตาราง, และ ฟอร์ม 9jk'q

/public: Contains all the static assets for your application, such as images, fonts, and favicons.
โฟเดอร์ public จะเป็นที่เก็บไฟล์สแตติกที่ใช้ในแอพพลิเคชั่น เช่น รูปภาพ, ฟอนต์, และ ไอคอน (แนะนำให้ใช้ Image Component ของ Next.js ในการแสดงรูปภาพจะดีกว่า)

/scripts: Contains a seeding script that you'll use to populate your database in a later chapter.
โฟเดอร์ scripts จะเป็นที่เก็บสคริปต์ที่ใช้ในการเติมข้อมูลลงในฐานข้อมูล

Config Files: You'll also notice config files such as next.config.js at the root of your application. Most of these files are created and pre-configured when you start a new project using create-next-app. You will not need to modify them in this course.

ไฟล์ config: คุณจะเห็นไฟล์ config เช่น next.config.js อยู่ root ของแอพพลิเคชั่น ไฟล์เหล่านี้ส่วนใหญ่จะถูกสร้างขึ้นและกำหนดค่าไว้ล่วงหน้าเมื่อคุณเริ่มโปรเจ็คใหม่โดยใช้ create-next-app คุณจะไม่จำเป็นต้องแก้ไขไฟล์เหล่านี้ในคอร์สนี้

For now, take a look at the /app/lib/definitions.ts file. Here, we manually define the types that will be returned from the database. For example, the invoices table has the following types:

ต่อมานี้ให้คุณมองหา /app/lib/definitions.ts ไฟล์ ที่นี่เรากำหนดชนิดของข้อมูลที่จะถูกส่งกลับมาจากฐานข้อมูลเอง ตัวอย่างเช่น ตาราง invoices

```tsx
export type Invoice = {
  id: string;
  customer_id: string;
  amount: number;
  date: string;
  // In TypeScript, this is called a string union type.
  // It means that the "status" property can only be one of the two strings: 'pending' or 'paid'.
  status: 'pending' | 'paid';
};
```

#Chapter 2 CSS Styling
