계산기 웹페이지를 Flask로 구현해주세요.

## 요구사항

### 기술 스택
- Flask (Python 웹 프레임워크)
- HTML5, CSS3, JavaScript (ES6+)
- 프론트엔드는 순수 HTML/CSS/JavaScript로 구현 (프레임워크 없음)

### 기능 요구사항
1. 기본 사칙연산 계산기
   - 숫자 입력 (0-9)
   - 사칙연산 (+, -, ×, ÷)
   - 등호(=) 계산
   - 초기화(C) 기능
   - 소수점(.) 지원
   - 키보드 입력 지원
   - 연산자 우선순위 처리

2. UI/UX 요구사항
   - 모던한 디자인 (그리드 레이아웃)
   - 반응형 디자인
   - 버튼 호버 효과
   - 시각적 피드백
   - 디스플레이 영역 (계산 결과 표시)

### 파일 구조
```
BrowserDemo/
├── app.py                 # Flask 애플리케이션 메인 파일
├── requirements.txt       # Flask 의존성 파일
├── templates/
│   └── index.html        # 계산기 메인 HTML 페이지
├── static/
│   ├── css/
│   │   └── style.css     # 계산기 스타일시트
│   └── js/
│       └── calculator.js # 계산기 로직 (JavaScript)
└── README.md             # 설치 및 실행 방법 포함
```

### 구현 세부사항

#### Flask 서버 (app.py)
- Flask 애플리케이션 생성
- 루트 경로('/')에서 index.html 렌더링
- 정적 파일 서빙 설정
- 개발 모드로 실행 (debug=True)

#### HTML (templates/index.html)
- 계산기 UI 구조
- 디스플레이 영역
- 버튼 그리드 레이아웃
- CSS와 JavaScript 파일 연결

#### CSS (static/css/style.css)
- 모던한 다크 테마 디자인
- 그라데이션 배경
- 그리드 레이아웃으로 버튼 배치
- 반응형 디자인 (모바일 지원)
- 버튼 호버 및 액티브 효과
- 등호 버튼은 2행에 걸쳐 배치

#### JavaScript (static/js/calculator.js)
- 계산기 상태 관리 (currentInput, previousInput, operator)
- 숫자 입력 처리
- 연산자 처리
- 계산 로직 (사칙연산)
- 소수점 처리
- 키보드 이벤트 핸들링
- 0으로 나누기 오류 처리
- 디스플레이 업데이트

### 실행 방법
1. Python 가상환경 생성 및 활성화
2. `pip install -r requirements.txt`로 의존성 설치
3. `python app.py`로 서버 실행
4. 브라우저에서 `http://localhost:5000` 접속

### 추가 고려사항
- 코드는 깔끔하고 주석이 잘 달려있어야 함
- 에러 처리가 적절히 구현되어야 함
- 사용자 경험이 좋아야 함 (시각적 피드백, 반응성 등)

