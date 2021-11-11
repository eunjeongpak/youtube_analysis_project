# project 기획
## Youtube Popular Chart Analysis
  - 작성자 : 박은정
  - 작성날짜 : 2021/10/21
  - GITHUB : https://github.com/eunjeongpak/youtube_analysis_project
  - LICENSE: GNU General Public License v3.0
   ![image](https://user-images.githubusercontent.com/76864400/138218131-603e665c-10a1-4a2e-8c59-d39687fd1596.png)

- 프로젝트 주제
  - 유튜브 API를 활용한 유튜브 인기 동영상 데이터 분석 및 인기 키워드가 포함된 영상을 추출하여 해당 영상들의 댓글을 7가지의 감정으로 분류하는 모델을 활용한 감성 분석

- 프로젝트 목적
  - Youtube API로부터 유튜브 인기 동영상 데이터 등을 불러와 데이터 분석(키워드 분석 및 감성 분석) 후 웹페이지를 만들어 배포
    - 누구에게나 실시간 유튜브 인기 동영상 혹은 유튜브 채널의 분석 결과를 제공해주는 웹페이지를 만들어 누구나 사용할 수 있는 웹페이지를 구축하는 것
  - 현재는 감성 분석까지만 진행한 상황으로, 앞으로 웹페이지 배포할 예정

- 프로젝트에 사용한 데이터
  1. Youtube API를 활용해 가져온 인기 동영상 데이터
      - 출처: https://developers.google.com/youtube/v3
      - 설명: 유튜브 API를 사용하여 한국에서의 인기 동영상(mostPopular)을 매일 TOP 20개씩 18:00PM 기준으로 추출하여 Postgresql 데이터베이스에 저장해 스프레드시트로 업로드
        ![image](https://user-images.githubusercontent.com/76864400/138220402-a9e32e0f-0e77-43f3-acc6-a50647cd5dc5.png)

  
  2. 한국어 단발성 대화 데이터셋
      - 출처: https://aihub.or.kr/opendata/keti-data/recognition-laguage/KETI-02-009
      - 설명
        - 해당 데이터는 SNS 글 및 온라인 댓글에 대한 웹 크롤링을 실시하여 총 38,594 문장을 선정하여 7개 감정(기쁨, 슬픔, 놀람, 분노, 공포, 혐오, 중립) 레이블링 수행한 데이터
        - 해당 프로젝트에서는 해당 데이터를 사전학습된 KoBERT 모델에 Finetuning하는 용도로 사용함
        ![image](https://user-images.githubusercontent.com/76864400/138218777-6d2e6605-bc26-4ae8-b59d-34bbdb56653c.png)

- 프로젝트 분석 방법 및 내용
  - pandas 활용해 인기 동영상에 대한 기본적인 시각화
    - 현재 어떤 카테고리 혹은 어떤 채널에 속한 유튜브 영상이 인기있는지 등 기본적인 분석
  - Wordcloud를 활용한 키워드 분석
    - 어떠한 키워드가 가장 많이 등장하는지(인기있는지) 분석
  - KoBERT 모델을 활용한 댓글 감성 분석
    - 인기 키워드에 해당하는 동영상 댓글을 추출해 댓글에 나타난 사람들의 감정을 분류할 수 있는 감성 분석 예측 모델 생성 후 예측

- 프로젝트 목차
  1) 라이브러리 설치 및 데이터 업로드
  2) 데이터 분석 및 시각화
  3) 워드클라우드를 활용한 키워드 분석
  4) KoBERT 모델을 활용한 댓글 감성 분석
  5) 결과 및 한계점

- 프로젝트 언어: python

- KoBERT 모델 참고 자료: https://www.dinolabs.ai/m/271?category=1203530







