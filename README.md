# 🌍 공간 임베딩 튜토리얼 (Spatial Embedding Tutorial)

https://nbviewer.org/github/thlee33/understand_embeding/blob/main/embedding_tutorial.ipynb  

컴퓨터가 지구 전체나 특정 장소를 어떻게 기억하고 분석하는지 궁금했나요? 이 튜토리얼은 컴퓨터가 지도 위의 다양한 속성(바다, 도시, 산, 사막)을 어떻게 숫자 암호인 **'임베딩(Embedding)'**으로 바꾸어 이해하는지 흥미롭고 쉽게 설명하는 가이드라인입니다.

가로세로 200m 크기의 아주 작은 2x2 가상 세계부터 시작하여, 실제 구글이나 NVIDIA 등이 사용하는 고차원 공간 임베딩의 원리까지 파이썬 코드를 통해 재미있게 학습해 봅니다.

---

## 🗺️ 학습 목차

1. **1단계: 우리만의 작은 세상(2x2 격자 지도) 만들기**
   - 바다(🌊), 도시(🏢), 산(🌲), 사막(🏜️)으로 이루어진 200m x 200m 공간 생성 및 시각화
2. **2단계: 1비트 임베딩으로 시작하기**
   - 이진 암호(0과 1)로 공간 정보 표현하기
3. **3단계: 고차원(128차원) 임베딩의 마법**
   - 단순 구분을 넘어 공간의 의미적 유사성을 벡터 공간에 투영하는 방법 학습
   - 코사인 유사도(Cosine Similarity)를 이용한 지역 간 속성 비교 실습
4. **4단계: 현실의 공간 임베딩 기술**
   - 구글 맵, 자율주행, 기상 예보 AI 등에서 사용되는 실제 공간 임베딩 응용 모델 소개

---

## 🛠️ 개발 환경 및 실행 방법

이 프로젝트는 파이썬(Python) 환경에서 실행되며, 초고속 파이썬 패키지 매니저인 **uv**를 사용하여 가상환경을 구축합니다.

### 1. 가상환경 생성 및 패키지 설치
터미널을 열고 프로젝트 폴더 경로에서 다음 명령어를 순서대로 실행하세요.

```bash
# 1. uv를 사용하여 .venv 가상환경 생성
uv venv

# 2. 가상환경 활성화 (Windows PowerShell 기준)
.venv\Scripts\Activate.ps1

# 3. 실습에 필요한 패키지 설치 (matplotlib 한글 깨짐 방지용 koreanize-matplotlib 포함)
uv pip install numpy matplotlib scipy koreanize-matplotlib notebook jupyter
```

### 2. 주피터 노트북 실행
패키지 설치가 완료되면 아래 명령어로 주피터 노트북을 열어 실습을 시작할 수 있습니다.

```bash
jupyter notebook embedding_tutorial.ipynb
```
(또는 VS Code 등의 에디터에서 `embedding_tutorial.ipynb` 파일을 직접 열고 우측 상단 커널을 `.venv`로 선택하여 실습을 진행할 수 있습니다.)

---

## 📊 시각화 및 주요 라이브러리
- **NumPy**: 공간 데이터를 수치화하고 벡터 연산을 수행합니다.
- **Matplotlib & Koreanize-Matplotlib**: 공간 격자 및 임베딩 유사도 그래프를 한글 깨짐 없이 미려하게 시각화합니다.
- **SciPy**: 벡터 간 거리 및 코사인 유사도를 계산합니다.
