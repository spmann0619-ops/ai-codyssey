# ai-codyssey

'''
## 4. 터미널 기본 조작

### 1) 현재 위치 및 파일 확인

```bash
$ pwd
/home/user

$ ls -la


$ mkdir practice
$ cd practice

$ pwd
/home/user/practice


$ touch file1.txt
$ ls
file1.txt


$ cp file1.txt file2.txt
$ ls
file1.txt file2.txt


$ mv file2.txt renamed.txt
$ ls
file1.txt renamed.txt


$ rm file1.txt
$ ls
renamed.txt


$ echo hello > renamed.txt
$ cat renamed.txt
hello



---

# 🔥 4. 권한 파트도 개선 (추가 추천)

```md
## 5. 파일 권한 변경

```bash
$ ls -l
-rw-r--r-- 1 user user 0 file.txt

$ chmod 755 file.txt

$ ls -l
-rwxr-xr-x 1 user user 0 file.txt
'''