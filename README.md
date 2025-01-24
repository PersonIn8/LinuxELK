# PEOPLE_IN_EIGHT 8️⃣
<aside>

## 👨🏻‍💻 프로젝트 개요


## 👨‍👨‍👦‍👦 팀원 소개
| <img src="https://github.com/wns5120.png" width="200px"> | <img src="https://github.com/JaeHee-devSpace.png" width="200px"> | <img src="https://github.com/andytjdqls.png" width="200px"> | <img src="https://github.com/wild-turkey.png" width="200px"> |
| :---: | :---: | :---: | :---: |
| [유호준](https://github.com/wns5120) | [박재희](https://github.com/JaeHee-devSpace) | [이성빈](https://github.com/andytjdqls) | [김지훈](https://github.com/wild-turkey) |

## 📚 기술 스택
 ![Requests](https://img.shields.io/badge/Requests-00599C?style=flat&logo=python&logoColor=white) ![Visual Studio Code](https://img.shields.io/badge/VSCode-007ACC?style=flat&logo=visualstudiocode&logoColor=white)  ![Logstash](https://img.shields.io/badge/Logstash-005571?style=flat&logo=elastic&logoColor=white) ![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=flat&logo=elastic&logoColor=white) ![Kibana](https://img.shields.io/badge/Kibana-005571?style=flat&logo=elastic&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black) ![VirtualBox](https://img.shields.io/badge/VirtualBox-183A61?style=flat&logo=virtualbox&logoColor=white) ![MobaXterm](https://img.shields.io/badge/MobaXterm-008FBA?style=flat&logoColor=white)  ![Markdown](https://img.shields.io/badge/Markdown-000000?style=flat&logo=markdown&logoColor=white) ![ChatGPT](https://img.shields.io/badge/ChatGPT-412991?style=flat&logo=openai&logoColor=white)


## 🎯 프로젝트 목표

       

## 💡 기술적 목표 
 
            

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

- **원인**: Elasticsearch의 기본 설정이 생산 환경에 적합하지 않은 경우.
- **해결 방법**:
    - `/etc/elasticsearch/elasticsearch.yml`에서 `discovery.type: single-node`를 설정하여 싱글 노드 모드로 실행.
    - Elasticsearch 로그 확인 (`/var/log/elasticsearch/elasticsearch.log`)하여 구체적인 오류 메시지 확인.
    - `bootstrap.mlockall` 옵션을 활성화하여 메모리 잠금 문제 해결.
- `vm.max_map_count` 값을 증가시키는 명령어 실행:
- bash
- 
- sudo sysctl -w vm.max_map_count=262144
    - 

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

- 데이터를 관리하는 여러 스택간의 유기적인 활용을 실습해 볼 수 있어서 좋았습니다.
- 그림으로만 보던 파이프라인을 구축하는 경험을 하게 되어 이해하는데 큰 도움이 되었습니다.
- 짧은 프로젝트 기간으로 인해서 처음에 계획했었던 실시간 크롤링 기능과, 구체적인 시각화 기능을 구현하지 못해 아쉽습니다.


