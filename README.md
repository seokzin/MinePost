# MINE POST (CSUOS capstone-project)
Django 기반 GPT-2를 활용한 인공지능 뉴스 사이트

## Services
### 1. AI Writing
  - 제목에 적합한 단어 실시간 추천
  - 첫 문장 입력시 기사 자동 완성
  - 글 스타일(문체) 선택 (fine turning 적용)

### 2. Image Recommendation
  - 크롤링을 통해 기사에 적합한 이미지 추천 (본인 버전에 맞는 chromedriver 필요)

### 3. 3-Line Summary
  - TextRank를 통한 핵심 문장 세줄 요약 (패키지 문제로 개선 중)

## Link
https://capstone.uos.ac.kr/cdc/index.php/%EB%AF%B8%EB%84%A4%EB%A5%B4%EB%B0%94

## Structure
![image](https://user-images.githubusercontent.com/43740455/122677094-b6ef0600-d21b-11eb-80a6-c58afaf40aa1.png)

## Install
```sh
&git init
&git clone https://github.com/ssorry123/capstone.git
&cd capstone
&pip3 install -r requirements.txt
```

### Requirements
* Python >= 3.6
* gluonnlp == 0.9.1
* mxnet == 1.6.0
* sentencepiece >= 0.1.85
* torch == 1.5.0
* transformers == 2.11.0
* django_extensions==2.2.9
* selenium==3.141.0
* Django==3.0.7
* minegpt2

### 1. Main Page
![image](https://user-images.githubusercontent.com/43740455/122677186-32e94e00-d21c-11eb-8417-cfadd150a226.png)

1. 헤드라인 뉴스
    - 전체 뉴스 최신순
2. 카테고리별 뉴스
    - 카테고리별 최신순
3. 투데이 랭킹
    - 스크랩 기반 순위
    - 우측 사이드바 위치

### 2. Writing Page
![image](https://user-images.githubusercontent.com/43740455/122677267-9c695c80-d21c-11eb-9277-fefe227d35e4.png)
![image](https://user-images.githubusercontent.com/43740455/122677273-a1c6a700-d21c-11eb-97a2-eb56411e2e37.png)

1. 출력 글 스타일 지정(핵심 1)
    - 학습된 다양한 글 스타일 모델 선택
2. 제목 단어 추천 (핵심 2)
    - 통계 기반의 적절한 다음 단어 추천
3. 기사 자동 완성 (핵심 3)
    - 첫 문장을 작성한다면 문맥을 파악해 한 문단의 글 완성
4. 이미지 추천 (핵심 4)
    - 구글 이미지 크롤링을 통해 제공

### 3. Category Page (IT/Science)
![image](https://user-images.githubusercontent.com/43740455/122677356-f9fda900-d21c-11eb-98da-1bf0fc819881.png)

1. 핫이슈
    - 카테고리 최다 스크랩 기사
2. 뉴스 리스트
    - 10개 단위 페이지네이션

### 4. Scrap Page
![image](https://user-images.githubusercontent.com/43740455/122677401-11d52d00-d21d-11eb-9abe-cb9eb2b6f83d.png)

1. 스크랩 글 조회
2. 스크랩 삭제
    - 체크박스 통한 복수 삭제 가능

### 5. Article Page
![image](https://user-images.githubusercontent.com/43740455/122677443-33ceaf80-d21d-11eb-89fc-806a1b4de2b5.png)

1. 요약 봇 (핵심 5)
    - Text-Rank 통한 기사 3줄 요약
2. 스크랩
    - 스크랩 페이지에 추가
3. 댓글
    - Disqus API 사용

