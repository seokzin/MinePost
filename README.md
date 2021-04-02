# MINE POST (CSUOS capstone-project)
Django 기반의 인공지능 보조 뉴스 사이트

## Services
1. AI Writing
  - 실시간 단어 추천
  - 자동 기사 완성
  - 글 스타일 선택(fine turning 적용)

2. Image Recommendation
  - 이미지 크롤링을 사용한 이미지 추천
  - (본인의 chrome 버전에 맞는 chromedriver 필요)

3. 3-Line Summary
  - TextRank를 통한 핵심 문장 요약
  - (패키지 문제로 개선 중)

## Link
https://capstone.uos.ac.kr/cdc/index.php/%EB%AF%B8%EB%84%A4%EB%A5%B4%EB%B0%94

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
