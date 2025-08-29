# 🚀 GreenWear Replit 배포 가이드

## 📋 **Replit 프로젝트 설정**

### **1. Replit 프로젝트 생성**
1. [Replit](https://replit.com/login?source=home&goto=%2F%7E)에 로그인
2. **Create Repl** 클릭
3. **Import from GitHub** 선택
4. 저장소: `saway126/greaenwear`
5. 언어: **Java** 선택

### **2. 환경 설정**
- **RAM**: Hobby 플랜 권장 (1GB)
- **CPU**: 1 코어
- **디스크**: 1GB (충분)

## 🛠️ **배포 단계**

### **1단계: 프로젝트 클론**
```bash
git clone https://github.com/saway126/greaenwear.git
cd greaenwear
```

### **2단계: 백엔드 실행**
```bash
cd backend-spring/demo
./gradlew bootRun --args='--spring.profiles.active=replit'
```

### **3단계: 프론트엔드 실행 (새 터미널)**
```bash
cd frontend
npm install
npm run dev
```

## 🌐 **접속 정보**

### **백엔드 API**
- **URL**: `https://your-repl-name.your-username.repl.co`
- **포트**: 8080
- **Health Check**: `/health`
- **SSE 스트림**: `/vitals/stream?deviceId=test`

### **프론트엔드**
- **URL**: `https://your-repl-name.your-username.repl.co:5173`
- **포트**: 5173

## 🔧 **Replit 최적화 설정**

### **환경 변수**
```bash
JAVA_HOME=/nix/store/*/openjdk-21
PATH=/nix/store/*/openjdk-21/bin:$PATH
```

### **포트 설정**
- 백엔드: 8080
- 프론트엔드: 5173
- H2 데이터베이스: 8080/h2-console

## 📊 **모니터링**

### **Replit 대시보드**
- **Resources**: CPU, RAM, 디스크 사용량
- **Logs**: 애플리케이션 로그
- **Console**: 터미널 출력

### **Health Check**
```bash
curl https://your-repl-name.your-username.repl.co/health
```

## 🚨 **문제 해결**

### **메모리 부족**
- Hobby 플랜으로 업그레이드
- 불필요한 로그 레벨 낮추기

### **포트 충돌**
- Replit에서 포트 설정 확인
- 방화벽 설정 확인

### **빌드 실패**
- Java 21 설치 확인
- Gradle 캐시 정리

## 💰 **비용 최적화**

### **무료 플랜 (500MB RAM)**
- 백엔드만 실행
- 프론트엔드는 정적 파일로 빌드

### **Hobby 플랜 ($7/월)**
- 백엔드 + 프론트엔드 동시 실행
- SSE 스트림 실시간 동작

## 🎯 **성공 지표**

- ✅ 백엔드 서버 시작 (8080 포트)
- ✅ 프론트엔드 서버 시작 (5173 포트)
- ✅ SSE 스트림 연결 성공
- ✅ 생체신호 데이터 실시간 수신
- ✅ UI/UX 정상 동작

---

**🚀 GreenWear가 Replit에서 성공적으로 실행되면, 전 세계 어디서나 접근 가능한 실시간 생체신호 모니터링 시스템이 완성됩니다!**
