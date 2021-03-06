# 개인프로젝트 기획안\__현승우

### 프로젝트 명

**주소 기반의 다양한 세권 점수 산출 알고리즘 및 사이트 개발**



### 프로젝트 개요

디벨로퍼(부동산 개발업체)가 땅을 살 때 가장 중요한 기준으로 흔히 입지를 꼽는다. 수요자가 집을 고를 때도 마찬가지다. 입지의 대표적인 사례가 역세권이다. 지하철과의 도보 거리로, 보통 10분 이내를 의미한다. 최근에는 학세권, 스세권, 맥세권, 몰세권 등 신조어가 속속 등장하고 있다.

같은 지역에서 지하철이 가까운 아파트 단지의 가격(한국 갤럽의 미래주택 조사 기준)이 멀리 떨어져 있는 아파트보다 7~9% 가량 더 비싼 것으로 알려져 있다. 서울 강남의 대단지 아파트에서도 지하철 접근성에 따라 가격 차이가 최대 1억원까지 나기도 한다.

입지 여건도 점차 세분화되고 있다. 1~2인 가구가 늘어나고 자기만의 생활을 추구하면서 편의시설이 가까운 게 주택 선택의 기준으로 부각되고 있어서다. 편세권 스세권 등이 대표적이다. 미국 빅데이터 업체 질로에 따르면 뉴욕에서 스타벅스 인근에 있는 집의 가치가 그렇지 않은 집보다 높다. 1997년 스타벅스 인근 주택이 더 멀리 떨어진 집보다 5.5% 비쌌다. 2013년에는 그 격차가 7.1%로 벌어졌다.

- 현재 직방 다방 앱은 정확한 주소 기반이 아닌, 역명, 지역명, (다방은 대학교명)으로 큰 범주로 검색되고 있다.



집 근처에서 지갑을 여는 트렌드는 점차 강해지고 있다. 집에서 걸어 갈 수 있는 거리의 유통매장에서 식료품을 비롯한 생필품을 구매하는 것은 물론이다. 영화 등 문화 상품도 집 근처에서 소비하는 경향이 보인다.

![](https://user-images.githubusercontent.com/17154958/51781648-eb4f5c80-215e-11e9-8d9e-f207be5fb642.png)

![](https://user-images.githubusercontent.com/17154958/51781657-281b5380-215f-11e9-9dcd-bcc415acd7e2.png)

*출처 신한카드 빅데이터 센터(신한트렌디스)*



### 프로젝트 기획 의도

집 근처에서 소비하는 패턴이 점차 증가하고 있다.

1인 가구가 집을 구할 때 중요하게 보는 조건에는 학교 또는 직장 근처에 있는 지, 자신이 살고 있는 집 근처에 필요한 여가생활이나 생필품 구입에 필요한 매장이 있는 지가 중요 조건이다. 또한 좋아하는 브랜드 매장이 어디에 있는지도 중요하기 때문에 현재 다방이나 직방에서 제공하고 있는 큰 분류(동, 역, 학교)보다는 세부적으로 브랜드 매장(맥도날드, 스타벅스), 영화관, 백화점 등 세부적인 주소로 검색하여 각 세권의 점수를 산출하여 자신이 원하는 입지에 있는 매물을 한눈에 보고 비교해 볼 수 있는 알고리즘 & 사이트를 개발하는 것이 목적이다.



##### 세권의 종류

- **스세권**: 국내에서는 연간 13만톤 이상의 커피를 소비하고 10명 중 8명은 하루에 2잔 이상 커피를 마신다. 스세권은 스타벅스가 도보 가능한 거리에 위치한 지역을 말한다. 
- **맥세권**: 맥도날드 배달 서비스(맥딜리버리)가 가능한 지역을 말한다.
  통상적으로 맥딜리버리는 주문 후 배달까지 17분 30초가 걸린다.
- **몰세권**: 편리하게 문화생활을 즐길 수 있는 지역을 말한다. 한 건물에서 쇼핑과 외식, 영화관, 서점 등을 한번에 즐길 수 있는 곳으로 삼성동 코엑스몰이나 영등포 타임스퀘어 등을 생각할 수 있다.
- **의세권**: (종합병원) 의료 혜택을 가깝게 받아 볼 수 있는 지역이다. 종합병원은 100개 이상의 병실을 갖추고 7개 상의 진료과목과 전문의를 갖춘 의료 기관을 말한다. 서울에서는 영등포구(7), 동대문구(5), 강남구(4), 종로구(4)로 조사된다.
- **편세권**: 편의점인근을 지칭, 1인 가구에게 편의점은 대형마트만큼이나 중요한 생활 인프라로 자리잡았다. 혼밥, 혼술을 가능하게 해주는 음식점 역할은 물론이고, ATM기를 이용하면 현금 인출 등 간단한 은행 업무도 해결할 수 있다. '직방'과 '다방' 등의 부동산 앱에서는 해당 매물 인근에 편의점 위치를 표시해 '편세권'의 유무를 확인할 수 있게 해준다.



### 프로젝트 프로세스

##### 1. 필요 데이터 수집

- [서울열린데이터광장](http://data.seoul.go.kr/dataList/datasetList.do)

  - 역세권: 역 정보 
  - 학세권: 초등학교, 중학교, 고등학교, 대학교 

  

- 각 매장 사이트 크롤링

  - 스세권: 스타벅스 홈페이지 크롤링 
  - 맥세권: 맥도날드 홈페이지 크롤링
  - 몰세권: 신세계, 엔터식스, 갤러리아, 롯데백화점, 현대백화점, NC백화점, 아이파크몰, 코엑스몰 
  - 의세권: 종합병원 
  - 편세권: CU, 이마트 24, GS25, Seven Eleven, MINISTOP



##### 2. 주소 -> 위,경도 변환

- 구글 지도 api 
- api에서 불러들이지 못한 주소값은 직접 구글 지도에 들어가서 채워넣는다.



##### 3. 직방 데이터 크롤링

- 상세 주소(타겟)로 검색했을 시 나와있는 매물을 검색하기 위해 직방에서 크게 동명으로 크롤링.



##### 4. 거리 계산

- 상세 주소(타겟)와 매물의 가까운 점수를 계산, 세권 점수와 합하여 제공할 것.



##### 5. 점수 산출 



##### 6. 추후 분석 

- 각 세권 점수, 집 건축년도, 집 크기 등의 데이터로 집 가격 예측 분석

  
