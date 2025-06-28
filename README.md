# Github-Download
github를 사용하기 위해서는 git을 다운받아야한다.
윈도우 시작 메뉴에서 터미널 검색 후 실행한다.

    git --version

#### 컴퓨터에 git이 존재하는지 확인해야 한다.
git이 존재하지 않을 땐 아래와 같이 나타난다.

![Image](https://github.com/user-attachments/assets/36069dc9-481e-4272-90db-12895f78eaec)

git이 설치되었을 때는 아래와 같이 나타난다.

![Image](https://github.com/user-attachments/assets/a263592b-2af1-44d9-9d3f-57f9dddb7920)

#### github에서 repogitory에 파일을 넣기 위해서
 1. github에 repo를 생성한다.
 2. github 계정 초기설정
    로컬저장소 = 내 컴퓨터 저장소(C:\Users\SAMSUNG)
    <pre>
    git config --global user.name "깃허브이름"
    git config --global user.email "깃허브 사용 메일"
    </pre>
 3. 로컬저장소 지정
    <pre>
    cd 폴더명/
    git init
    ls
    </pre>
    - git init : 저장소를 초기화하는 명령어
    - ls : 해당 폴더 내 파일목록 보는 명령어
    <pre>
    git add .
    git commit -m "first commit"
    git remote add origin "해당 레포 주소"
    git push origin master
    </pre>
    - add . : 점(.)은 모든 파일이 들어갈 수 있도록 설정
    - commit -m "해당 repo의 설명"을 추가

    #### + git commit -m이 오류가 발생할 수 있다.
    <pre>
    On branch master
    Initial commit
    nothing to commit (create/copy files and use "git add" to track)
    </pre>
    - On branch master: 현재 master브랜치에 있음
    - No commits yet: 커밋한 파일이 아직 없음
    - nothing to commit (create/copy files and use "git add" to track) : 현재 커밋할 파일이 없음
    
    즉, 폴더 내에 파일이 있어야 commit이 가능한 것 같다.
    
    그래서 테스트용이기 때문에 직접 text.txt파일을 폴더에 넣어봤다.
    
    테스트용이 아니라 사용하는 레포였다면 파일들을 미리 넣어놓고 commit해야되는 것 같다.

### + 정리

    test.txt파일을 폴더에 직접 추가 ->
    
    `git add test.txt` 파일 git에 추가 ->
    
    `git commit -m "first commit"` 등록하고 커밋 ->
    
    `git remote add origin "해당 레포 주소"` 레포 주소를 원격저장소에 추가 ->

    'git push origin master' master에 추가한 원격저장소를 push함

    해당 파일이 github의 repo에 추가되어 있을 것이다.
----
### Tip

    `git remote -v` : 로컬저장소와 원격저장소가 연결되어 있는지 확인하는 명령어
    
                     연결된 저장소가 없다면 나와 같이 아무 내역이 나오지 않는다.
    
    `git status` : 파일 변경 상태 보기
    
    `git log` : 커밋했던 기록 보는 명령
    
    




