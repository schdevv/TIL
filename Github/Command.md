#### Repository

### 1. Git Clone

1. Git Clone : 원격 저장소에 있는 파일 및 폴더를 로컬 저장소로 연동하는 방법 중 하나이다.
- 커맨드 : git clone [Repository의 주소: 예시) http://github.com/oooo/oooo.git] 
- 연동방법
(1) 원격 저장소에서 새로운 Repository를 생성
(2) Repository의 주소지를 복사
(3) 원하는 로컬 저장소의 위치에서 Git Bash를 통해 커맨드 입력
(4) 로컬 저장소에서 연결된 Repository 확인

- 버전관리 방법
(0) 커맨드: git init
(1) Remote Branch → Local Branch (다운로드)
-커맨드 : git pull origin main
(2) Local Branch → Remote Branch (업로드)
-Local Branch의 업데이트 내용 저장 : git add . 
-Local Branch의 업데이트 내용을 확정함(Github에 표출됨) git commit -m '20230819 13:49 Update TIL(커밋내용)'
-Local Branch의 업데이트 내용 업로드 : git push origin main


|NO|Command|Content|
|---|---|---|
|1|**git clone**|원격 저장소를 로컬 저장소와 연동함|
|2|**git init**|새로운 Git 저장소 생성|
|3|**git add .**|모든 Working Directory의 변경 내용을 Staging Area에 추가함(Staged 상태화)|
|4|**git commit -m 'xxx'**|Staiging Area에 저장된 변경사항을 로컬저장소에 등록함(변경사항 확정)|
|5|**git push origin main**|로컬저장소의 commit된 파일을 모두 원격저정소로 업로드|
|6|**git pull origin main**|원격저장소의 파일을 로컬저장소로 업로드|
|7|**git status**|Working Directory와 Staging Area의 상태를 확인함|
