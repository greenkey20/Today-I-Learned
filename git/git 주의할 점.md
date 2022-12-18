## git reset
git reset 옵션에 따라.. 주의하자 ㅜㅜ
- —soft →
- —mixed →
- —hard → 물리적인 파일도 다 삭제됨

git reflog 통해서 어떤 포인트로 되돌릴지 참고 가능 → git reset —hard HEAD^ 하기 전, e.g. 오늘 [Solution27.java](http://Solution27.java) 파일이 있던 때로 돌아감

### References
- [git add/commit/push 취소](https://gmlwjd9405.github.io/2018/05/25/git-add-cancle.html) ← 2022.12.7(수) AWS 배포 자동화 실습하면서 급하게 참고.. 위와 같이 조심해서 사용하지 못함

## 변경 사항 확인
GitHub 원격 저장소 vs local 저장소 변경 사항 있는지 보고 싶을 때
- 원격 저장소에 변경 사항 있는 경우, git fetch로 변경 사항 알아보기 → 필요한 경우 git pull (origin main)
- local 저장소에 변경 사항 있는 경우, git status → 필요한 경우 git add, git commit..

