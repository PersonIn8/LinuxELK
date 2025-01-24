# ELK with Ubuntu
<aside>

## 👨🏻‍💻 프로젝트 개요


## 👨‍👨‍👦‍👦 팀원 소개
| <img src="https://github.com/wns5120.png" width="200px"> | <img src="https://github.com/JaeHee-devSpace.png" width="200px"> | <img src="https://github.com/andytjdqls.png" width="200px"> | <img src="https://github.com/wild-turkey.png" width="200px"> |
| :---: | :---: | :---: | :---: |
| [유호준](https://github.com/wns5120) | [박재희](https://github.com/JaeHee-devSpace) | [이성빈](https://github.com/andytjdqls) | [김지훈](https://github.com/wild-turkey) |

## 📚 기술 스택
 ![Requests](https://img.shields.io/badge/Requests-00599C?style=flat&logo=python&logoColor=white) ![Visual Studio Code](https://img.shields.io/badge/VSCode-007ACC?style=flat&logo=visualstudiocode&logoColor=white)  ![Logstash](https://img.shields.io/badge/Logstash-005571?style=flat&logo=elastic&logoColor=white) ![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=flat&logo=elastic&logoColor=white) ![Kibana](https://img.shields.io/badge/Kibana-005571?style=flat&logo=elastic&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black) ![VirtualBox](https://img.shields.io/badge/VirtualBox-183A61?style=flat&logo=virtualbox&logoColor=white) ![MobaXterm](https://img.shields.io/badge/MobaXterm-008FBA?style=flat&logoColor=white)  ![Markdown](https://img.shields.io/badge/Markdown-000000?style=flat&logo=markdown&logoColor=white) ![ChatGPT](https://img.shields.io/badge/ChatGPT-412991?style=flat&logo=openai&logoColor=white)


## 🎯 프로젝트 목표

- 데이터 수집 및 분석: 카드 데이터를 효과적으로 수집하고 분석하여 유의미한 인사이트를 도출할 수 있습니다.

- 실시간 데이터 시각화: Elasticsearch, Logstash, Kibana(ELK 스택)를 활용하여 실시간으로 데이터를 시각화하고 모니터링할 수 있습니다.

- 사용자 친화적인 대시보드 제공: 최종 사용자에게 직관적이고 이해하기 쉬운 대시보드를 제공하여 데이터에 기반한 의사 결정을 지원합니다.

- 포트포워딩을 통한 접근성 향상: 윈도우 환경에서 리눅스 가상 머신의 ELK 스택에 원활하게 접근할 수 있도록 포트포워딩 설정을 구성합니다.
       

## 💡 기술적 목표 
- ELK 스택 설치 및 구성: 리눅스 가상 머신에 Elasticsearch, Logstash, Kibana를 성공적으로 설치하고, 각 구성 요소가 원활하게 작동하도록 설정합니다.

- 포트포워딩 설정: 리눅스 가상 머신의 ELK 스택 포트를 윈도우에서 접근할 수 있도록 포트포워딩을 설정합니다.

- 시각화 및 대시보드 설계: Kibana를 활용하여 카드사 데이터에 대한 다양한 시각화(예: 차트, 그래프 등)를 생성하고, 사용자 요구에 맞는 대시보드를 디자인합니다.

- 성능 최적화: Elasticsearch의 성능을 최적화하여 대량의 데이터 처리 시에도 빠른 검색과 분석이 가능하도록 설정합니다.
            

## 📐 System Architecture

## 🛢 데이터베이스




## 📊 데이터

--------------------------------------------------------------------------------------------------



# 🚀 트러블 슈팅
# Untitled

**1. Kibana 접속 안 될 때 (ERR_CONNECTION_RESET)문제**: Kibana가 실행 중이지만 `localhost:5601`에서 접속이 안 되는 경우 발생할 수 있습니다.

- **원인**: 방화벽, Kibana 설정, Elasticsearch 설정 문제 등.
- **해결 방법**:
    - Kibana 서비스가 제대로 실행되고 있는지 확인 (`sudo systemctl status kibana`).
    - 방화벽 설정 확인: `sudo ufw allow 5601/tcp`로 포트 열기.
    - Kibana 설정 파일 (`/etc/kibana/kibana.yml`)에서 `server.host: "0.0.0.0"`으로 외부 접속 허용.
    - Kibana 로그 확인 (`sudo tail -f /var/log/kibana/kibana.log`)하여 오류 메시지 점검.
    - Elasticsearch 연결 상태 확인 (`curl [http://localhost:9200](http://localhost:9200/)`)하여 Elasticsearch가 정상적으로 작동하는지 확인.

**2. Elasticsearch 서비스 실패 (Status 78/CONFIG)문제**: Elasticsearch 서비스가 시작되지 않고 `status=78/CONFIG` 오류 발생.

![image](https://github.com/user-attachments/assets/bf58af76-08d8-4d72-b1c6-92ea2d6fd56a)


- **원인**: Elasticsearch의 기본 설정이 생산 환경에 적합하지 않은 경우.
- **해결 방법**:
    - `/etc/elasticsearch/elasticsearch.yml`에서 `discovery.type: single-node`를 설정하여 싱글 노드 모드로 실행.
    - Elasticsearch 로그 확인 (`/var/log/elasticsearch/elasticsearch.log`)하여 구체적인 오류 메시지 확인.


**3. Elasticsearch에서 연결 문제 (Unable to connect to localhost:9200)문제**: `curl [http://localhost:9200](http://localhost:9200/)` 명령어로 Elasticsearch에 접속할 수 없는 경우.

- **원인**: Elasticsearch가 제대로 실행되지 않거나, 방화벽 설정 문제.
- **해결 방법**:
    - Elasticsearch 서비스 상태 확인 (`sudo systemctl status elasticsearch`).
    - 방화벽에서 포트 9200을 열었는지 확인 (`sudo ufw allow 9200/tcp`).
    - `elasticsearch.yml` 파일에서 `network.host: 0.0.0.0`을 설정하여 모든 IP에서 접근할 수 있도록 변경.
    - 로그 확인 (`sudo journalctl -xeu elasticsearch.service`)하여 더 구체적인 오류 파악.

**4. Kibana와 Elasticsearch 간 연결 문제문제**: Kibana가 Elasticsearch에 연결할 수 없는 경우.

- **원인**: Kibana 설정 파일에서 `elasticsearch.hosts` 값이 잘못 설정된 경우.
- **해결 방법**:
    - `/etc/kibana/kibana.yml` 파일에서 `elasticsearch.hosts: ["[http://localhost:9200](http://localhost:9200/)"]` 설정.
    - Kibana가 실행 중인 호스트와 Elasticsearch가 실행 중인 호스트가 동일한지 확인.
    - Kibana와 Elasticsearch 모두 동일한 버전인지 확인하여 호환성 문제 해결.
----

# 🤔 회고

