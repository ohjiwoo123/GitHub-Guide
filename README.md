# GitHub-Guide (CLI 기본사용법)
## Git의 큰 그림 
pull -> push -> commit <br>
git fetch -> git merge Fetch_HEAD -> commit -> push <br>
git pull = git fetch; git merge origin/master <br>

### 0) 처음 repo 만들고 기본 Add, Commit, Push 
…or create a new repository on the command line
echo "# cs2dddx" >> README.md
```
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/ohjiwoo123/cs2dddx.git
git push -u origin main
```
…or push an existing repository from the command line
```
git remote add origin https://github.com/ohjiwoo123/cs2dddx.git
git branch -M main
git push -u origin main
```
…or import code from another repository
You can initialize this repository with code from a Subversion, Mercurial, or TFS project.
### 1) 기본 사용법
```zsh
# git 연습을 위한 폴더 생성
cd ~
cd Documents
mkdir git
cd git
mkdir hello-git-cli
cd hello-git-cli

# 현재 폴더에서 git 
# initialized git repository in ~/Documents/git/hello-git-cli/.git
git init .

# .git 폴더가 생긴 것을 확인할 수 있다.
ls -al

# .git 폴더 안에 git과 관련하여 여러 폴더와 파일이 생성된다.
cd .git 
ls
```
<img width="355" alt="스크린샷 2021-08-09 오후 9 25 40" src="https://user-images.githubusercontent.com/80387186/128706894-005f0c28-157d-4baf-9cba-81baa6df03e4.png">
<img width="342" alt="스크린샷 2021-08-09 오후 9 25 55" src="https://user-images.githubusercontent.com/80387186/128706899-7a777fbe-dcf6-4b07-b182-c1e19adfc8f3.png">

### 2) 명령어 정리
- (1) `git init`  
    - 현재 폴더를 git 폴더로 초기화한다. (git과 연결된다.)  
- (2) `git status`  
    - git의 현재 상태를 볼 수 있다. (커밋 내역 및 현재 브랜치)<br>
<img width="343" alt="스크린샷 2021-08-09 오후 9 45 15" src="https://user-images.githubusercontent.com/80387186/128708155-b66510ee-70df-418c-8972-71429ab4a43e.png"><br>
- (3) `git log`<br> 
    - git 안에서의 기록(역사)를 볼 수 있다. (커밋내역 등)<br>
    - 나갈 때는 q 버튼으로 나가면 된다. <br>
<img width="566" alt="스크린샷 2021-08-09 오후 9 41 43" src="https://user-images.githubusercontent.com/80387186/128707928-30fff9bf-063b-484c-a6b0-1b36df2afc93.png"><br>
- (4) `git log --stat` <br>
    - 커밋 내역 뿐만 아니라 자세한 커밋 목록까지 볼 수 있다.<br>
<img width="564" alt="스크린샷 2021-08-09 오후 9 50 39" src="https://user-images.githubusercontent.com/80387186/128715679-6c99a5ce-20f7-4df0-b39f-01355300e91f.png"><br>
- (5) `git log -p` <br>
    - git log 에서 추가로 이전 커밋에서 어떤 것이 바뀌었는지 보여준다. <br>
 <img width="561" alt="스크린샷 2021-08-09 오후 10 53 18" src="https://user-images.githubusercontent.com/80387186/128717812-3d0ab800-73f1-4547-b2c4-5ee7b146dee5.png"><br>
- (6) `git diff`<br>
    - 이전 커밋과의 차이점을 볼 수 있다. <br>
<img width="562" alt="스크린샷 2021-08-09 오후 10 44 10" src="https://user-images.githubusercontent.com/80387186/128716248-7922756e-735e-460d-8f40-0697ca286c40.png"><br>
- (7) `git reset --hard` <br>
    - 현재 파일의 이전의 상태로 돌아간다. <br>
<img width="529" alt="스크린샷 2021-08-09 오후 10 51 04" src="https://user-images.githubusercontent.com/80387186/128717331-de412062-526a-44dc-990e-be76c9a1dc0b.png"><br>
- (8) `git revert 일련번호`<br>
    - `git revert 일련번호`를 하게 되면, 해당 일련번호의 commit은 살아있지만, 일련번호의 commit의 내용이 사라지고 새로운 커밋이 생긴다.<br>
<img width="564" alt="스크린샷 2021-08-09 오후 11 53 58" src="https://user-images.githubusercontent.com/80387186/128728390-1c226641-4f79-47e7-b61f-fd8d9617a126.png"><br>
<img width="557" alt="스크린샷 2021-08-09 오후 11 54 28" src="https://user-images.githubusercontent.com/80387186/128728436-9e599f76-4e97-470b-af5a-4a53f8d21d15.png"><br>
<img width="567" alt="스크린샷 2021-08-09 오후 11 55 54" src="https://user-images.githubusercontent.com/80387186/128728494-48afda6a-17c6-48c9-a0a8-5b78846510c1.png"><br>
- (9) `git checkout f95dcac5d325a57a48b87d7dda27ad4ad4d480ce` <br>
    - commit 일련번호의 위치로 버전을 이동한다. <br>
<img width="559" alt="스크린샷 2021-08-09 오후 10 57 20" src="https://user-images.githubusercontent.com/80387186/128719185-6a677a44-1274-4a6e-acaf-6ad897a4efbc.png"><br>
<img width="563" alt="스크린샷 2021-08-09 오후 10 57 41" src="https://user-images.githubusercontent.com/80387186/128719224-ea3e3540-841b-4ed6-b614-f6911f85906b.png"><br>
- (10) `git checkout 브랜치이름`<br>
    - 해당 branch로 이동한다. (브랜치가 master일 경우에는 `<git checkout master>` <br>
<img width="558" alt="스크린샷 2021-08-09 오후 11 21 14" src="https://user-images.githubusercontent.com/80387186/128722040-42d44085-acab-418f-9a7a-6ccef8acdad8.png"><br>
- (11) `git commit -am "4"`<br>
    - add와 commit을 동시에 한다. **적어도 한 번은 add를 하여서 tracked 상태가 되어야 쓸 수 있다.** <br>
- (12) `git commit`<br>
    - 뒤에 메세지를 안 적고 그냥 `git commit`만 하는 경우에는 에디터가 뜨면서 직접 여러 줄의 메세지를 편하게 적을 수 있다.<br>
<img width="564" alt="스크린샷 2021-08-09 오후 11 42 42" src="https://user-images.githubusercontent.com/80387186/128725587-747f776c-70da-4b8f-826d-becddf001968.png"><br>
<img width="560" alt="스크린샷 2021-08-09 오후 11 43 33" src="https://user-images.githubusercontent.com/80387186/128725603-de9abe0e-bbf2-4d6f-84e6-e74196ecdacb.png"><br>
- (13) `git commit --amend`<br>
    - 커밋 메세지를 수정할 수 있다. <br>
- (14) `git config --global core.editor "nano"`<br>
    - 원하는 에디터로 설정할 수 있다. nano || vim 등등 <br>
- (15) `git branch ooo`<br>
    - 그냥 `git branch`를 하게 되면 현재 branch 목록을 보여주고, `git branch 이름`을 하게 되면 새로운 브랜치를 만든다. <br>
- (16) `git log --all --graph --oneline`<br>
    - 브랜치의 상관관계를 CLI 그래프로 표시해준다. <br>
<img width="565" alt="스크린샷 2021-08-14 오후 10 22 27" src="https://user-images.githubusercontent.com/80387186/129474008-424e38e2-10d2-4ee4-9ea7-287b0f67f3eb.png"><br>
- (17) `git merge ooo`<br>
    - 현재 브랜치에다가 ooo브랜치를 합친다. merge를 할 경우 conflict가 일어날 수 있으므로 유의해야한다.<br>
- (18) `git clone URL주소`
    - URL주소에 있는 원격저장소(Repository)를 연결한다.(나의 로컬 저장소에 복제한다)<br>
- (19) `git pull`<br>
    - 당겨오는 것. 즉 원격저장소에서 로컬저장소로 파일을 끌어온다. pull -> commit -> push <br>
- (20) `git remote` <br>
    - `git remote`를 통해서 현재 연결된 원격저장소의 이름을 보여준다. ex)origin <br>
    - `git remote -v`를 통해서 현재 연결된 원격저장소의 URL을 보여준다. ex) https://github.com/ohjiwoo123/blahblah.git <br>
    - `git remote add origin URL주소` URL주소와 현재 로컬 저장소를 연결시킨다. 
- (21) `git push`<br>
    - 로컬 저장소에서 원격 저장소로 파일을 보내는 것(업로드).<br>
- (22) `git fetch` <br>
    - `git pull`과 비슷한 개념으로 정확하게 `git pull`=== `git fetch` -> `git merge FETCH_HEAD`와 같다.


## Git 관련 Tool 소개
- (1) p4 merge Tool <br>
    - merge 합칠 때, 도움을 주는 기능. Helix Visual Merge Tool(P4Merge)은 3방향 병합 및 병렬 파일 비교 도구입니다. <br>
- (2) cherry-pick <br>
    - git cherry-pick임의의 Git 커밋을 참조로 선택하고 현재 작업 중인 HEAD에 추가할 수 있는 강력한 명령입니다. 체리 따기는 브랜치에서 커밋을 골라 다른 브랜치에 적용하는 행위입니다. git cherry-pick변경 사항을 취소하는 데 유용할 수 있습니다. 예를 들어 실수로 잘못된 브랜치에 커밋했다고 가정해 보겠습니다. 올바른 분기로 전환하고 커밋이 속해야 할 위치를 선택하면 됩니다. <br>
    
    
    
## git rebase와 merge 
- master branch와 sub branch가 있다고 가정한다.  
- 현재 나는 sub branch에서 작업중 `git checkout sub`  
- `git rebase master` 하면 sub가 master 앞으로감.  
- git merge의 경우 `git merge`   
