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

git log --oneline hiện id đã commit, gonj hơn với git log

git checkout id: trở về commit đầu tiên
trở lại commit đầu tiên phải dùng id dau tien
git checkout (breanch name) master: trở lại dự án ban đầu
git branch: master
git checkout -b (branch name): đặt tên mình mong muốn (dev)
trong dev sẽ xây dựng 1 trang contactm 

git merge branch: tổng hợp lại 2 branch
git branch -d branch name: xóa branchg




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



PS D:\Downloads\github> git log --oneline
596ffb1 (HEAD -> master) second commit
591142b initial commit
PS D:\Downloads\github> git checkout 591142b
M       note.md
Note: switching to '591142b'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 591142b initial commit
PS D:\Downloads\github> git checkout master
M       note.md
Previous HEAD position was 591142b initial commit
Switched to branch 'master'



PS D:\Downloads\github> git branch
* master
PS D:\Downloads\github> git add .
PS D:\Downloads\github> git commit -m 'third commit'
[master a1757ff] third commit
 1 file changed, 19 insertions(+)
PS D:\Downloads\github> 


dev
PS D:\Downloads\github> git checkout -b dev
Switched to a new branch 'dev'
PS D:\Downloads\github> git branch
* dev
  master
PS D:\Downloads\github> git add .
PS D:\Downloads\github> git commit -m 'contact mit'
[dev 1f8f1fd] contact mit
 2 files changed, 59 insertions(+), 3 deletions(-)
 create mode 100644 contact.html
PS D:\Downloads\github> 
PS D:\Downloads\github> git checkout master: chuyển từ dev sang branch và mất contact.html tại vì nó ở dev chứ o phải master
Switched to branch 'master'
PS D:\Downloads\github> 


PS D:\Downloads\github> git add .
PS D:\Downloads\github> git commit -m 'git branch'
[master 60dd46e] git branch
 1 file changed, 5 insertions(+)
PS D:\Downloads\github> 


PS D:\Downloads\github> git checkout -b conflict
Switched to a new branch 'conflict'
PS D:\Downloads\github> git add .
PS D:\Downloads\github> git commit -m 'create conflict'
[conflict 4c655ab] create conflict
 2 files changed, 16 insertions(+), 1 deletion(-)
PS D:\Downloads\github> git checkout master
Switched to branch 'master'
PS D:\Downloads\github> git add .
PS D:\Downloads\github> git commit -m 'conflict from master'
[master ef1bb66] conflict from master
 1 file changed, 1 insertion(+)
PS D:\Downloads\github> 

Local, remove
git push 
PS D:\Downloads\github> git push https://github.com/ThanhHuy0707/github.git master









