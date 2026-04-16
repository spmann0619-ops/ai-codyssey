# ai-codyssey

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

#깃허브 연동 증거
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