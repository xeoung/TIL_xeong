# CLI 기초 

## 1. GUI CLI 정의 
(1) GUI ( graphic user interface) : 
> ##### 그래픽을 통해 사용자와 컴퓨터가 상호작용하는 방식. 
- 사용하기 쉽지만 단계가 많고 성능 많이 소모

(2) CLI (command line interface) : 
> ##### 터미널을 통해 사용자와 컴퓨터가 상호작용하는 방식. 
- GUI로는 불가능한 많은 세부적인 기능을 사용할 수 있다. 

*인터페이스 : 서로 다른 개체끼리 맞닿아 있는 면. 사용자와 컴퓨터가 서로 소통하는 접점*

(3) Git Bash 가 뭔가요?
- 일종의 번역기이다
- 윈도우 유저가 UNIX 계열 운영체제의 명령어를 연습할 수 있음 
- window의 명령어 차이가 존재하기 때문에 Git Bash 로 Unix 운영체제의 터미널 명령어를 사용하기 위함.

## 2. 경로 
(1) 루트와 홈 디렉토리 
- 루트 디렉토리 (/)
    - 모든 파일과 폴더를 담고 있는 최상위 폴더
    - 윈도우의 경우 보통 c 드라이브
- 홈 디렉토리 (~)
    - 틸드(Tilde)라고 부름
    - 현재 로그인 된 사용자의 홈 폴더. 
    - 맥의 경우 /users/현재 사용자 계정 

> ##### 폴더와 디렉토리는 거의 같은 의미로 사용되지만, 폴더가 디렉토리보다 넓은 개념 
> ##### 예를들어 윈도우 탐색기에서 ‘내컴퓨터’, ‘네트워크 환경’ 와 같은 특수 폴더는 폴더이지만 디렉토리는 아니다.  ( 폴더 > 디렉토리)


(2) 절대 경로와 상대 경로 
- 절대 경로 : 루트 디렉토리부터 목적 지점까지 거치는 모든 경로
  > 윈도우 바탕화면의 절대 경로 C: Users/Kyle/Desktop

- 상대 경로 : 현재 작업하고 있는 디렉토리를 기준으로 계산된 상대적 위치 
  >현재 작업하고 있는 디렉토리가 C:/Users 면 
    > 윈도우 바탕화면의 상대 경로는 Kyle/Desktop
- ##### 간결해서 좋지만 현재 작업하고 있는 디렉토리가 변경되면 상대 경로도 바뀐다 

* ./ : 현재 작업중인 폴더 
* ../: 현재 작업중인 폴더의 부모 폴더 

## 3. 터미널 명령어 
- touch : touch text.txt
    - 파일 생성. 띄어쓰기로 구분, 여러 파일을 한번에 생성 가능 
    - 숨김 파일을 만들기 위해서는 .을 파일 명 앞에 붙인다

- mkdir : mkdir folder / mkdir ‘happy hacking’
    - 새 폴더를 생성하는 명령어  
    - 띄어쓰기로 구분하여 여러 폴더 한번에 생성 가능
    - 폴더 이름 사이에 공백 넣고 싶을 때 ‘이 렇 게’

- ls : ls (기본) ls -a(all 옵션) ls -a -l (all, long 옵션 함께) ls -al(여러 옵션 축약 기능)
    - List segments
    - 현재 작업 중인 디렉토리의 폴더, 파일 목록을 보여준다 
    - <-a> all 옵션. 숨김 파일까지 모두 보여준다 
    - <-l> long 옵션. 용량, 수정 날짜 등 파일 정보를 자세히 보여준다 

- mv : mv text.txt folder
    - 폴더, 파일을 다른 폴더 내로 이동하거나 이름을 변경 
    - 다른 폴더로 이동할 때 작성한 폴더가 반드시 있어야. 없으면 이름이 바뀜
    - 예1) text.txt를 folder 폴더 안에 넣을 때 : mv text.txt folder
    - 예2) text.txt 의 이름을 text2.txt로 바꿀 때 : mv text1.txt text2.txt

- cd : cd folder 
    - Change directory 
    - 현재 작업 중인 디렉토리를 변경하는 명령어 
    - cd ~ 를 입력하면 홈 디렉토리로 이동.(그냥 cd만 입력해도 됨)
    - cd..를 입력하면 부모 디렉토리로 이동(위로 가기)
    - cd -를 입력하면 바로 전 디렉토리로 이동(뒤로 가기)

##### 현재 작업 중인 디렉토리에 있는 folder 폴더로 이동 $ cd folder 
##### 절대 경로를 통한 디렉토리 변경 $ cd C:/Users/kyle/Desktop 
##### 상대 경로를 통한 디렉토리 변경 $ cd ../parent/child

- rm : rm test.txt / rm -r folder 
    - 폴더나 파일을 지우는 명령어 
    - 휴지통 거치지 않고 바로 삭제합니다. 
    - rm *.txt 라고 입력하면 txt 파일 전체를 다 지운다! 아마겟돈~
    -  -r : recursive 옵션. 폴더를 지울 때 사용 

- Start, open 
    - 윈도우에서 폴더/파일을 열 때 : start (start test.txt)
    - 맥에서 폴더/파일을 열 때 : open (open test.txt) 
 
 * ***유용한 단축키들***

    * 위,아래 방향키 : 과거에 작성했던 명령어 조회
    * Tab : 폴더, 파일 이름 자동완성
    * Ctrl + a : 커서 맨 앞으로 이동 
    *  Ctrl + e : 커서가 맨 뒤로 이동 
    * Ctrl + w : 커서가 앞 단어를 삭제 
    * Ctrl + l : 터미널 화면을 깨끗하게 청소 (스크롤 올리면 과거 내역 조회 가능)
    * Ctrl + insert :  복사 
    * Shift  + insert : 붙여넣기 

## 4. Markup
- 마크로 둘러싸인 언어
> ##### 여기서 마크란 글의 역할을 지정하는 일종의 표시 . 예를 들어 HTML에서 M이 의미하는 것은 Markup! 즉 HTML도 마크업 언어다. 

HTML에서 제목을 표시할 때는 `<h1>제목1</h1>` 과 같이 작성허눈대 
제목1을 둘러싸고 있는 `<h1>`을 태그(tag)라고 말하며, 마크 역할을 한다.
각각의 글이 제목, 내용, 목록, 인용 등등 ‘어떤 역할을 가지고 있는지’ 표시하는 것입니다.


## 5. Martkdown
- 일반 텍스트 기반의 경량 마크업 언어.
- 마크업을 더 쉽고 간단하게 사용할 수 있게 만들어둔 게 마크다운 
- 개발과 관련된 많은 문서는 마크다운 형식으로 저장되어 있다.


GIT 기본 명령어 

1.  로컬 저장소  (아래 순서대로 버전 관리를 수행한다) 
- working directory = working Tree : 사용자의 일반적인 작업이 일어나는 곳 
- Staging area = index : 커밋을 위한 파일 및 폴더가 추가되는 곳 
- Repository : staging area에 있던 파일 및 폴더의 변경사항 (커밋)을 저장하는 곳 


2. Git init (git 들어가유! Git 이 관리할게유!) 
> $ git init Initialized empty Git repository in C:/Users/kyle/git-practice/.git/ kyle@KYLE MINGW64 ~/git-practice (master)

- 현재 작업 중인 디렉토리를 git 으로 관리한다는 명령어 
- .git 이라는 숨김폴더를 생성하고 터미널에는 (master)라고 표기된다 

> 주의!
이미 git 저장소인 폴더 내에 또 다른 git 저장소를 만들지 않는다 
터미널에 master 가 이미 있다면 git init 절대금지. 

절대 홈 디렉토리에서 git init을 하지 않는다. 터미널의 경로가 ~인지 확인한다 

3. Git status
> Working directory 와 staging area  에 있는 파일의 현재 상태를 알려줌 
> 어떤 작업을 시행하기 전에 수시로 확인해주면 좋다. 
* 상태
    1. Untracked : Git이 관리하지 않는 파일 (한번도 Staging Area에 올라간 적 없는 파일)
    2. Tracked : Git이 관리하는 파일
        1. Unmodified : 최신 상태
        2. Modified : 수정되었지만 아직 Staging Area에는 반영하지 않은 상태
        3. Staged : Staging Area에 올라간 상태

![파일의 라이프사이클] (Untitled.png)

4. Git add 
# 특정 파일 
$ git add a.txt 
# 특정 폴더 $ git add my_folder/ 
# 현재 디렉토리에 속한 파일/폴더 전부 $ git add .

- Working directory의 파일을 staging area로 올리는 명령어 
- Git 이 해당 파일을 추적 관리할 수 있도록 만들고 
- Untracked, modified->staged 로 상태 변경 

5. Git commit 
- Staging area에 올라온 파일의 변경 사항을 하나의 버전(커밋)으로 저장하는 명령어 
- 커밋 메시지는 변경사항들을 잘 나타낼 수 있게 의미있게 작성하는 것을 권장. 
- 각각의 커밋은 고유의 해시 값을 id 로 가진다. 

6. Git log 
- 커밋의 내역(아이디, 작성자, 시간, 메세지 등)을 조회할 수 있는 명령어 

* --oneline : 한 줄로 축약해서 보여줍니다.
* --graph : 브랜치와 머지 내역을 그래프로 보여줍니다.
* --all : 현재 브랜치를 포함한 모든 브랜치의 내역을 보여줍니다.
* --reverse : 커밋 내역의 순서를 반대로 보여줍니다. (최신이 가장 아래)
* -p : 파일의 변경 내용도 같이 보여줍니다.
* -2 : 원하는 갯수 만큼의 내역을 보여줍니다. (2 말고 임의의 숫자 사용 가능)

![한눈에 보는 git 명령어 ](Untitled.png)

---
git 특강 1일차 끝 

---

