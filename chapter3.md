# Chapter 3. 오픈소스 개발 도구

- ## 이슈트래커

### 1. 이슈 관리

우리가 프로젝트를 개발할 때 프로젝트 관리에서는 **이슈 관리(Issue Management), 위험 관리(Risk Mangagement)** 등의 용어가 자주 사용됩니다. 프로젝트 관리에서 이야기하는 **위험(Risk)**은 다음과 같이 정의됩니다.

```
-아직 발생되지 않았으나 발생될 가능성이 있는 것
-발생될 경우, 프로젝트에 차질을 가져올 수 있는 것
-하지만, 적절히 대처할 경우, 기회가 될 수도 있는 것
```

그리고 **이슈(Issue)**는 다음과 같이 정의됩니다.

```
-프로젝트 진행에 차질을 가져올수 있는 "발생된 위험"
```

또한 미리 예상해 두 지 못했던 문제점이나 하고 싶은 것, 요청하는 것, 삭제해야 할 것 등 다양한 주제가 될 수 있습니다.  

프로젝트를 진행하면서 갖가지 위험은 피해 갈 수 있지만, 이슈는 이미 발생해 버린 문제점이기 때문에 어떻게든 해결이 되어야 합니다. 그 문제점이 버그일수도 있고, 기능 구현일 수도 있습니다. 그래서 **이슈는 버그, 기능 구현 등을 포함한 업무의 단위**로 볼 수 있습니다. 그래서 이슈는 담당자 한 사람이 맡아서 해결할 수 있도록 구체적으로 설정하는 것이 좋습니다. 

 이러한 이슈들을 **목록으로 정리**하고, **우선 순위**를 정하고, **담당자를 지정**하고, **해결 상황을 체크**하는 일련의 행위를 바로 **이슈 관리**라고 합니다. 

### 2. 이슈 관리 시스템

이슈 추적 시스템(Issue tracking system, ITS)은 단체의 필요에 의해 이슈목록을 관리하고 유지보수하는 컴퓨터 소프트웨어의 일종입니다.  즉, 이슈관리를 적절히 할 수 있도록 만들어진 툴입니다. 이러한 이슈 관리 시스템을 사용하는 도구를 **이슈 트래커**라고 합니다. 버그, 요구사항, 작업내용 등의 이슈들을 해당 시스템에 게시물 형태로 올리고 개발자, 테스터 들이 작업 진행상황을 기록하는 시스템입니다.

이슈는 다양한 추가 정보를 가지며, 이 정보들을 다양한 주체가 업데이트 하면서 이슈들을 관리하는 것이 이슈 트래커의 주된 기능입니다. 이슈가 어떤 정보들을 가지고 있는지는 이슈 트래커의 종류에 따라 차이가 있지만 일반적으로 다음과 같습니다.

* **담당자** :  이슈를 해결할 사람
* **우선 순위**:  이슈의 우선 순위. 담당자는 우선순위가 높은 이슈부터 해결하는 것이 원칙.
* **마감일**: 이슈가 반드시 이 날까지 해결되어야 하는 경우 집어넣기도 합니다. 
* **상태**: 기본적으로 열림/닫힘(open/close)로 구분하고 그 외에 세부적인 상태(작업 시작, 수정됨, 재현 불가 등)를 가지고 있기도 합니다.

이슈 트래커는 인터넷 게시판과 비슷한 형태를 하고 있으며, 해당 이슈의 속성을 지정하고 내용을 올립니다.  이슈가 해결되지 않은 상태가 열린 이슈이며, 이슈에 대한 작업이 진행되면 작업결과를 답글 형식으로 올립니다. 이슈에 대한 작업이 모두 끝나면 이슈를 닫습니다.  이미 해결한 이슈여도 문제가 생겼을 경우 다시 열 수 있습니다(Reopen). 또는 보류(Pending)할 수도 있습니다.

일반적인 이슈 관리 시스템의 사용 흐름은 대략적으로 다음과 같습니다.

* **이슈 등록** : 사용자 혹은 품질관리팀이 발견한 버그 혹은 신규 기능을 추가합니다. 담당자를 지정하기도 하고, 공란으로 두기도 합니다. 
* **이슈 검토/분류** :  등록된 이슈는 개발팀이 검토합니다. 중복, 재현 불가, 해결 불가능한 이슈의 경우 이 단계에서 이슈를 닫습니다. 개발팀에서 해결할 이슈의 경우 담당자. 우선순위, 마감일 등을 지정합니다.
* **이슈 해결 ** : 이슈가 해결되면 이슈를 닫습니다. 담당자와 별개로 검증 담당자를 따로 두어 진짜로 이슈가 해결되었는지 검증하는 경우도 있다. 

자세한 사용방법은 아래 

### 3. 이슈 관리 시스템의 필요성

소프트웨어를 개발하다 보면 일반적인 기능 구현 작업과 함께 버그 수정과 요구하항 반영 작업을 많이 하게 됩니다. 오픈 소스 프로젝트는 주로 원격으로 이루어지기 때문에 적합한 커뮤니케이션 방식을 필요로 합니다.  이슈 관리 시스템을 사용하지 않고 개발하는 경우 버그나 요구사항을 엑셀 파일에 저장하여 관리하는 경우가 많습니다. 그리고 이메일이나 메시지 등으로 공유하곤 합니다. 혹은 엑셀 파일에 조차 버그와 요구사항을 기록하지 않는 경우도 많습니다.

이슈 관리 시스템의 가장 큰 특징은 **변경 이력이 다 남는다**는 것입니다.  누군가가 제 때 완료하지 못한 이슈를 지워버리거나 축소/은폐하기 어렵습니다. 또한 **저장된 속성**을 사용하여 필터링이나 통계 등을 활용할 수 있어 프로젝트 진행상황을 일목요연하게 확인할 수 있습니다. 세부적인 기능들을 버그 처리 기능과 이슈 처리 기능 및 편의 기능으로 나누어서 살펴보면 다음과 같습니다.

* **버그 처리 기능**

```
- 다양한 항목에 대한 버그 제출 및 검색 기능
- 패치(Patch), 첨부 파일 제공 기능
- 변경 이력 및 이에 대한 메일링 기능
```

* **이슈 처리 기능**

```
- 기능상 개선 사항 포함
- 마일스톤(milestone)에 관련된 이슈에 대한 처리도 가능
```

* **편의 기능**

```
- 게시판 형태로 웹에서 쉽게 조회 가능
- 저장된 속성으로 여러 통계 자료 얻을 수 있음
```

[^마일스톤(milestone)]: 프로젝트 진행 과정에서 특기할 만한 사건이나 이정표.
[^패치(Patch)]: 소프트웨어의 버그 등을 수정하는 것.

따라서 이슈 관리 시스템을 잘 활용하는 것이 오픈소스 프로젝트 개발에 중요한 요소입니다. 

### 4. 이슈트래커의 종류

이슈관리시스템은 대부분 버그관리시스템(Bug Tracking System, BTS)에서 출발 하였으나, 단순히 버그 뿐 아니라 다양한 이슈를 관리할 수 있도록 의미가 확장되고 있습니다. 

이슈트래커는 개발자와 테스터, 기획자, 운영자 모두의 상호 소통을 위한 도구입니다. 버그 수정 누락 방지와 버그 개선 및 개발 사항을 물어보지 않고도 실시간으로 파악하는데 도움을 줍니다. 따라서 시스템을 도입 이 후부터는 업무를 직접 대화하거나 메신저로 했던 부분을 시스템에 모두 기록을 해야만 합니다.

그리고 한가지 선택에 있어서 중요한 부분이 있는데, 커스텀마이징이 쉽거나 개선 할수 있는 언어로 작성된 시스템을 선택해야 합니다. 즉, 이슈 트래커를 잘 선택하는 것이 아주 중요합니다. 대표적인 이슈트래커는 다음과 같습니다.

#### Redmine

|  로고   | ![redmine](data:image/png;base64,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) |
| :---: | :--------------------------------------: |
| 라이선스  |               오픈소스(GNU v2)               |
| 개발 언어 |                   Ruby                   |
| 홈페이지  |          http://www.redmine.org          |
|  개발자  |            Jean-Philippe Lang            |

**특징**:

- 다중 프로젝트 지원
- 유연한 역할기반 접근제어
- 유연한 이슈추적 기능
- 간트차트와 달력기능 제공
- 알림, 문서, 파일관리기능 제공
- 이메일 알람기능
- 프로젝트별 위키 페이지 제공
- 프로젝트별 게시판 기능 제공
- 형상관리 소프트웨어와의 통합(SVN, CVS, Git, Mercurial, Bazaar, Darcs)
- 다중 LDAP 기반 인증 지원
- 다국어 지원
- 여러 데이터베이스 지원
- 플러그인 기능 지원



#### Mantis

|  로고   | ![mantis](https://www.mantisbt.org/images/mantis_logo_262x90.png) |
| :---: | :--------------------------------------: |
| 라이선스  |               오픈소스(GNU v2)               |
| 개발 언어 |                   PHP                    |
| 홈페이지  |         http://www.mantisbt.org          |
|  원작자  |              Kenzaburo Ito               |

**특징**:

* 각각의 작업이나 전체 프로젝트에 대해서 작업 진행 상태를 도식화 가능
* 프로젝트 변경 이력에 대한 추적/관리 및 유지보수
* 프로젝트 참여자들의 작업 내용을 추가/보고/관리



#### Trac

|  로고   | ![trac](https://www.edgewall.org/gfx/trac_logo.png) |
| :---: | :--------------------------------------: |
| 라이선스  |                오픈소스(BSD)                 |
| 개발 언어 |                  Python                  |
| 홈페이지  |         http://trac.edgewall.org         |
|  개발자  |                엣지월 소프트웨어                 |

**특징**:

* 버전 관리 소프트웨어의 웹 인터페이스 제공
* 개선점과 버그와 같은 프로젝트의 이슈 트래킹
* 위키를 통한 문서 관리 및 각 리소스 연동

#### Jira

|  로고   | ![jira](https://wac-cdn.atlassian.com/dam/jcr:e348b562-4152-4cdc-8a55-3d297e509cc8/Jira%20Software-blue.svg?cdnVersion=hh) |
| :---: | :--------------------------------------: |
| 라이선스  |                오픈소스(BSD)                 |
| 개발 언어 |                   JAVA                   |
| 홈페이지  | https://www.atlassian.com/software/jira  |
|  개발자  |                  아틀라시안                   |

**특징**:

* 맞춤 필터
* 개발자 도구 통합
* 3000개 이상의 앱
* 모든 작업 스타일에 매핑되는 사용자 지정 가능한 워크 플로 만들기 가능
* 풍부하고 강력한 API
* 자체 호스팅 및 클라우드 옵션

#### Bugzilla

|  로고   | ![jira](https://wac-cdn.atlassian.com/dam/jcr:e348b562-4152-4cdc-8a55-3d297e509cc8/Jira%20Software-blue.svg?cdnVersion=hh) |
| :---: | :--------------------------------------: |
| 라이선스  |                모질라 공용 허가서                |
| 개발 언어 |                   Perl                   |
| 홈페이지  |         http://www.bugzilla.org/         |
|  개발자  |                  모질라재단                   |

**특징**:

* 향상된 성능 및 확장성을 위한 최적화 된 데이터베이스 구조
* 기밀 유지를 위한 탁월한 보안성
* 편집 가능한 사용자 프로필 및 포괄적인 전자 메일 기본 설정
* 사용자 정의 워크플로우, 필드
* 고도로 사용자 정의 가능한 확장 메커니즘



#### 그 외 이슈 트래커

- [Request Tracker](http://bestpractical.com/rt/) (라이센스: GPL v2)
- [The Bug Genie](http://www.thebuggenie.com/) (라이센스: MPL)
- [WebIssues](http://webissues.mimec.org/) (라이센스: GPL v3)
- [ChiliProject](https://www.chiliproject.org/) (라이센스: GPL v2)




- ## 버전컨트롤

### 1. 버전 컨트롤 소개

버전 관리 시스템은 **파일의 변화를 시간에 따라 기록하여 과거 특정 시점의 버전을 다시 불러올 수 있는 시스템**입니다. 모든 컴퓨터 파일이 버전 관리의 대상이 될 수 있습니다. 이미지나 레이아웃을 수정할 때마다 각각의 형태를 모두 보존하고 싶은 그래픽 디자이너나 웹 디자이너라면 버전 관리 시스템(Version Control System; VCS)을 사용하는 것이 현명할 수 있습니다. VCS를 사용하면 개별 파일 혹은 프로젝트 전체를 이전 상태로 되돌리거나 시간에 따른 변경 사항을 검토할 수 있으며, 문제가 되는 부분을 누가 마지막으로 수정했는지, 누가 언제 이슈를 만들어냈는지 등을 알 수 있습니다. 또한 파일을 잃어버리거나 무언가 잘못되어도 대개 쉽게 복구할 수 있습니다. 그리고 이 모든 장점을 누리는 데는 큰 노력이 들지 않습니다.

버전 컨트롤을 사용하는 이유를 정리하면 다음과 같습니다.

* 단일 변경 기록으로 이력 추적
* 파일 버전 관리
* 릴리스 버전 관리
* 단일 백업 지점 관리
* 적극적 리팩토링 가능 (소스 롤백 가능)
* 일관된 반복 빌드 가능
* 병렬 개발 및 팀 커뮤니케이션 가능

버전 관리하고자 하는 문서의 변경 사항들에 숫자나 문자로 이뤄진 ("개정판 번호"나 "개정판 레벨"이라고도 불리는) "버전"을 부여해서 구분합니다. "버전"을 통해서 시간적으로 변경 사항과 그 변경 사항을 작성한 작업자를 추적할 수 있습니다.

간단한 버전 관리 방법으로는 처음 작성한 코드에 버전 번호 1을 부여합니다. 변경 사항이 생기면, 버전 번호를 2로 증가 시킵니다. 이처럼 추후 변경 사항이 발생 시마다 버전 번호를 1씩 증가시킵니다. 

이처럼 버전 관리 소프트웨어 도구들은 거의 모든 소프트웨어 개발 프로젝트에서 필수적인 요소로 인식되고 있습니다.

### 2. 중앙 집중형 버전 컨트롤

중앙집중식 버전 관리 시스템(Centralized Version Control System; CVCS)은 시스템 외부에 있는 개발자들과 함께 작업하는 문제를 해결하기 위해 개발되었습니다. **CVS, Subversion, Perforce**와 같은 시스템들이 여기에 속합니다. CVCS에서는 버전 관리되는 모든 파일을 저장하는 하나의 서버와, 이 중앙 서버에서 파일들을 가져오는(checkout) 다수의 클라이언트가 존재합니다. 오랫동안 사용된 이 방식은 지금까지도 버전 관리의 대표적인 방식입니다.

CVCS는 로컬 VCS에 비해 장점이 많습니다. 누구나 다른 사람들이 무엇을 하고 있는지 알 수 있고, 관리자는 누가 무엇을 할 수 있는지 꼼꼼하게 관리할 수 있습니다. CVCS를 관리하는 것은 수많은 클라이언트의 로컬 데이터베이스를 관리하는 것보다 훨씬 쉽습니다. 

그러나 CVCS는 심각한 단점이 있습니다. 중앙 서버가 잘못되면 모든 것이 잘못된다는 점이죠. 서버가 다운될 경우 서버가 다시 복구될 때까지 다른 사람과의 협업도, 진행 중이던 작업을 버전 관리하는 것도 불가능해집니다. 중앙 데이터베이스가 저장된 하드디스크에 오류가 발생하고 백업도 없다면, 사람들이 각자 자신의 컴퓨터에 가지고 있던 스냅샷 외에는 그동안 쌓인 프로젝트의 이력을 모두 잃게 됩니다. 로컬 VCS 시스템도 같은 문제가 있습니다. 프로젝트의 모든 이력이 한곳에만 있을 경우 이것은 피할 수 없는 문제인 것이죠.

대표적인 중앙 집중형 버전 관리 시스템은 다음과 같이 CVS, Subversion이 있습니다.

* CVS

CVS(Concurrent Versions System)은 보통 소프트웨어 프로젝트를 진행할 때, 파일로 이뤄진 모든 작업과 모든 변화를 추적하고, 멀리 떨어진 개발자들도 서로 협력하여 작업할 수 있게 합니다. CVS는 GNU 일반 공중 사용 허가서 하에서 배포되며, 오픈 소스 프로젝트에서 널리 사용됩니다. 현재는 CVS가 한계를 맞아, Subversion이 개발되었습니다.

CVS는 몇 가지 한계를 가지고 있습니다.  

```
- 저장소의 파일 이름을 바꿀 수 없음(제거하고 나서 다시 추가해야함)
- CVS 프로토콜은 디렉토리의 이동이나 이름 변경을 허용하지 않음
- 서브 디렉토리의 파일은 모두 지우고 다시 추가해야 함
- 아스키 코드로 된 파일 이름이 아닌 유니코드 파일을 제한적으로 지원함
```

CVS를 만들었던 핵심 개발자들 몇몇이 이런 CVS의 한계를 깨닫고 다음에 소개할 Subversion(SVN)을 개발하였습니다.

* Subversion

서브버전은 오픈소스 커뮤니티에 잘 알려져있고, Apache Software Foundation, KDE, GNOME, Free Pascal, GCC, Python, Ruby, Samba, Mon와 같은 많은 오픈 소스 프로젝트에 사용되고 있습니다. CVS와 비교했을 때, 서브 버전의 장점은 다음과 같습니다.

```
- 원자적으로 쓰기를 지원하므로, 다른 사용자의 쓰기와 엉키지 않음
- 이름을 바꾸거나, 복사하거나, 파일을 지워도 리비전 기록을 유지함
- 바이너리 파일도 효율적으로 저장할 수 있음
- 디렉토리도 버전 관리를 할 수 있음(디렉토리 전체를 빠르게 옮기거나 복사할 수 있으며, 리비전 기록도 그대로 유지됨)
- 소스 저장소의 크기에 상관없이 일정한 시간 안에 branching이나 tagging을 할 수 있음
- 소스 저장소로의 접근이 최적화되어 필요없는 네트워크 트래픽을 줄일 수 있음
```

### 3. 분산형 버전 컨트롤

분산 버전 관리 시스템(Distributed Version Control System; DVCS)은 앞서 말한 문제를 해결하기 위해 개발되었습니다. Git, Mecurial, Bazaar, Darcs 등 DVCS에서는 클라이언트가 파일들의 마지막 스냅샷을 가져오는 대신 저장소(repository)를 통째로 복제합니다. 따라서 서버에 문제가 생겨도 어느 클라이언트든 복제된 저장소를 다시 서버로 복사하면 서버가 복구됩니다. 체크아웃(checkout)을 할 때마다 전체 백업이 일어나는 셈이죠

게다가 대부분의 DVCS에서는 다수의 원격 저장소(remote repository)를 갖는 것이 가능하기 때문에 동시에 여러 그룹과 여러 방법으로 함께 작업할 수 있습니다. 이로 인해 계층 모델(hierarchical model) 등 중앙집중 시스템에서는 할 수 없는 다양한 작업 방식(workflow)들을 사용해볼 수 있습니다.

대표적인 분산형 버전 관리 시스템으로는 다음과 같습니다.

* Mercurial

머큐리얼은 소프트웨어 개발을 위한 크로스 플랫폼 분산 버전 관리 툴입니다. 머큐리얼의 대부분은 파이썬으로 개발되었으며, diff부분은 c를 사용해서 개발되었습니다. 머큐리얼은 기본적으로 명령 줄 인터페이스 프로그램입니다. 모든 명령은 hg로 시작하는데, hg는 수은의 원소 기호이죠.

머큐리얼이 궁극적으로 추구하는 것은 고도의퍼포먼스와 스케일러빌리티입니다. 다시말해, 서버가불필요해야하며(serverless), 분산된(distributed) 협동 개발 플랫폼 형태이어야 합니다. 또한 플레인텍스트 및 바이너리 파일들을 견고히(robustly) 지원해야합니다. 기술적으로 진보된 브랜칭(branching)과 머징(merging) 기능도 가지고있되, 개념적으로는 간결해야합니다. 머큐리얼은 통합 웹 인터페이스를 포함하고 있습니다. 

머큐리얼의 소스 코드는 GNU 일반 공중 사용 허가서 하에 배포됩니다. 머큐리얼의 장점은 웹 기반 인터페이스가 뛰어나다는 점입니다. 소스 코드 뷰어나 체크인 기록등을 모두 볼 수 있으며, 다양한 방식으로 개발 이력을 추적할 수 있습니다.

* Git

Git은 리누스 토르발스가 Subversion을 쓰다가 화가 난 나머지 2주만에 만든 분산형 버전 관리 프로그램입니다. 처음에는 토르발스가 리눅스 커널 관리를 위해서 개발한 것인데, 현재는 다른 곳에도 널리 사용되고 있습니다. 매우 빠른 속도와 분산형 저장소 지원이 특징입니다. 오픈소스 개발의 특성상 여럿이 달려들어 자기 맘에 드는걸 하기도 하며, 또한 뭘 하나 잘못 붙였다 이상한 걸 건드려 망하기 쉬운데, Git는 이런 환경의 특성에 맞게끔 잘 만들어져 있습니다. Git 자체는 오픈소스이며 저장소는 <https://github.com/git/git>입니다.

Git는 다음과 같은 체제를 갖고 있습니다. 일단 Git의 작업 폴더는 전체 기록과 각 기록을 추적할 수 있는 정보를 포함하고 있는 저장소입니다. 즉 자기 컴퓨터에 모든 파일을 다 받아서 하는 셈 입니다.

작업이 끝나면 Git 원격 저장소로 다시 발행하는데, 여기에도 원 저장소를 보호하기 위한 가지치기가 있어 가지의 개발이 완료될 시 원 저장소와 합칠 수 있으며, 또한 개발 중간중간 꼬리표를 매겨 개발을 더 수월하게 할 수 있습니다.

어쩌면 리누스 토르발스가 리눅스를 개발하지 않았더라도, Git을 개발함으로 인해서 존경을 받았을지 모릅니다. 오픈소스는 공산주의라고 혹평하던 마이크로소프트와 트위터, 모질라 재단등에서도 Git를 잘 사용하고 있습니다. 윈도우의 경우 현재 90%까지 Git 처리가 완료되었는데, 하루 8500건의 커밋과 더불어 1760번의 빌드를 거친다고 합니다. 

이러한 강력한 Git을 호스팅해주는 Github란 서비스가 있어, 영리적인 서비스와 오픈소스를 위한 무상 서비스를 모두 제공하고 있습니다. 

### 참고 문서

- [Comparison of issue-tracking systems](http://en.wikipedia.org/wiki/Comparison_of_issue-tracking_systems)
- [Issue tracking system](http://en.wikipedia.org/wiki/Issue_tracking_system)
- [Bug Tracking system](http://en.wikipedia.org/wiki/Bug_tracking_system)
- [https://yckim.wordpress.com/2010/02/05/%EC%9D%B4%EC%8A%88%EA%B4%80%EB%A6%AC%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80/](https://yckim.wordpress.com/2010/02/05/%EC%9D%B4%EC%8A%88%EA%B4%80%EB%A6%AC%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80/)
- [https://ko.wikipedia.org/wiki/%EC%9D%B4%EC%8A%88_%EC%B6%94%EC%A0%81_%EC%8B%9C%EC%8A%A4%ED%85%9C](https://ko.wikipedia.org/wiki/%EC%9D%B4%EC%8A%88_%EC%B6%94%EC%A0%81_%EC%8B%9C%EC%8A%A4%ED%85%9C)
- [https://www.ibm.com/developerworks/community/blogs/9e635b49-09e9-4c23-8999-a4d461aeace2/entry/238?lang=en](https://www.ibm.com/developerworks/community/blogs/9e635b49-09e9-4c23-8999-a4d461aeace2/entry/238?lang=en)
- [https://namu.wiki/w/%EC%9D%B4%EC%8A%88%20%ED%8A%B8%EB%9E%98%EC%BB%A4](https://namu.wiki/w/%EC%9D%B4%EC%8A%88%20%ED%8A%B8%EB%9E%98%EC%BB%A4)