# myblog 작업 워크플로우

## 구조

```
hyojunjung.github.io 레포
├── main 브랜치     → Hugo 소스 (내가 편집하는 파일들)
└── gh-pages 브랜치 → 빌드된 HTML (GitHub Actions가 자동 관리)
```

## 글/내용 수정할 때

1. `/Volumes/macmini_sharing/02-AREAS/myblog/content/` 안에서 md 파일 수정
2. 터미널에서:

```bash
cd /Volumes/macmini_sharing/02-AREAS/myblog
git add -A
git commit -m "수정 내용 간단히 설명"
git push
```

3. GitHub Actions가 자동으로 빌드 + 배포 (약 1-2분 소요)
4. https://hyojunjung.github.io 에서 확인

## 주요 폴더

| 폴더 | 역할 |
|------|------|
| `content/` | 마크다운 글 파일들 (여기만 편집) |
| `static/` | 이미지, PDF 등 정적 파일 |
| `themes/PaperMod/` | 테마 (건드리지 않음) |
| `public/` | 빌드 결과물 (자동 생성, 건드리지 않음) |
| `.github/workflows/` | GitHub Actions 설정 (건드리지 않음) |

## 로컬 미리보기 (선택)

```bash
cd /Volumes/macmini_sharing/02-AREAS/myblog
hugo server
# → http://localhost:1313 에서 확인
```

## 주의사항

- `gh-pages` 브랜치는 직접 편집하지 않음 (자동 관리)
- push 후 사이트 반영까지 1-2분 걸림
- GitHub Actions 실행 상태 확인: https://github.com/hyojunjung/hyojunjung.github.io/actions
