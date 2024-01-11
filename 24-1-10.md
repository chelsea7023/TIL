# Git
## git과 github의 차이점
* git은 로컬 프로그램
  * Distributed Version Control System - 분산 관리 시스템
  * 컴퓨터 파일의 변경사항을 추적하고 여러 명의 사용자들 간의 작업을 조율
  * 로컬 저장소를 사용하는 명령어 기반의 시스템
  * Linus Torvalds, 2005

* github은 클라우드 서비스 
  * git 프로젝트를 지원하는 웹 호스팅 서비스 
  * 클라우드 서브를 통해 로컬 저장소 (git)의 코드를 업로드하고 공유
  * 코드 관리 및 협업으로 사용

* 버전 관리 시스템
  * vcs 의 장점
    * 각 파일을 이전의 상태로 되돌릴 수 있다
    * 각 프로젝트를 통째로 이전 상태로 되돌릴 수 있다
    * 시간에 따라 수정내용을 비교해볼 수 있다
    * 누가 문제를 일으켰는지 추적할 수 잇다
  * 중앙집중식 버전 관리(CSVS)
    * 한개의 서버에서만 버전 관리
    *  서버가 망가지면 복구가 어려움
   * 분산 버전관리 (DVCS)
     * git과 github에 적용된 시스템
     * 버전 관리를 한 개의 서버에서만 하지 않고 로컬 저장소에서도 함께 관리 
     * 문제가 생기면 복제된 클라이언트 서버로 복원 가능
  
## Git 설정
* local, .git, repository
  * git폴더 이름과 github repositiory 이름이 꼭 같아야 할 필요는 없지만 같으면 좋다.
* git init
  * git을 시작할때 가장 먼저 사용하는 명령어
  * git으로 한 폴더를 버전관리하겠다는 선언
  * git init 후에 가장 기본 브랜치인 (master)가 터미널에 표시됨
  * 아무데서나 사용하면 안되고 git으로 관리할 폴더를 생성하고 사용해야 됨
* git remote
  * git remote add origin <github url>
  * origin은 깃허브의 원격 저장소를 의미
  * 현재 git으로 관리를 선언한 로컬 저장소와 클라우드 호스팅으로 관리할 github의 연결
  * git remote remove origin -> 삭제

## Git 명령어
* git status
* git add
  * staging area로 올리는 명령어
  * . : 전체 파일 올리기
  * 파일 이름. 확장자 : 한 파일 올리기
  * 여러 개의 파일 add라고 싶으면 공백문자(space bar)로 파일 이름 구분
  * 파일 이름에 공백 문자가 잇다면 따옴표로 파일 이름 감싸기 (single/double)
  * git commit
  * staging area에 올린 파일에 메시지 작성
  * -m "message" : 텍스트 에디터에서 별도의 메시지를 작성하지 않아도 인라인 형식으로 바로 커밋 메시지를 작성
  * git push origin <branch>
  * staging area에서 add, commit을 마친 파일 및 폴더들을 repository로 전달