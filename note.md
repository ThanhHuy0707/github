#term danh từ

Repository(repo): thư mục dự án(github_vn)
Branch: cành, một dự án sẽ có nhiều cành khác nhau

#Cmmmands: lệnh
git init: sẽ làm dự án để giuhub_vn trở thành repository

git status: trangj thái dự án

git add: cho phép chuẩn bị lưu lại thời điểm hiện tại của dự án (git add index.html), git add . để lưu toàn bộ 

git reset: bỏ lưu hết

git commit: ghi chú trươcs khi lưu
git commit -m 'ghi chu'

git log: muốn coi thời điểm mà chúng ta đã lưu

khi chúng ta thay đổi file index.html 
status thì file được thay đổi chưa được lưu
add và commit rồi ghi lại ghi chú

git log --oneline hiện id đã commit

git checkout id: trở về commit đầu tiên
trở lại commit đầu tiên phải dùng id thứ 2
git checkout (breanch name) master: trở lại dự án ban đầu
git branch: master
git checkout -b (branch name): đặt tên mình mong muốn 

PS D:\Downloads\github> git commit -m 'initial commit'
[master (root-commit) 591142b] initial commit
 2 files changed, 45 insertions(+)
 create mode 100644 index.html
 create mode 100644 note.md
PS D:\Downloads\github> git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")
PS D:\Downloads\github> git add .
PS D:\Downloads\github> git commit -m 'second commit'
[master 596ffb1] second commit
 1 file changed, 1 insertion(+)
PS D:\Downloads\github> 




