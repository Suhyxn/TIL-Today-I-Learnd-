220329 

## Github 란?
<ul>
<li>Git Repository를 위한 웹 기반 호스팅 서비스 </li>
<li>클라우드 서버를 사용해서 로컬에서 버전 관리한 소스코드를 업로드하여 공유 가능 </li>
<li>분산 버전 제어, 액세스 제어, 소스 코드 관리,  버그 추적, 기능 요청 및 작업 관리를 제공 </li>
</ul>

## Git & GitHub 의 차이 
<blockquote>
Git은 버전 관리 '프로그램'이고 
Github는 버전 관리, 소스 코드 공유, 분산 버전 제어 등등이 가능한 원격 '저장소' 이다.
</blockquote>

### Before Git Start
git --version :  Git 버전 확인 
git 환경설정  :
```
$ git config --global user.name "당신의유저네임"
$ git config --global user.email "당신의메일주소"
$ git config --global core.editor "vim"
$ git config --global core.pager "cat"
```
$ git config --list : 정상 설정 확인
&emsp; &emsp; &emsp;( 수정이 필요할 경우, $ vi ~/.gitconfig 에서 수정 가능 )


## GIT > REPO 를 생성하는 방법

### 1번째 ( Clone 사용 )
GitHub에서 Repo를 설정에 맞게 생성해 준다. <small> (ex.TIL) </small>
```
$ git clone <복사한 repo link>
'TIL'에 복제합니다...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
오브젝트를 받는 중: 100% (3/3), 완료.
```

### 2번째 ( Remote 사용 )
 &emsp;! git init 할 때 다른 디렉토리와 헷갈리지 않도록 꼭 주의
```
$ mkdir first-repo && cd first-repo
$ git init
$ git remote add origin https://github.com/{username}/{reponame}.git
$ touch README.md
$ git add README.md
$ git commit -m "docs: Create README.md"  /* -m 옵션은 사용 자제!*/
$ git push -u origin master /* -u : origin 이라는 원격저장소의 master 브랜치로 연결하여 origin이라는 원격저장소의 master 브랜치를 로컬 저장소의 master 브랜치로 merge 할수 있게 해주겠다는 의미 */
```

## Push와 Commit <small> (ex.README.md) </small>
```
$ git add README.md
$ git commit
$ git push origin master
```

## Commit 할 때 기억해야 할 것
<ul>
<li> commit은 동작 가능한 최소단위로 자주 할 것. </li>
<li> 해당 작업단위에 수행된 모든 파일 변화가 해당 commit에 포함되어야 함. </li>
<li> 모두가 이해할 수 있는 log를 작성할 것. </li>
<li> Open Source Contribution시 영어가 강제되지만, 그렇지 않을 경우 팀 내 사용 언어를 따라 쓸 것. </li>
<li> 제목은 축약하여 쓰되(50자 이내), 내용은 문장형으로 작성하여 추가설명 할 것. </li>
<li> 제목과 내용은 한 줄 띄워 분리할 것. </li>
<li>내용은 이 commit의 구성과 의도를 충실히 작성할 것. </li>
</ul>

## Commit Convention
<ul>
<li> 커밋 제목은 50자 이내로 요약하여 작성한다 </li>
<li> prefix를 사용하여 한 눈에 커밋의 용도를 알기 쉽게 한다 </li>
</ul>
<blockquote>
feat (features) : 새로운 기능 추가  <br/>
docs (documentations) : 문서 수정 <br/>
conf (configurations) : 환경설정 관련 <br/>
test : 테스트 코드, 리펙토링 테스트 코드 추가 <br/>
fix: 버그 수정 <br/>
refactor : 코드 리펙토링 <br/>
ci (continous integration) : 기업 관련 사항 설정 수정 <br/>
build : 빌드와 관련 <br/>
perf (performance) : 성능 개선 <br/>
style : 코드 변경이 없는 경우, 세미콜론 추가 <br/>
chore : (코드의 수정 없이) 설정을 변경 또는 자잘한 수정 <br/>
</blockquote>


