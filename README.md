<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=venom&color=54B399&height=150&section=header&text=ELK%20With%20Ubuntu&fontSize=60" alt="Header" width="100%">
</p>


<aside>

## 👨🏻‍💻 프로젝트 개요
**고객 소비 데이터**를 기반으로 **소비 패턴과 선호도를 분석**하여 **새로운 고객군을 정의**하고, **맞춤형 카드 혜택**을 제안하는 것을 목표로 합니다. **카드 사용 데이터**를 활용해 고객의 **라이프스타일**과 **소비 취향**에 최적화된 혜택을 제공하며, **분기별 소비 패턴 분석**을 통해 **혜택 구조**를 유연하게 조정하여 **고객 만족도**를 높이고자 합니다.
<br>
## 👨‍👨‍👦‍👦 팀원 소개
| <img src="https://github.com/wns5120.png" width="200px"> | <img src="https://github.com/JaeHee-devSpace.png" width="200px"> | <img src="https://github.com/andytjdqls.png" width="200px"> | <img src="https://github.com/wild-turkey.png" width="200px"> |
| :---: | :---: | :---: | :---: |
| [유호준](https://github.com/wns5120) | [박재희](https://github.com/JaeHee-devSpace) | [이성빈](https://github.com/andytjdqls) | [김지훈](https://github.com/wild-turkey) |

## 📚 기술 스택
 ![Requests](https://img.shields.io/badge/Requests-00599C?style=flat&logo=python&logoColor=white) ![Visual Studio Code](https://img.shields.io/badge/VSCode-007ACC?style=flat&logo=visualstudiocode&logoColor=white)  ![Logstash](https://img.shields.io/badge/Logstash-005571?style=flat&logo=elastic&logoColor=white) ![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=flat&logo=elastic&logoColor=white) ![Kibana](https://img.shields.io/badge/Kibana-005571?style=flat&logo=elastic&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black) ![VirtualBox](https://img.shields.io/badge/VirtualBox-183A61?style=flat&logo=virtualbox&logoColor=white) ![MobaXterm](https://img.shields.io/badge/MobaXterm-008FBA?style=flat&logoColor=white)  ![Markdown](https://img.shields.io/badge/Markdown-000000?style=flat&logo=markdown&logoColor=white) ![ChatGPT](https://img.shields.io/badge/ChatGPT-412991?style=flat&logo=openai&logoColor=white)

<br>

## 🎯 프로젝트 목표
**실무 데이터의 분석:**
- 다양한 시각화 아이디어를 기반으로 실무 데이터를 분석하여 유의미한 인사이트를 도출합니다.

**시각화 아이디어를 기반으로 데이터 인사이트 도출:**
- 데이터를 직관적으로 이해할 수 있도록 다양한 차트와 그래프를 활용해 분석 결과를 시각화합니다.

**고객 친화적인 대시보드와 새로운 기능 설계:**
- 분석 결과를 바탕으로 최종 사용자가 쉽게 활용할 수 있는 대시보드를 설계하고, 새로운 기능을 제안합니다.

       
<br>

## 💡 주요 기술적 목표 
- LINUX OS에 ELK 스택 설치 및 설정
- 포트포워딩 설정
- Kibana를 활용한 시각화 및 대시보드 설계
- Elasticsearch 성능 최적화

<br>

## 📐 System Architecture
<div align="center">
  <img src="https://github.com/user-attachments/assets/dfefaaf0-a9bb-4eb0-826a-6d66c086173e" alt="Architecture Diagram" style="width: 80%; max-width: 800px; height: auto;">
</div>

<br>

## 🗂️ 데이터 분석
### 1. 시각화 아이디어

- 나이별 이용금액 비교
- 등급별 이용금액 비교
- 분기별 이용금액 비교
- 거주지역별 이용금액 비교
- 성별 이용금액 비교
- 특정 카테고리(예: 가전/가구/주방용품) 이용금액 비교
   - OO별(예: 지역, 나이 등) 가장 높은 이용금액
- 나이별 등급 분포
   - 나이가 많을수록 VVIP 비율이 높은가?
- 디지털 채널 가입 여부별 이용금액 비교
- 라이프 스테이지별 이용금액 비교
- 고객 등급별 비율 비교
   - VVIP+VIP vs 일반 고객
- 가장 높은 이용금액을 기록한 카테고리
   - 중분류, 대분류 기준
- 업종별 VVIP 분포
   - VVIP가 많은 업종 탐색
- 등급별 이용금액의 최대값/최솟값 비교
   - 등급 업그레이드 기준 탐색


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

# 🌟 맞춤형 카드 혜택
### 1. **주요 타겟 고객군 정의**

- **연령대**: 소비 금액이 가장 많은 **40대**
  ![1](https://github.com/user-attachments/assets/bc997214-5bc9-42e1-b744-08412e9add17)

- **회원 등급**: **골드 등급**
  ![2](https://github.com/user-attachments/assets/0b422dfb-1042-4ae9-abb5-3862c3900540)

- **지역**: **서울 및 경기 거주**
  ![3](https://github.com/user-attachments/assets/34fb3db7-809f-4835-a4f7-5f25a9a9eddb)

- **가족 구성**: **의무교육을 받고 있는 자녀**가 있는 고객
  ![4](https://github.com/user-attachments/assets/c0574f99-a1c9-4f3d-a5af-ab9cba9765a9)


### 2. **추천 상품 설계**

- **연회비가 높은 대신, 캐시백 혜택이 많은 카드 상품**을 이 고객군에 추천
    - **고객 관점의 이점**: 월별 카드 사용 금액에 비례한 높은 캐시백 혜택 제공
    - **기업 관점의 이점**: 연회비를 통한 추가 수익 창출

### 3. **시사점 및 비즈니스 성과**

- **기업 이득**:
    - 연회비를 많이 징수함으로써 안정적인 수익 확보 가능
    - 높은 소비 금액을 가진 고객 유지 및 추가 유치
- **고객 이득**:
    - 카드 사용에 따른 직접적인 캐시백 혜택으로 만족도 증가
    - 소비 습관에 최적화된 상품으로 실질적인 혜택 체감

### 4. **추가 인사이트 및 활용 방안**

- **분기별 소비 패턴 분석 기반 혜택 조정**
    - 40대 골드 등급 고객의 **월별 주요 소비 카테고리(예: 자녀 교육비, 주유, 대형마트)**를 분석하여 분기별로 혜택 최적화.
    - 특정 분기에 소비가 많은 항목(예: 신학기 교육비)에 대해 추가 혜택 제공.
- **추가 고객군 발굴**
    - 유사한 소비 패턴을 보이는 **다른 연령대** 또는 **등급**의 고객군에 대한 확장 적용 가능성 평가.

### 5. **결론**

본 프로젝트를 통해 도출된 고객 맞춤형 전략은 기업과 고객 모두에게 **Win-Win**이 되는 결과를 낳았습니다.

이를 바탕으로 지속적으로 데이터 기반 마케팅을 활용해 효율적인 상품 설계와 고객 만족도를 향상시킬 수 있는 방안을 모색할 수 있습니다.

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
   ![image](https://github.com/user-attachments/assets/f7217c27-d22b-4637-8a29-a4048c0c5b40)

   
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
![image](https://github.com/user-attachments/assets/1e20eb12-c99b-4bcb-8914-d479223b3d5e)


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

4. **포트포워딩 확인**
   ![image](https://github.com/user-attachments/assets/4020b34f-451e-4bd2-8818-f1caa36a7abc)

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
이번 프로젝트를 통해 ELK 스택을 가상환경에 설치하면서 다양한 오류를 겪었고, 이를 해결하며 환경 설정의 중요성을 깊이 깨달았습니다. 특히, Elasticsearch와 Kibana의 버전을 일치시키는 것이 안정적인 스택 구성을 위해 필수적이라는 점을 느꼈습니다. 또한, 스택 간 통신을 위해 .yml 파일을 상황에 맞게 정확히 수정해야 한다는 사실을 알게 되었습니다.

Windows 환경에서 사용했던 ELK 스택을 Linux 환경에 설치하며, 환경 설정을 복습하고 새로운 관점을 얻을 수 있었습니다. 더불어, ELK 스택을 활용해 데이터를 분석하고 개인화된 마케팅 전략을 설계하는 과정에서 자료의 우선순위를 정하고 시각화하는 경험을 하였습니다.

