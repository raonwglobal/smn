# SMNetworks

**Network Security · Infrastructure · AX/DX Consulting**

**SMNetworks Company** 공식 웹사이트입니다.

Technical Director: **magnox**  
전문 분야: Network Security, Xen / Hyper-V, Nutanix, 엔터프라이즈 인프라, AX/DX  
주요 실적: Lotte Group, Shinhan 등 국내 대기업 인프라  
위치: 베트남 호치민시 Quan 7  
시작: 2008년 (한–베 엔터프라이즈 인프라)

---

## 라이브 사이트

이 저장소는 **Cloudflare Pages**에 배포하는 것을 전제로 합니다.

- 정적 SPA (`index.html` 셸 + `assets/`)
- 빌드 단계 없음
- 권장 Cloudflare Pages 설정:
  - **Framework preset**: None
  - **Build command**: *(비워 둠)*
  - **Build output directory**: `/` (또는 비워 둠)
  - **Root directory**: `/`

GitHub 저장소를 Cloudflare Pages에 연결하면 `main` 브랜치에 push할 때마다 자동으로 사이트가 게시됩니다.

---

## 프로젝트 구조

```
.
├── index.html              # HTML 셸 + SEO 메타
├── assets/
│   ├── app.css             # Tailwind 유틸리티
│   ├── content.js          # i18n / 카피 (ko · en · vi) — 문구 수정은 여기
│   └── app.js              # React 런타임 + UI
├── README.md               # 영어 버전
├── README.ko.md            # 이 파일 (한국어)
├── LICENSE                 # MIT
└── .gitignore
```

빌드 없음(완전 정적). 마케팅 문구는 **`assets/content.js`** 를 수정하세요.

> **참고**  
> `.agents/` 디렉터리와 `AGENTS.md`(로컬에 존재하는 경우)는 AI 코딩 보조 도구(luna-chat-coder 등)용입니다.  
> 웹사이트 코드의 일부가 **아니며**, `.gitignore`에 등록되어 있고, 게시된 사이트나 프로덕션 산출물에 포함되어서는 안 됩니다.

---

## 기술 스택

- React 애플리케이션 (`assets/app.js` 사전 번들)
- Tailwind CSS (`assets/app.css`)
- 카피/i18n 분리 (`assets/content.js` — 한국어 / 영어 / 베트남어)
- 완전 정적 — 모든 정적 호스트에서 동작, Cloudflare Pages / CDN에 최적화
- 브랜드 마크: **SMN** (헤더·푸터)
- 경력 연수(2008년 기준)는 런타임에 자동 계산

---

## 로컬 미리보기

ES 모듈 로드를 위해 HTTP 서버로 실행하세요.

```bash
# 저장소 루트에서
python -m http.server 8080

# 또는 Node
npx serve .
```

이후 `http://localhost:8080`을 엽니다.

---

## Cloudflare 배포 체크리스트

1. [Cloudflare Dashboard](https://dash.cloudflare.com) 로그인 → **Workers & Pages** → **Create** → **Pages** → Git 연결.
2. 저장소 `raonwglobal/smn` 선택.
3. 설정:
   - Production branch: `main`
   - Build command: *(비움)*
   - Build output directory: `/` 또는 비움
4. Deploy.
5. (선택) 커스텀 도메인 연결 및 Cloudflare SSL / CDN 기능 활성화.

Node.js, package.json, 빌드 파이프라인은 필요하지 않습니다.

---

## 문의

- Email: [magnox@sm-networks.net](mailto:magnox@sm-networks.net)
- LinkedIn: [magnox](https://www.linkedin.com/in/magnox-netnox-a856443a)

---

## 라이선스

MIT — [LICENSE](LICENSE) 참고.
