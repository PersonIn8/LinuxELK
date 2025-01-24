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
**실무 데이터의 분석:**
- 다양한 시각화 아이디어를 기반으로 실무 데이터를 분석하여 유의미한 인사이트를 도출합니다.

**시각화 아이디어를 기반으로 데이터 인사이트 도출:**
- 데이터를 직관적으로 이해할 수 있도록 다양한 차트와 그래프를 활용해 분석 결과를 시각화합니다.

**고객 친화적인 대시보드와 새로운 기능 설계:**
- 분석 결과를 바탕으로 최종 사용자가 쉽게 활용할 수 있는 대시보드를 설계하고, 새로운 기능을 제안합니다.

       

## 💡 기술적 목표 
**ELK 스택 설치 및 구성**:
- 리눅스 가상 머신에 **Elasticsearch**, **Logstash**, **Kibana**를 성공적으로 설치하고, 각 구성 요소가 원활하게 작동하도록 설정합니다.

**포트포워딩 설정**:
- 리눅스 가상 머신의 **ELK 스택 포트**를 윈도우에서 접근할 수 있도록 **포트포워딩**을 설정합니다.

**시각화 및 대시보드 설계**:
- **Kibana**를 활용하여 **카드사 데이터**에 대한 다양한 시각화(예: 차트, 그래프 등)를 생성하고, 사용자 요구에 맞는 **대시보드**를 디자인합니다.

**실시간 데이터 수집 및 분석**:
- **카드 데이터를 효과적으로 수집**하고 분석하여 유의미한 인사이트를 도출합니다. **Elasticsearch**와 **Logstash**를 활용하여 **실시간 데이터**를 효율적으로 처리합니다.

**실시간 데이터 시각화 및 모니터링**:
- **Kibana**를 통해 **데이터를 실시간으로 시각화**하고 **모니터링**하여 사용자 친화적인 **대시보드**를 제공합니다.

**성능 최적화**:
- **Elasticsearch**의 성능을 최적화하여 대량의 데이터 처리 시에도 빠른 검색과 분석이 가능하도록 설정합니다.


            

## 📐 System Architecture


## 데이터 분석 & 시각화
### 1. 시각화 아이디어

- **나이별 이용금액 비교**
- **등급별 이용금액 비교**
- **분기별 이용금액 비교**
- **거주지역별 이용금액 비교**
- **성별 이용금액 비교**
- **OO별 특정 카테고리 이용금액 비교** (예: 가전가구주방용품 이용금액이 가장 높은 지역, 나이 등)
- **나이별 등급 비교** (나이가 많은 사람이 VVIP 비율이 높은가?)
- **디지털채널가입별 이용금액 비교**
- **라이프스테이지별 이용금액 비교**
- **VVIP+VIP와 일반 고객 비율 비교**
- **가장 많은 이용금액을 쓴 카테고리(중분류, 대분류)**
- **어느 업종에 VVIP가 많은지**
- **각 등급별 이용금액의 최대값/최솟값 비교** (등급 업그레이드 기준 탐색)

---

### 2. 데이터 목적에 따른 시각화 분류

#### 소비 분석 (등급, 혜택)
- **혜택 대상 선정**: 어떤 등급에게 혜택을 많이 줄 것인가?
- **잠재적 VVIP 발굴**: VVIP 비율이 많은 라이프스타일, 나이, 지역 등 주요 요소를 분석하여 잠재 고객층 파악.

#### 새로운 기능 추가
- **카드 커스터마이징 기능 설계**: 소비 패턴 기반의 커스터마이징 가능한 혜택 제공 카드 설계.

#### 고객 세분화
- **소비 패턴 그룹화**: 고객 소비 데이터를 기반으로 그룹화하여 등급 조정.
- **지역별 활발한 거래 파악**: 지역별 인기 거래 카테고리 분석.

---

### 3. 카테고리별 소비 분포

#### 주요 분석
1. **업종별 소비 비중**
   - 식음료, 여행, 쇼핑, 엔터테인먼트 등 카테고리별 소비 데이터를 **원형 차트**로 시각화.

2. **소비 증가/감소 업종 트렌드**
   - 특정 기간 동안 성장하거나 감소한 업종 트렌드를 분석하여 **다음 분기 혜택 선정**에 반영.

---

### 4. 이상치 탐지 및 분석
- **이상치 탐지**: 고객별 평균 소비량에서 크게 벗어나는 금액 탐지 (범죄 연루 가능성 검토).
- **전처리 필요성**: 데이터의 전처리, 이상치 제거, 가공 여부를 고려하여 분석 정확도 향상.

<br>
<br>





# 🚀 트러블 슈팅

## 1. Kibana 접속 불가 (ERR_CONNECTION_RESET)
Kibana가 실행 중이지만 `localhost:5601`에서 접속이 안 되는 경우 발생할 수 있습니다.

### 원인
- 방화벽 설정 문제
- Kibana 설정 오류
- Elasticsearch 설정 문제

### 해결 방법
1. **Kibana 서비스 확인**
   ```bash
   sudo systemctl status kibana
   ```

2. **방화벽 설정 확인**
   ```bash
   sudo ufw allow 5601/tcp
   ```

3. **Kibana 설정 수정**
   `/etc/kibana/kibana.yml` 파일에서 다음과 같이 수정하여 외부 접속을 허용합니다:
   ```yaml
   server.host: "0.0.0.0"
   ```

4. **Kibana 로그 확인**
   ```bash
   sudo tail -f /var/log/kibana/kibana.log
   ```

5. **Elasticsearch 연결 확인**
   ```bash
   curl http://localhost:9200
   ```

---

## 2. Elasticsearch 서비스 실패 (Status 78/CONFIG)
Elasticsearch 서비스가 시작되지 않고 `status=78/CONFIG` 오류가 발생하는 경우.

### 원인
- Elasticsearch 기본 설정이 생산 환경에 적합하지 않은 경우.

### 해결 방법
1. **싱글 노드 모드로 실행**
   `/etc/elasticsearch/elasticsearch.yml` 파일에서 다음과 같이 설정:
   ```yaml
   discovery.type: single-node
   ```

2. **Elasticsearch 로그 확인**
   ```bash
   sudo tail -f /var/log/elasticsearch/elasticsearch.log
   ```

3. **메모리 잠금 문제 해결**
   `/etc/elasticsearch/elasticsearch.yml` 파일에서 다음을 추가:
   ```yaml
   bootstrap.mlockall: true
   ```

4. **`vm.max_map_count` 값 증가**
   ```bash
   sudo sysctl -w vm.max_map_count=262144
   ```

---

## 3. Elasticsearch 연결 문제 (Unable to connect to localhost:9200)
`curl http://localhost:9200` 명령어로 Elasticsearch에 접속할 수 없는 경우.

### 원인
- Elasticsearch가 제대로 실행되지 않음
- 방화벽 설정 문제

### 해결 방법
1. **Elasticsearch 서비스 상태 확인**
   ```bash
   sudo systemctl status elasticsearch
   ```

2. **방화벽에서 포트 9200 열기**
   ```bash
   sudo ufw allow 9200/tcp
   ```

3. **Elasticsearch 설정 수정**
   `/etc/elasticsearch/elasticsearch.yml` 파일에서 다음과 같이 설정:
   ```yaml
   network.host: 0.0.0.0
   ```

4. **Elasticsearch 로그 확인**
   ```bash
   sudo journalctl -xeu elasticsearch.service
   ```

---

## 4. Kibana와 Elasticsearch 간 연결 문제
Kibana가 Elasticsearch에 연결할 수 없는 경우.

### 원인
- Kibana 설정 파일에서 `elasticsearch.hosts` 값이 잘못 설정된 경우.

### 해결 방법
1. **Kibana 설정 파일 수정**
   `/etc/kibana/kibana.yml` 파일에서 다음과 같이 설정:
   ```yaml
   elasticsearch.hosts: ["http://localhost:9200"]
   ```

2. **호스트 상태 확인**
   Kibana와 Elasticsearch가 동일한 호스트에서 실행 중인지 확인.

3. **버전 호환성 확인**
   Kibana와 Elasticsearch의 버전이 호환되는지 확인.

---

## 5. Elasticsearch 보안 인증 관리
Elasticsearch의 보안 기능 활성화로 인해 HTTP 인증이 필요한 상황에서 발생하는 문제.

### 원인
- 보안 인증 또는 HTTPS 설정으로 인해 연결 제한 발생.

### 해결 방법

1. **보안 인증 비활성화**
   `/etc/elasticsearch/elasticsearch.yml` 파일에서 다음과 같이 수정:
   ```yaml
   xpack.security.enabled: false
   xpack.security.http.ssl.enabled: false
   ```

   **수정 후 적용:**
   ```bash
   sudo systemctl restart elasticsearch
   ```

2. **Elasticsearch 연결 확인**
   ```bash
   curl -X GET "http://127.0.0.1:9200/"
   ```

---

### 추가 참고 사항
- **로그**를 반드시 **확인**하여 구체적인 오류를 **분석**하고 해결
- 각 **설정 파일을 수정**한 뒤에는 변경 사항 반영을 위해 **서비스를 반드시 재시작**

```bash
sudo systemctl restart kibana
sudo systemctl restart elasticsearch
```


----

# 🤔 회고

