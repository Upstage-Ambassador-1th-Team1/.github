<p align="center">
  <!-- Replace with your logo -->
  <img width="994" height="616" alt="logo" src="https://github.com/user-attachments/assets/f893d2ee-8927-4f27-896d-a3d5dd981a56" width="45%"/>

</p>

<h1 align="center">Jibchack (집착)</h1>

<p align="center">
  <strong>AI-Powered Public Rental Housing Search Platform</strong><br>
  <em>AI 기반 공공임대주택 검색 플랫폼</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Upstage-Solar%20Pro2-FF6B35?style=flat-square&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij48Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIgZmlsbD0iI0ZGNkIzNSIvPjwvc3ZnPg==" alt="Upstage"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white" alt="Streamlit"/>
  <img src="https://img.shields.io/badge/Apache%20Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white" alt="Airflow"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker"/>
</p>

<p align="center">
  <a href="#demo">Demo</a> •
  <a href="#features">Features</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#repositories">Repositories</a> •
  <a href="#tech-stack">Tech Stack</a> •
  <a href="#getting-started">Getting Started</a>
</p>

---

## Demo

<p align="center">
  <!-- Replace with actual screenshots -->
  <video src="https://github.com/user-attachments/assets/91e1a38d-4696-4a66-91ca-ac8ad57514ac" alt="Map Search" width="45%"/>

</p>

---

## Features

### AI Chatbot | AI 챗봇
Ask questions in natural language and get personalized public housing recommendations.
> 자연어로 질문하면 맞춤형 공공임대주택을 추천받을 수 있습니다.

### Map-Based Search | 지도 검색
Explore available housing on an interactive map with filters for region, price, and size.
> 지역, 가격, 면적 필터와 함께 인터랙티브 지도에서 주택을 탐색하세요.

### Automated Data Collection | 자동 데이터 수집
Daily automated crawling of SH and LH housing announcements with AI-powered information extraction.
> SH, LH 공고를 매일 자동 크롤링하고 AI로 정보를 추출합니다.

---

## Architecture

```
┌─────────────────────────────────────────────────────────────────────────┐
│                         Jibchack Platform                               │
└─────────────────────────────────────────────────────────────────────────┘
                                    │
         ┌──────────────────────────┼──────────────────────────┐
         │                          │                          │
         ▼                          ▼                          ▼
┌─────────────────┐      ┌─────────────────┐      ┌─────────────────┐
│  Data-ETL       │      │  Embedding      │      │  jibchack       │
│  Pipeline       │      │  chatBot        │      │  -backend       │
│                 │      │                 │      │                 │
│  • SH/LH        │      │  • RAG Engine   │      │  • REST API     │
│    Crawling     │ ───▶ │  • pgvector     │ ───▶ │  • LLM Service  │
│  • Airflow      │      │  • Embeddings   │      │  • Search API   │
│  • AI Extract   │      │                 │      │                 │
└─────────────────┘      └─────────────────┘      └────────┬────────┘
                                                           │
                                                           ▼
                                                 ┌─────────────────┐
                                                 │  streamlit      │
                                                 │  -homepage      │
                                                 │                 │
                                                 │  • Chat UI      │
                                                 │  • Map View     │
                                                 │  • Filters      │
                                                 └─────────────────┘
                                                           │
                                                           ▼
                                                      [ Users ]
```

---

## Repositories

| Repository | Description | Tech Stack |
|------------|-------------|------------|
| **[Data-ETL-Pipeline](./Data-ETL-PipeLIne)** | Automated data collection from SH/LH websites with AI-powered information extraction | Apache Airflow, Selenium, BeautifulSoup, Upstage API |
| **[Embedding_chatBot](./Embedding_chatBot)** | RAG-based chatbot engine with vector search capabilities | FastAPI, pgvector, LangChain, Redis |
| **[jibchack-backend](./jibchack-backend)** | Main API server providing housing data and chat services | FastAPI, SQLAlchemy, Upstage Solar LLM |
| **[streamlit-homepage](./streamlit-homepage)** | User-friendly web interface with chat and map features | Streamlit, Folium, Kakao Maps API |

---

## Tech Stack

### AI / ML
- **[Upstage Solar Pro2](https://www.upstage.ai/)** - Korean-optimized Large Language Model
- **[Upstage Embeddings](https://www.upstage.ai/)** - Text embedding for semantic search
- **[LangChain](https://langchain.com/)** - LLM orchestration framework

### Backend
- **[FastAPI](https://fastapi.tiangolo.com/)** - High-performance Python web framework
- **[PostgreSQL](https://www.postgresql.org/)** - Relational database
- **[pgvector](https://github.com/pgvector/pgvector)** - Vector similarity search extension
- **[SQLAlchemy](https://www.sqlalchemy.org/)** - Python ORM
- **[Redis](https://redis.io/)** - Session and cache management

### Frontend
- **[Streamlit](https://streamlit.io/)** - Python web app framework
- **[Folium](https://python-visualization.github.io/folium/)** - Interactive map visualization
- **[Kakao Maps API](https://apis.map.kakao.com/)** - Geocoding service

### Data Pipeline
- **[Apache Airflow](https://airflow.apache.org/)** - Workflow orchestration
- **[Selenium](https://www.selenium.dev/)** - Dynamic web crawling
- **[BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/)** - HTML parsing

### Infrastructure
- **[Docker](https://www.docker.com/)** - Containerization
- **[Docker Compose](https://docs.docker.com/compose/)** - Multi-container orchestration

---

## Getting Started

### Prerequisites
- Python 3.11+
- Docker & Docker Compose
- PostgreSQL with pgvector extension
- Upstage API Key

### Quick Start

```bash
# Clone all repositories
git clone https://github.com/YOUR_ORG/Data-ETL-Pipeline.git
git clone https://github.com/YOUR_ORG/Embedding_chatBot.git
git clone https://github.com/YOUR_ORG/jibchack-backend.git
git clone https://github.com/YOUR_ORG/streamlit-homepage.git
```

### Running Services with Docker

**1. Data Pipeline** (Airflow - Port 8081)
```bash
cd Data-ETL-Pipeline
cp .env.example .env  # Configure environment variables
docker-compose up -d
# Access Airflow UI: http://localhost:8081
```

**2. Backend API** (FastAPI - Port 8000)
```bash
cd jibchack-backend/backend
cp .env.example .env  # Configure environment variables
docker-compose up -d
# API available at: http://localhost:8000
```

**3. Frontend** (Streamlit - Port 8501)
```bash
cd streamlit-homepage
cp .env.example .env  # Configure environment variables
docker-compose up -d
# Access UI: http://localhost:8501
```

For detailed setup instructions, please refer to each repository's README.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<br>

<h1 align="center">한국어 안내</h1>

## 프로젝트 소개

**집착(Jibchack)** 은 공공임대주택 정보를 AI로 쉽게 검색할 수 있는 플랫폼입니다.

SH(서울주택도시공사)와 LH(한국토지주택공사)의 공공임대주택 공고를 자동으로 수집하고, AI 챗봇을 통해 자연어로 검색할 수 있습니다.

### 주요 기능

| 기능 | 설명 |
|------|------|
| **AI 챗봇** | "청년이 신청할 수 있는 임대주택 알려줘" 같은 자연어 질문으로 맞춤 추천 |
| **지도 검색** | 원하는 지역의 공공임대주택을 지도에서 한눈에 확인 |
| **자동 수집** | 매일 SH/LH 공고를 자동으로 크롤링하고 AI로 정보 추출 |
| **실시간 응답** | 스트리밍 방식으로 빠른 채팅 응답 제공 |

### 기술적 특징

- **Upstage Solar Pro2**: 한국어에 최적화된 대형 언어 모델 사용
- **RAG 아키텍처**: 검색 증강 생성으로 정확한 정보 제공
- **하이브리드 검색**: 벡터 유사도(70%) + 키워드 매칭(30%) 결합
- **자동화 파이프라인**: Apache Airflow로 매일 자동 데이터 수집

### 레포지토리 구성

```
upstage/
├── Data-ETL-Pipeline/    # 데이터 수집 파이프라인
├── Embedding_chatBot/    # RAG 챗봇 엔진
├── jibchack-backend/     # API 백엔드 서버
└── streamlit-homepage/   # 웹 프론트엔드
```

### 지원 주택 유형

**SH 공사**: 국민공공임대주택, 도시형생활주택, 매입임대주택, 장기안심주택, 장기전세주택, 청년안심주택, 행복주택 등

**LH 공사**: 국민임대, 공공임대, 영구임대, 행복주택, 매입임대 등

---

## 시작하기

### 필수 요구사항
- Python 3.11 이상
- Docker & Docker Compose
- PostgreSQL (pgvector 확장 포함)
- Upstage API 키

### 환경 설정

각 레포지토리의 `.env.example` 파일을 참고하여 환경 변수를 설정하세요.

```bash
# 주요 환경 변수
UPSTAGE_API_KEY=your_api_key
DB_HOST=localhost
DB_NAME=sh_housing_db
DB_USER=postgres
DB_PASSWORD=your_password
```

### 실행 방법 (Docker)

**1. 데이터 수집 파이프라인** (Airflow - 포트 8081)
```bash
cd Data-ETL-Pipeline
cp .env.example .env  # 환경 변수 설정
docker-compose up -d
# Airflow UI: http://localhost:8081 (기본 계정: admin/admin)
```

**2. 백엔드 API 서버** (FastAPI - 포트 8000)
```bash
cd jibchack-backend/backend
cp .env.example .env  # 환경 변수 설정
docker-compose up -d
# API 문서: http://localhost:8000/docs
```

**3. 프론트엔드** (Streamlit - 포트 8501)
```bash
cd streamlit-homepage
cp .env.example .env  # 환경 변수 설정
docker-compose up -d
# 웹 UI: http://localhost:8501
```

### 전체 서비스 중지
```bash
# 각 디렉토리에서
docker-compose down
```

---

## 팀 정보

<!-- Add team member information here -->
| 역할 | 이름 | GitHub |
|------|------|--------|
| 팀장 | 박태영 | [@taeyoung1005](https://github.com/taeyoung1005) |
| 팀원 | 허예진 | [@dpqhd01](https://github.com/dpqhd01) |
| 팀원 | 신재영 | [@LimePencil](https://github.com/LimePencil) |
| 팀원 | 이재용 | [@Sharon0320](https://github.com/Sharon0320) |
| 팀원 | 박다영 | [@bydayoung](https://github.com/bydayoung) |

---

<p align="center">
  Made with Upstage Solar API
</p>
