<p align="center">
  <a href="https://www.terminalizer.com">
    <img src="/img/logo.png?raw=true" width="200"/>
  </a>
</p>

# Terminalizer

[![npm](https://img.shields.io/npm/v/terminalizer.svg)](https://www.npmjs.com/package/terminalizer)
[![npm](https://img.shields.io/npm/l/terminalizer.svg)](https://github.com/faressoft/terminalizer/blob/master/LICENSE)
[![Gitter](https://badges.gitter.im/join_chat.svg)](https://gitter.im/terminalizer/Lobby)
[![Unicorn](https://img.shields.io/badge/nyancat-approved-ff69b4.svg)](https://www.youtube.com/watch?v=QH2-TGUlwu4)
[![Tweet](https://img.shields.io/badge/twitter-share-76abec.svg)](https://goo.gl/QJzJu1)

> บันทึกเทอร์มินัลของคุณและสร้างภาพ GIF แอนิเมชันหรือแชร์ลิงก์ web player [www.terminalizer.com](https://www.terminalizer.com)

<p align="center"><img src="/img/demo.gif?raw=true"/></p>

สร้างขึ้นเพื่อให้เท่ห์สุดๆ 👌🦄 !

> หากคิดเช่นนั้น สนับสนุนด้วย `star` และ `follow` กันนะ 😘

---

<p align="center"><img src="/img/trending.png?raw=true"/></p>

---

# สารบัญ

- [Terminalizer](#terminalizer)
- [สารบัญ](#สารบัญ)
- [คุณสมบัติ](#คุณสมบัติ)
- [สิ่งที่กำลังมา](#สิ่งที่กำลังมา)
- [การติดตั้ง](#การติดตั้ง)
  - [การติดตั้งบน Windows (แก้ไขสำหรับ Version นี้)](#การติดตั้งบน-windows-แก้ไขสำหรับ-version-นี้)
- [เริ่มต้นใช้งาน](#เริ่มต้นใช้งาน)
  - [การบีบอัด](#การบีบอัด)
- [การใช้งาน](#การใช้งาน)
  - [Init](#init)
  - [Config](#config)
  - [Record](#record)
  - [Play](#play)
  - [Render](#render)
  - [Share](#share)
  - [Generate](#generate)
- [การกำหนดค่า](#การกำหนดค่า)
  - [การบันทึก](#การบันทึก)
  - [ความล่าช้า](#ความล่าช้า)
  - [ธีม](#ธีม)
  - [Watermark](#watermark)
  - [กรอบหน้าต่าง](#กรอบหน้าต่าง)
    - [กรอบแบบ Null](#กรอบแบบ-null)
    - [กรอบแบบ Window](#กรอบแบบ-window)
    - [กรอบแบบ Floating](#กรอบแบบ-floating)
    - [กรอบแบบ Solid](#กรอบแบบ-solid)
    - [กรอบแบบ Solid ไม่มีชื่อ](#กรอบแบบ-solid-ไม่มีชื่อ)
    - [เคล็ดลับการปรับแต่ง](#เคล็ดลับการปรับแต่ง)
- [คำถามที่พบบ่อย](#คำถามที่พบบ่อย)
  - [วิธีใช้งาน ZSH](#วิธีใช้งาน-zsh)
- [ปัญหาที่พบ](#ปัญหาที่พบ)
- [ลิขสิทธิ์](#ลิขสิทธิ์)

# คุณสมบัติ

- ปรับแต่งได้อย่างหลากหลาย
- รองรับหลายแพลตฟอร์ม (Linux, Windows, MacOS)
- `กรอบหน้าต่าง` แบบกำหนดเอง
- `ฟอนต์` แบบกำหนดเอง
- `สี` แบบกำหนดเอง
- `สไตล์` แบบกำหนดเองด้วย `CSS`
- Watermark
- แก้ไขเฟรมและปรับความล่าช้าก่อนการเรนเดอร์
- ข้ามเฟรมด้วยค่า step เพื่อลดจำนวนเฟรมที่เรนเดอร์
- เรนเดอร์รูปภาพพร้อมข้อความแทนการจับภาพหน้าจอเพื่อคุณภาพที่ดีกว่า
- ความสามารถในการกำหนดค่า:
  - คำสั่งที่จะจับภาพ (bash, powershell.exe, คำสั่งของคุณเอง ฯลฯ)
  - ไดเรกทอรีการทำงานปัจจุบัน
  - ค่าจำนวนคอลัมน์และแถวที่ชัดเจน
  - คุณภาพและการวนซ้ำของ GIF
  - ความล่าช้าของเฟรม
  - เวลาหยุดสูงสุดระหว่างเฟรม
  - สไตล์เคอร์เซอร์
  - ฟอนต์
  - ขนาดฟอนต์
  - ความสูงของบรรทัด
  - ระยะห่างระหว่างตัวอักษร
  - ธีม

# สิ่งที่กำลังมา

- คำสั่ง `Generate` เพื่อสร้าง web player สำหรับไฟล์บันทึก
- รองรับการติดตั้งด้วย `apt-get`, `yum`, `brew`

# การติดตั้ง

คุณต้องติดตั้ง [Node.js](https://nodejs.org/en/download/) ก่อน จากนั้นติดตั้งเครื่องมือแบบ global ด้วยคำสั่งนี้:

```bash
yarn global add terminalizer
```

![การติดตั้ง](/img/install.gif?raw=true)

> ยังคงมีปัญหาอยู่หรือไม่? ตรวจสอบส่วน [ปัญหาที่พบ](#ปัญหาที่พบ) หรือเปิด issue ใหม่

การติดตั้งควรจะราบรื่นกับ Node.js v4-v16 สำหรับเวอร์ชันใหม่กว่า หากการติดตั้งล้มเหลว คุณอาจต้องติดตั้งเครื่องมือพัฒนาเพื่อ build `C++` add-ons ตรวจสอบ [node-gyp](https://github.com/nodejs/node-gyp#installation)

## การติดตั้งบน Windows (แก้ไขสำหรับ Version นี้)

⚠️ **หมายเหตุสำหรับผู้ใช้ Windows**: Version นี้ได้ทำการแก้ไขเพื่อให้ทำงานบน Windows ได้:

### วิธีการติดตั้งและใช้งาน:

1. **Clone หรือ Download โปรเจ็คนี้**
```bash
git clone https://github.com/faressoft/terminalizer.git
cd terminalizer
```

2. **ติดตั้ง Dependencies**
```bash
npm install --ignore-scripts
```

3. **Build โปรเจ็ค**
```bash
npm run build
```

4. **ใช้งาน Terminalizer**
```bash
# ใช้คำสั่งผ่าน Node.js โดยตรง
node bin/app.js --help

# หรือสร้าง alias ใน PowerShell profile
echo 'function terminalizer { node "$(Get-Location)/bin/app.js" @args }' >> $PROFILE
```

### ข้อจำกัดบน Windows:
- ฟังก์ชัน **Record** อาจไม่ทำงานเต็มที่เนื่องจาก node-pty dependency ถูก disable
- ฟังก์ชัน **Render**, **Play**, **Generate** ใช้งานได้ปกติ
- สำหรับการ record จริง แนะนำให้ใช้บน Linux/Mac หรือ WSL

### การใช้งานแทน Record บน Windows:
```bash
# สร้างไฟล์ YAML ด้วยตนเอง แล้วใช้ Play และ Render
node bin/app.js config
node bin/app.js play existing-recording.yml
node bin/app.js render existing-recording.yml
```

# เริ่มต้นใช้งาน

เริ่มบันทึกเทอร์มินัลของคุณโดยใช้คำสั่ง `record`

```bash
terminalizer record demo
```

ไฟล์ชื่อ `demo.yml` จะถูกสร้างขึ้นในไดเรกทอรีปัจจุบัน คุณสามารถเปิดด้วยโปรแกรมแก้ไขใดๆ เพื่อแก้ไขการกำหนดค่าและเฟรมที่บันทึกไว้ คุณสามารถเล่นการบันทึกของคุณใหม่โดยใช้คำสั่ง `play`

```bash
terminalizer play demo
```

ตอนนี้มาเรนเดอร์การบันทึกของเราเป็น GIF แอนิเมชันกัน

```bash
terminalizer render demo
```

## การบีบอัด

การบีบอัด GIF ยังไม่ได้ถูกใช้งาน ตอนนี้เราแนะนำ [https://gifcompressor.com](https://gifcompressor.com)

# การใช้งาน

> คุณสามารถใช้ตัวเลือก `--help` เพื่อดูรายละเอียดเพิ่มเติมเกี่ยวกับคำสั่งและตัวเลือกต่างๆ

```bash
terminalizer <command> [options]
```

## Init

> สร้างไดเรกทอรีกำหนดค่าส่วนกลาง

```bash
terminalizer init
```

## Config

> สร้างไฟล์กำหนดค่าในไดเรกทอรีปัจจุบัน

```bash
terminalizer config
```

## Record

> บันทึกเทอร์มินัลของคุณและสร้างไฟล์บันทึก

```bash
terminalizer record <recordingFile>
```

ตัวเลือก

```
-c, --config        เขียนทับการกำหนดค่าเริ่มต้น                                [string]
-d, --command       คำสั่งที่จะถูกดำเนินการ                         [string] [default: null]
-k, --skip-sharing  ข้ามการแชร์และแสดงข้อความแจ้งการแชร์    [boolean] [default: false]
```

ตัวอย่าง

```
terminalizer record foo                      เริ่มบันทึกและสร้างไฟล์บันทึกชื่อ foo.yml
terminalizer record foo --config config.yml  เริ่มบันทึกด้วยการกำหนดค่าของคุณเอง
```

## Play

> เล่นไฟล์บันทึกบนเทอร์มินัลของคุณ

```bash
terminalizer play <recordingFile>
```

ตัวเลือก

```
-r, --real-timing   ใช้ความล่าช้าจริงระหว่างเฟรมตามที่บันทึกไว้  [boolean] [default: false]
-s, --speed-factor  ตัวคูณความเร็ว คูณความล่าช้าของเฟรมด้วยตัวคูณนี้ [number] [default: 1]
```

## Render

> เรนเดอร์ไฟล์บันทึกเป็นภาพ GIF แอนิเมชัน

```bash
terminalizer render <recordingFile>
```

ตัวเลือก

```
-o, --output   ชื่อสำหรับไฟล์เอาต์พุต                                    [string]
-q, --quality  คุณภาพของภาพที่เรนเดอร์ (1 - 100)                      [number]
-s, --step     เพื่อลดจำนวนเฟรมที่เรนเดอร์ (step > 1)   [number] [default: 1]
```

## Share

> อัปโหลดไฟล์บันทึกและรับลิงก์สำหรับ online player

```bash
terminalizer share <recordingFile>
```

## Generate

> สร้าง web player สำหรับไฟล์บันทึก

```bash
terminalizer generate <recordingFile>
```

# การกำหนดค่า

ไฟล์ `config.yml` เริ่มต้นถูกเก็บไว้ภายใต้ไดเรกทอรีรูทของโปรเจ็ค ดำเนินคำสั่งด้านล่างเพื่อคัดลอกไปยังไดเรกทอรีปัจจุบันของคุณ

> ใช้โปรแกรมแก้ไขใดๆ เพื่อแก้ไข `config.yml` ที่คัดลอกมา จากนั้นใช้ตัวเลือก `-c` เพื่อเขียนทับค่าเริ่มต้น

```bash
terminalizer config
```

> แนะนำ ใช้คำสั่ง `init` เพื่อสร้างไฟล์กำหนดค่าส่วนกลางที่จะใช้แทนค่าเริ่มต้น

```bash
terminalizer init
```

สำหรับ Linux และ MacOS ไดเรกทอรีที่สร้างขึ้นจะอยู่ภายใต้ไดเรกทอรีหลัก `~/config/terminalizer` สำหรับ Windows จะอยู่ภายใต้ `AppData`

## การบันทึก

- `command`: ระบุคำสั่งที่จะดำเนินการเช่น `/bin/bash -l`, `ls`, หรือคำสั่งอื่นใด ค่าเริ่มต้นคือ `bash` สำหรับ `Linux` หรือ `powershell.exe` สำหรับ `Windows`
- `cwd`: ระบุเส้นทางไดเรกทอรีการทำงานปัจจุบัน ค่าเริ่มต้นคือเส้นทางไดเรกทอรีการทำงานปัจจุบัน
- `env`: ส่งออกตัวแปร ENV เพิ่มเติม เพื่อให้อ่านโดยสคริปต์ของคุณเมื่อเริ่มการบันทึก
- `cols`: กำหนดจำนวนคอลัมน์อย่างชัดเจนหรือใช้ `auto` เพื่อใช้จำนวนคอลัมน์ปัจจุบันของ shell ของคุณ
- `rows`: กำหนดจำนวนแถวอย่างชัดเจนหรือใช้ `auto` เพื่อใช้จำนวนแถวปัจจุบันของ shell ของคุณ

## ความล่าช้า

- `frameDelay`: ความล่าช้าระหว่างเฟรมเป็นมิลลิวินาที หากค่าเป็น `auto` ใช้ความล่าช้าในการบันทึกจริง
- `maxIdleTime`: ความล่าช้าสูงสุดระหว่างเฟรมเป็นมิลลิวินาที จะถูกละเว้นหาก `frameDelay` ไม่ได้ตั้งเป็น `auto` ตั้งเป็น `auto` เพื่อป้องกันการจำกัดเวลาหยุดสูงสุด

## GIF

- `quality`: คุณภาพของภาพ GIF ที่สร้างขึ้น (1 - 100)
- `repeat`: จำนวนครั้งในการวนซ้ำ GIF:
  - หากค่าเป็น `-1` เล่นครั้งเดียว
  - หากค่าเป็น `0` วนซ้ำไม่จำกัด
  - หากค่าเป็นจำนวนบวก วนซ้ำ `n` ครั้ง

## เทอร์มินัล

- `cursorStyle`: สไตล์เคอร์เซอร์สามารถเป็น `block`, `underline`, หรือ `bar`
- `fontFamily`: คุณสามารถใช้ฟอนต์ใดๆ ที่ติดตั้งในเครื่องของคุณเช่น `Monaco` หรือ `Lucida Console` (รายการแบบ CSS)
- `fontSize`: ขนาดของฟอนต์เป็นพิกเซล
- `lineHeight`: ความสูงของบรรทัดเป็นพิกเซล
- `letterSpacing`: ระยะห่างระหว่างตัวอักษรเป็นพิกเซล

## ธีม

คุณสามารถตั้งค่าสีของเทอร์มินัลของคุณโดยใช้รูปแบบ CSS อย่างใดอย่างหนึ่ง:

- Hex: `#FFFFFF`
- RGB: `rgb(255, 255, 255)`
- HSL: `hsl(0, 0%, 100%)`
- Name: `white`, `red`, `blue`

> คุณสามารถใช้ค่า `transparent` ได้เช่นกัน

สีเริ่มต้นที่กำหนดให้กับสีเทอร์มินัลคือ:

- background: ![#ffffff](https://placehold.it/15/ffffff/000000?text=+) `transparent`
- foreground: ![#afafaf](https://placehold.it/15/afafaf/000000?text=+) `#afafaf`
- cursor: ![#c7c7c7](https://placehold.it/15/c7c7c7/000000?text=+) `#c7c7c7`
- black: ![#232628](https://placehold.it/15/232628/000000?text=+) `#232628`
- red: ![#fc4384](https://placehold.it/15/fc4384/000000?text=+) `#fc4384`
- green: ![#b3e33b](https://placehold.it/15/b3e33b/000000?text=+) `#b3e33b`
- yellow: ![#ffa727](https://placehold.it/15/ffa727/000000?text=+) `#ffa727`
- blue: ![#75dff2](https://placehold.it/15/75dff2/000000?text=+) `#75dff2`
- magenta: ![#ae89fe](https://placehold.it/15/ae89fe/000000?text=+) `#ae89fe`
- cyan: ![#708387](https://placehold.it/15/708387/000000?text=+) `#708387`
- white: ![#d5d5d0](https://placehold.it/15/d5d5d0/000000?text=+) `#d5d5d0`
- brightBlack: ![#626566](https://placehold.it/15/626566/000000?text=+) `#626566`
- brightRed: ![#ff7fac](https://placehold.it/15/ff7fac/000000?text=+) `#ff7fac`
- brightGreen: ![#c8ed71](https://placehold.it/15/c8ed71/000000?text=+) `#c8ed71`
- brightYellow: ![#ebdf86](https://placehold.it/15/ebdf86/000000?text=+) `#ebdf86`
- brightBlue: ![#75dff2](https://placehold.it/15/75dff2/000000?text=+) `#75dff2`
- brightMagenta: ![#ae89fe](https://placehold.it/15/ae89fe/000000?text=+) `#ae89fe`
- brightCyan: ![#b1c6ca](https://placehold.it/15/b1c6ca/000000?text=+) `#b1c6ca`
- brightWhite: ![#f9f9f4](https://placehold.it/15/f9f9f4/000000?text=+) `#f9f9f4`

## Watermark

คุณสามารถเพิ่มโลโก้ลายน้ำในภาพ GIF ที่สร้างขึ้น

<p align="center"><img src="/img/watermark.gif?raw=true"/></p>

```
watermark:
  imagePath: เส้นทางสัมบูรณ์หรือ URL
  style:
    position: absolute
    right: 15px
    bottom: 15px
    width: 100px
    opacity: 0.9
```

- `watermark.imagePath`: เส้นทางสัมบูรณ์สำหรับภาพในเครื่องของคุณหรือ URL
- `watermark.style`: ใช้สไตล์ CSS (camelCase) กับภาพลายน้ำ เช่น การปรับขนาด

## กรอบหน้าต่าง

Terminalizer มาพร้อมกับกรอบที่กำหนดไว้ล่วงหน้าที่คุณสามารถใช้เพื่อทำให้ภาพ GIF ของคุณดูเท่

- `frameBox.type`: สามารถเป็น `null`, `window`, `floating`, หรือ `solid`
- `frameBox.title`: เพื่อแสดงชื่อเรื่องของกรอบหรือ `null`
- `frameBox.style`: เพื่อใช้สไตล์ CSS แบบกำหนดเองหรือเพื่อเขียนทับสไตล์ปัจจุบัน

### กรอบแบบ Null

ไม่มีกรอบ เพียงแค่การบันทึกของคุณ

<p align="center"><img src="/img/frames/null.gif?raw=true"/></p>

> อย่าลืมเพิ่ม `backgroundColor` ภายใต้ `style`

```
frameBox:
  type: null
  title: null
  style:
    backgroundColor: black
```

### กรอบแบบ Window

<p align="center"><img src="/img/frames/window.gif?raw=true"/></p>

```
frameBox:
  type: window
  title: Terminalizer
  style: []
```

### กรอบแบบ Floating

<p align="center"><img src="/img/frames/floating.gif?raw=true"/></p>

```
frameBox:
  type: floating
  title: Terminalizer
  style: []
```

### กรอบแบบ Solid

<p align="center"><img src="/img/frames/solid.gif?raw=true"/></p>

```
frameBox:
  type: solid
  title: Terminalizer
  style: []
```

### กรอบแบบ Solid ไม่มีชื่อ

<p align="center"><img src="/img/frames/solid_without_title.gif?raw=true"/></p>

```
frameBox:
  type: solid
  title: null
  style: []
```

### เคล็ดลับการปรับแต่ง

คุณสามารถปิดเงาและระยะขอบเริ่มต้นได้

<p align="center"><img src="/img/frames/solid_without_title_without_shadows.gif?raw=true"/></p>

```
frameBox:
  type: solid
  title: null
  style:
    boxShadow: none
    margin: 0px
```

# คำถามที่พบบ่อย

## วิธีใช้งาน ZSH

คำสั่งเริ่มต้นที่ถูกบันทึกสำหรับ Linux คือ `bash -l` คุณต้องเปลี่ยนคำสั่งเริ่มต้นเป็น `zsh`

- สร้างไฟล์กำหนดค่าในไดเรกทอรีปัจจุบัน

```bash
terminalizer config
```

- เปิดไฟล์กำหนดค่าที่สร้างขึ้นด้วยโปรแกรมแก้ไขที่คุณต้องการ
- เปลี่ยน `command` เป็น `zsh`:

```
command: zsh
```

- คุณอาจต้องเปลี่ยนฟอนต์ ตรวจสอบฟอนต์ที่ใช้ในเทอร์มินัลของคุณ:

```
fontFamily: "Meslo for Powerline, Meslo LG M for Powerline"
```

- ใช้ตัวเลือก `-c` เพื่อเขียนทับไฟล์กำหนดค่า:

```bash
terminalizer record demo -c config.yml
```

# ปัญหาที่พบ

> error while loading shared libraries: libXss.so.1: cannot open shared object file: No such file or directory

วิธีแก้ไข:

```bash
sudo yum install libXScrnSaver
```

> error while loading shared libraries: libgconf-2.so.4: cannot open shared object file: No such file or directory

วิธีแก้ไข:

```bash
sudo apt-get install libgconf-2-4
```

> node-gyp compilation errors บน Windows

วิธีแก้ไข:

```bash
# ใช้ version ที่แก้ไขแล้วนี้ หรือ
npm install --ignore-scripts
# หรือใช้บน WSL/Linux
```

# ลิขสิทธิ์

โครงการนี้อยู่ภายใต้ลิขสิทธิ์ MIT - ดูรายละเอียดในไฟล์ [LICENSE](LICENSE)

---

Made with ❤️ by [Fares Softi](https://www.faressoft.net)

แปลเป็นภาษาไทยและปรับปรุงสำหรับ Windows โดย GitHub Copilot

> Error: EACCES: permission denied, access '/usr/local/lib'

Solution:

```bash
sudo mkdir -p /usr/local/lib/node_modules && sudo chown -R $(whoami):$(whoami) /usr/local/lib/node_modules

# then use the install command in the "Installation" section above
yarn global add terminalizer
```

# License

This project is under the MIT license.
