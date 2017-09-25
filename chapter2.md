# 오픈소스의 역사



## 1. 초기의 자유 소프트웨어

1950~60년대엔 거의 모든 소프트웨어들이 학자들과 기업의 연구자들의 공동작업으로 만들어졌고, 주로 공용 도메인 소프트웨어로 공유되었습니다. 따라서 오랫동안 확립된 공개와 협력의 원칙하에 배포되었고, 소프트웨어 자체가 상품으로 취급받진 않았습니다. 이 때에 사람이 읽을수 있는 형태의 소스코드는 소프트웨어와 함께 배포되었습니다. 왜냐하면 사용자들이 하드웨어나 OS에 따라 실행되지 않는 경우도 있었고, 버그 수정이나 기능 추가를 위해서 소프트웨어를 자주 수정해야 했기 때문이였습니다. 특히 IBM의 거의 모든 소프트웨어들이 소스코드와 함께 배포되었고, 사용자들이 SHARE와 같은 그룹을 형성해서 소프트웨어를 교환했습니다. 

하지만 1960년대 후반에 들어서면서 OS와 프로그래밍 언어 컴파일러는 진화하기 시작했습니다. 결국 소프트웨어 생산비용은 하드웨어에 비해 급격히 증가했고 하드웨어 제조업체끼리의 경쟁이 심화되면서 제한된 라이선스로 판매되는 소프트웨어들이 증가했습니다. 1970년대 후반과 1980년대 초반에 컴퓨터 벤더와 소프트웨어 전문 회사들은 라이선스에 비용을 부과한 후 소프트웨어를 "프로그램 제품" 으로 마케팅하고 저작권이나 상표를 이용해 새로운 소프트웨어 개발에 법적 제한을 가하기 시작했습니다. 1983년에 IBM은 더이상 소스코드를 배포하지 않겠다고 발표했습니다.

## 2. 자유 소프트웨어 운동과 GNU프로젝트 

리차드 스톨만(Richard Stallman, 1953~ )은 당시 MIT의 인공지능 연구소에 근무하던 유능한 프로그래머였습니다. 그는 연구소에서 일하던 동료 프로그래머들이 하나씩 돈을 벌기 위해 떠나고, 그들이 소프트웨어 저작권과 돈 때문에 분쟁에 시달리는 것을 보고 현재의 상업적 소프트웨어 경제 시스템의 문제점을 통감합니다. 스톨만은 1970년대 소프트웨어가 컴퓨터 하드웨어로부터 떨어져 나오면서 상업적인 제품으로 팔리기 시작한 것은 지극히 잘못된 일이라고 주장했습니다. 그는 모든 소프트웨어는 무제한 공유되고 무료로 배포돼야 한다는 주장과 함께, MIT를 떠나 상업용 소프트웨어와의 전쟁을 선포합니다. 

그는 1983년에 자유 소프트웨어 운동(free software movement)을 시작하고 자유 소프트웨어 재단(Free Software Foundation)을 설립했습니다. 이 운동의 목적은 사람들이 서로 협력하는 것을 막는 사유 소프트웨어를 반대하고 사람들이 소프트웨어를 자유롭게 사용하고, 읽고, 수정하고, 재배포 할수 있도록 하는 것이었습니다. 그는 자유 소프트웨어 개발 프로젝트인 GNU프로젝트를 시작하므로서 자유 소프트웨어 운동의 공식적인 시작을 알렸습니다. 스톨만과 프로그래머들은 시스템 소프트웨어를 만들기 시작했고, 그렇게 만들어진 소프트웨어드은 모두 무료로 개방돼었습니다. 프로그래머라면 누구나 GNU의 소프트웨어를 가져다가 수정하고 개량해 사람들에게 재배포 할 수 있었습니다. 

자유 소프트웨어 재단은 C 컴파일러나 텍스트 에디터, 시스템 라이브러리와 같은 기술적으로 뛰어난 소프트웨어들을 만들었지만, 정작 OS의 핵심 모듈인 커널(kernel)은 개발하지 못했습니다. 이를 위한 최초의 커널은 바로 리눅스(Linux)였습니다. 

## 3. 리눅스 

1991년 리누스 토르발스(Linus Torvalds, 1969~ ) 는 ''리눅스''라고 이름지은 운영체제 커널을 개발하기 시작했습니다. 이때까지 GNU프로젝트는 커널이 없었고 이건 자유로운 OS가 존재하지 않는 다는 것을 의미했습니다. 하지만 리눅스는 자유롭게 개발될수 있는 커널이었고 이는 프로그래머들의 관심을 끌었습니다.  GNU는 리눅스와 합쳐진 후로 완성된 OS가 되었고, 사람들은 이를 흔히 리눅스라 했지만 자유소프트웨어 재단에서는 "GNU/Linux"라는 명칭을 써야한다고 주장했습니다. 



## 4. 오픈소스의 탄생

1997년에 에릭 레이먼드(Eric S. Raymond, 1957~ )는 해커 커뮤니티와 자유 소프트웨어 분석에 대한 철저한 분석인 <성당과 시장>(The Cathedral and the Bazaar)을  발표했습니다. 이 분석글은 엄청난 관심을 끌었고 넷스케이프(Netscape)가 자신들의 인기있던 인터넷 제품군인 넷스케이프 커뮤니케이터를 무료로 배포한 계기가 되었습니다. 넷스케이프의 행동은 레이먼드와 다른 사람들이 자유 소프트웨어의 원칙과 장점을 상업적인 소프트웨어 산업에 이용할수 있는 방법을 찾게 했습니다. 그들은 자유 소프트웨어 재단의 사회적 행동주의가 회사들에게 호소력이 없다고 생각했고 소스코드 공유의 잠재력을 알릴수 있도록 자유 소프트웨어운동을 재 브랜드화하는 방법을 모색했습니다. 

1998년 1월 넷스케이프의 네비게이터에 관한 소스코드 배포에 관해 자유 소프트웨어 재단은 전략 회의를 열었습니다. 이 회의에서 토드 엔더슨, 래리 앙구스틴, 존 홀, 샘 옥맨, 마이클 티맨, 에릭 레이먼드는 크리스틴 피터슨이 제안한 오픈소스란 단어를 채택했습니다. 자유 소프트웨어 운동의 개척자인 스톨만도 이 단어를 쓰기로 결정합니다. 레이먼드와 다른 사람들은 이를 자유소프트웨어가 가지고있던 공짜(free)같은 부정적인 의미를 벗어날수 있는 기회로 여기고 이 단어를 널리 알리는데 힘썼습니다.  



##### 참고자료

- https://en.wikipedia.org/wiki/History_of_free_and_open-source_software
- https://wiki.kldp.org/HOWTO/html/Secure-Programs-HOWTO/history.html
- https://magic.piktochart.com/output/2385023-history-of-the-open-source-movem
- http://www.econote.co.kr/main/view_post.asp?post_seq_no=23725
