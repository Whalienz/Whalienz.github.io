# Chutima Selakhun - Portfolio

Portfolio website built with Jekyll and hosted on GitHub Pages.

## 🚀 Quick Start

### วิธีที่ 1: ใช้ GitHub Pages (แนะนำ)
1. Push โค้ดขึ้น GitHub
2. ไปที่ Settings > Pages
3. เลือก Source: Deploy from a branch
4. เลือก Branch: main หรือ develop
5. รอสักครู่ เว็บจะพร้อมใช้งานที่ `https://whalienz.github.io`

### วิธีที่ 2: รันบนเครื่องของคุณ

#### ติดตั้ง Jekyll
```bash
# ติดตั้ง Ruby ก่อน (ถ้ายังไม่มี)
# Download จาก: https://rubyinstaller.org/ (Windows)
# macOS/Linux: Ruby มักติดตั้งมาแล้ว

# ติดตั้ง dependencies
bundle install

# รัน Jekyll server
bundle exec jekyll serve

# เปิดเบราว์เซอร์ไปที่: http://localhost:4000
```

## 📝 วิธีแก้ไขเนื้อหา

### แก้ไขข้อมูลส่วนตัว
แก้ไขไฟล์ `_config.yml`:
```yaml
title: Your Name - Portfolio
email: your.email@example.com
phone: xxx-xxxxxxx
github_username: yourusername
```

### แก้ไข Skills
แก้ไขไฟล์ `_data/skills.yml`:
```yaml
- name: JavaScript
  icon: fab fa-js
  icon_type: fontawesome
  level: 85
```

### แก้ไข Projects
แก้ไขไฟล์ `_data/projects.yml`:
```yaml
- title: My Project
  description: Project description
  image: https://example.com/image.jpg
  tags:
    - React
    - Node.js
  code_url: https://github.com/...
  demo_url: https://demo.com
```

### แก้ไข Social Links
แก้ไขไฟล์ `_data/social.yml`:
```yaml
- name: GitHub
  icon: fab fa-github
  url: https://github.com/yourusername
```

## 📁 โครงสร้างโปรเจค

```
.
├── _config.yml          # การตั้งค่าหลัก
├── _layouts/
│   └── default.html     # Template หลัก
├── _includes/           # ส่วนประกอบต่างๆ
│   ├── navbar.html
│   ├── hero.html
│   ├── about.html
│   ├── skills.html
│   ├── projects.html
│   ├── contact.html
│   └── footer.html
├── _data/               # ข้อมูลในรูปแบบ YAML
│   ├── skills.yml
│   ├── projects.yml
│   └── social.yml
├── images/              # รูปภาพ
├── styles.css           # CSS
├── script.js            # JavaScript
└── index.html           # หน้าหลัก
```

## 🎨 ปรับแต่งสี

แก้ไขใน `styles.css`:
```css
:root {
    --primary-color: #667eea;
    --secondary-color: #764ba2;
    --accent-color: #f093fb;
}
```

## 🔧 Tips

- หลังแก้ไข `_config.yml` ต้อง restart Jekyll server
- ไฟล์อื่นๆ จะ reload อัตโนมัติ
- เก็บ backup ไว้ที่ `index.html.backup`

## 📦 Deployment

### GitHub Pages
1. Commit และ push ไปยัง GitHub
2. GitHub จะ build และ deploy อัตโนมัติ
3. เว็บจะอัพเดทภายใน 1-2 นาที

### Custom Domain (ถ้าต้องการ)
1. เพิ่มไฟล์ `CNAME` ใส่ชื่อ domain
2. ตั้งค่า DNS ที่ domain provider
3. ตั้งค่าใน GitHub Settings > Pages

## 📄 License

MIT License - ใช้งานได้อย่างอิสระ

---

Made with ❤️ and ☕