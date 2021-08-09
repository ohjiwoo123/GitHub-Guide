# GitHub-Guide
## GitHub Guide (CLI 기본사용법)
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
- (1) git init  
    - 현재 폴더를 git 폴더로 초기화한다. (git과 연결된다.)  
- (2) git status  
    - git의 현재 상태를 볼 수 있다. (커밋 내역 및 현재 브랜치)<br>
<img width="343" alt="스크린샷 2021-08-09 오후 9 45 15" src="https://user-images.githubusercontent.com/80387186/128708155-b66510ee-70df-418c-8972-71429ab4a43e.png"><br>
- (3) git log<br> 
    - git 안에서의 기록(역사)를 볼 수 있다. (커밋내역 등)<br>
    - 나갈 때는 q 버튼으로 나가면 된다.<br>
<img width="566" alt="스크린샷 2021-08-09 오후 9 41 43" src="https://user-images.githubusercontent.com/80387186/128707928-30fff9bf-063b-484c-a6b0-1b36df2afc93.png"><br>
- (4) git log --stat<br>
    - 커밋 내역 뿐만 아니라 자세한 커밋 목록까지 볼 수 있다.<br>
<img width="564" alt="스크린샷 2021-08-09 오후 9 50 39" src="https://user-images.githubusercontent.com/80387186/128715679-6c99a5ce-20f7-4df0-b39f-01355300e91f.png"><br>
- (5) git diff<br>
    - 이전 커밋과의 차이점을 볼 수 있다. <br>
<img width="562" alt="스크린샷 2021-08-09 오후 10 44 10" src="https://user-images.githubusercontent.com/80387186/128716248-7922756e-735e-460d-8f40-0697ca286c40.png"><br>
- (6) git 
