# SMNetworks

**Network Security · Infrastructure · AX/DX Consulting**

**SMNetworks / NST Company** 공식 웹사이트입니다.

Technical Director: **magnox netnox**  
전문 분야: Network Security, Xen / Hyper-V, Nutanix, 엔터프라이즈 인프라  
주요 실적: Lotte Group, Shinhan 등 국내 대기업 인프라  
위치: 베트남 호치민시 Quan 7

---

## 라이브 사이트

이 저장소는 **Cloudflare Pages**에 배포하는 것을 전제로 합니다.

- 정적 단일 페이지 애플리케이션 (`index.html`이 저장소 루트에 위치)
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
├── index.html          # 완전한 SPA (React + Tailwind, 단일 파일)
├── README.md           # 영어 버전
├── README.ko.md        # 이 파일 (한국어)
├── LICENSE             # MIT
└── .gitignore
```

> **참고**  
> `.agents/` 디렉터리와 `AGENTS.md`(로컬에 존재하는 경우)는 AI 코딩 보조 도구(luna-chat-coder 등)용입니다.  
> 웹사이트 코드의 일부가 **아니며**, `.gitignore`에 등록되어 있고, 게시된 사이트나 프로덕션 산출물에 포함되어서는 안 됩니다.

---

## 기술 스택

- 단일 파일 React 애플리케이션 (사전 번들)
- Tailwind CSS (유틸리티 클래스 인라인)
- 완전 정적 — 모든 정적 호스트에서 동작, Cloudflare Pages / CDN에 최적화
- 애플리케이션 내부에서 한국어 / 영어 이중 언어 지원

---

## 로컬 미리보기

사이트가 단일 정적 HTML 파일이므로 다음과 같이 간단히 확인할 수 있습니다.

```bash
# Python
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
큰 용량의 자체 완결형 `index.html`은 설정 없는 정적 호스팅을 위해 의도적으로 설계되었습니다.

---

## 문의

- Email: [magnox@nate.com](mailto:magnox@nate.com)
- LinkedIn: [magnox-netnox](https://www.linkedin.com/in/magnox-netnox-a856443a)

---

## 라이선스

MIT — [LICENSE](LICENSE) 참고.
