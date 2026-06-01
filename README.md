# 사무실 레이아웃 편집기 PWA

사무실 레이아웃을 2D로 편집하고 3D로 확인할 수 있는 단일 HTML 기반 PWA입니다.

## GitHub Pages 배포

1. 이 폴더를 GitHub 저장소의 루트로 커밋합니다.
2. 저장소의 `Settings > Pages`에서 `Source`를 `GitHub Actions`로 설정합니다.
3. `main` 브랜치에 push하면 `.github/workflows/pages.yml` 워크플로가 자동 배포합니다.

## PWA 구성 파일

- `index.html`: 앱 본문과 PWA 메타 태그
- `manifest.json`: 설치형 앱 이름, 색상, 아이콘 설정
- `service-worker.js`: 앱 쉘 캐시와 오프라인 기본 동작
- `icons/icon-192.png`, `icons/icon-512.png`: PWA 설치 아이콘
- `.nojekyll`: GitHub Pages에서 정적 파일을 그대로 제공하기 위한 파일

## 로컬 확인

PWA의 서비스 워커는 `file://`보다 로컬 서버 또는 GitHub Pages 같은 HTTPS 환경에서 제대로 동작합니다.

```powershell
python -m http.server 8080
```

브라우저에서 `http://localhost:8080`으로 접속해 확인합니다.
