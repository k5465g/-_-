# 리:듬 랜딩페이지 배포 가이드

이 폴더는 순수 정적 HTML(스크립트/스타일 인라인)이라 빌드 과정이 필요 없습니다.

## 1. assets 이미지 채우기
`assets/` 폴더에 아래 파일명 그대로 넣어주세요 (Claude Design에서 만들 때 쓰던 스크린샷들):
- flow1.png ~ flow6.png

없으면 갤러리 섹션 이미지가 깨진 채로 보입니다.

## 2. GitHub에 올리기
```
git init
git add .
git commit -m "리듬 랜딩페이지"
git branch -M main
git remote add origin <본인 GitHub 저장소 URL>
git push -u origin main
```

## 3. Vercel에 배포
1. vercel.com 로그인 → New Project
2. 방금 만든 GitHub 저장소 선택 → Import
3. Framework Preset: **Other** (또는 "No framework") 선택 — 빌드 커맨드 없음, Output Directory는 루트(`.`)
4. Deploy 클릭 끝

Cursor나 Claude Code 플러그인, MCP 연동 없이도 이 3단계만으로 배포됩니다. 저 도구들은 "코드를 수정하면서 배포까지 자동화하고 싶을 때" 쓰는 개발 워크플로우 도구이지, 정적 사이트 배포의 필수 조건이 아닙니다.
