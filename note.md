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

PS D:\Downloads\github> git add .
PS D:\Downloads\github> git commit -m 'new remote push'
[master cd0ee9e] new remote push
 2 files changed, 4 insertions(+), 1 deletion(-)
PS D:\Downloads\github> git remote add origin https://github.com/ThanhHuy0707/github.git
PS D:\Downloads\github> git push origin master


PS D:\Downloads\github> git add .
PS D:\Downloads\github> git commit -m 'remote clone'
[master 45846d6] remote clone
 2 files changed, 8 insertions(+)
PS D:\Downloads\github> git push
fatal: The current branch master has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin master

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS D:\Downloads\github> git remote -v
origin  https://github.com/ThanhHuy0707/github.git (fetch)
origin  https://github.com/ThanhHuy0707/github.git (push)
PS D:\Downloads\github> git push --set-upstream origin master
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 518 bytes | 518.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ThanhHuy0707/github.git
   cd0ee9e..45846d6  master -> master
branch 'master' set up to track 'origin/master'.
PS D:\Downloads\github> git push
Everything up-to-date


PS D:\Downloads\github> git branch
  conflict
* dev
  master
PS D:\Downloads\github> git push -u origin dev


Unpacking objects: 100% (3/3), 859 bytes | 66.00 KiB/s, done.
From https://github.com/ThanhHuy0707/github
 * [new branch]      main       -> origin/main
 * [new branch]      staging    -> origin/staging
PS D:\Downloads\github> git checkout -b staging origin/staging
M       note.md
branch 'staging' set up to track 'origin/staging'.
Switched to a new branch 'staging'
PS D:\Downloads\github> git branch
  conflict
  dev
  master
* staging








