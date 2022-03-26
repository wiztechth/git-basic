# สอนการใช้งาน Git และ GitHub เบื้องต้น
#### slide ในคลิป [กดตรงนี้](https://github.com/wiztechth/git-basic/blob/main/Git-and-GitHub.pdf)
#### YouTube video - [คลิปสอนการใช้ Git & GitHub](https://youtube.com/wiztechth)

```Shell
# after you aready create your account on https://github.com
# from the terminal
git clone https://github.com/wiztechth/git-basic.git

# change directory to your git directory
cd git-basic
git status

# สร้างไฟล์ด้วย editor ที่ถนัด หรือ copy file จากที่อื่นเข้ามาภายใน directory
cp ../t1/home.html ../t1/i-dont-want.txt ../t1/style.css ../t1/README.md .

# add ไฟล์ให้ git รู้จัก
git add .
git status

# สมมติ ลบไฟล์ที่ไม่ต้องการออกจากการติดตามของ git
git rm --cached i-dont-want.txt
git status

# ถึงจุดนี้ สมมติว่าพร้อมแล้วที่จะส่งไฟล์ไปเก็บที่ GitHub
git commit -m 'first commit'

# ส่งไฟล์ไปเก็บบน GitHub.com
# ต้องมีการสร้าง Personal access token สำหรับใช้แทน password ก่อน
# ดูวิธีทำใน clip บน YouTube
git push

# you can check what you just uploaded (ใช้ browser ไปที่ GitHub.com)



# ทำการแก้ไขไฟล์ ครั้งที่ 2 ด้วย vi หรือ editor อะไรก็ได้
vi home.html

# check status and run 'git add xx' again
git status
git add home.html


# run git commit - second time
git commit -m 'second commit'

# push to GitHub.com
git push


# check from your browser


# ปกติ เราจะไม่ทำการแก้ไขโปรแกรมบน main branch
# แต่จะใช้วิธี branch ย่อยแทน หลังจากแก้ไขจนสมบูรณ์แล้ว จึงจะ merge กลับไปที่ main branch
# ต่อไปเป็นการสร้าง branch ชื่อ 'dev'
git branch dev


# IMPORTANT!! ย้ายการทำงานจาก main branch มาที่ dev branch
git switch dev
git status

# สมมติว่า มีการสร้าง directory และไฟล์เพิ่มเติม
mkdir fixbug
cd fixbug

# สร้างไฟล์จำลอง
touch a b c
cd ..

# add new directory
git add fixbug/
git commit -m 'fix bug from dev branch'
git status

# pubh dev branch ครั้งแรก
git push --set-upstream origin dev

# ทดสอบสร้างไฟล์เพิ่มเติม
cd fixbug/
touch d e f
git add d e f
git status
git commit -m 'fix bug second time'
git push

# ต่อไปเป็นขั้นตอนการทำ Pull Request และการ Merge กลับไปใน main branh 
# แนะนำไปทำใน browser จะสะดวกกว่า
ภาพ#1
ภาพ#2
```


