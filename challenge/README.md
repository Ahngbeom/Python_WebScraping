# Challenge

## 1.  부동산 매물 조회 및 추출

## 2.  나만의 비서 만들기 (포탈사이트 주요 정보 추출 및 특정 사이트에서 특정 데이터 추출)

    * 첫 번째 구현 시도 :

        강의를 듣기 전 나 혼자서 구현을 해보기로 했다.

        전체적으로 Selenium - WebDriver프레임워크 기반으로 구현을 했다.
        구현 과정에서 웹 브라우저를 띄워 크롤링하는 과정을 직접 볼 수 있다는 것이 매력적이었다고 생각했다.

        하지만 해커스 홈페이지와 같은 광고배너, 팝업 창에 대한 처리를 어떻게 해야될지 고민스러웠다.
        단순하게 '닫기' 버튼을 누르기위해 click() 메소드를 호출해보았지만
        뜻대로 정상적인 처리가 되지않았다.

        그래서 다시 처음으로 돌아가서 문제 원인을 찾아보았다.
        여러가지 문제가 있겠지만 그 중 근본적인 문제는
        주소 접근 과정을 어려운 방식으로 구현했던 것 같다.

        webdriver의 get 메소드 url 인자를 www.naver.com 부터 시작해서
        목적 페이지 또는 사이트를 접근하기위해 검색 바에 문자열을 삽입하고 Enter 키 이벤트를 발생시키거나
        검색 버튼 태그에 click 메소드를 호출하는 방식을 토대로 코드 구현을 이어나갔다.

        웹 스크래핑, 크롤링의 목적은 원하는 데이터만을 추출하는 것이 목적이기 때문에
        위와 같은 방식은 코드 길이만 길어지고 수행 속도도 느려질 수 있다는 단점이 있을 것이다.

        일반적으로 유저가 알아내기 어려운 주소를 접근하기 위해서는 위와 같은 방식으로 구현해야할 수도 있겠지만

        지금 구현해야하는 프로젝트는 그 수준은 아니기 때문에 잠시 접어두기로 했다.

        ps. 프로젝트를 구현하기 전에 Selenium 강의와 예제코드를 봐왔기 때문에 자연스럽게 Selenium 기반으로 구현하게 된 것도 원인 중 하나일 것 같다.

    * 두 번째 구현 시도 :

        selenium 을 굳이 안써도 될 것 같다.

        데이터를 추출할 사이트와 페이지를 탐색해보니 동적 크롤링이 필요해보이지 않았다.

        초기 URL 설정만 잘해주고 데이터를 추출하기위한 처리를 매끄럽게만 해준다면 

        requests 와 BeautifulSoup 만을 통해서도 간단하게 데이터를 추출할 수 있을 것 같았다.

        이전에 구현한 코드에서 WebDriver 대신 requests와 BeautifulSoup로 변환하고

        소량의 코드를 추가하니 성공적으로 데이터를 추출하여 터미널에 출력할 수 있었다.

        코드의 길이도 간략화되었고 수행 속도도 확실히 빨라진 것을 느낄 수 있었다.

        Selenium을 기반으로 구현할 때 따르는 단점에 대해서도 생각해볼 수 있는 기회였다.


