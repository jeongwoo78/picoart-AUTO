# 🚀 PicoArt v5 - 자동 설정 완료!

## ✅ vercel.json 파일 1개만 수정하면 끝!

**코드 파일(convert.js)은 건드릴 필요 없어요!**

---

## 📝 배포 2단계

### 1️⃣ GitHub 업로드

```
1. https://github.com/new 접속
2. Repository name: picoart-final-deploy
3. ✅ Public 선택 (필수!)
4. Create repository
5. "uploading an existing file" 클릭
6. 압축 푼 모든 파일 업로드
   ⚠️ artworks 폴더 반드시 포함!
7. Commit changes
```

### 2️⃣ vercel.json 수정 (딱 2줄!)

**GitHub 저장소에서:**
```
1. vercel.json 파일 클릭
2. 연필 아이콘 (Edit) 클릭
3. 3-4번째 줄 수정:
```

**수정 전:**
```json
{
  "version": 2,
  "env": {
    "GITHUB_USER": "YOUR-USERNAME",
    "GITHUB_REPO": "YOUR-REPO"
  }
}
```

**수정 후:**
```json
{
  "version": 2,
  "env": {
    "GITHUB_USER": "jeongwoo78",
    "GITHUB_REPO": "picoart-final-deploy"
  }
}
```

**4. Commit changes 클릭**

### 3️⃣ Vercel 배포

```
1. https://vercel.com/new
2. Import Git Repository
3. picoart-final-deploy 선택
4. Deploy 클릭
5. 완료! ✨
```

---

## 🎯 왜 이 방법이 좋나요?

### ✅ 장점
- **파일 1개만 수정** (vercel.json)
- **코드(convert.js) 건드리지 않음**
- **환경 변수 자동 적용**
- **재배포 시 설정 유지**

### 🔧 작동 원리
```
vercel.json → 환경 변수 설정
    ↓
convert.js → 환경 변수 자동 읽기
    ↓
GitHub URL 자동 생성
```

---

## ✅ 테스트

### 1. 이미지 URL 확인
브라우저에서:
```
https://raw.githubusercontent.com/jeongwoo78/picoart-final-deploy/main/artworks/vangogh/01_starry_night.jpg
```
→ 이미지가 보이면 성공!

### 2. 사이트 테스트
```
1. 시크릿 창에서 사이트 접속
2. F12 → Console
3. Replicate API 토큰 입력
4. Van Gogh 선택
5. 사진 업로드
6. 변환 시작
```

### 3. Console 확인
```
🌐 GitHub User: jeongwoo78
📦 GitHub Repo: picoart-final-deploy
🖼️ Artwork URL: https://raw.githubusercontent.com/.../artworks/vangogh
🎨 ===== AI Auto-Matching =====
✅ Prediction created!
```

---

## 🔍 문제 해결

### 422 에러?
1. **GitHub 저장소가 Public인지 확인**
2. **vercel.json의 GitHub 정보가 올바른지 확인**
3. **artworks 폴더가 업로드되었는지 확인**

### 환경 변수가 적용 안 됨?
- Vercel에서 재배포 (Project → Deployments → 최신 배포의 점 3개 → Redeploy)

---

## 📋 수정해야 할 파일

**✅ vercel.json (딱 이것만!)**
```json
"GITHUB_USER": "본인아이디",
"GITHUB_REPO": "본인저장소"
```

**❌ convert.js (수정 불필요!)**
```javascript
// 이미 자동으로 환경 변수 읽음
const GITHUB_USER = process.env.GITHUB_USER;
```

---

## 🎊 요약

### 수정할 것
- **vercel.json** → 2줄 (GitHub 아이디, 저장소명)

### 수정 안 해도 되는 것
- **convert.js** → 자동 처리됨
- **index.html** → 완벽함
- **status.js** → 완벽함

---

## 💡 팁: Vercel 대시보드에서 설정하기

vercel.json 수정 대신 Vercel 대시보드에서도 가능:

```
1. Vercel 프로젝트 → Settings
2. Environment Variables
3. Add New:
   - Key: GITHUB_USER, Value: jeongwoo78
   - Key: GITHUB_REPO, Value: picoart-final-deploy
4. Save
5. Redeploy
```

이 방법은 vercel.json 수정도 필요 없어요!

---

**수정: vercel.json 딱 2줄!**
**끝! 🎉**
