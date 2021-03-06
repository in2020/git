# git
- git config --list
- index = staging area
- git add : commit할 파일 추가(생성,수정,conflict)
- git status -s
- git diff : staged 상태가 아닌 파일들 수정사항 출력
- git diff --staged(--cached) : staged 상태의 파일 변경 사항 출력
- git commit -a : git add 생략 tracked 파일 commit
- git rm : 파일 삭제사항을 stage에 올림
- git rm --cached : stage에서 삭제
- git mv: mv -> git rm -> git add
- git log -p : show history with diff
- git remote -v : 모든 remote 저장소 출력
- git remote : 현재 remote 저장소 출력
- git remote add :  remote 저장소 추가
- git checkout -- : 변경사항 삭제
- origin : remote 저장소 이름 일뿐... 
- git remote rename, git remote rm
- git tag tag_name sha1, git push tag_name git push --tags
- git checkout -b branch_name tag_name
- git config --global alias.co checkout
- master 브랜치는 특별하지않다. 굳이 다른 이름으로 바꾸지 않는 것 뿐
- git brach -b branch_name origin/master
- git brach -u origin/master
- 두개의 브랜치를 합치는 방법은 두가지 1.merge 2.rebase rebase가 히스토리가 깔끔하게 나타난다. git rebase master -> git merge branch1
- rebase의 위험성 : push한  commit을 rebase하지마라
- git merge --squash brach_name : 머지시 커밋을 하나의 커밋으로 합쳐 merge
- git clean -fd : stage에 올라가지 않은 파일 
- git reset [option] HEAD^ : HEAD^ === HEAD^1 하나전 parent로 reset

## 기존 프로젝트를 원격 저장소에 업로드 하는 방법
```
git init 
git remote add <remote name> <remote url>
git fetch 
git --set-upstream <remote name> <branch>
git pull --allow-unrelated-histories
git push
```
## tag 정렬
```
git tag -l --sort=v:refname
git tag -l --sort=-v:refname #reverse
```
## git alias
```
git config --global alias.tl 'git tag -l --sort=-v:refname'
```
## 윈도우10 git symbolic link 적용 방법
- [윈도우10 개발자 모드 설정](http://codedragon.tistory.com/3874)
- [git 설치 시 enable symbolic link 옵션 선택](https://i.stack.imgur.com/rQF1w.png)
- [git clone 옵션 추가 ]
```
git clone -c core.symlinks=true [url]
```
