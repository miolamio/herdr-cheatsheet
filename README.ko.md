# Herdr 치트시트

> [English](README.md) · **한국어**

[Herdr](https://herdr.dev/docs/)의 자주 쓰는 단축키와 CLI 명령을 한 장에 모은, 인쇄에 적합한 단일 파일 치트시트입니다: 패널 분할, 탭, 워크스페이스, 세션, 에이전트, 그리고 Herdr를 전역 설치하고 공식 [SKILL.md](https://github.com/ogulcancelik/herdr/blob/master/SKILL.md)를 가져오는 복붙용 **에이전트 설정 프롬프트**까지 담았습니다.

`index.html`을 직접 열거나, GitHub Pages 사이트를 방문하세요 → https://cskwork.github.io/herdr-cheatsheet/

## 구성

- **Install** 블록: curl / brew / mise / Windows 한 줄 설치 명령.
- **에이전트 설정 프롬프트**: 프롬프트 하나로 Herdr를 전역 설치하고 코딩 에이전트에게 CLI 사용법을 학습시킵니다.
- **Prefix 단축키**: 패널(세로/가로 분할, 닫기, 확대, 크기 조절, 교체), 탭(생성, 다음/이전, 1~9 전환, 이름 변경, 닫기), 워크스페이스(선택기, 생성, 이름 변경, 닫기, worktree), 세션(분리, 사이드바, 복사 모드, 도움말).
- **CLI 핵심 명령**: launch, server, session, workspace, tab, pane, agent, wait, update.
- **에이전트 상태**: blocked / working / done / idle / unknown.

## 기능

- 키캡이나 명령을 클릭하면 클립보드로 복사됩니다.
- 모든 명령을 가로지르는 실시간 검색(한/영 어느 쪽으로 입력해도 매칭).
- 인쇄 스타일시트(2단 레이아웃, 불필요한 UI 제거).
- 빌드 과정 없는 단일 자체 완결 `index.html`. Google Fonts로 Geist + JetBrains Mono 사용.
- **한국어/영어 토글**: 우상단 KO/EN 스위치. 첫 방문 시 브라우저 언어를 자동 감지하고, 선택은 `localStorage`에 저장되어 다음 방문에도 유지됩니다.

## 로컬 미리보기

```sh
python3 -m http.server 8000
# http://localhost:8000 열기
```

## GitHub Pages

이 저장소는 `main` 브랜치 루트에서 GitHub Pages로 서빙되도록 설정되어 있습니다(`.nojekyll` 포함). 저장소 Settings에서 Pages를 활성화하거나 `gh`로 설정합니다:

```sh
gh repo create herdr-cheatsheet --public --source=. --push
gh api -X POST /repos/<user>/herdr-cheatsheet/pages -f "build_type=workflow" \
  -f "source[branch]=main" -f "source[path]=/"
```

배포된 사이트: https://cskwork.github.io/herdr-cheatsheet/

Herdr와 제휴 관계 없음. 공식 문서를 바탕으로 제작.
