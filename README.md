# [maplecal.com](http://maplecal.com/)
메이플스토리 게임을 더 재밌게 즐길 수 있도록 도와주는 웹사이트입니다.

# 개발환경
* 사용 언어 : JavaScript, Python, Html, CSS, jQuery
* 프레임워크 : Flask, Bootstrap
* 라이브러리 : Selenium, BeautifulSoup

# 기능
* 심볼 계산기  
심볼 개수를 입력값으로 받아 남은 일 수와 소요되는 메소를 계산합니다.

* 몬스터파크 계산기  
몬스터파크 클리어 횟수와 메포사용 여부를 입력받아 달성 날짜와 누적 메포를 계산합니다.

* 하이퍼스텟 계산기  
메이플 게임상 하이퍼스텟을 1000만 메소를 지불하고 초기화 해야하는 비용적 문제를
해결하기 위해 똑같은 기능을 구현하였습니다.

# 업데이트 내역
* 22 / 05 / 09 업데이트
    * 아케인 심볼 가격 하락 반영
    * 추후 가격 변동에 대응하기 위한 코드 일원화
    * 일일 컨텐츠 선택여부 제공
    * 닉네임 검색 기능 비활성화
    * 하이퍼스텟 스탠스 능력치 제거

* 21 / 08 / 14 업데이트
    * 레헬른 일일 퀘스트 4 -> 8개로 증가
    * 모라스 일일 컨텐츠 추가 -> 6개
    * 에스페라 일일 컨텐츠 추가 -> 6개
    * 일반 몬스터 공격 시 데미지 하이퍼 스텟 추가

* 21 / 01 / 14 업데이트
    * 어센틱 심볼 추가
	* 리버스 시티, 얌얌 아일랜드 탐험 시 여로, 츄츄 심볼 2배 적용
    * 만렙 확장으로 인해 하이퍼스텟 레벨 입력값 300까지 증가

* 20 / 09 / 09 업데이트
    * 리부트 서버 닉네임을 통한 검색 기능 지원
	* 검색 크롤링 방식 수정 (월드 랭킹 -> 유니온 랭킹 검색)

* 20 / 05 / 06 업데이트
	* 검색 엔진 meta 태그 추가
	* 당분간 업데이트 x

* 20 / 05 / 03 업데이트
	* 닉네임을 통한 검색 기능 추가
	* 웹사이트 크롤링을 통하여 데이터를 수집하고 있으므로 계정 내 권한 허용 필수
	* 깃허브 -> 개인 서버로 이전함에 따라 동시접속자 많을 시 서버가 다운되는 현상 발생
	* 서버 상황에 따라 접속, 검색 기능 비활성화 될 수 있음

## 심볼 계산기
* 심볼의 레벨과 성장치를 입력하면 Max.Lv 까지 남은 일 수를 자동으로 계산합니다.
* 계산하고 싶은 심볼을 클릭하면 입력창이 화면에 출력되고 입력한 심볼만이 출력창에 표시됩니다.
* 소멸의 여로 심볼 가격 하향 조정으로 인해 나머지 5개 지역과 차이가 발생합니다.
* 남은 일 수 계산에서 입력한 기준 당일 심볼은 획득했다고 가정
* 지역 별 획득 가능 심볼 개수
* 소멸의 여로
	* 일일 퀘스트 : 8개 x 2배(리버스 시티 퀘스트 완료 후) = 16개
	* 에르다 스펙트럼 : 6개
* 츄츄 아일랜드
	* 일일 퀘스트 : 4개 x 2배(얌얌 아일랜드 퀘스트 완료 후) = 8개
	* 배고픈 무토 : 15개(어려움)
* 레헬른
	* 일일 퀘스트 : 8개
	* 드림 브레이커 : 최대 17개(층 수에 따라 다름)
	* Npc : 평균 1개
* 아르카나
	* 일일 퀘스트 : 8개
	* 스피릿 세이비어 : 최대 10개(점수에 따라 다름)
* 모라스
	* 일일 퀘스트 : 8개
    * 엔하임 디펜스 : 6개
* 에스페라
	* 일일 퀘스트 : 8개
    * 프로텍트 에스페라 : 6개
* 세르니움
    * 일일 퀘스트 : 10개

## 몬스터파크 계산기
* 아직 훈장을 획득 하지 못한 요일, 혹은 계산하고자 하는 요일을 선택합니다.
* 오늘까지 몬스터파크를 클리어한 뒤 퀘스트 창을 열어 클리어 횟수를 입력합니다.
* 하루에 2판 무료 / +5판 1500메포 지불하고 이용가능 (판당 300메포)
* 메포를 사용한다면 체크박스를 선택합니다.
* 요일별로 달성 날짜와 누적메포가 계산되어 출력됩니다.

## 하이퍼스텟 계산기
* 메이플스토리 게임 상 하이퍼스텟을 초기화 하는 과정에서 비용이 발생하는 문제를 해결하기 위해 구현됨
* 사용법은 게임 상과 동일하며 실시간으로 증가시킨 하이퍼스텟 레벨을 인식하여 출력창에 증가된 스텟을 표시함
* 남은 포인트가 마이너스( - )로 표시되면 실제 인게임 상 적용할 수 없음
