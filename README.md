# Git-Tutorial

git (vs. dropbox) 
- dropbox 크게 두가지로 이루어져있는데 dropbox client / dropbox.com server 
- dropbox client 와 git client 유사함 
- git 은 오픈소스위에서 만들어짐 
- git에서 만들어진 내용들을 git server에 저장하는 것 (여기서 가장 유명한 것이 github) 


git 기본기능 
- git init: 새로운 저장소 생성 
- git add: 파일을 추가함 
- git commit: local repository 로 올리는 것 
- git push: Remote repository 로 올리는 것 
- git fetch: 다른 사람의 작업을 자신의 컴퓨터에 사용
- git merge: 병합 (충돌 발생할 때) // 컴퓨터와 remote 모두에 동일하게 

commit 함으로서 컴퓨터에 적용이 됨. github에는 적용이 안됨.
git push를 통해서 remote repository, github에 올려야 함 

git 프로젝트에 담겨있는 데이터들은 파일 시스템 상에서의 스냅샷이라고 볼 수 있음. 
실제로 프로젝트를 commit 하여 적용할 때의 순간을 중요시함. 파일 자체의 저장 보다는 수정 내역 자체를 저장함 

▶ Working Directory: 작업할 파일이 있는 디렉토리 
▶ Staging Area: 커밋을 수행할 파일들이 올라가는 영역 (커밋 하기 전에 우리는 수정할 때 git add 추가 명령 수행할 때 수행될 추가 명령들만 올라감)
▶ Git Directory: Git 프로젝트들의 메타 데이터와 데이터 정보가 저장되는 디렉토리 

*git의 기본적인 디렉토리 
[실제 github에 반영하기] 
Working Directory – Staging Area – Local Repository – Remote Repository 
우리가 어떤 프로젝트를 추가, 수정 하는 작업을 W.D에서 수행. 
작업이 완료된 내용을 반영하기 위해서는 먼저 Staging Area 에 올리겠다는 의미로 git add. 
올라간 것은 commit 이 이루어지는 파일들. 수정이 덜된 아이들은 나중에 add 하면 됨. 

정상적으로 수정된 아이들은 commit을 이용해서 local repository (컴퓨터의 repository에 올라감, 하지만 github, remote 에는 반영은 안됨) 

그거를 push까지 해야 remote 에까지 반영되는 것 

--------------------------
[github 내용을 컴퓨터로 데이터 반영하고자 할 때] 
다른 사람이 수정한 내용을 우리가 받고자 할 때는 git fetch를 이용하면 다른 사람이 수행한걸 받을 수 있음. 

동시에 동일한 파일을 수정해서 충돌, conflict 가 발생하면 merge를 수행해서 컴퓨터와 리모트가 동일하게 구성될 수 있음. 동기화 하는 것 
-> git fetch + git merge => git pull 

*Repo (저장소) 
▶ 각종 파일, 소스코드, 프로젝트의 메타데이터 등 담겨져 있음 
▶ 각종 데이터, 해시값. (해시값이 왜 사용되느냐 – 각 작업을 분류하기 위해 / 정확한 커밋 내역 관리) 


*git branch 
▶ 동시에 여러 개발자들이 프로젝트에서 각기 다른 기능을 개발할 수 있도록 브랜치 기능을 제공함 
▶ 서로에게 영향받지 않음
▶ 브랜치를 여러개 만들어서 서로 다른 환경에서 서로 다른 작업 가능 
▶ 브랜치 만들면 -> master branch 생성됨. (배포 가능한 버전) 
▶ 특정 지점에서 개발해야 하면 develop branch 만듦. 고쳐야 하면 Bug Fix Branch를 만들어냄. 따로따로 병렬적으로 작업하다가 후에 합침. Merge 시키는 것. 
- 통합 브랜치 = 마스터브랜치
- 토픽 브랜치 = 마스터브랜치를 제외한 브랜치 
