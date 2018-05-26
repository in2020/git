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

- 
