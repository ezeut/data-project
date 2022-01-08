# 음화당 : 음악을 좋아하는 당신께, 이 영화를 드려요.
- 음악적 요소 기반의 영화 추천 서비스 입니다.

</br>

## 1. 프로젝트 소개

  - 웹서비스에 대한 자세한 개요 : 영화의 타이틀곡의 음악적 요소를 기반으로 데이터 분석을하여 영화를 추천해주는, 음악적 요소 기반 영화 추천 서비스 입니다. 
  - 평소에 음악을 즐겨 듣는, 특히 영화에서의 음악을 중시하는 사용자가 저희 서비스의 주요 대상입니다. 
  1. 유저는 다섯가지의 서로 다른 분위기의 영화 타이틀곡 중에 하나를 선택하게 되며, 저희는 그 타이틀곡들이 속해있는 영화의 장르로 데이터베이스를 한번 필터링 합니다. 
  1. 그 다음, 유저가 현재 느끼는 감정 (혹은 유저가 원하는 무드)과 음악의 템포를 입력하게 되면, 저희는 그것을 기반으로 데이터베이스를 한번 더 필터링 합니다. 음악적 요소들은 다음과 같습니다: energy, danceability, valence, tempo
  1. 다음으로, 유저는 영화 (음악)을 선택하게 되고, 저희는 그 영화가 가진 음악들 요소들을 이용해 데이터 분석을 해서 유저가 선택한 영화와 가장 비슷한 영화, 두번째로 비슷한 영화, 세번째, 네번째로 비슷한 영화들을 추천해 줍니다. 데이터 분석에 사용되는 음악적 요소들은 다음과 같습니다 : acousticness, danceability, energy, tempo, valence, instrumentalness, liveness, loudness, speechiness 


**어떠한 인공지능 모델과 알고리즘을 사용했는지에 대한 설명과 엔드유저에게 보이는 웹서비스에 대한 소개**

  - 사용하려는 인공지능 모델과 알고리즘을 명시 ... 지은님 보연님 부탁드립니다...
  - 인공지능에 사용하려는 데이터를 명시, 이에 대한 설명 ... 지은님 보연님 부탁드립니다...
  - 기술 스택 (python, d3, pandas, jupyter, javascript, MySQL 등) ... python, pandas, jupyter, javascript, MySQL, React, d3 

<details><summary>사용된 라이브러리</summary>

alembic==1.7.5  </br>

attrs==19.3.0  

Automat==0.8.0 

beautifulsoup4==4.10.0 

blinker==1.4 

bs4==0.0.1 

certifi==2019.11.28 

chardet==3.0.4 

click==8.0.3

cloud-init==21.4

colorama==0.4.4

command-not-found==0.3

configobj==5.0.6

constantly==15.1.0

cryptography==2.8

dbus-python==1.2.16

distro==1.4.0

distro-info===0.23ubuntu1

EditorConfig==0.12.2

entrypoints==0.3

Flask==2.0.2

Flask-Cors==3.0.10

Flask-Migrate==3.1.0

Flask-SQLAlchemy==2.5.1

greenlet==1.1.2

httplib2==0.14.0 

hyperlink==19.0.0 

idna==2.8 

importlib-metadata==4.10.0 

importlib-resources==5.4.0 

incremental==16.10.1 

itsdangerous==2.0.1 

Jinja2==3.0.3 

jsbeautifier==1.10.3 

jsonpatch==1.22 

jsonpointer==2.0 

jsonschema==3.2.0 

keyring==18.0.1 

language-selector==0.1 

launchpadlib==1.10.13 

lazr.restfulclient==0.14.2 

lazr.uri==1.0.3 

Mako==1.1.6 

MarkupSafe==2.0.1 

more-itertools==4.2.0 

mysql-connector-python==8.0.27 

netifaces==0.10.4 

numpy==1.22.0 

oauthlib==3.1.0 

pandas==1.3.5 

pexpect==4.6.0 

protobuf==3.19.1 

pyasn1==0.4.2 

pyasn1-modules==0.2.1 

PyGObject==3.36.0 

PyHamcrest==1.9.0 

PyJWT==1.7.1 

pymacaroons==0.13.0 

PyMySQL==1.0.2 

PyNaCl==1.3.0 

pyOpenSSL==19.0.0 

pyparted==3.11.2 

pyrsistent==0.15.5 

pyserial==3.4 

python-apt==2.0.0+ubuntu0.20.4.6 

python-dateutil==2.8.2 

python-debian===0.1.36ubuntu1 

python-dotenv==0.19.2 

pytz==2021.3 

PyYAML==5.3.1 

requests==2.22.0 

requests-unixsocket==0.2.0 

scipy==1.7.3 

SecretStorage==2.3.1 

service-identity==18.1.0 

simplejson==3.16.0 

six==1.16.0 

sos==4.1 

soupsieve==2.3.1 

SQLAlchemy==1.4.29 

ssh-import-id==5.10 

systemd-python==234 

Twisted==18.9.0 

ubuntu-advantage-tools==27.4 

ufw==0.36 

unattended-upgrades==0.1 

urllib3==1.25.8 

wadllib==1.3.3 

WALinuxAgent==2.2.46 

Werkzeug==2.0.2 

zipp==3.7.0 

zope.interface==4.7.1 

</details>




## 2. 프로젝트 목표

**웹서비스의 해결 과제와 인공지능으로 해결하기 위한 방안 논의 (50자 이상)**
  - 영화의 분위기와 영화의 타이틀곡의 분위기는 상당히 비슷할 것이라는 가정으로 시작합니다. 
  - 영화에서 사용된 음악을 기반으로 영화를 추천해 주기에, 평소에 음악을 즐겨 들으시거나 영화에서의 음악이 차지하는 비중이 크다는 믿음이 있으신 유저에게 유용한 솔루션입니다. 
  - 추천은 보통 추천 받는 사람과 추천 해 주는 사람의 주관에 따라 굉장히 다른 만족을 줍니다. 하지만 데이터를 분석하여 그 결과를 추천해 준다면, 가능 한 최대한 객관적인 추천이 될 수 있습니다. 개개인에 최적화 되었다기보다는 많은 사람에게 만족스러운 결과를 주는 것을 목표로 했습니다. 
  - '우리가 배운 기술들 중에 어떤 기술이 논리적으로 가장 객관적인 추천을 해 줄 수 있을까?' 에 답하기 위해서 후보 기술들 ( A, B, C) 중에 B를 선택했습니다. 근거는 어쩌구 보연님 지은님...

  </br>

## 3. 프로젝트 기능 설명

**웹서비스의 유용성, 편의성 및 시각화의 실용성에 대한 설명**
  - 영화를 음악을 기준으로 분석한, 새로운 시각의 추천을 해 줍니다.  
  - 음악 미리듣기 기능으로 단순히 음악의 장르를 선택하는것 대신, 그 곡의 분위기를 잘 느끼고 선택할 수 있습니다. 
  - 유저가 선택한 영화와 추천으로 나온 영화가 얼마나 음악적으로 유사한지를 보여주는 레이더 플롯을 제공합니다. 
  - 전체 영화를 클러스터로 나눴을 때, 유저가 선택한 영화가 어느 클러스터에 속하는지를 보여주는 스캐터 플롯을 제공합니다. 

  </br>

## 4. 프로젝트 구성도
  - [와이어프레임](https://whimsical.com/wireframe-GVvpXpFxByvR7TZ9XvCzyi) 
  - 스토리보드 ???

  </br>

## 5. 프로젝트 팀원 역할 분담
| 이름 | 담당 업무 |
| ------ | ------ |
| 이호준 | 프론트엔드 개발 |
| 백정하 | 백엔드 개발, 팀장 |
| 정진묵 | 백엔드 개발 |
| 이보연 | 데이터 분석 |
| 이지은 | 데이터 분석 |

**멤버별 responsibility**

1. 팀장

- 일정 및 의견 조율 
- 발표 준비 

2. 프론트엔드

- react 기반 화면 구현 
- css 적용 
- API 연동 

3. 백엔드

- 데이터베이스 스키마 구성 
- 제공받은 데이터 데이터베이스에 입력 
- API 작성, 연동 
- 배포 

4. 데이터 분석

- 기획 단계: 웹 서비스 프로젝트 주제에 맞는 모델 및 알고리즘 설정, 모델과 알고리즘에 적합한 데이터셋 수집
- 개발 단계: 데이터 전처리, 학습 모델 구현, 학습 데이터 가공 및 모델 정밀도 향상

5. 팀 전체

- 프로젝트의 기획이나 CSS 등, 합의가 필요한 부분들은 모두가 함께 참여하였습니다. 

## 6. 버전
  - 프로젝트의 버전 기입

## 7. FAQ
  - 자주 받는 질문 정리
