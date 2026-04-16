
# AI Codyssey - 개발 워크스테이션 구축

## 1. 프로젝트 개요
터미널, Git, Docker를 활용하여 개발 워크스테이션 환경을 구축하는 과제이다.  
터미널 기본 조작, 파일 권한 관리, GitHub 연동, Docker 컨테이너 실행 및 검증 과정을 수행하며 재현 가능한 개발 환경 구성을 목표로 한다.

---

## 2. 실행 환경
- OS: macOS
- Shell: zsh
- Terminal: VSCode Terminal
- Git: 2.53.0
- Docker: (docker --version 결과 입력)

---

## 3. 수행 체크리스트

- [x] 터미널 기본 조작
- [x] 파일 권한 변경 실습
- [x] Git 설정
- [x] GitHub 저장소 생성 및 연동
- [x] README 작성 및 Push
- [ ] Docker 설치 및 점검
- [ ] hello-world 실행
- [ ] Dockerfile 빌드
- [ ] 포트 매핑 검증
- [ ] 볼륨 영속성 검증
- [ ] 트러블슈팅 2건 이상

---

## 4. 터미널 기본 조작

### 현재 위치 확인

```bash
$ pwd
(결과 입력)

'''
## 4. 터미널 기본 조작

### 1) 현재 위치 및 파일 확인

```bash
$ pwd
/Users/spman06195118

결과: pwd 명령어를 사용해 현재 위치를 확인하였다. 절대 경로를 보여준다.


$ ls -la
total 24
drwxr-x---+ 23 spman06195118  spman06195118   736 Apr  5 20:57 .
drwxr-xr-x   9 root           admin           288 Apr  5 19:32 ..
-r--------   1 spman06195118  spman06195118     7 Apr  5 19:32 .CFUserTextEncoding
drwxr-xr-x   5 spman06195118  spman06195118   160 Apr  5 19:34 .docker
drwxr-xr-x  11 spman06195118  spman06195118   352 Apr  5 20:51 .git
-rw-r--r--   1 spman06195118  spman06195118    38 Apr  5 20:57 .gitconfig
drwxr-xr-x  10 spman06195118  spman06195118   320 Apr  5 19:34 .orbstack
drwxr-xr-x   3 spman06195118  spman06195118    96 Apr  5 19:34 .ssh
drwx------+  2 spman06195118  spman06195118    64 Apr  5 19:33 .Trash
drwxr-xr-x   5 spman06195118  spman06195118   160 Apr  5 20:38 .vscode
-rw-------   1 spman06195118  spman06195118   201 Apr  5 20:50 .zsh_history
drwx------   3 spman06195118  spman06195118    96 Apr  5 20:38 .zsh_sessions
drwx------+  3 spman06195118  spman06195118    96 Apr  5 19:32 Desktop
drwx------+  3 spman06195118  spman06195118    96 Apr  5 19:32 Documents
drwx------+  4 spman06195118  spman06195118   128 Apr  5 20:36 Downloads
drwx------@ 79 spman06195118  spman06195118  2528 Apr  5 19:52 Library
drwx------   3 spman06195118  spman06195118    96 Apr  5 19:32 Movies
drwx------+  3 spman06195118  spman06195118    96 Apr  5 19:32 Music
drwx------   4 spman06195118  spman06195118   160 Apr  5 19:34 OrbStack
drwx------+  4 spman06195118  spman06195118   128 Apr  5 19:33 Pictures
-rw-r--r--   1 spman06195118  spman06195118     0 Apr  5 20:39 projects
drwxr-xr-x   5 spman06195118  spman06195118   160 Apr  5 21:18 projectss
drwxr-xr-x+  4 spman06195118  spman06195118   128 Apr  5 19:32 Public

결과: ls -la 명령어를 사용해 숨겨져 있는 파일을 포함해서 상세 정보를 확인하였다.


$ mkdir practice
$ cd practice

$ pwd
/Users/spman06195118/practice

결과: mkdir 명령어를 사용해 practice라는 디렉토리를 만들고 cd 명령어를 사용해 현재 위치를 practice로 이동하였다.
 pwd 명령어를 사용해 위치가 변경된 것을 확인하였다.


$ touch file1.txt
$ ls
file1.txt

결과: touch 명령어를 사용해 빈 파일을 생성하였다. ls 명령어를 사용해 파일이 생성된 것을 확인하였다.


$ cp file1.txt file2.txt
$ ls
file1.txt file2.txt

결과: cp 명령어를 사용해 기존 파일을 복사하여 새로운 파일을 생성항였다. ls 명령어를 사용해 파일이 복사된 것을 확인하였다.


$ mv file2.txt renamed.txt
$ ls
file1.txt renamed.txt

결과: mv 명령어를 사용해 파일의 이름을 변경하였다. ls 명령어를 사용해 파일이 변경된 것을 확인하였다.


$ rm file1.txt
$ ls
renamed.txt

결과: rm 명령어를 사용해 파일을 삭제하였다. ls 명령어를 사용해 파일이 삭제되었는지 확인하였다.


$ cat renamed.txt

결과: cat 명령어를 사용해 파일을 실행하였다. 파일이 비어있어 아무 것도 실행되지 않았다.




---

# 🔥 4. 권한 파트도 개선 (추가 추천)

```md
## 5. 파일 권한 변경

```bash
$ ls -l
-rw-r--r--  1 spman06195118  spman06195118  0 Apr  5 21:54 renamed.txt

결과: ls -l 명령어를 사용해 권한을 확인하였다.


$ chmod 755 renamed.txt

결과: chmod 명령어를 사용해 644였던 파일 권한을 755로 변경하였다.

의미: 755는 소유자에게 rwx 권한을 부여하고 그룹과 기타 사용자에게는 rx 권한을 부여한다. 
r = 4, w = 2, x = 1 을 뜻하고 이를 더한 값으로 나타낸다. 맨 앞자리는 소유자, 두번 째자리는 그룹, 마지막자리는 기타 사용자를 의미한다. 


$ ls -l
-rwxr-xr-x  1 spman06195118  spman06195118  0 Apr  5 21:54 renamed.txt

결과: ls -l 명령어를 사용해 권한이 변경되었는지 확인하였다.
'''

#깃허브 설정 증거
'''
spman06195118@c4r7s7 project % git config --list
credential.helper=osxkeychain
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
core.ignorecase=true
core.precomposeunicode=true
user.name=JH
user.email=your@email.com
'''

#깃허브 연동 증거
'''spman06195118@c4r7s7 ai-codyssey % git remote -v
origin  https://github.com/spmann0619-ops/ai-codyssey (fetch)
origin  https://github.com/spmann0619-ops/ai-codyssey (push)
'''

## 트러블슈팅 1. Git Push가 되지 않은 문제

### 문제
README.md 파일을 수정한 뒤 git push를 실행했지만 GitHub 저장소에 변경 내용이 반영되지 않았다.

### 원인 가설
파일 내용을 수정했지만 저장하지 않아 Git이 변경 사항을 인식하지 못했을 가능성이 있다고 판단하였다.

### 확인

```bash
$ git status
nothing to commit, working tree clean

###해결
$ git add .
$ git commit -m "README 수정"
$ git push